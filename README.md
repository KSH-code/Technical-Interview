## Purpose

- 2021.01.07. I am going to share Posts are grouped by date that I read.
- 2020.11.22. I am going to share posts I read with summary.

## 2021.05.31.

- [What Is MJIT in Ruby 2.6 & How Does It Work?](https://www.rubyguides.com/2018/11/ruby-mjit/)
  - It explains that MJIT is method based just in time compiler as simple.
  - [A look at how Ruby interprets your code](https://blog.appsignal.com/2017/08/01/ruby-magic-code-interpretation.html)
    - If you do not know about MJIT how it works, read this first. and you are into optimization, next up is [Tail Call Optimization in Ruby](https://nithinbekal.com/posts/ruby-tco/)
      - TCO is really intersting to me.
      - If you are intersted in algorithm problems, you may know TCO, is because stack overflow is occured in many recursion problems.
  - Get back to MJIT, Koichi Sasada's report is intersting "YARV: Yet Another RubyVM". I don't know its copyright so I just share the title.
  - Finally, we should know about MJIT. So what?
  - The real important thing is Ruby may not be used without any library such as Rails.
  - Ultimately, I was wondering if Ruby uses JIT, then RoR performance is better than that without JIT.
  - [Ruby 3 JIT can make Rails faster](https://k0kubun.medium.com/ruby-3-jit-can-make-rails-faster-756310f235a) Here is helper to solve my problem.
  - My conclusion is that we should not use RoR with JIT yet. Because it is unstable. However I think that metric of method usage would be better that it without JIT in the future.

## 2021.04.29.

- [Flaky Tests at Google and How We Mitigate Them](https://testing.googleblog.com/2016/05/flaky-tests-at-google-and-how-we.html)
  - Most of developers will probabaly be facing flaky test.
  - this is about google's story that how they migrate.
  - it is saying that system to monitor and for fast solve are important.
- [Test Flakiness - One of the main challenges of automated testing](https://testing.googleblog.com/2020/12/test-flakiness-one-of-main-challenges.html)
  - following post is saying about flaky causes.
- [Test Flakiness - One of the main challenges of automated testing (Part II)](https://testing.googleblog.com/2021/03/test-flakiness-one-of-main-challenges.html)
  - in now, last following post, is saying flaky causes.
  - how to solve that and suggest guidelines.

## 2021.04.08.

- [Beware of “service objects” in Rails](https://www.codewithjason.com/rails-service-objects/)
  - today, I did not read articles about GC. but I was interested in.
  - because I misbelieve service object in Rails, as you know too many classes created.
  - to break down fat model is good for readability. but too many files incur similar problems.
  - anyway, it says service object is not solution.
  - and include good links to understand background.
  - [Don't Create Objects That End With -ER](https://www.yegor256.com/2015/03/09/objects-end-with-er.html)
  - [AnemicDomainModel](https://martinfowler.com/bliki/AnemicDomainModel.html)
    - I used to be hard to understand this. because of unfarmiliar terms.
    - but the point is like service object is bad one.
  - [Enough With the Service Objects Already](https://avdi.codes/service-objects/)
  - [Martin Fowler on Service Objects via the Ruby Rogues Parley mailing list](https://gist.github.com/blaix/5764401)
  - [How I code without service objects](https://www.codewithjason.com/code-without-service-objects/)
  - [What is a Rails model?](https://www.codewithjason.com/what-is-a-rails-model/)
  - too long, I can not sum-up.

## 2021.04.04.

- [Ruby Garbage Collection Deep Dive: Generational Garbage Collection](https://jemma.dev/blog/gc-generational)
  - Again, this is saying GC.
  - It explains GC generational such as young object and old object. I've not heared ever.
  - Anyway, that also include many terms be good.
  - I've understood what Minor GC is and Major GC is. However I want to know write barriers how actully works.
  - so I did surf using many terms to know it. and finally I found [Peter's Adventures in Ruby: Garbage Collection in Ruby](https://blog.peterzhu.ca/notes-on-ruby-gc/).
  - intersting! this explains a little about compaction and write barriers in detail. and also include another article [Incremental Garbage Collection in Ruby 2.2](https://blog.heroku.com/incremental-gc).
  - sum-up, the first article is to summerize about GC, and the second article explains GC in detail using GC and many figures. the final article explains.
  - the next step is reading [Copying Garbage Collection](https://www.cs.cornell.edu/courses/cs312/2003fa/lectures/sec24.htm) and understanding ruby GC.start how works.

## 2021.03.22.

- [Ruby Garbage Collection Deep Dive: GC::INTERNAL_CONSTANTS](https://jemma.dev/blog/gc-internal)
  - Technically, I don't think it that is saying as deep. but it is helpful to understand how GC works in basic.
  - In this post, also has good link [Visualizing Your Ruby Heap](https://tenderlovemaking.com/2017/09/27/visualizing-your-ruby-heap.html).
    - It says Ruby is using page address and its position. it is same idea OS how to manage memory.
    - so I remind that I have learned about OS. and I realize why Ruby uses HEAP_PAGE_OBJ_LIMIT as 409.
  - Finally, I can read [Ruby Garbage Collection Deep Dive: Tri-Color Mark and Sweep](https://jemma.dev/blog/gc-mark-and-sweep).
  - so those are not actul helpful coding technique now. but I think that are helpful in the future when I learn new technique.

## 2021.03.05.

- [What does the other user using Ruby thinks of harder test](https://anthonysciamanna.com/2016/02/14/should-private-methods-be-tested.html)
  - Private method tested means to be complicated software and might be violated SRP. It says that to solve method is refactoring. But test would then be test still complicated. Hence says again that could be solved by stub or mock.
  - By the way, it may make following question. What are stub and mock? so is it appropriate solution? and in TDD can use that? does?
  - Martin Fowler(a.k.a Unkle Bob) introduces [what is the unit test?](https://martinfowler.com/bliki/UnitTest.html) and differences between [classical testing and mockist testing](https://martinfowler.com/articles/mocksArentStubs.html).
    - It is helpful to understand that to use mock and stub might be appropriate in TDD.
    - What I'm saying is that in tranditional TDD, test is only concerned about input and output. However to use stub and mock means that test code knows how such implemented. But mockist testing is allowed mock and stub in test code since unit test must be isolated.
    - So, How am I supposed to choose? my answer is that it depends on.

## 2021.02.01.

- [Ruby on Rails about Predicate](https://github.com/rails/rails/pull/5329)
  - [Further article](https://github.com/rails/rails/commit/3756a3fdfe8d339a53bf347487342f93fd9e1edb)
  - It does not post. but it is important to think what rails core developers' think.
  - And make a deep think predicate methods.
  - [Official Ruby FAQ](https://www.ruby-lang.org/en/documentation/faq/6/)
    - However, this post says predicate methods can return true or false. so I'm confused now.
    - Finally, I've realized good to use predicate method'd be return only true and false because of usability and for documenting. as you know nil is unexpected value.

## 2021.01.13.

- [Mocking in Ruby with Minitest](https://semaphoreci.com/community/tutorials/mocking-in-ruby-with-minitest)
  - You guys know what the test doubles are? If no, this post explains simple examples.
  - [Behavior-driven Development](https://semaphoreci.com/community/tutorials/behavior-driven-development)
    - If you are intersted in to improve test code, would be good to read along with it. I recommend.

## 2021.01.07.

- [How Can We Measure Our Software’s Modularity and Dependencies?](https://medium.com/better-programming/inside-software-modularity-and-related-metrics-2e5af2b447dc)
  - It makes me to think about modularity via discrete mathematics.
  - Since cohesive and coupling are important to maintain, I should use method that explaind by post.
- [Microservices Architecture From A to Z](https://medium.com/swlh/microservices-architecture-from-a-to-z-7287da1c5d28)
  - Microservice architecture is one of the most shared techinique and hot nowdays maybe.
  - The post explains how to use simple and detail.

## Before

### Ruby

- [JIT and Ruby's MJIT](https://engineering.appfolio.com/appfolio-engineering/2019/7/18/jit-and-rubys-mjit)
  - Simple introduction how ruby implemenets JIT. More details are going to be explained another link.
- [Ruby 3 is released - The list of Ruby 3 features](https://bigbinary.com/blog/ruby-3-features)
  - Ruby 3 was released and introduced new features.
- [MJIT Support in Ruby 2.6](https://bigbinary.com/blog/mjit-support-in-ruby-2-6)
  - Since ruby 2.6, it supports MJIT which is called JIT. JIT of Ruby is too important to optimmize.
- [Hidden cost of string indexing in Ruby](https://www.greyblake.com/blog/2020-12-21-hidden-cost-of-string-indexing-in-ruby/)
  - Actually, ruby is not always O(1) to use index of string.
- [Refactoring checklist for beautiful Ruby code](https://dev.to/junko911/refactoring-checklist-for-beautiful-ruby-code-175c)
- [Encapsulating Ruby on Rails views](https://github.blog/2020-12-15-encapsulating-ruby-on-rails-views/)
- [The Evolution of Ruby Strings from 1.8 to 2.7](https://medium.com/rubycademy/the-evolution-of-ruby-strings-from-1-8-to-2-5-8b2ed8f39fad)
- [Fun with Ruby method argument defaults](https://zverok.github.io/blog/2020-11-19-arg_defaults.html)
- [Peter's Adventures in Ruby: The Ruby inplace bug](https://blog.peterzhu.ca/ruby-inplace-bug/)
- [Currency Calculations in Ruby](https://www.honeybadger.io/blog/ruby-currency/)
- [Rails 6.1 deprecates rails db:structure:dump and rails db:structure:load](https://blog.bigbinary.com/2020/09/22/rails-6-1-deprecates-rails-db-structure-dump.html)
- [Ruby 2.8 adds endless method definition](https://blog.bigbinary.com/2020/09/15/ruby-2-8-adds-endless-method-definition.html)

### JS

- [JavaScript Interview Questions: Functions](https://codeburst.io/javascript-interview-questions-functions-5a3081c1f3f5)
- [npm vs Yarn — Choosing the right package manager](https://medium.com/javascript-in-plain-english/npm-vs-yarn-choosing-the-right-package-manager-a5f04256a93f)
- [JavaScript Under The Hood Pt. 4: Bind(), Call(), and Apply()](https://codeburst.io/javascript-under-the-hood-pt-4-bind-call-and-apply-22e2b46b3882)
- [Avoid These Common JavaScript Mistakes](https://codeburst.io/avoid-these-common-javascript-mistakes-11f5311c9ec3)
  - Basic of JS.
- [Maintainable JavaScript — Throwing Errors](https://medium.com/dev-genius/maintainable-javascript-throwing-errors-e6c2ccf90c71)
  - How to throw error.
  - Need to know what the difference between exception and unexcpected situation.
- [4 Reasons to Avoid Using Array.reduce](https://medium.com/better-programming/think-again-before-you-use-array-reduce-28f785b5aea9)
  - Explain how to use Array.reduce clarify
- [Frameworks will never be as fast as Vanilla JavaScript](https://medium.com/javascript-in-plain-english/javascript-frameworks-performance-60f71d321693)
  - Explain why Vanilla JS has not been used alone.

### Architecture

- [Avoiding Double Payments in a Distributed Payments System](https://medium.com/airbnb-engineering/avoiding-double-payments-in-a-distributed-payments-system-2981f6b070bb)
  - Using idempotency key which idea is good solution for me now. and to seperate internal logics into three phases using RPC is good. isn't it?
- [System Design 101](https://towardsdatascience.com/system-design-101-b8f15162ef7c)
  - This article makes me to remind what is the important things construct architecture such as network bandwidth and etc..
- [You Aren’t Gonna Need Microservices](https://blog.ttulka.com/you-are-not-gonna-need-microservices)
  - Explain why modern architecture does not need MSA with YANGI.
- [Microservice Architecture — Communication & Design Patterns](https://medium.com/dev-genius/microservice-architecture-communication-design-patterns-70b37beec294)
- [Everything A Developer Must Know About Microservices](https://medium.com/dev-genius/everything-a-developer-must-know-about-microservices-dae854782ab)

  - SDLC: Software Development Life Cycle
  - [SOA vs. MSA](https://www.ibm.com/cloud/blog/soa-vs-microservices)
  - [ESB](https://www.ibm.com/cloud/learn/esb)
  - [SOAP](https://www.redhat.com/ko/topics/integration/whats-the-difference-between-soap-rest)
    - [Security](https://www.redhat.com/ko/topics/security/api-security)

- [Modern-Day Architecture Design Patterns for Software Professionals](https://medium.com/better-programming/modern-day-architecture-design-patterns-for-software-professionals-9056ee1ed977)

### Data Science

- [Understanding ReLU: The Most Popular Activation Function in 5 Minutes!](https://towardsdatascience.com/understanding-relu-the-most-popular-activation-function-in-5-minutes-459e3a2124f)
  - Pros and Cons of ReLU
- [Backpropagation paper from scratch](https://towardsdatascience.com/backpropagation-paper-from-scratch-796793789248)
  - The post generalizes backpropagation using delta rule.
- [The Facebook Data Engineer Interview](https://towardsdatascience.com/the-facebook-data-engineer-interview-345235afaac0)
- [Understanding Markov Chains and Stationary Distribution](https://www.reddit.com/r/learnmachinelearning/comments/jhtbqk/understanding_markov_chains_and_stationary)

### Basic CS

- Parallelism
  - [Wikipedia Green Thread](https://en.wikipedia.org/wiki/Green_threads)
  - [D langauge fiber explanation](https://tour.dlang.org/tour/kr/multithreading/fibers)
  - [Ruby fiber explanation](https://weicomes.tistory.com/100)
  - [Wikipedia Coroutine](https://en.wikipedia.org/wiki/Coroutine#Implementations_for_Scala)

### Refactoring

- [소프트웨어 개발 3대 원칙 : KISS, YAGNI, DRY](https://m.blog.naver.com/PostView.nhn?blogId=complusblog&logNo=221163007357)
  - Korean post is 3 principles of software development.
- [5 Rules to Improve Code Readability](https://medium.com/better-programming/5-rules-to-improve-code-readability-83eda50ca780)
  - All of posts about refactoring are going to be read.
- [4 Principles When Refactoring Your Functions](https://medium.com/better-programming/4-principles-when-refactoring-your-functions-81ce7f365e6d)
  - Four princples when refactoring, but real technology is complicate. so we need to select method empirically.
- [50 Quotes for Better Coding](https://codeburst.io/50-quotes-for-better-coding-76bdac3fc234)
- [6 Tips to Improve Your Conditional Statements for Better Readability](https://medium.com/javascript-in-plain-english/6-tips-to-improve-your-conditional-statements-for-better-readability-56256c5a5245)
  - The post explains I naturally use method of refactoring if..elsif
- [Software Architectural Thinking for Developers [Part 1]](https://dev.to/edisonnpebojot/software-architectural-thinking-for-developers-part-1-2a34)
  - In my opinion, I don't know what he's saying but it was intersting.

### Web

- [Prevent unnecessary network requests with the HTTP Cache](https://web.dev/http-cache/)
  - Basic ways to optimize http request cost.
- [Back/forward cache](https://web.dev/bfcache/#optimize-your-pages-for-bfcache)
  - Bfcache is important for usability. it explains how to use bfcache simple.
- [Detached window memory leaks](https://web.dev/detached-window-memory-leaks/)
  - Intersting things of Vaninlla JS about memory leak occurs.
- [How to View Your Live Localhost From Your Laptop on Your Mobile Device](dev.to/brendamichellle/how-to-view-your-localhost-from-your-laptop-on-your-mobile-device-516c)
  - Easy way to test mobile web using local server on VSCode.
- [Goodbye Nginx, hello Caddy](https://blog.bigbinary.com/2020/09/22/rails-6-1-deprecates-rails-db-structure-dump.html)
  - [Caddy vs. Nginx](https://stackshare.io/stackups/caddy-vs-nginx) summary: performanec or usability.

### Others

- [MVC vs MVP vs MVVM](https://levelup.gitconnected.com/mvc-vs-mvp-vs-mvvm-35e0d4b933b4)
  - The fun fact is most application codes do not use that clear. so just to know what that mean is not important.
- [Web Developers Outlook](https://www.bls.gov/ooh/computer-and-information-technology/web-developers.htm#tab-6)
  - From 2019 to 2029, employing web developer will be grwoing 8 percents.
- [The XY Problem](https://xyproblem.info/)
  - How to question a problem clear.
- [THERE'S ALWAYS MORE HISTORY](https://www.hillelwayne.com/post/always-more-history)
  - Deep dive into the funny histories.
- [3 Books to Improve Your Coding Skills](https://medium.com/better-programming/3-books-to-improve-your-coding-skills-afa67621192)
  - Recommended books about Algoirthm, Engineering and Functional Thinking
- [5 Signs of a Senior Developer](https://levelup.gitconnected.com/5-signs-of-a-senior-developer-7f5c59093c73)
  - The difference between senior developer and junior developer.

### [이전 문서](archive/README.md)
