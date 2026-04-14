## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:4b470a8b7a4fc4830bfddd9b54c1fff266c473cf9e87e3a7a20c2b090f53994e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:8e3b20831272d17bb2b028231b90de3deeadd375a8c7607d998a41681d9998e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.2 MB (431191030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4bdc58017357ecb32a5d899fe6b51c4a95726cde61615a2aedaf8a07f80d3cb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:57 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:57 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:48:55 GMT
ARG version=17.0.18.9-1
# Mon, 13 Apr 2026 22:48:55 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 13 Apr 2026 22:48:55 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:48:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 13 Apr 2026 23:42:47 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 13 Apr 2026 23:42:56 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 13 Apr 2026 23:42:56 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 13 Apr 2026 23:42:56 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:42:56 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:42:56 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 13 Apr 2026 23:42:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 13 Apr 2026 23:42:56 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 13 Apr 2026 23:42:56 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:42:56 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 13 Apr 2026 23:42:56 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 13 Apr 2026 23:42:56 GMT
ARG MAVEN_VERSION=3.9.14
# Mon, 13 Apr 2026 23:42:56 GMT
ARG USER_HOME_DIR=/root
# Mon, 13 Apr 2026 23:42:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 13 Apr 2026 23:42:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 13 Apr 2026 23:42:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841336e34bc21be90376dcd4366b4f047a142ba752a85812b67638d89d8c6388`  
		Last Modified: Mon, 13 Apr 2026 22:49:16 GMT  
		Size: 152.5 MB (152456080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31649b39f8644e6e194d0e5d735c4373f171bc311e2ae657c27761c1ac71b34b`  
		Last Modified: Mon, 13 Apr 2026 23:43:26 GMT  
		Size: 176.4 MB (176386400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a53282b4d687894a2d15faaf12999b1fdfb316c85cd44d898ec123cd05d0804`  
		Last Modified: Mon, 13 Apr 2026 23:43:23 GMT  
		Size: 30.1 MB (30081067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93485b6305d9a5e8a6ac92f8fd70b0742e2f92db6ec3f1a6b9e2b0d0cfbf265b`  
		Last Modified: Mon, 13 Apr 2026 23:43:22 GMT  
		Size: 9.3 MB (9311177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874bda490bc9c09f4d9d672c47979e247326b7a48211cd972ab73c03b11cb421`  
		Last Modified: Mon, 13 Apr 2026 23:43:21 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3548a462cd21639b9b528cd0356ac9759ae384b7e697f370e90196ebe2227ff9`  
		Last Modified: Mon, 13 Apr 2026 23:43:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:7b2d89e0278b3bf651d4f6f18aa34eaf6b881064485b802929cbe8aea79ac9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db83793c39ae862c2f9826581bddcbb340859c3e9f46d769652d30d85b506375`

```dockerfile
```

-	Layers:
	-	`sha256:0e75105a1ea1d10b450e3c3034c3f5dd0a49f0bbfe20dbe4ecdb07143d5659c4`  
		Last Modified: Mon, 13 Apr 2026 23:43:22 GMT  
		Size: 6.9 MB (6932346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f12c62c63c18890c7b88e0865bc21df538161396fffaa1e59e6eda1313f1d462`  
		Last Modified: Mon, 13 Apr 2026 23:43:21 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:17e42167c4f22dce611b77605f02e9bfd81427bc7d00c6b6005712e03a23d20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.2 MB (408215742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b671a378e0a1eaa670fdc668f1570f416f5f6b4e39feaa712b4beea0b9c1edc4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Apr 2026 22:22:09 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:22:09 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:11:23 GMT
ARG version=17.0.18.9-1
# Mon, 13 Apr 2026 23:11:23 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 13 Apr 2026 23:11:23 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:11:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 13 Apr 2026 23:55:51 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 13 Apr 2026 23:55:59 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 13 Apr 2026 23:55:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 13 Apr 2026 23:55:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:55:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:55:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 13 Apr 2026 23:55:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 13 Apr 2026 23:55:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 13 Apr 2026 23:55:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:55:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 13 Apr 2026 23:55:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 13 Apr 2026 23:55:59 GMT
ARG MAVEN_VERSION=3.9.14
# Mon, 13 Apr 2026 23:55:59 GMT
ARG USER_HOME_DIR=/root
# Mon, 13 Apr 2026 23:55:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 13 Apr 2026 23:55:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 13 Apr 2026 23:55:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968f8f47edb6f24de6d0822709352f2d91e9b9fce4050736f9c63c0870041431`  
		Last Modified: Mon, 13 Apr 2026 23:11:45 GMT  
		Size: 151.0 MB (150970875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fefa29b8c598814a0a84ded3b1b118ff1d0ffdc415a7a4fd94ffde6ab550b34`  
		Last Modified: Mon, 13 Apr 2026 23:56:25 GMT  
		Size: 151.9 MB (151932518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e813703ee019c70871cfae0cc27ef8d127da52d45a9e291c0651a9f0af497020`  
		Last Modified: Mon, 13 Apr 2026 23:56:22 GMT  
		Size: 31.2 MB (31197160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52573e74dbf330e4f5fcff17e2aa3234fd5007104cb2d50840f0fc020e1c932e`  
		Last Modified: Mon, 13 Apr 2026 23:56:22 GMT  
		Size: 9.3 MB (9311174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e97004e7775b01ddeaecb5a41d96e4d9aeca964028992be0b870f556f03a2a`  
		Last Modified: Mon, 13 Apr 2026 23:56:21 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2269fd01487ddf79f6a15433264fc8a6431dcc90f0f6394de1a03d25f282c50`  
		Last Modified: Mon, 13 Apr 2026 23:56:22 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:ce83dd940c8d41d727cebc0047db77ac2d62d36cc55457c48d6a2fdc4366f682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6948086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04b39219452ec99dbec8edff22bed9bc042666342499e5707ec00d8144d31cd`

```dockerfile
```

-	Layers:
	-	`sha256:c9e1a755c3e0c2268944ff05ca63913e3f2f432fb11c4d7c16e7859d2c3c939b`  
		Last Modified: Mon, 13 Apr 2026 23:56:21 GMT  
		Size: 6.9 MB (6929745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d8103f33cd5179bb6cd24cda82ab003962113476bdfd127e991e42554d773fc`  
		Last Modified: Mon, 13 Apr 2026 23:56:21 GMT  
		Size: 18.3 KB (18341 bytes)  
		MIME: application/vnd.in-toto+json
