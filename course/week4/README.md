# Week 4 Project: Retrieval augmented generation

```
pip install -e .
```

This project will explore data-centric approaches to building high quality RAG systems.

### Setup

Please copy the `.env.template` to a `.env` file. 
- Please ask the teaching team for an OpenAI API key to use GPT 3.5. You will set this key to the `OPENAI_API_KEY` variable in `.env`.
- Please ask the teaching team for a Starpoint API key to use the Starpoint vector db. You will set this key to the `STARPOINT_API_KEY` variable in `.env`.

### Project

There is code for you to complete in the following files

- `scripts/build_eval_set.py`
- `scripts/insert_docs.py`
- `scripts/optimizer_params.py`

We recommend you to follow the instructions on Uplimit closely.


### Running build_eval_set
(.venv) @stefansturlu ➜ /workspaces/data-centric-deep-learning/course/week4 (main) $ python scripts/build_eval_set.py run
Metaflow 2.12.7 executing BuildEvaluationSet for user:vscode
Validating your flow...
    The graph looks good!
Running pylint...
    Pylint not found, so extra checks are disabled.
2024-08-02 18:17:55.695 Workflow starting (run-id 1722622675693537):
2024-08-02 18:17:55.703 [1722622675693537/start/1 (pid 47656)] Task is starting.
2024-08-02 18:17:57.868 [1722622675693537/start/1 (pid 47656)] Task finished successfully.
2024-08-02 18:17:57.872 [1722622675693537/write_questions/2 (pid 47687)] Task is starting.
2024-08-02 18:19:53.622 [1722622675693537/write_questions/2 (pid 47687)] Writing questions:   0%|          | 0/57 [00:00<?Writing questions: 100%|██████████| 57/57 [01:53<00:00,  2.00s/it]
2024-08-02 18:19:53.622 [1722622675693537/write_questions/2 (pid 47687)] Wrote 197 questions.
2024-08-02 18:19:53.958 [1722622675693537/write_questions/2 (pid 47687)] Task finished successfully.
2024-08-02 18:19:53.961 [1722622675693537/grade_questions/3 (pid 48385)] Task is starting.
2024-08-02 18:21:29.693 [1722622675693537/grade_questions/3 (pid 48385)] Grading questions:   0%|          | 0/197 [00:00<Grading questions: 100%|██████████| 197/197 [01:33<00:00,  2.10it/s]
2024-08-02 18:21:29.693 [1722622675693537/grade_questions/3 (pid 48385)] Average rating: 4.771573604060913
2024-08-02 18:21:30.005 [1722622675693537/grade_questions/3 (pid 48385)] Task finished successfully.
2024-08-02 18:21:30.009 [1722622675693537/write_hypothetical_answers/4 (pid 48967)] Task is starting.
2024-08-02 18:24:00.671 [1722622675693537/write_hypothetical_answers/4 (pid 48967)] Writing answers:   0%|          | 0/19Writing answers: 100%|██████████| 197/197 [02:28<00:00,  1.32it/s]
2024-08-02 18:24:00.671 1 task is running: write_hypothetical_answers (1 running; 0 done).
2024-08-02 18:24:00.672 No tasks are waiting in the queue.
2024-08-02 18:24:00.672 2 steps have not started: save_questions, end.
2024-08-02 18:24:00.672 [1722622675693537/write_hypothetical_answers/4 (pid 48967)] Wrote 197 hypothetical answers.
2024-08-02 18:24:01.034 [1722622675693537/write_hypothetical_answers/4 (pid 48967)] Task finished successfully.
2024-08-02 18:24:01.038 [1722622675693537/save_questions/5 (pid 49869)] Task is starting.
2024-08-02 18:24:03.110 [1722622675693537/save_questions/5 (pid 49869)] Task finished successfully.
2024-08-02 18:24:03.113 [1722622675693537/end/6 (pid 49902)] Task is starting.
2024-08-02 18:24:04.886 [1722622675693537/end/6 (pid 49902)] done! great work!
2024-08-02 18:24:05.211 [1722622675693537/end/6 (pid 49902)] Task finished successfully.
2024-08-02 18:24:05.212 Done!