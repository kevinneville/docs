
---
title: "getAppSecEvalHostnames"
title_tag: "akamai.getAppSecEvalHostnames"
meta_desc: "Documentation for the akamai.getAppSecEvalHostnames function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use the `akamai.AppSecEvalHostnames` data source to retrieve the evaluation hostnames for a configuration. Evaluation mode for hostnames is only available for Web Application Protector. Run hostnames in evaluation mode to see how your configuration settings protect traffic for that hostname before adding a hostname directly to a live configuration. An evaluation period lasts four weeks unless you stop the evaluation. Once you begin, the hostnames you evaluate start responding to traffic as if they are your current hostnames. However, instead of taking an action the evaluation hostnames log which action they would have taken if they were your actively-protected hostnames and not a test.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Akamai = Pulumi.Akamai;

class MyStack : Stack
{
    public MyStack()
    {
        var configuration = Output.Create(Akamai.GetAppSecConfiguration.InvokeAsync(new Akamai.GetAppSecConfigurationArgs
        {
            Name = @var.Security_configuration,
        }));
        var evalHostnamesAppSecEvalHostnames = configuration.Apply(configuration => Output.Create(Akamai.GetAppSecEvalHostnames.InvokeAsync(new Akamai.GetAppSecEvalHostnamesArgs
        {
            ConfigId = configuration.ConfigId,
        })));
        this.EvalHostnames = evalHostnamesAppSecEvalHostnames.Apply(evalHostnamesAppSecEvalHostnames => evalHostnamesAppSecEvalHostnames.Hostnames);
        this.EvalHostnamesOutput = evalHostnamesAppSecEvalHostnames.Apply(evalHostnamesAppSecEvalHostnames => evalHostnamesAppSecEvalHostnames.OutputText);
        this.EvalHostnamesJson = evalHostnamesAppSecEvalHostnames.Apply(evalHostnamesAppSecEvalHostnames => evalHostnamesAppSecEvalHostnames.Json);
    }

    [Output("evalHostnames")]
    public Output<string> EvalHostnames { get; set; }
    [Output("evalHostnamesOutput")]
    public Output<string> EvalHostnamesOutput { get; set; }
    [Output("evalHostnamesJson")]
    public Output<string> EvalHostnamesJson { get; set; }
}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-akamai/sdk/v2/go/akamai"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := _var.Security_configuration
		configuration, err := akamai.LookupAppSecConfiguration(ctx, &akamai.LookupAppSecConfigurationArgs{
			Name: &opt0,
		}, nil)
		if err != nil {
			return err
		}
		evalHostnamesAppSecEvalHostnames, err := akamai.LookupAppSecEvalHostnames(ctx, &akamai.LookupAppSecEvalHostnamesArgs{
			ConfigId: configuration.ConfigId,
		}, nil)
		if err != nil {
			return err
		}
		ctx.Export("evalHostnames", evalHostnamesAppSecEvalHostnames.Hostnames)
		ctx.Export("evalHostnamesOutput", evalHostnamesAppSecEvalHostnames.OutputText)
		ctx.Export("evalHostnamesJson", evalHostnamesAppSecEvalHostnames.Json)
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_akamai as akamai

configuration = akamai.get_app_sec_configuration(name=var["security_configuration"])
eval_hostnames_app_sec_eval_hostnames = akamai.get_app_sec_eval_hostnames(config_id=configuration.config_id)
pulumi.export("evalHostnames", eval_hostnames_app_sec_eval_hostnames.hostnames)
pulumi.export("evalHostnamesOutput", eval_hostnames_app_sec_eval_hostnames.output_text)
pulumi.export("evalHostnamesJson", eval_hostnames_app_sec_eval_hostnames.json)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as akamai from "@pulumi/akamai";

