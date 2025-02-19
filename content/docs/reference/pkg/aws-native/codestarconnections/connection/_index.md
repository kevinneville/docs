
---
title: "Connection"
title_tag: "aws-native.codestarconnections.Connection"
meta_desc: "Documentation for the aws-native.codestarconnections.Connection resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Schema for AWS::CodeStarConnections::Connection resource which can be used to connect external source providers with AWS CodePipeline


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}


### Example


{{< example csharp >}}

```csharp
using Pulumi;
using AwsNative = Pulumi.AwsNative;

class MyStack : Stack
{
    public MyStack()
    {
        var sampleConnection = new AwsNative.CodeStarConnections.Connection("sampleConnection", new AwsNative.CodeStarConnections.ConnectionArgs
        {
            ConnectionName = "MyConnection",
            ProviderType = "Bitbucket",
            Tags = 
            {
                new AwsNative.CodeStarConnections.Inputs.ConnectionTagArgs
                {
                    Key = "Project",
                    Value = "ProjectB",
                },
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
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/codestarconnections"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := codestarconnections.NewConnection(ctx, "sampleConnection", &codestarconnections.ConnectionArgs{
			ConnectionName: pulumi.String("MyConnection"),
			ProviderType:   pulumi.String("Bitbucket"),
			Tags: []codestarconnections.ConnectionTagArgs{
				&codestarconnections.ConnectionTagArgs{
					Key:   pulumi.String("Project"),
					Value: pulumi.String("ProjectB"),
				},
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
import pulumi_aws_native as aws_native

sample_connection = aws_native.codestarconnections.Connection("sampleConnection",
    connection_name="MyConnection",
    provider_type="Bitbucket",
    tags=[aws_native.codestarconnections.ConnectionTagArgs(
        key="Project",
        value="ProjectB",
    )])

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const sampleConnection = new aws_native.codestarconnections.Connection("sampleConnection", {
    connectionName: "MyConnection",
    providerType: "Bitbucket",
    tags: [{
        key: "Project",
        value: "ProjectB",
    }],
});

```


{{< /example >}}




### Example


{{< example csharp >}}

```csharp
using Pulumi;
using AwsNative = Pulumi.AwsNative;

class MyStack : Stack
{
    public MyStack()
    {
        var sampleConnection = new AwsNative.CodeStarConnections.Connection("sampleConnection", new AwsNative.CodeStarConnections.ConnectionArgs
        {
            ConnectionName = "MyConnection",
            ProviderType = "Bitbucket",
            Tags = 
            {
                new AwsNative.CodeStarConnections.Inputs.ConnectionTagArgs
                {
                    Key = "Project",
                    Value = "ProjectB",
                },
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
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/codestarconnections"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := codestarconnections.NewConnection(ctx, "sampleConnection", &codestarconnections.ConnectionArgs{
			ConnectionName: pulumi.String("MyConnection"),
			ProviderType:   pulumi.String("Bitbucket"),
			Tags: []codestarconnections.ConnectionTagArgs{
				&codestarconnections.ConnectionTagArgs{
					Key:   pulumi.String("Project"),
					Value: pulumi.String("ProjectB"),
				},
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
import pulumi_aws_native as aws_native

sample_connection = aws_native.codestarconnections.Connection("sampleConnection",
    connection_name="MyConnection",
    provider_type="Bitbucket",
    tags=[aws_native.codestarconnections.ConnectionTagArgs(
        key="Project",
        value="ProjectB",
    )])

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const sampleConnection = new aws_native.codestarconnections.Connection("sampleConnection", {
    connectionName: "MyConnection",
    providerType: "Bitbucket",
    tags: [{
        key: "Project",
        value: "ProjectB",
    }],
});

```


{{< /example >}}




### Example


{{< example csharp >}}

