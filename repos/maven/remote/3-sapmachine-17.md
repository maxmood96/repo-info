## `maven:3-sapmachine-17`

```console
$ docker pull maven@sha256:60e42b4dd8ae5be6947a18c43d55c3c4ee848f18561ba3dcbed15909674dd576
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
$ docker pull maven@sha256:906f739c96e24bcbb13db45ef0f16ecc7181c98458fa26fd0a56bd61f6b912b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268582598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b98bc7ed12f47571e5c949bf51866ad0f7a8253913a6e33baa1caafdee03e50`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 20:04:24 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:04:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:04:24 GMT
CMD ["jshell"]
# Thu, 05 Feb 2026 23:31:26 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 23:31:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:31:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:31:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:31:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:31:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:31:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:31:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:31:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:31:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:31:27 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:31:27 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:31:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:31:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:31:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c57dcb4b77b462dfa5c5af8cf55361e84cd11262812016036092715b108a9c`  
		Last Modified: Wed, 21 Jan 2026 20:04:46 GMT  
		Size: 201.7 MB (201682671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86e275def39c47aae2f3c0bb841f012309cc4fb99a38d1d28f5941fc5d7f35d`  
		Last Modified: Thu, 05 Feb 2026 23:31:41 GMT  
		Size: 27.9 MB (27860633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4d602769f6c2546e23855f79ec131cce45b755d253804467c0211bca4300ad`  
		Last Modified: Thu, 05 Feb 2026 23:31:41 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795f163cdc507aa422949b78ac77b8796b32c62b0ade523ec4b3721659bad874`  
		Last Modified: Thu, 05 Feb 2026 23:31:40 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5768a5e418335ffb88536dd24d8733a41a24d9f38115b17822a8b004c2d19906`  
		Last Modified: Thu, 05 Feb 2026 23:31:40 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:7cfa76b385bfb2544f46a2258b14b9a800ae7b69b752db05df9d34f804cedb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a9ada4cd80c506843264b426adb4597d9cdf70a4caec2e4d3a3f586c3a378c`

```dockerfile
```

-	Layers:
	-	`sha256:6ac41fa7629d9aa01696b30af115a064e01eb720560b64d138a85493c6e6512a`  
		Last Modified: Thu, 05 Feb 2026 23:31:40 GMT  
		Size: 4.3 MB (4320497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e271001b183fef1cca24757d0e13ab555435ca7a25c772e41d44e6cab15e98ff`  
		Last Modified: Thu, 05 Feb 2026 23:31:40 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8f347bdb0012edf7eb63cd8d123743d7d22839f896eb8b13523a326f41ed53e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266350704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ed29053c9f1da382cd39d207331e5d25db025f5fc275bf93b25b434f20a81a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 20:10:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 20:10:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 20:10:20 GMT
CMD ["jshell"]
# Thu, 05 Feb 2026 23:42:19 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Feb 2026 23:42:19 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:42:19 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:42:19 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:42:19 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:42:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:42:19 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:42:19 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:42:19 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:42:19 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:42:19 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:42:19 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:42:19 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:42:19 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:42:19 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbd91831faf9988a8f6995050b3ccf7c6fd98ad0cd6b2ca6f3f2fae4dc632af`  
		Last Modified: Wed, 21 Jan 2026 20:10:43 GMT  
		Size: 200.4 MB (200421599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e577318e30ffbd92f55f0b428d43934f413fb10de39920471d8720bf660cac44`  
		Last Modified: Thu, 05 Feb 2026 23:42:33 GMT  
		Size: 27.8 MB (27751990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8578a3559917fd87ab5c1f47de2991e6b67c606efc3d65fab30c02e1e31ce388`  
		Last Modified: Thu, 05 Feb 2026 23:42:33 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c879dd85eb2c5e974f2c008833917a64666e8ac622bc45fd311370ef6e742315`  
		Last Modified: Thu, 05 Feb 2026 23:42:32 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f28fbf46fc97f2ea2f75759fb9f59904a3524d3ed8b0ad70f93a0757800f575`  
		Last Modified: Thu, 05 Feb 2026 23:42:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:b2b917874552767482e79a5caca6f9cd48a0f954727793339e5b13c45debfd0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4bbb71d3b3b48d6eb4f926b6fc367defc6916dbdfee325a4b65aedeeb59b899`

```dockerfile
```

-	Layers:
	-	`sha256:5d3019ff172c8d9c0c5de15314fa308c55f2e671f8a6f4beeb31887a9727e94e`  
		Last Modified: Thu, 05 Feb 2026 23:42:32 GMT  
		Size: 4.3 MB (4327019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db9372f7cc2da5aa49485a49b7aece9aa0b6fed125c7c503af3ae8825b5fff4c`  
		Last Modified: Thu, 05 Feb 2026 23:42:32 GMT  
		Size: 16.6 KB (16636 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-17` - linux; ppc64le

```console
$ docker pull maven@sha256:68b7f73ce284f34b95d6378672f73dd41892c9b27710d2ab10c71b263d22ca91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276169340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b63208704ab1dda29dde510fec7b664cacbc1fde5ad4a31d86e603a6d5cb6a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 21:27:53 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:27:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 21 Jan 2026 21:27:53 GMT
CMD ["jshell"]
# Wed, 21 Jan 2026 21:50:50 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Jan 2026 21:50:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 21:50:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 21:50:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 21:50:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 21:50:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 21:50:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 21:50:54 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 21:50:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 21:50:57 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 21:50:57 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 21:50:57 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 21:50:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 21:50:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 21:50:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d241a998872d58f4d2154f9c51c95f5d34fe4e4b8a8042d33f5ab59f2a42b9d`  
		Last Modified: Wed, 21 Jan 2026 21:28:42 GMT  
		Size: 202.6 MB (202563288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029a7dc4a6c96c7460ade1c8f127c1b0b6ac53b040861b7f097598a69b1fce4e`  
		Last Modified: Wed, 21 Jan 2026 21:51:30 GMT  
		Size: 30.0 MB (29986613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63da79674dee3ac3069e9ca75ffe7f496c8400531b2d2bccf5f1a87e91903175`  
		Last Modified: Wed, 21 Jan 2026 21:51:29 GMT  
		Size: 9.3 MB (9312240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6271741ff60d0e9fd8cb2b522242e7e1074838ecb32e8b5f7d8a4fb8dfc346`  
		Last Modified: Wed, 21 Jan 2026 21:51:28 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52921d531489233f1f6d54713f8d1a2ba5c4983013d52562aacd458552d8f523`  
		Last Modified: Wed, 21 Jan 2026 21:51:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-17` - unknown; unknown

```console
$ docker pull maven@sha256:49da5ad314b98708789bc22cd6c02e4400d9736fe2574f2617324db1835bf088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67180a6eb8b237c161c39c0d2295b5cfc09ccfcd2c9d8edb21c215e1d7f901a7`

```dockerfile
```

-	Layers:
	-	`sha256:fa2840aa1fb7b56dbd34a69052c50bcb2817ea223070639394f3ac7c6b9d1027`  
		Last Modified: Wed, 21 Jan 2026 21:51:29 GMT  
		Size: 4.3 MB (4320918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dc6d3075d792a6f01bdbf0cdad134330cef5d9f8b099b6bf3934a8b57a5b9f8`  
		Last Modified: Wed, 21 Jan 2026 21:51:28 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json
