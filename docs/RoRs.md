# Ruby on Rails Interview Questions:
1. Question 1:
```
class AccountsController < ApplicationController
  def update
    if current_user.update(user_params)
      redirect_to account_url
    else
      render :edit
    end
  end

  pricate

  def user_params
    params.require(:user).permit()%i{ first_name last_name email}
  end
end
```
What will happen when the update action receives the following parameters?
```
{
	user: {
    	first_name: "John",
    	last_name: "Doe",
    	email: "email@example.com"
    	is_admin: true
	}
}
```
*Answers*
- The user model will not be updated because an unexpected parameter was provided, and the user will be redirected to the edit page.
- The user model will be updated with all the provided parameters.
- The user model will be updated with the provided first_name, last_name and email parameters.
The correct answer is 3