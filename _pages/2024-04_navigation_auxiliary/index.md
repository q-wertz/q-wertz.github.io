---
permalink: /2024-04_navigation_auxiliary
title: "Auxiliary plots for navigation paper"
author_profile: false
---

## Introduction

This page contains some auxiliary information on the paper 

> Sonnleitner, C., Hobiger, T. Wide-area multilateration airspace surveillance with unsynchronized low-cost ADS-B receivers using TDOA observations. *NAVIGATION*.

As quite a lot of figures have been produced that break the frame of the paper but still contain useful insights they are given here.

## Simulations

### Overview 

The simulations presented in the paper are:

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg th{background-color:#cccccc;border-width:0;font-size:14px;font-weight:bold;overflow:hidden;padding:10px 5px;word-break:normal;text-align:center;vertical-align:center}
.tg td{border-width:0;font-size:14px;overflow:hidden;padding:10px 5px;word-break:normal;vertical-align:center}
.tg .tg-odd{border-color:#000000;text-align:center}
.tg .tg-even{background-color:#e6e6e6;border-color:#000000;text-align:center}
</style>
<table class="tg">
<thead>
  <tr>
    <th colspan="2">Observation types</th>
    <th colspan="2">Ground stations</th>
    <th rowspan="2">TOA measurement uncertainty</th>
    <th rowspan="2">Clocks</th>
    <th rowspan="2">Identifier</th>
  </tr>
  <tr>
    <th>TDOA</th>
    <th>ADS-B pos</th>
    <th>#</th>
    <th>Placement</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-odd">✅</td>
    <td class="tg-odd"></td>
    <td class="tg-odd">42</td>
    <td class="tg-odd">Grid placed 120km</td>
    <td class="tg-odd">100ns</td>
    <td class="tg-odd">Perfect</td>
    <td class="tg-odd">T_G42-P</td>
  </tr>
  <tr>
    <td class="tg-even">✅</td>
    <td class="tg-even"></td>
    <td class="tg-even">42</td>
    <td class="tg-even">Grid placed 120km</td>
    <td class="tg-even">100ns</td>
    <td class="tg-even">SI532</td>
    <td class="tg-even">T_G42-S</td>
  </tr>
  <tr>
    <td class="tg-odd">✅</td>
    <td class="tg-odd"></td>
    <td class="tg-odd">56</td>
    <td class="tg-odd">Grid placed 100km</td>
    <td class="tg-odd">100ns</td>
    <td class="tg-odd">SI532</td>
    <td class="tg-odd">T_G56-S</td>
  </tr>
  <tr>
    <td class="tg-even">✅</td>
    <td class="tg-even"></td>
    <td class="tg-even">42</td>
    <td class="tg-even">Grid placed 120km</td>
    <td class="tg-even">1us</td>
    <td class="tg-even">SI532</td>
    <td class="tg-even">T_G42-S-1u</td>
  </tr>
  <tr>
    <td class="tg-odd">✅</td>
    <td class="tg-odd">✅</td>
    <td class="tg-odd">42</td>
    <td class="tg-odd">Grid placed 120km</td>
    <td class="tg-odd">100ns</td>
    <td class="tg-odd">SI532</td>
    <td class="tg-odd">TP_G42-S</td>
  </tr>
  <tr>
    <td class="tg-even">✅</td>
    <td class="tg-even"></td>
    <td class="tg-even">60</td>
    <td class="tg-even">Largest cities</td>
    <td class="tg-even">100ns</td>
    <td class="tg-even">Perfect</td>
    <td class="tg-even">T_C60-P</td>
  </tr>
  <tr>
    <td class="tg-odd">✅</td>
    <td class="tg-odd"></td>
    <td class="tg-odd">40</td>
    <td class="tg-odd">Largest cities</td>
    <td class="tg-odd">100ns</td>
    <td class="tg-odd">SI532</td>
    <td class="tg-odd">T_C40-S</td>
  </tr>
  <tr>
    <td class="tg-even">✅</td>
    <td class="tg-even"></td>
    <td class="tg-even">60</td>
    <td class="tg-even">Largest cities</td>
    <td class="tg-even">100ns</td>
    <td class="tg-even">SI532</td>
    <td class="tg-even">T_C60-S</td>
  </tr>
  <tr>
    <td class="tg-odd">✅</td>
    <td class="tg-odd">✅</td>
    <td class="tg-odd">40</td>
    <td class="tg-odd">Largest cities</td>
    <td class="tg-odd">100ns</td>
    <td class="tg-odd">SI532</td>
    <td class="tg-odd">TP_C40-S</td>
  </tr>
</tbody>
</table>

The identifiers are built up by the relevant parameters that differ between the simulations:

{:style="text-align:center;"}
![Explanation of the simulation identifiers](files/identifier_explanation.svg){: width="250pt" }

### Individual plots

#### Ground stations placed in grid

{% tabs grid_placed %}

{% tab grid_placed T_G42-P %}
  {:style="text-align:center;"}
  ![Simulation T_G42-P position error histogram](files/T_G42-P/error_histogram.svg){: width="80%" }

  ![Simulation T_G42-P position error over time](files/T_G42-P/pos_error_in_meter_over_time.svg){: width="100%" }

  ![Simulation T_G42-P WRMSE over time](files/T_G42-P/avg_errors_over_time.svg){: width="100%" }

  {:style="text-align:center;"}
  ![Simulation T_G42-P error over estimated variance](files/T_G42-P/error_over_std.png){: width="50%"}
{% endtab %}

{% tab grid_placed T_G42-S %}
  {:style="text-align:center;"}
  ![Simulation T_G42-S position error histogram](files/T_G42-S/error_histogram.svg){: width="80%" }

  ![Simulation T_G42-S position error over time](files/T_G42-S/pos_error_in_meter_over_time.svg){: width="100%" }

  ![Simulation T_G42-S WRMSE over time](files/T_G42-S/avg_errors_over_time.svg){: width="100%" }

  {:style="text-align:center;"}
  ![Simulation T_G42-S error over estimated variance](files/T_G42-S/error_over_std.png){: width="50%" }
{% endtab %}

{% tab grid_placed T_G56-S %}
  {:style="text-align:center;"}
  ![Simulation T_G56-S position error histogram](files/T_G56-S/error_histogram.svg){: width="80%"}

  ![Simulation T_G56-S position error over time](files/T_G56-S/pos_error_in_meter_over_time.svg){: width="100%" }

  ![Simulation T_G56-S WRMSE over time](files/T_G56-S/avg_errors_over_time.svg){: width="100%" }

  {:style="text-align:center;"}
  ![Simulation T_G56-S error over estimated variance](files/T_G56-S/error_over_std.png){: width="50%" }
{% endtab %}

{% tab grid_placed T_G42-S-1u %}
  {:style="text-align:center;"}
  ![Simulation T_G42-S-1u position error histogram](files/T_G42-S-1u/error_histogram.svg){: width="80%" }

  ![Simulation T_G42-S-1u position error over time](files/T_G42-S-1u/pos_error_in_meter_over_time.svg){: width="100%" }

  ![Simulation T_G42-S-1u WRMSE over time](files/T_G42-S-1u/avg_errors_over_time.svg){: width="100%" }

  {:style="text-align:center;"}
  ![Simulation T_G42-S-1u error over estimated variance](files/T_G42-S-1u/error_over_std.png){: width="50%" }
{% endtab %}

{% tab grid_placed TP_G42-S %}
  {:style="text-align:center;"}
  ![Simulation TP_G42-S position error histogram](files/TP_G42-S/error_histogram.svg){: width="80%" }

  ![Simulation TP_G42-S position error over time](files/TP_G42-S/pos_error_in_meter_over_time.svg){: width="100%" }

  ![Simulation TP_G42-S WRMSE over time](files/TP_G42-S/avg_errors_over_time.svg){: width="100%" }

  {:style="text-align:center;"}
  ![Simulation TP_G42-S error over estimated variance](files/TP_G42-S/error_over_std.png){: width="50%" }
{% endtab %}

{% endtabs %}

#### Ground stations placed in cities

{% tabs cities_placed %}

{% tab cities_placed T_C60-P %}
  {:style="text-align:center;"}
  ![Simulation T_C60-P position error histogram](files/T_C60-P/error_histogram.svg){: width="80%" }

  ![Simulation T_C60-P position error over time](files/T_C60-P/pos_error_in_meter_over_time.svg){: width="100%" }

  ![Simulation T_C60-P WRMSE over time](files/T_C60-P/avg_errors_over_time.svg){: width="100%" }

  {:style="text-align:center;"}
  ![Simulation T_C60-P error over estimated variance](files/T_C60-P/error_over_std.png){: width="50%" }
{% endtab %}

{% tab cities_placed T_C40-S %}
  {:style="text-align:center;"}
  ![Simulation T_C40-S position error histogram](files/T_C40-S/error_histogram.svg){: width="80%" }

  ![Simulation T_C40-S position error over time](files/T_C40-S/pos_error_in_meter_over_time.svg){: width="100%" }

  ![Simulation T_C40-S WRMSE over time](files/T_C40-S/avg_errors_over_time.svg){: width="100%" }

  {:style="text-align:center;"}
  ![Simulation T_C40-S error over estimated variance](files/T_C40-S/error_over_std.png){: width="50%" }
{% endtab %}

{% tab cities_placed T_C60-S %}
  {:style="text-align:center;"}
  ![Simulation T_C60-S position error histogram](files/T_C60-S/error_histogram.svg){: width="80%" }

  ![Simulation T_C60-S position error over time](files/T_C60-S/pos_error_in_meter_over_time.svg){: width="100%" }

  ![Simulation T_C60-S WRMSE over time](files/T_C60-S/avg_errors_over_time.svg){: width="100%" }

  {:style="text-align:center;"}
  ![Simulation T_C60-S error over estimated variance](files/T_C60-S/error_over_std.png){: width="50%" }
{% endtab %}

{% tab cities_placed TP_C40-S %}
  {:style="text-align:center;"}
  ![Simulation TP_C40-S position error histogram](files/TP_C40-S/error_histogram.svg){: width="80%" }

  ![Simulation TP_C40-S position error over time](files/TP_C40-S/pos_error_in_meter_over_time.svg){: width="100%" }

  ![Simulation TP_C40-S WRMSE over time](files/TP_C40-S/avg_errors_over_time.svg){: width="100%" }

  {:style="text-align:center;"}
  ![Simulation TP_C40-S error over estimated variance](files/TP_C40-S/error_over_std.png){: width="50%" }
{% endtab %}

{% endtabs %}