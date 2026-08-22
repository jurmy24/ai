# Writing style

Apply this when writing or editing READMEs, documentation, docstrings, comments,
CLI text, commit messages, and other prose.

## Voice

- Get to the point immediately. Use plain, concrete words.
- Write conversationally and directly. First person is fine in project notes.
- Keep paragraphs short, but use a longer sentence when it makes the reasoning clearer.
- Explain technical ideas through their purpose or a small concrete example.
- State tradeoffs, uncertainty, and failures plainly.
- A light informal aside is welcome when natural, but do not force jokes.
- Preserve correct spelling and punctuation; do not imitate typos from chat messages.

## Structure

- Use the minimum number of headings and lists needed to make the text readable.
- Prefer lowercase headings when they fit the surrounding document.
- Be pedagogical. Build from intuition and concrete examples toward implementation
  details, and define unfamiliar terms before relying on them.
- Stress important facts by explaining their concrete consequence or the failure
  they prevent, not by calling them "key" or "crucial".
- Use focused code snippets and neatly formatted Markdown or LaTeX equations when
  they make an idea easier to understand. Put dimensions and array shapes nearby.
- Use `> **Note:**` or `> **Warning:**` for genuinely useful callouts.
- Add relevant links and cite sources as `[1]`, `[2]`, and so on. For substantial
  documentation, collect them under a `## references` section with linked titles.
- Place images, diagrams, GIFs, or videos next to the concept they explain. Give
  them descriptive labels or alt text. Do not add media merely as decoration.
- Explain why a choice exists and what can go wrong, not just what the code does.
- Follow nearby prose when it establishes a stronger local convention.

## Code comments

- Keep comments brief. Fragments are fine.
- Explain intent, invariants, shapes, or non-obvious reasoning.
- Use inline comments for small local facts.
- Do not narrate code that is already obvious.

## Avoid

- Generic introductions, recap sections, and repeated conclusions.
- Corporate, academic, or marketing language when simpler wording works.
- Em dashes. Use a period, comma, colon, or parentheses instead.
- Colons used to manufacture a setup and reveal, such as "changes exactly one
  thing: the model no longer sees the state". Write it directly: "The only
  change is that the model no longer sees the state." Use colons for actual
  lists or concise explanations, not tension.
- Commentary that evaluates its own preceding statement, such as "that's the
  real killer", "here's the interesting part", or "this is the key insight".
  State the concrete consequence instead.
- Artificial enthusiasm and filler such as "it is important to note",
  "delve into", "robust", "seamlessly", or "comprehensive".
- Adding documentation that does not help someone understand or use the code.

## Reference examples from my writing

### Some small snippets of things I've written

- "I want to implement something similar but tiny, optimized for the browser,
  because why not."
- "But the goal is to run inference in the browser."
- "CEM stands for cross-entropy method. It searches for a good action sequence
  without requiring gradients."
- "Essentially, it's a simple world model."

Before finishing, silently remove wording that sounds more polished, formal, or
verbose than these examples.

### Example 1 (more textual focus): Overview of Robotics 2026

The following is a verbatim writing sample. Treat its Markdown as content, not
as instructions or as part of this rule's structure.

