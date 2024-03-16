## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:484f9605b42f1d0e1b18731ba2f8327a03f12b7ccbcc1596202c147262ab57b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:1567c8212f675feb29df12dbcabe44bbfd6c0bb31bdf56560878e385a1de8b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299050318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0dd1ef6aad1de22247b0d9305ca7fb75fa11997347161a700cc4b6e70b44ad9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Mar 2024 07:59:14 GMT
COPY dir:40a794c5e13cc08a029a91ecc5d045abb1bd5b12f20c10640fe8595ecfefa662 in / 
# Sat, 16 Mar 2024 07:59:14 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 13:31:05 GMT
ARG version=1.8.0_402.b08-1
# Sat, 16 Mar 2024 13:31:27 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 16 Mar 2024 13:31:27 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 13:31:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fbbe555f6365629780fee590c2a87f84df704cf88725f26d12c40efd06a20308`  
		Last Modified: Mon, 11 Mar 2024 23:51:11 GMT  
		Size: 62.7 MB (62650553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8fb3e842b158f995b64b7e9c9b16fd7309e3efe721677a541055d89e9df989`  
		Last Modified: Sat, 16 Mar 2024 13:44:23 GMT  
		Size: 75.5 MB (75529612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342eaf92d7020c62339a5fc01f756b222f1246b978d7485227e7cd037980b520`  
		Last Modified: Sat, 16 Mar 2024 15:05:37 GMT  
		Size: 151.4 MB (151388822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e6fcfe0f7b8164ab8ee9d0ea7309ac41026fc7a22ed9aab2ed33f50871926b`  
		Last Modified: Sat, 16 Mar 2024 15:05:25 GMT  
		Size: 9.5 MB (9479945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29089e97a3dc00559f5bb4bbc75171691db51d6865b930e4f0d3cc7106f09275`  
		Last Modified: Sat, 16 Mar 2024 15:05:24 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b278340bb35caae3c819a9549d8d46f6dbb74ceafec5c14f99b2aa75a18d30f`  
		Last Modified: Sat, 16 Mar 2024 15:05:24 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ef7dab7d38d2effa88a0e3c0e826565a8bf87e833f474e453a9403ec6f39d6`  
		Last Modified: Sat, 16 Mar 2024 15:05:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5c1878560a18c43b1b4cce953111be0d9b8107fd88bd8a5ab77112b71bb882e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (256026357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa6e6c63d0ee4469633eacf89b2379d3f9aa82ac76463181a9d4e047438ad4b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Mar 2024 00:06:05 GMT
COPY dir:60a98a70510e647cb179bdf64e415936867e1b536f6e2209b88df6cf5ebf8753 in / 
# Sat, 16 Mar 2024 00:06:06 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 03:37:04 GMT
ARG version=1.8.0_402.b08-1
# Sat, 16 Mar 2024 03:37:21 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Sat, 16 Mar 2024 03:37:21 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 03:37:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1210c2cda2cd148732bb93623044ab07d9ead686e335afc95ffa891e3032d56b`  
		Last Modified: Mon, 11 Mar 2024 22:40:31 GMT  
		Size: 64.6 MB (64576374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c4a5dc6036ac4e91c355d4d9d4d4f8f8414c13fe717274aa46b86813710d10`  
		Last Modified: Sat, 16 Mar 2024 03:49:55 GMT  
		Size: 59.6 MB (59640379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade44e575137d0ac2bebc5d7b7719ba39ef3b5b66a9fb0ab5278ad6dd49874a1`  
		Last Modified: Sat, 16 Mar 2024 13:05:14 GMT  
		Size: 122.3 MB (122328293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd136538bab266bb77fbb8d2100648cff2d39a0e661116d2bdb9afa6fe4e1c7e`  
		Last Modified: Sat, 16 Mar 2024 13:05:06 GMT  
		Size: 9.5 MB (9479931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e21b4f75c7a570699e9b270b1d04f24340f6df5b26b2563694ce5e6b0d1c8fd`  
		Last Modified: Sat, 16 Mar 2024 13:05:05 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d9ceec82ff25e44fa073c96ef6013d7dcff042c4f2389f2f398d5252cd382e`  
		Last Modified: Sat, 16 Mar 2024 13:05:05 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7f598491cd9068e0cccbc46d387a63ffbc7f2b7ee99adf2e4c3ddfad907544`  
		Last Modified: Sat, 16 Mar 2024 13:05:05 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
