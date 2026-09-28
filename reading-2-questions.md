---
---
# Reading 2 — Discussion Questions

Questions for the Mon, Sep 28 discussion of MACE, MACE-MP-0, and Creed et al.  Most of these came out of your Gradescope comments.

Pick **one** per group, discuss for 25 minutes, then one person reports out. Aim for a 2 minute presentation. You will get 3 min max.

Put your group's answer on your group's slide in the
**[shared slide deck](https://docs.google.com/presentation/d/13krKlPiC_ex9x_mJVcTfGnUcLGzx3mOwjyIGqwILwt8/edit?usp=sharing)** —
everyone can edit. Write down your question number, get your answer written, and choose a presenter by minute 25.

## 1. List out and rank the main limitations of MLIPs.

## 2. Where are the gaps in MLIP evaluation? Come up with a wishlist for how MLIP evaluation should be done.

## 3. How can a user figure out whether to trust an MLIP in their application? For what kinds of applications are MLIPs useful vs. not useful?

**Report out:** your checklist, and where you draw the useful / not-useful line.

## 4. Suppose someone gave you a budget to spend on doing DFT at new atomic configurations to support MLIP training. Which configurations would you run?

## 5. An MLIP, mid-simulation, meets a configuration unlike anything in its training data. What should it do?

You can treat this as a research proposal for a new algorithm. Or as a way to
create an MLIP that is more trustworthy. 

## 6. Suppose you know how to run an MLIP to predict some macroscopic phenomenon, like crystal structures. Can this be used in training?

For example, you can predict crystal structure by placing atoms into a repeating structure and then
moving them to minimize their energy. Suppose you also have experimental data on the observed
macroscopic phenomenon in nature --- e.g., the actual locations of the atoms in a crystal structure.
**How could you include this data into your MLIP training, and what value would it have?**

**Report out:** your training scheme, and the observable you would start with.

## 7. MACE's central design choice is four-body messages. Is four the right number, and does the answer depend on the system?

## 8. Do you believe that it is possible to train a foundation model that is universal to a full range of chemistry?

- What would have to be true about **out-of-distribution extrapolation** for that to work?
- What limitations would need to be overcome to get there?
