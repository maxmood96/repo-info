## `maven:3-sapmachine-21`

```console
$ docker pull maven@sha256:a5d2af74aa4efdf6d355d89ad4ae33fcbc1cb3a3e3bd507b1e0ecc51066746d7
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
$ docker pull maven@sha256:942adefd388ec6ab4dfce100579d035c61f0388ca3b10980c4e6dff6bd32f46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279864685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232b1c8a94664987dd53b51ac79c62060e338ac1587ad321bdb2c7f311b90ad2`
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
# Thu, 15 Jan 2026 22:43:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 22:43:06 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 02:48:22 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 02:48:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:48:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:48:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:48:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:48:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:48:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:48:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:48:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:48:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:48:22 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:48:22 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:48:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:48:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:48:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e46c72759fe62eef331e472da7570293ca022c049d78e940a93915b0c6d1441`  
		Last Modified: Thu, 15 Jan 2026 22:43:48 GMT  
		Size: 215.4 MB (215363234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842372fa143397a4ecfaa3fe640aacfcdb37c05fed3c507af4494d72bc2727a8`  
		Last Modified: Fri, 16 Jan 2026 02:48:44 GMT  
		Size: 25.5 MB (25462160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354f22dda3880f458b2d5f2d6dba7f46a77ab26b065756a562619bce225b7f70`  
		Last Modified: Fri, 16 Jan 2026 02:48:45 GMT  
		Size: 9.3 MB (9312241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649600d200f16b9b4045f08562b8156fd38a2e24a55eee25ed88641765a1e085`  
		Last Modified: Fri, 16 Jan 2026 02:48:43 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cca49908eeec44304383a5e95f124c55b99eb1933ff2d25add8a77deb78adf0`  
		Last Modified: Fri, 16 Jan 2026 02:48:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:bce5043aa687171335eddd253257521bbe70f0624fa05f3dc72caef916b1ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4336494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951137dde67bcbb2706e7b2ce80313f89ff6d25820b13db42868ce292ecde423`

```dockerfile
```

-	Layers:
	-	`sha256:a37e28db07f1d05aa6242abe0e9a2ecff6c71aa37ff5a897b0359bbdf284462a`  
		Last Modified: Fri, 16 Jan 2026 03:32:57 GMT  
		Size: 4.3 MB (4319992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:088503a59375e52b2c4b07904d2e91748c846966749fd02f0129a9b6d9cf4cb9`  
		Last Modified: Fri, 16 Jan 2026 03:32:58 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:eb356d2283217746f296f01a17a363c27f1f7058b7ae52c7f04187b6f692ce77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277328259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fccd5190cffc37a160e86f58d8a1af4f9807882edb517ea43a8d6bbc74e5b8a`
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
# Thu, 15 Jan 2026 22:46:04 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:46:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 22:46:04 GMT
CMD ["jshell"]
# Fri, 16 Jan 2026 03:33:50 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 03:33:51 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 03:33:51 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:33:51 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 03:33:51 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 03:33:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 03:33:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 03:33:51 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 03:33:51 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 03:33:51 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 03:33:51 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 03:33:51 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 03:33:51 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 03:33:51 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 03:33:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0d90db03a16319b9d96ceba2e8b7b3222bfcd95633963e93eab81e03c0ad4`  
		Last Modified: Thu, 15 Jan 2026 22:48:09 GMT  
		Size: 213.6 MB (213619049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6f4724363b069800ccbcae54aab5491b035bbd71e60e60be9c2caeb60067c1`  
		Last Modified: Fri, 16 Jan 2026 03:34:12 GMT  
		Size: 25.5 MB (25532108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a94807716536cfdc23f6042a50a26f66b67b5ec0ba58c154d39bcfeef656aa3`  
		Last Modified: Fri, 16 Jan 2026 03:34:10 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e928273d1a4951342b5057b352cb1f2ea937a6814b5260aedafc2f2d58c1162`  
		Last Modified: Fri, 16 Jan 2026 03:34:09 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cdc6b95b927556d9f05d851283650986ed5e8e66694c3c294bb85ccf850603`  
		Last Modified: Fri, 16 Jan 2026 03:34:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:c21b82eeb86418d59a61a51bda46a3ceb9662034c5291073d7db9fabe790c5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4343150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc7181ad3a332fe448294bae52168dcec329d9b06ae7669ec2cf6466cacc89d`

```dockerfile
```

-	Layers:
	-	`sha256:c43da28eebcbfcf8e6917be4f480f5ef239d565c9ebe5dde91fb87e4359bcb3b`  
		Last Modified: Fri, 16 Jan 2026 06:31:05 GMT  
		Size: 4.3 MB (4326514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9df717e76ec45f510979957a08438a892727acdc3f38a586f51595301b7d23`  
		Last Modified: Fri, 16 Jan 2026 06:31:06 GMT  
		Size: 16.6 KB (16636 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; ppc64le

```console
$ docker pull maven@sha256:4550be1712eb91e52651c1a7a225a059c4dd49a46a37cc65a5bd2b4c9c03c447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289916743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b6baa4eee60156ea2b3b610162ceadfde38f3f4f940d72dd973b5f3081351c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:25:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:25:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 14 Nov 2025 01:25:32 GMT
CMD ["jshell"]
# Wed, 17 Dec 2025 20:22:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 20:22:56 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:22:56 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:22:56 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:22:56 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:22:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:22:56 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:22:57 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:22:58 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:22:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:22:59 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:22:59 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:22:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:22:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:22:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Tue, 16 Dec 2025 00:07:47 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc44e43c8e58b7a80c4c0a125b14aaf046d89720422f0223c0accff723e6f79`  
		Last Modified: Fri, 14 Nov 2025 01:26:24 GMT  
		Size: 216.3 MB (216312812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa10c633f34a69e178fe3facae508a392abe6d3be6f7f47f395957092a0aae6b`  
		Last Modified: Wed, 17 Dec 2025 20:23:47 GMT  
		Size: 30.0 MB (29986218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a80bf328011b3ef82d743d91a5ad437ee2a94b3ff7c27c538f3e574ee2dbc0a`  
		Last Modified: Wed, 17 Dec 2025 20:23:45 GMT  
		Size: 9.3 MB (9312249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b870471f4d319b21ddb2efba5142a4b0a7256d14f04a5fd9f32259eb1e211bce`  
		Last Modified: Wed, 17 Dec 2025 20:23:43 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72291455e05f6d3f0390c4450bf7d196d3190431a76d1b364b15ee4d32b05a0c`  
		Last Modified: Wed, 17 Dec 2025 20:23:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:3cb5a7ab7d03fe57a554393b8b62983cbf968321463c11b8a65431ee225421ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85592e37741d772d7d845a05f21a4fa9a98e280746433639827c97c493e81515`

```dockerfile
```

-	Layers:
	-	`sha256:877612447b81821d1cb4f8c57838e2b2e4a9d28c4d8c2e2a81c19016b77252c4`  
		Last Modified: Wed, 17 Dec 2025 21:35:11 GMT  
		Size: 4.3 MB (4318992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b7c84aba6596c017de2757924fc3405e81f74fe9352d667d862b843d7fbd24`  
		Last Modified: Wed, 17 Dec 2025 21:35:12 GMT  
		Size: 16.6 KB (16552 bytes)  
		MIME: application/vnd.in-toto+json
