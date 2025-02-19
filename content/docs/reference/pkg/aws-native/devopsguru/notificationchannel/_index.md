
---
title: "NotificationChannel"
title_tag: "aws-native.devopsguru.NotificationChannel"
meta_desc: "Documentation for the aws-native.devopsguru.NotificationChannel resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

This resource schema represents the NotificationChannel resource in the Amazon DevOps Guru.


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
        var myNotificationChannel = new AwsNative.DevOpsGuru.NotificationChannel("myNotificationChannel", new AwsNative.DevOpsGuru.NotificationChannelArgs
        {
            Config = new AwsNative.DevOpsGuru.Inputs.NotificationChannelNotificationChannelConfigArgs
            {
                Sns = new AwsNative.DevOpsGuru.Inputs.NotificationChannelSnsChannelConfigArgs
                {
                    TopicArn = "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel",
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
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/devopsguru"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := devopsguru.NewNotificationChannel(ctx, "myNotificationChannel", &devopsguru.NotificationChannelArgs{
			Config: &devopsguru.NotificationChannelNotificationChannelConfigArgs{
				Sns: &devopsguru.NotificationChannelSnsChannelConfigArgs{
					TopicArn: pulumi.String("arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel"),
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

my_notification_channel = aws_native.devopsguru.NotificationChannel("myNotificationChannel", config=aws_native.devopsguru.NotificationChannelNotificationChannelConfigArgs(
    sns=aws_native.devopsguru.NotificationChannelSnsChannelConfigArgs(
        topic_arn="arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel",
    ),
))

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const myNotificationChannel = new aws_native.devopsguru.NotificationChannel("myNotificationChannel", {config: {
    sns: {
        topicArn: "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel",
    },
}});

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
        var myNotificationChannel = new AwsNative.DevOpsGuru.NotificationChannel("myNotificationChannel", new AwsNative.DevOpsGuru.NotificationChannelArgs
        {
            Config = new AwsNative.DevOpsGuru.Inputs.NotificationChannelNotificationChannelConfigArgs
            {
                Sns = new AwsNative.DevOpsGuru.Inputs.NotificationChannelSnsChannelConfigArgs
                {
                    TopicArn = "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel",
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
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/devopsguru"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := devopsguru.NewNotificationChannel(ctx, "myNotificationChannel", &devopsguru.NotificationChannelArgs{
			Config: &devopsguru.NotificationChannelNotificationChannelConfigArgs{
				Sns: &devopsguru.NotificationChannelSnsChannelConfigArgs{
					TopicArn: pulumi.String("arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel"),
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

my_notification_channel = aws_native.devopsguru.NotificationChannel("myNotificationChannel", config=aws_native.devopsguru.NotificationChannelNotificationChannelConfigArgs(
    sns=aws_native.devopsguru.NotificationChannelSnsChannelConfigArgs(
        topic_arn="arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel",
    ),
))

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const myNotificationChannel = new aws_native.devopsguru.NotificationChannel("myNotificationChannel", {config: {
    sns: {
        topicArn: "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel",
    },
}});

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
        var myNotificationChannel1 = new AwsNative.DevOpsGuru.NotificationChannel("myNotificationChannel1", new AwsNative.DevOpsGuru.NotificationChannelArgs
        {
            Config = new AwsNative.DevOpsGuru.Inputs.NotificationChannelNotificationChannelConfigArgs
            {
                Sns = new AwsNative.DevOpsGuru.Inputs.NotificationChannelSnsChannelConfigArgs
                {
                    TopicArn = "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel",
                },
            },
        });
        var myNotificationChannel2 = new AwsNative.DevOpsGuru.NotificationChannel("myNotificationChannel2", new AwsNative.DevOpsGuru.NotificationChannelArgs
        {
            Config = new AwsNative.DevOpsGuru.Inputs.NotificationChannelNotificationChannelConfigArgs
            {
                Sns = new AwsNative.DevOpsGuru.Inputs.NotificationChannelSnsChannelConfigArgs
                {
                    TopicArn = "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel2",
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
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/devopsguru"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := devopsguru.NewNotificationChannel(ctx, "myNotificationChannel1", &devopsguru.NotificationChannelArgs{
			Config: &devopsguru.NotificationChannelNotificationChannelConfigArgs{
				Sns: &devopsguru.NotificationChannelSnsChannelConfigArgs{
					TopicArn: pulumi.String("arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel"),
				},
			},
		})
		if err != nil {
			return err
		}
		_, err = devopsguru.NewNotificationChannel(ctx, "myNotificationChannel2", &devopsguru.NotificationChannelArgs{
			Config: &devopsguru.NotificationChannelNotificationChannelConfigArgs{
				Sns: &devopsguru.NotificationChannelSnsChannelConfigArgs{
					TopicArn: pulumi.String("arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel2"),
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

my_notification_channel1 = aws_native.devopsguru.NotificationChannel("myNotificationChannel1", config=aws_native.devopsguru.NotificationChannelNotificationChannelConfigArgs(
    sns=aws_native.devopsguru.NotificationChannelSnsChannelConfigArgs(
        topic_arn="arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel",
    ),
))
my_notification_channel2 = aws_native.devopsguru.NotificationChannel("myNotificationChannel2", config=aws_native.devopsguru.NotificationChannelNotificationChannelConfigArgs(
    sns=aws_native.devopsguru.NotificationChannelSnsChannelConfigArgs(
        topic_arn="arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel2",
    ),
))

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const myNotificationChannel1 = new aws_native.devopsguru.NotificationChannel("myNotificationChannel1", {config: {
    sns: {
        topicArn: "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel",
    },
}});
const myNotificationChannel2 = new aws_native.devopsguru.NotificationChannel("myNotificationChannel2", {config: {
    sns: {
        topicArn: "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel2",
    },
}});

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
        var myNotificationChannel1 = new AwsNative.DevOpsGuru.NotificationChannel("myNotificationChannel1", new AwsNative.DevOpsGuru.NotificationChannelArgs
        {
            Config = new AwsNative.DevOpsGuru.Inputs.NotificationChannelNotificationChannelConfigArgs
            {
                Sns = new AwsNative.DevOpsGuru.Inputs.NotificationChannelSnsChannelConfigArgs
                {
                    TopicArn = "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel",
                },
            },
        });
        var myNotificationChannel2 = new AwsNative.DevOpsGuru.NotificationChannel("myNotificationChannel2", new AwsNative.DevOpsGuru.NotificationChannelArgs
        {
            Config = new AwsNative.DevOpsGuru.Inputs.NotificationChannelNotificationChannelConfigArgs
            {
                Sns = new AwsNative.DevOpsGuru.Inputs.NotificationChannelSnsChannelConfigArgs
                {
                    TopicArn = "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel2",
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
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/devopsguru"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := devopsguru.NewNotificationChannel(ctx, "myNotificationChannel1", &devopsguru.NotificationChannelArgs{
			Config: &devopsguru.NotificationChannelNotificationChannelConfigArgs{
				Sns: &devopsguru.NotificationChannelSnsChannelConfigArgs{
					TopicArn: pulumi.String("arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel"),
				},
			},
		})
		if err != nil {
			return err
		}
		_, err = devopsguru.NewNotificationChannel(ctx, "myNotificationChannel2", &devopsguru.NotificationChannelArgs{
			Config: &devopsguru.NotificationChannelNotificationChannelConfigArgs{
				Sns: &devopsguru.NotificationChannelSnsChannelConfigArgs{
					TopicArn: pulumi.String("arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel2"),
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

my_notification_channel1 = aws_native.devopsguru.NotificationChannel("myNotificationChannel1", config=aws_native.devopsguru.NotificationChannelNotificationChannelConfigArgs(
    sns=aws_native.devopsguru.NotificationChannelSnsChannelConfigArgs(
        topic_arn="arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel",
    ),
))
my_notification_channel2 = aws_native.devopsguru.NotificationChannel("myNotificationChannel2", config=aws_native.devopsguru.NotificationChannelNotificationChannelConfigArgs(
    sns=aws_native.devopsguru.NotificationChannelSnsChannelConfigArgs(
        topic_arn="arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel2",
    ),
))

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const myNotificationChannel1 = new aws_native.devopsguru.NotificationChannel("myNotificationChannel1", {config: {
    sns: {
        topicArn: "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel",
    },
}});
const myNotificationChannel2 = new aws_native.devopsguru.NotificationChannel("myNotificationChannel2", {config: {
    sns: {
        topicArn: "arn:aws:sns:us-east-1:123456789012:DefaultNotificationChannel2",
    },
}});

```


{{< /example >}}





{{% /examples %}}




## Create a NotificationChannel Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">NotificationChannel</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">NotificationChannelArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">NotificationChannel</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                        <span class="nx">config</span><span class="p">:</span> <span class="nx">Optional[NotificationChannelNotificationChannelConfigArgs]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">NotificationChannel</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                        <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">NotificationChannelArgs</a></span><span class="p">,</span>
                        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewNotificationChannel</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">NotificationChannelArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">NotificationChannel</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">NotificationChannel</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">NotificationChannelArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">NotificationChannelArgs</a></span>
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
        <span class="property-type"><a href="#inputs">NotificationChannelArgs</a></span>
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
        <span class="property-type"><a href="#inputs">NotificationChannelArgs</a></span>
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
        <span class="property-type"><a href="#inputs">NotificationChannelArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## NotificationChannel Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The NotificationChannel resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="config_csharp">
<a href="#config_csharp" style="color: inherit; text-decoration: inherit;">Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#notificationchannelnotificationchannelconfig">Pulumi.<wbr>Aws<wbr>Native.<wbr>Dev<wbr>Ops<wbr>Guru.<wbr>Inputs.<wbr>Notification<wbr>Channel<wbr>Notification<wbr>Channel<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="config_go">
<a href="#config_go" style="color: inherit; text-decoration: inherit;">Config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#notificationchannelnotificationchannelconfig">Notification<wbr>Channel<wbr>Notification<wbr>Channel<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="config_nodejs">
<a href="#config_nodejs" style="color: inherit; text-decoration: inherit;">config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#notificationchannelnotificationchannelconfig">Notification<wbr>Channel<wbr>Notification<wbr>Channel<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="config_python">
<a href="#config_python" style="color: inherit; text-decoration: inherit;">config</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#notificationchannelnotificationchannelconfig">Notification<wbr>Channel<wbr>Notification<wbr>Channel<wbr>Config<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the NotificationChannel resource produces the following output properties:



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







## Supporting Types



<h4 id="notificationchannelnotificationchannelconfig">Notification<wbr>Channel<wbr>Notification<wbr>Channel<wbr>Config</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="sns_csharp">
<a href="#sns_csharp" style="color: inherit; text-decoration: inherit;">Sns</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#notificationchannelsnschannelconfig">Pulumi.<wbr>Aws<wbr>Native.<wbr>Dev<wbr>Ops<wbr>Guru.<wbr>Inputs.<wbr>Notification<wbr>Channel<wbr>Sns<wbr>Channel<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="sns_go">
<a href="#sns_go" style="color: inherit; text-decoration: inherit;">Sns</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#notificationchannelsnschannelconfig">Notification<wbr>Channel<wbr>Sns<wbr>Channel<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="sns_nodejs">
<a href="#sns_nodejs" style="color: inherit; text-decoration: inherit;">sns</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#notificationchannelsnschannelconfig">Notification<wbr>Channel<wbr>Sns<wbr>Channel<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="sns_python">
<a href="#sns_python" style="color: inherit; text-decoration: inherit;">sns</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#notificationchannelsnschannelconfig">Notification<wbr>Channel<wbr>Sns<wbr>Channel<wbr>Config</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="notificationchannelsnschannelconfig">Notification<wbr>Channel<wbr>Sns<wbr>Channel<wbr>Config</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="topicarn_csharp">
<a href="#topicarn_csharp" style="color: inherit; text-decoration: inherit;">Topic<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="topicarn_go">
<a href="#topicarn_go" style="color: inherit; text-decoration: inherit;">Topic<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="topicarn_nodejs">
<a href="#topicarn_nodejs" style="color: inherit; text-decoration: inherit;">topic<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="topic_arn_python">
<a href="#topic_arn_python" style="color: inherit; text-decoration: inherit;">topic_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}


<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws-native">https://github.com/pulumi/pulumi-aws-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>

