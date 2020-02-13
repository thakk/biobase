Bootstrap: docker
From: alpine:3.10.3
Stage: release

%post
    apk update
	apk add bash
	apk add fuse
	apk add fuse-dev
	apk add openjdk11-jdk
	apk add wget
	apk add curl

%appinstall scoreclient
	wget -O score-client-2.2.1.tar.gz https://artifacts.oicr.on.ca/artifactory/dcc-release/bio/overture/score-client/2.2.1/score-client-2.2.1-dist.tar.gz
	tar zxvf score-client-2.2.1.tar.gz
	rm score-client-2.2.1.tar.gz
	mv score-client-2.2.1 /usr/local/score-client
		
%apphelp scoreclient
	Score-client

%apprun scoreclient
	java -Xmx3G --illegal-access=deny -Dlogging.path=/tmp -Dspring.config.additional-location=/usr/local/score-client/conf/ -Dlogging.config=/usr/local/score-client/conf/logback.xml -cp /usr/local/score-client/lib/score-client.jar org.springframework.boot.loader.JarLauncher help

%labels
	Author "tomi.hakkinen@tuni.fi"
	Version 1.0
