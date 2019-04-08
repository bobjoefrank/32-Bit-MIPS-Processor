# MIPS Processor in SystemVerilog
Final project for EECS 31L.
![](https://github.com/bobjoefrank/32-Bit-MIPS-Processor/blob/master/MIPS_design_flow.png)

## Abstract
Processor based on the principles of the MIPS architecture capable of executing 32-bit instructions. All files were combined into one for easier grading. A wrapper was used to display the output onto the 7-segment display of the Basys-3 FPGA board. 

## Supported Instructions
| Instruction | OpSel | Operation | Syntax |
|-------------|--------|-----------|--------|
| Nothing | 1111 | Do Nothing | NOP|
| Add | 0000 | R[rd] = R[rs] + R[rt] | add $rd, $rs, $rt |
| Add immediate | 0111 | R[rt] = R[rs] + immed. | addi $rt, $rs, immed. |
| Subtract | 0011 | R[rd] = R[rs] - R[rt] | sub $rd, $rs, $rt |
| And | 1000 | R[rd] = R[rs] & R[rt] | and $rd, $rs, $rt |
| Or | 1001 | R[rd] = R[rs] \| R[rt] | or $rd, $rs, $rt |
| Xor | 1010 | R[rd] = R[rs] ⊕ R[rt] | xor $rd, $rs, $rt |
| Complement | 1011 | R[rd] = ~R[rs] | nor $rd, $rs |
| 1-bit shift left | 1101 | R[rd] = R[rs] << 1 | shl $rd, $rs, 1 |
| Store to DM | 0110 | Mem(R[rs]+32) = R[rd] | sw $rd, 32($rs) |
| Load to Register | 0100 | R[rd] = Mem(R[rs]+32) | lw $rd, 32($rs) |
