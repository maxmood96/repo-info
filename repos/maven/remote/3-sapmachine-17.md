## `maven:3-sapmachine-17`

```console
$ docker pull maven@sha256:fcabf5ae91e782c099310d9ee1f2be7ea52c9f98739afc0a1230d0e39c6fb669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-sapmachine-17` - linux; amd64

```console
$ docker pull maven@sha256:9dba81509c87bd3626ffca64ad1f071a16d0db6fad6ce7787867e1e805b53653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260771076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96394fb082eb7c2fdcff11bce9fce06fc8ed41bad08684410e2082361adc3adc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:19:13 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Thu, 25 Apr 2024 23:19:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 25 Apr 2024 23:19:14 GMT
CMD ["jshell"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659f2d59e090f0117a4af1e5ec3573a3126c7bcc27cf09b8c32f8f42a166dc82`  
		Last Modified: Thu, 25 Apr 2024 23:29:00 GMT  
		Size: 199.9 MB (199917202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c783c89f376a9f93c7e622ea3c21225bf47c362c743c0b03009db95d8ebbd4`  
		Last Modified: Fri, 26 Apr 2024 05:15:19 GMT  
		Size: 20.9 MB (20932823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8573db517613f8b1768b374c1f47fb01b0bc1f8743fdcc4a3a326bd9f637ed9`  
		Last Modified: Fri, 26 Apr 2024 05:15:17 GMT  
		Size: 9.5 MB (9479961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eface7b9141a7671a651bfbf5e47646031e3618665fe5d1ded668e12c7ddf0f`  
		Last Modified: Fri, 26 Apr 2024 05:15:16 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c52ef6a55f228e43066bc99c3a49adc7ba96c576a58b601202a2544aa2b060`  
		Last Modified: Fri, 26 Apr 2024 05:15:16 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e145821534cd5607479b678c212ac8d90f5475174e6d8f9bb2a37e4bc0a9f103`  
		Last Modified: Fri, 26 Apr 2024 05:15:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:cf82e7c463b0289bf7dcbeb796509a1e4f97a33fb67d438841fbb4ff50901a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257292721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d7bb23afda029b823eb11c78fd683dc710a7f3609d1928e057b0f13d858073`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:39:22 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Thu, 25 Apr 2024 22:39:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 25 Apr 2024 22:39:24 GMT
CMD ["jshell"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da7b688d9ba794a950359d208cda6e58863e4922f3bdff3ddc0ced36607dcea`  
		Last Modified: Thu, 25 Apr 2024 22:47:52 GMT  
		Size: 198.5 MB (198499712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e02e1c4000d04cf2b4e3fa06ee4e27e9c54b07efd07ffb97d22d676f74eb427`  
		Last Modified: Fri, 26 Apr 2024 01:17:45 GMT  
		Size: 20.9 MB (20910676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910e051d12b8868e24f166a2e7a999d5184562399a1ec4e17f3fecd47e712b73`  
		Last Modified: Fri, 26 Apr 2024 01:17:43 GMT  
		Size: 9.5 MB (9479959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ae58cfd6bb474d4904b969e87ce0c41626865e35a18124aa75d40c07e4268a`  
		Last Modified: Fri, 26 Apr 2024 01:17:42 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bdf0b94cf281b00c24ceeb61485dd0f1f726eb869c47b03a65fc044fb1731b`  
		Last Modified: Fri, 26 Apr 2024 01:17:42 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c7e9aa9d91a4397ddac69e11f38fa54c4aaaffa64164a4ff1e1bb3b7750ee9`  
		Last Modified: Fri, 26 Apr 2024 01:17:42 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-17` - linux; ppc64le

```console
$ docker pull maven@sha256:4756bdc2aa96ecefdf1dfce1a52362591e96d942092a0e5b2a6b1b8b5f7b1e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270369987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9983b20e52c71887298616a3055ec8f306276f41cfd4b2be158727bf8f2acf1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:04:18 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Thu, 02 May 2024 03:04:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 02 May 2024 03:04:30 GMT
CMD ["jshell"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3df68772d972a96e616eca0c2f7c4db45c750e815838318117e5687e453eaad`  
		Last Modified: Thu, 02 May 2024 03:25:13 GMT  
		Size: 201.0 MB (200968360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55fcd37e690120d6408452e51b6223edbc718f3beb280704287d2133151f03f6`  
		Last Modified: Thu, 02 May 2024 04:35:11 GMT  
		Size: 24.3 MB (24331829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2343e494be21606f9228e63f2833315f7e60a8bea992e14f8c06559c5fad89c`  
		Last Modified: Thu, 02 May 2024 04:35:06 GMT  
		Size: 9.5 MB (9479910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4710e31983d411fa70811956d6f535b715c2c29dc98773ac891af916398cba3d`  
		Last Modified: Thu, 02 May 2024 04:35:05 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02cfdfa1e71cec59aaf038c46ef74a6ef9b734208821e3455c10c5e44ff8bc7`  
		Last Modified: Thu, 02 May 2024 04:35:06 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80e2565fccbe9ceb84e4f9e5d3fccba28ee7049a2a5fbba7b3bec443173b97c`  
		Last Modified: Thu, 02 May 2024 04:35:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
