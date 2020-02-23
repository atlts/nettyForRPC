# nettyForRPC
  基于TCP数据包的通信以获得更高的效率
  
  使用Netty进行客户端与服务端之间的通信，简化了NIO的复杂的配置和epoll空轮询的问题
  
  利用Spring依赖注入，管理server，handler等bean
  
  使用了长连接，并将所有连接放入ConnetcManager中进行管理
  
  当调用时通过代理的方法，将请求发到服务端之后立刻异步RpcFuture，此对象中借鉴了线程池的submit方法，利用AQS同步器实现类似countDownLatch的功能
  
  实现了有callBacks和无callBacks两种异步阻塞调用
  
  
