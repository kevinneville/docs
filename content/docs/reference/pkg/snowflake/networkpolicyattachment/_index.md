
---
title: "NetworkPolicyAttachment"
title_tag: "snowflake.NetworkPolicyAttachment"
meta_desc: "Documentation for the snowflake.NetworkPolicyAttachment resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

## Import

```sh
 $ pulumi import snowflake:index/networkPolicyAttachment:NetworkPolicyAttachment example attachment_policyname
```


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Snowflake = Pulumi.Snowflake;

class MyStack : Stack
{
    public MyStack()
    {
        var attach = new Snowflake.NetworkPolicyAttachment("attach", new Snowflake.NetworkPolicyAttachmentArgs
        {
            NetworkPolicyName = "policy",
            SetForAccount = false,
            Users = 
            {
                "user1",
                "user2",
            },
        });
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-snowflake/sdk/go/snowflake"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := snowflake.NewNetworkPolicyAttachment(ctx, "attach", &snowflake.NetworkPolicyAttachmentArgs{
			NetworkPolicyName: pulumi.String("policy"),
			SetForAccount:     pulumi.Bool(false),
			Users: pulumi.StringArray{
				pulumi.String("user1"),
				pulumi.String("user2"),
			},
		})
		if err != nil {
			return err
		}
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_snowflake as snowflake

attach = snowflake.NetworkPolicyAttachment("attach",
    network_policy_name="policy",
    set_for_account=False,
    users=[
        "user1",
        "user2",
    ])
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as snowflake from "@pulumi/snowflake";

