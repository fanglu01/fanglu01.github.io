---
title       : An Interactive View of R Datasets
subtitle    : Slidify + Shiny
author      : Fang Lu
job         : Biologist
framework   : io2012  # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [shiny, interactive, bootstrap, quiz]  # {}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
ext_widgets : {rCharts: [libraries/nvd3]}

---  

## Introductions

In this assignment, I use shiny to display a selected dataset of R package interactively, and create a presentation to introduce this function to users and make this application easily accessiable .

---  .class #id1

## How it works
The users first select the name of dataset and the number of  observations on the left panel. Then clike the submit button. Accordingly, a summary of the selected dataset and the the number of observations will be shown on the right panel.

---  .class #id1 bg:blank

## Interactive Console
<div class="row-fluid">
  <div class="container-fluid">
    <div class="col-sm-4">
      <form class="well">
        <div class="form-group shiny-input-container">
          <label class="control-label" for="dataset">Choose a dataset:</label>
          <div>
            <select id="dataset"><option value="diamonds" selected>diamonds</option>
<option value="economics">economics</option>
<option value="economics_long">economics_long</option>
<option value="faithfuld">faithfuld</option>
<option value="luv_colours">luv_colours</option>
<option value="midwest">midwest</option>
<option value="mpg">mpg</option>
<option value="msleep">msleep</option>
<option value="presidential">presidential</option>
<option value="seals">seals</option>
<option value="txhousing">txhousing</option>
<option value="AirPassengers">AirPassengers</option>
<option value="BJsales">BJsales</option>
<option value="BJsales.lead (BJsales)">BJsales.lead (BJsales)</option>
<option value="BOD">BOD</option>
<option value="CO2">CO2</option>
<option value="ChickWeight">ChickWeight</option>
<option value="DNase">DNase</option>
<option value="EuStockMarkets">EuStockMarkets</option>
<option value="Formaldehyde">Formaldehyde</option>
<option value="HairEyeColor">HairEyeColor</option>
<option value="Harman23.cor">Harman23.cor</option>
<option value="Harman74.cor">Harman74.cor</option>
<option value="Indometh">Indometh</option>
<option value="InsectSprays">InsectSprays</option>
<option value="JohnsonJohnson">JohnsonJohnson</option>
<option value="LakeHuron">LakeHuron</option>
<option value="LifeCycleSavings">LifeCycleSavings</option>
<option value="Loblolly">Loblolly</option>
<option value="Nile">Nile</option>
<option value="Orange">Orange</option>
<option value="OrchardSprays">OrchardSprays</option>
<option value="PlantGrowth">PlantGrowth</option>
<option value="Puromycin">Puromycin</option>
<option value="Seatbelts">Seatbelts</option>
<option value="Theoph">Theoph</option>
<option value="Titanic">Titanic</option>
<option value="ToothGrowth">ToothGrowth</option>
<option value="UCBAdmissions">UCBAdmissions</option>
<option value="UKDriverDeaths">UKDriverDeaths</option>
<option value="UKgas">UKgas</option>
<option value="USAccDeaths">USAccDeaths</option>
<option value="USArrests">USArrests</option>
<option value="USJudgeRatings">USJudgeRatings</option>
<option value="USPersonalExpenditure">USPersonalExpenditure</option>
<option value="UScitiesD">UScitiesD</option>
<option value="VADeaths">VADeaths</option>
<option value="WWWusage">WWWusage</option>
<option value="WorldPhones">WorldPhones</option>
<option value="ability.cov">ability.cov</option>
<option value="airmiles">airmiles</option>
<option value="airquality">airquality</option>
<option value="anscombe">anscombe</option>
<option value="attenu">attenu</option>
<option value="attitude">attitude</option>
<option value="austres">austres</option>
<option value="beaver1 (beavers)">beaver1 (beavers)</option>
<option value="beaver2 (beavers)">beaver2 (beavers)</option>
<option value="cars">cars</option>
<option value="chickwts">chickwts</option>
<option value="co2">co2</option>
<option value="crimtab">crimtab</option>
<option value="discoveries">discoveries</option>
<option value="esoph">esoph</option>
<option value="euro">euro</option>
<option value="euro.cross (euro)">euro.cross (euro)</option>
<option value="eurodist">eurodist</option>
<option value="faithful">faithful</option>
<option value="fdeaths (UKLungDeaths)">fdeaths (UKLungDeaths)</option>
<option value="freeny">freeny</option>
<option value="freeny.x (freeny)">freeny.x (freeny)</option>
<option value="freeny.y (freeny)">freeny.y (freeny)</option>
<option value="infert">infert</option>
<option value="iris">iris</option>
<option value="iris3">iris3</option>
<option value="islands">islands</option>
<option value="ldeaths (UKLungDeaths)">ldeaths (UKLungDeaths)</option>
<option value="lh">lh</option>
<option value="longley">longley</option>
<option value="lynx">lynx</option>
<option value="mdeaths (UKLungDeaths)">mdeaths (UKLungDeaths)</option>
<option value="morley">morley</option>
<option value="mtcars">mtcars</option>
<option value="nhtemp">nhtemp</option>
<option value="nottem">nottem</option>
<option value="npk">npk</option>
<option value="occupationalStatus">occupationalStatus</option>
<option value="precip">precip</option>
<option value="presidents">presidents</option>
<option value="pressure">pressure</option>
<option value="quakes">quakes</option>
<option value="randu">randu</option>
<option value="rivers">rivers</option>
<option value="rock">rock</option>
<option value="sleep">sleep</option>
<option value="stack.loss (stackloss)">stack.loss (stackloss)</option>
<option value="stack.x (stackloss)">stack.x (stackloss)</option>
<option value="stackloss">stackloss</option>
<option value="state.abb (state)">state.abb (state)</option>
<option value="state.area (state)">state.area (state)</option>
<option value="state.center (state)">state.center (state)</option>
<option value="state.division (state)">state.division (state)</option>
<option value="state.name (state)">state.name (state)</option>
<option value="state.region (state)">state.region (state)</option>
<option value="state.x77 (state)">state.x77 (state)</option>
<option value="sunspot.month">sunspot.month</option>
<option value="sunspot.year">sunspot.year</option>
<option value="sunspots">sunspots</option>
<option value="swiss">swiss</option>
<option value="treering">treering</option>
<option value="trees">trees</option>
<option value="uspop">uspop</option>
<option value="volcano">volcano</option>
<option value="warpbreaks">warpbreaks</option>
<option value="women">women</option></select>
            <script type="application/json" data-for="dataset" data-nonempty="">{}</script>
          </div>
        </div>
        <div class="form-group shiny-input-container">
          <label for="obs">Number of observations to view:</label>
          <input id="obs" type="number" class="form-control" value="10"/>
        </div>
        <span class="help-block">Note: while the data view will show only the specified number of observations, the summary will still be based on the full dataset.</span>
        <div>
          <button type="submit" class="btn btn-primary">Update View</button>
        </div>
      </form>
    </div>
    <div class="col-sm-8">
      <h4>Summary</h4>
      <pre id="summary" class="shiny-text-output"></pre>
      <h4>Observations</h4>
      <div id="view" class="shiny-html-output"></div>
    </div>
  </div>
</div>

--- 


## Summary

The interactive console is working in R Console. However for some reason, the result will not displayed in Slidify for some reason. 

--- 

