## `maven:3-sapmachine-21`

```console
$ docker pull maven@sha256:290aa4f5e8f7f1b3db8547b9238d151f73c60f7949d5042dd514a02500fecf45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-sapmachine-21` - linux; amd64

```console
$ docker pull maven@sha256:c3cf4f631b5847ed8a9a325bddea93fa63168f7d3a65751f65853fd5eaf49ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279227373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b663cc299f816791022edaf2d24b32db1defef46984d4070dbbb02503bff7198`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 22:42:17 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 14 May 2024 22:42:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 14 May 2024 22:42:18 GMT
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
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68902b9f6cb3ac66bf0262fbab64b88e6ad76e72071de090c186a1209762e99d`  
		Last Modified: Tue, 14 May 2024 23:00:42 GMT  
		Size: 215.5 MB (215458889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423689e47e78efa0b28c5d0fb718ac56283ec96a580ae5febb5dd73461913d1f`  
		Last Modified: Tue, 14 May 2024 23:38:45 GMT  
		Size: 24.6 MB (24584709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1e6b7d3936ec1774d1ddbb76b5084a5f6d4bc3d4def0e9dcd533cda40ed77`  
		Last Modified: Tue, 14 May 2024 23:38:42 GMT  
		Size: 9.5 MB (9479951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea9f70ab8f0148b7f4fa9b0b13c5cbc3ab654880663b9176113afef6e24efd35`  
		Last Modified: Tue, 14 May 2024 23:38:41 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7b866699e0e09f2d939008147b8dbd4b1960ef6f1bce89a2b165e9b1b8aaa1`  
		Last Modified: Tue, 14 May 2024 23:38:42 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2701d65876f90b139c747f22d4225b06526c4b137698741748bf4be55bf2df6f`  
		Last Modified: Tue, 14 May 2024 23:38:42 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6093910fa9bce28709b45e71a822c8c7bfa0833d9f411ecb2f589ec4753abb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.8 MB (276758526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa5a623c9d0cc28523c10dfeb9070ca2ff15a8047026aa0c17dd63f6a09fd33`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 22:08:27 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 14 May 2024 22:08:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 14 May 2024 22:08:29 GMT
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
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c65427894a1d59a110706b8dc688aa1c224cfcbceb551f9864e4078dd37b09`  
		Last Modified: Tue, 14 May 2024 22:24:44 GMT  
		Size: 213.6 MB (213561771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b296d5e946a7da858e1a7b4af6b2531ad9a5a8c083f0ffeb048a00fd31e0a0ac`  
		Last Modified: Tue, 14 May 2024 23:02:29 GMT  
		Size: 24.7 MB (24676781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452d372fa4cc463e98461b2d81906bb5266f4c306d8166fa11545807390081da`  
		Last Modified: Tue, 14 May 2024 23:02:27 GMT  
		Size: 9.5 MB (9479932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca5e37ebf6e9fdb1f3fe18e205e1dd6edb7f4f46c2a6fd35d35106cbc08b9c1`  
		Last Modified: Tue, 14 May 2024 23:02:26 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a39e2c22dd3d4322f0bb9627d9d7d978f9a9d5fd55c8a86614c0d5d5d54998`  
		Last Modified: Tue, 14 May 2024 23:02:26 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f3079975762c36d2e7433abf216ecb628bd7002d746dc756649b5ef4c1c848`  
		Last Modified: Tue, 14 May 2024 23:02:26 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-21` - linux; ppc64le

```console
$ docker pull maven@sha256:65d172542f1d6c54987cd7301fbc6b402223ff728c1dc312c2d3542b6b9b235e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285784518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8776521f48cf6b855d1235cbbafe2f3310ba8cdd48846af089d5815508d33449`
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
# Thu, 02 May 2024 03:12:20 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Thu, 02 May 2024 03:12:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 02 May 2024 03:12:26 GMT
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
	-	`sha256:72be7588ff6f2a5bb170a639556699e4feba34202db850eab266ce4d4911fc8c`  
		Last Modified: Thu, 02 May 2024 03:27:41 GMT  
		Size: 216.4 MB (216382706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4ad2b2a11b460d48bc917c636aa528569878d86ad4a122d33d532904d8ea9e`  
		Last Modified: Thu, 02 May 2024 04:35:27 GMT  
		Size: 24.3 MB (24331986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25087dda1f61c61af01222f75e6dcdd827af585935bc67c1c7f80605e1f0f794`  
		Last Modified: Thu, 02 May 2024 04:35:23 GMT  
		Size: 9.5 MB (9479938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814672eb8541cef4d82dabcf7823b90bb66b2337dc9528c7b0ed93ee3c3d4495`  
		Last Modified: Thu, 02 May 2024 04:35:22 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6add9b203bd263b4132bb376e9f2139112883f4cea44e231f8c94c2919588243`  
		Last Modified: Thu, 02 May 2024 04:35:22 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedea76def35b8661f44b976469e688c1695875993232f72be595ce26a903d2b`  
		Last Modified: Thu, 02 May 2024 04:35:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
