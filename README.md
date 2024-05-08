# Exploring OpenELM
Running it on WSL, so I'll still have to get used to it a bit.

First, create the Python environment:
  sudo apt-get update
  sudo apt-get install libpython3-dev
  sudo apt-get install python3-venv
  python3 -m venv .

To change into the venv:

  source bin/activate

I always forget about requirements.txt, so here is how to create it:

  pip freeze > requirements.txt

And then restoring from another machine:

    pip install -r requirements.txt

To run the model:

  python generate_openelm.py --model apple/OpenELM-1_1B-Instruct --hf_access_token [YOUR_TOKEN] --prompt "There once was a duck called" --generate_kwargs repetition_penalty=1.2
