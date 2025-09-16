## `maven:3-sapmachine-17`

```console
$ docker pull maven@sha256:9b2d565d1957dc336237fc064efde921038d05c199be3436ce8e50b261e0ade3
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
$ docker pull maven@sha256:8eee75e491bc6be7da4324898e25f7504fc7422620dbaf3175c21f5fc0cac98c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264921661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc99596c3d94c08386429c18964eda52a313048823257c4ed40cf7dcc0ac584`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc659d495de5c56a791cdb340d45f939fdd4e64a1b7f33b04a09fa1ea4870e1`  
		Last Modified: Tue, 16 Sep 2025 00:11:17 GMT  
		Size: 200.5 MB (200492698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9448685ee2ac38056f1c6476685099940251eeb474aa7810db39dca27e042bed`  
		Last Modified: Tue, 16 Sep 2025 00:18:48 GMT  
		Size: 25.5 MB (25461906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee63bc99e52edbdd3366e49ffecd93bc4a5d37d8bdaa183a6d068dc96ff0419`  
		Last Modified: Tue, 16 Sep 2025 00:18:43 GMT  
		Size: 9.2 MB (9242573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4901cab9a26c2bb8804854a88885eac74eea95295a21c9c69b22d1dadd9c196d`  
		Last Modified: Tue, 16 Sep 2025 00:18:42 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7444bfbfe769886185901608baf0749af24471f390eacb1b2729342bdf7862`  
		Last Modified: Tue, 16 Sep 2025 00:18:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:3d5760dea038396a14139987b79820ae8b2649449d1b59024f1a3480421c4f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4334656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3663f7b2e988e2fae39f47f9364f820e7c384392e2e36f386cb5b330a1ef359a`

```dockerfile
```

-	Layers:
	-	`sha256:a556586525480d3c9cf001964f970e6f98457e55c2a6ee4e8a8bd10d00e33bfa`  
		Last Modified: Tue, 16 Sep 2025 02:33:03 GMT  
		Size: 4.3 MB (4318110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72495e6fb5e1a42cafa8ff8039eb5e608760f35aca3e4356b09905295c1823d`  
		Last Modified: Tue, 16 Sep 2025 02:33:04 GMT  
		Size: 16.5 KB (16546 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9cf7ca2c1554333a703361da78627df9cabc7126f2eed104c7bb9872e55e4f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262847593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6f68845e06ce919e9ccf5cfc0f2cf82c7690d1bbdfabc41a4d4fc4984abce5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd2fa76e3bd8dd4a13334c30bdd4ab0b4d44cba0213b6362bcb3581f7476e56`  
		Last Modified: Mon, 15 Sep 2025 22:26:26 GMT  
		Size: 199.2 MB (199210508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856ba70a37349f1d08c1926d846fe2cce8368c454efb18cb72e834b65706e47`  
		Last Modified: Tue, 16 Sep 2025 00:18:55 GMT  
		Size: 25.5 MB (25532154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef63aad89990d1e7b9c81f7401a93f56aada8bd13a7708ccbae6c3d0d7616d4`  
		Last Modified: Tue, 16 Sep 2025 00:18:53 GMT  
		Size: 9.2 MB (9242578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a065a5fe9a0b1fbfaa3fde3f02106c4bcebf11ccb154506ad58905722a845e3`  
		Last Modified: Tue, 16 Sep 2025 00:18:52 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4243f089ef918effdd3fb323a0cc1fa9280ddf9ee2ab3e52819beea4ab4a8463`  
		Last Modified: Tue, 16 Sep 2025 00:18:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:9bb64925fd4a9722fb5bdbe333cfdd895f9fdba4af9a8b68eb9d1732269e7e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4341311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbae9ca1989bfc040a9881d46f9188ba05e1baef92cdf05eaf4cfe9fd1b1fbda`

```dockerfile
```

-	Layers:
	-	`sha256:b36053cc1c08458a0638856e65cd77015fb72c884b45f9eea7a823f8d5851aa5`  
		Last Modified: Tue, 16 Sep 2025 02:33:09 GMT  
		Size: 4.3 MB (4324632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e2abba08b3f0b42e44d48e5c2e80cd9b3824f6ceef15d0e3756d2b880d33bed`  
		Last Modified: Tue, 16 Sep 2025 02:33:10 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; ppc64le

```console
$ docker pull maven@sha256:978a9b888c304cbfa531da5ac0916b81c7cc2f16f978559f0b9c6bce64cb1665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274828549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ceba55c23c50d4323c5c3f491db49d0804ea6a3575c0ef961bb55933cdbfe6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
# Wed, 16 Jul 2025 06:51:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfca9032c81ee396fa8ea0f3a43747df1af86db3ef5230d9f319472e01d100a2`  
		Last Modified: Tue, 02 Sep 2025 09:38:06 GMT  
		Size: 201.3 MB (201270110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d6ff1c2f5fbfe004b11361aca9cfdcfb22c1588584dc4f03e2107a4cca0923`  
		Last Modified: Tue, 02 Sep 2025 12:12:46 GMT  
		Size: 30.0 MB (29985281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6baac85003330f00ce7e099ca733c233f2cf8b0aa9fa7d5c28b2ce2acd729d`  
		Last Modified: Tue, 02 Sep 2025 12:12:44 GMT  
		Size: 9.2 MB (9242587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f9e7155d0cb76c9f175df902285308a4b187ca2dc99e6de66eeecc99e45bca`  
		Last Modified: Tue, 02 Sep 2025 12:12:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f232aad3fd399d3508e27343569f1719b7dda9822826dcace7ac5a5de9eeae6`  
		Last Modified: Tue, 02 Sep 2025 12:12:44 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:8c85c5fcd137b17b70c299a4c8dbb33b7100eac03ad3a622fedb0e12e12dc6cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4333714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5202bd8a7e0563c237393ad60aaaf6893bf0d5230902e8b07a203c5f93d5f259`

```dockerfile
```

-	Layers:
	-	`sha256:040475a27ff0626098185606005fdb5b5503b86b6e01c97c7f55540e3e7fce06`  
		Last Modified: Tue, 02 Sep 2025 14:30:35 GMT  
		Size: 4.3 MB (4317118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba6e7e394b6d85bfc3c9f2b8ff19761f47c2a8e4115efeabba73c0ddaac7bf75`  
		Last Modified: Tue, 02 Sep 2025 14:30:36 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json
