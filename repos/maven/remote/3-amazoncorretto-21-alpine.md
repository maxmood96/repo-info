## `maven:3-amazoncorretto-21-alpine`

```console
$ docker pull maven@sha256:55d9ea7dc5f627a9f75320ea01ce666e484c6121a66f2a21e045e2cb2de0824a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-alpine` - linux; amd64

```console
$ docker pull maven@sha256:4d0e4a12cf5568d6ebf3b17894e3feb65c09137bb1a096536581c54775c11dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177060387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce067eb2e3a48afef99c6d864b2ca386adc4b789611c889caf03b0a45df92d62`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 01:06:54 GMT
ARG version=21.0.9.11.1
# Wed, 05 Nov 2025 01:06:54 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 05 Nov 2025 01:06:54 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 05 Nov 2025 01:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 16 Jan 2026 02:45:22 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 16 Jan 2026 02:45:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:45:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:45:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:45:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:45:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:45:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:45:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:45:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:45:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:45:22 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:45:22 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:45:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:45:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:45:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d4bc3368d3809cd8ad2e688cb5fe01f46190980ebdbfcac8e9822be3643f0c`  
		Last Modified: Sun, 04 Jan 2026 04:57:58 GMT  
		Size: 161.6 MB (161569892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31494b7ab944c3095f890e5d342b98b0c9d55d67fe28a10252d883642aa2e6fa`  
		Last Modified: Fri, 16 Jan 2026 02:45:30 GMT  
		Size: 2.4 MB (2374764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f3ea0111633ec62f937aac29b02ea11811319fe54b4da9b55f16b2feefa829`  
		Last Modified: Fri, 16 Jan 2026 02:45:36 GMT  
		Size: 9.3 MB (9312239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf4f098bb56893b1486f4537f8266615f0aafedf1d5fce7c58427f1b1a1c145`  
		Last Modified: Fri, 16 Jan 2026 02:45:35 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65314585c55bcbb3114eed41c138953614e137b0b7bdab3cec43f60d6b8ae98b`  
		Last Modified: Fri, 16 Jan 2026 02:45:35 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:4b856c34a44116e7c34dbc1b9b02fb0eaf2e980ba9d106eece8b1922a691670d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 KB (742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290e063d8ec23002c3596fa55c73dac2e84d3a20e9244340889d61e64eccc74c`

```dockerfile
```

-	Layers:
	-	`sha256:e4d38c46172407da1678107b2b4880801fac292e6d6410580caffdf7f9ee6820`  
		Last Modified: Fri, 16 Jan 2026 02:45:30 GMT  
		Size: 726.5 KB (726526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfcba5cf2aa23a3f17fcbf66a081a04a4818dc4c248fa10e108d74b1ae47dc42`  
		Last Modified: Fri, 16 Jan 2026 02:45:29 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:657bf5eeed3c4ae36bf968a0f30998d300b32368a85c17c7d10159f74d8aadc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175445484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad423967b20a97bdfcda162fdae5656af0a866f95deda91908f515ecff268dee`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:21 GMT
ARG version=21.0.9.11.1
# Tue, 04 Nov 2025 23:16:21 GMT
# ARGS: version=21.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:21 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 16 Jan 2026 03:32:20 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 16 Jan 2026 03:32:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 03:32:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:32:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:32:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 03:32:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 03:32:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 03:32:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 03:32:20 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 03:32:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 03:32:20 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 03:32:20 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 03:32:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 03:32:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 03:32:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fd450f0185222facf50c3585803b24553a293cbfa900eb12641a7831d0da01`  
		Last Modified: Sun, 04 Jan 2026 01:36:57 GMT  
		Size: 159.6 MB (159588499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6f3aaf8c0f8feee96958152bd3137d47f8b6e0738cd9e382086adcc9ce4bb9`  
		Last Modified: Fri, 16 Jan 2026 03:32:34 GMT  
		Size: 2.4 MB (2405635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4de498e4588bcb714c7f639a39bec53381df753a09d2d30a13ab28a7b130548`  
		Last Modified: Fri, 16 Jan 2026 03:32:34 GMT  
		Size: 9.3 MB (9312241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d1961df67bd39e7fe600d9335253e6c2a076a4f85c6a57ae2095ac4dbf87eb`  
		Last Modified: Fri, 16 Jan 2026 03:32:33 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeaeb01129e30ca3853ce3f1e1573738760a5e57cd9aafe91e55c79b6480f5f`  
		Last Modified: Fri, 16 Jan 2026 03:32:33 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:810f97c34f8c95fe8b99183e0ad1647cc8a83d080e32028a8022ecb2667a4f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.4 KB (742428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b43b19d97f199c0e013560a29a187fe1fae6fe1f78cf7ea2e2e57b559a4e9ee`

```dockerfile
```

-	Layers:
	-	`sha256:f65b084ecd1991e6359e676b175681e79aa54d17f1e3f0027bad4a2c49cb0683`  
		Last Modified: Fri, 16 Jan 2026 06:28:33 GMT  
		Size: 725.9 KB (725933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1978037840c92621e47a1cd805d3335fb85a0ca227034fbf75c297bb53791543`  
		Last Modified: Fri, 16 Jan 2026 03:32:28 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