const attach = new snowflake.NetworkPolicyAttachment("attach", {
    networkPolicyName: "policy",
    setForAccount: false,
    users: [
        "user1",
        "user2",
    ],
});
```


{{< /example >}}





{{% /examples %}}




## Create a NetworkPolicyAttachment Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">NetworkPolicyAttachment</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">NetworkPolicyAttachmentArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">NetworkPolicyAttachment</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                            <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                            <span class="nx">network_policy_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                            <span class="nx">set_for_account</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">,</span>
                            <span class="nx">users</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">NetworkPolicyAttachment</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                            <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">NetworkPolicyAttachmentArgs</a></span><span class="p">,</span>
                            <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewNetworkPolicyAttachment</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">NetworkPolicyAttachmentArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">NetworkPolicyAttachment</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">NetworkPolicyAttachment</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">NetworkPolicyAttachmentArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">NetworkPolicyAttachmentArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language python %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">NetworkPolicyAttachmentArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">ResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties"><dt
        class="property-optional" title="Optional">
        <span>ctx</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span>
    </dt>
    <dd>Context object for the current deployment.</dd><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">NetworkPolicyAttachmentArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-required" title="Required">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">NetworkPolicyAttachmentArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## NetworkPolicyAttachment Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The NetworkPolicyAttachment resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="networkpolicyname_csharp">
<a href="#networkpolicyname_csharp" style="color: inherit; text-decoration: inherit;">Network<wbr>Policy<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the identifier for the network policy; must be unique for the account in which the network policy is created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="setforaccount_csharp">
<a href="#setforaccount_csharp" style="color: inherit; text-decoration: inherit;">Set<wbr>For<wbr>Account</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether the network policy should be applied globally to your Snowflake account<br><br>**Note:** The Snowflake
user running `terraform apply` must be on an IP address allowed by the network policy to set that policy globally on the
Snowflake account.<br><br>Additionally, a Snowflake account can only have one network policy set globally at any given
time. This resource does not enforce one-policy-per-account, it is the user's responsibility to enforce this. If
multiple network policy resources have `set_for_account: true`, the final policy set on the account will be
non-deterministic.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="users_csharp">
<a href="#users_csharp" style="color: inherit; text-decoration: inherit;">Users</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Specifies which users the network policy should be attached to
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="networkpolicyname_go">
<a href="#networkpolicyname_go" style="color: inherit; text-decoration: inherit;">Network<wbr>Policy<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the identifier for the network policy; must be unique for the account in which the network policy is created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="setforaccount_go">
<a href="#setforaccount_go" style="color: inherit; text-decoration: inherit;">Set<wbr>For<wbr>Account</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether the network policy should be applied globally to your Snowflake account<br><br>**Note:** The Snowflake
user running `terraform apply` must be on an IP address allowed by the network policy to set that policy globally on the
Snowflake account.<br><br>Additionally, a Snowflake account can only have one network policy set globally at any given
time. This resource does not enforce one-policy-per-account, it is the user's responsibility to enforce this. If
multiple network policy resources have `set_for_account: true`, the final policy set on the account will be
non-deterministic.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="users_go">
<a href="#users_go" style="color: inherit; text-decoration: inherit;">Users</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Specifies which users the network policy should be attached to
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="networkpolicyname_nodejs">
<a href="#networkpolicyname_nodejs" style="color: inherit; text-decoration: inherit;">network<wbr>Policy<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the identifier for the network policy; must be unique for the account in which the network policy is created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="setforaccount_nodejs">
<a href="#setforaccount_nodejs" style="color: inherit; text-decoration: inherit;">set<wbr>For<wbr>Account</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Specifies whether the network policy should be applied globally to your Snowflake account<br><br>**Note:** The Snowflake
user running `terraform apply` must be on an IP address allowed by the network policy to set that policy globally on the
Snowflake account.<br><br>Additionally, a Snowflake account can only have one network policy set globally at any given
time. This resource does not enforce one-policy-per-account, it is the user's responsibility to enforce this. If
multiple network policy resources have `set_for_account: true`, the final policy set on the account will be
non-deterministic.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="users_nodejs">
<a href="#users_nodejs" style="color: inherit; text-decoration: inherit;">users</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Specifies which users the network policy should be attached to
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="network_policy_name_python">
<a href="#network_policy_name_python" style="color: inherit; text-decoration: inherit;">network_<wbr>policy_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the identifier for the network policy; must be unique for the account in which the network policy is created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="set_for_account_python">
<a href="#set_for_account_python" style="color: inherit; text-decoration: inherit;">set_<wbr>for_<wbr>account</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether the network policy should be applied globally to your Snowflake account<br><br>**Note:** The Snowflake
user running `terraform apply` must be on an IP address allowed by the network policy to set that policy globally on the
Snowflake account.<br><br>Additionally, a Snowflake account can only have one network policy set globally at any given
time. This resource does not enforce one-policy-per-account, it is the user's responsibility to enforce this. If
multiple network policy resources have `set_for_account: true`, the final policy set on the account will be
non-deterministic.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="users_python">
<a href="#users_python" style="color: inherit; text-decoration: inherit;">users</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Specifies which users the network policy should be attached to
{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the NetworkPolicyAttachment resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd></dl>
{{% /choosable %}}



## Look up an Existing NetworkPolicyAttachment Resource {#look-up}

Get an existing NetworkPolicyAttachment resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">NetworkPolicyAttachmentState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">NetworkPolicyAttachment</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">network_policy_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">set_for_account</span><span class="p">:</span> <span class="nx">Optional[bool]</span> = None<span class="p">,</span>
        <span class="nx">users</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">) -&gt;</span> NetworkPolicyAttachment</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetNetworkPolicyAttachment<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">NetworkPolicyAttachmentState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">NetworkPolicyAttachment</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">NetworkPolicyAttachment</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">NetworkPolicyAttachmentState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>resource_name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Optional">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
</dl>
{{% /choosable %}}

{{% choosable language go %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

{{% choosable language csharp %}}

<dl class="resources-properties">
    <dt class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The unique name of the resulting resource.</dd>
    <dt class="property-required" title="Required">
        <span>id</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>The <em>unique</em> provider ID of the resource to lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>state</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>Any extra arguments used during the lookup.</dd>
    <dt class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
    </dt>
    <dd>A bag of options that control this resource's behavior.</dd>
</dl>

{{% /choosable %}}

The following state arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_networkpolicyname_csharp">
<a href="#state_networkpolicyname_csharp" style="color: inherit; text-decoration: inherit;">Network<wbr>Policy<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the identifier for the network policy; must be unique for the account in which the network policy is created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_setforaccount_csharp">
<a href="#state_setforaccount_csharp" style="color: inherit; text-decoration: inherit;">Set<wbr>For<wbr>Account</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether the network policy should be applied globally to your Snowflake account<br><br>**Note:** The Snowflake
user running `terraform apply` must be on an IP address allowed by the network policy to set that policy globally on the
Snowflake account.<br><br>Additionally, a Snowflake account can only have one network policy set globally at any given
time. This resource does not enforce one-policy-per-account, it is the user's responsibility to enforce this. If
multiple network policy resources have `set_for_account: true`, the final policy set on the account will be
non-deterministic.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_users_csharp">
<a href="#state_users_csharp" style="color: inherit; text-decoration: inherit;">Users</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}Specifies which users the network policy should be attached to
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_networkpolicyname_go">
<a href="#state_networkpolicyname_go" style="color: inherit; text-decoration: inherit;">Network<wbr>Policy<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the identifier for the network policy; must be unique for the account in which the network policy is created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_setforaccount_go">
<a href="#state_setforaccount_go" style="color: inherit; text-decoration: inherit;">Set<wbr>For<wbr>Account</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether the network policy should be applied globally to your Snowflake account<br><br>**Note:** The Snowflake
user running `terraform apply` must be on an IP address allowed by the network policy to set that policy globally on the
Snowflake account.<br><br>Additionally, a Snowflake account can only have one network policy set globally at any given
time. This resource does not enforce one-policy-per-account, it is the user's responsibility to enforce this. If
multiple network policy resources have `set_for_account: true`, the final policy set on the account will be
non-deterministic.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_users_go">
<a href="#state_users_go" style="color: inherit; text-decoration: inherit;">Users</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}Specifies which users the network policy should be attached to
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_networkpolicyname_nodejs">
<a href="#state_networkpolicyname_nodejs" style="color: inherit; text-decoration: inherit;">network<wbr>Policy<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Specifies the identifier for the network policy; must be unique for the account in which the network policy is created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_setforaccount_nodejs">
<a href="#state_setforaccount_nodejs" style="color: inherit; text-decoration: inherit;">set<wbr>For<wbr>Account</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Specifies whether the network policy should be applied globally to your Snowflake account<br><br>**Note:** The Snowflake
user running `terraform apply` must be on an IP address allowed by the network policy to set that policy globally on the
Snowflake account.<br><br>Additionally, a Snowflake account can only have one network policy set globally at any given
time. This resource does not enforce one-policy-per-account, it is the user's responsibility to enforce this. If
multiple network policy resources have `set_for_account: true`, the final policy set on the account will be
non-deterministic.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_users_nodejs">
<a href="#state_users_nodejs" style="color: inherit; text-decoration: inherit;">users</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}Specifies which users the network policy should be attached to
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_network_policy_name_python">
<a href="#state_network_policy_name_python" style="color: inherit; text-decoration: inherit;">network_<wbr>policy_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Specifies the identifier for the network policy; must be unique for the account in which the network policy is created.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_set_for_account_python">
<a href="#state_set_for_account_python" style="color: inherit; text-decoration: inherit;">set_<wbr>for_<wbr>account</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Specifies whether the network policy should be applied globally to your Snowflake account<br><br>**Note:** The Snowflake
user running `terraform apply` must be on an IP address allowed by the network policy to set that policy globally on the
Snowflake account.<br><br>Additionally, a Snowflake account can only have one network policy set globally at any given
time. This resource does not enforce one-policy-per-account, it is the user's responsibility to enforce this. If
multiple network policy resources have `set_for_account: true`, the final policy set on the account will be
non-deterministic.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_users_python">
<a href="#state_users_python" style="color: inherit; text-decoration: inherit;">users</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}Specifies which users the network policy should be attached to
{{% /md %}}</dd></dl>
{{% /choosable %}}







<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-snowflake">https://github.com/pulumi/pulumi-snowflake</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`snowflake` Terraform Provider](https://github.com/chanzuckerberg/terraform-provider-snowflake).{{% /md %}}</dd>
</dl>

