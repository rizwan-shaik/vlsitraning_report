1. IC (integrated circuit),An integrated circuit or monolithic integrated circuit  is a set of electronic circuits on one small flat piece (or "chip")
of semiconductor material, usually silicon.Large numbers of tiny MOSFETs integrate into a small chip.
2. To design an IC we need to develop a code(programe),for this code we use verilog language which is HDL(Hard Description Language).
3. This IC are build with transistors in it with the gates too,we use the gates in verilog logics codes 
4. lets use design a Hafe Adder circuit in (fig 1)
                            ![image](https://user-images.githubusercontent.com/93262817/147666166-c30646a2-cc2b-401e-9438-b4e3d1bfa64e.png)
                                      (fig 1)
5. In this image (or code) we first write module which is keyword and and next in side the bracets we write all inputs and outputs which is called port list,
    next we write all i/p and o/p and then the gates which are used in the ic and then endmodule
6. we also write testbench for it which is written to verify wether the dsign is perfectly working or not
7.             `timescale 1ns/1ps
                 module half_adder_tb;
                 reg a,b;
                wire sum,co;
                half_adder ha1(a,b,sum,co);
                initial
                begin
                $dumpfile("ha.vcd");
                $dumpvars(1);
                end
                initial
                begin
               {a,b}=2'b00;
               #5 {a,b}=2'b01;
               #5 {a,b}=2'b10;
               #5 {a,b}=2'b11;
               end
               initial
            $monitor("simtime=%0g, a=%b, b=%b, sum=%b, co=%b", $time, a,b,sum,co);
               endmodule 
8. In this testbench we need to write first timescale in every testbenchs for every ic design codes, next we write module and all i/p and o/p,next we write $dumpfile 
   to get vcd file which is for graph and $dumpvars to take module next we give input values and $monitor to view output of the programe and endmodule to end the code 
9. we various tools to run and check the programe we use a simple tool called edaplayground tool 
10. Which looks like as the below picture (fig 2)
                ![image](https://user-images.githubusercontent.com/93262817/147925829-a9ffc105-2c13-454c-8a68-0e4cc0cbb68d.png)
                       (fig 2)
12.  In this image we can see the design in the we write design code and we write testbench in left side 
13.  we give a name to it here in the imge we can see in (fig 3) 
                      ![image](https://user-images.githubusercontent.com/93262817/147925930-f17f685c-540f-4ecf-9578-c6cb86189e90.png)
                                   (fig 3)
15.   we select the tools from here like icorus and yosys tools (fig 4.1,4.2) 
                      ![image](https://user-images.githubusercontent.com/93262817/147735781-57ccad3d-5125-40b0-bff0-f283aac35770.png)
                                            (fig 4.1)
                     ![image](https://user-images.githubusercontent.com/93262817/147735867-99d69b5d-8219-4802-9aed-f9179ac03782.png)
                                      (fig 4.2)
18.   and after runnig the code we get this kind of graph in (fig 5) 
                        ![image](https://user-images.githubusercontent.com/93262817/147926824-d7208297-ea09-4a66-8222-b638c55c15a2.png)
                                         (fig 5) 










