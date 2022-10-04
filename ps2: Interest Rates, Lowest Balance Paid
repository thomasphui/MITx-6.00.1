#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Created on Fri Jun 17 22:37:34 2022

@author: thomashui1997
"""


balance = 320000
annualInterestRate = 0.2

monthlyInterestRate = annualInterestRate / 12
monthlyLowBound = balance / 12
monthlyUppBound = (balance * (1 + monthlyInterestRate)**12)/12.0

epsilon = 0.01
originalBal = balance

while abs(balance) > epsilon:
    monthlyPaymentRate = (monthlyUppBound + monthlyLowBound)/2   
    balance = originalBal
    
    for month in range(12):
        monUnpaidBal = balance - monthlyPaymentRate
        interest = monUnpaidBal * monthlyInterestRate
        balance = monUnpaidBal + interest
    if balance > epsilon:
        monthlyLowBound = monthlyPaymentRate
    elif balance < -epsilon:
        monthlyUppBound = monthlyPaymentRate 
    else:
        break

print("Lowest payment: " + str(round(monthlyPaymentRate,2)))
        


'''
balance = 3329
annualInterestRate = 0.2

monthlyIntRate = annualInterestRate / 12.0
monthlyInterestRate = annualInterestRate / 12

originalBal = balance

lowestPayment = 0
while lowestPayment <= balance:
    lowestPayment = lowestPayment + 10
    month = 0
    while month < 12:
        month = month + 1
        monUnpaidBal = balance - lowestPayment
        balance = monUnpaidBal + monthlyInterestRate * monUnpaidBal
    if balance >= 0:
        balance = originalBal

print("Lowest Payment: " + str(lowestPayment))
'''

balance = 42.00
annualInterestRate = 0.2
monthlyPaymentRate = 0.04

month = 1

monthlyInterestRate = annualInterestRate / 12
minMonthlyPayment = monthlyPaymentRate

while month <= 12:
    month = month + 1
    minMonthlyPayment = monthlyPaymentRate * balance
    monUnpaidBal = balance - minMonthlyPayment
    balance = monUnpaidBal + monthlyInterestRate * monUnpaidBal

print("Remaining balance: " + str(round(balance,2)))
'''
