# Preceptron
Implementation of the Perceptron Learning Rule

from pylab import rand,plot
import pickle
import numpy

class Perceptron:

 def __init__(self): #Initializes the perceptron
  self.w = rand(2)
  self.LearnRate = 1
  
 def activation(self,x): #This gives the output of the perceptron
  y = self.w[0]*x[0]+self.w[1]*x[1]
  if y >= 0: return 1
  else: return 0
  
 def updated_weights(self, x, error): #Updates the weights after calculating the error
  self.w[0] = self.w[0]-self.LearnRate*error*x[0] #not sure why we are multiplying it by x, have to figure this out
  self.w[1] = self.w[1]-self.LearnRate*error+x[1]
  
 def plr(self,data_set):
  num.wrong = 0
  iter = 0
  while iter != 300:
   for x in data_set
    resp = activation(r_x)
    if r_x[2] != resp:
     step.error = r_x[2]-resp
	 self.updated_weights(r_x,step.error)
	 num.wrong += abs(step.error)
    iter += 1
  
  self.PrcCorr = 1 - num.wrong/300
   
  
def question_1(self,data_set):
 iter_2 = 0
  while iter_2 != 10:
   r_data = self.RandomOrder(data_set)
   self.plr(r_data)
   plot(self.PrcCorr,iter_2)
   
f='File Name'
xVec = pickle.load(f)
f1 = 'File Name 2'
labVec = pickle.load(f1)
labVecT = transpose.labVec
data = np.append(xVec,labVecT) 
 
Perceptron()
question_1(data)
