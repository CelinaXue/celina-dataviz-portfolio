| [home page](https://celinaxue.github.io/celina-dataviz-portfolio/) | [data viz examples](dataviz-examples) | [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

# Critique by Design: Comparing the Cost of Protein

For this assignment, I explored how a protein cost chart could better help readers compare affordable food options. I critiqued the original visualization, developed an initial Tableau draft, gathered peer feedback, and revised the design.

## Step one: The visualization

![Original visualization comparing the cost of 30g of protein](https://pub-cee805df54de4b6c8f93bee984e3c725.r2.dev/datasets/2023w8/original_viz.png)

Original visualization: [The Bodybuilding Dietitians — What Are The Cheapest High-Protein Foods?](https://www.thebodybuildingdietitians.com/blog/how-cost-effective-is-your-high-protein-diet)

Challenge and dataset: [Makeover Monday — 2023 Week 8](https://makeovermonday.vercel.app/dataset/2023w8)

I selected this visualization because food costs are relevant to everyday decisions, especially for students shopping on a budget. The question is easy to relate to: which foods provide protein at a lower cost? I was interested in making the comparison easier to read and more useful for people with different dietary preferences.

The original already uses sorted bars, but its angled labels, product images, and calorie labels compete with the cost information. This gave me an opportunity to explore how layout, labeling, and selective highlighting could improve the comparison.

**A note about the data:** The challenge page provides both the original graphic and a file called `Protein Costs.xlsx`. The graphic shows 10 foods and costs per 30g of protein, while the supplied workbook contains 22 foods and costs per 20g of protein in US dollars. I used the graphic for the design critique and the challenge's supplied workbook for my Tableau visualization. The final chart therefore uses a different food selection and measurement basis, rather than reproducing the original values. I did not convert the original chart's prices into the workbook values.

## Step two: The critique

I used Stephen Few's Data Visualization Effectiveness Profile to evaluate the original chart. The following ratings summarize my assessment.

- **Usefulness — 8/10:** The chart addresses a practical question for readers interested in affordable protein. Comparing costs for an equal amount of protein is useful, although the prices may not reflect every reader's location or shopping options.
- **Completeness — 5/10:** Food names, a cost axis, and calorie labels are included. However, exact costs are not labeled, and the graphic does not specify the currency, collection date, or location. The serving basis for the calorie values could also be clearer.
- **Perceptibility — 7/10:** The sorted bars and zero baseline make the overall ranking easy to see. However, angled food labels take more effort to read, and calorie numbers draw attention away from the cost comparison.
- **Truthfulness — 6/10:** A zero baseline supports a fair comparison of bar lengths. However, the graphic alone does not provide enough context to verify the prices or understand how representative they are. This limits confidence without demonstrating that the data are incorrect.
- **Intuitiveness — 7/10:** The familiar bar chart and direct title are easy to understand. Readers still need to distinguish between the cost encoded by bar height and the calories written inside each bar.
- **Aesthetics — 6/10:** Consistent colors and recognizable food images make the chart approachable. The product images, logo, and angled labels also compete for attention.
- **Engagement — 7/10:** The topic encourages readers to compare their own food choices. However, the chart offers limited support for identifying options that fit particular dietary preferences.

The likely audience includes budget-conscious shoppers, students, and people interested in protein intake. For these readers, finding an affordable option quickly matters more than decorative detail. My main redesign goals were to make labels easier to read, make cost information clearer, and support comparisons within relevant food groups.

Few's criteria helped me separate problems with missing context from problems with visual presentation. However, the numerical scores still involve judgment and do not explain exactly how to redesign the chart. Connecting the critique to the audience's question helped me turn the assessment into specific design changes.

## Step three: Sketch a solution

<div class="tableauPlaceholder" id="viz1794522529212" style="position: relative;">
  <noscript>
    <a href="https://public.tableau.com/views/AssignmentCritiqueandRedesign_MakeoverMonday_CelinaXue_InitialDraft/InitialDraft">
      <img
        alt="Initial draft comparing food costs per 20g of protein"
        src="https://public.tableau.com/static/images/As/AssignmentCritiqueandRedesign_MakeoverMonday_CelinaXue_InitialDraft/InitialDraft/1_rss.png"
        style="border: none;"
      />
    </a>
  </noscript>

  <object class="tableauViz" style="display: none;">
    <param name="host_url" value="https%3A%2F%2Fpublic.tableau.com%2F" />
    <param name="embed_code_version" value="3" />
    <param name="site_root" value="" />
    <param name="name" value="AssignmentCritiqueandRedesign_MakeoverMonday_CelinaXue_InitialDraft/InitialDraft" />
    <param name="tabs" value="no" />
    <param name="toolbar" value="yes" />
    <param name="static_image" value="https://public.tableau.com/static/images/As/AssignmentCritiqueandRedesign_MakeoverMonday_CelinaXue_InitialDraft/InitialDraft/1.png" />
    <param name="animate_transition" value="yes" />
    <param name="display_static_image" value="yes" />
    <param name="display_spinner" value="yes" />
    <param name="display_overlay" value="yes" />
    <param name="display_count" value="yes" />
    <param name="language" value="en-US" />
    <param name="filter" value="publish=yes" />
  </object>
</div>

<script type="text/javascript">
  var draftContainer = document.getElementById("viz1794522529212");
  var draftViz = draftContainer.getElementsByTagName("object")[0];

  draftViz.style.width = "100%";
  draftViz.style.height = (draftContainer.offsetWidth * 0.75) + "px";

  var draftScript = document.createElement("script");
  draftScript.src = "https://public.tableau.com/javascripts/api/viz_v1.js";
  draftViz.parentNode.insertBefore(draftScript, draftViz);
</script>

I used an early Tableau visualization as my digital sketch. I changed the vertical bars to horizontal bars so the food names could be read without rotation. I sorted the foods from lowest to highest cost and added price labels to make exact values easier to find.

My early draft highlighted foods costing less than $1 per 20g of protein. This gave readers a quick way to identify lower-cost options. I also explored dietary filters so readers could focus on vegan or vegetarian foods.

This draft improved readability, but displaying every price and all 22 foods in one list still created a lot of information to scan. I needed feedback on whether the visual emphasis and organization helped readers answer the main question.

## Step four: Test the solution

I gathered peer feedback on my initial Tableau draft and recorded it on a feedback sheet. The comments below summarize the group notes rather than individual interview transcripts.

### Peer feedback

The feedback confirmed that the title clearly introduced the main question. However, there were too many foods to scan at once, and labeling every price made the chart feel crowded. The subtitle also repeated information already provided by the axis.

Suggestions included highlighting expensive options in red, using bold labels to emphasize important information, adding average costs as reference points, and organizing foods into groups. Dietary preferences, such as vegan and vegetarian options, were also suggested as ways to help readers find relevant foods.

### Changes based on the feedback

I organized the foods into three groups: **Beans, nuts & tofu**, **Dairy & eggs**, and **Meat & Fish**. This kept all 22 foods while breaking the long list into smaller sections. Within each group, I sorted the foods from lowest to highest cost.

I added dashed group-average lines to provide comparison points. I highlighted each group's lowest-cost food in green and highest-cost food in red, leaving the other bars gray. I also reduced the visible price labels to each group's minimum and maximum, made those labels bold, and retained hover tooltips for other exact prices.

To reduce repetition, I changed the subtitle to explain how to use the chart. I also combined the separate dietary filters into one **Diet preference** menu with **All Foods**, **Vegetarian**, and **Vegan** options.

### What I learned

The main pattern in the feedback was a need for clearer organization and stronger visual emphasis. I learned that improving the chart did not require removing foods or adding more information. Grouping the foods and selectively highlighting important values helped guide readers toward the comparisons that mattered.

## Step five: Build the solution

<div class="tableauPlaceholder" id="viz1794522692727" style="position: relative;">
  <noscript>
    <a href="https://public.tableau.com/views/AssignmentCritiqueandRedesign_MakeoverMonday_CelinaXue_FinalRedesign/FinalRedesign">
      <img
        alt="Final redesign comparing protein costs within food groups"
        src="https://public.tableau.com/static/images/As/AssignmentCritiqueandRedesign_MakeoverMonday_CelinaXue_FinalRedesign/FinalRedesign/1_rss.png"
        style="border: none;"
      />
    </a>
  </noscript>

  <object class="tableauViz" style="display: none;">
    <param name="host_url" value="https%3A%2F%2Fpublic.tableau.com%2F" />
    <param name="embed_code_version" value="3" />
    <param name="site_root" value="" />
    <param name="name" value="AssignmentCritiqueandRedesign_MakeoverMonday_CelinaXue_FinalRedesign/FinalRedesign" />
    <param name="tabs" value="no" />
    <param name="toolbar" value="yes" />
    <param name="static_image" value="https://public.tableau.com/static/images/As/AssignmentCritiqueandRedesign_MakeoverMonday_CelinaXue_FinalRedesign/FinalRedesign/1.png" />
    <param name="animate_transition" value="yes" />
    <param name="display_static_image" value="yes" />
    <param name="display_spinner" value="yes" />
    <param name="display_overlay" value="yes" />
    <param name="display_count" value="yes" />
    <param name="language" value="en-US" />
    <param name="filter" value="publish=yes" />
  </object>
</div>

<script type="text/javascript">
  var finalContainer = document.getElementById("viz1794522692727");
  var finalViz = finalContainer.getElementsByTagName("object")[0];

  finalViz.style.width = "100%";
  finalViz.style.height = (finalContainer.offsetWidth * 0.75) + "px";

  var finalScript = document.createElement("script");
  finalScript.src = "https://public.tableau.com/javascripts/api/viz_v1.js";
  finalViz.parentNode.insertBefore(finalScript, finalViz);
</script>

<p>
  <a href="https://public.tableau.com/views/AssignmentCritiqueandRedesign_MakeoverMonday_CelinaXue_FinalRedesign/FinalRedesign">
    Open the interactive visualization on Tableau Public
  </a>
</p>

<!-- Optional: paste your Tableau Public embed code here to display the interactive visualization directly on this page. -->

The final visualization asks, **“Which foods provide protein at the lowest cost?”** It compares costs per 20g of protein in US dollars using the supplied challenge dataset.

I retained horizontal bars because their lengths make cost differences easy to compare, while the food names remain readable. Foods are sorted from lowest to highest cost within each group and use a shared axis starting at zero.

The final design includes:

- **Food groups** to organize the 22 foods into smaller sets.
- **Green and red highlights** for the lowest- and highest-cost foods within each group, with other foods shown in gray.
- **Bold price labels at each group's cost extremes** to emphasize key comparisons without labeling every bar.
- **Dashed group-average lines** to provide a reference point within each group.
- **Hover tooltips** for exact costs on the remaining bars.
- **One Diet preference menu** with All Foods, Vegetarian, and Vegan options.

I initially used separate Vegan and Vegetarian filters. However, choosing False means excluding foods in that dietary category; it does not mean turning the filter off. I replaced the two controls with one menu to make the choices clearer.

In this dataset, chicken legs and skim milk each cost about **$0.65 per 20g of protein**, while peanuts are the lowest-cost option in the beans, nuts, and tofu group at about **$0.68**. Canned chicken is the highest-cost food shown at about **$3.54**. These findings apply to the supplied foods and prices, rather than all products available to shoppers.

The group averages describe the foods included in each group, not the average prices of those food categories across the wider market. The chart compares protein cost; it does not measure overall nutritional quality or account for every factor involved in choosing food.

This process helped me see that a redesign involves more than changing chart orientation or colors. The critique identified potential problems, the draft made my ideas concrete, and peer feedback helped me decide which changes would make the comparison easier to use.

## References

- [Makeover Monday — 2023 Week 8](https://makeovermonday.vercel.app/dataset/2023w8). Challenge page and supplied `Protein Costs.xlsx` dataset. The challenge credits Lifehacker and data preparation by Brittany Rosenau.
- [The Bodybuilding Dietitians — What Are The Cheapest High-Protein Foods?](https://www.thebodybuildingdietitians.com/blog/how-cost-effective-is-your-high-protein-diet). Original visualization, published November 26, 2021.
- [Lifehacker — The Cheapest Ways to Get Your Protein Right Now](https://lifehacker.com/the-cheapest-ways-to-get-your-protein-right-now-1850001760). Article linked by the challenge.
- [Stephen Few — Data Visualization Effectiveness Profile](https://www.perceptualedge.com/articles/visual_business_intelligence/data_visualization_effectiveness_profile.pdf). Framework used for the critique.
- [Design and Redesign in Data Visualization](https://medium.com/@hint_fm/design-and-redesign-4ab77206cf9). Course reading about critique through redesign.

## AI acknowledgements

I used ChatGPT to help provide Tableau guidance, and to help modify the GitHub md. I built the visualization in Tableau and used the peer feedback recorded on my feedback sheet to guide the redesign.

[Back to my portfolio](https://celinaxue.github.io/celina-dataviz-portfolio/)
