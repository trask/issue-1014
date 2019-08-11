Repro

* Update instrumentation key in `application.properties`
* Build: `mvn clean package`
* Run: `java -jar target/app.jar`
* Go to: http://localhost:8080/hello

Check log for sending telemetry of type Message with text "this is an warn message", e.g.

`AI: TRACE 11-08-2019 20:06:15.204+0000, 27(http-nio-8080-exec-1): InProcessTelemetryChannel sending telemetry: {"ver":1,"name":"Microsoft.ApplicationInsights.00000000000000000000000000000000.Message","time":"2019-08-11T13:06:10.690-0700","sampleRate":100.0,"iKey":"00000000-0000-0000-0000-000000000000","tags":{"ai.internal.sdkVersion":"java:2.3.1","ai.device.id":"MININT-PLOJ2RD.redmond.corp.microsoft.com","ai.device.locale":"en-US","ai.internal.nodeName":"MININT-PLOJ2RD.redmond.corp.microsoft.com","ai.operation.id":"8a093ba085844d1ebceeac129527a859","ai.cloud.roleInstance":"MININT-PLOJ2RD.redmond.corp.microsoft.com","ai.operation.name":"GET HelloController\/index","ai.cloud.role":"Issue 1014","ai.device.osVersion":"Windows 10","ai.operation.parentId":"|8a093ba085844d1ebceeac129527a859.","ai.session.isFirst":"false","ai.device.os":"Windows 10","ai.user.userAgent":"Mozilla\/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit\/537.36 (KHTML, like Gecko) Chrome\/76.0.3809.100 Safari\/537.36"},"data":{"baseType":"MessageData","baseData":{"ver":2,"message":"this is an warn message","severityLevel":"Warning","properties":{"LoggerName":"issue1014.HelloController","LoggingLevel":"WARN","SourceType":"LOGBack","ThreadName":"http-nio-8080-exec-1","DeveloperMode":"true","TimeStamp":"Sun, 11 Aug 2019 13:06:10 GMT"}}}}`
