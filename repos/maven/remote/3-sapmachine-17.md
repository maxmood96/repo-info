## `maven:3-sapmachine-17`

```console
$ docker pull maven@sha256:17f2a45905164299c94daf2c0639631772d65d56dcb38c935166acc47d6b475d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-17` - linux; amd64

```console
$ docker pull maven@sha256:30606c80d903ffab4cfd5f8b5b7d79d689cf0a587647a12e4082b700bd0f117c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266193643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6189c202a239e83ad9cef19ba6ffd9712e7b84887e28ecca3bd46e1db5ca42f9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:35:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:35:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:35:12 GMT
CMD ["jshell"]
# Tue, 17 Feb 2026 22:30:50 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:30:51 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:30:51 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:30:51 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:30:51 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:30:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:30:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:30:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:30:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:30:51 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:30:51 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:30:51 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:30:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:30:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:30:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a48afd434df06b47b33aeb0dad4e1cf69b3fd04ce825430ca0c3cdbe0d38f9`  
		Last Modified: Tue, 17 Feb 2026 20:35:34 GMT  
		Size: 201.7 MB (201688266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc90094a8305ce9535b7cdfefde1af5eaa4dbf9b50eae59847ede121a67ea201`  
		Last Modified: Tue, 17 Feb 2026 22:31:04 GMT  
		Size: 25.5 MB (25464480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0ee34e8045c135e35a3a99c38b0588676986823fd102c88e04def12efa4043`  
		Last Modified: Tue, 17 Feb 2026 22:31:04 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363db2b87890d2a32671710c4dd897b42c699d7ec7d0dd64bc7e49e8e4a6bae1`  
		Last Modified: Tue, 17 Feb 2026 22:31:03 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36b87182b84e3d61086fc4ea90829d34a284f5299af6011f30268945225d744`  
		Last Modified: Tue, 17 Feb 2026 22:31:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:0a8b2a016f9472a17aa53bbefa04635a511368e68b4ac5aec86f70f58414568e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741f3073486e4c4e63c16c1b7e00ec0a9f9588a2cd0b89501e610e4f439d7013`

```dockerfile
```

-	Layers:
	-	`sha256:39932183e1882729a9fd8f3785ccad9cde598d4b1898f86a41e75c9421f9c87e`  
		Last Modified: Tue, 17 Feb 2026 22:31:04 GMT  
		Size: 4.3 MB (4320497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ad3076a08fab5f2fcf58b6607dc5b9ad705e560d43923813950aa18fabddfb4`  
		Last Modified: Tue, 17 Feb 2026 22:31:03 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ca80ef7968461861fe959f0984fe29ff77e7cd6e3672d2e34d22fa74114703f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264132178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c231699ccb112ecf2102a9e784e0d80ae9e0cbbd183edf38d52b3dfcd9df53`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:34:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 20:34:12 GMT
CMD ["jshell"]
# Tue, 17 Feb 2026 22:19:23 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:19:23 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:19:23 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:19:23 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:19:23 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:19:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:19:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:19:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:19:23 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:19:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:19:23 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:19:23 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:19:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:19:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:19:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0b6dc86cf5225d30e4160bd5ee9a80a6dc40c555e8454166d92ee08127ceaa`  
		Last Modified: Tue, 17 Feb 2026 20:34:35 GMT  
		Size: 200.4 MB (200421623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6409ddb8ce95b69dcd87adfbbfcb163f34f38292287f7b2cfa79850cc2474fa`  
		Last Modified: Tue, 17 Feb 2026 22:19:37 GMT  
		Size: 25.5 MB (25532154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd588592cc5c2293e459f09454df695a977b1c9399f58b0f1cb15d9c3f3bada3`  
		Last Modified: Tue, 17 Feb 2026 22:19:37 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82160ff0c2c55b6a2fab25ff85052f72cacafb57906ffe625d86af9d0634d98b`  
		Last Modified: Tue, 17 Feb 2026 22:19:36 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4fc94eadbcce6227ab5ba2069902ee6fcb99a8950cd0e267355067259e426f`  
		Last Modified: Tue, 17 Feb 2026 22:19:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:53194f052261888a53c3621208b057aa9d15aa6d342799d0ee99c549449c84bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29afe633777bfec8172f2c4eec898d8ca794af769dc99b4bd410739892303638`

```dockerfile
```

-	Layers:
	-	`sha256:94d50910f30bc2a047e34dc0d472fd780ee6491ee2b86f448c4e07d514b6fae7`  
		Last Modified: Tue, 17 Feb 2026 22:19:37 GMT  
		Size: 4.3 MB (4327019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec6f5e4a785a9183ac00126da7c9eeff4ced0e27b92e29e268c1039db6765cec`  
		Last Modified: Tue, 17 Feb 2026 22:19:36 GMT  
		Size: 16.6 KB (16636 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; ppc64le

```console
$ docker pull maven@sha256:afaf7481d410c79e197f534a51e0399ab9e466e85124ee61ef60d0c4ee3441e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276185659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69c72d1740b7bfede44d20c5a74e252dba427ba9bf3b49bddd40d6b300b45c3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:33:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:33:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 21:33:32 GMT
CMD ["jshell"]
# Wed, 18 Feb 2026 02:46:06 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 02:46:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 18 Feb 2026 02:46:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 18 Feb 2026 02:46:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 18 Feb 2026 02:46:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 18 Feb 2026 02:46:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 18 Feb 2026 02:46:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 18 Feb 2026 02:46:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 18 Feb 2026 02:46:09 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 18 Feb 2026 02:46:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 18 Feb 2026 02:46:11 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 18 Feb 2026 02:46:11 GMT
ARG USER_HOME_DIR=/root
# Wed, 18 Feb 2026 02:46:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 18 Feb 2026 02:46:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 18 Feb 2026 02:46:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a10c874c6feabea993f50ba9cb1c5952afac19d83f218ed450342438089f8f`  
		Last Modified: Tue, 17 Feb 2026 21:34:18 GMT  
		Size: 202.6 MB (202575980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1781c301b5a3e27e93be164544566b1640662c673888c83d0e9a0b4efff56adc`  
		Last Modified: Wed, 18 Feb 2026 02:47:09 GMT  
		Size: 30.0 MB (29989492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe847dc677a6d47a6b8a0bc185d2e33a5c563dc825bf984e1869d07d8c58f0c7`  
		Last Modified: Wed, 18 Feb 2026 02:47:08 GMT  
		Size: 9.3 MB (9312245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916d294f76f4809c1539fb63fc75cbbc75311a220241112111872693c5d485ca`  
		Last Modified: Wed, 18 Feb 2026 02:47:08 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2279c3fecf46613095e22251eff2c409b24ae768958b03aad6615a0cd2c05870`  
		Last Modified: Wed, 18 Feb 2026 02:47:08 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:07c5c955c6f35213ad7df757e50d6a5bd63f7348eb1400a02e5b2ef44df4bc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932e3ec6221f6aa6b6ac22c3490bc7607554e304ff3e94c37a8935df230615a3`

```dockerfile
```

-	Layers:
	-	`sha256:4434a42ba9114d370828872651f023200097fc2569fe05f08d9e05172908f597`  
		Last Modified: Wed, 18 Feb 2026 02:47:08 GMT  
		Size: 4.3 MB (4320926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ce84f2d2d9cd250b51c09ab36c910914bcc00796070126bac72bc72b30091e0`  
		Last Modified: Wed, 18 Feb 2026 02:47:08 GMT  
		Size: 16.6 KB (16552 bytes)  
		MIME: application/vnd.in-toto+json
