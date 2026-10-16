{
"title": "[Internship] Test Suite Analyses",
"layout": "blogpost",
"publishDate": "2026-10-15"
}

## Context

Tests are code too and as such they exhibit specific problems. Several approaches propose test smells. The work we did in the past is a good start  [See Test Quality Assessment](https://rmod-files.lille.inria.fr/Team/Texts/Papers/Reic07aTestQualityAssessment.pdf) or [Rotten Green Tests] (https://rmod-files.lille.inria.fr/Team/Texts/Papers/Delp19a-RottenGreenTests-ICSE2019-v2.pdf).




## Objectives

Now tests are often structured in test suites and we need to have better way to assess the quaity of the suite as a whole. 

We would like to have a linter for test suite. 
Here are some criterias to provide feedback on the suite:
- is the suite cohesive in the sense of fixture use
- is the suite cohesive in the sense of references to external classes, e.g

## Tasks 

The intern will:

- Read the Test Quality Assessment paper and master of the first author
- Read the Rotten Green Test paper
- Study the implementation of Rotten Green Test as available in Pharo
- Study the implementation of https://github.com/Ducasse/pharo-test-analysis and in particular the Smell Detector package and its tests
- Implement a simple TEST smell in Smell Detector
- Study ClapDbgBasicCommandsTest in Pharo 14 as an example of a suite that could be reorganized
- Define a Suite detector that reports information about Suite. 
-- number of assertion/testcase
-- whether it is defining the same fixture multiple times without having a setUp method
-- cancelling and redefining the test fixture
-- whether the test methods use different groups of external project


## Refs


- Rule-based Assessment of Test Quality, S. Reichhart,T. Gırba, and S. Ducasse. https://rmod-files.lille.inria.fr/Team/Texts/Papers/Reic07aTestQualityAssessment.pdf
- Rotten Green Tests https://rmod-files.lille.inria.fr/Team/Texts/Papers/Delp19a-RottenGreenTests-ICSE2019-v2.pdf
## For the students

Interns should:
- learn fast, for example https://pharo.org
- open minded
- working in an international settings

Student benefits: 
- work on a hot topic
- be immersed in a core language
- learn deep object-oriented design skills 

