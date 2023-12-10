# Use an official miniconda runtime as a parent image
FROM --platform=linux/amd64 continuumio/miniconda3:latest


# Set the working directory inside the container
WORKDIR /app

# Copy the environment.yml file into the container at /app
COPY environment.yml /app/environment.yml
# Copy the ejecutables directory
COPY JupyterNotebooks /app/JupyterNotebooks  

# Create a Conda environment from the YAML file
RUN conda env create -f environment.yml

# Activate the Conda environment
SHELL ["conda", "run", "-n", "myenv", "/bin/bash", "-c"]

# Install IPython kernel for the Conda environment
RUN python -m ipykernel install --user --name myenv --display-name "env_GeoPandas"

# Expose the Jupyter Lab port
EXPOSE 8888

# Start Jupyter Lab without password
CMD ["conda", "run", "-n", "myenv", "jupyter", "lab", "--ip='0.0.0.0'", "--port=8888", "--no-browser", "--allow-root", "--NotebookApp.token=''"]
