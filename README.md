# Production Optimization

## Overview

This project implements a Linear Programming (LP) model to maximize the daily profit toy production during the Christmas season. The optimization problem considers individual toy production constraints, an overall daily production limit, and special packages that yield higher profits than the sum of their individual components.

The solution is developed in Python using the **PuLP** library to formulate and solve the LP problem.

## Problem Statement

UbiquityInc produces `t` types of wooden toys, each with a specific profit and production limit. Additionally, `p` special packages containing three distinct toys can be sold for a higher combined profit. The company faces the following constraints:

1. Each toy type has a maximum production capacity.
2. The total number of toys produced daily cannot exceed a given limit.
3. Special packages can only be sold if all three toys in the package are produced.

The goal is to determine the maximum possible daily profit.

## Input Format

The input file provides the following information:

1. The first line contains three integers:
   - `t` – Number of distinct toy types (`t ≥ 1`)
   - `p` – Number of special packages (`p ≥ 0`)
   - `max` – Maximum number of toys that can be produced daily

2. The next `t` lines contain two integers each:
   - `li` – Profit per unit of toy `i`
   - `ci` – Maximum daily production capacity of toy `i`

3. The following `p` lines contain four integers each:
   - `i`, `j`, `k` – The three toy types in the special package
   - `lijk` – Profit of the special package `{i, j, k}`

All integers in the input file are separated by exactly one space.

## Output Format

The program outputs a single integer:  
- The maximum daily profit that can be achieved.

## Dependencies
- PuLP library

## Installation

To install PuLP, run:

```sh
pip install pulp