```csharp
using Pulumi;
using AwsNative = Pulumi.AwsNative;

class MyStack : Stack
{
    public MyStack()
    {
        var sampleConnection = new AwsNative.CodeStarConnections.Connection("sampleConnection", new AwsNative.CodeStarConnections.ConnectionArgs
        {
            ConnectionName = "MyConnection",
            ProviderType = "GitHubEnterpriseServer",
            HostArn = "arn:aws:codestar-connections:us-west-2:123456789123:host/abc123-example",
            Tags = 
            {
                new AwsNative.CodeStarConnections.Inputs.ConnectionTagArgs
                {
                    Key = "Project",
                    Value = "ProjectB",
                },
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
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/codestarconnections"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := codestarconnections.NewConnection(ctx, "sampleConnection", &codestarconnections.ConnectionArgs{
			ConnectionName: pulumi.String("MyConnection"),
			ProviderType:   pulumi.String("GitHubEnterpriseServer"),
			HostArn:        pulumi.String("arn:aws:codestar-connections:us-west-2:123456789123:host/abc123-example"),
			Tags: []codestarconnections.ConnectionTagArgs{
				&codestarconnections.ConnectionTagArgs{
					Key:   pulumi.String("Project"),
					Value: pulumi.String("ProjectB"),
				},
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
import pulumi_aws_native as aws_native

sample_connection = aws_native.codestarconnections.Connection("sampleConnection",
    connection_name="MyConnection",
    provider_type="GitHubEnterpriseServer",
    host_arn="arn:aws:codestar-connections:us-west-2:123456789123:host/abc123-example",
    tags=[aws_native.codestarconnections.ConnectionTagArgs(
        key="Project",
        value="ProjectB",
    )])

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const sampleConnection = new aws_native.codestarconnections.Connection("sampleConnection", {
    connectionName: "MyConnection",
    providerType: "GitHubEnterpriseServer",
    hostArn: "arn:aws:codestar-connections:us-west-2:123456789123:host/abc123-example",
    tags: [{
        key: "Project",
        value: "ProjectB",
    }],
});

```


{{< /example >}}




### Example


{{< example csharp >}}

```csharp
using Pulumi;
using AwsNative = Pulumi.AwsNative;

class MyStack : Stack
{
    public MyStack()
    {
        var sampleConnection = new AwsNative.CodeStarConnections.Connection("sampleConnection", new AwsNative.CodeStarConnections.ConnectionArgs
        {
            ConnectionName = "MyConnection",
            ProviderType = "GitHubEnterpriseServer",
            HostArn = "arn:aws:codestar-connections:us-west-2:123456789123:host/abc123-example",
            Tags = 
            {
                new AwsNative.CodeStarConnections.Inputs.ConnectionTagArgs
                {
                    Key = "Project",
                    Value = "ProjectB",
                },
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
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/codestarconnections"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := codestarconnections.NewConnection(ctx, "sampleConnection", &codestarconnections.ConnectionArgs{
			ConnectionName: pulumi.String("MyConnection"),
			ProviderType:   pulumi.String("GitHubEnterpriseServer"),
			HostArn:        pulumi.String("arn:aws:codestar-connections:us-west-2:123456789123:host/abc123-example"),
			Tags: []codestarconnections.ConnectionTagArgs{
				&codestarconnections.ConnectionTagArgs{
					Key:   pulumi.String("Project"),
					Value: pulumi.String("ProjectB"),
				},
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
import pulumi_aws_native as aws_native

sample_connection = aws_native.codestarconnections.Connection("sampleConnection",
    connection_name="MyConnection",
    provider_type="GitHubEnterpriseServer",
    host_arn="arn:aws:codestar-connections:us-west-2:123456789123:host/abc123-example",
    tags=[aws_native.codestarconnections.ConnectionTagArgs(
        key="Project",
        value="ProjectB",
    )])

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const sampleConnection = new aws_native.codestarconnections.Connection("sampleConnection", {
    connectionName: "MyConnection",
    providerType: "GitHubEnterpriseServer",
    hostArn: "arn:aws:codestar-connections:us-west-2:123456789123:host/abc123-example",
    tags: [{
        key: "Project",
        value: "ProjectB",
    }],
});

```


{{< /example >}}





{{% /examples %}}




