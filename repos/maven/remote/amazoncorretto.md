## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:a3dfea22412e8f9a8e59304fdcea853fad913e1ca6354757a3892c3b275d1a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:bd7ef505fec1c6ad1c53fa4d686216843f8099576b631a0b70dbf56388ee9222
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306567754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e61fa733705971a401f625e759be4ab9eea5bc0ee54de4fe843585302c431ce`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 30 Jun 2020 20:20:04 GMT
ADD file:788af9048b1c163347d7a8349f8ecf5721b4d8b63395ec8c6ca6d0732f57acdd in / 
# Tue, 30 Jun 2020 20:20:05 GMT
CMD ["/bin/bash"]
# Tue, 30 Jun 2020 20:55:22 GMT
ARG version=11.0.7.10-1
# Tue, 30 Jun 2020 20:55:56 GMT
# ARGS: version=11.0.7.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 30 Jun 2020 20:55:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 30 Jun 2020 21:37:16 GMT
ARG MAVEN_VERSION=3.6.3
# Tue, 30 Jun 2020 21:37:17 GMT
ARG USER_HOME_DIR=/root
# Tue, 30 Jun 2020 21:37:17 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Tue, 30 Jun 2020 21:37:17 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Tue, 30 Jun 2020 21:37:30 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN yum install -y tar which gzip
# Tue, 30 Jun 2020 21:37:32 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 30 Jun 2020 21:37:32 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 30 Jun 2020 21:37:32 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 30 Jun 2020 21:37:32 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 30 Jun 2020 21:37:32 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 30 Jun 2020 21:37:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 30 Jun 2020 21:37:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3d24604292f287c31563b1f563e83307e7915909506659401fb07c1c3e6e164c`  
		Last Modified: Tue, 30 Jun 2020 20:21:31 GMT  
		Size: 61.7 MB (61684682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab273e3d40f4b0aa1d84e06a6acc3e2ce0ef6c02e4c57cbdbd8e782b81276308`  
		Last Modified: Tue, 30 Jun 2020 20:56:41 GMT  
		Size: 145.1 MB (145105822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77151a0aaf98a4fcc8724dee95680d2e44f326e1b6cca22590b9cfe663d049b0`  
		Last Modified: Tue, 30 Jun 2020 21:38:53 GMT  
		Size: 90.2 MB (90194819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f5549f0b4a1941b4877c70992040b4a0eaabec895e272e4e3690e7795211a5`  
		Last Modified: Tue, 30 Jun 2020 21:38:43 GMT  
		Size: 9.6 MB (9581221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2dc5dd950c35f651b2d4fc9d02f4006d8e6c43d2eb02a3f788d38373adb106`  
		Last Modified: Tue, 30 Jun 2020 21:38:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44262e96f29498fff0fbe755e47d706155ab2aa8f71d74f0f5462181f5ddadb6`  
		Last Modified: Tue, 30 Jun 2020 21:38:43 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1865fbb6f560fc589918f95df31792d32fd65fc4d3a814ad259f965916f73cd0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.3 MB (273262483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c061195f6526565b5b3509261fb8b16b90201016ae6b1ce1dbf9e413ff701a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 30 Jun 2020 21:59:07 GMT
ADD file:c597ed16b945b44bdc9a607ac9730b470dd169fb94a5ca4e000d07318157d4f8 in / 
# Tue, 30 Jun 2020 21:59:09 GMT
CMD ["/bin/bash"]
# Tue, 30 Jun 2020 23:33:41 GMT
ARG version=11.0.7.10-1
# Tue, 30 Jun 2020 23:34:16 GMT
# ARGS: version=11.0.7.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Tue, 30 Jun 2020 23:34:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 01 Jul 2020 00:06:51 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 01 Jul 2020 00:06:51 GMT
ARG USER_HOME_DIR=/root
# Wed, 01 Jul 2020 00:06:52 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 01 Jul 2020 00:06:53 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Wed, 01 Jul 2020 00:07:06 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN yum install -y tar which gzip
# Wed, 01 Jul 2020 00:07:10 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 01 Jul 2020 00:07:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 01 Jul 2020 00:07:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 01 Jul 2020 00:07:12 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 01 Jul 2020 00:07:13 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 01 Jul 2020 00:07:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 01 Jul 2020 00:07:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6c0fd36c9881cb99dbcd7fe98cfd04a4a653e35c4c1195b7cb7d339eaec9dd79`  
		Last Modified: Tue, 30 Jun 2020 22:00:22 GMT  
		Size: 63.2 MB (63163782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daab62318288a0701ecd7841a45ef6f0e4588c0f5b686fb375f3347826005bdf`  
		Last Modified: Tue, 30 Jun 2020 23:35:19 GMT  
		Size: 144.0 MB (143967434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5fa23269e617b498a5c69d30386b361cae5cca48ab16be9f03a326e2abfed33`  
		Last Modified: Wed, 01 Jul 2020 00:08:27 GMT  
		Size: 56.5 MB (56548842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b031d580e9f805556a8c59b5b6526080af0980b7783aee5c6269832f1b3a49`  
		Last Modified: Wed, 01 Jul 2020 00:08:17 GMT  
		Size: 9.6 MB (9581211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb0854f563fe169e791ebdafb3c4487c0ce2082afa76db688a2ffcf7c1a34ca`  
		Last Modified: Wed, 01 Jul 2020 00:08:15 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de62e9d8305faadbe63197dfbde91f7470ddb1a28d3a0a3ecf83c65ad1bde943`  
		Last Modified: Wed, 01 Jul 2020 00:08:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
