Download Link: https://assignmentchef.com/product/solved-mae-290chomework-2
<br>
<strong>Problem 1.         </strong>Let us consider the 1D dissipative Burgers equation

<em>∂<sub>t</sub>u </em>+ <em>u∂<sub>x</sub>u </em>= <em>ν∂<sub>xx</sub>u                                                                                  </em>(1)

in a periodic domain 0 ≤ <em>x &lt; </em>2<em>π </em>with <em>ν </em>= 0<em>.</em>001.

<ol>

 <li>Write a pseudospectral code with no dealiasing scheme to solve this equation using <em>N </em>= 128 grid points and the low-storage RK2-<em>θ </em>scheme you derived in Homework 1. Integrate in time for <em>t &lt; </em>2 using a CFL number <em>γ </em>= 0<em>.</em> Let us call this numerical solution raw Burgers.</li>

 <li>Modify your code to include dealiasing with the 2/3 rule (i.e. <em>N </em>= 128 and <em>M </em>= 192) and integrate in time for <em>t &lt; </em>2 using <em>γ </em>= 0<em>.</em> Let us call this numerical solution well done padded Burgers.</li>

 <li>Modify your code to include dealiasing phase shifting (or aliasing error flipping) and integrate in timefor <em>t &lt; </em>2 using <em>γ </em>= 0<em>.</em> Let us call this numerical solution well done flipped Burgers.</li>

 <li>Recall that the RK2-<em>θ </em>scheme in Homework 1 had two degrees of freedom. Let us explore whether we can use that freedom to find a time integration scheme of this family that can perform cheap aliasing error flipping. The idea is to use the flipped error in the second RK2 substep to cancel the error of the first substep.

  <ul>

   <li>Find the Taylor expansion for the aliasing error of the scheme as a function of the constants<em>α<sub>i</sub>, β<sub>i</sub>, γ<sub>i</sub>,ζ</em><sub>1</sub>, <em>i </em>= 1<em>, </em> Assume that the non-linear terms in the second substep are performed on a shifted grid so that the aliasing error of <em>H</em>(<em>u</em><sup>∗</sup>) flips sign.</li>

   <li>Show that there is a scheme where it is possible to cancel out the aliasing error up to first orderwithout additional evaluations of the non-linear terms. Implement this solver and integrate in time for <em>t &lt; </em>2 using <em>γ </em>= 0<em>.</em> Let us call this numerical solution rare cheap flipped Burgers.</li>

  </ul></li>

 <li>Compare the cost and quality of raw Burgers, well done padded Burgers, well done flipped Burgersand rare cheap flipped Burgers.</li>

</ol>