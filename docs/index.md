---
layout:     default
title:      Documentation
body_id:    docs
created_at: Fri Nov 30 15:29:01 +1030 2007
---

{{ page.title }}
================

<dl>
  <dt><a href="http://rubydoc.info/gems/dm-core/1.1.0/frames">API</a></dt>
  <dd>The API for the current gem release.</dd>
  <dt><a href="/why.html">Why DataMapper?</a></dt>
  <dd>If you haven't read this yet, you should, right now!</dd>
  <dt><a href="/getting-started.html">Getting Started</a></dt>
  <dd>A whirlwind tour of DM. This is the place to start if you haven't used the library before.</dd>
  <dt><a href="/datamapper-docs/docs/install.html">Common installation issues</a></dt>
  <dd>Troubleshooting installation, with instructions for specific platforms.</dd>
  <dt><a href="/datamapper-docs/docs/properties.html">Properties</a></dt>
  <dd>Properties declared in your model map to the fields in the database.</dd>
  <dt><a href="/datamapper-docs/docs/create_and_destroy.html">Creating, Saving, Updating and Destroying Records</a></dt>
  <dd>Obviously you're going to be doing a lot of this :)</dd>
  <dt><a href="/datamapper-docs/docs/validations.html">Validations</a></dt>
  <dd>Auto-validations, manual validations, contextual validations</dd>
  <dt><a href="/datamapper-docs/docs/find.html">Finding and Counting Records</a></dt>
  <dd>There are lots of nice ways to find records.</dd>
  <dt><a href="/datamapper-docs/docs/associations.html">Associations</a></dt>
  <dd>Models can be associated to each other in various ways using the <code>has</code> keyword</dd>
  <dt><a href="/datamapper-docs/docs/callbacks.html">Hooks</a></dt>
  <dd>Hooks, AKA Callbacks, allow you to "advise other methods" by running methods before or after calling other methods.</dd>
  <dt><a href="/datamapper-docs/docs/misc.html">Misc. Features</a></dt>
  <dd>Paranoia, Timezone Handling, Single Table Inheritance, and Multiple Repositories.</dd>
  <dt><a href="/datamapper-docs/docs/legacy.html">Working with Legacy Schemas</a></dt>
  <dd>Adapting data-store naming conventions to your own property names.</dd>
  <dt><a href="/datamapper-docs/docs/pitfalls.html">Common Pitfalls</a></dt>
  <dd>Solutions and work-arounds to common problems.</dd>
  <dt><a href="/datamapper-docs/docs/dm_more/">More</a></dt>
  <dd>Plugins galore for DataMapper.</dd>
</dl>

Documentarians Wanted!
----------------------

Want to help DataMapper, but don't know where to start? A great way to contribute is to help out in the documentation effort.

If you know of some interesting and useful functionality that isn't covered on [datamapper.org](http://datamapper.org), just go ahead and fork [datamapper.github.com](http://github.com/datamapper/datamapper.github.com), send us a pull request, and we'll merge it as fast as we can. If you want to contribute more, we can give you commit access to the repository right after that.

If you find some undocumented piece of code inside [dm-core](http://github.com/datamapper/dm-core) or any of the other [datamapper](http://github.com/datamapper) repositories, we would greatly appreciate it if you take the time to read and understand that code, fork the repository, add the necessary docs and send us a pull request. Again, we'll try to merge them as fast as we can.

Documentation Style
-------------------

DataMapper uses the YARD standard for RDoc documentation. Here's a brief sample
from the internals of DM-Core:

{% highlight ruby linenos %}
# Setups up a connection to a data-store
#
# @param [Symbol] name
#   a name for the context, defaults to :default
# @param [Hash(Symbol => String), Addressable::URI, String] uri_or_options
#   connection information
#
# @return [DataMapper::Adapters::AbstractAdapter]
#   the resulting setup adapter
#
# @raise [ArgumentError] "+name+ must be a Symbol, but was..."
#   indicates that an invalid argument was passed for name[Symbol]
# @raise [ArgumentError] "+uri_or_options+ must be a Hash, URI or String, but was..."
#   indicates that connection information could not be gleaned from
#   the given uri_or_options[Hash, Addressable::URI, String]
#
# @api public
def self.setup(name, uri_or_options)
  raise ArgumentError, "+name+ must be a Symbol, but was #{name.class}", caller unless Symbol === name
  #...
end
{% endhighlight %}

For more information about the YARD documentation style, see the YARD
[Getting Started](http://rubydoc.info/datamapper-docs/docs/yard/file/datamapper-docs/docs/GettingStarted.md) document.

* [YARD]: Yet Another Ruby Documentation (tool)
