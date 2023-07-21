# Accelerator Log

## Options
```json
{
  "bsGitBranch" : "main",
  "bsGitRepository" : "github.com?owner=tanzu-demo&repo=bar-processor",
  "eventProcessRole" : true,
  "eventSinkRole" : false,
  "eventSourceRole" : false,
  "groupId" : "com.example",
  "includeBuildToolWrapper" : true,
  "liveUpdateIDESupport" : true,
  "mainClassName" : "StreamApplication",
  "msgBrokerName" : "stream-sample-message-broker",
  "objectModelClassName" : "Foo",
  "packageName" : "com.example.tanzu.streamtemplate",
  "projectName" : "bar-processor",
  "resultChannel" : "foo-result",
  "sourceChannel" : "foo-source",
  "sourceChannelGroup" : "foo-source-group"
}
```
## Log
```
┏ engine (Chain)
┃  Info Running Chain(GeneratorValidationTransform, UniquePath)
┃ ┏ ┏ engine.transformations[0].validated (Combo)
┃ ┃ ┃  Info Combo running as Let
┃ ┃ ┃ engine.transformations[0].validated.delegate (Let)
┃ ┃ ┃ Debug Adding symbol packageDirectory with value 'com/example/tanzu/streamtemplate'
┃ ┃ ┃ Debug Adding symbol workloadResourceName with value 'bar-processor'
┃ ┃ ┃ Debug Adding symbol lambaObjectPlural with value 'foos'
┃ ┃ ┃ Debug Adding symbol lambaObjectSingleton with value 'foo'
┃ ┃ ┃ Debug Adding symbol bindingName with value 'foo'
┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in (Chain)
┃ ┃ ┃ ┃  Info Running Chain(Combo, Combo, Combo, Combo, Combo)
┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0] (Combo)
┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[0].delegate (Chain)
┃ ┃ ┃ ┃ ┃  Info Running Chain(Merge, UniquePath)
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0] (Merge)
┃ ┃ ┃ ┃ ┃ ┃  Info Running Merge(Combo, Combo, Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[0] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[0].delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, Exclude)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[0].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [**]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug catalog/catalog-info.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplication.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSink.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSource.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/resources/application.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplicationTests.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug templates/application.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[0].delegate.transformations[1] (Exclude)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will exclude [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE didn't match [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug catalog/catalog-info.yaml matched [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml didn't match [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml matched [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplication.java didn't match [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java didn't match [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSink.java didn't match [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSource.java didn't match [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java didn't match [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/resources/application.yaml didn't match [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplicationTests.java didn't match [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┗ ┗ Debug templates/application.yaml matched [pom.xml, **/templates/application.yaml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[1] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[1].delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[1].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [pom.xml, **/catalog/catalog-info.yaml]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [pom.xml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE didn't match [pom.xml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [pom.xml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug catalog/catalog-info.yaml matched [pom.xml, **/catalog/catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml didn't match [pom.xml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml matched [pom.xml, **/catalog/catalog-info.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplication.java didn't match [pom.xml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java didn't match [pom.xml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSink.java didn't match [pom.xml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSource.java didn't match [pom.xml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java didn't match [pom.xml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/resources/application.yaml didn't match [pom.xml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplicationTests.java didn't match [pom.xml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug templates/application.yaml didn't match [pom.xml, **/catalog/catalog-info.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[1].delegate.transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┗ ┗  Info Will replace [<groupId>com.example</groupId>-><groupId>com.example...(truncated), streaming-app-template->bar-processor, <groupId>streaming-app-template</groupId>-><groupId>bar-process...(truncated)]
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[2] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[2].delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, ReplaceText, YTT, RewritePath)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[2].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [**/templates/application.yaml]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [**/templates/application.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE didn't match [**/templates/application.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [**/templates/application.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug catalog/catalog-info.yaml didn't match [**/templates/application.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml didn't match [**/templates/application.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml didn't match [**/templates/application.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplication.java didn't match [**/templates/application.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java didn't match [**/templates/application.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSink.java didn't match [**/templates/application.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSource.java didn't match [**/templates/application.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java didn't match [**/templates/application.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/resources/application.yaml didn't match [**/templates/application.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplicationTests.java didn't match [**/templates/application.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug templates/application.yaml matched [**/templates/application.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[2].delegate.transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [Foo->Foo]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[2].delegate.transformations[2] (YTT)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug Wrote values file with json content:   {"msgBrokerName":"stream-sample-message-broker","resultChannel":"foo-result","bsGitBranch":"main","artifactVersion":"0.0.1-beta","workloadResourceName":"bar-processor","sourceChannel":"foo-source","bsGitRepository":"github.com?owner=tanzu-demo&repo=bar-processor","groupId":"com.example","bindingName":"foo","eventSinkRole":false,"eventSourceRole":false,"liveUpdateIDESupport":true,"includeBuildToolWrapper":true,"lambaObjectPlural":"foos","artifactId":"bar-processor","mainClassName":"StreamApplication","packageName":"com.example.tanzu.streamtemplate","packageDirectory":"com/example/tanzu/streamtemplate","objectModelClassName":"Foo","projectName":"bar-processor","eventProcessRole":true,"lambaObjectSingleton":"foo","sourceChannelGroup":"foo-source-group"}
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗  Info Shelling out to YTT with args: [ytt, -f, /tmp/ytt-input4793701794213163296, --data-values-file, /tmp/accelerator-options8070433766808939984.json, --output-files, /tmp/ytt-output8320571092843834552]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[0].sources[2].delegate.transformations[3] (RewritePath)
┃ ┃ ┃ ┃ ┃ ┗ ┗ ┗ Debug Path 'templates/application.yaml' matched 'templates/application.yaml' with groups {g0=templates/application.yaml} and was rewritten to 'src/main/resources/application.yaml'
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[0].delegate.transformations[1] (UniquePath)
┃ ┃ ┃ ┃ ┗ ┗ Debug Multiple representations for path 'src/main/resources/application.yaml', will use the one appearing last 
┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1] (Combo)
┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[1].delegate (Chain)
┃ ┃ ┃ ┃ ┃  Info Running Chain(Merge, UniquePath)
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0] (Merge)
┃ ┃ ┃ ┃ ┃ ┃  Info Running Merge(Combo, Combo, Combo, Combo, Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[0] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Exclude
┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[0].delegate (Exclude)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will exclude [**/*.java]
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [**/*.java] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplicationTests.java matched [**/*.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSource.java matched [**/*.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplication.java matched [**/*.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java matched [**/*.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml didn't match [**/*.java] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug catalog/catalog-info.yaml didn't match [**/*.java] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [**/*.java] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml didn't match [**/*.java] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java matched [**/*.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSink.java matched [**/*.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE didn't match [**/*.java] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug src/main/resources/application.yaml didn't match [**/*.java] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[1] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[1].delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, ReplaceText, ReplaceText, ReplaceText, RewritePath, RewritePath, RewritePath, RewritePath)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[1].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplicationTests.java matched [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSource.java didn't match [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplication.java matched [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java matched [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml didn't match [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug catalog/catalog-info.yaml didn't match [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml didn't match [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java didn't match [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSink.java didn't match [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE didn't match [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug src/main/resources/application.yaml didn't match [**/StreamingAppTemplateApplicationTests.java, **/StreamingAppTemplateApplication.java, **/Foo.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[1].delegate.transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [com.example.tanzu.streamtemplate->com.example.tanzu.st...(truncated)]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[1].delegate.transformations[2] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [StreamingAppTemplateApplication->StreamApplication]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[1].delegate.transformations[3] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [Foo->Foo]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[1].delegate.transformations[4] (RewritePath)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug Path 'src/test/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplicationTests.java' matched 'src/(?<sourceset>.*)/java/(?<currentpackage>.*/)streamtemplate/StreamingAppTemplateApplicationTests.java' with groups {sourceset=test, currentpackage=com/example/tanzu/, g0=src/test/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplicationTests.java, g1=test, g2=com/example/tanzu/} and was rewritten to 'src/test/java/com/example/tanzu/streamtemplate/StreamApplicationTests.java'
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[1].delegate.transformations[5] (RewritePath)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug Path 'src/main/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplication.java' matched 'src/(?<sourceset>.*)/java/(?<currentpackage>.*/)streamtemplate/StreamingAppTemplateApplication.java' with groups {sourceset=main, currentpackage=com/example/tanzu/, g0=src/main/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplication.java, g1=main, g2=com/example/tanzu/} and was rewritten to 'src/main/java/com/example/tanzu/streamtemplate/StreamApplication.java'
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[1].delegate.transformations[6] (RewritePath)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug Path 'src/main/java/com/example/tanzu/streamtemplate/model/Foo.java' matched 'src/(?<sourceset>.*)/java/(?<currentpackage>.*/)streamtemplate/model/Foo.java' with groups {sourceset=main, currentpackage=com/example/tanzu/, g0=src/main/java/com/example/tanzu/streamtemplate/model/Foo.java, g1=main, g2=com/example/tanzu/} and was rewritten to 'src/main/java/com/example/tanzu/streamtemplate/model/Foo.java'
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[1].delegate.transformations[7] (RewritePath)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug Path 'src/test/java/com/example/tanzu/streamtemplate/StreamApplicationTests.java' matched 'src/(?<sourceset>.*)/java/(?<currentpackage>.*/)streamtemplate(?<untouchedpath>.*)' with groups {sourceset=test, currentpackage=com/example/tanzu/, untouchedpath=/StreamApplicationTests.java, g0=src/test/java/com/example/tanzu/streamtemplate/StreamApplicationTests.java, g1=test, g2=com/example/tanzu/, g3=/StreamApplicationTests.java} and was rewritten to 'src/test/java/com/example/tanzu/streamtemplate//StreamApplicationTests.java'
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug Path 'src/main/java/com/example/tanzu/streamtemplate/StreamApplication.java' matched 'src/(?<sourceset>.*)/java/(?<currentpackage>.*/)streamtemplate(?<untouchedpath>.*)' with groups {sourceset=main, currentpackage=com/example/tanzu/, untouchedpath=/StreamApplication.java, g0=src/main/java/com/example/tanzu/streamtemplate/StreamApplication.java, g1=main, g2=com/example/tanzu/, g3=/StreamApplication.java} and was rewritten to 'src/main/java/com/example/tanzu/streamtemplate//StreamApplication.java'
┃ ┃ ┃ ┃ ┃ ┃ ┗ ┗ Debug Path 'src/main/java/com/example/tanzu/streamtemplate/model/Foo.java' matched 'src/(?<sourceset>.*)/java/(?<currentpackage>.*/)streamtemplate(?<untouchedpath>.*)' with groups {sourceset=main, currentpackage=com/example/tanzu/, untouchedpath=/model/Foo.java, g0=src/main/java/com/example/tanzu/streamtemplate/model/Foo.java, g1=main, g2=com/example/tanzu/, g3=/model/Foo.java} and was rewritten to 'src/main/java/com/example/tanzu/streamtemplate//model/Foo.java'
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[2] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Condition (#eventSourceRole) evaluated to false
┃ ┃ ┃ ┃ ┃ ┃ ┗ null ()
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[3] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Condition (#eventProcessRole) evaluated to true
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[3].delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, ReplaceText, ReplaceText, ReplaceText, ReplaceText, RewritePath)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[3].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [**/FooProcessor.java]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [**/FooProcessor.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplicationTests.java didn't match [**/FooProcessor.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSource.java didn't match [**/FooProcessor.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamingAppTemplateApplication.java didn't match [**/FooProcessor.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java didn't match [**/FooProcessor.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml didn't match [**/FooProcessor.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug catalog/catalog-info.yaml didn't match [**/FooProcessor.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [**/FooProcessor.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml didn't match [**/FooProcessor.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java matched [**/FooProcessor.java] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooSink.java didn't match [**/FooProcessor.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE didn't match [**/FooProcessor.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug src/main/resources/application.yaml didn't match [**/FooProcessor.java] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[3].delegate.transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [com.example.tanzu.streamtemplate->com.example.tanzu.st...(truncated)]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[3].delegate.transformations[2] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [Foo->Foo]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[3].delegate.transformations[3] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [foos->foos]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[3].delegate.transformations[4] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗  Info Will replace [foo->foo]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[3].delegate.transformations[5] (RewritePath)
┃ ┃ ┃ ┃ ┃ ┃ ┗ ┗ Debug Path 'src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java' matched 'src/(?<sourceset>.*)/java/(?<currentpackage>.*/)streamtemplate/functions/FooProcessor.java' with groups {sourceset=main, currentpackage=com/example/tanzu/, g0=src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java, g1=main, g2=com/example/tanzu/} and was rewritten to 'src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java'
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[0].sources[4] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Condition (#eventSinkRole) evaluated to false
┃ ┃ ┃ ┃ ┃ ┗ ┗ null ()
┃ ┃ ┃ ┃ ┗ ╺ engine.transformations[0].validated.delegate.in.transformations[1].delegate.transformations[1] (UniquePath)
┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[2] (Combo)
┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[2].delegate (Chain)
┃ ┃ ┃ ┃ ┃  Info Running Chain(Merge, UniquePath)
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[2].delegate.transformations[0] (Merge)
┃ ┃ ┃ ┃ ┃ ┃  Info Running Merge(Combo, Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[2].delegate.transformations[0].sources[0] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Exclude
┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[2].delegate.transformations[0].sources[0].delegate (Exclude)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will exclude [config/workload.yaml]
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml matched [config/workload.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [config/workload.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java didn't match [config/workload.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java didn't match [config/workload.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamApplicationTests.java didn't match [config/workload.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamApplication.java didn't match [config/workload.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/resources/application.yaml didn't match [config/workload.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE didn't match [config/workload.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml didn't match [config/workload.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [config/workload.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug catalog/catalog-info.yaml didn't match [config/workload.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[2].delegate.transformations[0].sources[1] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[2].delegate.transformations[0].sources[1].delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, YTT)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[2].delegate.transformations[0].sources[1].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [config/workload.yaml]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml matched [config/workload.yaml] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [config/workload.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java didn't match [config/workload.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java didn't match [config/workload.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamApplicationTests.java didn't match [config/workload.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamApplication.java didn't match [config/workload.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/resources/application.yaml didn't match [config/workload.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE didn't match [config/workload.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml didn't match [config/workload.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [config/workload.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug catalog/catalog-info.yaml didn't match [config/workload.yaml] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[2].delegate.transformations[0].sources[1].delegate.transformations[1] (YTT)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug Wrote values file with json content:   {"msgBrokerName":"stream-sample-message-broker","resultChannel":"foo-result","bsGitBranch":"main","artifactVersion":"0.0.1-beta","workloadResourceName":"bar-processor","sourceChannel":"foo-source","bsGitRepository":"github.com?owner=tanzu-demo&repo=bar-processor","groupId":"com.example","bindingName":"foo","eventSinkRole":false,"eventSourceRole":false,"liveUpdateIDESupport":true,"includeBuildToolWrapper":true,"lambaObjectPlural":"foos","artifactId":"bar-processor","mainClassName":"StreamApplication","packageName":"com.example.tanzu.streamtemplate","packageDirectory":"com/example/tanzu/streamtemplate","objectModelClassName":"Foo","projectName":"bar-processor","eventProcessRole":true,"lambaObjectSingleton":"foo","sourceChannelGroup":"foo-source-group"}
┃ ┃ ┃ ┃ ┃ ┗ ┗ ┗  Info Shelling out to YTT with args: [ytt, -f, /tmp/ytt-input13128774740939397734, --data-values-file, /tmp/accelerator-options17046851197658230519.json, --output-files, /tmp/ytt-output12897502506690826745]
┃ ┃ ┃ ┃ ┗ ╺ engine.transformations[0].validated.delegate.in.transformations[2].delegate.transformations[1] (UniquePath)
┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[3] (Combo)
┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[3].delegate (Chain)
┃ ┃ ┃ ┃ ┃  Info Running Chain(Merge, UniquePath)
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0] (Merge)
┃ ┃ ┃ ┃ ┃ ┃  Info Running Merge(InvokeFragment, Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[0] (InvokeFragment)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[0].validated (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[0].validated.delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Merge, UniquePath)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[0].validated.delegate.transformations[0] (Merge)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Merge(Combo, Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[0].validated.delegate.transformations[0].sources[0] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Condition (#liveUpdateIDESupport) evaluated to true
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[0].validated.delegate.transformations[0].sources[0].delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[0].validated.delegate.transformations[0].sources[0].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [Tiltfile]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamApplicationTests.java didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamApplication.java didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/resources/application.yaml didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug catalog/catalog-info.yaml didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug DEPLOYING.md didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [Tiltfile] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug Tiltfile matched [Tiltfile] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[0].validated.delegate.transformations[0].sources[0].delegate.transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ ┗  Info Will replace [my-project->bar-processor]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[0].validated.delegate.transformations[0].sources[1] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Condition (#liveUpdateIDESupport) evaluated to true
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[0].validated.delegate.transformations[0].sources[1].delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Include, ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[0].validated.delegate.transformations[0].sources[1].delegate.transformations[0] (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [DEPLOYING.md]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml didn't match [DEPLOYING.md] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [DEPLOYING.md] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java didn't match [DEPLOYING.md] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java didn't match [DEPLOYING.md] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamApplicationTests.java didn't match [DEPLOYING.md] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamApplication.java didn't match [DEPLOYING.md] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml didn't match [DEPLOYING.md] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE didn't match [DEPLOYING.md] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/resources/application.yaml didn't match [DEPLOYING.md] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug catalog/catalog-info.yaml didn't match [DEPLOYING.md] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [DEPLOYING.md] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug DEPLOYING.md matched [DEPLOYING.md] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [DEPLOYING.md] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug Tiltfile didn't match [DEPLOYING.md] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[0].validated.delegate.transformations[0].sources[1].delegate.transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ ┗ ┗  Info Will replace [my-project->bar-processor]
┃ ┃ ┃ ┃ ┃ ┃ ┗ ┗ ╺ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[0].validated.delegate.transformations[1] (UniquePath)
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[1] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Include
┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[0].sources[1].delegate (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [**]
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamApplicationTests.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamApplication.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/resources/application.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug catalog/catalog-info.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┗ ┗ Debug README.md matched [**] -> included
┃ ┃ ┃ ┃ ┗ ╺ engine.transformations[0].validated.delegate.in.transformations[3].delegate.transformations[1] (UniquePath)
┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[4] (Combo)
┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[4].delegate (Chain)
┃ ┃ ┃ ┃ ┃  Info Running Chain(Merge, UniquePath)
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0] (Merge)
┃ ┃ ┃ ┃ ┃ ┃  Info Running Merge(InvokeFragment, Combo, InvokeFragment, Provenance)
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[0] (InvokeFragment)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[0].validated (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Condition (#bsGitRepository != null) evaluated to true
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Let
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[0].validated.delegate (Let)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug Adding symbol repoUrl with value 'https://github.com?owner=tanzu-demo&repo=bar-processor'
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[0].validated.delegate.in (Chain)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(OpenRewriteRecipe, ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ╺ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[0].validated.delegate.in.transformations[0] (OpenRewriteRecipe)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[0].validated.delegate.in.transformations[1] (ReplaceText)
┃ ┃ ┃ ┃ ┃ ┃ ┗ ┗ ┗ ┗  Info Will replace regex '(?<beforeBranch>[\s\S]+)(?<branch>branch: [\S]+)(?<rest>[\S\s]*)' with '${beforeBranch}branc...(truncated)'
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[1] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Include
┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[1].delegate (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [**]
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug Tiltfile matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug DEPLOYING.md matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamApplicationTests.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamApplication.java matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/resources/application.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┗ Debug catalog/catalog-info.yaml matched [**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[2] (InvokeFragment)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[2].validated (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Chain
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[2].validated.delegate (Chain)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Chain(Merge, UniquePath)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[2].validated.delegate.transformations[0] (Merge)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Running Merge(Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[2].validated.delegate.transformations[0].sources[0] (Combo)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Condition (#includeBuildToolWrapper) evaluated to true
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Combo running as Include
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[2].validated.delegate.transformations[0].sources[0].delegate (Include)
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃  Info Will include [mvnw, mvnw.cmd, .mvn/**]
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug config/workload.yaml didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .gitignore didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug Tiltfile didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug DEPLOYING.md didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/model/Foo.java didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/test/java/com/example/tanzu/streamtemplate/StreamApplicationTests.java didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/java/com/example/tanzu/streamtemplate/StreamApplication.java didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug src/main/resources/application.yaml didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug LICENSE didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug pom.xml didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug catalog/catalog-info.yaml didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug .mvn/wrapper/maven-wrapper.properties matched [mvnw, mvnw.cmd, .mvn/**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug README.md didn't match [mvnw, mvnw.cmd, .mvn/**] -> excluded
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ Debug mvnw matched [mvnw, mvnw.cmd, .mvn/**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┃ ┃ ┗ ┗ Debug mvnw.cmd matched [mvnw, mvnw.cmd, .mvn/**] -> included
┃ ┃ ┃ ┃ ┃ ┃ ┗ ┗ ╺ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[2].validated.delegate.transformations[1] (UniquePath)
┃ ┃ ┃ ┃ ┃ ┗ ╺ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[0].sources[3] (Provenance)
┃ ┃ ┃ ┃ ┃ ┏ engine.transformations[0].validated.delegate.in.transformations[4].delegate.transformations[1] (UniquePath)
┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path '.gitignore', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'src/main/java/com/example/tanzu/streamtemplate/model/Foo.java', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'pom.xml', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'src/main/resources/application.yaml', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'catalog/catalog-info.yaml', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'README.md', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'config/workload.yaml', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'src/main/java/com/example/tanzu/streamtemplate/functions/FooProcessor.java', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'Tiltfile', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'DEPLOYING.md', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'src/test/java/com/example/tanzu/streamtemplate/StreamApplicationTests.java', will use the one appearing first 
┃ ┃ ┃ ┃ ┃ ┃ Debug Multiple representations for path 'src/main/java/com/example/tanzu/streamtemplate/StreamApplication.java', will use the one appearing first 
┃ ┗ ┗ ┗ ┗ ┗ Debug Multiple representations for path 'LICENSE', will use the one appearing first 
┗ ╺ engine.transformations[1] (UniquePath)
```
