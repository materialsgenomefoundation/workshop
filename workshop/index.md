<script src="https://www.paypal.com/sdk/js?client-id=AT6qOEFhfDUQo5WD8iQF3odXJz0Hu8rvDSST1A-ge0vbZTwNgf6oatt5h2q6T4nRMi1_IuBT2xzZLUQY" data-sdk-integration-source="button-factory"></script>

# Software Tools from Machine Learning to Phase Diagrams (July 13 and 14, 2022)

## Organizers

Richard Otis (Materials Genome Foundation)<br>
Dongwon Shin (Oak Ridge National Laboratory)<br>
Brandon Bocklund (Lawrence Livermore National Laboratory)<br>
Zi-Kui Liu (Pennsylvania State University)<br>

*Where:* Virtual (Zoom)<br>
*When:* 11 am - 2 pm EST (5 - 8 pm CET / 8 - 11 am PST) on July 13 and 14, 2022<br>
*Registration deadline:* **July 8, 2022**<br>

## Overview
CALPHAD (Calculation of Phase Diagrams) is one of the most powerful techniques for Materials Genome and Integrated Computational Materials Engineering (ICME) modeling. While originally based on experimental measurements and extrapolation, the CALPHAD approach has been extended to also include results of atomistic simulation for phases and states which are not experimentally accessible. With the introduction of modern workflow management tools in the atomistic community, it is now possible to use atomistic simulations to facilitate rapid CALPHAD database development. More recently, methods and user tools have been developed that enable automated, reproducible CALPHAD parameter evaluation and uncertainty quantification.

This workshop will give a detailed introduction to computational thermodynamic software based on the CALPHAD method  – pycalphad and ESPEI - as well as an introduction to machine learning methods in computational materials science using the ASCENDS software. It will feature hands-on demonstrations in an interactive cloud environment and practical exercises that will enable attendees to perform machine learning calculations, develop CALPHAD databases with quantified uncertainty, and to propagate uncertainty to any thermodynamic calculation.
 
### [ASCENDS](https://github.com/ornlpmcp/ASCENDS)

