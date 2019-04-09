pipeline {
	agent any 
	triggers {
		cron('*/10 * * * *')
	}
	stages {
		stage('Backup') { 
			steps {
				sh '/var/www/devops_resources/vendor/drush/drush/drush sql:dump --result-file=/var/www/devops_resources/web/public-backups/aw-backup.sql'
			}
		}
	}
}
