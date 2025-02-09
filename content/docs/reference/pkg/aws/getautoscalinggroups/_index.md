
---
title: "getAutoscalingGroups"
title_tag: "aws.getAutoscalingGroups"
meta_desc: "Documentation for the aws.getAutoscalingGroups function with examples, input properties, output properties, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->
<p class="resource-deprecated">Deprecated: {{% md %}}aws.getAutoscalingGroups has been deprecated in favor of aws.autoscaling.getAmiIds{{% /md %}}</p>

The Autoscaling Groups data source allows access to the list of AWS
ASGs within a specific region. This will allow you to pass a list of AutoScaling Groups to other resources.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using Aws = Pulumi.Aws;

class MyStack : Stack
{
    public MyStack()
    {
        var groups = Output.Create(Aws.AutoScaling.GetAmiIds.InvokeAsync(new Aws.AutoScaling.GetAmiIdsArgs
        {
            Filters = 
            {
                new Aws.AutoScaling.Inputs.GetAmiIdsFilterArgs
                {
                    Name = "key",
                    Values = 
                    {
                        "Team",
                    },
                },
                new Aws.AutoScaling.Inputs.GetAmiIdsFilterArgs
                {
                    Name = "value",
                    Values = 
                    {
                        "Pets",
                    },
                },
            },
        }));
        var slackNotifications = new Aws.AutoScaling.Notification("slackNotifications", new Aws.AutoScaling.NotificationArgs
        {
            GroupNames = groups.Apply(groups => groups.Names),
            Notifications = 
            {
                "autoscaling:EC2_INSTANCE_LAUNCH",
                "autoscaling:EC2_INSTANCE_TERMINATE",
                "autoscaling:EC2_INSTANCE_LAUNCH_ERROR",
                "autoscaling:EC2_INSTANCE_TERMINATE_ERROR",
            },
            TopicArn = "TOPIC ARN",
        });
    }

}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-aws/sdk/v4/go/aws/autoscaling"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		groups, err := autoscaling.GetAmiIds(ctx, &autoscaling.GetAmiIdsArgs{
			Filters: []autoscaling.GetAmiIdsFilter{
				autoscaling.GetAmiIdsFilter{
					Name: "key",
					Values: []string{
						"Team",
					},
				},
				autoscaling.GetAmiIdsFilter{
					Name: "value",
					Values: []string{
						"Pets",
					},
				},
			},
		}, nil)
		if err != nil {
			return err
		}
		_, err = autoscaling.NewNotification(ctx, "slackNotifications", &autoscaling.NotificationArgs{
			GroupNames: interface{}(groups.Names),
			Notifications: pulumi.StringArray{
				pulumi.String("autoscaling:EC2_INSTANCE_LAUNCH"),
				pulumi.String("autoscaling:EC2_INSTANCE_TERMINATE"),
				pulumi.String("autoscaling:EC2_INSTANCE_LAUNCH_ERROR"),
				pulumi.String("autoscaling:EC2_INSTANCE_TERMINATE_ERROR"),
			},
			TopicArn: pulumi.String("TOPIC ARN"),
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
import pulumi_aws as aws

groups = aws.autoscaling.get_ami_ids(filters=[
    aws.autoscaling.GetAmiIdsFilterArgs(
        name="key",
        values=["Team"],
    ),
    aws.autoscaling.GetAmiIdsFilterArgs(
        name="value",
        values=["Pets"],
    ),
])
slack_notifications = aws.autoscaling.Notification("slackNotifications",
    group_names=groups.names,
    notifications=[
        "autoscaling:EC2_INSTANCE_LAUNCH",
        "autoscaling:EC2_INSTANCE_TERMINATE",
        "autoscaling:EC2_INSTANCE_LAUNCH_ERROR",
        "autoscaling:EC2_INSTANCE_TERMINATE_ERROR",
    ],
    topic_arn="TOPIC ARN")
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws from "@pulumi/aws";

const groups = aws.autoscaling.getAmiIds({
    filters: [
        {
            name: "key",
            values: ["Team"],
        },
        {
            name: "value",
            values: ["Pets"],
        },
    ],
});
const slackNotifications = new aws.autoscaling.Notification("slackNotifications", {
    groupNames: groups.then(groups => groups.names),
    notifications: [
        "autoscaling:EC2_INSTANCE_LAUNCH",
        "autoscaling:EC2_INSTANCE_TERMINATE",
        "autoscaling:EC2_INSTANCE_LAUNCH_ERROR",
        "autoscaling:EC2_INSTANCE_TERMINATE_ERROR",
    ],
    topicArn: "TOPIC ARN",
});
```


{{< /example >}}





{{% /examples %}}




## Using getAutoscalingGroups {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getAutoscalingGroups<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetAutoscalingGroupsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetAutoscalingGroupsResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_autoscaling_groups(</span><span class="nx">filters</span><span class="p">:</span> <span class="nx">Optional[Sequence[GetAutoscalingGroupsFilter]]</span> = None<span class="p">,</span>
                           <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetAutoscalingGroupsResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetAutoscalingGroups<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetAutoscalingGroupsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetAutoscalingGroupsResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetAutoscalingGroups` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetAutoscalingGroups </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetAutoscalingGroupsResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetAutoscalingGroupsArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="filters_csharp">
<a href="#filters_csharp" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getautoscalinggroupsfilter">List&lt;Get<wbr>Autoscaling<wbr>Groups<wbr>Filter&gt;</a></span>
    </dt>
    <dd>{{% md %}}A filter used to scope the list e.g. by tags. See [related docs](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_Filter.html).
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="filters_go">
<a href="#filters_go" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getautoscalinggroupsfilter">[]Get<wbr>Autoscaling<wbr>Groups<wbr>Filter</a></span>
    </dt>
    <dd>{{% md %}}A filter used to scope the list e.g. by tags. See [related docs](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_Filter.html).
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="filters_nodejs">
<a href="#filters_nodejs" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getautoscalinggroupsfilter">Get<wbr>Autoscaling<wbr>Groups<wbr>Filter[]</a></span>
    </dt>
    <dd>{{% md %}}A filter used to scope the list e.g. by tags. See [related docs](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_Filter.html).
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="filters_python">
<a href="#filters_python" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getautoscalinggroupsfilter">Sequence[Get<wbr>Autoscaling<wbr>Groups<wbr>Filter]</a></span>
    </dt>
    <dd>{{% md %}}A filter used to scope the list e.g. by tags. See [related docs](http://docs.aws.amazon.com/AutoScaling/latest/APIReference/API_Filter.html).
{{% /md %}}</dd></dl>
{{% /choosable %}}




## getAutoscalingGroups Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arns_csharp">
<a href="#arns_csharp" style="color: inherit; text-decoration: inherit;">Arns</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of the Autoscaling Groups Arns in the current region.
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
        <span id="names_csharp">
<a href="#names_csharp" style="color: inherit; text-decoration: inherit;">Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of the Autoscaling Groups in the current region.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filters_csharp">
<a href="#filters_csharp" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getautoscalinggroupsfilter">List&lt;Get<wbr>Autoscaling<wbr>Groups<wbr>Filter&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arns_go">
<a href="#arns_go" style="color: inherit; text-decoration: inherit;">Arns</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of the Autoscaling Groups Arns in the current region.
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
        <span id="names_go">
<a href="#names_go" style="color: inherit; text-decoration: inherit;">Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of the Autoscaling Groups in the current region.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filters_go">
<a href="#filters_go" style="color: inherit; text-decoration: inherit;">Filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getautoscalinggroupsfilter">[]Get<wbr>Autoscaling<wbr>Groups<wbr>Filter</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arns_nodejs">
<a href="#arns_nodejs" style="color: inherit; text-decoration: inherit;">arns</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of the Autoscaling Groups Arns in the current region.
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
        <span id="names_nodejs">
<a href="#names_nodejs" style="color: inherit; text-decoration: inherit;">names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of the Autoscaling Groups in the current region.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filters_nodejs">
<a href="#filters_nodejs" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getautoscalinggroupsfilter">Get<wbr>Autoscaling<wbr>Groups<wbr>Filter[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="arns_python">
<a href="#arns_python" style="color: inherit; text-decoration: inherit;">arns</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of the Autoscaling Groups Arns in the current region.
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
        <span id="names_python">
<a href="#names_python" style="color: inherit; text-decoration: inherit;">names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of the Autoscaling Groups in the current region.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="filters_python">
<a href="#filters_python" style="color: inherit; text-decoration: inherit;">filters</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#getautoscalinggroupsfilter">Sequence[Get<wbr>Autoscaling<wbr>Groups<wbr>Filter]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="getautoscalinggroupsfilter">Get<wbr>Autoscaling<wbr>Groups<wbr>Filter</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the filter. The valid values are: `auto-scaling-group`, `key`, `value`, and `propagate-at-launch`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_csharp">
<a href="#values_csharp" style="color: inherit; text-decoration: inherit;">Values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}The value of the filter.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the filter. The valid values are: `auto-scaling-group`, `key`, `value`, and `propagate-at-launch`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_go">
<a href="#values_go" style="color: inherit; text-decoration: inherit;">Values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The value of the filter.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the filter. The valid values are: `auto-scaling-group`, `key`, `value`, and `propagate-at-launch`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_nodejs">
<a href="#values_nodejs" style="color: inherit; text-decoration: inherit;">values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The value of the filter.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the filter. The valid values are: `auto-scaling-group`, `key`, `value`, and `propagate-at-launch`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="values_python">
<a href="#values_python" style="color: inherit; text-decoration: inherit;">values</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}The value of the filter.
{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-aws">https://github.com/pulumi/pulumi-aws</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`aws` Terraform Provider](https://github.com/terraform-providers/terraform-provider-aws).{{% /md %}}</dd>
</dl>

