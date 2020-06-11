# ml-project-scoping-talk

Notes still in a draft state.

## Why Project Scoping is a Hard Problem

* Obersvation 1: Well-defined performance curve. Two stages: early development and optimization.
* Another view: superlinear growth of cost with performance benchmarks.
* Observation 2: difficulty of forecasting.
* Introduce and discuss CACE principle.
* Kaggle's experience: some problems are easy, some problems are hard, here are the competition curves demonstrating that even experienced organizers don't get it right.
* Conclusion: machine learning project scoping is a hard problem, one that's not discussed nearly often enough.

## Some Suggested Techniques

* Tip 1: Separate the project into exploratory phase and an implementation phase. Use the exploratory phase to estimate the time cost of the project.
  * TODO Quote from https://www.ethanrosenthal.com/2020/01/08/freelance-ds-consulting/

* Tip 2: Benchmark human and model performance on the task.
  * It’s important that this be model performance on your dataset, not on some academic benchmark dataset. Remember the CACE principle: it’s dangerous to assume that performance on a benchmark is commutative to your specific project.
  * Go to paperswithcode, which is pretty much the premier model-sharing platform in the community, grab some off-the-shelf models, and throw them at the problem.
  * If you aren’t aware of them, or haven’t been there recently, they recently had a big update, check it out.
  * TODO raid https://karpathy.github.io/2014/09/02/what-i-learned-from-competing-against-a-convnet-on-imagenet/ for notes.

* Tip 3: Get performance breakpoints
  * What is "good enough"? What is "great"?
  * This is typically a business decision.
  * These breakpoints are natural stopping points for the project. When you reach a performance breakpoint, you should take a moment to assess how much additional work you think it would take to reach the next level.
  * If the answer is “a lot”, instead of burying time investigating more tricky network or data augmentations you should just finalize your current model (clean up your code, run a hyperparameter search job to finalize your weights, etcetera) and move on to a different project.

* Tip 4: Cost estimate updates
  * Your estimate of time cost will greatly improve over the course of the project.
  * Businesspeople don’t like uncertainty, so communicating these updated timestamps as the project proceeds helps ameliorate risk and align the other processes surrounding model development (for example, making sure that your data engineers will have the time budget to productionize the model once it’s ready, and won’t be stuck in other things).

* Tip 5: Well-optimized model zoo
  * Having a variety of models already on hand serious speeds up the early stage of development, allowing you to get to the lower-level optimizations faster.
  * TODO: Tell the story of Vladimir Iglovikov, the Kaggle GM that kick-started his career with papers written using models he’d refined (and refined his understanding of) over the course of competing on Kaggle: https://drive.google.com/drive/u/1/folders/1Vnvq2FZkSn_F9x3btRmhuJvKab4v2VQn.