The Advanced data SCiEnce toolkit for Non-Data scientists (ASCENDS) is an open-source toolkit to assist scientists/engineers who want to apply modern data analytics to their own tabular data _without_ any programming from their local machines. It provides a streamlined, intuitive interface to analyze correlation, train machine learning models, and make predictions from surrogate digital twins within minutes.
[<img class="logo_image" width="100px" src="assets/ascends-logo.png" alt="pyiron logo">](https://github.com/ornlpmcp/ASCENDS)
 
### [pycalphad](https://pycalphad.org)
pycalphad is a free and open-source Python library for calculating phase diagrams, designing thermodynamic models, and investigating phase equilibria within the CALPHAD method.
[<img class="logo_image" width="100px" src="assets/pycalphad-logo-withtext.png" alt="pycalphad logo">](https://pycalphad.org)
It provides routines for reading thermodynamic databases and solving the multi-component, multi-phase Gibbs energy minimization problem.
All Gibbs energy and property models in pycalphad are described symbolically allowing the models to be customized or overridden by users at runtime without changing any of the pycalphad source code. Calculation results from pycalphad are returned as multidimensional xarray datasets that make it easy to incorporate pycalphad into any tool or workflow.
 
### [ESPEI](https://espei.org)
The Extensible Self-optimizing Phase Equilibria Infrastructure (ESPEI) package is a tool for thermodynamic database development and uncertainty quantification within the CALPHAD method.
[<img class="logo_image" width="120px" src="assets/ESPEI-logo-withtext-200px.png" alt="ESPEI logo">](https://espei.org)
It uses pycalphad for the forward calculation of thermodynamic properties to solve the inverse of parameter evaluation problem. ESPEI uses a two step method to first parameterize thermodynamic models and then optimize and determine the uncertainty of the parameters using Markov Chain Monte Carlo (MCMC).

## How to register
Interested graduate students, postdoctoral or early-career researchers, and other enthusiasts are encouraged to register prior to the deadline on **July 8, 2022**.

Please be sure to use a valid e-mail address with payment, as this is how the organizers will communicate with you regarding workshop logistics.

<div id="smart-button-container">
      <div style="text-align: center;">
        <div style="margin-bottom: 1.25rem;">
          <select id="item-options" size="2"><option value="MGF Virtual Workshop Registration - July 13 and 14, 2022 - Standard Attendee" price="199">Standard Attendee - 199 USD</option><option value="MGF Virtual Workshop Registration - July 13 and 14, 2022 - Student Attendee" price="29">Student Attendee - 29 USD</option></select>
          <select style="visibility: hidden" id="quantitySelect"></select>
        </div>
      <div id="paypal-button-container"></div>
      </div>
</div>
<script>
      function initPayPalButton() {
        var shipping = 0;
        var itemOptions = document.querySelector("#smart-button-container #item-options");
    var quantity = parseInt();
    var quantitySelect = document.querySelector("#smart-button-container #quantitySelect");
    if (!isNaN(quantity)) {
      quantitySelect.style.visibility = "visible";
    }
    var orderDescription = 'Software Tools from Machine Learning to Phase Diagrams (July 13 and 14, 2022) MGF Virtual Workshop Registration';
    if(orderDescription === '') {
      orderDescription = 'Item';
    }
    paypal.Buttons({
      style: {
        shape: 'pill',
        color: 'blue',
        layout: 'vertical',
        label: 'paypal',
      },
      createOrder: function(data, actions) {
        var selectedItemDescription = itemOptions.options[itemOptions.selectedIndex].value;
        var selectedItemPrice = parseFloat(itemOptions.options[itemOptions.selectedIndex].getAttribute("price"));
        var tax = (0 === 0 || false) ? 0 : (selectedItemPrice * (parseFloat(0)/100));
        if(quantitySelect.options.length > 0) {
          quantity = parseInt(quantitySelect.options[quantitySelect.selectedIndex].value);
        } else {
          quantity = 1;
        }
        tax *= quantity;
        tax = Math.round(tax * 100) / 100;
        var priceTotal = quantity * selectedItemPrice + parseFloat(shipping) + tax;
        priceTotal = Math.round(priceTotal * 100) / 100;
        var itemTotalValue = Math.round((selectedItemPrice * quantity) * 100) / 100;
        return actions.order.create({
          purchase_units: [{
            description: orderDescription,
            amount: {
              currency_code: 'USD',
              value: priceTotal,
              breakdown: {
                item_total: {
                  currency_code: 'USD',
                  value: itemTotalValue,
                },
                tax_total: {
                  currency_code: 'USD',
                  value: tax,
                }
              }
            },
            items: [{
              name: selectedItemDescription,
              unit_amount: {
                currency_code: 'USD',
                value: selectedItemPrice,
              },
              quantity: quantity
            }],
          }],
          application_context: {
            brand_name: 'Materials Genome Foundation',
            shipping_preference: 'NO_SHIPPING',
          },
        });
      },
      onApprove: function(data, actions) {
        return actions.order.capture().then(function(orderData) {
          // Full available details
          console.log('Capture result', orderData, JSON.stringify(orderData, null, 2));
          // Show a success message within this page, e.g.
          const element = document.getElementById('paypal-button-container');
          element.innerHTML = '';
          element.innerHTML = '<h3>Thank you for registering! If you have any questions, please contact richard.otis@materialsgenomefoundation.org</h3>';
          // Or go to another URL:  actions.redirect('thank_you.html');
        });
      },
      onError: function(err) {
        console.log(err);
      },
    }).render('#paypal-button-container');
  }
  initPayPalButton();
</script>

## Agenda
All times are in Eastern Standard Time.
### Day 1 (July 13, 2022)
- 11:00am Opening
- 11:05 Introduction to data science for materials research
- 11:35 ASCENDS overview
- 12:05pm Break
- 12:15 ASCENDS demonstration
- 12:45 Interactive: Case Studies and Examples
- 1:30 Q&A and closing
 
### Day 2 (July 14, 2022)
- 11:00am Opening
- 11:05 Introduction to pycalphad
- 11:15 Interactive: Calculating thermodynamic properties with pycalphad
- 11:45 Introduction to ESPEI
- 12:00pm Interactive: ESPEI for CALPHAD database assessment and uncertainty quantification
- 12:30 Break
- 12:40 Interactive: Uncertainty propagation with PDUQ
- 1:10 Day 2 Summary and Discussion
- 1:55 Closing
