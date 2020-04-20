# M1522.002400 Principles and Practices of Software Development

- Instructor: Prof. [Chung-Kil Hur](http://sf.snu.ac.kr/gil.hur)
- TA: [Juneyoung Lee](http://sf.snu.ac.kr/juneyoung.lee/)(@aqjune), [Sung-Hwan Lee](http://sf.snu.ac.kr/sunghwan.lee/)(@Sung-HwanLee)
    + Email address: swpp@sf.snu.ac.kr. 
        * In the case of sending TA an email, specify sender's name and student ID.  
    + Place: Bldg 302 Rm 312-2 

## Announcements 

- Mar. 17: To build LLVM, please follow [BuildLLVM.md](BuildLLVM.md). If it doesn't work due to insufficient memory / free space, please contact TA to request a laptop for a class. EDIT: please use this form to request a laptop: https://forms.gle/jDV6K4sD61WEZKh99 *until: Mar. 25 Wed*

## Projects

- Apr. 13: Check the [issue](https://github.com/snu-sf-class/swpp202001/issues/3) for making up project teams.

- Apr. 19: On Apr. 28, you're going to have an idea presentation session.
Each team should come up with an optimization that will be helpful for the project.
Each team will have a presentation for 3 minutes and get feedback for 2 minutes.
For the specification of backend assembly as well as the restrictions on the
input programs, see [project/spec.pdf](project/spec.pdf).

- Apr. 20: To ask questions about the assembly & source programs, please use [issue #6](https://github.com/snu-sf-class/swpp202001/issues/6) and [#7](https://github.com/snu-sf-class/swpp202001/issues/7).

## Assignments

- Mar. 19: Assignment 1 is announced. See here: https://github.com/aqjune/swpp202001-assn1

If you cannot compile word.cpp, please check whether your `g++` supports c++17. `g++ -version` should print version 7 or upper.

- Mar. 27: Assignment 2 is announced. Deadline is Apr. 1, midnight.
See here: https://github.com/snu-sf-class/swpp202001/tree/master/practice/2.assn

NOTE: The goal of assignment 2 is to write a simple function using IR by your own.
Please don't simply create .ll file using `clang -emit-llvm ..` and submit it.
Such .ll file has idioms/variable namings that are generated by compiler optimizations, such as a zero-extended induction variable (variable `i` in `for (i=0; ..)`).

- Apr. 3: Assignment 3 is announced. Deadline is Apr. 12, midnight.

NOTE: The `Failed to load passes from ...` error at `3.materials/run-passes.sh` was fixed.
Special thanks to Woosung Song.

NOTE 2: N in `polygon` is not larger than 100. input5.txt's answer was incorrect and fixed (thanks to Jeyeon Si). Block names in `unreachable`'s inputs are always lower-case alphabets.

- Apr. 14: Assignment 4 is announced. Deadline is Apr. 21, midnight. Late penalty is 10% per day.

NOTE: `fillundef.cpp` had bugs regarding the type of undef value / the way how
uses are iterated. Now fixed.

NOTE 2: Added [FAQ.md](practice/4.assn/FAQ.md) (Updated: Apr. 20).

NOTE 3: If you compiled LLVM with release and seeing `This analysis pass was not registered prior to being queried` error, please use this code to get DominatorTree:

```
DominatorTree DT(F);
```

NOTE 4: *IMPORTANT: We have one more constraint to guarantee that there is only one
possible output. Please see the updated README.md of assignment 4.*
