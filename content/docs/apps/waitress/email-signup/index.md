---
title: "Create Email Signup Form"
description: "Want to collect emails or short forms on your website but don't want to setup a backend. Don't like the embedded google form layout but only the functionality? In this post will walk through how to create a email signup or any forms with the Waitress app in three easy steps."
lead: "Want to collect emails or short forms on your website but don't want to setup a backend. Don't like the embedded google form layout but only the functionality? In this post will walk through how to create a email signup or any forms with the Waitress app in three easy steps."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "waitress"
weight: 320
toc: true
---

Navigate to [Waitress App on Telescope](https://telescope.apiobuild.com/app/waitress) to start.

## 1. Create New Google Sheet

[Create a new google sheets →](https://docs.google.com/spreadsheets/create)

You don't need to create a new one if you wish to use an existing one. Just go to the one you wish to use and follow the instruction on Telescope:

{{< alert icon="💡" text="Pop-up blocker could disable the login window. Allow or disable pop-up blocker if you are not able to sign-in." >}}

1. Click Share on the top right of the google sheet
2. Share to `waitress-dev@apio-277201.iam.gserviceaccount.com` as an Editor
3. Copy the google sheet to the console and click the 🔓 icon to authorize us to access your google sheets.
  {{< img src="waitress-app-instruction.png" >}}
4. Copy the API route with you, we will need it in the next step.
  {{< img src="copy-waitress-route.png" >}}

## 2. Create Auth Token

<!-- trampoline auth ref -->
<!-- trampoline token -->

In order to use apio's platform services outside of Telescope, we require general users to create apio's platform auth token. To create a token:

{{< alert icon="💡" text="If you don't see the gear icon ⚙️ on the top left, click on the sign in icon on the top left corner on Telescope <img src='telescope-sign-in.png' style='width: 100%'>" >}}

<!-- TODO: view token and add token -->

1. Click the gear button ⚙️ to view [Telescope user settings](https://telescope.apiobuild.com/settings).
2. Click `VIEW TOKEN` and scroll to the bottom to `Add New Token`.
   - Alias
     You can use any alias that you wish. This just so that you can remember what the token was created for.
   - Target Audience
     {{< alert icon="💡" text="Use http://localhost:port if you are testing locally." >}}
     This will be the domain you wish to use the token with. For example, we put `https://apiobuild.com/` for [the email form sign up form on apiobuild.com](https://apiobuild.com/#sign-up). You can always update audience as needed.
3. Expand the token you just created. Paste the API route from [Step 1](/docs/apps/waitress/email-signup/#1-create-new-google-sheet), select `POST` and click ➕ button.  
  {{< alert icon="💡" text="This means the token allows you to make post request to the API route from domain (audience) specified." >}}

## 3. Add HTML Form

{{< alert icon="💡" text="The sky is the limit, you can customize to your needs as long as your form captures the fields you wish to capture and make a post request to the Waitress API endpoint." >}}

### HTML

All it does is to create a form on your page. If you use other frameworks such as Vue, you don't need to follow the bootstrap convention. This is a short bootstrap example:

<form>
  <div class="row px-4">
    <div class="col col-12 col-sm-4 px-1 py-1">
      <input type="text" class="form-control" id="fname" placeholder="Enter name">
    </div>
    <div class="col col-12 col-sm-6 px-1 py-1">
      <input type="text" class="form-control" id="femail" placeholder="Enter email">
    </div>
    <div class="col col-12 col-sm-4 px-1 py-1">
      <button id="email-sign-up-submit-btn" type="button" class="btn btn-primary btn-md" style="width: 100%" onclick="submitForm()">Sign Up
      </button>
    </div>
  </div>
</form>

```html
<form>
  <div class="row">
    <div class="col col-12 col-sm-4">
      <input
        type="text"
        class="form-control"
        id="fname"
        placeholder="Enter name"
      >
    </div>
    <div class="col col-12 col-sm-6">
      <input
        type="text"
        class="form-control"
        id="femail"
        placeholder="Enter email"
      >
    </div>
    <div class="col col-12 col-sm-4">
      <button
        type="button"
        class="btn btn-primary btn-md btn-block"
        onclick="submitForm()">
        Sign Up
      </button>
    </div>
  </div>
</form>
```

### Javascript

Notice the `submitForm` function above. We need to define a javascript function to make a POST request to the Waitress API route with the token you just created.

<!-- TODO: image to copy token and API url -->

Copy the Telescope Service Token and Waitress API Route into the following snippet.

<!-- TODO: update token -->

<script type="text/javascript">
  let token = "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImYyZmU4NmMyLWYzNDktNGEwMC1hZWI1LWI5MmRiYzQ0ZDQyMCIsImF1ZCI6Imh0dHA6Ly9sb2NhbGhvc3Q6MTMxMyIsImlhdCI6MTYxNTc2ODkzOCwiaXNzIjoiZ29vZ2xlLW9hdXRoMnwxMDYzMDg1MzI3NDc1Mzc3MjU1MTciLCJzdWIiOiJnb29nbGUtb2F1dGgyfDEwNjMwODUzMjc0NzUzNzcyNTUxNyJ9.L3JhEVdYSJ2oXc9--Nmp7zMOpRPhmQhRzMsD9jC_Kcg"
  let url = "https://trampoline.apiobuild.com/router/waitress/gsheets/1tVY9mAf_VMZXJbgQANj3CJhD7by05adONOI7EDsUR3s";

  const submitForm = async () => {
    const btn = document.getElementById("email-sign-up-submit-btn");
    let name = document.getElementById('fname').value;
    let email = document.getElementById('femail').value;
    let created = new Date().toISOString();
    let payload = [
      {
        Name: name,
        Email: email,
        Created: created
      },
    ];

    btn.setAttribute("disabled", "");

    const resp = await fetch(url, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        'Authorization': token,
      },
      body: JSON.stringify(payload)
    });
    if (resp.status === 200) {
      btn.classList.remove("btn-primary");
      btn.classList.add("btn-success");
      btn.innerHTML = "Added";
    } else {
      btn.removeAttribute("disabled");
    }
  }
</script>

```html
<script type="text/javascript">
  let token = "Bearer <Telescope Service Token>"
  let url =
  "https://trampoline.apiobuild.com/router/<Waitress API Route>";

  const submitForm = async () => {
    const btn = document.getElementById("email-sign-up-submit-btn");
    let name = document.getElementById('fname').value;
    let email = document.getElementById('femail').value;
    let created = new Date().toISOString();
    let payload = [
      {
        Name: name,
        Email: email,
        Created: created
      },
    ];
    const resp = await fetch(url, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
        'Authorization': token,
      },
      body: JSON.stringify(payload)
    });
  }
</script>
```

## Happy Emailing 📧

That's it. We will continue to improve our process to make this even easier. Let us know if you run into any issue. [Drop us a message →](/docs/introduction/introduction/#contact-us).
