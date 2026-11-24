---
title: "About"
permalink: /
author_profile: true
---

I'm a **Data Scientist and Python developer** based in Berlin, working across machine learning, data analysis, scientific computing, and software development.

I like problems where the difficult part is not simply training a model, but figuring out **what is actually in the data, what can reasonably be learned from it, and whether the result will still work outside the dataset it was developed on**.

My background is in experimental science, so I tend to approach data with a mix of curiosity and skepticism. Before reaching for a more complex model, I want to understand the structure of the problem, the assumptions behind the data, and what the validation results are really telling me.

These days, a lot of my work involves taking that process beyond notebooks: building reproducible pipelines, analytical tools, databases, dashboards, and small applications that connect data analysis with real workflows.

## What I'm Working On

I'm currently working as a **Data Scientist at IAP in Berlin-Adlershof**.

My day-to-day work includes:

* Exploring and modelling complex datasets
* Regression and classification
* Feature engineering and multivariate analysis
* Model validation, robustness, and generalisation
* Data-processing and automation pipelines
* Structured data and database workflows
* Interactive tools and dashboards with Python
* Connecting data acquisition, analysis, modelling, and visualisation

The data I currently work with mainly comes from scientific and technical measurements. But the questions behind it are much more general: how to work with noisy or limited data, how to handle correlated variables and domain shifts, how to validate models properly, and how to turn analysis into something useful.


## Featured Project

<section id="taxi-project" aria-labelledby="taxi-project-title">
  <h3 id="taxi-project-title">NYC Taxi Demand Forecasting & Optimization</h3>
  <p><strong data-field="status">In progress</strong></p>
  <p data-field="summary">An applied forecasting project exploring how recorded taxi pickups can support fleet planning. I use DuckDB and pandas to validate trip records, combine daily counts with weather data, and compare simple forecasts using chronological evaluation.</p>
  <p data-field="finding">In an April experiment, daily updates reduced forecast bias but increased mean absolute error by 15.2% compared with a fixed monthly forecast. More frequent updates did not automatically improve accuracy.</p>
  <p><strong>Built so far:</strong> <span data-field="completed">Daily data validation, weather integration, weekday-mean baselines, daily walk-forward evaluation, and five metric unit tests.</span></p>
  <p><strong>Next:</strong> <span data-field="next">Evaluate longer rolling windows and reserve a later unseen period for final testing. Fleet assignment optimization is planned.</span></p>
  <p data-field="technologies">Python · SQL · DuckDB · pandas · pytest</p>
  <p><a href="https://github.com/cakirtufan/nyc-taxi-forecasting-and-optimization">Explore the project on GitHub</a></p>
  <p><small>Project update: <span data-field="updated">2026-11-24</span></small></p>
</section>

<script>
(function () {
  var card = document.getElementById("taxi-project");
  fetch("https://raw.githubusercontent.com/cakirtufan/nyc-taxi-forecasting-and-optimization/main/portfolio-summary.json", {cache: "no-cache"})
    .then(function (response) {
      if (!response.ok) throw new Error("Summary unavailable");
      return response.json();
    })
    .then(function (data) {
      ["status", "summary", "finding", "completed", "next", "updated"].forEach(function (key) {
        if (typeof data[key] === "string" && data[key].trim()) {
          card.querySelector('[data-field="' + key + '"]').textContent = data[key];
        }
      });
      if (typeof data.title === "string" && data.title.trim()) {
        document.getElementById("taxi-project-title").textContent = data.title;
      }
      if (Array.isArray(data.technologies) && data.technologies.every(function (item) { return typeof item === "string"; })) {
        card.querySelector('[data-field="technologies"]').textContent = data.technologies.join(" · ");
      }
    })
    .catch(function () { /* Keep the embedded project description available. */ });
}());
</script>

## How I Work

I'm not particularly interested in throwing every available algorithm at a dataset and keeping whichever one produces the highest score.

I'd rather understand why a model works, what information it is using, where it starts to fail, and whether the validation setup actually represents the problem we care about.

For me, good data science sits somewhere between **statistics, software, domain knowledge, and careful reasoning**.

## Background

Before moving more deeply into data science and machine learning, I worked in experimental research and materials science.

That background still influences how I approach technical problems, especially when data comes from a real physical process and uncertainty, measurement conditions, or experimental constraints matter.

I see that experience as useful context rather than a domain boundary: the tools and ways of thinking I use are applicable far beyond scientific data.

## Interests

Some areas I currently enjoy working with:

* Machine learning and statistical modelling
* Exploratory data analysis
* Model validation and generalisation
* Multivariate analysis
* Optimisation and adaptive sampling
* Computer vision
* Data pipelines and automation
* Interactive analytical software
* Databases and structured data workflows
* Decision-support tools
* Python applications for data-heavy problems

## Links

* [Google Scholar](https://scholar.google.com/citations?user=Fw-rZvQAAAAJ&hl=en)
* [ORCID](https://orcid.org/0000-0002-5033-9577)
* [GitHub](https://github.com/cakirtufan)
* [LinkedIn](https://www.linkedin.com/in/cafer-tufan-%C3%A7ak%C4%B1r-26b2b731/)
