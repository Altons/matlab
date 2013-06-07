LIBSVM for Octave (Mac OSX Lion)
=




I wasted a terrible amount of time trying to compile LIBSVM for Octave (Octave.app bundle) on my Macbook pro. Luckily I manage to create VM with Lion and install Octave using homebrew. After that compiling LIBSVM was quick and easy.

Although I could have done the same on my MBP I did not want to mess up my Octave installation so I created a github repo and just cloned it up.

Just add

addpath('../yourpath/matlab');

to your ~/.octaverc file and you should be ready to go.

Example
=

I have added sample data from Prof. Andrew Ng to test LIBSVM.