FROM python:3

RUN apt-get update && apt-get install -y python3-pip

COPY requirements.txt .

RUN pip install -r requirements.txt

# Install jupyter
RUN pip3 install jupyter

# Create a new system user
RUN useradd -ms /bin/bash demo

# Change to this new user to move Jupyeter off root (for security reasons)
USER demo

# Set the container working directory to the user home folder
# need to specidfy the working directory
WORKDIR /home/demo

# Start the jupyter notebook
ENTRYPOINT ["jupyter", "notebook", "--ip=0.0.0.0"]
