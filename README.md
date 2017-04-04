Symfony3-Bootstrap3.3.7
===================

This Bundle could be used to integrate [Bootstrap 3.3.7](http://getbootstrap.com) with Symfony 3 v3.2.6. The Bundle also includes [jQuery 3.2.1](https://jquery.com/) from a CDN with a local fallback

Instalation
---------------

Add the project to your composer file.

<dl>
	<dt>composer.json</dt>
	<dd>
	<pre>
"repositories": [
    {
        "type" : "git",
        "url": "https://github.com/mihaiureche/symfony3-bootstrap3.git",
    }
],
    </pre>
	</dd>
	<dd><pre>
"require": {
    "mihaiureche/symfony3-bootstrap3": "0.*"
}
	</pre></dd>
</dl>

Add the Bootstrap bundle to AppKernal and include the template.

<dl>
	<dt>/app/AppKernel.php</dt>
	<dd><pre>new MU\Bundle\BootstrapBundle\BootstrapBundle()</pre></dd>
	<dt>/app/Resources/views/base.html.twig</dt>
	<dd><pre>{% extends 'BootstrapBundle::base.html.twig' %}</pre></dd>
</dl>

Defined Blocks
-------------------

<dl>
	<dt>{% block meta %}</dt>
	<dd>Contains base <meta> html tags.</dd>
	<dt>{% block stylesheets %}</dt>
	<dd>Contains base styles for Bootstrap bundle. Implement {{ parent() }} when overriding.</dd>
	<dt>{% block title %}</dt>
	<dd>Contains the page meta title.</dd>
	<dt>{% block nav %}</dt>
	<dd>Optional block before the content, outside of the container, but inside the wrap.</dd>
	<dt>{% block body %}</dt>
	<dd>Wrapper for the container.</dd>
	<dt>{% block header %}</dt>
	<dd>Adds a header before the content area.</dd>
	<dt>{% block content %}</dt>
	<dd>Base content area inside the container.</dd>
	<dt>{% block footer %}</dt>
	<dd>Optional block after the content, outside the container and wrap.</dd>
	<dt>{% block javascripts %}</dt>
	<dd>Contains base javascript for Bootstrap bundle. Implement {{ parent() }} when overridding.</dd>
</dl>