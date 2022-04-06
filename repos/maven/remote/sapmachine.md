## `maven:sapmachine`

```console
$ docker pull maven@sha256:c22bd69e10ea47c2e2ddeefaee16f5f9a58f6d6b705013e7fe3a4a1b6155f7be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:9d1645f790ef32893670e6006a86c91fad8115bf6c96f348c114030593adad23
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275125146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce67d6c80baa03d9b20ef20dc2e54fb9e2f9e06080e83c1022cf1bbde1782c9b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:16:31 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:16:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 06 Apr 2022 04:16:32 GMT
CMD ["jshell"]
# Wed, 06 Apr 2022 04:59:09 GMT
RUN apt-get update     && apt-get install -y curl git     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:59:10 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 06 Apr 2022 04:59:10 GMT
ARG USER_HOME_DIR=/root
# Wed, 06 Apr 2022 04:59:10 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 06 Apr 2022 04:59:10 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 06 Apr 2022 04:59:12 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 06 Apr 2022 04:59:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 06 Apr 2022 04:59:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 06 Apr 2022 04:59:12 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 06 Apr 2022 04:59:12 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 06 Apr 2022 04:59:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 06 Apr 2022 04:59:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dbd16ff38383c60b8fc1bf647050936263de1dd59479348cbd39aa26485b59`  
		Last Modified: Wed, 06 Apr 2022 04:16:51 GMT  
		Size: 8.3 MB (8317679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7512af92b6ae0be0aaf1818560cdb45b872292100901f10b6509350d9f9ac285`  
		Last Modified: Wed, 06 Apr 2022 04:17:53 GMT  
		Size: 197.6 MB (197647563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa7eab7d130867a74414870cd744cc7bbf2b7f0eadd1c1bd8e0488cf1ee93f9`  
		Last Modified: Wed, 06 Apr 2022 05:04:03 GMT  
		Size: 31.9 MB (31856015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a7f648db2728e449e40d914cdeb1aa7fe67702489de8d9de215706b0e12018`  
		Last Modified: Wed, 06 Apr 2022 05:03:59 GMT  
		Size: 8.7 MB (8736388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f149489895bcabb644cd83b6b8d0d8ce5f8af3bfeded675fcefda358802e14ca`  
		Last Modified: Wed, 06 Apr 2022 05:03:58 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84e72c8b5bbcc8f021daf2411d9fa1b3e92566dcf82c906fba5c91e105eb539`  
		Last Modified: Wed, 06 Apr 2022 05:03:58 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
