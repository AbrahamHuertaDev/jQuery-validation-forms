jQuery-validation-forms
=======================

jQuery plugin for validation forms


Example

```html
<!--Name the inputs name same as jquery-->
<input type="text" name="username">
```

```javascript
$('.form').weValidate({
    validate: {
        username: {
            //rules for validate form
            rules: 'required|min:6',
            //as will be the name that appears in the notification
            as: 'Username',
        },
        email: {
            rules: 'required|email',
            as: 'E-mail'
        },
        password: {
            rules: 'required|min:6',
            as: 'Password'
        },
        password_repeat: {
            rules: 'required|min:6|same:password',
            as: 'Confirm'
        }
    },
    messages: {
        //custom messages
        //plugin replaces the :name with the name labeled as
        required: ':name is required',
        //plugin replaces the :min with the min characters
        min: ':name muts have more than :min characters',
        email: ':name not valid',
        //plugin replaces the :max with the max characters
        max: ':name must have less than :max characters',
        //plugin replaces the :same with the name labeled same
        same: ':name must match the :same'
    }
});
```
