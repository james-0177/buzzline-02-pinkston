# buzzline-02-case

Streaming data is often too big for any one machine. Apache Kafka is a popular streaming platform that uses publish-subscribe patterns:

- **Producers** publish streaming data to topics
- **Consumers** subscribe to topics to process data in real-time

We'll write Python producers and consumers to work with Kafka topics.

Kafka needs space - it's big. 

It also comes from the Linux world. We'll use WSL on Windows machines.

## Copy This Example Project & Rename

1. Copy/fork this project into your GitHub account and create your own version of this project to run and experiment with.
2. Name it `buzzline-02-yourname` where yourname is something unique to you.

## Task 1. Install and Start Kafka (using WSL if Windows)

Before starting, ensure you have completed the setup tasks in <https://github.com/denisecase/buzzline-01-case> first.
Python 3.11 is required.

In this task, we will download, install, configure, and start a local Kafka service.

1. Install Windows Subsystem for Linux (Windows machines only)
2. Install Kafka Streaming Platform
3. Start the Kafka service (leave the terminal open).

For detailed instructions, see:

- [SETUP_KAFKA](SETUP_KAFKA.md)

## Task 2. Manage Local Project Virtual Environment

Open your project in VS Code and use the commands for your operating system to:

1. Create a Python virtual environment
2. Activate the virtual environment
3. Upgrade pip
4. Install from requirements.txt

### Windows

Open PowerShell terminal in VS Code (Terminal / New Terminal / PowerShell).

```powershell
py -3.11 -m venv .venv
.venv\Scripts\Activate.ps1
py -m pip install --upgrade pip wheel setuptools
py -m pip install --upgrade -r requirements.txt
```

If you get execution policy error, run this first:
`Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`

### Mac / Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install --upgrade pip
python3 -m pip install --upgrade -r requirements.txt
```

## Task 3. Start a Kafka Producer

Producers generate streaming data for our topics.

In VS Code, open a terminal.
Use the commands below to activate .venv, and start the producer.

Windows:

```shell
.venv\Scripts\activate
py -m producers.kafka_producer_case
```

Mac/Linux:

```zsh
source .venv/bin/activate
python3 -m producers.kafka_producer_case
```

## Task 4. Start a Kafka Consumer

Consumers process data from topics or logs in real time.

In VS Code, open a NEW terminal in your root project folder.
Use the commands below to activate .venv, and start the consumer.

Windows:

```shell
.venv\Scripts\activate
py -m consumers.kafka_consumer_case
```

Mac/Linux:

```zsh
source .venv/bin/activate
python3 -m consumers.kafka_consumer_case
```

## Later Work Sessions

When resuming work on this project:

1. Open the folder in VS Code.
2. Start the Kafka service.
3. Activate your local project virtual environment (.venv).

## Save Space

To save disk space, you can delete the .venv folder when not actively working on this project.
You can always recreate it, activate it, and reinstall the necessary packages later.
Managing Python virtual environments is a valuable skill.

## License

This project is licensed under the MIT License as an example project.
You are encouraged to fork, copy, explore, and modify the code as you like.
See the [LICENSE](LICENSE.txt) file for more.

## Task 5. Create custom producer file

Create a new file named kafka_producer_pinkston.py. Copy and paste contents of kafka_producer_case.py into kafka_producer_pinkston.py as a starting basis.

## Task 6. Add, commit, and push after creating custom producer file

```shell
.venv\Scripts\activate
git add.
git commit -m "created custom producers file"
git push -u origin main
```

## Task 7. Modify custom producer file

Update custom producer file kafka_producer_pinkston.py with custom messages.

```shell
string_list: list = [
        "I don't love Python, but it's ok!",
        "Kafka is interesting.",
        "Streaming data is fun.",
        "I'm not so sure about this.",
        "Today (Sunday), my friends and I met to play Dungeons and Dragons.",
        "We've been playing off-and-on for over 20 years!",
        "In our current campaign, my warlock has reached 9th level!",
        "This is a buzz message.",
        "Have a great day!",
    ]
```

## Task 8. Add, commit, and push updated custom producer file

```shell
.venv\Scripts\activate
git add.
git commit -m "modified custom producer file"
git push -u origin main
```

## Task 9. Tested new custom producer file

Followed Step 4 and Step 5 [here](https://github.com/denisecase/buzzline-02-case/blob/main/SETUP_KAFKA.md) to start the Kafka broker. Then opened a second terminal.

```shell
.venv\Scripts\activate
py -m producers.kafka_producer_pinkston
```

After testing, entered ctrl + c to stop producer file and return to PowerShell prompt.

## Task 10. Create custom consumer file

Create a new file named kafka_consumer_pinkston.py. Copy and paste contents of kafka_consumer_case.py into kafka_consumer_pinkston.py as a starting basis.

## Task 11. Add, commit, and push after creating custom consumer file

```shell
.venv\Scripts\activate
git add.
git commit -m "created custom consumers file"
git push -u origin main
```

## Task 12. Modify custom consumer file

Update custom consumer file kafka_consumer_pinkston.py with custom analytics to include basic message counter to include total messages, and messages in the last 30 seconds.

## Task 13. Add, commit, and push updated custom consumer file

```shell
.venv\Scripts\activate
git add.
git commit -m "modified custom consumers file"
git push -u origin main
```