## Create a Connection Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">Connection</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">ConnectionArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Connection</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
               <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
               <span class="nx">connection_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
               <span class="nx">host_arn</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
               <span class="nx">provider_type</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
               <span class="nx">tags</span><span class="p">:</span> <span class="nx">Optional[Sequence[ConnectionTagArgs]]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Connection</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
               <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">ConnectionArgs</a></span><span class="p">,</span>
               <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewConnection</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">ConnectionArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Connection</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">Connection</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">ConnectionArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">ConnectionArgs</a></span>
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
        <span class="property-type"><a href="#inputs">ConnectionArgs</a></span>
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
        <span class="property-type"><a href="#inputs">ConnectionArgs</a></span>
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
        <span class="property-type"><a href="#inputs">ConnectionArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## Connection Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The Connection resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="connectionname_csharp">
<a href="#connectionname_csharp" style="color: inherit; text-decoration: inherit;">Connection<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the connection. Connection names must be unique in an AWS user account.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="hostarn_csharp">
<a href="#hostarn_csharp" style="color: inherit; text-decoration: inherit;">Host<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The host arn configured to represent the infrastructure where your third-party provider is installed. You must specify either a ProviderType or a HostArn.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="providertype_csharp">
<a href="#providertype_csharp" style="color: inherit; text-decoration: inherit;">Provider<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the external provider where your third-party code repository is configured. You must specify either a ProviderType or a HostArn.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectiontag">List&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>Code<wbr>Star<wbr>Connections.<wbr>Inputs.<wbr>Connection<wbr>Tag<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}Specifies the tags applied to a connection.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="connectionname_go">
<a href="#connectionname_go" style="color: inherit; text-decoration: inherit;">Connection<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the connection. Connection names must be unique in an AWS user account.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="hostarn_go">
<a href="#hostarn_go" style="color: inherit; text-decoration: inherit;">Host<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The host arn configured to represent the infrastructure where your third-party provider is installed. You must specify either a ProviderType or a HostArn.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="providertype_go">
<a href="#providertype_go" style="color: inherit; text-decoration: inherit;">Provider<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the external provider where your third-party code repository is configured. You must specify either a ProviderType or a HostArn.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectiontag">[]Connection<wbr>Tag<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}Specifies the tags applied to a connection.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="connectionname_nodejs">
<a href="#connectionname_nodejs" style="color: inherit; text-decoration: inherit;">connection<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the connection. Connection names must be unique in an AWS user account.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="hostarn_nodejs">
<a href="#hostarn_nodejs" style="color: inherit; text-decoration: inherit;">host<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The host arn configured to represent the infrastructure where your third-party provider is installed. You must specify either a ProviderType or a HostArn.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="providertype_nodejs">
<a href="#providertype_nodejs" style="color: inherit; text-decoration: inherit;">provider<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the external provider where your third-party code repository is configured. You must specify either a ProviderType or a HostArn.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectiontag">Connection<wbr>Tag<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}Specifies the tags applied to a connection.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="connection_name_python">
<a href="#connection_name_python" style="color: inherit; text-decoration: inherit;">connection_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the connection. Connection names must be unique in an AWS user account.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="host_arn_python">
<a href="#host_arn_python" style="color: inherit; text-decoration: inherit;">host_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The host arn configured to represent the infrastructure where your third-party provider is installed. You must specify either a ProviderType or a HostArn.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="provider_type_python">
<a href="#provider_type_python" style="color: inherit; text-decoration: inherit;">provider_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the external provider where your third-party code repository is configured. You must specify either a ProviderType or a HostArn.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectiontag">Sequence[Connection<wbr>Tag<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}Specifies the tags applied to a connection.{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the Connection resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="connectionarn_csharp">
<a href="#connectionarn_csharp" style="color: inherit; text-decoration: inherit;">Connection<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the  connection. The ARN is used as the connection reference when the connection is shared between AWS services.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="connectionstatus_csharp">
<a href="#connectionstatus_csharp" style="color: inherit; text-decoration: inherit;">Connection<wbr>Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The current status of the connection.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="owneraccountid_csharp">
<a href="#owneraccountid_csharp" style="color: inherit; text-decoration: inherit;">Owner<wbr>Account<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the external provider where your third-party code repository is configured. For Bitbucket, this is the account ID of the owner of the Bitbucket repository.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="connectionarn_go">
<a href="#connectionarn_go" style="color: inherit; text-decoration: inherit;">Connection<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the  connection. The ARN is used as the connection reference when the connection is shared between AWS services.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="connectionstatus_go">
<a href="#connectionstatus_go" style="color: inherit; text-decoration: inherit;">Connection<wbr>Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The current status of the connection.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="owneraccountid_go">
<a href="#owneraccountid_go" style="color: inherit; text-decoration: inherit;">Owner<wbr>Account<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the external provider where your third-party code repository is configured. For Bitbucket, this is the account ID of the owner of the Bitbucket repository.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="connectionarn_nodejs">
<a href="#connectionarn_nodejs" style="color: inherit; text-decoration: inherit;">connection<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the  connection. The ARN is used as the connection reference when the connection is shared between AWS services.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="connectionstatus_nodejs">
<a href="#connectionstatus_nodejs" style="color: inherit; text-decoration: inherit;">connection<wbr>Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The current status of the connection.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="owneraccountid_nodejs">
<a href="#owneraccountid_nodejs" style="color: inherit; text-decoration: inherit;">owner<wbr>Account<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the external provider where your third-party code repository is configured. For Bitbucket, this is the account ID of the owner of the Bitbucket repository.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="connection_arn_python">
<a href="#connection_arn_python" style="color: inherit; text-decoration: inherit;">connection_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Amazon Resource Name (ARN) of the  connection. The ARN is used as the connection reference when the connection is shared between AWS services.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="connection_status_python">
<a href="#connection_status_python" style="color: inherit; text-decoration: inherit;">connection_<wbr>status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The current status of the connection.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="owner_account_id_python">
<a href="#owner_account_id_python" style="color: inherit; text-decoration: inherit;">owner_<wbr>account_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the external provider where your third-party code repository is configured. For Bitbucket, this is the account ID of the owner of the Bitbucket repository.{{% /md %}}</dd></dl>
{{% /choosable %}}







