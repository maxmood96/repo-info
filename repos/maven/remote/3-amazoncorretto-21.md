## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:1f81747dc56173fe74e9deb9ae5686e578565989229f5b8fc41c4fecf3b56fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:1e2b8013b880ef3a7073a8d80765338c35fc137420dfc250e33f0d923ea18f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 MB (389168727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47da0f033e29cc5761247be0e1b32dd6f310f50965a032bb3a559e07b6243e55`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Mar 2024 07:59:14 GMT
COPY dir:40a794c5e13cc08a029a91ecc5d045abb1bd5b12f20c10640fe8595ecfefa662 in / 
# Sat, 16 Mar 2024 07:59:14 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 13:41:24 GMT
ARG version=21.0.2.14-1
# Sat, 16 Mar 2024 13:41:49 GMT
# ARGS: version=21.0.2.14-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 16 Mar 2024 13:41:49 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 13:41:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 18 Dec 2023 19:11:15 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fbbe555f6365629780fee590c2a87f84df704cf88725f26d12c40efd06a20308`  
		Last Modified: Mon, 11 Mar 2024 23:51:11 GMT  
		Size: 62.7 MB (62650553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e49efdabe18d080499bb81cf60869f43212994c7325a67b45c2f62d148e29e`  
		Last Modified: Sat, 16 Mar 2024 13:51:04 GMT  
		Size: 165.6 MB (165629272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cab98a29879be001e1ae061a22521ed9c234f5b0c61e402f948ccd67336601`  
		Last Modified: Sat, 16 Mar 2024 15:04:54 GMT  
		Size: 151.4 MB (151407569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbfdfd981d5471e3036c7d4a0fe96c5beaeedff7590cfcb594257e267a8fdd4`  
		Last Modified: Sat, 16 Mar 2024 15:04:42 GMT  
		Size: 9.5 MB (9479945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667d01e8da30999243d308841bb7e838a16fc6bfde1fbbede25d6da8db3735e1`  
		Last Modified: Sat, 16 Mar 2024 15:04:41 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c836ce4f249de6596f91ec4974327d684624339b5c5ef9af73059075f80bdb`  
		Last Modified: Sat, 16 Mar 2024 15:04:41 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5797e847e4f3405e5e9d2d7a01e9428cb84e9d96f1ddbbf5d80f60aaf9bcce`  
		Last Modified: Sat, 16 Mar 2024 15:04:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9aecf87e4a548793acb15f4ca5467d53e3b6419be5c31187ba58e048b8e75436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (362002864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81157d8a19097a42d5e991cb083a9a0cab75125b397b9d9ad6aaef71fd96f9db`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:30 GMT
COPY dir:5c5e76fbf44d4b5d5bbd02274337780df6faf67a7b224750d628854242527355 in / 
# Fri, 05 Apr 2024 18:07:31 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 18:50:54 GMT
ARG version=21.0.2.14-1
# Fri, 05 Apr 2024 18:51:13 GMT
# ARGS: version=21.0.2.14-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 05 Apr 2024 18:51:15 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 18:51:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 18 Dec 2023 19:11:15 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1e9d4daaed12ccc925403048e4968011b475e192de72d80e36180798aac508fa`  
		Last Modified: Wed, 03 Apr 2024 01:52:31 GMT  
		Size: 64.6 MB (64560609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779cd1668acb10c3d6c1fcd0c590d1ddb2a95909a5fa2ab00209497cccbea74c`  
		Last Modified: Fri, 05 Apr 2024 19:01:22 GMT  
		Size: 163.7 MB (163678762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0628ad92787df3af077f9d16a9ee133a095920a3e62152d68cf477cea0eacdde`  
		Last Modified: Fri, 05 Apr 2024 19:41:18 GMT  
		Size: 124.3 MB (124282165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81afea36253482c23ac5b1406a844e020a3567efa2ff71a647862af073e24acf`  
		Last Modified: Fri, 05 Apr 2024 19:41:10 GMT  
		Size: 9.5 MB (9479945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ee02334830996f9dbafe4aa55e430647eddc57b10e30a9d9371bedf3300f52`  
		Last Modified: Fri, 05 Apr 2024 19:41:09 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70744efd887f3e41d182eaebacc4d58c4e1dc1a9216d64f989d418271f224e4`  
		Last Modified: Fri, 05 Apr 2024 19:41:09 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299f15baafbfd8b0ea86dadf529113b3b55e9c2c376f69edf1e38d825a63757d`  
		Last Modified: Fri, 05 Apr 2024 19:41:09 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
