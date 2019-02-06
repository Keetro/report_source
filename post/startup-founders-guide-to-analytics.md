---
title: "The Startup Founder’s Guide to Analytics"
author: tristan
team: fishtown
type: article
date: '2019-01-30'
categories:
  - analytics
slug: startup-founders-guide-to-analytics
tags: [analytics,data,start-ups]
---

**You need analytics.**

I’m very confident of that, because today, everyone needs analytics. Not just product, not just marketing, not just finance… sales, fulfillment,  **everyone at a startup needs analytics today** . Analytics powers every decision, from the strategic to the tactical, from the board room to your line level employees.

**This post is about how to create the analytics competency at your organization.**  It’s not about what metrics to track (there are plenty of good posts about that), it’s about how to actually get your business to produce them. As it turns out, the implementation question —  *How do I build a business that produces actionable data?* —is much harder to answer.

And the answer is changing fast. The analytics ecosystem is moving very quickly, and the options you have at your disposal have changed significantly in the past 24 months.  **This post reflects recommendations and experience with the data technology of 2017.**

### First: Why should you listen to me?

I’ve spent the better part of two decades working in analytics. In that time, I’ve seen plenty of things go well, but a lot more go poorly. I spent the early part of my career implementing legacy enterprise BI  *(ugh)* . I built  **Squarespace** ’s first analytics competency from 2009–2010 and raised [massive A round](https://techcrunch.com/2010/07/13/squarespace-raises-38-5-million-from-accel-index-ventures/) with the data. I was then COO of  **Argyle Social** , a social media analytics startup, and subsequently VP Marketing at  **RJMetrics** , a leading BI platform for startups.

Now I spend my days helping startup execs implement analytics as the CEO and Founder of [ **Fishtown Analytics** ](http://fishtownanalytics.com/). At Fishtown, we start working with companies who have raised an A round and help them build their internal analytics competency as they grow. We’ve been through the exact process I’m going to describe in this article with over a dozen companies at this point, including  **Casper** ,  **SeatGeek** , and  **Code Climate** .

I’m going to walk you through, stage by stage, how your startup should be doing analytics. At each stage, my recommendations are going to answer to the question  *“What’s the absolute least I can get away with?”*  We’re not here to build castles in the sky; we need answers as cheaply as possible.

Let’s do it.

![](https://cdn-images-1.medium.com/max/1600/1*wIS1i_m51Ku8ZShDm9yHhA.jpeg)

### Founding Stage

> (0 to 10 employees)

At this stage, you have no resources and no time. There are a million things you could be measuring, but you’re so close to the details of your business that you’re actually able to make fairly good instinctual decisions. The one thing you need to make sure you  *are*  measuring is your product, because it’s your product metrics that will help you iterate quickly in this critical phase. Everything else can take a back seat.

#### What to do

* Install Google Analytics on your website via [Google Tag Manager](https://www.google.com/analytics/tag-manager/). The data won’t be perfect without more work but it’s not the right time to worry about that.
* If you are an ecommerce business, you really need to make sure that your Google Analytics ecommerce data is good. GA can do a decent job of tracking your ecommerce business all the way from visitor to purchase, so spend the time to make sure it’s right.
* If you build software of any type, you need real event tracking. I don’t care what tool you use — Mixpanel and Heap are very similar and they’re both good. At this point I wouldn’t think too hard about what you’re tracking: just use Mixpanel’s [autotrack](https://mixpanel.com/autotrack/) or Heap’s default installation. If you realize you need a datapoint, you’ll find it’s already there.  **This approach does not scale well, but for now, it’ll do.**
* Your financial reporting should be done in Quickbooks. Your forecasting should be done in Excel. If you’re a subscription business, use [Baremetrics](https://baremetrics.com/)for your subscription metrics. If you’re an ecommerce business, use your shopping cart platform to measure GMV.  **Don’t get fancy.**

If you’re not technical, you may need an engineer to help out with GA and event tracking. This entire exercise shouldn’t take more than an hour or two, including reading the docs. It’s worth it to take the time out of building for this.

#### What not to do

**Everything that is not one of the things above.**  Do not let someone sell you a data warehouse, a BI platform, a big consulting project, or…yeah, you get it.  **Stay focused.**  When you make a commitment to analytics, there is an ongoing cost. Data changes. Business logic changes. Once you start down this road, you can’t really put the project on pause. Wait to make this investment until later.

There will be many questions that you just can’t answer yet.  **That’s fine (for now).**

### Very Early Stage

> (10 to 20 employees)

You’re growing your team a bit. These people need data to do their jobs. They may or may not be data experts, and you need to make sure that they’re doing the basic things right.

#### What to do

* You’ve probably hired a marketing person. Make sure they own GA. Hold them accountable for making sure the data is clean. They need to [UTM track](https://www.launchdigitalmarketing.com/what-are-utm-codes/) every damn link they create. They need to make sure your [subdomains aren’t double-tracking](http://www.lunametrics.com/blog/2016/08/11/subdomain-tracking-google-analytics/). Your marketing person may say that they’re “not a GA person”.  **Don’t listen.**  There is enough information on the web about GA that if they’re smart and motivated they can learn it and figure it out. If they can’t figure it out, fire them and find someone else (seriously).
* If you have a sales person or two and use a CRM, use the built-in reporting. Make sure that your people know how to use it. You need to be able to know basic things like rep productivity and conversion rates by stage. Salesforce can do this stuff out of the box. Don’t export data to Excel, build the reports in the (terrible) report builder. Even if it’s painful, this will save you tons of time in the coming months.
* You probably have a couple of people in customer success. Most help desk systems don’t have great reporting, so choose KPIs that you can measure easily within the interface.
* Make sure you track NPS. Use [Wootric](https://www.wootric.com/) or [Delighted](https://delighted.com/).

#### What not to do

It’s still too early for a data warehouse and for SQL-based analytics—it just takes too much time.  **You need to spend all of your time doing, not analyzing** , and the most straightforward way to do that is to use the built-in reporting capabilities of the various SaaS products you’re using to run your business. You also shouldn’t hire a full-time analyst yet. There are more important things to spend your limited funds on at this point.

### Early Stage

> (20 to 50 employees)

This is where things get interesting, and where the changes in the past two years really start to become apparent. Once you’ve raised your A round and have 20+ employees you start to have new options.

These options are all driven by one thing:  **analytics tech is getting better, fast** . Previously this type of infrastructure was reserved for much larger companies. Its benefits? More reliable metrics, more flexibility, and  **a better platform for future growth** .

> This is the hardest and most critical phase: promising if you do it right, but pain-inducing if you do it wrong.

#### What to do

* **Set up your data infrastructure.**  This means choosing a data warehouse, an ETL tool, and a BI tool. For data warehouses, look into [Snowflake](https://www.snowflake.net/) and [Redshift](https://aws.amazon.com/redshift/) (I prefer to work with Snowflake given the choice). For ETL tools look into [Stitch](http://stitchdata.com/) and [Fivetran](http://fivetran.com/). For BI look into [Mode](http://modeanalytics.com/) and [Looker](http://looker.com/). There are  *many, many*  products in this space; these six are the ones that we come back to time and again with our clients.
* **Hire a strong analytics lead.**  Down the road, you’re going to need an entire team of analytics professionals: engineers, analysts, data scientists… But for now, you can only afford (at most) a single headcount. You need to find that special person who will be able to provide value on day 1, but who will also be able to hire the team around them as you grow.  *This person is hard to find—* invest the time to find them. Often these folks have backgrounds in consulting or finance, and they frequently have MBAs. While this person should be able to roll up their sleeves and get their hands dirty, focus on hiring someone that can think about data, and about your business, strategically: they’re going to be the most important piece of your analytics puzzle for years to come.
* **Consider hiring a consultant.**  While it’s great that you’ve found your analytics lead, that person isn’t going to have the expertise required to put together all of the components of your tech stack or the experience to solve all of the different analytics problems you’ll face across your business. Mistakes made at this critical stage have serious costs in both time and money as you grow, so  *it’s important to lay a solid foundation* . To do this, more startups today are choosing to work with consultants to help them get set up, and then building a team around that infrastructure.

#### What not to do

* Unless machine learning is a core part of your product, don’t hire a data scientist yet. You need a generalist, not a specialist, to build your analytics team.
* For the love of all that is holy,  **do not build your own ETL pipelines** . This will waste so many hours of engineering time. Buy off-the-shelf from Stitch or Fivetran.
* Don’t use any other BI tool than the two I mentioned above. You will pay for this down the road,  *hard* .
* Don’t try to “get away with” using a more traditional database like Postgres as your data warehouse. It’s not that much cheaper and it’ll be a real time suck to switch later when you max it out. Postgres does not scale well as a data warehouse.

### Mid-Stage

> (50 to 150 employees)

This stage is potentially the most challenging. You still have a relatively small team and few resources, but you’re being asked to deliver increasingly sophisticated and diverse analytics to the business, and your work can directly impact the success or failure of the company as a whole.  *No pressure.*

It’s important to make forward progress here while making sure that you continue to lay the groundwork for future phases of your growth.  **The decisions you make in this phase can cause you to charge straight into a brick wall**  if you don’t think hard about the future.

#### What to do

* **Implement a solid process for SQL-based data modeling.**  Your data models serve as the underlying business logic for your analytics and should be shared across all of your analytics use cases, from BI to data science. Make sure that your process allows  **all users**  to make changes to data modeling scripts, is  **version-controlled** , and is run in a  **transparent environment** . We maintain an open-source product called [dbt](http://getdbt.com/) that many growth-stage companies use to do exactly this.
* **Migrate from your existing web analytics and event tracking to** [ **Snowplow Analytics** ](http://snowplowanalytics.com/). Snowplow does everything that the paid tools do, but it’s open source. You can either host it yourself (and just pay the costs of your EC2 instances), or you can pay Snowplow or Fivetran to host the collector for you. If you don’t make this transition during this phase, you’re going to be missing out on collecting much more granular data, and you’re going to be setting yourself up for truly massive bills from Segment, Heap, or Mixpanel down the road. Once you grow past this stage these paid tools can easily charge $10k+ per month at minimum.
* **Grow your team thoughtfully** . The core of your team should always be business analysts: folks who are experts in SQL and your BI tool and spend their time working with business users to help them service their data requests. Figuring out the profile of this person and how to train and equip them is incredibly important. You should also hire your first data scientist in this phase. It’s important to have your data infrastructure and core analytics team in place prior to hiring experienced (and expensive) data science talent, but at some point you should add this skill set.
* **Begin selectively tackling some forecasting challenges** . Forecasting is harder than just running counts and sums, but there are a couple of key areas where it makes sense to begin diving in. If you’re a SaaS business, you should be working on a churn forecasting model. If you’re an ecommerce business, you absolutely need to be working on a demand forecasting model. These models will probably not be extremely sophisticated, but they’ll be a big improvement over the random Excel workbook that someone in Finance hacked together.
* **Spend time and energy on figuring out your marketing attribution** . This is a whole blog post on its own, but suffice it to say that you simply can’t trust this critical business question to a third party.

#### What not to do

It’s easy to get carried away with yourself and begin investing in heavy-duty data infrastructure.  **Don’t do this.**  At this stage, major infrastructure investments are still an expensive distraction. Here are some suggestions on how to stay agile:

* Push SQL, and your data warehouse, hard. You can get away with doing almost anything you want at this stage using the processing power of your data warehouse. Buy as much data warehouse horsepower as you need — paying for servers is far cheaper than paying for humans.
* Add in Jupyter Notebooks for data science work. If the data has been pre-aggregated in your warehouse, you typically won’t need to do this processing on a Spark or Hadoop cluster yet.
* Find low-cost ways to ETL datasets that don’t have off-the-shelf integrations. This is one of the things we love about [Singer](http://singer.io/).

Avoiding expensive boondoggles will keep you focused on solving real business problems.

### Growth Stage

> (150 to 500 employees)

**This stage is all about creating analytics processes that scale.**  You need to balance getting answers that you need  *today*  with implementing analytics practices that will scale as you continue growing your team.

At 150 employees you’ll probably only have a small team (3–6) full-time focused on analytics. By the time you have 500 employees you could easily have 30 or more. 3–6 analysts can operate in a fairly ad-hoc manner, exchanging knowledge (and code) informally. By the time you have 8+ analysts, this begins to break down very quickly.

If you don’t manage this transition well,  **you’ll actually perform less well as your team grows** : it will take you longer to produce meaningful insights, and your answers will be of lower quality. This is simply a function of non-linear complexity: you’ll have more data being produced and more analysts working with it. In order to combat this, you need processes to keep them working together reliably.

#### What to do

* **Implement data testing** . You have data flowing into your warehouse from at least a dozen sources at this point and you need a process to ensure that the data being loaded continues to conform to the rules you’re expecting it to: uniqueness, foreign key relationship, not null fields, and custom business logic. If you don’t have a rock-solid automated process that checks this stuff the quality of your analysis will continue to degrade and you won’t know why. We use [dbt’s testing functionality](http://dbt.readthedocs.io/en/master/guide/testing/) for this with our clients.
* **Use pull requests and code reviews.**  Your analytic code is an asset, just like the code that powers your website and application. Producing high-quality code requires being serious about version control. Get every one of your team members in git, train them how to use branches, and disable force-pushes to master. All code that gets deployed to production should be merged via a pull request process that includes a review from a team member.
* **Get serious about documentation** . The data environment at your company is complicated. The only way to effectively manage that knowledge and share it with your team is to invest the time and energy needed to document it. This will add some overhead, but if you don’t make this investment you’ll find your analysts spend more time figuring out where to get certain data or how to use it than they do actually conducting analytics. Airbnb has done [excellent work in this area](https://medium.com/airbnb-engineering/scaling-knowledge-at-airbnb-875d73eff091#.1msebtoxt).
* **Be intentional about your analytics team structure.**  There are two primary models for how to structure an analytics team: centralized and embedded. There is no clear right answer, but this decision is going to be central to how you deliver analytics to your growing organization. Carl Anderson describes the tradeoffs well in his book [Creating a Data-Driven Organization](http://shop.oreilly.com/product/0636920035848.do).

#### What not to do

**Don’t accept excuses.**  Doing analytics right at this level is hard work, and it requires a talented and motivated team that is constantly innovating and improving. Code reviews take time and energy. Analysts aren’t used to having to test their code. And documentation is painstaking. There will be resistance to doing things this way, especially among your long-term team members who remember the “good old days”. But as complexity increases, you need to evolve your processes to adapt.

These processes will actually make analytics easier, faster, and more reliable, but implementing them will feel like pulling teeth. If you’re serious about scaling analytics, you’ll push through.

### You’re a Pioneer

I’ve come to each one of these recommendations after years of doing it myself within companies and now scaling the approach as a consultant. The opportunity to work with a range of similar clients has made it incredibly clear  **just how rare it is for companies to do this stuff well** .

If you take all of the recommendations in this post,  **you will literally be one of the highest-functioning analytics organizations in the world** . Not a bad competitive advantage.
