# Flyway-Migrator: Database Migration

This is an example repository that demonstrates how to set up automated database migrations using **Flyway** and **GitHub Actions**

**Flyway** is a popular database migration tool that can be easily integrated with GitHub Actions to automate your migration process.

## 🚀 Getting started

To get started with this example, you'll need to have the following:

- A PostgreSQL database
- Flyway installed on your local machine
- A GitHub account

## ⚙️ Setting up Flyway

Before you can use Flyway, you'll need to download it and configure it with your database connection details. You can download Flyway from the official website: https://flywaydb.org/download/.

Once you've downloaded and installed Flyway, you'll need to update a configuration file (`flyway.conf`) in `/conf` directory with appropriate values as per your database setup.

## 🏃‍♂️ Run

### Clone this repository

```sh
git clone git@github.com:Chetan07j/flyway-migrator.git
```

### Enter into directory

```sh
cd flyway-migrator
```

### **Migrate**

You can execute the following command to run migration scripts and set the schema to the latest version:

```sh
flyway -configFiles="./conf/flyway.conf" migrate
```

## GitHub Action

GitHub Action workflow_dispatch event allows you to manually trigger a workflow from the GitHub Actions tab. It provides a way to run workflows without pushing any changes to the repository.

After adding the migration script to the sql directory in this repository, you can easily run the GitHub Action to execute those migrations in any location you specify.

An additional step is included in the Action file, which saves the output of `flyway info` command into a text file with a filename containing a `timestamp`, and then places that file under the `migration-status` directory.

## 🔗 References

- [Flyway Commands](https://documentation.red-gate.com/fd/commands-184127446.html)

## 🙋‍♂️ Support

💙 If you like this project, give it a ⭐
