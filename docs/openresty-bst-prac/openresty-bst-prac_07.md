# LuaRestyLock

# lock

# 缓存失效风暴

看下这个段伪代码：

```
local value = get_from_cache(key)
if not value then
    value = query_db(sql)
    set_to_cache(value， timeout ＝ 100)
end
return value 
```

看上去没有问题，在单元测试情况下，也不会有异常。

但是，进行压力测试的时候，你会发现，每隔 100 秒，数据库的查询就会出现一次峰值。如果你的 cache 失效时间设置的比较长，那么这个问题被发现的机率就会降低。

为什么会出现峰值呢？想象一下，在 cache 失效的瞬间，如果并发请求有 1000 条同时到了 `query_db(sql)` 这个函数会怎样？没错，会有 1000 个请求打向数据库。这就是缓存失效瞬间引起的风暴。它有一个英文名，叫 **"dog-pile effect"**。

怎么解决？自然的想法是发现缓存失效后，加一把锁来控制数据库的请求。具体的细节，春哥在 lua-resty-lock 的文档里面做了详细的说明，我就不重复了，请看[这里](https://github.com/openresty/lua-resty-lock#for-cache-locks)。多说一句，lua-resty-lock 库本身已经替你完成了 wait for lock 的过程，看代码的时候需要注意下这个细节。