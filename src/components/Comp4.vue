<template>
<div class="container my-2 py-2">
<h1 class="text-center" id="account">Account</h1>
<form id="create_account" class="needs-validation" novalidate action="success.html">
    <div class="mb-3 mt-3">
        <label for="email">Email</label>
        <input type="text" class="form-control" id="email" name="email" placeholder="name@provider.com" required>
        <div class="valid-feedback">Valid.</div>
        <div class="invalid-feedback">Email must be valid.</div>
    </div>
    <div class="mb-3">
        <label for="reEmail">Confirm Email</label>
        <input type="text" class="form-control" id="reEmail" name="reEmail" placeholder="name@provider.com" required>
        <div class="valid-feedback">Valid.</div>
        <div class="invalid-feedback">Email must match.</div>
    </div>
    <div class="mb-3">
        <label for="password">Password</label>
        <input type="text" class="form-control" id="password" name="password" placeholder="strongPassword1!" required>
        <div class="valid-feedback">Valid.</div>
        <div class="invalid-feedback">Minimum eight characters, at least one letter, one number and one special character</div>
    </div>
    <div class="mb-3">
        <label for="rePassword">Confirm Password</label>
        <input type="text" class="form-control" id="rePassword" name="rePassword" placeholder="strongPassword1!" required>
        <div class="valid-feedback">Valid.</div>
        <div class="invalid-feedback">Password must match.</div>
    </div>
    <div class="mb-3">
        <label class="form-check-label">
        <input class="form-check-input" type="checkbox" name="terms" required> Terms and Conditions
        </label>
        <div class="valid-feedback">Valid.</div>
        <div class="invalid-feedback">Please agree to terms and conditions.</div>
    </div>
        <button type="submit" class="btn btn-success">Submit</button>
        <button type="reset" class="btn btn-danger">Clear</button>
</form>
</div>
<div class="container my-2 py-2">
<h1 class="text-center" id="contact">Contact Us</h1>
<form class="needs-validation" action="success.html">
    <div class="mb-3 mt-3">
        <label for="email">Email</label>
        <input type="text" class="form-control" id="email" name="email" placeholder="name@provider.com" required>
    </div>
    <div class="mb-3">
        <label for="message">Message</label>
        <textarea class="form-control" id="message" name="message" placeholder="Enter your message here" rows="3" required></textarea>
    </div>
    <div class="mb-3">
    <button type="submit" class="btn btn-success">Submit</button>
    <button type="reset" class="btn btn-danger">Clear</button>
    </div>
</form>
</div>


</body>
</template>

<script>
export default {
  name: 'Comp4',
  props: {
    msg: String
  }
}
'use strict'
// validation
const forms = document.querySelectorAll('.needs-validation')
const inputs = document.querySelectorAll('.form-control')
const emailPattern = /\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,4}\b/
const passwordPattern = /^(?=.*[A-Za-z])(?=.*\d)(?=.*[@$!%*#?&])[A-Za-z\d@$!%*#?&]{8,}$/
let valid = true
// validate
function validation () {
  Array.prototype.slice.call(inputs)
    .forEach(function (input) {
      if (input.id === 'email') {
        if (!emailPattern.test(input.value)) {
          valid = false
          input.classList.add('is-invalid')
        } else {
          input.classList.add('is-valid')
        }
      } else if (input.id === 'reEmail') {
        if (input.value !== document.getElementById('email').value || input.value === '') {
          valid = false
          input.classList.add('is-invalid')
        } else {
          input.classList.add('is-valid')
        }
      } else if (input.id === 'password') {
        if (!passwordPattern.test(input.value)) {
          valid = false
          input.classList.add('is-invalid')
        } else {
          input.classList.add('is-valid')
        }
      } else if (input.id === 'rePassword') {
        if (input.value !== document.getElementById('password').value || input.value === '') {
          valid = false
          input.classList.add('is-invalid')
        } else {
          input.classList.add('is-valid')
        }
      }
      document.getElementById('create_account').classList.add('was-validated')
    })
}
// reset
function reset () {
  Array.prototype.slice.call(inputs)
    .forEach(function (input) {
      input.classList.remove('is-invalid')
      input.classList.remove('is-valid')
    })
  Array.prototype.slice.call(forms)
    .forEach(function (form) {
      form.classList.remove('was-validated')
    })
}
// submit
Array.prototype.slice.call(forms)
  .forEach(function (form) {
    form.addEventListener('submit', function (event) {
      validation()
      if (valid !== false) {
        Array.prototype.slice.call(forms)
          .forEach(function (form) {
            form.classList.remove('was-validated')
          })
      } else {
        event.preventDefault()
      }
    }
    )
  })
Array.prototype.slice.call(forms)
  .forEach(function (form) {
    form.addEventListener('reset', function (event) {
      reset()
    }
    )
  })

//

</script>

<style scoped>
body{
  background-color: #e8eddf;
}
div{
  background-color: #E8EDDF;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

</style>