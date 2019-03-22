Serverless for netcoreapp2.1 (dotnet)

export aws keys as environment variables
```
export AWS_ACCESS_KEY_ID=<your-key-here>
export AWS_SECRET_ACCESS_KEY=<your-secret-key-here>
```

Creating AWS Access Keys
`https://serverless.com/framework/docs/providers/aws/guide/credentials#creating-aws-access-keys`

Controller folder is for webapi
Services folder is for functions

Build
`run build.[sh/ps1]` 
or
```
dotnet restore
dotnet lambda package --configuration release --framework netcoreapp2.1 --output-package bin/release/netcoreapp2.1/deploy-package.zip
```
Deploy
`sls deploy -v `

Invoke a function
`sls invoke -f hello --data '{"Key1": 1, "Key2": 2, "Key3": 3}'`

Logs: check on cloudwatch or use `sls logs -f <function name>`


TODO: add unit test framework and CI/CD