LIBSVM for Octave (Mac OSX Lion)
=




I wasted a terrible amount of time trying to compile LIBSVM for Octave (Octave.app bundle) on my Macbook pro. Luckily I manage to create VM with Lion and install Octave using homebrew. After that compiling LIBSVM was quick and easy.

Although I could have done the same on my MBP I did not want to mess up my Octave installation so I created a github repo and just cloned it up.

Just add

addpath('../yourpath/matlab');

to your ~/.octaverc file and you should be ready to go.

Example
=

I have added sample data from Prof. Andrew Ng to test LIBSVM. Goto the matlab/ folder open octave and run the following code:

```matlab
>> [trainlabels, trainfeatures] = libsvmread('twofeature.txt');
>> model = svmtrain(trainlabels, trainfeatures, '-s 0 -t 0 -c 1');
```

if no complains then you are ready to use LIBSVM

##UPDATE:

The compiled library failed to run using Octave.app (3.4.2) as the one in homebrew is 3.6.4 and diff architecture.

If you want to install octave using homebrew following instructions on this link

http://wiki.octave.org/Octave_for_MacOS_X
