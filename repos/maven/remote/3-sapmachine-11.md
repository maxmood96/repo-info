## `maven:3-sapmachine-11`

```console
$ docker pull maven@sha256:dd198799b8ab81c4a944681aa54120678f6531294c0d1be0ee54f3b25af367aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-sapmachine-11` - linux; amd64

```console
$ docker pull maven@sha256:9128c8738b1d890954875657f0f46113207e261a658492ebf524662a79abfc9d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275189150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd65802ec74e02009f01f02feb42e00f7ada22b91252c85c039552f480e9074`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:15:12 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.14.1     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:15:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 06 Apr 2022 04:15:13 GMT
CMD ["jshell"]
# Wed, 06 Apr 2022 04:58:55 GMT
RUN apt-get update     && apt-get install -y curl git     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:58:56 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 06 Apr 2022 04:58:56 GMT
ARG USER_HOME_DIR=/root
# Wed, 06 Apr 2022 04:58:56 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 06 Apr 2022 04:58:56 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 06 Apr 2022 04:58:58 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 06 Apr 2022 04:58:58 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 06 Apr 2022 04:58:58 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 06 Apr 2022 04:58:58 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 06 Apr 2022 04:58:58 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 06 Apr 2022 04:58:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 06 Apr 2022 04:58:58 GMT
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
	-	`sha256:24060e712a80036e70b0c41da5d08017d1b47fcd2b7660b78aad24452bcd270e`  
		Last Modified: Wed, 06 Apr 2022 04:17:04 GMT  
		Size: 197.7 MB (197711339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf8f88053c0c70049f0ddd9716cc2ecd987ca583dd7b38878d88d4656581b4c`  
		Last Modified: Wed, 06 Apr 2022 05:03:44 GMT  
		Size: 31.9 MB (31856255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd220e5b754b7c17f8411110fe10c8b6f146f1b9d172a5921af7dc4f25eb3701`  
		Last Modified: Wed, 06 Apr 2022 05:03:40 GMT  
		Size: 8.7 MB (8736375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc67df7fe6c230cc05e0045e22cfefe5383f1acaa64d97d01a38a49c652c1c2d`  
		Last Modified: Wed, 06 Apr 2022 05:03:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daecb8faf93c98e685c18550dec6213fe63a9f1abdd7102c0127feb31ec7991`  
		Last Modified: Wed, 06 Apr 2022 05:03:39 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
