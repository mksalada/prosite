+++
title = 'CSS Cardio'
date = 2020-05-06T14:18:37+08:00 # 2024-02-19T14:18:37+08:00
draft = false
description = ""
slug = ""
tags = ["courses", "css", "dev.to"]
canonicalUrl = 'https://dev.to/mksalada/css-cardio-10of'
+++

I took the CSS Grid course on the 19th day of March. I downloaded first all of the videos and study repeatedly offline. I tweeted updates regarding my progress on Twitter ([see here](https://twitter.com/tinsalada/status/1240565911481798658)). I didn't study everyday because I have some things to do and finally today, I finished the course. 

On the 11th video, there's the Spanning and Placing Cardio. 
Spanning and Placing Cardio

```html
<div class="container">
    <div class="item item1">1</div>
    <div class="item item2">2</div>
    <div class="item item3">3</div>
    <div class="item item4">4</div>
    <div class="item item5">5</div>
    <div class="item item6">6</div>
    <div class="item item7">7</div>
    <div class="item item8">8</div>
    <div class="item poop">💩</div>
    <div class="item item9">9</div>
    <div class="item item10">10</div>
    <div class="item item11">11</div>
    <div class="item item12">12</div>
    <div class="item item13">13</div>
    <div class="item item14">14</div>
    <div class="item item15">15</div>
    <div class="item item16">16</div>
    <div class="item item17">17</div>
    <div class="item item18">18</div>
    <div class="item item19">19</div>
    <div class="item item20">20</div>
    <div class="item item21">21</div>
    <div class="item item22">22</div>
    <div class="item item23">23</div>
    <div class="item item24">24</div>
    <div class="item item25">25</div>
    <div class="item item26">26</div>
    <div class="item item27">27</div>
    <div class="item item28">28</div>
    <div class="item item29">29</div>
    <div class="item item30">30</div>
</div>

<style>
    .container {
        display: grid;
        grid-gap: 20px;
        /* Make the grid 10 columns wide, every other taking up twice the free space */

        /* Make the grid have 10 explicit rows, 50px high each */

    }

    /* With Item 1, start at col 3 and go until 5 */

    /* With Item 2, start at col 5 and go until the end */

    /* Make Item 5 double span 2 cols and rows */

    /* Make Item 8 two rows high */

    /* Make Item 15 span the entire grid width */

    /* Make item 18 span 4 widths, but end 9 */

    /* Make item 20 start at row 4 and go for 3 */
</style>
```

### My Answer

I paused the video and answered it. Here's my answer: 

```css
/* Maria Kristina Salada - 04-05-2020 */
    .container {
        display: grid;
        grid-gap: 20px;
        /* Make the grid 10 columns wide, every other taking up twice the free space */
        grid-template-columns: repeat(10, 2fr);
        /* Make the grid have 10 explicit rows, 50px high each */
        grid-template-rows: repeat(10, 50px);
    }

    /* With Item 1, start at col 3 and go until 5 */
    .item1 { grid-column: 3 / 5; }
    /* With Item 2, start at col 5 and go until the end */
    .item2 { grid-column: 5 / -1; }
    /* Make Item 5 double span 2 cols and rows */
    .item5 { grid-column: span 2; grid-row: span 2; }
    /* Make Item 8 two rows high */
    .item8 { grid-row: span 2; }
    /* Make Item 15 span the entire grid width */
    .item15 { grid-column: 1 / -1; }
    /* Make item 18 span 4 widths, but end 9 */
    .item18 { grid-column: span 4 / 9; }
    /* Make item 20 start at row 4 and go for 3 */
    .item20 { grid-row: 4 / span 3; }
```

### Correct Answer

Here's the correct answer: 

```css
.container {
        display: grid;
        grid-gap: 20px;
        /* Make the grid 10 columns wide, every other taking up twice the free space */
        grid-template-columns: repeat(5, 1fr 2fr);

        /* Make the grid have 10 explicit rows, 50px high each */
        grid-template-rows: repeat(10, 50px);
    }

    /* With Item 1, start at col 3 and go until 5 */

    .item1 {
        grid-column: 3 / 5;
    }

    /* With Item 2, start at col 5 and go until the end */

    .item2 {
        grid-column: 5 / -1;
    }

    /* Make Item 5 double span 2 cols and rows */

    .item5 {
        grid-column: span 2;
        grid-row: span 2;
    }

    /* Make Item 8 two rows high */

    .item8 {
        grid-row: span 2;
    }

    /* Make Item 15 span the entire grid width */

    .item15 {
        grid-column: 1 / -1;
    }

    /* Make item 18 span 4 widths, but end 9 */

    .item18 {
        grid-column: span 4 / 9;
    }

    /* Make item 20 start at row 4 and go for 3 */

    .item20 {
        grid-row: 4 / span 3;
    }
```

I only got one wrong answer. The codes are really different but result is almost the same. 

#### Previews

- [My Answer](https://mksalada-demo.netlify.app/page/css-grid-course/Spanning-and-Placing-Cardio/my-answer.html)
- [Correct Answer](https://mksalada-demo.netlify.app/page/css-grid-course/Spanning-and-Placing-Cardio/correct-answer.html)

#### Thanks to

Thanks to Wes Bos, the teacher for the course and to Mozilla for that free course about CSS Grid. You can also take the course. I recommended it for learning CSS Grid because it's fun and informative. Just go to [cssgrid.io](https://cssgrid.io/) and sign up.

![WesBos' CSS Grid Course](https://res.cloudinary.com/practicaldev/image/fetch/s--FY_LTeAy--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://mksalada.tk/file/image/css-grid-course-wesbos.png)
