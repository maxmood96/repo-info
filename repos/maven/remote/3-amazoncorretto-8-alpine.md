## `maven:3-amazoncorretto-8-alpine`

```console
$ docker pull maven@sha256:3486a4a897afd1564527d2eae3ddb9cf8e3f8666d59818bba3c6837c87a2ef79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:7da7d0c0dfe4bf73a68f56bef94bfce76a2a3f56a8ac379f5784a90523876bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115396517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f71c084bb56a145b42acd2b42feab3acfe14f521351f08cd057284def2ac43`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 24 Sep 2024 11:57:06 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=8.442.06.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 11:57:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 24 Sep 2024 11:57:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 24 Sep 2024 11:57:06 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 24 Sep 2024 11:57:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 24 Sep 2024 11:57:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a6ce8261665c77bbb111b6283cf23d0a069f611bcf5a4fc474c7f16073f8e2`  
		Last Modified: Mon, 03 Feb 2025 20:40:58 GMT  
		Size: 100.2 MB (100224409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd3b4cf6c4bbb48c40cc6a0f2189a0feed0739d15a190d2ee6503d70aa6dc75`  
		Last Modified: Tue, 04 Feb 2025 13:34:08 GMT  
		Size: 2.4 MB (2358922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70724795bdb1dd5a8177cb2bfa34d4562dddd77b0dd79609212c28985bf61337`  
		Last Modified: Tue, 04 Feb 2025 11:17:50 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0cec1618d3cc55d4322dbe7d7487bbc311f66a092cea71b7ed96eea72bbad1`  
		Last Modified: Wed, 05 Feb 2025 04:17:34 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0e2b880e76b98717f5fbe5aa9e2678f3f31b9c3d0684e2ec3b8110c8f06e1d`  
		Last Modified: Tue, 04 Feb 2025 09:42:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:27957947069da0ecd00b39278c68ab9891babda73715961230cb1e5a7f392eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 KB (401509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447839d8dfc848bbdca84633c234680af0b7e0078a245faaa03631f71513b957`

```dockerfile
```

-	Layers:
	-	`sha256:74a7f51e048ca6d11c812c321a729fdd315d5070df0c711207b524546fb2c5b4`  
		Last Modified: Tue, 04 Feb 2025 06:15:57 GMT  
		Size: 385.1 KB (385124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40465282844c60a422468f3f91c7414cb70dcc9bab31a6568110ccc177033805`  
		Last Modified: Tue, 04 Feb 2025 06:15:57 GMT  
		Size: 16.4 KB (16385 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d2273bd04f467e7b241f433dcc40947f109e9dd1415dca4705bfce55cf50bc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115563335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf909a53b1bcc5ee593c5e448a12ab868eafb507f487947669fdf0ef7d9a8a06`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 24 Sep 2024 11:57:06 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
ARG version=8.442.06.1
# Tue, 24 Sep 2024 11:57:06 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ENV LANG=C.UTF-8
# Tue, 24 Sep 2024 11:57:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 24 Sep 2024 11:57:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 24 Sep 2024 11:57:06 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 24 Sep 2024 11:57:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 24 Sep 2024 11:57:06 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 24 Sep 2024 11:57:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 24 Sep 2024 11:57:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 24 Sep 2024 11:57:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 24 Sep 2024 11:57:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138417d13daa22c6cc12a75838baabad16a7f9093ef076866c298184d1f24973`  
		Last Modified: Wed, 05 Feb 2025 01:15:04 GMT  
		Size: 100.0 MB (100009092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8598c4c11c1bd048029de4c180e8e284e5fc07c0b1bc3546583f7f3e0cbe1a`  
		Last Modified: Thu, 06 Feb 2025 00:41:15 GMT  
		Size: 2.4 MB (2390407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6362ccf9e6f56ca5d8ff5148c0dd651dc7e15d4830fc7b60123b1d3727774c`  
		Last Modified: Wed, 05 Feb 2025 18:37:48 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b3b6d6cf66a71ec4fb4c6f6a4883982f523efd99d040d56c54f8d25c432b36`  
		Last Modified: Wed, 05 Feb 2025 18:37:47 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba37ea05e572e113b6b57c0fad7e6f68eb2fba2bf5ca264c8312d423e8327cd`  
		Last Modified: Wed, 05 Feb 2025 18:37:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:92a7af76144f59f44612fb4ef6722bc9f4b1f6888b6ac58b242724b46a65e77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.8 KB (401762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23caccb6e6e711adf6b441b766a06c937d87f14f90a3e590e7aa005a28f219c7`

```dockerfile
```

-	Layers:
	-	`sha256:5a633f3e6173b048d567f3d77945359f22ee6892adea5f756e10b960d3f2e733`  
		Last Modified: Wed, 05 Feb 2025 14:27:39 GMT  
		Size: 385.2 KB (385244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e66b72089246532237303f243597952dc206ac0ec1c9b6c3aac07da4d48c1eb6`  
		Last Modified: Wed, 05 Feb 2025 14:27:39 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json
