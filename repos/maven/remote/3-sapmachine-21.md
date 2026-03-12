## `maven:3-sapmachine-21`

```console
$ docker pull maven@sha256:4dea84a5406f19c302ce5152db2763ac8edd2430fce89f5df6e5c3ac93369299
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-21` - linux; amd64

```console
$ docker pull maven@sha256:14549e8e82d715b0469af812ce31e18704c7f8f874d91e001bc402a0b35780ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (281002354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0b00bd96d60c833db6282ca382fa5ee8ee6fe273d4c5fdc602c9a54d6ed529`
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
# Wed, 18 Feb 2026 19:22:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 19:22:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 18 Feb 2026 19:22:32 GMT
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
	-	`sha256:c43aa35203f5eb148fa114917a74cf759d79101eb42035777448778f6400edb1`  
		Last Modified: Wed, 18 Feb 2026 19:22:55 GMT  
		Size: 216.5 MB (216493900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d2087ca783ee7cbf2267ec7872eb1d5edf1802c0e8456f6350f4610ec8f37a`  
		Last Modified: Thu, 12 Mar 2026 20:14:44 GMT  
		Size: 25.5 MB (25468627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c8e3ce625f77110c46f559db6cf07db086fe62dd87d4536ca3537e42bc51b9`  
		Last Modified: Thu, 12 Mar 2026 20:14:44 GMT  
		Size: 9.3 MB (9311180 bytes)  
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

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:ccbff576ea9bcb8e9155031bd297487f51ae85c68fc96af4525efd7cb0fa9ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90f7430970474851466c3b149bcd2748938c2c80f48207ebe40d0636d652aa7`

```dockerfile
```

-	Layers:
	-	`sha256:1bcd216d208fdab26e937b330d0bf4ab376586cbabc6764b575e651bc41d2f1a`  
		Last Modified: Thu, 12 Mar 2026 20:14:43 GMT  
		Size: 4.3 MB (4322372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa395dd923ac8369066629cc31099633cd7d43846d570015bbe3d2951aeca02c`  
		Last Modified: Thu, 12 Mar 2026 20:14:43 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9a0efe9cd340bd84e691e493f2367554e704f404cc7e23d0186552fe70572343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278467767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff8ba139067df14b8813252d5694ae10893d0e0dd9381a4a9897cc603ded3b2`
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
# Wed, 18 Feb 2026 19:21:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 19:21:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 18 Feb 2026 19:21:14 GMT
CMD ["jshell"]
# Thu, 12 Mar 2026 20:13:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Mar 2026 20:13:15 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:13:15 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:13:15 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:13:15 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:13:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:13:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:13:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:13:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:13:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:13:15 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:13:15 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:13:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:13:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:13:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8b6b0da145858f0888b2b052857f80e42950c6cd6dcfcc57b508dedf3568e2`  
		Last Modified: Wed, 18 Feb 2026 19:21:38 GMT  
		Size: 214.8 MB (214757105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143e7db6a5977d2b6482f40693f63a00dc2eb34dd08cfc016524dd13b647297e`  
		Last Modified: Thu, 12 Mar 2026 20:13:29 GMT  
		Size: 25.5 MB (25533329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e32d88a5fac48fade49f28857d75d1d6e397ece52648eaefac29ffa862787f6`  
		Last Modified: Thu, 12 Mar 2026 20:13:28 GMT  
		Size: 9.3 MB (9311174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d2dabf6637b959b43eae4f5e5e4a5c101556daf9caba5f7393a43595b02552`  
		Last Modified: Thu, 12 Mar 2026 20:13:28 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ffdc94becdb643f7ecdffb7e6b10183ab710a0e0d9a9e6d9cf50266fcdaec`  
		Last Modified: Thu, 12 Mar 2026 20:13:28 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:287ca205f7730d8ad68f5a57823d4edbefeb5c08e4386e2c87b3fc34294f2d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4345529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afd2c4889db5edde0bc2a451e0b2c48254865b241cc4559b9f192729a7fd8d6`

```dockerfile
```

-	Layers:
	-	`sha256:58c774f47d5d04ae571ea2a61700fe7a604ca06f595f632980e0c0838400d7a0`  
		Last Modified: Thu, 12 Mar 2026 20:13:28 GMT  
		Size: 4.3 MB (4328894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28863f2fb162ae014bb7d384157f67b712f56a56fe54a6d869b31a5719eb4b70`  
		Last Modified: Thu, 12 Mar 2026 20:13:28 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; ppc64le

```console
$ docker pull maven@sha256:abd7a28e50f5b525ef0e2f943c697517982550e54c20036d94c1bef25d2c459a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291196124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075c9949490701ec745052b0397ea98e9dee6524208dc362d2000c2956ac7381`
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
# Wed, 18 Feb 2026 19:13:36 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 19:13:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 18 Feb 2026 19:13:36 GMT
CMD ["jshell"]
# Mon, 09 Mar 2026 21:21:58 GMT
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
	-	`sha256:b739ab332ad76e7d7c2e9fe29e0c0876cff5eda905248b72a2c767bcf5ac19eb`  
		Last Modified: Wed, 18 Feb 2026 19:14:22 GMT  
		Size: 217.6 MB (217583886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c9a8702e0a665d8a4704bf673f7d231f264dd92c3200355599fcbffeeec58f`  
		Last Modified: Mon, 09 Mar 2026 21:22:42 GMT  
		Size: 30.0 MB (29993111 bytes)  
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

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:3d6f565d8942186aae0f9a8cde7aeb54d090f998a75eedd6fd328d5c0a65913e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4339354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12a4cd3df231e10b58c3eddbedf0dfcc8d37e14a0f70c44a35749a1245299e8`

```dockerfile
```

-	Layers:
	-	`sha256:a2a6a93df4ebfcc30a1e817140c5a4c2e837254c7e554b5a1a6c84d062055e39`  
		Last Modified: Thu, 12 Mar 2026 20:13:41 GMT  
		Size: 4.3 MB (4322801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76537659c9674f9a0b403ce000bbfd2509c2506b6324d3931721bb4d8913dcec`  
		Last Modified: Thu, 12 Mar 2026 20:13:40 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json
