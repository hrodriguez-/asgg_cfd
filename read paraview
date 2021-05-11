"""Provides a scripting component.
    Inputs:
        x: The x script variable
        y: The y script variable
    Output:
        a: The a output variable"""

__author__ = "HiramRodriguez"
__version__ = "2021.04.23"

import rhinoscriptsyntax as rs
import os
import csv
import itertools
import System
import StringIO
import math
import clr


# for accesssing GH classes
clr.AddReference("Grasshopper")
from Grasshopper.Kernel.Data import GH_Path
from Grasshopper import DataTree
from System import Object


from glob import glob
from os import walk
from csv import reader


path = Directory
ext = "*.csv"
all_csv_file=[file for path,subdir, files in os.walk(Directory) for file in glob(os.path.join(path,ext))]
Name=all_csv_file[FileNumber]

#print(a)

newlist =[]
newlist2 =[]
newlist3 =[]

#skip first line for example the header
#this is exporting Point Location 
with open(Name,'r') as read_obj:
    csv_reader= reader(read_obj)
    Pts = next(csv_reader)
    #check file as empty 
    if Pts !=None:
        for row in csv_reader:
                   data1=(',').join([row[2],row[3],row[4]])
                   newlist.append(data1)
                   Point=newlist
                   #print(data1)
                   
#this is exporting Vector Direction
with open(Name,'r') as read_obj:
    csv_reader= reader(read_obj)
    Vector = next(csv_reader)
    #check file as empty 
    if Vector !=None:
        for row in csv_reader:
                   data2=(',').join([row[5],row[6],row[7]])
                   newlist2.append(data2)
                   Vector=newlist2
                   print(data2)
                   
#this is exporting Vector Mag
with open(Name,'r') as read_obj:
    csv_reader= reader(read_obj)
    VectorMag = next(csv_reader)
    #check file as empty 
    if VectorMag !=None:
        for row in csv_reader:
                   data3=(row[8])
                   newlist3.append(data3)
                   Magnitude=newlist3
                   #print(data3)
        
            

