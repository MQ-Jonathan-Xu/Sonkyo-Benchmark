# Sonkyo-Benchmark

Sonkyo-Benchmark is a vibration-based study of a small-scale wind turbine (WT) blade, with the aim of establishing a benchmark
work for the Structural Health Monitoring (SHM) community. The blade is part of the Windspot 3.5kW WT, provided by Sonkyo Energy, and is tested both experimentally and numerically in healthy and damaged states, under varying environmental and operational conditions.

## Experimental Part

<div style="margin-left:105px">
<table>
  <thead>
      <tr>
        <th align="center", width="120"> Case label </th>
        <th colspan=3, align="left", width="600"> Description </th>
        <th align="center", width="300"> Number of experiments </th>
      </tr>
  </thead>
  <body>
      <tr>
          <td align="center"> R </td>
          <td colspan=3> Healthy state </td>
          <td align="center"> 21 per temperature per set-up </td>
      </tr>
      <tr>
          <td align="center"> A </td>
          <td colspan=3> Added mass 1 x 44 gr </td>
          <td align="center"> 6 per temperature per set-up </td>
      </tr>
      <tr>
          <td align="center"> B </td>
          <td colspan=3> Added mass 2 x 44 gr </td>
          <td align="center"> 6 per temperature per set-up </td>
      </tr>
      <tr>
          <td align="center"> C </td>
          <td colspan=3> Added mass 3 x 44 gr </td>
          <td align="center"> 6 per temperature per set-up </td>
      </tr>
      <tr>
          <td align="center"> D </td>
          <td colspan=3> Crack 1: l1 = 5 cm </td>
          <td align="center"> 6 per temperature per set-up </td>
      </tr>
      <tr>
          <td align="center"> E </td>
          <td> Crack 1: l1 = 5 cm, </td> 
          <td colspan=2> Crack 2: l2 = 5 cm </td>
          <td align="center"> 6 per temperature per set-up </td>
      </tr>
      <tr>
          <td align="center"> F </td>
          <td> Crack 1: l1 = 5 cm, </td>
          <td> Crack 2: l2 = 5 cm, </td>
          <td> Crack 3: l3 = 5 cm </td>
          <td align="center"> 6 per temperature per set-up </td>
      </tr>
      <tr>
          <td align="center"> G </td>
          <td> Crack 1: l1 = 10 cm, </td>
          <td> Crack 2: l2 = 5 cm, </td>
          <td> Crack 3: l3 = 5 cm </td>
          <td align="center"> 6 per temperature per set-up </td>
      </tr>
      <tr>
          <td align="center"> H </td>
          <td> Crack 1: l1 = 10 cm, </td>
          <td> Crack 2: l2 = 10 cm, </td>
          <td> Crack 3: l3 = 5 cm </td>
          <td align="center"> 6 per temperature per set-up </td>
      </tr>
      <tr>
          <td align="center"> I </td>
          <td> Crack 1: l1 = 10 cm, </td>
          <td> Crack 2: l2 = 10 cm, </td>
          <td> Crack 3: l3 = 10 cm </td>
          <td align="center"> 6 per temperature per set-up </td>
      </tr>
      <tr>
          <td align="center"> J </td>
          <td> Crack 1: l1 = 15 cm, </td>
          <td> Crack 2: l2 = 5 cm, </td>
          <td> Crack 3: l3 = 5 cm </td>
          <td align="center"> 6 per temperature per set-up </td>
      </tr>
      <tr>
          <td align="center"> K </td>
          <td> Crack 1: l1 = 15 cm, </td>
          <td> Crack 2: l2 = 15 cm, </td>
          <td> Crack 3: l3 = 5 cm </td>
          <td align="center"> 6 per temperature per set-up </td>
      </tr>
      <tr>
          <td align="center"> L </td>
          <td> Crack 1: l1 = 15 cm, </td>
          <td> Crack 2: l2 = 15 cm, </td>
          <td> Crack 3: l3 = 15 cm </td>
          <td align="center"> 6 per temperature per set-up </td>
      </tr>
  </tbody>
</table>
</div>


## Numerical Part

In this numerical part, a Finite Element (FE) model of the Windspot 3.5kW blade is constructed with the aim of supplementing the experimental work with a physical model exposed to diverse operational conditions, loading scenarios and damage patterns that are not easily explorable and controllable in the laboratory.

A detailed description of the numerical model and the underlying assumptions, as well as the spectrum of operational conditions, the measured quantities and the wind load model is offered in the [paper](https://github.com/ETH-WindMil/Sonkyo-Benchmark), which also serves as the manual for the Matlab application.

### Getting started

Pull down a copy by downloading or cloning the repository

```
git clone https://github.com/ETH-WindMil/Sonkyo-Benchmark ~/Sonkyo-Benchmark
```

### Results

Upon submission and completion of a job named *Job_name*, the following result files are generated, depending on the type of analysis:

**Modal analysis**

<div style="margin-left:55px">
<table>
  <thead>
      <tr>
        <th align="left", width="160">File</th>
        <th align="left", width="160">Field</th>
        <th align="left", width="400">Description</th>
      </tr>
  </thead>
  <body>
      <tr>
          <td rowspan=2, valign="top"> <i>Job_name</i>.mat </td>
          <td> frequencies </td>
          <td> The system natural frequencies in Hz. </td>
      </tr>
      <tr>
          <td> modes </td>
          <td> The corresponding mode shapes at output locations. </td>
      </tr>
  </tbody>
</table>
</div>

**Dynamic analysis**

<div style="margin-left:55px">
<table>
  <thead>
      <tr>
        <th align="left", width="160">File</th>
        <th align="left", width="160">Field</th>
        <th align="left", width="400">Description</th>
      </tr>
  </thead>
  <body>
      <tr>
          <td rowspan=4, valign="top"> <i>Job_name</i>.mat </td>
          <td> time </td>
          <td> The time instants at which solution is obtained. </td>
      </tr>
      <tr>
          <td> strains </td>
          <td> The strain time history at output locations. </td>
      </tr>
      <tr>
          <td> displacements </td>
          <td> The displacement time history at output locations. </td>
      </tr>
      <tr>
          <td> accelerations </td>
          <td> The acceleration time history at output locations. </td>
      </tr>
  </tbody>
</table>
</div>


## Cite as

Ou, Y. and Tatsis, K. E. and Dertimanis, V. K. and Spiridonakos, M. D. and Chatzi, E. N. (2019) "Vibration-based monitoring of a small scale wind turbine blade under varying climate conditions: An experimental benchmark".

Tatsis, K. E. and Ou, Y. and Dertimanis, V. K. and Spiridonakos, M. D. and Chatzi, E. N. (2019) "Vibration-based monitoring of a small scale wind turbine blade under varying climate conditions: A numerical benchmark".

## Found a Bug?

If you think you've found a bug, go ahead and create a new [GitHub issue](https://help.github.com/en/articles/creating-an-issue). Be sure to include as much information as possible so that we can reproduce the bug.
