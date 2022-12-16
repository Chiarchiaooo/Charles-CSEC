<div align="center">
  <h1>Charles CSEC (Beta)</h1>
  <img src="https://user-images.githubusercontent.com/76649588/208201214-add50e06-c0da-4e2d-ba87-d33c797d035b.png">
</div>

## Index

- [Features](#features)

- [Installation](#installation)
  
  - [From source code](#from-source-code)

- [Configuration (server-side)](#configuration)

- [Running](#running)

- [How work](#how-work)

- [License](#license)

- [Contributors](#contributors)

## Features

- RSA encryption

- Easy to read code

- Protected by network sniffer

- No trace of your IP

## Installation

### From source code

You need to have [**Python**](https://www.python.org/downloads/) and [**PIP**]([Python PIP](https://www.w3schools.com/python/python_pip.asp)) installed which you can download from your [**package manager**]([How to install Python on Linux? - GeeksforGeeks](https://www.geeksforgeeks.org/how-to-install-python-on-linux/)) or site.

After installing Python and PIP you can install ***program dependencies***.
You can ***go to the directory of the repository that you will have downloaded or download it*** with this command:

```bash
git clone https://github.com/aniko33/Charles-CSEC && cd Charles-CSEC
```

To install dependencies:

```bash
pip install -r requirements.txt
```

You ***have installed the various dependencies*** now you **can configure your server or start your client**.

## Configuration

To configure your server **open the file named *server.py***.

Go to the top of code until you find this part:

```python
#vars
welcome_message = "[red]Welcome to <chat name>[/red]"
clients = []
username = {}
buffer = 1024

#config
ip = "127.0.0.1"
port = 8889
```

| Variable        | Description                                                                                                                                       |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| welcome_message | Welcome message to new users, the colors can be found in the **[Rich documentation](https://rich.readthedocs.io/en/stable/appendix/colors.html)** |
| buffer          | It is the maximum network buffer, if you change this value the ***RSA key*** will ***increase in size***                                          |
| ip              | The IP address where the server will start waiting for connections                                                                                |
| port            | It is the **connection port**, it is recommended to ***keep it as the default*** (***8889***)                                                     |

## Running

To start the program just ***go to the program folder*** and execute this command:

#### Client

```bash
python client.py
```

#### Server

```bash
python server.py
```

## How work

The **keys are created *by the server*** and ***distributes them to connected clients***.
when the client wants to send a message, **it encrypts it with the *public key***, passes through the ***server and sends it to the clients***, who **decrypt it with the *private key***.

<div align="center">
<img width="800px" src="https://user-images.githubusercontent.com/76649588/208201163-7e596078-c95d-4902-8d94-e496b60fe315.png" title="" alt="flow.png" data-align="center">
</div>

## License

The library is distributed under the ***[GPL](https://it.wikipedia.org/wiki/GNU_General_Public_License) license*** you can ***consult the file***: ***[License.txt](License.txt)***

## Contributors

<a href="https://github.com/aniko33/NukeLib/graphs/contributors">
  <img src="https://contributors-img.web.app/image?repo=aniko33/NukeLib"/>
</a>