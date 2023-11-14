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
