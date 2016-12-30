# ansible_recipes [![Build Status](https://travis-ci.org/fede2cr/ansible_recipes.svg?branch=master)](https://travis-ci.org/fede2cr/ansible_recipes)
Ansible recipes for my own stuff... might be useful for your stuff as well

## Instructions
1. Create inside the recipe folder, an ```inventory/``` folder with a ```hosts``` file inside with a content like:

```
10.1.2.3 ansible_user=alvaro
```
2. ```ssh-copy-id``` to the server
3. Either create a ```sudo``` file to avoid writing the password, or add ```-K``` to ```ansible-playbook```
4. Run ansible-playbook inside the recipe dir
```
ansible-playbook some-recipe.yml
```
