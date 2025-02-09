
---
title: "PropertyVariables"
title_tag: "akamai.PropertyVariables"
meta_desc: "Documentation for the akamai.PropertyVariables resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->




## Create a PropertyVariables Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">PropertyVariables</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">?:</span> <span class="nx"><a href="#inputs">PropertyVariablesArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">PropertyVariables</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                      <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                      <span class="nx">variables</span><span class="p">:</span> <span class="nx">Optional[Sequence[PropertyVariablesVariableArgs]]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">PropertyVariables</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                      <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">Optional[PropertyVariablesArgs]</a></span> = None<span class="p">,</span>
                      <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewPropertyVariables</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx"><a href="#inputs">PropertyVariablesArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">PropertyVariables</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">PropertyVariables</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">PropertyVariablesArgs</a></span><span class="p">? </span><span class="nx">args = null<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language nodejs %}}

<dl class="resources-properties"><dt
        class="property-required" title="Required">
        <span>name</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>The unique name of the resource.</dd><dt
        class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">PropertyVariablesArgs</a></span>
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
        class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">PropertyVariablesArgs</a></span>
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
        class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">PropertyVariablesArgs</a></span>
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
        class="property-optional" title="Optional">
        <span>args</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#inputs">PropertyVariablesArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## PropertyVariables Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The PropertyVariables resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span id="variables_csharp">
<a href="#variables_csharp" style="color: inherit; text-decoration: inherit;">Variables</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#propertyvariablesvariable">List&lt;Property<wbr>Variables<wbr>Variable<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}The setting &#34;akamai_property_variables&#34; has been deprecated.{{% /md %}}</p></dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span id="variables_go">
<a href="#variables_go" style="color: inherit; text-decoration: inherit;">Variables</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#propertyvariablesvariable">[]Property<wbr>Variables<wbr>Variable<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}The setting &#34;akamai_property_variables&#34; has been deprecated.{{% /md %}}</p></dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span id="variables_nodejs">
<a href="#variables_nodejs" style="color: inherit; text-decoration: inherit;">variables</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#propertyvariablesvariable">Property<wbr>Variables<wbr>Variable<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}The setting &#34;akamai_property_variables&#34; has been deprecated.{{% /md %}}</p></dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span id="variables_python">
<a href="#variables_python" style="color: inherit; text-decoration: inherit;">variables</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#propertyvariablesvariable">Sequence[Property<wbr>Variables<wbr>Variable<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}The setting &#34;akamai_property_variables&#34; has been deprecated.{{% /md %}}</p></dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the PropertyVariables resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="json_csharp">
<a href="#json_csharp" style="color: inherit; text-decoration: inherit;">Json</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}JSON variables representation
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="json_go">
<a href="#json_go" style="color: inherit; text-decoration: inherit;">Json</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}JSON variables representation
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="json_nodejs">
<a href="#json_nodejs" style="color: inherit; text-decoration: inherit;">json</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}JSON variables representation
{{% /md %}}</dd></dl>
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
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="json_python">
<a href="#json_python" style="color: inherit; text-decoration: inherit;">json</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}JSON variables representation
{{% /md %}}</dd></dl>
{{% /choosable %}}



## Look up an Existing PropertyVariables Resource {#look-up}

Get an existing PropertyVariables resource's state with the given name, ID, and optional extra properties used to qualify the lookup.
{{< chooser language "typescript,python,go,csharp" / >}}

{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">public static </span><span class="nf">get</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#ID">Input&lt;ID&gt;</a></span><span class="p">,</span> <span class="nx">state</span><span class="p">?:</span> <span class="nx">PropertyVariablesState</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">): </span><span class="nx">PropertyVariables</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@staticmethod</span>
<span class="k">def </span><span class="nf">get</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">id</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
        <span class="nx">json</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
        <span class="nx">variables</span><span class="p">:</span> <span class="nx">Optional[Sequence[PropertyVariablesVariableArgs]]</span> = None<span class="p">) -&gt;</span> PropertyVariables</code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetPropertyVariables<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">id</span><span class="p"> </span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#IDInput">IDInput</a></span><span class="p">,</span> <span class="nx">state</span><span class="p"> *</span><span class="nx">PropertyVariablesState</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">PropertyVariables</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static </span><span class="nx">PropertyVariables</span><span class="nf"> Get</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.Input-1.html">Input&lt;string&gt;</a></span><span class="p"> </span><span class="nx">id<span class="p">,</span> <span class="nx">PropertyVariablesState</span><span class="p">? </span><span class="nx">state<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span id="state_json_csharp">
