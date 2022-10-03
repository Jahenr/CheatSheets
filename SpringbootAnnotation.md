@Configuration 
        This annotation marks a class as a Configuration class for Java-based configuration.

@ComponentScan 
         This annotation enables component-scanning so that the web controller classes and other components you create will be automatically discovered and registered as beans in Spring's Application Context. All the@Controller classes you write are discovered by this annotation.

@EnableAutoConfiguration
        This annotation enables the magical auto-configuration feature of Spring Boot, which can automatically configure a lot of stuff for you.

@SpringBootApplication
        @SpringBootApplication annotation indicates a configuration class that declares one or more @Bean methods and also triggers auto-configuration and component scanning.
        The @SpringBootApplication annotation is equivalent to using @Configuration, @EnableAutoConfiguration, and @ComponentScan with their default attributes.

@ConditionalOnClass and @ConditionalOnMissingClass
        These annotations belong to Class conditions. The @ConditionalOnClass and @ConditionalOnMissingClass annotations let configuration be included based on the presence or absence of specific classes.

@ConditionalOnBean Annotation
        The @ConditionalOnBean annotations let a bean be included based on the presence or absence of specific beans.Use when we want to define conditions based on the presence or absence of a specific bean.

@ConditionalOnMissingBean
        The @ConditionalOnMissingBean annotations let a bean be included based on the presence or absence of specific beans.When placed on a @Bean method, the target type defaults to the return type of the method

@ConditionalOnProperty
        The @ConditionalOnProperty annotation lets configuration be included based on a Spring Environment property.
        With this annotation, we can make conditions on the values of properties.

@ConditionalOnResource
        The @ConditionalOnResource annotation lets configuration be included only when a specific resource is present.

@ConditionalOnWebApplication and @ConditionalOnNotWebApplication
        The @ConditionalOnWebApplication and @ConditionalOnNotWebApplication annotations let configuration be included depending on whether the application is a “web application”. 
        A web application is an application that uses a Spring WebApplicationContext, defines a session scope, or has a StandardServletEnvironment.

@ConditionalExpression
        We can use this annotation in more complex situations. Spring will use the marked definition when the SpEL expression is evaluated to true.

@Conditional
        For even more complex conditions, we can create a class evaluating the custom condition. 
        We tell Spring to use this custom condition with @Conditional.

@ContextConfiguration
        This annotation specifies how to load the application context while writing a unit test for the Spring environment. Here is an example of using @ContextConfiguration along with @RunWith annotation of JUnit to test a Service class in Spring Boot.

@SpringApplicationConfiguration
        It provides full Spring Boot treatment to your test classes like it not only load the beans in the Spring application context but also enables logging and loads properties from application.properties file.

        Btw, you should always use @SpringApplicaitonConfiguration instead of @ContextConfigruation for writing unit tests in Spring boot.

@ConditionalOnJava
        The Configuration is applied if the version of Java matches a specific value or range of versions.

@Required
        It applies to the bean setter method. It indicates that the annotated bean must be populated at configuration time with the required property, else it throws an exception BeanInitilizationException.

@Autowired
        Spring provides annotation-based auto-wiring by providing @Autowired annotation. It is used to autowire spring bean on setter methods, instance variable, and constructor. When we use @Autowired annotation, the spring container auto-wires the bean by matching data-type.

@Bean
        It is a method-level annotation. It is an alternative of XML <bean> tag. It tells the method to produce a bean to be managed by Spring Container.

@Controller
        The @Controller is a class-level annotation. It is a specialization of @Component. It marks a class as a web request handler. It is often used to serve web pages. By default, it returns a string that indicates which route to redirect. It is mostly used with @RequestMapping annotation.

@Service
        It is also used at class level. It tells the Spring that class contains the business logic.

@RequestMapping
        It is used to map the web requests. It has many optional elements like consumes, header, method, name, params, path, produces, and value. We use it with the class as well as the method.

@GetMapping
        It maps the HTTP GET requests on the specific handler method. It is used to create a web service endpoint that fetches It is used instead of using: @RequestMapping(method = RequestMethod.GET).

@PostMapping
         It maps the HTTP POST requests on the specific handler method. It is used to create a web service endpoint that creates It is used instead of using: @RequestMapping(method = RequestMethod.POST).

@PutMapping
         It maps the HTTP PUT requests on the specific handler method. It is used to create a web service endpoint that creates or updates It is used instead of using: @RequestMapping(method = RequestMethod.PUT).

@DeleteMapping
        It maps the HTTP DELETE requests on the specific handler method. It is used to create a web service endpoint that deletes a resource. It is used instead of using: @RequestMapping(method = RequestMethod.DELETE).

@PatchMapping
         It maps the HTTP PATCH requests on the specific handler method. It is used instead of using: @RequestMapping(method = RequestMethod.PATCH).

@RequestBody
         It is used to bind HTTP request with an object in a method parameter. Internally it uses HTTP MessageConverters to convert the body of the request. When we annotate a method parameter with @RequestBody, the Spring framework binds the incoming HTTP request body to that parameter.

@ResponseBody
         It binds the method return value to the response body. It tells the Spring Boot Framework to serialize a return an object into JSON and XML format.

@PathVariable
         It is used to extract the values from the URI. It is most suitable for the RESTful web service, where the URL contains a path variable. We can define multiple @PathVariable in a method.

@RequestParam
         It is used to extract the query parameters form the URL. It is also known as a query parameter. It is most suitable for web applications. It can specify default values if the query parameter is not present in the URL.

@RequestHeader
         It is used to get the details about the HTTP request headers. We use this annotation as a method parameter. The optional elements of the annotation are name, required, value, defaultValue. For each detail in the header, we should specify separate annotations. We can use it multiple time in a method.

@RestController
         It can be considered as a combination of @Controller and @ResponseBody annotations. The @RestController annotation is itself annotated with the @ResponseBody annotation. It eliminates the need for annotating each method with @ResponseBody.
         
@RequestAttribute
         It binds a method parameter to request attribute. It provides convenient access to the request attributes from a controller method. With the help of @RequestAttribute annotation, we can access objects that are populated on the server-side.