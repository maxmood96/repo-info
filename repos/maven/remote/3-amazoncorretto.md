## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:6458e0960206ab5b65b84c0dcf68a8e6587798c39796e1923de05f60fcee060a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:626c9a6939fce973bf51a541c55b63a7e5078ce864b2b86406c543e051fafc9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 MB (398370813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f9e117f64e9199041041a6db688ec6a8eda3a6aa32c21aee47cdf37a271500`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:58bb137858502de3ba6195f39c5c12f1e4303651c580b206205fa863d5c0c343`  
		Last Modified: Sat, 07 Sep 2024 01:05:57 GMT  
		Size: 148.2 MB (148176921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13dd9cda1d515a9611c81e6c3575cf688f5f922f1d1eaedc5513ea0811203e7a`  
		Last Modified: Tue, 17 Sep 2024 03:03:00 GMT  
		Size: 148.2 MB (148244501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5ed6425d1407c2554a9877ac4c831f5961ec0de4995c783475223f002b15f1`  
		Last Modified: Tue, 17 Sep 2024 03:02:58 GMT  
		Size: 30.1 MB (30082359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db328fdb83abcb6755f35d04a6b18432312d7b662ebeb0c427231f6879b7480`  
		Last Modified: Tue, 17 Sep 2024 03:02:58 GMT  
		Size: 9.2 MB (9170443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2698721488f1fc60c56e54bdd75e15c0eefcad59f38edfd547d5943af6f410f4`  
		Last Modified: Tue, 17 Sep 2024 03:02:57 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df440de9afa7063b599970c86eb6697c23e33daa5899e75d51823c0772b3bfa1`  
		Last Modified: Tue, 17 Sep 2024 03:02:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:53f0ad91e1fa4d2b85d00f8ea2febb1c5b20e17840efbf0326d4940749c979b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6944849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585d89b96a33be9aec0e774ecbcd3f0b7f38dc789e3a337b97fbd7a0bc155478`

```dockerfile
```

-	Layers:
	-	`sha256:3c4ade3c8a3df8f32d19c5ba75715fed974b5c972634aa1ec0e7b54620061e14`  
		Last Modified: Tue, 17 Sep 2024 03:02:58 GMT  
		Size: 6.9 MB (6925381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a91b8394e7ca5088cfe83e356ec9f39f14dcebfa5a32c7438dda02d730d9e4a0`  
		Last Modified: Tue, 17 Sep 2024 03:02:57 GMT  
		Size: 19.5 KB (19468 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6256e981d7804ad72e9db66074670ab2746b129b2c8737ec88a6da727eff1e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.5 MB (374459648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba1c84031b9b23876431f758ca283a8ef717ca2bc137bd31bd4a7ed5a00ba44`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:cdb3fe1f403f0830206c1222f8dcae6c885401b65b5e2d386c6e9c7399f5e732`  
		Last Modified: Sat, 07 Sep 2024 13:12:18 GMT  
		Size: 145.3 MB (145250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79b5d1b6147545df9a1262d369df8e274c69017452e2985f18be61e34111363`  
		Last Modified: Sat, 07 Sep 2024 14:52:32 GMT  
		Size: 124.3 MB (124281961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd7bcc4ebf63c84b47b981f52a8ac8306b09aeaf8aeff1604c3e431d6fa6d36`  
		Last Modified: Sat, 07 Sep 2024 14:52:29 GMT  
		Size: 31.2 MB (31169189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9a8635936c10b52180f82b1f07c2cb9b50138b32e97833d983de548326c18f`  
		Last Modified: Sat, 07 Sep 2024 14:52:29 GMT  
		Size: 9.2 MB (9170440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3f2acf47b2b925201a2e7a8b62c370886288d3f18113acf00cd2ab592de2fc`  
		Last Modified: Sat, 07 Sep 2024 14:52:29 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a954787a93f4c9b78b3a1a237fd81ef52b7c295dedf4f1900febe9566fa9ea7`  
		Last Modified: Sat, 07 Sep 2024 14:52:30 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:959df3f3003f21596d3e3d8a13dab966b15bb3403b64c83136420f141c6b90c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6943871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12943b2dc122963882d3f597e14c0ad35aac66c76fa01091eb71985919f3b5fd`

```dockerfile
```

-	Layers:
	-	`sha256:23a5b05d4ae3c8fe412bea9c7713157d669d5e598e121940b0576da244774385`  
		Last Modified: Sat, 07 Sep 2024 14:52:29 GMT  
		Size: 6.9 MB (6923630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e897b6f914bee2f181817dd95073df10b260f5db1e3b986a1e4f2a84aa38c177`  
		Last Modified: Sat, 07 Sep 2024 14:52:28 GMT  
		Size: 20.2 KB (20241 bytes)  
		MIME: application/vnd.in-toto+json
