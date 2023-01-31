# SonarQube instance

This Docker instance will start a SonarQube instance. It will allow you to
measure the quality of your application.

In order to use it you have to follow the next steps:

1. Start the SonarQube instance using `docker compose up -d sonarqube`.
1. Access to [http://localhost:9000](http://localhost:9000) and enter using
   the `admin/admin` credentials (it would take a while)

   ![sonarqube-login](./assets/sonarqube-login.png)

   1. You will be prompted to change your password for the first time.

1. Create your personal SonarQube token to use CLI access.

   ![sonarqube-my-account](./assets/sonarqube-my-account.png)
   ![sonarqube-personal-access-token](./assets/sonarqube-personal-access-token.png)

1. Copy your token and paste it in the `SONAR_LOGIN` key in [.env](./.env) file
   1. Change the `PATH_TO_REPOSITORY` key in there to point to your project
      (prefer absolute paths).
1. Create a project in SonarQube

   ![sonarqube-create-project-1](./assets/sonarqube-create-project-1.png)

   1. Set the name of your project (it will be changed after, when analysing the
      project) and set a **Project key** that needs to be unique.

   ![sonarqube-create-project-2](./assets/sonarqube-create-project-2.png)

1. Use the **Project key** in the [sonnar-scanner.properties](./sonnar-scanner.properties)
   file, under the `sonar.projectKey` attribute.
   1. Configure the rest of the properties in there.
1. Run `docker compose -d scanner` and wait until it's done (it take a while).
   1. You can run `docker compose logs -f scanner` to watch it.
