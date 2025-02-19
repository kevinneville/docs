
---
title: "getAppSecApiRequestConstraints"
title_tag: "akamai.getAppSecApiRequestConstraints"
meta_desc: "Documentation for the akamai.getAppSecApiRequestConstraints function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use the `akamai.AppSecApiRequestConstraints` data source to retrieve a list of APIs with their constraints and associated actions, or the constraints and actions for a particular API. The information available is described [here](https://developer.akamai.com/api/cloud_security/application_security/v1.html#getapirequestconstraints).


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
        var apisRequestConstraints = configuration.Apply(configuration => Output.Create(Akamai.GetAppSecApiRequestConstraints.InvokeAsync(new Akamai.GetAppSecApiRequestConstraintsArgs
        {
            ConfigId = configuration.ConfigId,
            SecurityPolicyId = @var.Security_policy_id,
        })));
        this.ApisConstraintsText = apisRequestConstraints.Apply(apisRequestConstraints => apisRequestConstraints.OutputText);
        this.ApisConstraintsJson = apisRequestConstraints.Apply(apisRequestConstraints => apisRequestConstraints.Json);
        var apiRequestConstraints = configuration.Apply(configuration => Output.Create(Akamai.GetAppSecApiRequestConstraints.InvokeAsync(new Akamai.GetAppSecApiRequestConstraintsArgs
        {
            ConfigId = configuration.ConfigId,
            SecurityPolicyId = @var.Security_policy_id,
            ApiId = @var.Api_id,
        })));
        this.ApiConstraintsText = apiRequestConstraints.Apply(apiRequestConstraints => apiRequestConstraints.OutputText);
        this.ApiConstraintsJson = apiRequestConstraints.Apply(apiRequestConstraints => apiRequestConstraints.Json);
    }

    [Output("apisConstraintsText")]
    public Output<string> ApisConstraintsText { get; set; }
    [Output("apisConstraintsJson")]
    public Output<string> ApisConstraintsJson { get; set; }
    [Output("apiConstraintsText")]
    public Output<string> ApiConstraintsText { get; set; }
    [Output("apiConstraintsJson")]
    public Output<string> ApiConstraintsJson { get; set; }
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
		apisRequestConstraints, err := akamai.LookupAppSecApiRequestConstraints(ctx, &akamai.LookupAppSecApiRequestConstraintsArgs{
			ConfigId:         configuration.ConfigId,
			SecurityPolicyId: _var.Security_policy_id,
		}, nil)
		if err != nil {
			return err
		}
		ctx.Export("apisConstraintsText", apisRequestConstraints.OutputText)
		ctx.Export("apisConstraintsJson", apisRequestConstraints.Json)
		opt1 := _var.Api_id
		apiRequestConstraints, err := akamai.LookupAppSecApiRequestConstraints(ctx, &akamai.LookupAppSecApiRequestConstraintsArgs{
			ConfigId:         configuration.ConfigId,
			SecurityPolicyId: _var.Security_policy_id,
			ApiId:            &opt1,
		}, nil)
		if err != nil {
			return err
		}
		ctx.Export("apiConstraintsText", apiRequestConstraints.OutputText)
		ctx.Export("apiConstraintsJson", apiRequestConstraints.Json)
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
apis_request_constraints = akamai.get_app_sec_api_request_constraints(config_id=configuration.config_id,
    security_policy_id=var["security_policy_id"])
pulumi.export("apisConstraintsText", apis_request_constraints.output_text)
pulumi.export("apisConstraintsJson", apis_request_constraints.json)
api_request_constraints = akamai.get_app_sec_api_request_constraints(config_id=configuration.config_id,
    security_policy_id=var["security_policy_id"],
    api_id=var["api_id"])
pulumi.export("apiConstraintsText", api_request_constraints.output_text)
pulumi.export("apiConstraintsJson", api_request_constraints.json)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as akamai from "@pulumi/akamai";

