## Language

* Whats the difference between an abstract class and interface? When would you want to use them?
* What's the difference between overriding and overloading a method? Explain how both are done.
* What's the difference between protected and internal? What about "protected internal"?
* How do short-circuited operators work?
* What's the difference between a static method and a non-static method?
* What does the "volatile" keyword in C# mean?
* Explain what happens when you pass a `ref` or `out` parameter into a method. What's the difference between those two keywords?
* What's a weakreference? When would you want to use one?
* What's the difference between a value-type and a reference type?
* What does the "readonly" keyword in C# mean?
* What is strong-typing versus weak-typing?

## General

* What is the difference between a thread and a process?
* What is the difference between an EXE and a DLL?

* What is the difference between a.Equals(b) and a == b?
* What is boxing?
* Is string a value type or a reference type?

* What is the Global Assembly Cache (GAC)? What problem does it solve?
* What is FullTrust? Do GAC’ed assemblies have FullTrust?

* What is Reflection?
* Conceptually, what is the difference between early-binding and late-binding?
* When would using Assembly.LoadFrom or Assembly.LoadFile be appropriate?
* What is an Asssembly Qualified Name? Is it a filename? How is it different?
* How is a strongly-named assembly different from one that isn’t strongly-named?
* What does this do? sn -t foo.dll

* How does the generational garbage collector in the .NET CLR manage object lifetime? What is non-deterministic finalization?
* What is the difference between Finalize() and Dispose()? (external article)
* What is the difference between in-proc and out-of-proc? What technology enables out-of-proc communication in .NET?

* What is the difference between Debug.Write and Trace.Write? When should each be used?
* What is the difference between a Debug and Release build? Is there a significant speed difference? Why or why not?
* What is the difference between: catch (Exception e) {throw e;} and catch (Exception e) {throw;} ?
* What is the difference between typeof(foo) and myFoo.GetType()?

## ASP.NET

* What is a PostBack?
* What is ViewState? 
    * How is it encoded? 
    * Is it encrypted? 
    * Who uses ViewState? 
    * Why is it either useful or evil?

* What Session State providers are available in ASP.NET? 
    * What are the pros and cons of each?
    
* What is the OO relationship between an ASPX page and its CS/VB code behind file?
* How would one implement ASP.NET HTML output caching, caching outgoing versions of pages generated via all values of q= except where q=5 (as in http://localhost/page.aspx?q=5)?
* What are HttpHandlers?
* What are HttpModules?
* What is needed to configure a new extension for use in ASP.NET? 
For example, what if I wanted my system to serve ASPX files with a *.jsp extension?

* What kind of data is passed via HTTP Headers?
* How do cookies work? 
* What is an example of Cookie abuse?

* How does IIS communicate at runtime with ASP.NET? 
* Where is ASP.NET at runtime in the different versions of IIS (5 to 7)?

## ASP.NET MVC

* What is MVC (Model view controller)?
* Explain MVC application life cycle?
* Is MVC suitable for both Windows and web applications?
* What are the benefits of using MVC?
* Is MVC different from a three layered architecture?

* What is the latest version of MVC?
* What is the difference between each version of MVC 2, 3 , 4, 5 and 6?
* What are HTML helpers in MVC?
* What is the difference between `HTML.TextBox` vs `HTML.TextBoxFor`?

* What is routing in MVC?
* Where is the route mapping code written?
* Can we map multiple URLs to the same action?
* Explain attribute based routing in MVC?
* What is the advantage of defining route structures in the code?
* How can we navigate from one view to other view using a hyperlink?

* How can we restrict MVC actions to be invoked only by GET or POST?

* How can we maintain sessions in MVC?

* What is the difference between `TempData`, `ViewData`, and `ViewBag`?
* What is the use of Keep and Peek in “TempData”?

* What are partial views in MVC?
* How do you create a partial view and consume it?

* How can we do validations in MVC?
* Can we display all errors in one go?
* How can we enable data annotation validation on the client side?

* What is Razor in MVC?
* Why Razor when we already have ASPX?
* So which is a better fit, Razor or ASPX?

* How can you do authentication and authorization in MVC?
* How to implement Windows authentication for MVC?
* How do you implement Forms authentication in MVC?

* How to implement AJAX in MVC
* What kind of events can be tracked in AJAX?

* What are the different types of results in MVC?
* What is the difference between `ActionResult` and `ViewResult`?
* What are ActionFilters in MVC?

* Can we create our own custom view engine using MVC?
* How to send result back in JSON format in MVC

* What is WebAPI?
    * But WCF SOAP also does the same thing, so how does WebAPI differ?
    * With WCF you can implement REST, so why WebAPI?

* How can we detect that a MVC controller is called by POST or GET?

* What is Bundling and Minification in MVC?
* How does bundling increase performance?
* How do we implement bundling in MVC?
* How can you test bundling in debug mode?
* Explain minification and how to implement it
* How do we implement minification?

* Explain Areas in MVC?
* Explain the concept of View Model in MVC?
* What kind of logic view model class will have?
* How can we use two ( multiple) models with a single view?
* Explain the need of display mode in MVC?
* Explain MVC model binders?

* Explain the concept of MVC Scaffolding?
* What does scaffolding use internally to connect to database?

* How can we do exception handling in MVC?
* How can you handle multiple Submit buttons pointing to multiple actions in a single MVC view?
