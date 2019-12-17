# Heroku with Rails Homework HW12

### Do the Following
1. **[CD to your rails Book app] (The one we did in the lab)** in the terminal `cd book_app`
2. **[Create a new repository]** Oben your github account and create a new repository and call it book_app
3. **[Initialize the repository] (Follow repository steps)**

```Bash
echo "# Book_app" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/daghustani/Book_app.git //your github repo link
git push -u origin master
```

4. **[Open the book_app]:** In the terminal `code .`
5. **[Go to Gemfile in Rails app]:** Add this in the end.  

```Bash
group :production do
  gem 'pg'
end
```

6. **[Go to config/database.yml]:** change inside this code the encoding to `encoding:utf8`
```bash
default: &default
  adapter: mysql2
  encoding: utf8mb4 #change inside this code the encoding to `encoding:utf8`
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  username: root
  socket: /tmp/mysql.sock
```
7. **[bundle]:** In the terminal `bundle`
8. **[Push it in github]:(Follow steps)** 

```Bash
git add .
git commit -m 
git push origin master 
```

9. **[Create an account in Heroku]:(Follow steps)**(https://signup.heroku.com/devcenter)
10. **[Create a new app in Heroku]:** In Heroku website create a new app after signing up. Make sure you (Add an app name and choose Europe as a region)

11. **[Download and install the Heroku CLI]:**(https://devcenter.heroku.com/articles/heroku-cli#download-and-install)
12.**[Follow Heroku steps]:**

```bash
heroku login
heroku git:clone -a appName # The appname you created in Heroku
cd appName #To the appname you created in Heroku
git add .
git commit -am "make it better"
git push heroku master
```

13. **[Open your Heroku website]:** go to your app name
14. **[Click More]** on the right hand side of the page next to Open app button.
15. **[Run Console]** go to Run Console
17. **[In Heroku Console] (Follow this steps)** 

```bash
bundle
db:migrate
```

### After Finishing the Previous Steps Do the Following in this repo
1. Fork this Repo 
2. Add the Link of the Heroku website
4. Do a Pull Request


