## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:eb78866161d0ab2cb7c885e08b8e6c5fbdb98c1d62ad360e99ee3b675f9ead58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:89a977292d9f7f7373b64d2f0793e671f270d5275312ace0cf829a1559ba7999
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221820801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79b69cfca1d243e9f1c01c886450b816f904b34a03388cb39bada40445d48c9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 29 Apr 2021 22:25:37 GMT
ADD file:47fcf0318dccec16b61a0d21a0f16c45b77dea5abf50ba6604f1ffadcb299d10 in / 
# Thu, 29 Apr 2021 22:25:38 GMT
CMD ["/bin/bash"]
# Thu, 29 Apr 2021 22:44:48 GMT
ARG version=11.0.11.9-1
# Thu, 29 Apr 2021 22:45:13 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 29 Apr 2021 22:45:13 GMT
ENV LANG=C.UTF-8
# Thu, 29 Apr 2021 22:45:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 29 Apr 2021 23:12:35 GMT
ARG MAVEN_VERSION=3.8.1
# Thu, 29 Apr 2021 23:12:35 GMT
ARG USER_HOME_DIR=/root
# Thu, 29 Apr 2021 23:12:35 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Thu, 29 Apr 2021 23:12:35 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Thu, 29 Apr 2021 23:12:45 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Thu, 29 Apr 2021 23:12:47 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 29 Apr 2021 23:12:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 29 Apr 2021 23:12:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 29 Apr 2021 23:12:48 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 29 Apr 2021 23:12:48 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 29 Apr 2021 23:12:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 29 Apr 2021 23:12:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3c2c91c7c4311eca863331479504040ee4f45fda9a610947b82886e7bbd5b737`  
		Last Modified: Thu, 29 Apr 2021 22:27:18 GMT  
		Size: 61.9 MB (61947132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17eb3d153b3376801c1da7fc410637e77e5b7e2891bf6e58d32dc6a02ab1473a`  
		Last Modified: Thu, 29 Apr 2021 22:47:15 GMT  
		Size: 146.7 MB (146668563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179994bcd834bdfde319f4ea4cbdf4cf836ab62bca89025b19bee3f639bcc35f`  
		Last Modified: Thu, 29 Apr 2021 23:15:39 GMT  
		Size: 3.6 MB (3592934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16ff32b04d5e5fa321b6be59805d02e9227eefb2d497344a3a5a24d9123f566`  
		Last Modified: Thu, 29 Apr 2021 23:15:39 GMT  
		Size: 9.6 MB (9610963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c234d73ccfcad32f2217017cda7c8445e4ae7b81351a9efa546b98e1a64267f`  
		Last Modified: Thu, 29 Apr 2021 23:15:38 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8186dfe8f88b53d295e4bb834ef088d5f2e2a9a54e47fb961a488a39aa8dd82c`  
		Last Modified: Thu, 29 Apr 2021 23:15:38 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7781d47c9974c8cab293402d017c068ab8aa2ae4783060b7084a0aad64276e07
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 MB (221603855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d99e330544d36ead1601d3089a46febc975aecc1da10857bb82582037b322d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 29 Apr 2021 22:40:32 GMT
ADD file:03605b69274d89b78234df03d53dacc9cac408d68b82b1fb5d63b84c01b69300 in / 
# Thu, 29 Apr 2021 22:40:37 GMT
CMD ["/bin/bash"]
# Thu, 29 Apr 2021 22:59:09 GMT
ARG version=11.0.11.9-1
# Thu, 29 Apr 2021 22:59:48 GMT
# ARGS: version=11.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Thu, 29 Apr 2021 22:59:50 GMT
ENV LANG=C.UTF-8
# Thu, 29 Apr 2021 22:59:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 29 Apr 2021 23:40:33 GMT
ARG MAVEN_VERSION=3.8.1
# Thu, 29 Apr 2021 23:40:34 GMT
ARG USER_HOME_DIR=/root
# Thu, 29 Apr 2021 23:40:35 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Thu, 29 Apr 2021 23:40:36 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Thu, 29 Apr 2021 23:40:48 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN yum install -y tar which gzip   && rm -rf /var/cache/yum/*   && yum clean all
# Thu, 29 Apr 2021 23:40:59 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 29 Apr 2021 23:41:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 29 Apr 2021 23:41:01 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 29 Apr 2021 23:41:02 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 29 Apr 2021 23:41:03 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 29 Apr 2021 23:41:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 29 Apr 2021 23:41:05 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:316be4ce82c0add9f71a6ce1face38b99f456abd45232cf7ad96ccac098ef5fe`  
		Last Modified: Thu, 29 Apr 2021 22:41:52 GMT  
		Size: 63.7 MB (63660068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95858667f8940b79869dc419ce2be62c27d5e0291f6dfd0e8829db451947c2d`  
		Last Modified: Thu, 29 Apr 2021 23:01:52 GMT  
		Size: 144.7 MB (144746424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836dfac2722df497ffcfdc3ed3e20c3291b8747c17244de69a303bb59b653787`  
		Last Modified: Thu, 29 Apr 2021 23:44:09 GMT  
		Size: 3.6 MB (3585194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9779738e6e5437e1212ace62ad53a896c8f60a49925cdcd19bef7d94a6325ad5`  
		Last Modified: Thu, 29 Apr 2021 23:44:09 GMT  
		Size: 9.6 MB (9610957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70aa63c03a3eeafab9636fdff60ff7b1a43a132ac1a1a5a4999eb8c36fb36e31`  
		Last Modified: Thu, 29 Apr 2021 23:44:08 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e17db4c70b76d60097cbe32908a2b0408a2c181fe51c84993d3bfb2e5323298`  
		Last Modified: Thu, 29 Apr 2021 23:44:08 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
