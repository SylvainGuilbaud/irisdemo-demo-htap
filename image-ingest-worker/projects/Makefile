
# This makefile will be run by the build script or docker autobuild hooks to produce the app.jar file we need
# for this worker. 
build:
	(cd /usr/projects/ingest-worker-project && mvn clean package)

	# This parent project has many modules. Each module is a type of worker with exceptio of app-module
	# that has the shared code base for all workers.

	# Add a cp command here for each type of worker that has been created. 
	# We are eliminating the version number.
	cp /usr/projects/ingest-worker-project/iris-jdbc-ingest-worker/target/iris-jdbc-ingest-worker-*.jar /usr/projects/iris-jdbc-ingest-worker.jar
	cp /usr/projects/ingest-worker-project/mysql-jdbc-ingest-worker/target/mysql-jdbc-ingest-worker-*.jar /usr/projects/mysql-jdbc-ingest-worker.jar
	cp /usr/projects/ingest-worker-project/hana-jdbc-ingest-worker/target/hana-jdbc-ingest-worker-*.jar /usr/projects/hana-jdbc-ingest-worker.jar