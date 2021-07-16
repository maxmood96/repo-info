## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:85deca70c9aa4869e78251d9369deb486aa79d8d45a8aeb3b22bc4285594d908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:c6e2c405139029a8a56e4e9ccc490b38d49e9466a71fa7b643a2342016e9d072
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221850593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f21fbc4613c231cb9736cc14e0cc458af4880de77ab2cc0db4aa5ac4270c96`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jul 2021 23:38:14 GMT
ADD file:87c0c8c13a50d18c9b35e048d635d04fcd6fc06e9416c68a5c3024c83b166177 in / 
# Thu, 15 Jul 2021 23:38:15 GMT
CMD ["/bin/bash"]
# Fri, 16 Jul 2021 00:33:07 GMT
ARG version=11.0.11.9-1
# Fri, 16 Jul 2021 00:33:30 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 16 Jul 2021 00:33:31 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jul 2021 00:33:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 16 Jul 2021 01:10:25 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 16 Jul 2021 01:10:25 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jul 2021 01:10:25 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 16 Jul 2021 01:10:26 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 16 Jul 2021 01:10:35 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 16 Jul 2021 01:10:42 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 16 Jul 2021 01:10:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jul 2021 01:10:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jul 2021 01:10:43 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 16 Jul 2021 01:10:43 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 16 Jul 2021 01:10:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jul 2021 01:10:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:430235fb155c55a4e5a8c494a918c1d1bf2473e93cc35c4242ae089785dc1a42`  
		Last Modified: Fri, 09 Jul 2021 13:29:48 GMT  
		Size: 62.0 MB (61966006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a3fc4711644454fbc9851b78f9c371b21a34549e0c5cfb9136c6faaef71e7c`  
		Last Modified: Fri, 16 Jul 2021 00:35:28 GMT  
		Size: 146.7 MB (146678002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f51757276e056448d9fccb3b562c37af8a225a0d76428c928666832c2fd625`  
		Last Modified: Fri, 16 Jul 2021 01:13:47 GMT  
		Size: 3.6 MB (3594429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa339bd342384ee244478b8448ac1427ec224ee39e7ca5bb44801bb98ba3ac72`  
		Last Modified: Fri, 16 Jul 2021 01:13:47 GMT  
		Size: 9.6 MB (9610944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc16e498bf6088b0037b027f1c4bbcbf5d8f240b2be7e8b4cd961d14effbbe33`  
		Last Modified: Fri, 16 Jul 2021 01:13:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019fca845ddc3a9c9323585a3394b6dcdae3156ea954fee2f9d52ff51702483b`  
		Last Modified: Fri, 16 Jul 2021 01:13:46 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6c7919799a529a7ea2631cec0ce1f742cb031b7b4b441fcde3409595f0fa982a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221525642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9515a6cfdc61e0f27de240629e7898117e423cecd14cac4cd964cd132c88f703`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 16 Jul 2021 00:09:26 GMT
ADD file:555fe2ebaf4a5e69a533b39ac234d3f7c6d7de6333e2882558b1b92f1320c8a9 in / 
# Fri, 16 Jul 2021 00:09:27 GMT
CMD ["/bin/bash"]
# Fri, 16 Jul 2021 00:39:30 GMT
ARG version=11.0.11.9-1
# Fri, 16 Jul 2021 00:39:58 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 16 Jul 2021 00:39:58 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jul 2021 00:39:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 16 Jul 2021 01:05:52 GMT
ARG MAVEN_VERSION=3.8.1
# Fri, 16 Jul 2021 01:05:52 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jul 2021 01:05:52 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Fri, 16 Jul 2021 01:05:52 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Fri, 16 Jul 2021 01:06:01 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Fri, 16 Jul 2021 01:06:03 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 16 Jul 2021 01:06:03 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jul 2021 01:06:03 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jul 2021 01:06:04 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 16 Jul 2021 01:06:04 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 16 Jul 2021 01:06:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jul 2021 01:06:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6bc2b81b61fecbd717658fab4af4ed0a6b9e5a2e28323439c47d57a34db1908f`  
		Last Modified: Fri, 16 Jul 2021 00:10:24 GMT  
		Size: 63.6 MB (63567892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c303754cf668ab4480ec5b49db7d581120ef9d4abe16449f1dbe54eaec133f`  
		Last Modified: Fri, 16 Jul 2021 00:42:05 GMT  
		Size: 144.8 MB (144752643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc230e0509436add9e2831a0836dcf1d60130ee62345293dbf8ea3c01f06e0b`  
		Last Modified: Fri, 16 Jul 2021 01:10:46 GMT  
		Size: 3.6 MB (3592929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e03c1c4d125bde5a80353d84fca6344bb20216db8f8c7606ef08eb06898843`  
		Last Modified: Fri, 16 Jul 2021 01:10:46 GMT  
		Size: 9.6 MB (9610965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f5930a94bef7169263f8359ae6cb6ac6d5a64dbe4ad7521276b27e663bdc0`  
		Last Modified: Fri, 16 Jul 2021 01:10:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90173c61c6c33f7a1967bc9074f8da140e4d08ee24ab0c41f19856bb2b76dca2`  
		Last Modified: Fri, 16 Jul 2021 01:10:45 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