## Supporting Types



<h4 id="connectiontag">Connection<wbr>Tag</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_csharp">
<a href="#key_csharp" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The key name of the tag. You can specify a value that is 1 to 128 Unicode characters in length and cannot be prefixed with aws:. You can use any of the following characters: the set of Unicode letters, digits, whitespace, _, ., /, =, +, and -. {{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_csharp">
<a href="#value_csharp" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value for the tag. You can specify a value that is 0 to 256 Unicode characters in length and cannot be prefixed with aws:. You can use any of the following characters: the set of Unicode letters, digits, whitespace, _, ., /, =, +, and -. {{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_go">
<a href="#key_go" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The key name of the tag. You can specify a value that is 1 to 128 Unicode characters in length and cannot be prefixed with aws:. You can use any of the following characters: the set of Unicode letters, digits, whitespace, _, ., /, =, +, and -. {{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_go">
<a href="#value_go" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value for the tag. You can specify a value that is 0 to 256 Unicode characters in length and cannot be prefixed with aws:. You can use any of the following characters: the set of Unicode letters, digits, whitespace, _, ., /, =, +, and -. {{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_nodejs">
<a href="#key_nodejs" style="color: inherit; text-decoration: inherit;">key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The key name of the tag. You can specify a value that is 1 to 128 Unicode characters in length and cannot be prefixed with aws:. You can use any of the following characters: the set of Unicode letters, digits, whitespace, _, ., /, =, +, and -. {{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_nodejs">
<a href="#value_nodejs" style="color: inherit; text-decoration: inherit;">value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The value for the tag. You can specify a value that is 0 to 256 Unicode characters in length and cannot be prefixed with aws:. You can use any of the following characters: the set of Unicode letters, digits, whitespace, _, ., /, =, +, and -. {{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_python">
<a href="#key_python" style="color: inherit; text-decoration: inherit;">key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The key name of the tag. You can specify a value that is 1 to 128 Unicode characters in length and cannot be prefixed with aws:. You can use any of the following characters: the set of Unicode letters, digits, whitespace, _, ., /, =, +, and -. {{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_python">
<a href="#value_python" style="color: inherit; text-decoration: inherit;">value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The value for the tag. You can specify a value that is 0 to 256 Unicode characters in length and cannot be prefixed with aws:. You can use any of the following characters: the set of Unicode letters, digits, whitespace, _, ., /, =, +, and -. {{% /md %}}</dd></dl>
{{% /choosable %}}


<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws-native">https://github.com/pulumi/pulumi-aws-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

