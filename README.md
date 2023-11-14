# verilog-code-for-2-1mux-and-4-1mux-
#verilog code for 2*1 mux 

module mux21(
   input in1,in2,s,
   output reg y  
   );
    always@( in1 or in2 or s)
    begin
    
    if(s)
    y = in2;
    else
    y=in1;
    
    end
   
endmodule


#4*1mux using modules of 2*1muxes

module mux41(input in1,in2,in3,in4,s0,s1,
             output  y
              );
    wire w1,w2;
    mux21 m1(.in1(in1),.in2(in2),.s(s0),.y(w1));
    mux21 m2(.in1(in3),.in2(in4),.s(s0),.y(w2));
    mux21 m3(.in1(w1),.in2(w2),.s(s1),.y(y));
endmodule

