---
title: Mermaid for Markdown
category: Advanced Marksgown/Github
order: 1
---

<h2>Enabling Mermaid on a page</h2>
Add these two lines of Javscript to the '''<body>''' of your web page

```javascript
<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>mermaid.initialize({startOnLoad:true});</script>
```
Doing so will command the mermaid parser to look for the ```<div>``` tags with ```class="mermaid"``` in your HTML Document. <br>
From these tags mermaid will try to read the diagram/chart definitons and render them as svg charts.

<h2>Box's and Arrows</h2>

```javascript
<div class="mermaid">
graph TD
person --> xxx
person --> yyy
person --> zzz
</div>
```

<div class="mermaid">
graph TD
person --> xxx
person --> yyy
person --> zzz
</div>


<h2>Customer Journey</h2>

```javascript
<div class="mermaid">
journey
    title Get Covid funding support
    section Find Funding
      Google it: 4: Customer
      Talk to peers: 5: Customer
      Visit FBS: 4: Customer
      Do work: 1: Customer, Stakeholder
    section Choose Support
      Reduce number of options: 3: Customer
      Read details of shortlist: 4: Customer
    section Apply for Support
      Start Application: 5: Customer
      Create Account: 2: Customer
      Submit Application: 4: Customer
</div>
```
<br>
<div class="mermaid">
journey
    title Get Covid funding support
    section Find Funding
      Google it: 4: Customer
      Talk to peers: 5: Customer
      Visit FBS: 4: Customer, Stakeholder
    section Choose Support
      Reduce number of options: 3: Customer
      Read details of shortlist: 4: Customer
    section Apply for Support
      Start Application: 5: Customer
      Create Account: 2: Customer
      Submit Application: 4: Customer
</div>

<div class="mermaid">
journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 3: Me
</div>


<div class="mermaid">
journey
    title Get Covid funding support
    section Find Funding
      Google it: 4: Customer
      Talk to peers: 5: Customer
      Visit FBS: 4: Customer, Stakeholder
    section Choose Support
      Reduce number of options: 3: Customer
      Read details of shortlist: 4: Customer
</div>


<h2>PIE Chart</h2>
```
<div class="mermaid">
pie title Exports
    "Food & Drink" : 386
    "Tech" : 85
    "Life Sciences" : 15
</div>
```
<div class="mermaid">
pie title Exports
    "Food & Drink" : 386
    "Tech" : 85
    "Life Sciences" : 15
</div>


<h2>Flow Chart</h2>
```
<div class="mermaid">
graph LR
    A[Search] -->|Google Financial Support| B(Google Results)
    B --> C{Choose}
    C -->|UK| D[GovUK]
    C -->|UK| E[HMRC]
    C -->|Scot| F[FBS]
    C -->|Scot| G[GovScot]
</div>
```

<div class="mermaid">
graph LR
    A[Search] -->|Google Financial Support| B(Google Results)
    B --> C{Choose}
    C -->|UK| D[GovUK]
    C -->|UK| E[HMRC]
    C -->|Scot| F[FBS]
    C -->|Scot| G[GovScot]
</div>


<h2>ERD</h2>
```
<div class="mermaid">
classDiagram
    FBS_Listing <|-- Body
    FBS_Listing <|-- Fund
    FBS_Listing <|-- Segment
    FBS_Listing : +String Funding_Body
    FBS_Listing : +String Fund_Name
    FBS_Listing : +String Segment
    FBS_Listing: +isOpen()
    class Body{
      +String Funding_Body
      +String Email
      +String Phone
      +emailMe()
      +phoneMe()
    }
    class Fund{
      +String Fund_Name
      -int LowerLimit
      -int UpperLimit
      -isOpen()
    }
    class Segment{
      +String Segment
      -int Rank
      -isPriority()
    }
</div>
```

<div class="mermaid">
classDiagram
    FBS_Listing <|-- Body
    FBS_Listing <|-- Fund
    FBS_Listing <|-- Segment
    FBS_Listing : +String Funding_Body
    FBS_Listing : +String Fund_Name
    FBS_Listing : +String Segment
    FBS_Listing: +isOpen()
    class Body{
      +String Funding_Body
      +String Email
      +String Phone
      +emailMe()
      +phoneMe()
    }
    class Fund{
      +String Fund_Name
      -int LowerLimit
      -int UpperLimit
      -isOpen()
    }
    class Segment{
      +String Segment
      -int Rank
      -isPriority()
    }
</div>
