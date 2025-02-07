---
slug: test-mdx
title: Testing MDX
authors: [jimgenna]
---

<!-- truncate -->
# testing 


## Highlight color test

<!-- Highlight coloring example: -->
<!-- worked -->
export const Highlight = ({children, color}) => (
    <span
       style={{
		      backgroundColor: color,
		      borderRadius: '2px',
		      color: '#fff',
		      padding: '0.2rem',
		    }}>
        {children}
  </span>
);

<Highlight color="#25c2a0">Docusaurus green</Highlight> and <Highlight color="#1877F2">Facebook blue</Highlight> are my favorite colors.
		
I can write **Markdown** alongside my _JSX_!

<!-- another Highlight coloring example: -->

<span style={{backgroundColor: 'red'}}>Red</span>
<span style={{backgroundColor: 'blue', color: 'white'}}>Blue</span>
<span style={{backgroundColor: 'green'}}>Green</span>
<span style={{backgroundColor: 'yellow', color: 'red'}}>Yellow</span>

<!-- ****** -->

## image URL test

![image](https://thesquare.americanexpress.com/api/users/userphotobyid?userId=42375)

#### TIMS pricing 
![image](https://thesquare.americanexpress.com/media/32977660/2024-tims-pricing.jpg?width=724&height=510)
<!-- ****** -->

## Admonitions test

<!-- Admonitions testing -->
<!-- worked -->
:::note
    Some **content** with _Markdown_ `syntax`. Check [this `api`](#).
:::

:::tip
    Some **content** with _Markdown_ `syntax`. Check [this `api`](#).
:::

:::info
    Some **content** with _Markdown_ `syntax`. Check [this `api`](#).
:::

:::warning
    Some **content** with _Markdown_ `syntax`. Check [this `api`](#).
:::

:::danger
    Some **content** with _Markdown_ `syntax`. Check [this `api`](#).
:::

<!-- ****** -->

## mermaid testing

<!-- worked -->
```mermaid
graph TD;
A-->B;
A-->C;
B-->D;
C-->D;
``` 

```mermaid
timeline
    title 2025 Big Rocks
    First Quarter : Perform CAS SR
        : AMP AIU POC
    Second Quarter : India Decom
        : DataGate App on-boarding
        : COBOL Explainability POC 
        : PostGres POC
    Third Quarter : PureScale for GCCP
    Fourth Quarter : Safe Guarded Copy
        : Finalize Kyndryl contract
        : Hydra Integration
```

<!-- worked -->
## Timeline test
```mermaid
timeline
    title History of Social Media Platform
    2002 : LinkedIn
    2004 : Facebook
         : Google         
    2005 : Youtube
    2006 : Twitter
    2022'ish : X
```

```mermaid
timeline
    title Timeline of Industrial Revolution
    section 17th-20th century
        Industry 1.0 : Machinery, Water power, Steam <br>power
        Industry 2.0 : Electricity, Internal combustion engine, Mass production
        Industry 3.0 : Electronics, Computers, Automation
    section 21st century
        Industry 4.0 : Internet, Robotics, Internet of Things
        Industry 5.0 : Artificial intelligence, Big data, 3D printing
```
<!-- ****** -->


<!-- tab testing -->
<!-- worked -->
## Tabs test

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
    <TabItem value="apple" label="Apple" default>
        This is an apple 🍎
    </TabItem>
    <TabItem value="orange" label="Orange">
        This is an orange 🍊
    </TabItem>
    <TabItem value="banana" label="Banana">
        This is a banana 🍌
    </TabItem>
</Tabs>

## Another tab test 

<Tabs
     defaultValue="apple"
     values={[
	    {label: 'Apple', value: 'apple'},
	    {label: 'Orange', value: 'orange'},
	    {label: 'Banana', value: 'banana'},
    ]}>
     <TabItem value="apple">This is an apple 🍎</TabItem>
     <TabItem value="orange">This is an orange 🍊</TabItem>
     <TabItem value="banana">This is a banana 🍌</TabItem>
</Tabs>

<Tabs groupId="operating-systems">
  <TabItem value="win" label="Windows">Use Ctrl + C to copy.</TabItem>
  <TabItem value="mac" label="macOS">Use Command + C to copy.</TabItem>
</Tabs>

<Tabs groupId="operating-systems">
  <TabItem value="win" label="Windows">Use Ctrl + V to paste.</TabItem>
  <TabItem value="mac" label="macOS">Use Command + V to paste.</TabItem>
</Tabs>

<!-- ****** -->

<!-- math testing -->
## Math test 

```mermaid
graph LR
  A["$$x^2$$"] -->|"$$\sqrt{x+3}$$"| B("$$\frac{1}{2}$$")
  A -->|"$$\overbrace{a+b+c}^{\text{note}}$$"| C("$$\pi r^2$$")
  B --> D("$$x = \begin{cases} a &\text{if } b \\ c &\text{if } d \end{cases}$$")
  C --> E("$$x(t)=c_1\begin{bmatrix}-\cos{t}+\sin{t}\\ 2\cos{t} \end{bmatrix}e^{2t}$$")

```

<!-- block-beta testing 
https://mermaid.js.org/syntax/block.html
-->
## block-beta test 
```mermaid

%% comment in mermaid 
%% A@{shape: flag, label:"flag"}

block-beta
  columns 3
  test:3
  block:group1:3
    columns 4
    a["H Label"] space:2 id1(("circle")) i j k l
  end
  block:group2:3
    blockArrowId<["right"]>(right)
    blockArrowId2<["left"]>(left)
    blockArrowId3<["123"]>(up)
    blockArrowId4<["abcd"]>(down)
  end
  block:group3:4
    %% columns auto (default)
    db[("database")] rarrow<["right"]>(right) crl(("circle")) id5{"c"} d e f    
  end
  columns 4
  A space B
  A-->B
  db1["Hazelcast"] space trit(["Triton Server"])
  db1 --> trit
  
   style db1 fill:#636,stroke:#333,stroke-width:4px
   style trit fill:#bbf,stroke:#f66,stroke-width:2px,color:#000,stroke-dasharray: 5 5
```

<!-- other options
id1[("database")] id2(("circle")) id3("box") id4(["block"]) id5>"asymmetric"] id6["P details"] id7{"rhombus"} id8[["double box"]]
blockArrowId5<["right"]>(right)
blockArrowId5<["left"]>(left)
---->

```mermaid 

%% arch beta test 

%% icons are: cloud, database, disk, internet, server 
%% *** for logo icons:
%% https://mermaid.js.org/config/icons.html
%% list of logos: https://icones.js.org/
%%    example logos are: aws-aurora, aws-glacier, aws-s3, aws-ec2 
%% service inmemdb(logos:memory)[Hazelcast] in api
%% service inmemdb(logos:memory-alt)[Hazelcast] in api
%% service inmemdb(logos:redis)[Hazelcast] in api
%% service mainfame(logos:ibm)[IBM Z] in api
%% service redhat1(logos:redhat)[RedHat] in api
%% service kub1(logos:kubernetes)[OCPz] in api
%% service server2(logos:aws-ec2)[Server] in api
%% service server3(logos:linux)[Linux] in api

architecture-beta
    group api(cloud)[IBM Z]

    service db(database)[Hazelcast] in api    
    %% service disk1(disk)[Storage] in api
    service memory(database)[Memory] in api
    %%service mainframe(server)[IBMZ] in api
    service server1(server)[Triton Server] in api
    service aiu(internet)[AIU] in api 
    
    db:L -- R:server1
    aiu:T -- B:server1
    memory:T -- B:db
```


<!-- didn't work --

## Math equation

import remarkMath from 'remark-math';
import rehypeKatex from 'rehype-katex';
export default {
  presets: [
    [
      '@docusaurus/preset-classic',
      {
        docs: {
          path: 'docs',
          remarkPlugins: [remarkMath],
          rehypePlugins: [rehypeKatex],
        },
      },
    ],
  ],
};

$$
I = \int_0^{2\pi} \sin(x)\,dx
$$


<!-- ****** -->

<!-- ****** -->