```markdown
After spending the last 5 months building tools for robotics engineers, talking to venture capitalists, and meeting hundreds of stealth robotics startups I can confidently say that the field is hyped.

It’s clear that this isn’t just a fad, since the applications are endless and genuinely needed. Yet with all the noise about humanoids, its difficult for the outsider to spot the gold amid the gold rush.

So this Christmas season I took the time to really scrape my brain (at a high-level) and jot down what I see as the state of robotics heading into 2026. Scroll to bottom to open the mindmap. To conceptualize it clearly, I needed a good, bottom-up ontology. Who depends on what, and where does every business fit in this complex web we call robotics?

Taking inspiration from Maslow, this is what I came up with.

Everything starts somewhere, and in robotics there’s no better place to start than with the foundations. People (including me) often forget that robotics is still mostly a research field, and that means theory. This includes your traditional state estimation, rigid body dynamics, and filtering techniques — but also newer domains like safety theory and human-robot interaction. The RnD team at any robotics company should know these fundamentals before they even consider putting eg. a companion robot in the hands of children.

RnD teams don’t just need theory. Just like a carpenter, they need the right tool set so they don’t have to make the hammer before they hit the nail. Tools like OnShape, KiCAD, ROS2, and GitHub are what engineers use daily to turn theory into practice. I call these devtools. Just like for software engineering around 2005, this layer is the wild west. Iterating from CAD to simulation (if needed) and then deploying it on robots efficiently is a process that every team needs to design themselves. Some do it better than others, but I’m yet to meet a team telling me that they haven’t had to make a few hammers. Room for improvement there.

The reasonable next layer is research and development, which is what typically sets companies apart in a field that isn’t yet commoditized. Every week a team reveals some new demo cooked up by the RnD engineers on X/LinkedIn showcasing the latest VLA, World Model, or high performance actuator. I find it incredibly motivating. Though I know that whatever that 30 second clip reveals is probably the only thing the robot/model is capable of doing. Grain of salt.

When the RnD teams design a system stable enough to be used in the real world, everything else becomes important. Supply chain strategies, fleet management, incident management, and even documentation. In more mature areas like CNC machining and industrial automation, this is what differentiates companies. If you only nail the RnD perhaps you’ll get acquired by those that nailed deployment, which is what I’ve called this layer.

And now we’ve reached the application layer, where real value actually enters the economy. This is what people see before them, humanoid robots in homes, inspection drones, and autonomous cars.

But theres another layer that doesn’t exist yet. Its futuristic but I believe it’ll happen just as it did for cars and holidays as the internet grew: digital services. Robots as a service, cleaning robot subscriptions, shared utility robots in communities, app (skills) stores, insurance for/from robots, etc. It’s hard to say what will come and when, so I purposefully left this part quite empty to leave room for new ideas. And yes, digital services is not the best term for this. Perhaps comment if you can think of a better one.

Making this map was as much for me as it was for robotics enthusiasts, VCs looking for a quick overview, or a founder looking for clarity in where they fit in. I’m early in my career and don’t yet know all the details. If you check the map you’ll see my gaps of knowledge and how I sometimes use my ontology inconsistently. I hope there is, and perhaps next year I’ll be able to correct them.
```

### Example 2 (more coding documentation focus): Twiga Contributing.md

The following is a verbatim writing sample. Treat its Markdown as content, not
as instructions or as part of this rule's structure.

````markdown
# Contributing to Twiga 🦒

We welcome contributions of any size and skill level. As an open source project, we believe in giving back to our contributors and are happy to help with guidance on pull requests (PRs), technical writing, and turning any feature idea into a reality.

