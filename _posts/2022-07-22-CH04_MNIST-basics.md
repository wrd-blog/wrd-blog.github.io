# Chapter 04_mnist_basics
Well, the intro to this chapter didn't lie when it claimed that this would be
the most difficult chapter. It presents a lot of technical jargon, concepts,
tricks and Fast.ai API instruction; more than my aging brain was able to absorb
on one pass through it.

I was able to make my way through all the material and understand it after repeating
the reading of some of the sections several time and practicing coding them in
my own notebook.

At the end of the chapter is a list of questions which were not too difficult
to answer, sometimes with a bit of scrolling back into the notebook to research
something that didn't stick in my memory the first time through. I higly recommend
answering all of the questions at the end of each notebook and attempting to 
complete some or all of the suggested learning projects. It was amazing to me how
much I had forgotten as I attempted to answer the questions.

In order to be sure I understand all the steps required to create a Pytorch database,
set up the NN and train it, I decided to attempt to rewrite the lesson code in
my sandbox notebook in order to create and train a NN that could recognize all 9
of the handwritten digits in the full MNIST database.

My first discovery was that the MNIST database as downloaded requires considerable
massaging with Python to put it into a form that Pytorch/Fastai can consume.
Fortunately, the people at fast.ai have already done the database reconstruction
and made it available on their website. 

#### July 24 2022
I have finally worked my way through this brain-smoker of a chapter and understand
most of it. 
To test my knowledge, I created a jupyter notebook containing my attempt at creating
and training a NN (resnet18) that is capable of recognizing images of hand-written
numbers. The training database I used came with fastai when I installed it. Taking a
clue from the 04_mnist_basics notebook, I borrowed the learner from the "Going Deeper"
section of the course notebook:

learn = vision_learner(dls, resnet18, pretrained=False,
        loss_func=CrossEntropyLossFlat(), metrics=accuracy).
        
I had a bit of trouble with inference until I changed the loss_function from F.Cross_entropy
to CrossEntropyLossFlat() as suggested on a Stackoverflow.com page.
I was then able to train and export the model then reload the trained model and do
some inference testing which worked great.

Now, on to the next chapter of the book to learn something more about this fascinating
subject.

WrD
