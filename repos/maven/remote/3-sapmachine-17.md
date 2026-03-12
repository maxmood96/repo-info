## `maven:3-sapmachine-17`

```console
$ docker pull maven@sha256:d830793ce1b256a69633e50d20901020d4ca2256846c8941c4e90dbd28f9bbba
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
$ docker pull maven@sha256:6ae336360936ddbed8d2acf6fb92eb7e2c5dcb3f76484e1289a286df83df6de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266197113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780d2691726393e7febf22514659787c35f09e5a92531ccfbfcd775ec932d7bb`
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
# Thu, 12 Mar 2026 20:14:30 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Mar 2026 20:14:31 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:14:31 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:14:31 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:14:31 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:14:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:14:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:14:31 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:14:31 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:14:31 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:14:31 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:14:31 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:14:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:14:31 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:14:31 GMT
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
	-	`sha256:633a0cb9b750f523861e30c110f88455d06594f1c35a0e104be709df5a5ee61c`  
		Last Modified: Thu, 12 Mar 2026 20:14:44 GMT  
		Size: 25.5 MB (25469021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46934b3d0b70b5967ce3ecfa8245de4dccfc062f1618364b51f049c2324a79b6`  
		Last Modified: Thu, 12 Mar 2026 20:14:43 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03fa84a33a58ace321f8acdd57cab6ba37096da4898ddc61597030504a6c39c`  
		Last Modified: Thu, 12 Mar 2026 20:14:43 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daab8a037feb4d8cb091fc1079a60f315b010bb66693771d4a404885dac62b86`  
		Last Modified: Thu, 12 Mar 2026 20:14:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:3ba38ae3a425881220c206815cf03fd6f66609cfe7961ae204f23d40fe2cb241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4336988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93cd61a63e2b4ad0d6580bcdca601a8b4d36da70f04e323fb7f1f673900f8cc`

```dockerfile
```

-	Layers:
	-	`sha256:52579a7e4129269eb6802081a48ceea57de96383ba16ede62cdb53527e5e4e9a`  
		Last Modified: Thu, 12 Mar 2026 20:14:43 GMT  
		Size: 4.3 MB (4320485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae8f4b0d0e42d5e7fbf5434688f832129ed6d56c8fc40cc71295b61f5a4181f`  
		Last Modified: Thu, 12 Mar 2026 20:14:43 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:25d785a323a17f6c3e2af224385f8bd1284ef5ed8e1bbbedfad60e68e3b88756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264131906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecc95993f539b30dfdf715fa9c5fcd3d4c5fb5a68070e620fc5ab137486ffbf`
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
# Thu, 12 Mar 2026 20:13:09 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Mar 2026 20:13:09 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:13:09 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:13:09 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:13:09 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:13:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:13:09 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:13:09 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:13:09 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:13:09 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:13:09 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:13:09 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:13:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:13:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:13:09 GMT
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
	-	`sha256:2b0d0511f79315687faed0d10e534f328866e69da192fbb733d9493508ce3718`  
		Last Modified: Thu, 12 Mar 2026 20:13:22 GMT  
		Size: 25.5 MB (25532949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efaf5eb2e81b27dcc2e32f84fd41ba1fa55d51d546d5ae45e8adde6becfaf90`  
		Last Modified: Thu, 12 Mar 2026 20:13:22 GMT  
		Size: 9.3 MB (9311174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d20ed58b2f191fbdfbf8ec5be5bc2875d7c11a6c2e6bf0f594a2cf4aef89f40`  
		Last Modified: Thu, 12 Mar 2026 20:13:22 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fd23aaf483d4cf0f12513642eabec227f4f3389150404cc14747198140fc6a`  
		Last Modified: Thu, 12 Mar 2026 20:13:22 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:4c0309545ee5b723edf52677c5dc8575a2b2832acd58b4bdb68ec06bc77eae06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53af66286ea2b5455ff3ef1dad8eb1c5507c12f69b583ac0d214a2a18e60f7de`

```dockerfile
```

-	Layers:
	-	`sha256:e43ce8a989fb4dce4924f44b8de19147c1ef3de479bfa71a8f9505cf50983765`  
		Last Modified: Thu, 12 Mar 2026 20:13:22 GMT  
		Size: 4.3 MB (4327007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336dce2d5027b0e65ff99828127c16d49026fe92d6bf2b6c68f63436d735e45a`  
		Last Modified: Thu, 12 Mar 2026 20:13:21 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; ppc64le

```console
$ docker pull maven@sha256:d329068147c4ef75047575737693754605aac9c49fec83cbdd33edb86b216c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276188181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ac975d46a04644ad0e27a2aa1ac3d36fed0138cc56a4575d6dee5c5c05167f`
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
# Mon, 09 Mar 2026 21:22:02 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Mar 2026 20:13:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:13:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:13:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:13:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:13:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:13:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:13:13 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:13:14 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:13:14 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:13:14 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:13:14 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:13:14 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:13:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:13:14 GMT
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
	-	`sha256:5e833f46e79f1e5c3806e5c369a935cb8d781b0a200d87f362c85bbfb3f05756`  
		Last Modified: Mon, 09 Mar 2026 21:22:40 GMT  
		Size: 30.0 MB (29993074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4101a298e6987dc3d19fe1b26798a77ecb7c55978ab71a05357066afe9337d46`  
		Last Modified: Thu, 12 Mar 2026 20:13:42 GMT  
		Size: 9.3 MB (9311181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676cd306d839f7145e8d3e47e03091eeabb66b12516485617d56ea950206659f`  
		Last Modified: Thu, 12 Mar 2026 20:13:40 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09054a399dc56174b77e05ceee1b33b952bb16fe74874e9565a5694fbd5ed784`  
		Last Modified: Thu, 12 Mar 2026 20:13:40 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:c1a13ce80893c74904c95ce0e3745c4aaf55e1bc09fbe61b8034d7e6a84618f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f68678e9fd9f68fb2300af915318252843dc91af5e32e74435831a336690f41`

```dockerfile
```

-	Layers:
	-	`sha256:5d1c69609e75696fd9ac47cc9fc5d4a03eae2767f2888ec12c88ee4f3dc68678`  
		Last Modified: Thu, 12 Mar 2026 20:13:41 GMT  
		Size: 4.3 MB (4320914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb126b1cc833f6c07594343bbff75d838debf0f3f5b3a14d16a7c2b7753117a`  
		Last Modified: Thu, 12 Mar 2026 20:13:40 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json