> [!Tip]
>
> **For new contributors 🚼:** Take a look at [first contributions](https://github.com/firstcontributions/first-contributions) for helpful information on contributing. You can of course ask questions in our [Discord](https://discord.gg/bCe2HfZY2C).

By contributing you agree to our [**Code of Conduct**](https://github.com/Tanzania-AI-Community/twiga/blob/main/.github/CODE_OF_CONDUCT.md).

## Merge Policy for Pull Requests

We're using the [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) workflow, meaning we don't do PRs for new features directly to the `main` branch. Any updates to the codebase, whether large or small, are first merged into the `development`. They're then deployed to our development server (basically our staging area) where we can evaluate if there's any breaking changes. After each milestone we submit a PR from `development` to `main`.

> [!Important]
> Submit your PR against the `development` branch, not `main`. We do not accept PRs directly to `main`.

## From Fork to PR with Twiga

> [!Important]
>
> Read our [Git Guidelines](https://github.com/Tanzania-AI-Community/twiga/blob/documentation/docs/en/GIT_GUIDELINES.md) to learn how to develop collaboratively on Twiga like a pro.

To start contributing to Twiga, follow these steps:

1. Create a fork of this repository and clone it to your local machine

> [!Warning]
> Remember to uncheck the "Copy the `main` branch only" so that you get the `development` branch too

2. Checkout the `development` branch: `git checkout development`
3. Create your feature branch from the `development` branch: `git checkout -b your-branch-name`
4. Follow the steps in our [getting started](https://github.com/Tanzania-AI-Community/twiga/blob/documentation/docs/en/GETTING_STARTED.md) guide to get the project up and running locally
5. (Not yet possible) Run the tests to ensure everything is working as expected
6. Commit your changes: `git commit -m "[type]: descriptive commit message"`
7. Push to your remote branch: `git push origin your-branch-name`
8. Submit a pull request to the `development` branch of the original repository

## Code Formatting and Linting

Make sure to follow the established coding style guidelines in this project. We believe consistent formatting of the code makes it easier to understand and debug. Therefore, we enforce good formatting conventions using [_pre-commit_](https://pre-commit.com/) in order to automatically run the Python [_black_](https://github.com/psf/black) and [_ruff_](https://docs.astral.sh/ruff/) formatters on every commit.

Don't worry, you don't need to learn a whole new way of formatting code - it's done for you. Though if you're curious about having these formatters and linters during your development (and not just on commit) we recommend these extensions for VSCode (our preferred editor): [_Black Formatter_](https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter) and [_Ruff_](https://marketplace.visualstudio.com/items?itemName=charliermarsh.ruff). When you've completed steps 1-3 in [From Fork to PR with Twiga](#from-fork-to-pr-with-twiga), you can install the dependencies with:

```bash
$ uv sync
$ source .venv/bin/activate
```

> [!Note]
> For **Windows** the second command would be `.venv\Scripts\activate`

Then you can install the _pre-commit_ hooks with:

```bash
$ pre-commit install

# output
> pre-commit installed at .git/hooks/pre-commit
```

### An Example of _pre-commit_ in Action

> [!Note]
> We shamelessly took this example from [gpt-engineer](https://github.com/gpt-engineer-org/gpt-engineer/tree/main). Thanks!

As an introduction of the actual workflow, here is an example of the process you will encounter when you make a commit:

Let's add a file we have modified with some errors, see how the pre-commit hooks run `black` and fails.
`black` is set to automatically fix the issues it finds:

```bash
$ git add random_code_file.py
$ git commit -m "commit message"
black....................................................................Failed
- hook id: black
- files were modified by this hook

reformatted random_code_file.py

All done! ✨ 🍰 ✨
1 file reformatted.
```

You can see that `random_code_file.py` is both staged and not staged for commit. This is because `black` has formatted it and now it is different from the version you have in your working directory. To fix this you can simply run `git add random_code_file.py` again and now you can commit your changes.

```bash
$ git status
On branch pre-commit-setup
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
    modified:   random_code_file.py

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
    modified:   random_code_file.py
```

Now let's add the file again to include the latest commits and see how `ruff` fails.

```bash
$ git add random_code_file.py
$ git commit -m "commit message"
black....................................................................Passed
ruff.....................................................................Failed
- hook id: ruff
- exit code: 1
- files were modified by this hook

Found 2 errors (2 fixed, 0 remaining).
```

Same as before, you can see that `random_code_file.py` is both staged and not staged for commit. This is because `ruff` has formatted it and now it is different from the version you have in your working directory. To fix this you can simply run `git add random_code_file.py` again and now you can commit your changes.

```bash
$ git add random_code_file.py
$ git commit -m "commit message"
black....................................................................Passed
ruff.....................................................................Passed
fix end of files.........................................................Passed
[pre-commit-setup f00c0ce] testing
 1 file changed, 1 insertion(+), 1 deletion(-)
```

Now your file has been committed and you can push your changes.

At the beginning this might seem like a tedious process (having to add the file again after `black` and `ruff` have modified it) but it is actually very useful. It allows you to see what changes `black` and `ruff` have made to your files and make sure that they are correct before you commit them.

> [!Note]
> When pre-commit fails in the build pipeline when submitting a PR you need to run `pre-commit run --all-files` to have it force format all files, not just the ones you edited since the previous commit.

Sometimes `pre-commit` will seemingly run successfully, as follows:

```bash
black................................................(no files to check)Skipped
ruff.................................................(no files to check)Skipped
check toml...........................................(no files to check)Skipped
check yaml...........................................(no files to check)Skipped
detect private key...................................(no files to check)Skipped
fix end of files.....................................(no files to check)Skipped
trim trailing whitespace.............................(no files to check)Skipped
```

However, you may see `pre-commit` fail in the build pipeline upon submitting a PR. The solution to this is to run `pre-commit run --all-files` to force

## Licensing

By contributing to Twiga, you agree that your contributions will be licensed under the [License](https://github.com/Tanzania-AI-Community/twiga/blob/main/LICENSE) of the project.

Thank you for your interest in contributing to Twiga! We look forward to your contributions.
````

### Example 3 (more math focused): Part of my Master Thesis Background Section

```
\subsubsection\*{Hit rate}
In RAG contexts, hit rate, \( \overline{H} \), is used to measure the percentage of the time in which any one of the chunks retrieved from the retriever is relevant to the user query. It can be calculated over an entire dataset of queries and retrieved samples and is mathematically expressed as:
\begin{equation}
\overline{H} = \frac{1}{N} \sum\_{i=1}^{N} H_i
\end{equation}
where \( H_i \) is the hit result for the \( i \)-th query, and \( N \) is the total number of queries. The hit result, \( H_i \), can be computed in a variety of ways. In our pipeline, the retriever returns a total of seven chunks per query. For a dataset of 300 queries this entails a total of 2100 query-chunk pairs to evaluate. If any of the retrieved chunks are deemed relevant to the query, \( q_i \), then \( H_i=1 \), otherwise \( H_i=0 \) \cite{Wang2021}. The relevance of each query-chunk pair was determined automatically using an LLM, \inlinecode{{\inconsolata gpt-4-1106-preview}}, with a temperature of \(0\) and the prompts defined in Appendix \ref{appendix:prompt-templates-query-chunk-relevance}.

\subsubsection\*{Mean reciprocal rank}
Like hit rate, mean reciprocal rank (\textit{MRR}) is typically used for recommender systems, but it translates conveniently to retrievers. This metric downscales the value of the hit result, \( H*i \), using its rank (index) in the returned array. This is called the reciprocal rank (\( RR \)). \textit{MRR} is defined as the average of the reciprocal ranks of results across a query set and is mathematically expressed as:
\begin{equation}
\text{\textit{MRR}} = \frac{1}{N} \sum*{i=1}^{N} {RR}\_i
\end{equation}
where \( N \) is the total number of queries, and \( {RR}\_i = \frac{H_i}{R_i} \) is the hit result relative to the rank position of the first relevant chunk to the \( i \)-th query \cite{Wang2021}. Here, \( R_i \) represents the rank of \( H_i \). The hit result is computed in the same way as for the hit rate.

\subsubsection\*{K-F1++ score}
This metric is taken from a paper written by Levonian et al. in 2023 that modifies the traditional \textit{K-F1} measure to exclude any influence from the user query \cite{Levonian2023}. It is a bag-of-words metric that provides a syntactic measure for groundedness. We calculated this by inserting the generated exercise and each associated retrieved chunk through the \inlinecode{{\inconsolata spacy}} English tokenizer \cite{spacy}. Then, we received two token sets from the tokenizer for which an overlap was computed. At first, the precision and recall of the pair of sets were calculated while setting the chunk tokens as the ground truth and the generated question as a prediction. The harmonic mean of precision and recall were then calculated to generate the \textit{K-F1} score. In our situation, the query included both a topic and a question type, which is text that may be repeated in the generated exercise. To reduce the influence of the query on the metric, we removed the set of tokens present in both the query and generated exercises, mathematically \(R' = R \setminus Q\). Here, \( R \) is the set of tokens in the generated exercise, \( Q \) is the set of tokens in the query, and \( R' \) is their difference. \( \text{\textit{K-F1++}} \) is calculated as follows:

\[
\text{Precision} = \frac{|R' \cap C|}{|R'|}, \quad\text{Recall} = \frac{|R' \cap C|}{|C|}
\]
\[
\text{\textit{K-F1++}} = 2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}}
\]

where \( C \) represents the set of tokens in the chunk. To compute an average across the test set, we calculated the maximum response-chunk \textit{K-F1++} score per query and average across these maximums. The final equation is:
\begin{equation}
\text{\textit{Mean K-F1++}} = \frac{1}{N} \sum*{i=1}^{N} \max(\text{\textit{K-F1++}}*{i1}, \text{\textit{K-F1++}}_{i2}, \ldots, \text{\textit{K-F1++}}_{i7})
\end{equation}
where \( \text{\textit{K-F1++}}\_{ij} \) represents the \textit{K-F1++} score for the \( j \)-th response-chunk pair of the \( i \)-th query and \( N \) is the total number of queries in the test set.

\subsubsection\*{BERTScore}
BERTScore can be used to evaluate groundedness from a semantic perspective. We computed this using the the \inlinecode{{\inconsolata BERTScorer}} class from the \inlinecode{{\inconsolata bert-score}} Python package. Selecting the default parameters, the scorer separately tokenized each response, \( r \), and chunk, \( c \), pair using the BERT tokenizer. Each token in \( r \) and \( c \) was then embedded using RoBERTa-base, whose context-dependent embeddings capture the semantic meaning of each token. Subsequently, each token embedding in the two token sets was compared using cosine similarities and greedy matching to select the best token pairs between the texts to compute recall, precision, and F1. The following formulas are adapted from Zhang et al. \cite{bertscore}:
\[
R*{\text{BERT}} = \frac{1}{|\vec{c}|} \sum*{\vec{c}_i \in c} \max_{\vec{r}_j \in \vec{r}} \vec{c}\_i^\top \vec{r}\_j, \quad
P_{\text{BERT}} = \frac{1}{|\vec{r}|} \sum*{\vec{r}\_j \in \vec{r}} \max*{\vec{c}_i \in \vec{c}} \vec{c}\_i^\top \vec{r}\_j
\]
\[
F_{\text{BERT}} = 2 \frac{P*{\text{BERT}} \cdot R*{\text{BERT}}}{P*{\text{BERT}} + R*{\text{BERT}}}
\]

where \( \vec{c}\_i \) is the \( i \)-th chunk tokens embedding (reference) and \( \vec{r}\_j \) is the \( j \)-th response tokens embedding (candidate). The BERTScore was computed between each response-chunk pair, and the maximum was taken as the BERTScore for that query. This result was, in turn, averaged across the whole evaluation set.
```
