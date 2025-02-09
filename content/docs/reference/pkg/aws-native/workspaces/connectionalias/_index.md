
---
title: "ConnectionAlias"
title_tag: "aws-native.workspaces.ConnectionAlias"
meta_desc: "Documentation for the aws-native.workspaces.ConnectionAlias resource with examples, input properties, output properties, lookup functions, and supporting types."
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Resource Type definition for AWS::WorkSpaces::ConnectionAlias




## Create a ConnectionAlias Resource {#create}
{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new </span><span class="nx">ConnectionAlias</span><span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">ConnectionAliasArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions">CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>
{{% /choosable %}}

{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class=nd>@overload</span>
<span class="k">def </span><span class="nx">ConnectionAlias</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                    <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">,</span>
                    <span class="nx">connection_string</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">tags</span><span class="p">:</span> <span class="nx">Optional[Sequence[ConnectionAliasTagArgs]]</span> = None<span class="p">)</span>
<span class=nd>@overload</span>
<span class="k">def </span><span class="nx">ConnectionAlias</span><span class="p">(</span><span class="nx">resource_name</span><span class="p">:</span> <span class="nx">str</span><span class="p">,</span>
                    <span class="nx">args</span><span class="p">:</span> <span class="nx"><a href="#inputs">ConnectionAliasArgs</a></span><span class="p">,</span>
                    <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.ResourceOptions">Optional[ResourceOptions]</a></span> = None<span class="p">)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span><span class="nx">NewConnectionAlias</span><span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">name</span><span class="p"> </span><span class="nx">string</span><span class="p">,</span> <span class="nx">args</span><span class="p"> </span><span class="nx"><a href="#inputs">ConnectionAliasArgs</a></span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#ResourceOption">ResourceOption</a></span><span class="p">) (*<span class="nx">ConnectionAlias</span>, error)</span></code></pre></div>
{{% /choosable %}}

{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public </span><span class="nx">ConnectionAlias</span><span class="p">(</span><span class="nx">string</span><span class="p"> </span><span class="nx">name<span class="p">,</span> <span class="nx"><a href="#inputs">ConnectionAliasArgs</a></span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span></code></pre></div>
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
        <span class="property-type"><a href="#inputs">ConnectionAliasArgs</a></span>
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
        <span class="property-type"><a href="#inputs">ConnectionAliasArgs</a></span>
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
        <span class="property-type"><a href="#inputs">ConnectionAliasArgs</a></span>
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
        <span class="property-type"><a href="#inputs">ConnectionAliasArgs</a></span>
    </dt>
    <dd>The arguments to resource properties.</dd><dt
        class="property-optional" title="Optional">
        <span>opts</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.CustomResourceOptions.html">CustomResourceOptions</a></span>
    </dt>
    <dd>Bag of options to control resource&#39;s behavior.</dd></dl>

{{% /choosable %}}

## ConnectionAlias Resource Properties {#properties}

To learn more about resource properties and how to use them, see [Inputs and Outputs]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) in the Architecture and Concepts docs.

### Inputs

The ConnectionAlias resource accepts the following [input]({{< relref "/docs/intro/concepts/inputs-outputs" >}}) properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="connectionstring_csharp">
<a href="#connectionstring_csharp" style="color: inherit; text-decoration: inherit;">Connection<wbr>String</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_csharp">
<a href="#tags_csharp" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliastag">List&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>Work<wbr>Spaces.<wbr>Inputs.<wbr>Connection<wbr>Alias<wbr>Tag<wbr>Args&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="connectionstring_go">
<a href="#connectionstring_go" style="color: inherit; text-decoration: inherit;">Connection<wbr>String</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_go">
<a href="#tags_go" style="color: inherit; text-decoration: inherit;">Tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliastag">[]Connection<wbr>Alias<wbr>Tag<wbr>Args</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="connectionstring_nodejs">
<a href="#connectionstring_nodejs" style="color: inherit; text-decoration: inherit;">connection<wbr>String</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_nodejs">
<a href="#tags_nodejs" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliastag">Connection<wbr>Alias<wbr>Tag<wbr>Args[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="connection_string_python">
<a href="#connection_string_python" style="color: inherit; text-decoration: inherit;">connection_<wbr>string</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="tags_python">
<a href="#tags_python" style="color: inherit; text-decoration: inherit;">tags</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliastag">Sequence[Connection<wbr>Alias<wbr>Tag<wbr>Args]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}


### Outputs

All [input](#inputs) properties are implicitly available as output properties. Additionally, the ConnectionAlias resource produces the following output properties:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="aliasid_csharp">
<a href="#aliasid_csharp" style="color: inherit; text-decoration: inherit;">Alias<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="associations_csharp">
<a href="#associations_csharp" style="color: inherit; text-decoration: inherit;">Associations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliasconnectionaliasassociation">List&lt;Pulumi.<wbr>Aws<wbr>Native.<wbr>Work<wbr>Spaces.<wbr>Outputs.<wbr>Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association&gt;</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="connectionaliasstate_csharp">
<a href="#connectionaliasstate_csharp" style="color: inherit; text-decoration: inherit;">Connection<wbr>Alias<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliasconnectionaliasstate">Pulumi.<wbr>Aws<wbr>Native.<wbr>Work<wbr>Spaces.<wbr>Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>State</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="aliasid_go">
<a href="#aliasid_go" style="color: inherit; text-decoration: inherit;">Alias<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="associations_go">
<a href="#associations_go" style="color: inherit; text-decoration: inherit;">Associations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliasconnectionaliasassociation">[]Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="connectionaliasstate_go">
<a href="#connectionaliasstate_go" style="color: inherit; text-decoration: inherit;">Connection<wbr>Alias<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliasconnectionaliasstate">Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>State</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="aliasid_nodejs">
<a href="#aliasid_nodejs" style="color: inherit; text-decoration: inherit;">alias<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="associations_nodejs">
<a href="#associations_nodejs" style="color: inherit; text-decoration: inherit;">associations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliasconnectionaliasassociation">Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association[]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="connectionaliasstate_nodejs">
<a href="#connectionaliasstate_nodejs" style="color: inherit; text-decoration: inherit;">connection<wbr>Alias<wbr>State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliasconnectionaliasstate">Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>State</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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
        <span id="alias_id_python">
<a href="#alias_id_python" style="color: inherit; text-decoration: inherit;">alias_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="associations_python">
<a href="#associations_python" style="color: inherit; text-decoration: inherit;">associations</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliasconnectionaliasassociation">Sequence[Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association]</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="connection_alias_state_python">
<a href="#connection_alias_state_python" style="color: inherit; text-decoration: inherit;">connection_<wbr>alias_<wbr>state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliasconnectionaliasstate">Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>State</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
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



<h4 id="connectionaliasconnectionaliasassociation">Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association</h4>

{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="associatedaccountid_csharp">
<a href="#associatedaccountid_csharp" style="color: inherit; text-decoration: inherit;">Associated<wbr>Account<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="associationstatus_csharp">
<a href="#associationstatus_csharp" style="color: inherit; text-decoration: inherit;">Association<wbr>Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliasconnectionaliasassociationassociationstatus">Pulumi.<wbr>Aws<wbr>Native.<wbr>Work<wbr>Spaces.<wbr>Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association<wbr>Association<wbr>Status</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="connectionidentifier_csharp">
<a href="#connectionidentifier_csharp" style="color: inherit; text-decoration: inherit;">Connection<wbr>Identifier</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="resourceid_csharp">
<a href="#resourceid_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="associatedaccountid_go">
<a href="#associatedaccountid_go" style="color: inherit; text-decoration: inherit;">Associated<wbr>Account<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="associationstatus_go">
<a href="#associationstatus_go" style="color: inherit; text-decoration: inherit;">Association<wbr>Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliasconnectionaliasassociationassociationstatus">Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association<wbr>Association<wbr>Status</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="connectionidentifier_go">
<a href="#connectionidentifier_go" style="color: inherit; text-decoration: inherit;">Connection<wbr>Identifier</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="resourceid_go">
<a href="#resourceid_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="associatedaccountid_nodejs">
<a href="#associatedaccountid_nodejs" style="color: inherit; text-decoration: inherit;">associated<wbr>Account<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="associationstatus_nodejs">
<a href="#associationstatus_nodejs" style="color: inherit; text-decoration: inherit;">association<wbr>Status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliasconnectionaliasassociationassociationstatus">Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association<wbr>Association<wbr>Status</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="connectionidentifier_nodejs">
<a href="#connectionidentifier_nodejs" style="color: inherit; text-decoration: inherit;">connection<wbr>Identifier</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="resourceid_nodejs">
<a href="#resourceid_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-optional"
            title="Optional">
        <span id="associated_account_id_python">
<a href="#associated_account_id_python" style="color: inherit; text-decoration: inherit;">associated_<wbr>account_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="association_status_python">
<a href="#association_status_python" style="color: inherit; text-decoration: inherit;">association_<wbr>status</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#connectionaliasconnectionaliasassociationassociationstatus">Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association<wbr>Association<wbr>Status</a></span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="connection_identifier_python">
<a href="#connection_identifier_python" style="color: inherit; text-decoration: inherit;">connection_<wbr>identifier</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="resource_id_python">
<a href="#resource_id_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

<h4 id="connectionaliasconnectionaliasassociationassociationstatus">Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association<wbr>Association<wbr>Status</h4>

{{% choosable language csharp %}}
<dl class="tabular"><dt>Not<wbr>Associated</dt>
    <dd>NOT_ASSOCIATED</dd><dt>Pending<wbr>Association</dt>
    <dd>PENDING_ASSOCIATION</dd><dt>Associated<wbr>With<wbr>Owner<wbr>Account</dt>
    <dd>ASSOCIATED_WITH_OWNER_ACCOUNT</dd><dt>Associated<wbr>With<wbr>Shared<wbr>Account</dt>
    <dd>ASSOCIATED_WITH_SHARED_ACCOUNT</dd><dt>Pending<wbr>Disassociation</dt>
    <dd>PENDING_DISASSOCIATION</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="tabular"><dt>Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association<wbr>Association<wbr>Status<wbr>Not<wbr>Associated</dt>
    <dd>NOT_ASSOCIATED</dd><dt>Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association<wbr>Association<wbr>Status<wbr>Pending<wbr>Association</dt>
    <dd>PENDING_ASSOCIATION</dd><dt>Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association<wbr>Association<wbr>Status<wbr>Associated<wbr>With<wbr>Owner<wbr>Account</dt>
    <dd>ASSOCIATED_WITH_OWNER_ACCOUNT</dd><dt>Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association<wbr>Association<wbr>Status<wbr>Associated<wbr>With<wbr>Shared<wbr>Account</dt>
    <dd>ASSOCIATED_WITH_SHARED_ACCOUNT</dd><dt>Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>Association<wbr>Association<wbr>Status<wbr>Pending<wbr>Disassociation</dt>
    <dd>PENDING_DISASSOCIATION</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="tabular"><dt>Not<wbr>Associated</dt>
    <dd>NOT_ASSOCIATED</dd><dt>Pending<wbr>Association</dt>
    <dd>PENDING_ASSOCIATION</dd><dt>Associated<wbr>With<wbr>Owner<wbr>Account</dt>
    <dd>ASSOCIATED_WITH_OWNER_ACCOUNT</dd><dt>Associated<wbr>With<wbr>Shared<wbr>Account</dt>
    <dd>ASSOCIATED_WITH_SHARED_ACCOUNT</dd><dt>Pending<wbr>Disassociation</dt>
    <dd>PENDING_DISASSOCIATION</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="tabular"><dt>NOT_ASSOCIATED</dt>
    <dd>NOT_ASSOCIATED</dd><dt>PENDING_ASSOCIATION</dt>
    <dd>PENDING_ASSOCIATION</dd><dt>ASSOCIATED_WITH_OWNER_ACCOUNT</dt>
    <dd>ASSOCIATED_WITH_OWNER_ACCOUNT</dd><dt>ASSOCIATED_WITH_SHARED_ACCOUNT</dt>
    <dd>ASSOCIATED_WITH_SHARED_ACCOUNT</dd><dt>PENDING_DISASSOCIATION</dt>
    <dd>PENDING_DISASSOCIATION</dd></dl>
{{% /choosable %}}

<h4 id="connectionaliasconnectionaliasstate">Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>State</h4>

{{% choosable language csharp %}}
<dl class="tabular"><dt>Creating</dt>
    <dd>CREATING</dd><dt>Created</dt>
    <dd>CREATED</dd><dt>Deleting</dt>
    <dd>DELETING</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="tabular"><dt>Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>State<wbr>Creating</dt>
    <dd>CREATING</dd><dt>Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>State<wbr>Created</dt>
    <dd>CREATED</dd><dt>Connection<wbr>Alias<wbr>Connection<wbr>Alias<wbr>State<wbr>Deleting</dt>
    <dd>DELETING</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="tabular"><dt>Creating</dt>
    <dd>CREATING</dd><dt>Created</dt>
    <dd>CREATED</dd><dt>Deleting</dt>
    <dd>DELETING</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="tabular"><dt>CREATING</dt>
    <dd>CREATING</dd><dt>CREATED</dt>
    <dd>CREATED</dd><dt>DELETING</dt>
    <dd>DELETING</dd></dl>
{{% /choosable %}}

<h4 id="connectionaliastag">Connection<wbr>Alias<wbr>Tag</h4>

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