const configuration = akamai.getAppSecConfiguration({
    name: _var.security_configuration,
});
const evalHostnamesAppSecEvalHostnames = configuration.then(configuration => akamai.getAppSecEvalHostnames({
    configId: configuration.configId,
}));
export const evalHostnames = evalHostnamesAppSecEvalHostnames.then(evalHostnamesAppSecEvalHostnames => evalHostnamesAppSecEvalHostnames.hostnames);
export const evalHostnamesOutput = evalHostnamesAppSecEvalHostnames.then(evalHostnamesAppSecEvalHostnames => evalHostnamesAppSecEvalHostnames.outputText);
export const evalHostnamesJson = evalHostnamesAppSecEvalHostnames.then(evalHostnamesAppSecEvalHostnames => evalHostnamesAppSecEvalHostnames.json);
```


{{< /example >}}





{{% /examples %}}




## Using getAppSecEvalHostnames {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getAppSecEvalHostnames<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetAppSecEvalHostnamesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetAppSecEvalHostnamesResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_app_sec_eval_hostnames(</span><span class="nx">config_id</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">,</span>
                               <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetAppSecEvalHostnamesResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupAppSecEvalHostnames<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupAppSecEvalHostnamesArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupAppSecEvalHostnamesResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupAppSecEvalHostnames` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetAppSecEvalHostnames </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetAppSecEvalHostnamesResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetAppSecEvalHostnamesArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="configid_csharp">
<a href="#configid_csharp" style="color: inherit; text-decoration: inherit;">Config<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the security configuration to use.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="configid_go">
<a href="#configid_go" style="color: inherit; text-decoration: inherit;">Config<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the security configuration to use.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="configid_nodejs">
<a href="#configid_nodejs" style="color: inherit; text-decoration: inherit;">config<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The ID of the security configuration to use.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="config_id_python">
<a href="#config_id_python" style="color: inherit; text-decoration: inherit;">config_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of the security configuration to use.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getAppSecEvalHostnames Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="configid_csharp">
<a href="#configid_csharp" style="color: inherit; text-decoration: inherit;">Config<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hostnames_csharp">
<a href="#hostnames_csharp" style="color: inherit; text-decoration: inherit;">Hostnames</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of the evaluation hostnames.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="json_csharp">
<a href="#json_csharp" style="color: inherit; text-decoration: inherit;">Json</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A JSON-formatted list of the evaluation hostnames.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputtext_csharp">
<a href="#outputtext_csharp" style="color: inherit; text-decoration: inherit;">Output<wbr>Text</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A tabular display showing the evaluation hostnames.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="configid_go">
<a href="#configid_go" style="color: inherit; text-decoration: inherit;">Config<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hostnames_go">
<a href="#hostnames_go" style="color: inherit; text-decoration: inherit;">Hostnames</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of the evaluation hostnames.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="json_go">
<a href="#json_go" style="color: inherit; text-decoration: inherit;">Json</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A JSON-formatted list of the evaluation hostnames.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputtext_go">
<a href="#outputtext_go" style="color: inherit; text-decoration: inherit;">Output<wbr>Text</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A tabular display showing the evaluation hostnames.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="configid_nodejs">
<a href="#configid_nodejs" style="color: inherit; text-decoration: inherit;">config<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hostnames_nodejs">
<a href="#hostnames_nodejs" style="color: inherit; text-decoration: inherit;">hostnames</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of the evaluation hostnames.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="json_nodejs">
<a href="#json_nodejs" style="color: inherit; text-decoration: inherit;">json</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A JSON-formatted list of the evaluation hostnames.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputtext_nodejs">
<a href="#outputtext_nodejs" style="color: inherit; text-decoration: inherit;">output<wbr>Text</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A tabular display showing the evaluation hostnames.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="config_id_python">
<a href="#config_id_python" style="color: inherit; text-decoration: inherit;">config_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="hostnames_python">
<a href="#hostnames_python" style="color: inherit; text-decoration: inherit;">hostnames</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of the evaluation hostnames.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="json_python">
<a href="#json_python" style="color: inherit; text-decoration: inherit;">json</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A JSON-formatted list of the evaluation hostnames.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="output_text_python">
<a href="#output_text_python" style="color: inherit; text-decoration: inherit;">output_<wbr>text</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A tabular display showing the evaluation hostnames.
{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-akamai">https://github.com/pulumi/pulumi-akamai</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`akamai` Terraform Provider](https://github.com/akamai/terraform-provider-akamai).{{% /md %}}</dd>
</dl>

