# Fault plane solution

SEISAN有四種不同計算方法找出斷層面解。

下面，示範兩種常用的方法FOCMEC和FPFIT。

SEISAN has 4 different programs for fault plane solutions, two of which also work with amplitudes. Here we will demonstrate two popular programs with polarities, FOCMEC and FPFIT.  
 Select the local event and pick all the possible polarities on the Z-channels \(select as shown in 5.4\), see 7.4.3 how this is done. Some traces are not so clear so use a lot of zoom and maybe amplify trace amplitudes \(see 5.2\). In the example below for station ASK, Z-component, both zoom and amplification has been used to clearly see the polarity.

![](/assets/seisan-tutorial-045.png)

Before attempting a fault plane solution, make sure the depth is reasonable and not zero. For this event it should be between 10 and 25 km. If not ok, the depth should be fixed in the S-file by putting an ‘F’ in column 44 on header line.  
 First the FPFIT program is used. It will automatically find a solution in a least squares sense. It does not mean it is correct solution but the best with the available data. Use command ‘fp’.

![](/assets/seisan-tutorial-046.png)

In this case multiple solutions are found and the first is saved in the S-file. Below is part of S- file with the solution.

![](/assets/seisan-tutorial-047.png)

We can now plot the solution with command ‘fo’. It is seen below that all polarities but one fits the solution and it is also seen that other solutions are possible.

![](/assets/seisan-tutorial-048.png)

It is possible to see which stations belong to which polarities, give command ‘f’.

![](/assets/seisan-tutorial-049.png)

and the following plot comes up showing stations and polarities.

![](/assets/seisan-tutorial-050.png)We will now try the FOCMEC program. This program will not automatically find a solution but show all the solutions possible within some given criteria. FOCMEC can also work with amplitude ratios but here only polarities will be used. Start with command ‘f’.

![](/assets/seisan-tutorial-051.png)

and this follows

![](/assets/seisan-tutorial-052.png)

The search is limited to a requirement that all polarities are ok, however, often there are no solutions without allowing some bad polarities. The search is in a 5 deg grid, allowing a finer grid will find more solutions and a courser grid fewer.  
 The solutions found are seen below. It is seen that the majority of the solutions are similar to the FPFIT solution. However searching with a smaller grid size will give hundreds of solutions so obviously the fault plane solution is not very constrained.

![](/assets/seisan-tutorial-053.png)

One of the solutions can be selected by moving the cursor to the corresponding P or T and pressing ‘p’ or ‘t’. The solution should then be saved:

![](/assets/seisan-tutorial-054.png)

and there are now 2 fault plane solutions in S-file, indicated by the F-lines:

![](/assets/seisan-tutorial-055.png)

The 2 solutions can be plotted with command ‘fo’ as before and we get:

![](/assets/seisan-tutorial-056.png)

It is seen that the two solutions are similar but FOCMEC also had very different solutions. It is always useful to compare solutions from different programs.  
 Doing the exercise yourself might result in quite different solutions since some polarities are uncertain.