const configuration = akamai.getAppSecConfiguration({
    name: _var.security_configuration,
});
const apisRequestConstraints = configuration.then(configuration => akamai.getAppSecApiRequestConstraints({
    configId: configuration.configId,
    securityPolicyId: _var.security_policy_id,
}));
export const apisConstraintsText = apisRequestConstraints.then(apisRequestConstraints => apisRequestConstraints.outputText);
export const apisConstraintsJson = apisRequestConstraints.then(apisRequestConstraints => apisRequestConstraints.json);
const apiRequestConstraints = configuration.then(configuration => akamai.getAppSecApiRequestConstraints({
    configId: configuration.configId,
    securityPolicyId: _var.security_policy_id,
    apiId: _var.api_id,
}));
export const apiConstraintsText = apiRequestConstraints.then(apiRequestConstraints => apiRequestConstraints.outputText);
export const apiConstraintsJson = apiRequestConstraints.then(apiRequestConstraints => apiRequestConstraints.json);
```


{{< /example >}}





{{% /examples %}}




## Using getAppSecApiRequestConstraints {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getAppSecApiRequestConstraints<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetAppSecApiRequestConstraintsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetAppSecApiRequestConstraintsResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_app_sec_api_request_constraints(</span><span class="nx">api_id</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">,</span>
                                        <span class="nx">config_id</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">,</span>
                                        <span class="nx">security_policy_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetAppSecApiRequestConstraintsResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupAppSecApiRequestConstraints<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupAppSecApiRequestConstraintsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupAppSecApiRequestConstraintsResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupAppSecApiRequestConstraints` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetAppSecApiRequestConstraints </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetAppSecApiRequestConstraintsResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetAppSecApiRequestConstraintsArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
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
    <dd>{{% md %}}The configuration ID to use.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="securitypolicyid_csharp">
<a href="#securitypolicyid_csharp" style="color: inherit; text-decoration: inherit;">Security<wbr>Policy<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the security policy to use.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="apiid_csharp">
<a href="#apiid_csharp" style="color: inherit; text-decoration: inherit;">Api<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of a specific API for which to retrieve constraint information.
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
    <dd>{{% md %}}The configuration ID to use.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="securitypolicyid_go">
<a href="#securitypolicyid_go" style="color: inherit; text-decoration: inherit;">Security<wbr>Policy<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the security policy to use.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="apiid_go">
<a href="#apiid_go" style="color: inherit; text-decoration: inherit;">Api<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of a specific API for which to retrieve constraint information.
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
    <dd>{{% md %}}The configuration ID to use.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="securitypolicyid_nodejs">
<a href="#securitypolicyid_nodejs" style="color: inherit; text-decoration: inherit;">security<wbr>Policy<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the security policy to use.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="apiid_nodejs">
<a href="#apiid_nodejs" style="color: inherit; text-decoration: inherit;">api<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The ID of a specific API for which to retrieve constraint information.
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
    <dd>{{% md %}}The configuration ID to use.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="security_policy_id_python">
<a href="#security_policy_id_python" style="color: inherit; text-decoration: inherit;">security_<wbr>policy_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the security policy to use.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="api_id_python">
<a href="#api_id_python" style="color: inherit; text-decoration: inherit;">api_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The ID of a specific API for which to retrieve constraint information.
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getAppSecApiRequestConstraints Result {#result}

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
    <dd>{{% md %}}A JSON-formatted list of information about the APIs and their constraints and actions.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputtext_csharp">
<a href="#outputtext_csharp" style="color: inherit; text-decoration: inherit;">Output<wbr>Text</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A tabular display showing the APIs and their constraints and actions.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="securitypolicyid_csharp">
<a href="#securitypolicyid_csharp" style="color: inherit; text-decoration: inherit;">Security<wbr>Policy<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="apiid_csharp">
<a href="#apiid_csharp" style="color: inherit; text-decoration: inherit;">Api<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}A JSON-formatted list of information about the APIs and their constraints and actions.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputtext_go">
<a href="#outputtext_go" style="color: inherit; text-decoration: inherit;">Output<wbr>Text</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A tabular display showing the APIs and their constraints and actions.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="securitypolicyid_go">
<a href="#securitypolicyid_go" style="color: inherit; text-decoration: inherit;">Security<wbr>Policy<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="apiid_go">
<a href="#apiid_go" style="color: inherit; text-decoration: inherit;">Api<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}A JSON-formatted list of information about the APIs and their constraints and actions.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputtext_nodejs">
<a href="#outputtext_nodejs" style="color: inherit; text-decoration: inherit;">output<wbr>Text</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A tabular display showing the APIs and their constraints and actions.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="securitypolicyid_nodejs">
<a href="#securitypolicyid_nodejs" style="color: inherit; text-decoration: inherit;">security<wbr>Policy<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="apiid_nodejs">
<a href="#apiid_nodejs" style="color: inherit; text-decoration: inherit;">api<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}A JSON-formatted list of information about the APIs and their constraints and actions.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="output_text_python">
<a href="#output_text_python" style="color: inherit; text-decoration: inherit;">output_<wbr>text</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A tabular display showing the APIs and their constraints and actions.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="security_policy_id_python">
<a href="#security_policy_id_python" style="color: inherit; text-decoration: inherit;">security_<wbr>policy_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="api_id_python">
<a href="#api_id_python" style="color: inherit; text-decoration: inherit;">api_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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

