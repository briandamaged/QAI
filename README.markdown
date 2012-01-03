QAI QTP Automation Infrastructure
===================================

This is a QTP framework that I developed about 2 years ago
during Washington DC's Snowmageddon.  It allows end-users
to overcome many of the common annoyances w/ QTP, such as:

* Massive code duplication
* Fragile Object Repositories
* The complete absence of high-level testing

This framework promotes the practice of creating Application
Models prior to testing.  Like QTP's Object Repositories,
these models allow end-users to specify which UI components
they expect to see during the testing.  However, these models
provide several other capabilities that are absent from
Object Repositories, including:

* The ability to create self-extending models based upon
generic patterns.  For instance, on a blog page, you don't
necessarily know how many blog posts there will be, who
the authors are, the specific content, etc.  You just know
"This page will contain several Blog Posts, and each Blog
Post has this generic structure."  QAI will use these descriptions
to generate the appropriate object models on-demand at runtime.

* The ability to inject meaningful methods into the runtime
object models.  For example, you can define a "LeaveComment(...)"
method on a BlogPost object.  Hence, QAI supports the
object-oriented programming paradigm.

* The ability to query the model quickly and easily.  For
instance, all of the following can be achieved in a single
line of code:
** Find all blog posts written by Brian Lauber
** From these, find all posts that are longer than 200 words
** For each of these, send a comment that says "You're blog
posts are way too long!  You suck!"

* The ability to encapsulate cross-cutting testing patterns
that can be reused across all applications and tests.  For
instance: "Navigate to a page and verify that all objects
are satisfying their visibility requirements."  Your script
doesn't need to explicitly indicate which components are
supposed to be visible/invisible.  It can read the requirements
from the model, compile these into code, and guarantee that
the tests will be executed correctly.

Alright, that should be enough to whet your appetites.  Enjoy!
