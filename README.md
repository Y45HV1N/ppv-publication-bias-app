# Positive Predictive Value and Publication Bias App

This repository contains a small interactive web app for visualizing how the positive predictive value (PPV) of statistically significant findings depends on the probability that the alternative hypothesis is true, the Type I error rate, statistical power, and publication probabilities.

The app is available here:

https://y45hv1n.github.io/ppv-publication-bias-app/

## What the app shows

The app begins with the standard positive predictive value framework. A fixed set of imaginary studies is classified according to whether:

1. The alternative hypothesis is true or the null hypothesis is true.
2. The study produces a statistically significant or nonsignificant result.

This produces four categories:

- True positives
- False positives
- False negatives
- True negatives

The app then applies a second-stage publication filter. Statistically significant findings are published with one probability, and nonsignificant findings are published with another probability. A second visualization shows the resulting composition of the published literature.

## Parameters

The app lets users manipulate five quantities:

- Probability that H₁ is true
- Type I error rate, alpha
- Statistical power
- Probability of publication if the result is statistically significant
- Probability of publication if the result is not statistically significant

The default values are:

- Probability that H₁ is true: 30%
- Alpha: 0.05
- Power: 36%
- Probability of publication if significant: 60%
- Probability of publication if not significant: 2%

## Interpretation

The app illustrates that the proportion of false positives among statistically significant findings is not determined by alpha alone. It also depends on statistical power and on the base rate of true hypotheses.

The publication filter further shows how selective publication can change the apparent composition of the published literature. Even if many studies are conducted, the published subset may contain a different balance of true positives, false positives, false negatives, and true negatives.

## Technical details

This is a standalone HTML file with embedded CSS and JavaScript. It does not require R, Shiny, a server, or external installation. The app can be run locally by opening `index.html` in a web browser, or hosted as a static site using GitHub Pages.

The visualization uses a fixed number of imaginary studies and rounded expected counts. It is intended as an educational visualization, not as a stochastic simulation of exact p-value distributions.

## Attribution

This app is adapted from Daniël Lakens’s Positive Predictive Value app in Chapter 2, "Error control," of *Improving Your Statistical Inferences*:

https://lakens.github.io/statistical_inferences/02-errorcontrol.html

The source code for the original book and app is available here:

https://github.com/Lakens/statistical_inferences

The original material is licensed under the Creative Commons Attribution 4.0 International License (CC-BY-4.0):

https://creativecommons.org/licenses/by/4.0/

This adapted version modifies the original PPV app by adding publication probabilities and a second visualization for the composition of the published literature.

The standalone HTML, CSS, and JavaScript code for this adaptation was updated with the help of ChatGPT 5.5 Thinking, because I ([Yashvin Seetahul](https://bsky.app/profile/yashvin.bsky.social)) have no formal competence in web app design.

This adaptation is not affiliated with or endorsed by Daniël Lakens.

## License

This adapted version is shared under the Creative Commons Attribution 4.0 International License (CC-BY-4.0).

You are free to share and adapt this material, provided appropriate credit is given.
