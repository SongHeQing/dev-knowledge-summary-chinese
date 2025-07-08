# 知识总结

Java
结论
Service 层返回业务对象（Entity/DTO），不返回 VO，会阻碍聚合Service。  
这样既保证了分层清晰，又方便聚合和复用业务逻辑。  
Entity必须和表结构一一对应，  
Controller 层尽量不返回Entity，会暴露表结构，可以返回DTO/VO。  
Mpaaer层可以接收返回 Entity/DTO  
VO 转换放在 Controller 层，使用 MapStruct 等工具自动转换。  
