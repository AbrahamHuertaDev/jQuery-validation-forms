jQuery-validation-forms
=======================

jQuery plugin for validation forms


Example
$('.form').weValidate({
    validate: {
        username: {
            rules: 'required|min:6',
            as: 'Usuario',
        },
        email: {
            rules: 'required|email',
            as: 'Correo Electrónico'
        },
        password: {
            rules: 'required|min:6',
            as: 'Contraseña'
        },
        password_repeat: {
            rules: 'required|min:6|same:password',
            as: 'Confrimación'
        }
    },
    messages: {
        required: ':name requerido',
        min: ':name debe tener mas de :min caracteres',
        email: ':name no valido',
        max: ':name debe tener menos de :max caracteres',
        same: ':name debe coincidir con :same'
    }
});
