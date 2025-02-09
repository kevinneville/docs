
---
title: "Pipeline"
title_tag: "aws-native.sagemaker.Pipeline"
meta_desc: "Documentation for the aws-native.sagemaker.Pipeline resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Resource Type definition for AWS::SageMaker::Pipeline


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
        var myPipeline = new AwsNative.SageMaker.Pipeline("myPipeline", new AwsNative.SageMaker.PipelineArgs
        {
            PipelineName = "<pipeline-name>",
            PipelineDisplayName = "<pipeline-display-name>",
            PipelineDescription = "<pipeline-description>",
            PipelineDefinition = 
            {
                { "pipelineDefinitionBody", "{\"Version\":\"2020-12-01\",\"Parameters\":[{\"Name\":\"InputDataSource\",\"DefaultValue\":\"\"},{\"Name\":\"InstanceCount\",\"Type\":\"Integer\",\"DefaultValue\":1}],\"Steps\":[{\"Name\":\"Training1\",\"Type\":\"Training\",\"Arguments\":{\"InputDataConfig\":[{\"DataSource\":{\"S3DataSource\":{\"S3Uri\":{\"Get\":\"Parameters.InputDataSource\"}}}}],\"OutputDataConfig\":{\"S3OutputPath\":\"s3://my-s3-bucket/\"},\"ResourceConfig\":{\"InstanceType\":\"ml.m5.large\",\"InstanceCount\":{\"Get\":\"Parameters.InstanceCount\"},\"VolumeSizeInGB\":1024}}}]}" },
            },
            RoleArn = "arn:aws:iam::<account-id>:root",
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/sagemaker"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := sagemaker.NewPipeline(ctx, "myPipeline", &sagemaker.PipelineArgs{
			PipelineName:        pulumi.String("<pipeline-name>"),
			PipelineDisplayName: pulumi.String("<pipeline-display-name>"),
			PipelineDescription: pulumi.String("<pipeline-description>"),
			PipelineDefinition: pulumi.Any{
				PipelineDefinitionBody: "{\"Version\":\"2020-12-01\",\"Parameters\":[{\"Name\":\"InputDataSource\",\"DefaultValue\":\"\"},{\"Name\":\"InstanceCount\",\"Type\":\"Integer\",\"DefaultValue\":1}],\"Steps\":[{\"Name\":\"Training1\",\"Type\":\"Training\",\"Arguments\":{\"InputDataConfig\":[{\"DataSource\":{\"S3DataSource\":{\"S3Uri\":{\"Get\":\"Parameters.InputDataSource\"}}}}],\"OutputDataConfig\":{\"S3OutputPath\":\"s3://my-s3-bucket/\"},\"ResourceConfig\":{\"InstanceType\":\"ml.m5.large\",\"InstanceCount\":{\"Get\":\"Parameters.InstanceCount\"},\"VolumeSizeInGB\":1024}}}]}",
			},
			RoleArn: pulumi.String("arn:aws:iam::<account-id>:root"),
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

my_pipeline = aws_native.sagemaker.Pipeline("myPipeline",
    pipeline_name="<pipeline-name>",
    pipeline_display_name="<pipeline-display-name>",
    pipeline_description="<pipeline-description>",
    pipeline_definition={
        "pipelineDefinitionBody": "{\"Version\":\"2020-12-01\",\"Parameters\":[{\"Name\":\"InputDataSource\",\"DefaultValue\":\"\"},{\"Name\":\"InstanceCount\",\"Type\":\"Integer\",\"DefaultValue\":1}],\"Steps\":[{\"Name\":\"Training1\",\"Type\":\"Training\",\"Arguments\":{\"InputDataConfig\":[{\"DataSource\":{\"S3DataSource\":{\"S3Uri\":{\"Get\":\"Parameters.InputDataSource\"}}}}],\"OutputDataConfig\":{\"S3OutputPath\":\"s3://my-s3-bucket/\"},\"ResourceConfig\":{\"InstanceType\":\"ml.m5.large\",\"InstanceCount\":{\"Get\":\"Parameters.InstanceCount\"},\"VolumeSizeInGB\":1024}}}]}",
    },
    role_arn="arn:aws:iam::<account-id>:root")

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const myPipeline = new aws_native.sagemaker.Pipeline("myPipeline", {
    pipelineName: "<pipeline-name>",
    pipelineDisplayName: "<pipeline-display-name>",
    pipelineDescription: "<pipeline-description>",
    pipelineDefinition: {
        pipelineDefinitionBody: "{\"Version\":\"2020-12-01\",\"Parameters\":[{\"Name\":\"InputDataSource\",\"DefaultValue\":\"\"},{\"Name\":\"InstanceCount\",\"Type\":\"Integer\",\"DefaultValue\":1}],\"Steps\":[{\"Name\":\"Training1\",\"Type\":\"Training\",\"Arguments\":{\"InputDataConfig\":[{\"DataSource\":{\"S3DataSource\":{\"S3Uri\":{\"Get\":\"Parameters.InputDataSource\"}}}}],\"OutputDataConfig\":{\"S3OutputPath\":\"s3://my-s3-bucket/\"},\"ResourceConfig\":{\"InstanceType\":\"ml.m5.large\",\"InstanceCount\":{\"Get\":\"Parameters.InstanceCount\"},\"VolumeSizeInGB\":1024}}}]}",
    },
    roleArn: "arn:aws:iam::<account-id>:root",
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
        var myPipeline = new AwsNative.SageMaker.Pipeline("myPipeline", new AwsNative.SageMaker.PipelineArgs
        {
            PipelineName = "<pipeline-name>",
            PipelineDisplayName = "<pipeline-display-name>",
            PipelineDescription = "<pipeline-description>",
            PipelineDefinition = 
            {
                { "pipelineDefinitionS3Location", 
                {
                    { "bucket", "<S3-bucket-location>" },
                    { "key", "<S3-bucket-key>" },
                } },
            },
            RoleArn = "arn:aws:iam::<account-id>:root",
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/sagemaker"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := sagemaker.NewPipeline(ctx, "myPipeline", &sagemaker.PipelineArgs{
			PipelineName:        pulumi.String("<pipeline-name>"),
			PipelineDisplayName: pulumi.String("<pipeline-display-name>"),
			PipelineDescription: pulumi.String("<pipeline-description>"),
			PipelineDefinition: pulumi.Any{
				PipelineDefinitionS3Location: map[string]interface{}{
					"bucket": "<S3-bucket-location>",
					"key":    "<S3-bucket-key>",
				},
			},
			RoleArn: pulumi.String("arn:aws:iam::<account-id>:root"),
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

my_pipeline = aws_native.sagemaker.Pipeline("myPipeline",
    pipeline_name="<pipeline-name>",
    pipeline_display_name="<pipeline-display-name>",
    pipeline_description="<pipeline-description>",
    pipeline_definition={
        "pipelineDefinitionS3Location": {
            "bucket": "<S3-bucket-location>",
            "key": "<S3-bucket-key>",
        },
    },
    role_arn="arn:aws:iam::<account-id>:root")

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const myPipeline = new aws_native.sagemaker.Pipeline("myPipeline", {
    pipelineName: "<pipeline-name>",
    pipelineDisplayName: "<pipeline-display-name>",
    pipelineDescription: "<pipeline-description>",
    pipelineDefinition: {
        pipelineDefinitionS3Location: {
            bucket: "<S3-bucket-location>",
            key: "<S3-bucket-key>",
        },
    },
    roleArn: "arn:aws:iam::<account-id>:root",
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
        var myAwesomePipeline = new AwsNative.SageMaker.Pipeline("myAwesomePipeline", new AwsNative.SageMaker.PipelineArgs
        {
            PipelineName = "<pipeline-name>",
            PipelineDisplayName = "<pipeline-display-name>",
            PipelineDescription = "<pipeline-description>",
            PipelineDefinition = 
            {
                { "pipelineDefinitionBody", "{\"Version\":\"2020-12-01\",\"Parameters\":[{\"Name\":\"InputDataSource\",\"DefaultValue\":\"\"},{\"Name\":\"InstanceCount\",\"Type\":\"Integer\",\"DefaultValue\":1}],\"Steps\":[{\"Name\":\"Training1\",\"Type\":\"Training\",\"Arguments\":{\"InputDataConfig\":[{\"DataSource\":{\"S3DataSource\":{\"S3Uri\":{\"Get\":\"Parameters.InputDataSource\"}}}}],\"OutputDataConfig\":{\"S3OutputPath\":\"s3://my-s3-bucket/\"},\"ResourceConfig\":{\"InstanceType\":\"ml.m5.large\",\"InstanceCount\":{\"Get\":\"Parameters.InstanceCount\"},\"VolumeSizeInGB\":1024}}}]}" },
            },
            RoleArn = "arn:aws:iam::<account-id>:root",
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/sagemaker"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := sagemaker.NewPipeline(ctx, "myAwesomePipeline", &sagemaker.PipelineArgs{
			PipelineName:        pulumi.String("<pipeline-name>"),
			PipelineDisplayName: pulumi.String("<pipeline-display-name>"),
			PipelineDescription: pulumi.String("<pipeline-description>"),
			PipelineDefinition: pulumi.Any{
				PipelineDefinitionBody: "{\"Version\":\"2020-12-01\",\"Parameters\":[{\"Name\":\"InputDataSource\",\"DefaultValue\":\"\"},{\"Name\":\"InstanceCount\",\"Type\":\"Integer\",\"DefaultValue\":1}],\"Steps\":[{\"Name\":\"Training1\",\"Type\":\"Training\",\"Arguments\":{\"InputDataConfig\":[{\"DataSource\":{\"S3DataSource\":{\"S3Uri\":{\"Get\":\"Parameters.InputDataSource\"}}}}],\"OutputDataConfig\":{\"S3OutputPath\":\"s3://my-s3-bucket/\"},\"ResourceConfig\":{\"InstanceType\":\"ml.m5.large\",\"InstanceCount\":{\"Get\":\"Parameters.InstanceCount\"},\"VolumeSizeInGB\":1024}}}]}",
			},
			RoleArn: pulumi.String("arn:aws:iam::<account-id>:root"),
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

my_awesome_pipeline = aws_native.sagemaker.Pipeline("myAwesomePipeline",
    pipeline_name="<pipeline-name>",
    pipeline_display_name="<pipeline-display-name>",
    pipeline_description="<pipeline-description>",
    pipeline_definition={
        "pipelineDefinitionBody": "{\"Version\":\"2020-12-01\",\"Parameters\":[{\"Name\":\"InputDataSource\",\"DefaultValue\":\"\"},{\"Name\":\"InstanceCount\",\"Type\":\"Integer\",\"DefaultValue\":1}],\"Steps\":[{\"Name\":\"Training1\",\"Type\":\"Training\",\"Arguments\":{\"InputDataConfig\":[{\"DataSource\":{\"S3DataSource\":{\"S3Uri\":{\"Get\":\"Parameters.InputDataSource\"}}}}],\"OutputDataConfig\":{\"S3OutputPath\":\"s3://my-s3-bucket/\"},\"ResourceConfig\":{\"InstanceType\":\"ml.m5.large\",\"InstanceCount\":{\"Get\":\"Parameters.InstanceCount\"},\"VolumeSizeInGB\":1024}}}]}",
    },
    role_arn="arn:aws:iam::<account-id>:root")

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const myAwesomePipeline = new aws_native.sagemaker.Pipeline("myAwesomePipeline", {
    pipelineName: "<pipeline-name>",
    pipelineDisplayName: "<pipeline-display-name>",
    pipelineDescription: "<pipeline-description>",
    pipelineDefinition: {
        pipelineDefinitionBody: "{\"Version\":\"2020-12-01\",\"Parameters\":[{\"Name\":\"InputDataSource\",\"DefaultValue\":\"\"},{\"Name\":\"InstanceCount\",\"Type\":\"Integer\",\"DefaultValue\":1}],\"Steps\":[{\"Name\":\"Training1\",\"Type\":\"Training\",\"Arguments\":{\"InputDataConfig\":[{\"DataSource\":{\"S3DataSource\":{\"S3Uri\":{\"Get\":\"Parameters.InputDataSource\"}}}}],\"OutputDataConfig\":{\"S3OutputPath\":\"s3://my-s3-bucket/\"},\"ResourceConfig\":{\"InstanceType\":\"ml.m5.large\",\"InstanceCount\":{\"Get\":\"Parameters.InstanceCount\"},\"VolumeSizeInGB\":1024}}}]}",
    },
    roleArn: "arn:aws:iam::<account-id>:root",
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
        var myAwesomePipeline = new AwsNative.SageMaker.Pipeline("myAwesomePipeline", new AwsNative.SageMaker.PipelineArgs
        {
            PipelineName = "<pipeline-name>",
            PipelineDisplayName = "<pipeline-display-name>",
            PipelineDescription = "<pipeline-description>",
            PipelineDefinition = 
            {
                { "pipelineDefinitionS3Location", 
                {
                    { "bucket", "<S3-bucket-location>" },
                    { "key", "<S3-bucket-key>" },
                } },
            },
            RoleArn = "arn:aws:iam::<account-id>:root",
        });
    }

}

```


{{< /example >}}


{{< example go >}}


```go
package main

import (
	"github.com/pulumi/pulumi-aws-native/sdk/go/aws/sagemaker"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		_, err := sagemaker.NewPipeline(ctx, "myAwesomePipeline", &sagemaker.PipelineArgs{
			PipelineName:        pulumi.String("<pipeline-name>"),
			PipelineDisplayName: pulumi.String("<pipeline-display-name>"),
			PipelineDescription: pulumi.String("<pipeline-description>"),
			PipelineDefinition: pulumi.Any{
				PipelineDefinitionS3Location: map[string]interface{}{
					"bucket": "<S3-bucket-location>",
					"key":    "<S3-bucket-key>",
				},
			},
			RoleArn: pulumi.String("arn:aws:iam::<account-id>:root"),
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

my_awesome_pipeline = aws_native.sagemaker.Pipeline("myAwesomePipeline",
    pipeline_name="<pipeline-name>",
    pipeline_display_name="<pipeline-display-name>",
    pipeline_description="<pipeline-description>",
    pipeline_definition={
        "pipelineDefinitionS3Location": {
            "bucket": "<S3-bucket-location>",
            "key": "<S3-bucket-key>",
        },
    },
    role_arn="arn:aws:iam::<account-id>:root")

```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as aws_native from "@pulumi/aws-native";

const myAwesomePipeline = new aws_native.sagemaker.Pipeline("myAwesomePipeline", {
    pipelineName: "<pipeline-name>",
    pipelineDisplayName: "<pipeline-display-name>",
    pipelineDescription: "<pipeline-description>",
    pipelineDefinition: {
        pipelineDefinitionS3Location: {
            bucket: "<S3-bucket-location>",
            key: "<S3-bucket-key>",
        },
    },
    roleArn: "arn:aws:iam::<account-id>:root",
});

```


{{< /example >}}





{{% /examples %}}




## Create a Pipeline Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">Pipeline</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">PipelineArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Pipeline</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
             <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
             <span class="nx">pipeline_definition</span><span class="p">:</span> <span class="nx">Optional[Any]</span> = None<span class="p">,</span>
             <span class="nx">pipeline_description</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
             <span class="nx">pipeline_display_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
             <span class="nx">pipeline_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
             <span class="nx">role_arn</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
             <span class="nx">tags</span><span class="p">:</span> <span class="nx">Optional[Sequence[PipelineTagArgs]]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">Pipeline</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
             <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">PipelineArgs</a></span><span class="p">,</span>
             <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewPipeline</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">PipelineArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">Pipeline</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">Pipeline</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">PipelineArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">PipelineArgs</a></span>
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
        <span class="property-type"><a href="#inputs">PipelineArgs</a></span>
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
        <span class="property-type"><a href="#inputs">PipelineArgs</a></span>
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
        <span class="property-type"><a href="#inputs">PipelineArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## Pipeline Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The Pipeline resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="pipelinedefinition_csharp">
<a href="#pipelinedefinition_csharp" style="color: inherit; text-decoration: inherit;">Pipeline<wbr>Definition</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">object</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="pipelinename_csharp">
<a href="#pipelinename_csharp" style="color: inherit; text-decoration: inherit;">Pipeline<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Pipeline.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rolearn_csharp">
<a href="#rolearn_csharp" style="color: inherit; text-decoration: inherit;">Role<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Role Arn{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="pipelinedescription_csharp">
<a href="#pipelinedescription_csharp" style="color: inherit; text-decoration: inherit;">Pipeline<wbr>Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the Pipeline.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="pipelinedisplayname_csharp">
<a href="#pipelinedisplayname_csharp" style="color: inherit; text-decoration: inherit;">Pipeline<wbr>Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name of the Pipeline.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#pipelinetag">List&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>Sage<wbr>Maker.<wbr>Inputs.<wbr>Pipeline<wbr>Tag<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="pipelinedefinition_go">
<a href="#pipelinedefinition_go" style="color: inherit; text-decoration: inherit;">Pipeline<wbr>Definition</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">interface{}</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="pipelinename_go">
<a href="#pipelinename_go" style="color: inherit; text-decoration: inherit;">Pipeline<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Pipeline.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rolearn_go">
<a href="#rolearn_go" style="color: inherit; text-decoration: inherit;">Role<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Role Arn{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="pipelinedescription_go">
<a href="#pipelinedescription_go" style="color: inherit; text-decoration: inherit;">Pipeline<wbr>Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the Pipeline.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="pipelinedisplayname_go">
<a href="#pipelinedisplayname_go" style="color: inherit; text-decoration: inherit;">Pipeline<wbr>Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name of the Pipeline.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#pipelinetag">[]Pipeline<wbr>Tag<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="pipelinedefinition_nodejs">
<a href="#pipelinedefinition_nodejs" style="color: inherit; text-decoration: inherit;">pipeline<wbr>Definition</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">any</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="pipelinename_nodejs">
<a href="#pipelinename_nodejs" style="color: inherit; text-decoration: inherit;">pipeline<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the Pipeline.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rolearn_nodejs">
<a href="#rolearn_nodejs" style="color: inherit; text-decoration: inherit;">role<wbr>Arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Role Arn{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="pipelinedescription_nodejs">
<a href="#pipelinedescription_nodejs" style="color: inherit; text-decoration: inherit;">pipeline<wbr>Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the Pipeline.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="pipelinedisplayname_nodejs">
<a href="#pipelinedisplayname_nodejs" style="color: inherit; text-decoration: inherit;">pipeline<wbr>Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name of the Pipeline.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#pipelinetag">Pipeline<wbr>Tag<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="pipeline_definition_python">
<a href="#pipeline_definition_python" style="color: inherit; text-decoration: inherit;">pipeline_<wbr>definition</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Any</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="pipeline_name_python">
<a href="#pipeline_name_python" style="color: inherit; text-decoration: inherit;">pipeline_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the Pipeline.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="role_arn_python">
<a href="#role_arn_python" style="color: inherit; text-decoration: inherit;">role_<wbr>arn</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Role Arn{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="pipeline_description_python">
<a href="#pipeline_description_python" style="color: inherit; text-decoration: inherit;">pipeline_<wbr>description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of the Pipeline.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="pipeline_display_name_python">
<a href="#pipeline_display_name_python" style="color: inherit; text-decoration: inherit;">pipeline_<wbr>display_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The display name of the Pipeline.{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#pipelinetag">Sequence[Pipeline<wbr>Tag<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the Pipeline resource produces the following output properties:



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



<h4 id="pipelinetag">Pipeline<wbr>Tag</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="key_csharp">
<a href="#key_csharp" style="color: inherit; text-decoration: inherit;">Key</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_csharp">
<a href="#value_csharp" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_go">
<a href="#value_go" style="color: inherit; text-decoration: inherit;">Value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_nodejs">
<a href="#value_nodejs" style="color: inherit; text-decoration: inherit;">value</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="value_python">
<a href="#value_python" style="color: inherit; text-decoration: inherit;">value</a>
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

