#### Show all list rbenv.

`rbenv install --list-all`

####  Update ruby building 
`brew update && brew upgrade ruby-build`

#### Install ruby 
`rbenv install 3.1.1 `

#### install rails
`gem install rails`

#### create new app

`rails new blog`

#### Create post module:

`bin/rails generate scaffold post title:string content:text`

#### rails action text for text area

```
rails action_text:install 
bundle
bin/rails db:migrate  
```

### Create comments
`rails g resource comment post:references  content:text`

### mailer
`rails g mailer comments submitted `

  preview: Link http://localhost:3000/rails/mailers/comments_mailer/submitted

### Changes database from SQlite to Postgresql
`rails db:system:change --to=postgresql`


### Run Test Case
  `rails test`

### Deploy application in to Heroku

Commit all files
```
git add .
git commit -m "Initial commit"
```

Add this in Gemlock if your in Mac:
`bundle lock --add-platform x86_64-linux`
`bundle install`

Login to heroku and create app and push it.

```
  heroku login
  heroku create
  git push heroku main
  heroku run rake db:migrate
```

Add Redis in to heroku as add ons.

`heroku addons:create heroku-redis:hobby-dev -a <APP Name>`


#### Exceptions during installations and fixes

Could not open library 'libvips.42.dylib': dlopen(libvips.42.dylib, 0x0005):

`brew install vips `
