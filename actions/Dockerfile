# Use the same Rasa version as your other container
FROM rasa/rasa:2.8.21-full

# Set the working directory
WORKDIR /app

# Copy your action server code and requirements into the Docker image
COPY . /app/actions
COPY ../requirements-actions.txt /app/requirements-actions.txt

# Change to root user to install dependencies
USER root

# Install your action server dependencies
RUN pip install -r /app/requirements-actions.txt

# Define the command that will be run when the container starts
ENTRYPOINT ["rasa"]
CMD [ "run", "actions"]