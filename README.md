
**设计模式总结**

1、工厂模式(Factory)：创建对象的车间  
2、单例模式(Singleton)：只创建一次，之后每次创建，返回同一个对象  
3、原型模式(Prototype)：克隆对象  
4、代理模式(Proxy)：中介，增强  
5、委派模式(Delegate)：分派调度  
6、策略模式(Strategy)：多种解决方案可以调用  
7、模板模式(Template)：流程  
8、适配器模式(Adapter)：扩展，覆盖  
9、装饰器模式(Decorator)：包装  
10、观察者模式(Observer)：通知  

**SpringAop**

@Aspect
public class Aop {

	@Pointcut("execution(* com.gupao.springcode.service..*.*(..))")
	public void pointcut(){}

	@Before("pointcut()")
	public void before(){
		System.out.println("before");
	}

	@After("pointcut()")
	public void after(){
		System.out.println("after");
	}

	@Around("pointcut")
	public void arond(){
		System.out.println("rond");
	}

	@AfterThrowing(pointcut="pointcut()",throwing="error")
	public void throwsExpetction(){
		System.out.println("throwsExpetction");
	}
}

**IOC**  
@Autowired
private UserService userService;

**DI**  
@Resource("userService")
public private UserService userService;