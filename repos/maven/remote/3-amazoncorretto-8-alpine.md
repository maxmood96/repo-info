## `maven:3-amazoncorretto-8-alpine`

```console
$ docker pull maven@sha256:bff729c62ae6d8c15020a8a7bfea966985a11b59fd43be9f8a874aa23f6e38f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:14cfde8c280aa91f7d98dd8ba87d2ca83d3d2a8caade83e63a666e7d4042ee8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.2 MB (116165982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353b44d2a299ee31022a50c366cbab9f465983f0f8a4257032fd56820141eecd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 14 Nov 2025 01:42:23 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 14 Nov 2025 01:42:23 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:42:23 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:42:23 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:42:23 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:42:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:42:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:42:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:42:23 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:42:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:42:23 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:42:23 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:42:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:42:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:42:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92574770f6746e0040e247649931c248a47ee8d6ac55cf021609a6a99672a25`  
		Last Modified: Tue, 21 Oct 2025 23:26:30 GMT  
		Size: 100.8 MB (100757885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91510ec211905576fee57a22fdca56f04a0185d7beffc3daef6416f33d9776f`  
		Last Modified: Fri, 14 Nov 2025 01:42:38 GMT  
		Size: 2.4 MB (2362030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8c353d0cb2c32dcb1bef1c9429ab93d5913084dfb2860ee7701b4327640c79`  
		Last Modified: Fri, 14 Nov 2025 01:42:44 GMT  
		Size: 9.2 MB (9242572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f293dbc660fdea0f5836da2755c9914a7daf37f1a6cac465660dfd411a4872e`  
		Last Modified: Fri, 14 Nov 2025 01:42:38 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fec63c6311d2f44155a680a0211cd43f367ce50cb8f7f1d44f6c4ce6e56c636`  
		Last Modified: Fri, 14 Nov 2025 01:42:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:e51077bd5edc5dcb44e8d2212c1705b61e5d5f4c52a867388e0933a07cd0cdbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.5 KB (407509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e28235a28cf5aff3cac12a9f55fe10d73a5a1f4bc73624272f8e9f56bc9a040`

```dockerfile
```

-	Layers:
	-	`sha256:a98d02e9fcc56415d575d9df64b9c5a0e1ec809ba4d2722239e24fd1f09fbf16`  
		Last Modified: Fri, 14 Nov 2025 03:29:05 GMT  
		Size: 391.2 KB (391156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e19a65f234630f3910a5b45c5ba2a8bf5bd3b936c5344d2917b0faf059df041`  
		Last Modified: Fri, 14 Nov 2025 03:29:05 GMT  
		Size: 16.4 KB (16353 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:05fdd2c5c85a5ba0d03e7d6503001726cf64551bf759bea9160a0a765dee0e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116307981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d36147938744717b3df426021617b5f2e39f26cf9e34c3fa914966033d725a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 14 Nov 2025 01:59:34 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 14 Nov 2025 01:59:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:59:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:59:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:59:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:59:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:59:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:59:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:59:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:59:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:59:34 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:59:34 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:59:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:59:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:59:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2744539f18ab260f7f42fe25f3c1d2ed1c04d685e18106e294c21f0dc1975c3f`  
		Last Modified: Tue, 21 Oct 2025 21:49:27 GMT  
		Size: 100.5 MB (100533297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7bb6dc46fa89ac9d8e009098af102ebac5cc48b959e5eec495e521eee6d100`  
		Last Modified: Fri, 14 Nov 2025 01:59:49 GMT  
		Size: 2.4 MB (2392997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfe5f57cfb9cdaec5818cfb48cdfecbea1d5439ca35a4180af6a11f528ab796`  
		Last Modified: Fri, 14 Nov 2025 01:59:49 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac49bfeff9f70a01422dff2a19ed75f0ab0c7196793d9684a851cba46160912`  
		Last Modified: Fri, 14 Nov 2025 01:59:49 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5781a71c60a5ffdcdaa615c882f01884fac0ed8deec35997b37af8fc669f766e`  
		Last Modified: Fri, 14 Nov 2025 01:59:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:ce3f739ad59854c19d45d3c39f38fc49debda44821688814876a21422ccbbf2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.8 KB (407762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b87f5978519322de5bbb70b37c8ab88fa9b0e66e35dd95c02949f70f4ce8a0a`

```dockerfile
```

-	Layers:
	-	`sha256:e9992b81dffeba172e720bccddf5e38c7e7401a1f0185613844aff4b08c54252`  
		Last Modified: Fri, 14 Nov 2025 03:29:09 GMT  
		Size: 391.3 KB (391276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e7da35bafe1fe58b9b57decba2b06200a85e52514412340cfd204e144dfb29a`  
		Last Modified: Fri, 14 Nov 2025 03:29:09 GMT  
		Size: 16.5 KB (16486 bytes)  
		MIME: application/vnd.in-toto+json
