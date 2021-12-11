## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:99f210a0259426d1d5c55419ce1db7d02f58122aa476bd787df67be25523eca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:334bd4a081f9631beaee7b3969c177e5bdb23f560f67bea22b39984fdb821032
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150187468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25e17138b3b11ec08a05eb9eed403dc76c43dc38dd8af93bf2f58719d64e9e0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 02 Dec 2021 23:20:03 GMT
ADD file:4eca58da351122eac20ffd87e3af2c0313089cb81650bdd4c2ef95a556fb842a in / 
# Thu, 02 Dec 2021 23:20:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Dec 2021 21:51:33 GMT
ARG version=1.8.0_312.b07-1
# Fri, 10 Dec 2021 23:26:39 GMT
# ARGS: version=1.8.0_312.b07-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 10 Dec 2021 23:26:39 GMT
ENV LANG=C.UTF-8
# Fri, 10 Dec 2021 23:26:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 11 Dec 2021 00:16:06 GMT
ARG MAVEN_VERSION=3.8.4
# Sat, 11 Dec 2021 00:16:06 GMT
ARG USER_HOME_DIR=/root
# Sat, 11 Dec 2021 00:16:06 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Sat, 11 Dec 2021 00:16:07 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Sat, 11 Dec 2021 00:16:16 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Sat, 11 Dec 2021 00:16:22 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 11 Dec 2021 00:16:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 11 Dec 2021 00:16:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 11 Dec 2021 00:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 11 Dec 2021 00:16:23 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 11 Dec 2021 00:16:24 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 11 Dec 2021 00:16:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 11 Dec 2021 00:16:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8b8a142162d22658bdf0283afcd00a9dd216c6637943ffe5f2ba53c4e3da0bd9`  
		Last Modified: Thu, 02 Dec 2021 06:01:08 GMT  
		Size: 62.1 MB (62090346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d1e37b8bd9515171ba007aa352f13b0ccf0ea7aaf95a135ba3b96e27d65761`  
		Last Modified: Fri, 10 Dec 2021 23:29:46 GMT  
		Size: 75.4 MB (75369831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aacd8bfe3edf3e222b73a71a90ba7d5bb0f4b7d9c9cc14bf1a4ed9683b0a6b5`  
		Last Modified: Sat, 11 Dec 2021 00:18:42 GMT  
		Size: 3.6 MB (3616262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b69a5bfa4f99b3660c3cba229bbcfa8338340f2cdb2105566aa40bf21fd88d7`  
		Last Modified: Sat, 11 Dec 2021 00:18:43 GMT  
		Size: 9.1 MB (9109817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e70571a585daeed7e639ff07ee417ecc17129b5a50f3236d56a60e85c3993f`  
		Last Modified: Sat, 11 Dec 2021 00:18:42 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4503693ca866e77141356236d0cad8bbfa2005ca4735d009c442f62335863ab`  
		Last Modified: Sat, 11 Dec 2021 00:18:42 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6ed0ec8c6646ea447cf43134ad4c7c28f16b7f9040a5f2b9e88e80b90719a45a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135815916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b9c83d08b037a19c4f0019c1ad8f18a228546edc3ca6253845aaa0588c71d9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 02 Dec 2021 21:25:17 GMT
ADD file:1f2ecfca149ab81a0527241077c1b366afd95b6b7a1dd91bddfd6c40988ba994 in / 
# Thu, 02 Dec 2021 21:25:18 GMT
CMD ["/bin/bash"]
# Fri, 03 Dec 2021 16:53:43 GMT
ARG version=1.8.0_312.b07-1
# Sat, 11 Dec 2021 00:12:56 GMT
# ARGS: version=1.8.0_312.b07-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 11 Dec 2021 00:12:56 GMT
ENV LANG=C.UTF-8
# Sat, 11 Dec 2021 00:12:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 11 Dec 2021 00:33:18 GMT
ARG MAVEN_VERSION=3.8.4
# Sat, 11 Dec 2021 00:33:19 GMT
ARG USER_HOME_DIR=/root
# Sat, 11 Dec 2021 00:33:20 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Sat, 11 Dec 2021 00:33:21 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Sat, 11 Dec 2021 00:33:26 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Sat, 11 Dec 2021 00:33:41 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 11 Dec 2021 00:33:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 11 Dec 2021 00:33:42 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 11 Dec 2021 00:33:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 11 Dec 2021 00:33:45 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 11 Dec 2021 00:33:46 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 11 Dec 2021 00:33:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 11 Dec 2021 00:33:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:74f9a6be36f3bc3bf6041c40376d548e3a8b720a0455674b19e9174a9e567078`  
		Last Modified: Thu, 02 Dec 2021 21:26:12 GMT  
		Size: 63.7 MB (63692547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583396cb1c34c851d7bace2bef7c3aefceb8289f97c3696a9bd75ea3cbda1783`  
		Last Modified: Sat, 11 Dec 2021 00:14:34 GMT  
		Size: 59.4 MB (59421680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366509013a43cfb76eaf4c15ea98395029dda21515d3306a3290c3d391dc58e`  
		Last Modified: Sat, 11 Dec 2021 00:37:13 GMT  
		Size: 3.6 MB (3590698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afd21f67241f3a0794ff0ef242034c4b0e77fb196704e5e2929537684d5ea1e`  
		Last Modified: Sat, 11 Dec 2021 00:37:13 GMT  
		Size: 9.1 MB (9109778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93846f7adaf354b90592adafe748f0a4313c59fe5ff87abdc0bfa504086a7d1`  
		Last Modified: Sat, 11 Dec 2021 00:37:12 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea5c2e392a6e1baf25cb0bde3760d93db188ae06f5aba6152565d7f3a3e8cdf`  
		Last Modified: Sat, 11 Dec 2021 00:37:12 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
