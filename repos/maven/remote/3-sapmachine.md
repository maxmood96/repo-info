## `maven:3-sapmachine`

```console
$ docker pull maven@sha256:5526b22d4c931c45fdea56304b3e7fc4a68790eaa7df0afb3d1e165979cdddde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:3fc734a736ad0dffc148646a5561817c5eef55cc919110228a1cb27a2e157e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (279966065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21edb96f9b7d5f2bb966a4442e72933d5e6b926cdb8f61161c2cec9c4357f825`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb619f111cd9a79835f8ab624a1b4713d2326306477299d9d2eaab9daf2a4571`  
		Last Modified: Sat, 12 Oct 2024 00:01:24 GMT  
		Size: 215.6 MB (215598426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e49f8c1047de3f7d95691818d0ec9405ec1cf19e4a913eed2d6f34d0f7baa46`  
		Last Modified: Sat, 12 Oct 2024 01:56:42 GMT  
		Size: 25.4 MB (25445723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c840545e7d25c7679f1a9bfe3f61be01e4f2501112e11d00cf31079d2e7cccff`  
		Last Modified: Sat, 12 Oct 2024 01:56:42 GMT  
		Size: 9.2 MB (9170423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0600deb63eca84b4da172e62595c4d88074ae6f853d1b23b1bfced97bd26ed`  
		Last Modified: Sat, 12 Oct 2024 01:56:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091e5406b5070a83e85fa2313ba58aaa7570f4434a1daafb28764281ef92befe`  
		Last Modified: Sat, 12 Oct 2024 01:56:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:8918d464258d9525de94a94456694c8c158c254ee39f5a1087ef16c57480b8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac32d1aff37626d5c79fdece017deaf75fc599e96c41ab697461ec353322919`

```dockerfile
```

-	Layers:
	-	`sha256:30caa66c9efcba7d81ff0d47457585c50907a43f7d1e8f4a5a6bcef872b40719`  
		Last Modified: Sat, 12 Oct 2024 01:56:42 GMT  
		Size: 4.1 MB (4133310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79141e63be3f7947d71730f0b27229bf3602c51ee6da79aae02abccd8c5eb006`  
		Last Modified: Sat, 12 Oct 2024 01:56:42 GMT  
		Size: 17.8 KB (17783 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:50617c30447e7019f8b8cca6db174fc38dd067dfee01667fd64e4a9d478e25ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277282460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726be601760e4f793548bab5fe55d0215e9bd950ee4ff9bb052d92e6748d48f9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6f410376e3ea641c8d322f9d6bcda25406671f32829386bd1c91c532d7254e`  
		Last Modified: Wed, 02 Oct 2024 03:49:37 GMT  
		Size: 213.7 MB (213701830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081421091e25ff31444da6d3f80db4102c1e0a058ae08c9af7a9a6a9f88ae005`  
		Last Modified: Wed, 02 Oct 2024 07:14:54 GMT  
		Size: 25.5 MB (25523710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72da780f780014cd0364b2a1e3874dc7a8db6db1f63190a1820294b5cb69c023`  
		Last Modified: Wed, 02 Oct 2024 07:14:53 GMT  
		Size: 9.2 MB (9170451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faf9336e9cb7026458a4195b2621d33b5e09ccb9cc986d8018ba66bad828e50`  
		Last Modified: Wed, 02 Oct 2024 07:14:53 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26217d2eb0d57268bf92ce05907992d14e3e1cad1abbeb8d1a34e96c2d7eb6ea`  
		Last Modified: Wed, 02 Oct 2024 07:14:53 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:ff146f2c82d63817c50cd2dd5838b931be45139043e50a0ed0a213e1b06319b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a45b00fc3fac641b28cbb679a494d27aacca8a96ee02c78cebb9861824d0557`

```dockerfile
```

-	Layers:
	-	`sha256:55930c5fea0adaa7c87553d744c0e8ca5e695a86812d999673ce89dfa8079d09`  
		Last Modified: Wed, 02 Oct 2024 07:14:53 GMT  
		Size: 4.1 MB (4139247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fe4ca014f44b34fc5624627b8f87471c055c25b9714cb011329ffacf7cd962a`  
		Last Modified: Wed, 02 Oct 2024 07:14:52 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:bb4f85d8aaf9738c7671e68e2b8af0f91ad55a04626c05f061823244b739debc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290733594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ff1642ab3c56030accdc156eca25f847ca372890587b248a687facf1fb8fcf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0928bff6b1e4da21216542e45d22ab1fd079cd88f8e7bb7adb765c59f7affac`  
		Last Modified: Wed, 02 Oct 2024 02:57:39 GMT  
		Size: 217.0 MB (217049576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f05bb9632cd46942e0477260543fe597e2ba155bc4642de97492d2284442e3`  
		Last Modified: Wed, 02 Oct 2024 05:10:33 GMT  
		Size: 30.1 MB (30120509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3b013349553debe0dc5c1845ae1b19836d6c7a3c6529f4bd158550545ae1c6`  
		Last Modified: Wed, 02 Oct 2024 05:10:33 GMT  
		Size: 9.2 MB (9170450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e500bfa1a01f81a9949737a6e5878ba2c429bd277ca64423fa14264bbf380c07`  
		Last Modified: Wed, 02 Oct 2024 05:10:32 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fb301cc62720fe58c3d5591a6c40ef67ffebf3dc11b09b31945a36591b63d6`  
		Last Modified: Wed, 02 Oct 2024 05:10:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:9516009e971ae21ed5b3b5b2e8024f61efafea609bddb4a2f87d1709480a6491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4155399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1e10ec7c0f8cabb60c7196d3200574c9b8dc5cf4edf796eb1693c7fec7aa23`

```dockerfile
```

-	Layers:
	-	`sha256:d7b36dc9c31837c0816d291c966c5ad8951f85b35de99be79f42f371d5849bc6`  
		Last Modified: Wed, 02 Oct 2024 05:10:32 GMT  
		Size: 4.1 MB (4137545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d64f4c58fdfdc35e9138b3d5471ed69ac2b95ba1edcc17f54551a8607f68ef8`  
		Last Modified: Wed, 02 Oct 2024 05:10:32 GMT  
		Size: 17.9 KB (17854 bytes)  
		MIME: application/vnd.in-toto+json
