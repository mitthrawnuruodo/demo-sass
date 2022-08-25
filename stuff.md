## Commands
sass input.scss output.css
sass --watch input.scss output.css
sass --watch app/sass:public/stylesheets

## Comments
// This comment won't be included in the CSS.
/* 
    But this comment will be included in the CSS, 
    except in compressed mode. 
*/

## Variables
$secondary-color: #543;

h1 {
  color: $secondary-color;
}

# Nesting
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}

## Extend

.button-basic  {
    border: none;
    padding: 15px 30px;
    text-align: center;
    font-size: 16px;
    cursor: pointer;
}
  
.button-report  {
    @extend .button-basic;
    background-color: red;
}
  
.button-submit  {
    @extend .button-basic;
    background-color: green;
    color: white;
}

## Operators

@use 'sass:math';

.container {
  display: flex;
}

article[role="main"] {
  width: math.div(600px, 960px) * 100%;
}

aside[role="complementary"] {
  width: math.div(300px, 960px) * 100%;
  margin-left: auto;
}