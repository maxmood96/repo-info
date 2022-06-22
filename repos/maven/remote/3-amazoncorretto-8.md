## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:594e42438ca4435aeee2b4a8658c00398201702d96bd876b8cd355fcd86c988d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:b2723484c334573528723ff7a04c6f900b7f8d4ee6faaac8c4b890955bb1ed9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150233318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3f7eb1662b60179c5bdffdc2b4598afe2f4123c1012d34f73156f01bfe801a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Jun 2022 23:19:41 GMT
ADD file:e6c6bb016423b24a28b273cc76e9fbbf81934b77a0ede797ccfd0eeac465c8a4 in / 
# Tue, 21 Jun 2022 23:19:42 GMT
CMD ["/bin/bash"]
# Wed, 22 Jun 2022 00:02:40 GMT
ARG version=1.8.0_332.b08-1
# Wed, 22 Jun 2022 00:03:00 GMT
# ARGS: version=1.8.0_332.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 22 Jun 2022 00:03:01 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jun 2022 00:03:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 22 Jun 2022 02:40:01 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 22 Jun 2022 02:40:01 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 22 Jun 2022 02:40:02 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Jun 2022 02:40:02 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 22 Jun 2022 02:40:02 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 22 Jun 2022 02:40:10 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 22 Jun 2022 02:40:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Jun 2022 02:40:10 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Jun 2022 02:40:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 22 Jun 2022 02:40:10 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 22 Jun 2022 02:40:10 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 22 Jun 2022 02:40:10 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Jun 2022 02:40:10 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:017c82d6391f0bf122516eac436a6e8d77ac13282fdd13dde7e7e47dc71d447e`  
		Last Modified: Wed, 15 Jun 2022 22:09:36 GMT  
		Size: 62.3 MB (62294977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504fd3bb327abb1ba634205d36672fa60af3ec2599a14ab4767fc3c338021cdd`  
		Last Modified: Wed, 22 Jun 2022 00:06:41 GMT  
		Size: 75.6 MB (75567456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a70eb5b09bff96b0ed8bb1e56db633aea58d1e52de139ec4aeb5196dbd2bb05`  
		Last Modified: Wed, 22 Jun 2022 02:42:52 GMT  
		Size: 3.6 MB (3630170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3788e9ccb390a3ec6c8a1b4cc3c1b58d45bdad1d24f745492b9b9bfcaa5bfb85`  
		Last Modified: Wed, 22 Jun 2022 02:42:52 GMT  
		Size: 8.7 MB (8739500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c21df3ce707b84ba1c67953156326e48f0286935f247c1edc0814ec2739a889`  
		Last Modified: Wed, 22 Jun 2022 02:42:51 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b64d2d88fd42843d210e44ce227099d8065c0de7716c17e4c9571c2b4a92605`  
		Last Modified: Wed, 22 Jun 2022 02:42:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:dbe2aa8cabdbb15be39a70e551e428874ddf9a87a4982011a0eb8f032ca0ffdf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135895172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6780d2371f1f9720523f8a3f6cc65608e8dac31e81fc20fe3917bb7d4fcfb543`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 03 May 2022 22:39:32 GMT
ADD file:c351a8c80719ef38e02c26849f50bb7d79c24a6347cc2a72ae1a0768964bd113 in / 
# Tue, 03 May 2022 22:39:34 GMT
CMD ["/bin/bash"]
# Wed, 04 May 2022 00:20:54 GMT
ARG version=1.8.0_332.b08-1
# Wed, 04 May 2022 00:21:08 GMT
# ARGS: version=1.8.0_332.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 04 May 2022 00:21:09 GMT
ENV LANG=C.UTF-8
# Wed, 04 May 2022 00:21:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 04 May 2022 00:43:06 GMT
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Wed, 15 Jun 2022 18:46:22 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 15 Jun 2022 18:46:23 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Jun 2022 18:46:24 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 15 Jun 2022 18:46:25 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 15 Jun 2022 18:46:28 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 15 Jun 2022 18:46:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Jun 2022 18:46:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Jun 2022 18:46:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 15 Jun 2022 18:46:33 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 15 Jun 2022 18:46:34 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 15 Jun 2022 18:46:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Jun 2022 18:46:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ec3b4c26678b188d3874bed5e14dd278311fc05c81e418d5f0da36ec38d9f488`  
		Last Modified: Tue, 03 May 2022 03:07:52 GMT  
		Size: 63.9 MB (63902179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72bda41d7e098c0ba578a1fb4533ac66008d9fba9666925b381d8f01a01266f`  
		Last Modified: Wed, 04 May 2022 00:23:15 GMT  
		Size: 59.6 MB (59606423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b72aa4519248ec2b5d899c80f20701011b89ed98a496b45c002a28a35b6042a`  
		Last Modified: Wed, 04 May 2022 00:46:51 GMT  
		Size: 3.6 MB (3645878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec3e67b79374d9276701e081825deeabf2f01bb89920c0dfbff6c339d27605f`  
		Last Modified: Wed, 15 Jun 2022 18:55:04 GMT  
		Size: 8.7 MB (8739477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bada254067f88d65cf1354fcee4e305a55c2c970f9da1d31a867c47750deb7`  
		Last Modified: Wed, 15 Jun 2022 18:55:03 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e337c4f585553cf4a16633dd69b96e675cee36dd028c9cb8205729448d1b89c`  
		Last Modified: Wed, 15 Jun 2022 18:55:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
