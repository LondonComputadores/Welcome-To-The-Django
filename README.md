# Welcome-To-The-Django
WTTD Recap to be up to date
 - Instructor: Henrique Bastos


Commands shot at wsl2 ubuntu zsh terminal:

 1. python -m venv .wttd
 2. source .wttd/bin/activate (optional: ls venv/bin; which python;)
 3. pip install django~=4.1.0
 4. django-admin startproject eventex .
 5. python manage.py runserver
 6. (Optional: python manage.py; python manage.py help inspectdb)
 7. echo $VIRTUAL_ENV
 8. alias manage='python $VIRTUAL_ENV/../manage.py'
 9. manage
 10. manage runserver (this can be ran from any directory now)

I unziped the frontend folder called landingpage.zip which there was inside:
 - css; fonts; img; js folders and also a index.html file.

Then I created a static folder in ./eventex/core path to add all the folders.
Then I created a template folder in ./eventex/core to add up the index.html

To replace html tags for django's template tags using the replace feature of your IDE:

 - On VSCode go to Edit>Replace then on the pop up window: 
  - Type in Search field this: (src|href)="((img|css|js).*?)"
  - Type in Replace field this: $1 ="{% static '$2' %}"

This will replace all the static links for dynamic links turning the index.html in a working dynamic page consuming the contents from the static (same as assets) folder