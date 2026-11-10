module full_adder_dataflow( input A, B, Cin, output Sum, Carry ); 
assign Sum = A ^ B ^ Cin; 
assign Carry = (A & B) | (B & Cin) | (A & Cin); 
endmodule



module full_adder_behavioral( input A, B, Cin, output reg Sum, Carry ); 
always @(*) 
begin 
Sum = A ^ B ^ Cin; 
Carry = (A & B) | (B & Cin) | (A & Cin); 
end endmodule
