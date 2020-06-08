---
layout: post
title:      "Rave-Sinatra"
date:       2020-06-08 15:14:33 +0000
permalink:  rave-sinatra
---


   Wow this was a fun project, finally felt like a genuine programmer. So this a Sinatra Project with a few requirements such as creating a CRUD(Create-Read-Update-Delete) and MVC(Model-View-Controller) application. Also at least two models with has_many & belongs_to relationship. My project decided to call it Rave-Sinatra(not super clever, I got to work on that).For those out there that enjoy going to raves/concerts  I wanted to create a way to keep track on money you think you will spend or keep track on how much you would need to save. Setting up for this project was made easy with the <a href=” https://github.com/thebrianemory/corneal.git”>cornel gem</a>. I recommend using if you already have a handle on setting up your environment and files from scratch. It saved me time and allow me to get right into setting up my 7 Restful routes.
		
		
   I started with Users and I will admit I wasn’t the best at using binding.pry but I got a lot of practice during this project.  The problems came with tracking what was being passed in my params and making sure I was getting the right information . Which it becomes more important when adding the second model. The raves to the user and making sure only that user can see, edit and delete their own raves.  This a cool code I learned to make sure all the fields are filled in and the params auto populate.

```
  get "/users/signup" do
    erb :"/users/signup.html"
  end

  post "/signup" do
    if params[:name] == "" || params[:email] == "" || params[:password] == ""
      redirect '/users/failure'
    else
      @user = User.create(params)
      session[:user_id] = @user.id
      redirect '/users/homepage'
    end 
  end ```

The Raves model didn’t take nearly as much time because it followed the same restful routes as the User model. Again just making sure the session[:user_id] matched took alittle working with.

   The last part  of this project involved me working with CSS, this was my first time learning and applying it. Thanks to one of my cohorts for mentioning <a href=”https://getbootstrap.com/>boot strap</a> It made this process easier. I still have a lot to learn but having the template and some code to mess around with was enjoyable. One thing I really appreciated is in their code it is fluid by default. So, as you change the size of your browser the content in it adjusts. Seeing your project not only working but become visually appealing is a great feeling. 
	 
Thanks for reading, this was a fun project and I do plan on coming back to it to add more features. 

