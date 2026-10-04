# 🐘 Square Cloud PgAdmin4
## Host pgAdmin on Square Cloud ☁️

> 🌐 Easily host your own pgAdmin on Square Cloud and manage your PostgreSQL databases from anywhere, right from your browser.

---

## 🚀 How to host this project on Square Cloud

New to Square Cloud? Follow these steps in order. You will create an account, choose a plan and upload a ready-made zip: no coding needed.

### 1️⃣ Create your Square Cloud account

Sign up on the [Square Cloud signup page](https://squarecloud.app/en/signup) with your email.

### 2️⃣ Choose a plan

Hosting on Square Cloud requires an active plan, and the upload in step 4 asks for one, so choose it now.

pgAdmin needs **1 GB of RAM**: the **[Hobby plan](https://squarecloud.app/en/pricing)** runs it. To also host the PostgreSQL database on Square Cloud, choose the **[Standard plan](https://squarecloud.app/en/pricing)**: managed databases need Standard or higher. Compare every plan and its price on the [pricing page](https://squarecloud.app/en/pricing).

### 3️⃣ Download the project

Download **`project.zip`** from the [latest release](https://github.com/squarecloud-education/pgadmin4-web/releases/latest). This is the file you upload in the next step: you don't need to extract it.

### 4️⃣ Upload it to Square Cloud

1. Open the [Square Cloud upload page](https://squarecloud.app/en/dashboard/new).
2. Select the **zip** option and send the `project.zip` you downloaded.
3. Select **Web Publication** and choose a subdomain, for example `my-pgadmin`. Your pgAdmin will be at `https://my-pgadmin.squareweb.app`.
4. Open **Advanced configuration** and add these environment variables. pgAdmin uses them to create your login on the first start:
   - `PGADMIN_SETUP_EMAIL`: the email you will log in with
   - `PGADMIN_SETUP_PASSWORD`: a strong password
5. Click **Deploy**.

![Uploading a project to Square Cloud](https://cdn.squarecloud.app/docs/articles/dashboard/uploading.gif)

### 5️⃣ Log in

Open `https://my-pgadmin.squareweb.app` and log in with the email and password you set. Then add your PostgreSQL server to manage it from anywhere. Need a database? See [how to create a managed database](https://docs.squarecloud.app/en/tutorials/how-to-deploy-your-database) on Square Cloud.

📖 Need more details? Read the [full pgAdmin guide](https://docs.squarecloud.app/en/tutorials/how-to-deploy-pgadmin) in the Square Cloud documentation.

---

## 📦 What's inside

- **pgAdmin 9.18**, served by **Gunicorn 26.2**, both pinned in `requirements.txt`.
- `main.py` starts pgAdmin on port 80 with a single worker (more workers cause CSRF errors).
- `config_local.py` keeps pgAdmin's data in the `.pgadmin4` folder of your application.

---

## 📚 About the project

The goal of this project is to let you host a pgAdmin instance on Square Cloud, so you can access your PostgreSQL databases from anywhere, directly from your browser.

---

🙋‍♂️ **Questions or suggestions?** Contact [Square Cloud Support](https://squarecloud.app/sac) or open an issue in this repository!

---

## 🙏 Credits

Maintained by [@josejooj](https://github.com/josejooj) on GitHub.
