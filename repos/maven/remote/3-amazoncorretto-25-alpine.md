## `maven:3-amazoncorretto-25-alpine`

```console
$ docker pull maven@sha256:23a3c9f900f5bab3c35bc9114b22b2e8a3413f2d0fcf898cb31be790a932ef7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:da9817ddd04ac8fae08fe83d27401dbf62eed22b69d61cfddebd0a21b9868482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193928752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c313ba16b61db0ad7cb61e2f34d86411e274a7cc2dfdf0586dcddf9aa7c79b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 19 Sep 2025 12:56:50 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 12:56:50 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 12:56:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 12:56:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cb07a476f609d2287eaf6b137a40ec572e48ba56eba9ad05879115a3fcefd1`  
		Last Modified: Wed, 17 Sep 2025 18:57:40 GMT  
		Size: 178.5 MB (178521010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ce9b91c849443ed551a7b935f15a406a7e5e32e67d1ad9abe6cef45947e726`  
		Last Modified: Thu, 02 Oct 2025 13:22:00 GMT  
		Size: 2.4 MB (2364425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf40d61ad353f11e99aeac9d0f8cbba064b21048190e3b79e6b2af11f65218fe`  
		Last Modified: Thu, 02 Oct 2025 13:22:06 GMT  
		Size: 9.2 MB (9242589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94242d553f43fe089fa456df6595c13f9c1eac150293d73e2c62379d66a0ea71`  
		Last Modified: Thu, 02 Oct 2025 13:21:59 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b389843b53c48f39d96ce827ab557b363aebd6daa208694f034297351cfc52`  
		Last Modified: Thu, 02 Oct 2025 13:21:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:adc2997676ca90f4f4734cbb70832ae9f759896f6497d047949dac83979575f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 KB (549437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628d20921681a8b7625638e9d36eb48402db682911b9e6d9b1ca8dc943de489a`

```dockerfile
```

-	Layers:
	-	`sha256:e2917e8a8e3a8f95d3f803fc2c205c5655960a9b425323f1afef87e09d719370`  
		Last Modified: Thu, 02 Oct 2025 14:29:17 GMT  
		Size: 533.0 KB (533032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ef1600b4ab9279268df626666735c9eb16eb69e3a4cffb91c426cb50373959`  
		Last Modified: Thu, 02 Oct 2025 14:29:19 GMT  
		Size: 16.4 KB (16405 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d33ee70a9683432bef90c78fa4e9d91fbb59d28834d5f06f52b857f7df9a7c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191841482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e9b7159f8b6074f8a3acf5b41ba768dd718714dd221e9c654d000652d1c805`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 19 Sep 2025 12:56:50 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 12:56:50 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 12:56:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 12:56:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c399b6f243d42421efe409b77ef3aa4b29e98e1b3e494cfddb5b45c3256dc6`  
		Last Modified: Wed, 17 Sep 2025 18:58:21 GMT  
		Size: 176.1 MB (176070661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9085d67903bcb3ac1b84c78ae6484ab71a7c68a47bfc0528b8060ef9e8c1e722`  
		Last Modified: Thu, 02 Oct 2025 03:33:02 GMT  
		Size: 2.4 MB (2396450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb2fb75edb762c5a96cf62bbdb81d2170188e39cc8163640fdbab8ebd0a6cac`  
		Last Modified: Thu, 02 Oct 2025 03:33:04 GMT  
		Size: 9.2 MB (9242582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a84c9427dba301488d7061c1fa65d7545e1fc4f258ed3555bc9be8c7c71d74`  
		Last Modified: Thu, 02 Oct 2025 03:33:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6adf3035eb1aa211104f9e1b0b6357961de1011cccc4e8cfb9e7713159486f`  
		Last Modified: Thu, 02 Oct 2025 03:33:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:13431c582027ff7c5f85078aa82a6609b82dca868e71c8edbdb57d6aada29135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.0 KB (548974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71dfe9b1c128784b301decf924cb396a115c72a17a7212430d148a0b630ced37`

```dockerfile
```

-	Layers:
	-	`sha256:34db66febf7f748507ea7b926d28f0bc3f6b2da1934495286863579b98479ce1`  
		Last Modified: Thu, 02 Oct 2025 05:29:16 GMT  
		Size: 532.4 KB (532436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ba075cb65e5d8605c4f60ed18d86ddd92b466638495f01d46be954123d9aed`  
		Last Modified: Thu, 02 Oct 2025 05:29:17 GMT  
		Size: 16.5 KB (16538 bytes)  
		MIME: application/vnd.in-toto+json
