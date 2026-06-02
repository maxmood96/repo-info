## `maven:3-sapmachine-21`

```console
$ docker pull maven@sha256:e9644e560ad1c92941e23630634511bd0f39ad4247ea59607ffd7b7acf11727e
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
$ docker pull maven@sha256:cf1470a83c8c3e6068a5d198995e9b094c6b9a7ed48bcba137209ff24ca8b464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281268424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b136b7c1cb8fb285a6aaa7219bd091132a09028100c9c95d1aeaec79164144`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:24:31 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:24:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 02 Jun 2026 08:24:31 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 10:29:57 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:29:57 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:29:57 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:29:57 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:29:57 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:29:57 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:29:57 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:29:57 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:29:58 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:29:58 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:29:58 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:29:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:29:58 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b85ce1238b29f8e0862c1d1bd43f73f087ce3a4ec3eb19b8cfdfeb78166e339`  
		Last Modified: Tue, 02 Jun 2026 08:24:54 GMT  
		Size: 216.7 MB (216700652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124fa5e35ee839b1baa9d1fbb880544e1630a42df04a8eb3e4f68d4edc770b76`  
		Last Modified: Tue, 02 Jun 2026 10:30:11 GMT  
		Size: 25.5 MB (25473999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e01451e212b79f3bcbb22aebc4392ca96dac6e82e81f570aeffbef39e9c807`  
		Last Modified: Tue, 02 Jun 2026 10:30:11 GMT  
		Size: 9.4 MB (9359959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7574cb77314e6a7e03a5b6a6e4481ab8e35271e31f3fbd6b70d07a88461c34`  
		Last Modified: Tue, 02 Jun 2026 10:30:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602726855ec4cbbbf78f78fb3c6778630459f22ee9a6cbf95ee75e99f86834d7`  
		Last Modified: Tue, 02 Jun 2026 10:30:10 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:477fb7606b1081417f90ab1671b6a6bf7da1bc1f2cfbc96031ac75cb6189e995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104096f828d6e24ae0670b9b9dc36d750a475fb50ef778f35af49d4cdbeaf71f`

```dockerfile
```

-	Layers:
	-	`sha256:c8e3a27ace4f6d8fd13759b80d1cf2ae1092f778210da72445854d7ee884d482`  
		Last Modified: Tue, 02 Jun 2026 10:30:11 GMT  
		Size: 4.3 MB (4323051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe8175bb3a82c8206cea711e926865bb04137a7ac7ef4550f37fa9434f8a68c5`  
		Last Modified: Tue, 02 Jun 2026 10:30:10 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f2bbda6e7540a9fbaf86e31cf4e9292c50636fc50b4f791fecda0bb73dee5307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278740960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e8c14683263e783de97e17be030625296a973e202b4c90a75545f25f2e17b1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:24:52 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:24:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 02 Jun 2026 08:24:52 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 10:27:06 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:27:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:27:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:27:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:27:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:27:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:27:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:27:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:27:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:27:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:27:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:27:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:27:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f69e667f0e7dc9e304bdf6e6d5109635cf647680519c7f35cf61a877edcd568`  
		Last Modified: Tue, 02 Jun 2026 08:25:15 GMT  
		Size: 215.0 MB (214968551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f1ce15b5c3432a6407565117ae4e5fc811dc0a310c0e502f633e4310d93b8f`  
		Last Modified: Tue, 02 Jun 2026 10:27:20 GMT  
		Size: 25.5 MB (25535022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61dc889c7af4570d1c88ddb90171bd770c0276160c78a4465764ef5b71e6858`  
		Last Modified: Tue, 02 Jun 2026 10:27:19 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0149ec3873c49ae25db6dfcf519db9a4ec147f24569235daa782fe10eecb95`  
		Last Modified: Tue, 02 Jun 2026 10:27:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6595c22c690701b5545524e6c067d96c5e7bd170b08ee85a86ea0fd7cfe0bc95`  
		Last Modified: Tue, 02 Jun 2026 10:27:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:506de841efae36bf6ce34e8f8114c497f06e64191b9f8d636590d9d0ba3c9ca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4344371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cac69fafd8464abdbf41e5e7d33bfac8a5357a2631777e5b32a91840cd9565a`

```dockerfile
```

-	Layers:
	-	`sha256:017ff027ffef4b8979a1198cb0452335f330ae26d73eb7aacce37697fa72e7ac`  
		Last Modified: Tue, 02 Jun 2026 10:27:19 GMT  
		Size: 4.3 MB (4329573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9804ad7dd5208868bcb5bde2136cc2224c687f5b72b51b164aedb13a5d6ee00`  
		Last Modified: Tue, 02 Jun 2026 10:27:19 GMT  
		Size: 14.8 KB (14798 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; ppc64le

```console
$ docker pull maven@sha256:3354a66614451ba76e7368731b1a2b9bc0cd4489561720c2c84b639afa8e8bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291443731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b449e8e68b615f380bc1a7ead3dd189a230d4b6264f1ef93b853398aab3bc5a0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:57:54 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:57:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 02 Jun 2026 08:57:54 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 12:07:41 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 12:07:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 12:07:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 12:07:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 12:07:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 12:07:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 12:07:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 12:07:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:07:42 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 12:07:42 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 12:07:42 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 12:07:42 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 12:07:42 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e3ce5aa23e3cd1a22314f215c02172d9832cf5ab8fb85955dd877111e883b9`  
		Last Modified: Tue, 02 Jun 2026 08:58:41 GMT  
		Size: 217.8 MB (217767532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f15bf49d29409400a04d6f06e991eceaace811ecc716fbd9f61af35f738a93b`  
		Last Modified: Tue, 02 Jun 2026 12:08:15 GMT  
		Size: 30.0 MB (30001126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deacbe46334c12ab346806c917909e5fcf9a4b51998a01f11c615e93681fa4d0`  
		Last Modified: Tue, 02 Jun 2026 12:08:14 GMT  
		Size: 9.4 MB (9359968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4a8a1835d86558d9b3d738b6afd1b384ae69dd7c29da897fff3e5e5ff0b3f6`  
		Last Modified: Tue, 02 Jun 2026 12:08:14 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913c4ce5f57454915cd7730dd0b1ce1536f62d677e7d48776cf728abb780e9d`  
		Last Modified: Tue, 02 Jun 2026 12:08:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:0ddd718f16388492b29d660cab370862409c75335cce16d24096321013b0c614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7457b7e64a9cad4843dba96e05cc37ca8dea9e1005e90d1f3e1e599520b7ab`

```dockerfile
```

-	Layers:
	-	`sha256:dc61ac85c9593461d5f2e519b343ecf1a2bb1f961f3479552465af6c18ec8ab2`  
		Last Modified: Tue, 02 Jun 2026 12:08:14 GMT  
		Size: 4.3 MB (4323480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c552db6b9ad36d52a03c96aaaa3014f9abbcc53a3f68b08518cd25987bc86a9`  
		Last Modified: Tue, 02 Jun 2026 12:08:13 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json
