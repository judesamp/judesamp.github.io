---
title: The Ironyard&#58; Beginning Week Three
date: 2014-04-14
tags:
- The Ironyard
- days
---

We're at the beginning of week 3 here at the Iron Yard Academy in Atlanta. This week, we're going to be building sites with Sinatra, talking about REST, gems, bundler, and dipping our toes into the world of databases. The preliminaries appear to be near their end; now we're building web apps. 


<p>
  But before diving headlong into this week, I wanted to linger a bit on the end of last week. The last three days and weekend were all about HTML and CSS. We basically got a pdf of a site—and had to mimic it as closely as possible. For me, it was a labor intensive assignment. Apparently, there are a lot of details of web design I don't even notice. (Hello, shadows!) I've been dabbling in HTML and CSS for a while, but a little piece of positioning finally clicked into place over the weekend.
</p>

<p>
  Basically, I discovered how to create rows of content using nested <a href="http://en.wikipedia.org/wiki/Span_and_div">divs</a>. Yeah, it ain't rocket science, but I was happy to understand it—even if all of the frameworks out there basically make this epiphany a little redundant. 
</p>

<p>
  So here's how I understand it. 
</p>

<p>
  <ol>
    <li>
      Create a parent div pair. We'll give them a class of grandparent. 
      <p>
      <code>
        <div class="grandparent">
          
        </div>
      </code>
      </p>

      In the css, we'll give grandparent a width of 100%.
      <p>
        <code>
          .grandparent {
            width: 100%;
          }
        </code>
      </p>
    </li>
      Nested inside of grandparent, we'll put another div pair. This one, we'll give a class of parent.
      <p>
        <code>
          <div class="grandparent">
            <div class="parent">
              
            </div>
          </div>
        </code>
      </P>

      In the css, we'll give parent the width we have in mind for our layout, whether that's 768, 940, or whatever. You'll also need to set margin to auto if you want your eventual content to be centered on the page. I suspect that it might be a good idea to set height here too. This chould help short circuit positioning confusion later, as you add more and more to your design.
      
      <P>
        <code>
          .parent {
            width: 940px;
            margin: auto
          }
        </code>
      </P>

    <li>
      Finally, we can nest our content inside of our two existing divs.
      <P>
        <pre  style="font-family:arial;font-size:12px;border:1px dashed #CCCCCC;width:99%;height:auto;overflow:auto;background:#f0f0f0;;background-image:URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif);padding:0px;color:#000000;text-align:left;line-height:20px;"><code style="color:#000000;word-wrap:normal;"> &lt;div class="grandparent"&gt;  
       &lt;div class="parent"&gt;  
        &lt;div class="child1"&gt;  
         content  
        &lt;/div&gt;  
         &lt;div class="child2"&gt;  
         content  
        &lt;/div&gt;  
        &lt;div class="child3"&gt;  
         content  
        &lt;/div&gt;  
       &lt;/div&gt;  
      &lt;/div&gt;  
</code></pre>
      </P>

      In the css, we can give these children divs widths that add up to our parent width (while taking margin, border, etc. into account). You'll also need to float the divs left or right to get them into the row formation. So, something like:
      
      <P>
       <pre  style="font-family:arial;font-size:12px;border:1px dashed #CCCCCC;width:99%;height:auto;overflow:auto;background:#f0f0f0;;background-image:URL(http://2.bp.blogspot.com/_z5ltvMQPaa8/SjJXr_U2YBI/AAAAAAAAAAM/46OqEP32CJ8/s320/codebg.gif);padding:0px;color:#000000;text-align:left;line-height:20px;"><code style="color:#000000;word-wrap:normal;"> .child1 {  
       width: 300px;  
       margin-right: 10px;  
       float:left;  
      }  
      .child2 {  
       width: 300px;  
       margin-left: 10px;  
       margin-right: 10px;  
       float:left;  
      }  
      .child3 {  
       width: 300px;  
       margin-left: 10px;  
       float:left;  
      }  
</code></pre>
      </P>
      
    </li>
  </ol>
</p>

<p>Of course, getting this to work responsively is a lot more complex. And there are probably some nuances of how all of this works together that I'm missing. But it's a start. 
</p>

