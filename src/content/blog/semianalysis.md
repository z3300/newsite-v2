---
title: "Semianalysis Work"
date: "2025-08-20"
description: "contract work for semianalysis"
new: true
---
![brand.png](/images/semilogo.png)

i did some contract work for [semianalysis](https://semianalysis.com/).

specifically, i worked on their api documentation.  

the goal was to make the documentation look clean and be easy to update later when adding new endpoints. their site was built entirely on wordpress using the block style “gutenberg” editor. that’s what block style means here.  

the main task was to create a theme with custom gutenberg blocks that would be simple for the team to edit and reuse.  

i built 3 custom blocks:  

1. a code block that displays python, javascript, or curl commands with custom syntax highlighting  
   ![code block](/images/code.png)  
2. a block for displaying json data in a formatted way  

<figure>
<img src="/images/json.png" alt="json block" style="max-width: 40%; display: block; margin: 0 auto;" />
<figcaption>json block</figcaption>
</figure>

3. a block for defining api parameters with a description and example  
   ![api parameters block](/images/peram.png)  

turns out building blocks wasn’t that hard.  

it’s basically creating two html/css templates: one for the user side and one for the admin side. 

the backend logic was handled in php, which included the parameters that the admin could edit directly in the block editor.  


<figure>
<img src="/images/wordpress.png" alt="wordpress editor" style="max-width: 40%; display: block; margin: 0 auto;" />
<figcaption>wordpress editor</figcaption>
</figure>