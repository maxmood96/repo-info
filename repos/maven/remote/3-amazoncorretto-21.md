## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:ac4a9980f3fd8805e0bab5553eb17a2317a33003deb434839bc1d550669fb683
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:76955c8eb612950dcec0ddfa18cc20551b0546b19d28587ed20a6209f59de6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.0 MB (416017009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48aa0861c9f5e8e969ab961b8358dbace36fd7efb2a3f368ed46534f921ebee`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31392d7ddaaf1b0a5a2312e768716ba381912bc41f814ef2a3e7e3a0ea9f9f5`  
		Last Modified: Sat, 07 Sep 2024 01:05:55 GMT  
		Size: 165.8 MB (165819543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5da44fb171f72b8f02679c7e4bd1bea2dcb902a5e04f2873e2eeaf8fc614a5d`  
		Last Modified: Tue, 17 Sep 2024 03:02:51 GMT  
		Size: 148.2 MB (148244459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b18c807648d7a471c2afb36c3f72028057f512fa48bcf89cc2a8e72737da3a`  
		Last Modified: Tue, 17 Sep 2024 03:02:50 GMT  
		Size: 30.1 MB (30085983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d14a854f1b6767e44fdc256d0b5e9c34f7c65947727b81ef4b855c6dfc6a06`  
		Last Modified: Tue, 17 Sep 2024 03:02:50 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5a114acd4b279779dc5142d96913c1529ead65e6392238d8e52b0088d284ca`  
		Last Modified: Tue, 17 Sep 2024 03:02:50 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66576de374d6207976c53028fa7278edf6d4d6d52fc3d1ae4e235d3100e8cd78`  
		Last Modified: Tue, 17 Sep 2024 03:02:51 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:5926d78992bffb4ce9452d436d086797109cb0b26161a54713d9f1711748bfec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb89f78c81c918ec644ff3c367c18681bb455e63a845cef54a31625046ab476c`

```dockerfile
```

-	Layers:
	-	`sha256:98f4aa8a6dfe5898f123eb577d01ed5547246c08f3fe78a85f4b66e53b36607e`  
		Last Modified: Tue, 17 Sep 2024 03:02:50 GMT  
		Size: 2.0 KB (2021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa7abd08d9aa3347237f9e3f9eec59416eec62c4a24d2e09be5166046be658ed`  
		Last Modified: Tue, 17 Sep 2024 03:02:50 GMT  
		Size: 18.2 KB (18195 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0ea739072a1713a2ee0d886cf14a8579b6ce95bfc004f9ab0b99ea33902c78b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.0 MB (393029355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5d03d12578b5a4a0557cc47b17e818b623b0bc25cbe29bd46f883ce4d5b2b1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0f0968c920788bb8a898446e0bbe8ea6b11fcbf7f55810ef51044775a045d6c9`  
		Last Modified: Fri, 06 Sep 2024 18:59:50 GMT  
		Size: 64.6 MB (64586343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccb17f585e623ab3c6d7898c58a94c2ecc6aac965f9d369b9389bfafa591557`  
		Last Modified: Sat, 07 Sep 2024 13:26:49 GMT  
		Size: 163.8 MB (163820593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b59daed8e456591f0381d603da22a8b184d41cd95ee1a3d07c239f9bc59923`  
		Last Modified: Tue, 17 Sep 2024 09:47:18 GMT  
		Size: 124.3 MB (124283017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95624650c2b66942ed3223dadac501bec7816c46a7542fae4eb72d766e922e83`  
		Last Modified: Tue, 17 Sep 2024 09:47:16 GMT  
		Size: 31.2 MB (31167913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f45ccf05ee8ff669ec6bbac35d40063146de6bdc442f8e9fce1b8b947eea952`  
		Last Modified: Tue, 17 Sep 2024 09:47:16 GMT  
		Size: 9.2 MB (9170448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6cd5d0407513b22c9d7c6da6316c433c30b121364977ee230c3fe577e04b50`  
		Last Modified: Tue, 17 Sep 2024 09:47:15 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d260f1d2b89f32f9e2ced6929e7781a8677ddc0466e930ae61cad6a8ef38e56`  
		Last Modified: Tue, 17 Sep 2024 09:47:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:d9b92b157b188432643854f8851c9f29b52076da8f5c8b1ab8537bd39a019bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6933008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e220010d640ad01f3e30c9b0238a2fd3840a53a9ddfb8e2fdaace1c92a6c08fd`

```dockerfile
```

-	Layers:
	-	`sha256:204bf753a4c74f70056ab6468541543c466a7b18927c8a652ef17872a3f85835`  
		Last Modified: Tue, 17 Sep 2024 09:47:16 GMT  
		Size: 6.9 MB (6914087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:944ec4cdf9629bb43951bd5a2bbf4b741d5277a262bf95bccafbc13e15db68bf`  
		Last Modified: Tue, 17 Sep 2024 09:47:15 GMT  
		Size: 18.9 KB (18921 bytes)  
		MIME: application/vnd.in-toto+json
