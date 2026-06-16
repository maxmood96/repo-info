## `maven:3-amazoncorretto-8-alpine`

```console
$ docker pull maven@sha256:4e52c22b205d0982519e3d94c2cdc8320e5d789e5857d0a58e29a9bd4c64f4d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:35474e0f8396dfa9f2e2e6236b57168aa670159914e5a7ebc7a8e3c4303bc3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116163813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f91d830c86fcb0f8f38d21583fa22e2d0eccc1bd172cacc40317ade607d0229`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:19:11 GMT
ARG version=8.492.09.2
# Tue, 16 Jun 2026 00:19:11 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:19:11 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:19:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:19:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 16 Jun 2026 01:23:08 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 16 Jun 2026 01:23:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 16 Jun 2026 01:23:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 01:23:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 01:23:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 16 Jun 2026 01:23:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jun 2026 01:23:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 Jun 2026 01:23:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:23:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 Jun 2026 01:23:08 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jun 2026 01:23:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jun 2026 01:23:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jun 2026 01:23:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e012724ee24b9e32ed4d9d059565bf64520db5852157bae5995083a5ad3c0a2`  
		Last Modified: Tue, 16 Jun 2026 00:19:25 GMT  
		Size: 100.8 MB (100751270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4126132a7b01c2ccabe6dd9d4dc834203b7ffa0775633c65e2bb44a4e241a4`  
		Last Modified: Tue, 16 Jun 2026 01:23:16 GMT  
		Size: 2.2 MB (2205177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4086aa80b403aeba75e616d123b48aeb5e1fd13c3046460830510f01872ae321`  
		Last Modified: Tue, 16 Jun 2026 01:23:16 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc62784325a2fb8f8072a5419e4be4c54ad130ad0f32dc1ae3cf5e76ffdc6cb`  
		Last Modified: Tue, 16 Jun 2026 01:23:15 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9891b62bacd0490eba4a199288213739555b2a43066dadc5563dede29b07cd16`  
		Last Modified: Tue, 16 Jun 2026 01:23:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:28e25eef587ec5333a94550db10b173a5626a5c939a1e3fe31d6bd601f0f05c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.8 KB (406831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70966c178e2e48a5b64d4818efa8163423476e8e72c55271f987dfa08dd7c97`

```dockerfile
```

-	Layers:
	-	`sha256:f88829e73504ec3174602b76e42106b456e8b12a011c04256a0d5e538c4e3a2d`  
		Last Modified: Tue, 16 Jun 2026 01:23:16 GMT  
		Size: 392.3 KB (392318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bca4359d4711b46cbc2b3ca118f660be328934ba33d5607906dd8a72a5782a99`  
		Last Modified: Tue, 16 Jun 2026 01:23:15 GMT  
		Size: 14.5 KB (14513 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:bd298eb9acaaf4134e9afa97d91dd5a2ec03874fab4abb89bb5a8383f1c307a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116333005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e14d4903fa9002dcbcf81f20d43ee37457b3fffb8792f4fb72498e4b4100280b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:10 GMT
ARG version=8.492.09.2
# Tue, 16 Jun 2026 00:17:10 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:17:10 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:17:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:17:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 16 Jun 2026 01:25:20 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 16 Jun 2026 01:25:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 16 Jun 2026 01:25:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 01:25:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 01:25:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 16 Jun 2026 01:25:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jun 2026 01:25:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 Jun 2026 01:25:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 01:25:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 Jun 2026 01:25:20 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jun 2026 01:25:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jun 2026 01:25:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jun 2026 01:25:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed179bb78cb0c8841268f0ec59940476bfd9103344c16e74580feeae5c187e87`  
		Last Modified: Tue, 16 Jun 2026 00:17:24 GMT  
		Size: 100.5 MB (100544728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf66279d527ca392d8a32ea2fdc4e4a1b36fefb5474889394bcd6f23739418f3`  
		Last Modified: Tue, 16 Jun 2026 01:25:27 GMT  
		Size: 2.2 MB (2244263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3b817f9ea898bb42cd498fd1cd94035b86de3d1eb77aa065f5fe21be7a8c9e`  
		Last Modified: Tue, 16 Jun 2026 01:25:27 GMT  
		Size: 9.4 MB (9359971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b45190b288d4a7cd8ee22819add7cb617ab712f311e3a6a0667019d8ff89ea4`  
		Last Modified: Tue, 16 Jun 2026 01:25:27 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37da1576eab24bfc7b32dc36686e258488d71accd9f8dfc64c3cf80b51581c05`  
		Last Modified: Tue, 16 Jun 2026 01:25:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:40b887deda68b7604ce9cdb60c8cc184b0930e0a863671fd18c09b17b0c8e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.4 KB (406434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1eaf79ce2b2d1d7d4c415c912c053232de1dd317fef1bf6ced22a9bfaab6c2`

```dockerfile
```

-	Layers:
	-	`sha256:2094ea4fe2f0ca5f1e21f2cacda26ae5d89b1581b6420f48783984bc28b9db83`  
		Last Modified: Tue, 16 Jun 2026 01:25:27 GMT  
		Size: 391.8 KB (391788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d29b48f3bff66932f5364fa48b74430ea8a3743f9a4207f5e41ad46f65d330e`  
		Last Modified: Tue, 16 Jun 2026 01:25:27 GMT  
		Size: 14.6 KB (14646 bytes)  
		MIME: application/vnd.in-toto+json
