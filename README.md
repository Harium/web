# Marine
A web framework over sparkjava

## Maven
```
<dependency>
    <groupId>com.harium.marine</groupId>
    <artifactId>core</artifactId>
    <version>1.0.0</version>
</dependency>
```

## Usage

Example using [dotenv](https://github.com/Harium/dotenv).
```
...
public class Main {

    public static void main(String[] args) {
        System.out.println("Starting Server");

        String host = Env.get("HOST");
        System.out.println(host);

        Web.port(Integer.parseInt(Env.get("PORT")));
        Web.host(host);

        Web.staticFileLocation("/public");

        // Register Web Modules
        Web.register(HealthCare.class);
        // Init Web Modules
        Web.init();
    }
}
```

## Need more information?
See examples