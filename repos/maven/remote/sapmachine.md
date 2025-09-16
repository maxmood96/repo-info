## `maven:sapmachine`

```console
$ docker pull maven@sha256:21c31d7f3487b4c58d3286df29f3f5c82bb8d5d51f70e0f0180e289d5023aca4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:c6a252120079cc3ada88004b621318c833fc543d0621c231e405f37b576847e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279738820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ebdc7fdbd9f4c80446ca63c03836680cb1b4f789b317d90f8791da2b12aaf20`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
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
	-	`sha256:6799639fa354b664aecbb07809bc430f5056b1c0fff0e692ee257009b4a23d88`  
		Last Modified: Tue, 16 Sep 2025 00:09:46 GMT  
		Size: 215.3 MB (215310058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece832d1aaf65e0e7fb34e6b74534363f770966f6d9cd8f35281b7be96842f8d`  
		Last Modified: Tue, 16 Sep 2025 00:18:36 GMT  
		Size: 25.5 MB (25461706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f90dc19015f2a34839225bd5ea3eea8d1b1802b47fe851b2cf3356e890a6fe8`  
		Last Modified: Tue, 16 Sep 2025 00:18:34 GMT  
		Size: 9.2 MB (9242573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcfaceb3cbdb943226b109c9e3a3289b3b1b559a240f3b8006a540b1f5a64c5`  
		Last Modified: Tue, 16 Sep 2025 00:18:35 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f03b604d2f3ad9baae1f9d852f64b2cbcb337511337852282f7bfc4d407274`  
		Last Modified: Tue, 16 Sep 2025 00:18:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:e58d900e779766e285188392f5e9b93a3e63ab758ab0971f30c40cf8bd3f8f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4339007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c03d151f6c272d78c84d11a36d731cc1960c0361f565605aac2c58d93e8fd`

```dockerfile
```

-	Layers:
	-	`sha256:8a42745f2bd6d1ba2d42c264f8daa50ab3f288bbf0e3cc69508499ac527b3b3c`  
		Last Modified: Tue, 16 Sep 2025 02:32:47 GMT  
		Size: 4.3 MB (4321219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cdf8b6d4bc9e59d4aecd549ae63d5d94914f89e743c6d6978b53c023a1a2de0`  
		Last Modified: Tue, 16 Sep 2025 02:32:48 GMT  
		Size: 17.8 KB (17788 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b418902353c16a89c9655510c5ae3877762dbb3d5eac2e5aa368b10b31834e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277183533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67efe8dcd257dc5d80fbbe2e4c2af0bf8991d114ea28abf745d89ddf85d185a1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
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
	-	`sha256:4f0fe52aef1b20b37b3c8be5f276ca686a29fafb64a47884d9c3862fdd9e7e26`  
		Last Modified: Tue, 16 Sep 2025 00:08:44 GMT  
		Size: 213.5 MB (213546473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91522a05d8cd974fe465645929841e76b93f7cbf433ce1456ad5ebbf29dd0d89`  
		Last Modified: Tue, 16 Sep 2025 00:18:08 GMT  
		Size: 25.5 MB (25532129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c197760f7b6300a153680a2612f7a8f77eb9fcc3dc79b7fb816985b08358768`  
		Last Modified: Tue, 16 Sep 2025 00:18:06 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577d9761a3724905c00e864c3891726436ac0f90ba6517b21338b61c3289c554`  
		Last Modified: Tue, 16 Sep 2025 00:18:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eaf201d83878eeeaf14c16bdea562daa526bc884db6e8ba0a5096fe120f0886`  
		Last Modified: Tue, 16 Sep 2025 00:18:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:28e2d0d28d156faaa396ae42d54a8b1f407f23a3235ef1f9d26adc4c5edb48cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4345758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f78c990d56cbd4b7b4923371b28adfabb6b51e5957327359454ce11e7b6198`

```dockerfile
```

-	Layers:
	-	`sha256:c06eeb2628bc1af8f73514e1c54c3195cc6f70a28d259fe57640971b0120c58d`  
		Last Modified: Tue, 16 Sep 2025 02:32:52 GMT  
		Size: 4.3 MB (4327789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:574cdf24e9cbd1d9826f7375f26d31ff113237aa8fe62529fc49770a6e20ad5e`  
		Last Modified: Tue, 16 Sep 2025 02:32:53 GMT  
		Size: 18.0 KB (17969 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:30ddeac67fddb22a994db3c5e41dce814818c5300ca805705b26348107eaa4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289822892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3817ecc8ee72cb4ea8b36e3ff0edf2fff6d6ad28a48668e89d8945af37bb6e44`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
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
	-	`sha256:110505d30f9d2a804b70954ece15e95c10049c25bdf4a800289377442f481ca8`  
		Last Modified: Tue, 02 Sep 2025 14:50:56 GMT  
		Size: 216.3 MB (216263999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3200a92d44868433cb14a0983582aa7e74d2a6737a401547bf9655e1dc8ed4d`  
		Last Modified: Tue, 02 Sep 2025 12:14:44 GMT  
		Size: 30.0 MB (29985728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bd75a80ef326e829f14934ed57095b9e20cb72f90c497d12050b4405c8c7ae`  
		Last Modified: Tue, 02 Sep 2025 12:14:43 GMT  
		Size: 9.2 MB (9242592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4047874f891d4a4a8459327cd041b59204ab13e37c36732fa63296d253dec2`  
		Last Modified: Tue, 02 Sep 2025 12:14:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6146b849fd5de99efdc04ca0ea700587d30d006f587f11215e957c8e3a2d9bf7`  
		Last Modified: Tue, 02 Sep 2025 12:14:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:891b9d3733d24e220ffaa0f1537d88a0b5eb729c5d3071360a4476049992ff16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021ec41581f256bdf2b9df58833cf3e68b2b4cd45ec9b9539de3c8f80fb7013b`

```dockerfile
```

-	Layers:
	-	`sha256:e5a05e5d4e52ccdf214e1a5891a84e922eee5533348d6e0109a2417f277bec49`  
		Last Modified: Tue, 02 Sep 2025 14:30:26 GMT  
		Size: 4.3 MB (4320251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af404fe628145334ec7f69ff8488eaf97fce2f01a830c9862733a56eeb97bf09`  
		Last Modified: Tue, 02 Sep 2025 14:30:28 GMT  
		Size: 17.9 KB (17862 bytes)  
		MIME: application/vnd.in-toto+json
