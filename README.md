raptor_rfc_5053
===============
  					RAPTOR CODES 


C++ implementation of raptor codes based on RFC 5053 exploring rateless erasure codes. 


1)Application encoder_exe-->
input-->Any file of any size basically any amount of data
output-->A .dat encrypted file

encoding Abstract: 
- "Raptorized" version  with LDPC + Hamming for precodes
- LT Encoder based on Robust Soliton Distribution & R10 Distribution

2)Loosy Channel Application-->
input-->*.dat encoded file,*File size in bytes of input source file
output-->.dat encoded file after random tempering and destruction of originally encoded file

IMP_Note----if file size in bytes of channelled output is less than original File size in bytes-----<"Error"---Raptor codes Failed> 


3)Application decoder_exe-->
input-->*Channeled output file,*File size in bytes of input source file
output-->Exact Reconstruction Source file originally transmitted

decoding Abstract: 
- gaussian elimination over GF(2) as specified in RFC 5053
- LT decoding


Overally mathematical Operations:-
---->Bitwise arithmatic and Xor operations:
---->Inversion of square and rectangular matrices over GF(2)
---->Multiplication of matrices over GF(2)


