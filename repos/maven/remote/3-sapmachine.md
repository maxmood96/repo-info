## `maven:3-sapmachine`

```console
$ docker pull maven@sha256:af73b53a8ae1debb757e790851c962ae088a7aac7b0bf2ad35253376ef4f5c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:dfc94721121e011ddb28be11f0da68a18e5116bd637c8b37addd6b657c887b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262699088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db8175d59ab384bf4d4c19c5ddf492cf595edabc3e31ca3e09951f03f89d660`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 04:11:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:18 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:12:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 16 Jun 2023 04:12:19 GMT
CMD ["jshell"]
# Tue, 16 May 2023 11:35:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 16 May 2023 11:35:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ARG MAVEN_VERSION=3.9.2
# Tue, 16 May 2023 11:35:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 May 2023 11:35:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 May 2023 11:35:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6b15304efa504d1484bbfb072ce73bd7392525c68a4cfe7b9a1c9169697dd`  
		Last Modified: Fri, 16 Jun 2023 04:13:09 GMT  
		Size: 4.6 MB (4614213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea4a1e74fee3694e6add3872cc34fdfbfd2d9ce9f1c1fa6ecc5dba07b4e0cad`  
		Last Modified: Fri, 16 Jun 2023 04:13:43 GMT  
		Size: 198.5 MB (198528900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f9ee8cbcbbfd36cf06e3aa281ecee676f55e7db736f8672247eef0fb8555c4`  
		Last Modified: Fri, 16 Jun 2023 07:30:55 GMT  
		Size: 19.8 MB (19809139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2204881e367f72b3c483191f5fee61e8c26e247a6f9e3fb16378d5835aacd974`  
		Last Modified: Fri, 16 Jun 2023 07:30:53 GMT  
		Size: 9.3 MB (9314432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071bcb00d4203dc51a280bcbf7ffc73e2bf528381d838e44ab24e65141eaa12a`  
		Last Modified: Fri, 16 Jun 2023 07:30:53 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36348108ce19cc0593b17491d9990376319a4edcf047fde8c28974120f34745b`  
		Last Modified: Fri, 16 Jun 2023 07:30:52 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dde802b5788619902e1ee50175ac0ec7fb91773e53222ef51866e3fb12305e9`  
		Last Modified: Fri, 16 Jun 2023 07:30:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:027273bda0cf62b960da00e48174288f7fde5ac814c4713692151b85dde53800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259208270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5b20aba81984c620d9b73e6f4e3854e2b9462e0ce842de172f4af5f4539585`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 03:26:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:27:00 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:27:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 16 Jun 2023 03:27:02 GMT
CMD ["jshell"]
# Tue, 16 May 2023 11:35:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 16 May 2023 11:35:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ARG MAVEN_VERSION=3.9.2
# Tue, 16 May 2023 11:35:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 May 2023 11:35:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 May 2023 11:35:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83116095c10e617d95f9c6b32d320d9dd255638ca26990b41fd74d8ef336db1f`  
		Last Modified: Fri, 16 Jun 2023 03:27:46 GMT  
		Size: 4.6 MB (4565026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae295182fb5bace5b001eed658010ee2fc042997eeb75d7e42fca8fc36bd341a`  
		Last Modified: Fri, 16 Jun 2023 03:28:16 GMT  
		Size: 197.1 MB (197133391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff74fdda21718bc057aa52778e4ae8db29f026755ea347b684a19509cb87e845`  
		Last Modified: Fri, 16 Jun 2023 05:43:40 GMT  
		Size: 19.8 MB (19804871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994aa64a633062de018e2e936eac377b0cc7427c0fbc241f9c671c7ce0053684`  
		Last Modified: Fri, 16 Jun 2023 05:43:37 GMT  
		Size: 9.3 MB (9314415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c792bfa0c8fa17a21192461c047cd148657f89543ff43740ae1b586db9485d79`  
		Last Modified: Fri, 16 Jun 2023 05:43:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61c4f035decbc4bbf67f09350d3779f81c42ca713895e1d97083f35e3228bfd`  
		Last Modified: Fri, 16 Jun 2023 05:43:37 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809fed2ebcaff2a069e617637f1b0a977e1b00bf26a87464c88fe46f8597a854`  
		Last Modified: Fri, 16 Jun 2023 05:43:37 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:17f664f7af23e9d31c98e295fab0b380ffd1e90497300b100bfc43762c2404e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.1 MB (273142445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc93f49ee3d435f19ec3e697bfacf6b5d3a4ea542e600e0f8ca9a159b478964`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:39:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:42:52 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.7     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 00:42:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 16 Jun 2023 00:42:58 GMT
CMD ["jshell"]
# Tue, 16 May 2023 11:35:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 May 2023 11:35:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 16 May 2023 11:35:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 May 2023 11:35:55 GMT
ARG MAVEN_VERSION=3.9.2
# Tue, 16 May 2023 11:35:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 May 2023 11:35:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 May 2023 11:35:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 May 2023 11:35:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cc78fcdff28960c7adbf3de6bd4e587d6a81a231ae53efd46a5e3e3a8e26ee`  
		Last Modified: Fri, 16 Jun 2023 00:45:02 GMT  
		Size: 5.4 MB (5381546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f39c886a3a370de9fca788de47f96fe5076c5868d55898b6263b63a3400fd6`  
		Last Modified: Fri, 16 Jun 2023 00:45:57 GMT  
		Size: 199.5 MB (199485036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b299835fd75d5b617a3c36189253ec23a82ec6ed44009a889feaa1737e09ec5`  
		Last Modified: Fri, 16 Jun 2023 02:57:04 GMT  
		Size: 23.2 MB (23248687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77dc5b39ccfd30631d96bbc48afb7a0db90c9d7bb8c78cd1ce3922c4a779d37b`  
		Last Modified: Fri, 16 Jun 2023 02:56:58 GMT  
		Size: 9.3 MB (9314407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d86b3c29b44317eae4f31b14ef0e71895c49e371c49e5485265fe4f2b88e240`  
		Last Modified: Fri, 16 Jun 2023 02:56:57 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d355b143a6756336a3a89f74fd9178969af3623ff2e5fb1120affa1be75dbfd`  
		Last Modified: Fri, 16 Jun 2023 02:56:57 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0995d143064d98381749d2413f8c502e41f8e8d4e8e0b1f68d4288f902a6ba`  
		Last Modified: Fri, 16 Jun 2023 02:56:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
