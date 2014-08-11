ADD
===

04 ib ADD AL, imm8 I Valid Valid Add imm8 to AL.
05 iw ADD AX, imm16 I Valid Valid Add imm16 to AX.
05 id ADD EAX, imm32 I Valid Valid Add imm32 to EAX.
REX.W + 05 id ADD RAX, imm32 I Valid N.E. Add imm32 sign-extended to 64-bits to RAX.
80 /0 ib ADD r/m8, imm8 MI Valid Valid Add imm8 to r/m8.
REX + 80 /0 ib ADD r/m8*, imm8 MI Valid N.E. Add sign-extended imm8 to r/m64.
81 /0 iw ADD r/m16, imm16 MI Valid Valid Add imm16 to r/m16.
81 /0 id ADD r/m32, imm32 MI Valid Valid Add imm32 to r/m32.
REX.W + 81 /0 id ADD r/m64, imm32 MI Valid N.E. Add imm32 sign-extended to 64-bits to r/m64.
83 /0 ib ADD r/m16, imm8 MI Valid Valid Add sign-extended imm8 to r/m16.
83 /0 ib ADD r/m32, imm8 MI Valid Valid Add sign-extended imm8 to r/m32.
REX.W + 83 /0 ib ADD r/m64, imm8 MI Valid N.E. Add sign-extended imm8 to r/m64.
00 /r ADD r/m8, r8 MR Valid Valid Add r8 to r/m8.
REX + 00 /r ADD r/m8*, r8* MR Valid N.E. Add r8 to r/m8.
01 /r ADD r/m16, r16 MR Valid Valid Add r16 to r/m16.
01 /r ADD r/m32, r32 MR Valid Valid Add r32 to r/m32.
REX.W + 01 /r ADD r/m64, r64 MR Valid N.E. Add r64 to r/m64.
02 /r ADD r8, r/m8 RM Valid Valid Add r/m8 to r8.
REX + 02 /r ADD r8*, r/m8* RM Valid N.E. Add r/m8 to r8.
03 /r ADD r16, r/m16 RM Valid Valid Add r/m16 to r16.
03 /r ADD r32, r/m32 RM Valid Valid Add r/m32 to r32.
REX.W + 03 /r ADD r64, r/m64 RM Valid N.E. Add r/m64 to r64.

## ADDPD

66 0F 58 /r
ADDPD xmm1, xmm2/m128
RM V/V SSE2 Add packed double-precision floating-point 
values from xmm2/m128 to xmm1.
VEX.NDS.128.66.0F.WIG 58 /r
VADDPD xmm1,xmm2, xmm3/m128
RVM V/V AVX Add packed double-precision floating-point 
values from xmm3/mem to xmm2 and stores 
result in xmm1.
VEX.NDS.256.66.0F.WIG 58 /r
VADDPD ymm1, ymm2, ymm3/m256
RVM V/V AVX Add packed double-precision floating-point 
values from ymm3/mem to ymm2 and stores 
result in ymm1.

## ADDPS

0F 58 /r
ADDPS xmm1, xmm2/m128
RM V/V SSE Add packed single-precision floating-point 
values from xmm2/m128 to xmm1 and stores 
result in xmm1.
VEX.NDS.128.0F.WIG 58 /r
VADDPS xmm1,xmm2, xmm3/m128
RVM V/V AVX Add packed single-precision floating-point 
values from xmm3/mem to xmm2 and stores 
result in xmm1.
VEX.NDS.256.0F.WIG 58 /r
VADDPS ymm1, ymm2, ymm3/m256
RVM V/V AVX Add packed single-precision floating-point 
values from ymm3/me
