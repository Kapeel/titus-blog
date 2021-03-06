My 2nd attempt at teaching Web Development Concepts
###################################################

:author: C\. Titus Brown
:tags: python
:date: 2009-12-30
:slug: more-web-dev
:category: python


I just finished teaching `Concepts in Database-Backed Web Development
<http://ged.msu.edu/courses/2009-fall-cse-491/>`__ for the second time
-- the post-mortem from the first course is `here
<http://ivory.idyll.org/blog/dec-08/concepts-database-backed-web-programming.html>`__.

In the course, the students implement a reasonably complete HTTP
server from the socket library on up, and integrate CSS, JavaScript
(jQuery), and a little bit of databases into the mix.

This year I just about doubled the work load, making it a true
"senior-level" course.  Despite that, most students did pretty well,
in part because I let students make up a HW's worth of credit at the
end by implementing some additional features for a message board.

I only made a few changes in addition to the increased workload.

The primary change was that rather than focusing on an internal API of
my own design for the interfaces they needed to implement, I used a
subset of `the WSGI interface
<http://www.python.org/dev/peps/pep-0333/>`__, which meant that they
had a "good" interface to work with, could use wsgiref to serve their
WSGI apps, and could double-check my test WSGI apps against wsgiref to
see what and how my code should work.

I also outlined a simple message board system (`meeplib
<http://class.ged.idyll.org/svn/files/hw10/meeplib.py>`__ and
`meep_example_app
<http://class.ged.idyll.org/svn/files/hw10/meep_example_app.py>`__)
that I had them flesh out with registration, deletion, and
persistence.  This was so that they didn't have to put it all together
themselves but would get to play with some semi-real code.

Successes:
----------

Subversion worked way better this term.  Last year it was a FUBARred
mess; this year I had students develop in trunk and then 'tag' (using
svn copy) their HWs -- you know, a semi-real developmental model...

I used a fast-food service skit (based on Culver's, if you must know)
to demonstrate some of the basic issues involved in scalability on the
server side.  It was at least entertaining and a bit
informative... and since it is very hard to actually demonstrate
scalability issues in an intro course on Web development, I think
I should limit myself to this kind of discussion.

Largely because of meeplib, I think students have a basic idea of how
cookies, logins, authentication, persistence, redirects, etc. all work
together.

At least two or three students who were marginal at the beginning
pulled through quite nicely.  Success!

Major failures:
---------------

I don't know how to teach databases.  At all.

I didn't introduce the students to any real Web dev frameworks.

Students are generally lousy at writing clean code and I did not
challenge them in this regard at all.  More code reviews!?

I erred on the side of leniency with respect to sloppiness.  I often
gave students a chance to fix non-parsing code, missing files, etc.
It turns out this does not discourage sloppiness.  Next time I teach
this, students will get a Big Fat Zero when they hand in something
that doesn't function at all.

Major challenges:
-----------------

Many students suck at solving their own problems, even when allowed to
work in groups, use the Internet, etc.

Juniors, oddly enough, seem to do better in this course than seniors.
I think our CSE program trains students to expect well-spec'ed out
problems, and the cognitive dissonance from getting very loose
instructions handicaps them.

Testing.  Testing testing testing testing.  We basically don't teach it,
and I think I'm going to refocus the class around testing at the beginning.
This leads to...

Reading code.  Many students don't seem to be able to read code -- which
is one of the most important skills you will need as a progammer.

Coding speed.  I cringe at the thought of increasing the homeworks any more,
but it's hard to cover the stuff I want to cover without doing so, and the
students are (frankly) rather slow at coding.  Partly this is because they
don't know how to use the available tools well.

Concluding thoughts:
--------------------

The more I teach, the less I know about teaching and the less capable
I seem to be of teaching well.

These kind of "inductive" classes seem to be popular with a certain
subset (60% or more?) of students, who love tackling "real" programming
problems.  A disjoint subset (~20%) seem to be incapable of dealing with
this kind of problem.

Students need this kind of stuff.  Mission of CSE.

20%/60%/20%

--titus
