
---
title: "OrganizationManagerOrganizationIamBinding"
title_tag: "yandex.OrganizationManagerOrganizationIamBinding"
meta_desc: "Documentation for the yandex.OrganizationManagerOrganizationIamBinding resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Allows creation and management of a single binding within IAM policy for
an existing Yandex.Cloud Organization Manager organization.

{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Yandex = Pulumi.Yandex;

class MyStack : Stack
{
    public MyStack()
    {
        var editor = new Yandex.OrganizationManagerOrganizationIamBinding("editor", new Yandex.OrganizationManagerOrganizationIamBindingArgs
        {
            Members = 
            {
                "userAccount:some_user_id",
            },
            OrganizationId = "some_organization_id",
            Role = "editor",
        });
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-yandex/sdk/go/yandex"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := yandex.NewOrganizationManagerOrganizationIamBinding(ctx, "editor", &yandex.OrganizationManagerOrganizationIamBindingArgs{
			Members: pulumi.StringArray{
				pulumi.String("userAccount:some_user_id"),
			},
			OrganizationId: pulumi.String("some_organization_id"),
			Role:           pulumi.String("editor"),
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
import pulumi_yandex as yandex

editor = yandex.OrganizationManagerOrganizationIamBinding("editor",
    members=["userAccount:some_user_id"],
    organization_id="some_organization_id",
    role="editor")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as yandex from "@pulumi/yandex";

const editor = new yandex.OrganizationManagerOrganizationIamBinding("editor", {
    members: ["userAccount:some_user_id"],
    organizationId: "some_organization_id",
    role: "editor",
});
```


{{< /example >}}





{{% /examples %}}




## Create a OrganizationManagerOrganizationIamBinding Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">OrganizationManagerOrganizationIamBinding</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">OrganizationManagerOrganizationIamBindingArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">OrganizationManagerOrganizationIamBinding</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                              <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                                              <span class="nx">members</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
                                              <span class="nx">organization_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                              <span class="nx">role</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                                              <span class="nx">sleep_after</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">OrganizationManagerOrganizationIamBinding</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                                              <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">OrganizationManagerOrganizationIamBindingArgs</a></span><span class="p">,</span>
                                              <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewOrganizationManagerOrganizationIamBinding</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">OrganizationManagerOrganizationIamBindingArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">OrganizationManagerOrganizationIamBinding</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">OrganizationManagerOrganizationIamBinding</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">OrganizationManagerOrganizationIamBindingArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">OrganizationManagerOrganizationIamBindingArgs</a></span>
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
        <span class="property-type"><a href="#inputs">OrganizationManagerOrganizationIamBindingArgs</a></span>
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
        <span class="property-type"><a href="#inputs">OrganizationManagerOrganizationIamBindingArgs</a></span>
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
        <span class="property-type"><a href="#inputs">OrganizationManagerOrganizationIamBindingArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## OrganizationManagerOrganizationIamBinding Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The OrganizationManagerOrganizationIamBinding resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="members_csharp">
<a href="#members_csharp" style="color: inherit; text-decoration: inherit;">Members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}An array of identities that will be granted the privilege in the `role`.
Each entry can have one of the following values:
* **userAccount:{user_id}**: A unique user ID that represents a specific Yandex account.
* **serviceAccount:{service_account_id}**: A unique service account ID.
* **federatedUser:{federated_user_id}**: A unique federated user ID.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="organizationid_csharp">
<a href="#organizationid_csharp" style="color: inherit; text-decoration: inherit;">Organization<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the organization to attach the policy to.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="role_csharp">
<a href="#role_csharp" style="color: inherit; text-decoration: inherit;">Role</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role that should be assigned. Only one
`yandex.OrganizationManagerOrganizationIamBinding` can be used per role.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="sleepafter_csharp">
<a href="#sleepafter_csharp" style="color: inherit; text-decoration: inherit;">Sleep<wbr>After</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="members_go">
<a href="#members_go" style="color: inherit; text-decoration: inherit;">Members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}An array of identities that will be granted the privilege in the `role`.
Each entry can have one of the following values:
* **userAccount:{user_id}**: A unique user ID that represents a specific Yandex account.
* **serviceAccount:{service_account_id}**: A unique service account ID.
* **federatedUser:{federated_user_id}**: A unique federated user ID.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="organizationid_go">
<a href="#organizationid_go" style="color: inherit; text-decoration: inherit;">Organization<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the organization to attach the policy to.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="role_go">
<a href="#role_go" style="color: inherit; text-decoration: inherit;">Role</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role that should be assigned. Only one
`yandex.OrganizationManagerOrganizationIamBinding` can be used per role.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="sleepafter_go">
<a href="#sleepafter_go" style="color: inherit; text-decoration: inherit;">Sleep<wbr>After</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="members_nodejs">
<a href="#members_nodejs" style="color: inherit; text-decoration: inherit;">members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}An array of identities that will be granted the privilege in the `role`.
Each entry can have one of the following values:
* **userAccount:{user_id}**: A unique user ID that represents a specific Yandex account.
* **serviceAccount:{service_account_id}**: A unique service account ID.
* **federatedUser:{federated_user_id}**: A unique federated user ID.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="organizationid_nodejs">
<a href="#organizationid_nodejs" style="color: inherit; text-decoration: inherit;">organization<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the organization to attach the policy to.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="role_nodejs">
<a href="#role_nodejs" style="color: inherit; text-decoration: inherit;">role</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role that should be assigned. Only one
`yandex.OrganizationManagerOrganizationIamBinding` can be used per role.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="sleepafter_nodejs">
<a href="#sleepafter_nodejs" style="color: inherit; text-decoration: inherit;">sleep<wbr>After</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="members_python">
<a href="#members_python" style="color: inherit; text-decoration: inherit;">members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}An array of identities that will be granted the privilege in the `role`.
Each entry can have one of the following values:
* **userAccount:{user_id}**: A unique user ID that represents a specific Yandex account.
* **serviceAccount:{service_account_id}**: A unique service account ID.
* **federatedUser:{federated_user_id}**: A unique federated user ID.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="organization_id_python">
<a href="#organization_id_python" style="color: inherit; text-decoration: inherit;">organization_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the organization to attach the policy to.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="role_python">
<a href="#role_python" style="color: inherit; text-decoration: inherit;">role</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The role that should be assigned. Only one
`yandex.OrganizationManagerOrganizationIamBinding` can be used per role.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="sleep_after_python">
<a href="#sleep_after_python" style="color: inherit; text-decoration: inherit;">sleep_<wbr>after</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the OrganizationManagerOrganizationIamBinding resource produces the following output properties:



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



## Look up an Existing OrganizationManagerOrganizationIamBinding Resource {#look-up}

Get an existing OrganizationManagerOrganizationIamBinding resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">OrganizationManagerOrganizationIamBindingState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">OrganizationManagerOrganizationIamBinding</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">members</span><span class="p">:</span> <span class="nx">Optional[Sequence[str]]</span> = None<span class="p">,</span>
        <span class="nx">organization_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">role</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">sleep_after</span><span class="p">:</span> <span class="nx">Optional[int]</span> = None<span class="p">) -&gt;</span> OrganizationManagerOrganizationIamBinding</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetOrganizationManagerOrganizationIamBinding<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">OrganizationManagerOrganizationIamBindingState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">OrganizationManagerOrganizationIamBinding</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">OrganizationManagerOrganizationIamBinding</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">OrganizationManagerOrganizationIamBindingState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span id="state_members_csharp">
<a href="#state_members_csharp" style="color: inherit; text-decoration: inherit;">Members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}An array of identities that will be granted the privilege in the `role`.
Each entry can have one of the following values:
* **userAccount:{user_id}**: A unique user ID that represents a specific Yandex account.
* **serviceAccount:{service_account_id}**: A unique service account ID.
* **federatedUser:{federated_user_id}**: A unique federated user ID.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_organizationid_csharp">
<a href="#state_organizationid_csharp" style="color: inherit; text-decoration: inherit;">Organization<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the organization to attach the policy to.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_role_csharp">
<a href="#state_role_csharp" style="color: inherit; text-decoration: inherit;">Role</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role that should be assigned. Only one
`yandex.OrganizationManagerOrganizationIamBinding` can be used per role.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_sleepafter_csharp">
<a href="#state_sleepafter_csharp" style="color: inherit; text-decoration: inherit;">Sleep<wbr>After</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_members_go">
<a href="#state_members_go" style="color: inherit; text-decoration: inherit;">Members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}An array of identities that will be granted the privilege in the `role`.
Each entry can have one of the following values:
* **userAccount:{user_id}**: A unique user ID that represents a specific Yandex account.
* **serviceAccount:{service_account_id}**: A unique service account ID.
* **federatedUser:{federated_user_id}**: A unique federated user ID.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_organizationid_go">
<a href="#state_organizationid_go" style="color: inherit; text-decoration: inherit;">Organization<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the organization to attach the policy to.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_role_go">
<a href="#state_role_go" style="color: inherit; text-decoration: inherit;">Role</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role that should be assigned. Only one
`yandex.OrganizationManagerOrganizationIamBinding` can be used per role.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_sleepafter_go">
<a href="#state_sleepafter_go" style="color: inherit; text-decoration: inherit;">Sleep<wbr>After</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_members_nodejs">
<a href="#state_members_nodejs" style="color: inherit; text-decoration: inherit;">members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}An array of identities that will be granted the privilege in the `role`.
Each entry can have one of the following values:
* **userAccount:{user_id}**: A unique user ID that represents a specific Yandex account.
* **serviceAccount:{service_account_id}**: A unique service account ID.
* **federatedUser:{federated_user_id}**: A unique federated user ID.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_organizationid_nodejs">
<a href="#state_organizationid_nodejs" style="color: inherit; text-decoration: inherit;">organization<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}ID of the organization to attach the policy to.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_role_nodejs">
<a href="#state_role_nodejs" style="color: inherit; text-decoration: inherit;">role</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The role that should be assigned. Only one
`yandex.OrganizationManagerOrganizationIamBinding` can be used per role.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_sleepafter_nodejs">
<a href="#state_sleepafter_nodejs" style="color: inherit; text-decoration: inherit;">sleep<wbr>After</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_members_python">
<a href="#state_members_python" style="color: inherit; text-decoration: inherit;">members</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}An array of identities that will be granted the privilege in the `role`.
Each entry can have one of the following values:
* **userAccount:{user_id}**: A unique user ID that represents a specific Yandex account.
* **serviceAccount:{service_account_id}**: A unique service account ID.
* **federatedUser:{federated_user_id}**: A unique federated user ID.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_organization_id_python">
<a href="#state_organization_id_python" style="color: inherit; text-decoration: inherit;">organization_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}ID of the organization to attach the policy to.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_role_python">
<a href="#state_role_python" style="color: inherit; text-decoration: inherit;">role</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The role that should be assigned. Only one
`yandex.OrganizationManagerOrganizationIamBinding` can be used per role.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="state_sleep_after_python">
<a href="#state_sleep_after_python" style="color: inherit; text-decoration: inherit;">sleep_<wbr>after</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}





## Import


IAM binding imports use space-delimited identifiers; first the resource in question and then the role. These bindings can be imported using the `organization_id` and role, e.g.

```sh
 $ pulumi import yandex:index/organizationManagerOrganizationIamBinding:OrganizationManagerOrganizationIamBinding viewer "organization_id viewer"
```




<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-yandex">https://github.com/pulumi/pulumi-yandex</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`yandex` Terraform Provider](https://github.com/yandex-cloud/terraform-provider-yandex).{{% /md %}}</dd>
</dl>

