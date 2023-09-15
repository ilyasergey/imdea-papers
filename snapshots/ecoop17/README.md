# ECOOP 2017 submission #

Submission info:

* ** LIPICS 25 pages + references + appendices. **
* ** Lightweight Double-Blind submission. **
* ** Artifacts: ** submitted through tar-file, could be a link to a website but has to be given in this optional materials tarfile. The artifact and/or extended appendices needen't be annonymized.

# Deadlines: #

 * Abstracts due : 7 January 2017 23.59h AOE.
 * Papers due: 13 January 2017 23.59h AOE.
 * Rebuttal : 20-22 March 2017.
 * Author notification: 12 April 2017.
 * Camera-ready versions: 19 April 2017.
 
 [NB:] The submission website list the following, slightly more precise info:
 
 * **Registration deadline:** 
 8 Jan 2017 6:59:59am EST (Sunday 8 Jan 2017 12:59:59 CEST).
* **Submission deadline:** 
* 14 Jan 2017 6:59:59am EST (Saturday 14 Jan 2017 12:59:59pm CEST).

# Optional Letter To Reviewers

ECOOP suggest submitting a letter to the reviewers indetifying the venues of previous submissions, a detail of the reviews and how the changes were addressed.


# Plan

1. ~~Annonymize submission~~.
1. Incorporate a paragraph about {\it Khyza et. al.} to the related work.
2. ~~Incorporate comments from the reviewers!!.
3. Add a paragraph, or a full section, about how to relate our specs to linearizability.
4. Add a paragraph about the generality of the method.

# Reviewer Commments

### TO DO List ###

~~1. Fix typos and errors from  ETAPS reviews.~~

    1. ~~Page:4  "(...) linearizability only permits reordering of non-overlapping operations. (...)" Here ```non-overlapping``` should be ```overlapping```.~~
    
    3. ~~Page 5, "the decision on the logical order of this write depends on
the execution of scan in a different thread, and only after the
execution of write has terminated". I think the decision is made only after the scan has executed line 15/16 in Fig 1. It *may* be made after the write terminates, but I guess we cannot say that it is made "only" after the write terminates.~~ [GAD] Fair enough. 

    2. ~~"Invariants 4 and 6: do the orders of the regular expressions follow
sigma?" [GAD] Yes! Maybe we should clarify. We haven't adressed this question
in the rebuttal.~~

    2. ~~Fig 6, ```setS``` should be ```set```.~~
		
	3. ~~Invariant 8:```W_p = Fwd t v \/ Done t v``` should be ```W_p = Fwd t v \/ W_p = Done t v```~~.
    
    4. ~~Page 21, "The concurrent write may change the color of s to
yellow, by invoking forward". Here "yellow" should be "green".~~

    6. ~~Invariant 5: Actually, the invariant is also valid through lines 15--16, so we should correct the statement to say "through lines 13--16".~~

	7. ~~Related work: Fix references to Vafeiadis' phD theis and TaDa.~~
	
    8. ~~R2Q1. Why there is only one candidate for relink.~~

2. Discussion Section

3. Related Work


 
# Coq Implementation: 

** Work on finishing the third model (with a proper, transitive, \omega) as well. If there is time, change the formal sections and the proof of scan to refer to the new implementation. **
