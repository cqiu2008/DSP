DSP48EII使用随想

1.Concatenated A and B ports (A:B) bypass the multiplier and feed the X multiplexer input.
The 30-bit A input port forms the upper 30 bits of A:B concatenated datapath, and the
18-bit B input port forms the lower 18 bits of the A:B datapath. The A:B datapath, together
with the C input port, enables each DSP48E2 slice to implement a full 48-bit

可以实现 {A[26:0],B[17:0]}+C 组成完整的48Bit加法器，看看可以考虑实现resNet中的A‘=A+B这种网络结构哦
48Bit的加法器也很有吸引力，一定要充分利用DSP资源，不放过任何机会，^_^

2.The multiplier can emulate unsigned math by setting the MSB of an input
operand to zero.

可以将补位的乘法器，最高位补成0,这样就变成了无符号数的乘法器了
嘎嘎噶
