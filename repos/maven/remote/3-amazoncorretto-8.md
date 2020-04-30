## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:dd8528d1e7aa9c70b4ff765895738a0c8bf35b6939469689655f8dffd1b2c18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:a0eb43bb3efd723a02e46595c1d383a3e12e0ae5bf83be9f65f1d88f13c5861c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231416064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f52a3109a2c42af43304f3365b635bbb02bda8252930316377cbea258fdf46a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Apr 2020 18:22:56 GMT
ADD file:c64a7d77d1e9f4364c8d2009059cb8668697d61f54f457215b6be6f0c9cded5b in / 
# Tue, 21 Apr 2020 18:22:56 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2020 18:51:00 GMT
ARG version=1.8.0_252.b09-1
# Wed, 29 Apr 2020 23:19:56 GMT
# ARGS: version=1.8.0_252.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 29 Apr 2020 23:19:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 29 Apr 2020 23:55:39 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 29 Apr 2020 23:55:39 GMT
ARG USER_HOME_DIR=/root
# Wed, 29 Apr 2020 23:55:40 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 29 Apr 2020 23:55:40 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Wed, 29 Apr 2020 23:55:51 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN yum install -y tar which gzip
# Wed, 29 Apr 2020 23:55:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 29 Apr 2020 23:55:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 29 Apr 2020 23:55:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 29 Apr 2020 23:55:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 29 Apr 2020 23:55:55 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 29 Apr 2020 23:55:55 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 29 Apr 2020 23:55:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 29 Apr 2020 23:55:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a3f8e652bdc470bbea38766fe41f8f12b9e4d44e9ce4037eb502839754b06b9c`  
		Last Modified: Tue, 21 Apr 2020 18:23:48 GMT  
		Size: 61.6 MB (61619066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b699171c4297c4e4464370fa7c9786475c8dba7e5afc538dabc7911b316b1a5d`  
		Last Modified: Wed, 29 Apr 2020 23:20:48 GMT  
		Size: 74.3 MB (74281751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705555d8aa0428e3001d78a9ae31c7af30339637415d65f08fcea4c5f755898c`  
		Last Modified: Wed, 29 Apr 2020 23:58:14 GMT  
		Size: 85.9 MB (85932782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2558f37731f044937d64771b4532b4b0cec54f8a40a5ed97e12c85f942a96a`  
		Last Modified: Wed, 29 Apr 2020 23:57:11 GMT  
		Size: 9.6 MB (9581250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2342071d08cda47f8ddc3b9147b11a6ac85150b368ab40a30e33f7471564dc`  
		Last Modified: Wed, 29 Apr 2020 23:57:10 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3ad48bad466d4d49bff75a819e1c7878c40430a757bee8452a01827c7aed48`  
		Last Modified: Wed, 29 Apr 2020 23:57:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9dfec1baddfc74e47c28fbf7a096fde376cac0eab710bb160540c6be20953d57
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183083531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd112683138fceea0f6065ebf484edd069d69f26be3ca0d866af3a5aa4854002`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Apr 2020 18:58:16 GMT
ADD file:85fc0908f460f80c41755d2b5ab9ff6a025bb2726628ccc4edceb21d2e3f8edf in / 
# Tue, 21 Apr 2020 18:58:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2020 19:26:04 GMT
ARG version=1.8.0_252.b09-1
# Wed, 29 Apr 2020 23:40:17 GMT
# ARGS: version=1.8.0_252.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 29 Apr 2020 23:40:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 29 Apr 2020 23:58:29 GMT
ARG MAVEN_VERSION=3.6.3
# Wed, 29 Apr 2020 23:58:30 GMT
ARG USER_HOME_DIR=/root
# Wed, 29 Apr 2020 23:58:30 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Wed, 29 Apr 2020 23:58:31 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Wed, 29 Apr 2020 23:58:44 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN yum install -y tar which gzip
# Wed, 29 Apr 2020 23:58:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 29 Apr 2020 23:58:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 29 Apr 2020 23:58:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 29 Apr 2020 23:58:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 29 Apr 2020 23:58:57 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 29 Apr 2020 23:58:57 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 29 Apr 2020 23:58:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 29 Apr 2020 23:58:58 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0a37a5cd26f245ce54aff575389ef7765520d37d3ea7c437144c936c6adffc8a`  
		Last Modified: Tue, 21 Apr 2020 18:59:54 GMT  
		Size: 63.1 MB (63079760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579fa6a1efa0bc56a162e59988223b67e1d33fb64d1a863e42a9a64dd4a00958`  
		Last Modified: Wed, 29 Apr 2020 23:41:28 GMT  
		Size: 58.3 MB (58325222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887c45fd96478beea375fdf5c4577eab723ddd26b514f75cfd38c15d44d1312`  
		Last Modified: Thu, 30 Apr 2020 00:00:00 GMT  
		Size: 52.1 MB (52096125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c633412afd2f66531d5389741c574d3308675eab15a91da140e01bea1889a0d`  
		Last Modified: Wed, 29 Apr 2020 23:59:50 GMT  
		Size: 9.6 MB (9581209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ce80d61f30cd00916d637f6db16300ec0375f61a9a94cc63a3aac1337a5c94`  
		Last Modified: Wed, 29 Apr 2020 23:59:48 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf92c9d895e50353801f773c1dfc6a8b4044390bd6541a0e4ef4aa0bd28fc30`  
		Last Modified: Wed, 29 Apr 2020 23:59:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
