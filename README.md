````
> OPEN API-3 WITH SPRINGBOOT:
https://www.dariawan.com/tutorials/spring/documenting-spring-boot-rest-api-springdoc-openapi-3/
One can follow above to obtain a Swagger API.


> GENERATING SDK APART FROM SWAGGER DOCUMENTATION:
Open API 3 Generators: 
https://openapi-generator.tech/docs/generators

1-) npm install @openapitools/openapi-generator-cli -g
2-) npx openapi-generator generate -i https://r2g.api.dev.services.rd2g.de/v3/api-docs -g typescript-axios -o ./
3-) Enums are generated in typescript 2.4.4 version. We need to normalize them to typescript 2.3.3.  
    Todo so in api.ts use replace regex as follow:
    Find with: (.*)( = '\w+')(,*)
    Relace by: $1$3
    
4-) tsc --declaration --sourceMap index.ts configuration.ts base.ts api.ts 

API client source will be generated following above steps. 

To make this as a library, one can follow below tutorial:
https://www.tsmean.com/articles/how-to-write-a-typescript-library/


