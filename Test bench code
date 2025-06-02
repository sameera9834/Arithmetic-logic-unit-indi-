module alu_tb;
    reg [3:0] A, B;
    reg op;
    wire [3:0] result;
    wire zero;

    // Instantiate the ALU
    alu uut (A, B, op, result, zero);

    initial begin
        // Test Addition: 5 + 3 = 8 (1000)
        A = 4'b0101; B = 4'b0011; op = 0;
        #10;
        $display("Add: %d + %d = %d, Zero=%b", A, B, result, zero);

        // Test Subtraction: 5 - 3 = 2 (0010)
        A = 4'b0101; B = 4'b0011; op = 1;
        #10;
        $display("Sub: %d - %d = %d, Zero=%b", A, B, result, zero);

        // Test Zero Flag: 4 - 4 = 0 (0000)
        A = 4'b0100; B = 4'b0100; op = 1;
        #10;
        $display("Sub: %d - %d = %d, Zero=%b", A, B, result, zero);

        $finish;
    end
endmodule
