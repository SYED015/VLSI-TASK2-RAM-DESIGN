module ram(
    input clk,
    input [7:0] addr,
    input [7:0] data_in,
    input we, // Write Enable
    output reg [7:0] data_out
);

    reg [7:0] mem [255:0]; // 256 bytes of memory

    always @(posedge clk) begin
        if (we) begin
            mem[addr] <= data_in;
        end
        data_out <= mem[addr];
    end

endmodule


module ram_tb;

    reg clk;
    reg [7:0] addr;
    reg [7:0] data_in;
    reg we;
    wire [7:0] data_out;

    ram uut (.clk(clk), .addr(addr), .data_in(data_in), .we(we), .data_out(data_out));

    initial begin
        clk = 0;
        forever #5 clk = ~clk;
    end

    initial begin
        $dumpfile("ram.vcd");
        $dumpvars(0, ram_tb);

        // Write data to RAM
        we = 1;
        addr = 8'd0;
        data_in = 8'd10;
        #10;

        addr = 8'd1;
        data_in = 8'd20;
        #10;

        // Read data from RAM
        we = 0;
        addr = 8'd0;
                                                     

        addr = 8'd1;
        #10 $display("Data at addr 1: %d", data_out);

        #10 $finish;
    end

endmodule
