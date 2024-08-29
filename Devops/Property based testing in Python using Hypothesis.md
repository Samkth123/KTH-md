
When we think of our usual unit tests, we could classify them as example-based. We already compute the output in some way for the given input(s) and that forms our test’s main assertion.

But our example inputs are usually a very small subset of the entire set of possible inputs. This raises the question – are we really confident about our program? Have we really exhausted all possibilities and edge cases? Property-based testing gives us an approach to increase that confidence — we will define a sort of rule (an invariant or property) and generate a large number of valid inputs. Our test will then verify if our properties hold true for each input.

En **==_invariant_==** är inom bland annat matematiken och informationstekniken en egenskap som inte förändras med avseende på någon avbildning.

It works by generating arbitrary data matching your specification and checking that your guarantee still holds in that case. If it finds an example where it doesn’t, it takes that example and cuts it down to size, simplifying it until it finds a much smaller example that still causes the problem. It then saves that example for later, so that once it has found a problem with your code it will not forget it in the future.


Writing tests of this form usually consists of deciding on guarantees that your code should make - properties that should always hold true, regardless of what the world throws at you. Examples of such guarantees might be:

- Your code shouldn’t throw an exception, or should only throw a particular type of exception (this works particularly well if you have a lot of internal assertions).
    
- If you delete an object, it is no longer visible.
    
- If you serialize and then deserialize a value, then you get the same value back.