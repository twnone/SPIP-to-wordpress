# SPIP-to-wordpress
Python notebook to import your SPIP data right to WordPress ! 
No need for your SPIP website to be online as long as you already have your DB and attached files backed up.

## Why am I here ?
Maybe you've been in this situation, or maybe you will be : having to migrate a 500+ articles SPIP website, all sorted into 200+ categories can be a burden if you plan on doing it manually.
I was asked to migrate ours to Wordpress ; I tried some plugin that didn't fit my needs if I didn't pay extra €€€.

I have short arms and deep pockets ....So I decided to have fun with the Wordpress REST API and simply shove our data into Wordpress ! :D

## Pre-requisites
In order to make this work out, you will have to backup your SPIP data into an SQLite database.
I started developping with the SQLite files, but for a reason I can't remember, I dumped my data into MySQL and worked from there.
You still can work with the SQLite files, but you'll have to make some changes to the code ; in that case, feel free to make a pull request !

You'll also have to locally backup the files attached to your SPIP website. You should find them in the **IMG** subdirectory of your SPIP instance.

## Setup your environment + variables

Setup a python environment (I personally work with [Conda](https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html), but you could also use virtualenv, I guess).
It should include the following packages :
- [mysql-connector-python](https://pypi.org/project/mysql-connector-python/)
- [pandas](https://pandas.pydata.org/)
- [notebook](https://jupyter.org/install)
- [requests](https://pypi.org/project/requests/)


The first Jupyter Notebook cell will let you change the following values :
- Path to the SPIP files linked to the SPIP articles
- URL to your Wordpress instance
- Wordpress REST API token
- SSL certificate state

## Run the notebook

I would highly suggest to check after each cell what is exactly happening. You may have to modify the code if you want a behaviour that is not the same as the one I needed.

## Good Luck !
Feel free to submit issues, I will try to answer your questions.