<a href="#state_json_csharp" style="color: inherit; text-decoration: inherit;">Json</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}JSON variables representation
{{% /md %}}</dd><dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span id="state_variables_csharp">
<a href="#state_variables_csharp" style="color: inherit; text-decoration: inherit;">Variables</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#propertyvariablesvariable">List&lt;Property<wbr>Variables<wbr>Variable<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}The setting &#34;akamai_property_variables&#34; has been deprecated.{{% /md %}}</p></dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_json_go">
<a href="#state_json_go" style="color: inherit; text-decoration: inherit;">Json</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}JSON variables representation
{{% /md %}}</dd><dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span id="state_variables_go">
<a href="#state_variables_go" style="color: inherit; text-decoration: inherit;">Variables</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#propertyvariablesvariable">[]Property<wbr>Variables<wbr>Variable<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}The setting &#34;akamai_property_variables&#34; has been deprecated.{{% /md %}}</p></dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_json_nodejs">
<a href="#state_json_nodejs" style="color: inherit; text-decoration: inherit;">json</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}JSON variables representation
{{% /md %}}</dd><dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span id="state_variables_nodejs">
<a href="#state_variables_nodejs" style="color: inherit; text-decoration: inherit;">variables</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#propertyvariablesvariable">Property<wbr>Variables<wbr>Variable<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}The setting &#34;akamai_property_variables&#34; has been deprecated.{{% /md %}}</p></dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="state_json_python">
<a href="#state_json_python" style="color: inherit; text-decoration: inherit;">json</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}JSON variables representation
{{% /md %}}</dd><dt class="property-optional property-deprecated"
            title="Optional, Deprecated">
        <span id="state_variables_python">
<a href="#state_variables_python" style="color: inherit; text-decoration: inherit;">variables</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#propertyvariablesvariable">Sequence[Property<wbr>Variables<wbr>Variable<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}<p class="property-message">Deprecated: {{% md %}}The setting &#34;akamai_property_variables&#34; has been deprecated.{{% /md %}}</p></dd></dl>
{{% /choosable %}}






## Supporting Types



<h4 id="propertyvariablesvariable">Property<wbr>Variables<wbr>Variable</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="variables_csharp">
<a href="#variables_csharp" style="color: inherit; text-decoration: inherit;">Variables</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#propertyvariablesvariablevariable">List&lt;Property<wbr>Variables<wbr>Variable<wbr>Variable&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="variables_go">
<a href="#variables_go" style="color: inherit; text-decoration: inherit;">Variables</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#propertyvariablesvariablevariable">[]Property<wbr>Variables<wbr>Variable<wbr>Variable</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="variables_nodejs">
<a href="#variables_nodejs" style="color: inherit; text-decoration: inherit;">variables</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#propertyvariablesvariablevariable">Property<wbr>Variables<wbr>Variable<wbr>Variable[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="variables_python">
<a href="#variables_python" style="color: inherit; text-decoration: inherit;">variables</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#propertyvariablesvariablevariable">Sequence[Property<wbr>Variables<wbr>Variable<wbr>Variable]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="propertyvariablesvariablevariable">Property<wbr>Variables<wbr>Variable<wbr>Variable</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="hidden_csharp">
<a href="#hidden_csharp" style="color: inherit; text-decoration: inherit;">Hidden</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="sensitive_csharp">
<a href="#sensitive_csharp" style="color: inherit; text-decoration: inherit;">Sensitive</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
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
        <span id="hidden_go">
<a href="#hidden_go" style="color: inherit; text-decoration: inherit;">Hidden</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="sensitive_go">
<a href="#sensitive_go" style="color: inherit; text-decoration: inherit;">Sensitive</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
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
        <span id="hidden_nodejs">
<a href="#hidden_nodejs" style="color: inherit; text-decoration: inherit;">hidden</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="sensitive_nodejs">
<a href="#sensitive_nodejs" style="color: inherit; text-decoration: inherit;">sensitive</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
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
        <span id="hidden_python">
<a href="#hidden_python" style="color: inherit; text-decoration: inherit;">hidden</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="sensitive_python">
<a href="#sensitive_python" style="color: inherit; text-decoration: inherit;">sensitive</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
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
	<dd><a href="https://github.com/pulumi/pulumi-akamai">https://github.com/pulumi/pulumi-akamai</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`akamai` Terraform Provider](https://github.com/akamai/terraform-provider-akamai).{{% /md %}}</dd>
</dl>

