## `sapmachine:jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:2feae267a1553a16f984d89e336a25266b19ed49d48975faf1f76342ec68f5f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:e8e687eda0d4af367ba46633cc1f16289b4dd168d9ef727c0ec5b61b3bb8b0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250577372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bb652a8c0541723190b3fcae48cd1cec5c56d0db8c31a2727f6047cc8ac707`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc24de399270f29ffcd210dd4ee592e42de32447de97b5f083e61b3a2f78a98`  
		Last Modified: Tue, 28 Jan 2025 01:30:04 GMT  
		Size: 221.0 MB (221041684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:09f13872d6012db79fc50f599c119642e4b036fda5f435fe0a584d7b5a22082b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2261897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42d53260ea28cebbf8aaad6188248f20efb7553d5798507685fea3fbc9b0d10`

```dockerfile
```

-	Layers:
	-	`sha256:98f97c88d6de7ed248a8f796b76dd0fdfdb254b1f696f9c640bb09f55b523433`  
		Last Modified: Tue, 28 Jan 2025 01:30:00 GMT  
		Size: 2.3 MB (2252285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16489be3664ce1101275b4ccc5cc53dfd83598a719a97ac85f908b0263ea922e`  
		Last Modified: Tue, 28 Jan 2025 01:30:00 GMT  
		Size: 9.6 KB (9612 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f269ff4466bcc188180424602ec5e0f32cc2b108b28d26a30cbb083caba9ccc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246375866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9982b581cec7efc431b32e02d6c757e9737f7bd1b8327a98480f93011c60cf`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd89bb6e7db46123064a9e9d0b8aeee3099b15930a8f327101bb8f1083889a9`  
		Last Modified: Tue, 28 Jan 2025 02:26:35 GMT  
		Size: 219.0 MB (219017537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5278d3d3e6f5aa16d3dffb1e5f1a8459b9704ede571252f8d40c8fdd59db0151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2261091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c63f216445166f1a690286f8a3d6b72d40f303b4eb2a73a3b609b33c81595cf`

```dockerfile
```

-	Layers:
	-	`sha256:3351a9893981bb9772a29a0e0c1d08c2ec2e10941055effc78e02f742ea63f86`  
		Last Modified: Tue, 28 Jan 2025 02:26:30 GMT  
		Size: 2.3 MB (2251351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72931bf5338ec315bb59132ec1c818145b836ed3f7f16a133e9525ac19138181`  
		Last Modified: Tue, 28 Jan 2025 02:26:30 GMT  
		Size: 9.7 KB (9740 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:eca2248dcecab5f4fac7b4ea0803edc5b48cab07f4a701803d71845060257569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256353718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4cbcd5dcb1d71b09b974a803fb9c65e91f5b87ffd87f3ce528e9fe319931ea1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934b8c9e34860bc70f80bbf8f1dad818c1e6566568839a3ed52fc0a275340378`  
		Last Modified: Tue, 28 Jan 2025 02:29:10 GMT  
		Size: 221.9 MB (221905476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:071685bc0ba56c6d6c8426920b34af04e74e52cae8875d00793d623cc15ed66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2263312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163ae1acf78e206a60135c6df71d39c6a2dc68d0f8b27b4d786aa4f9a8c6dfad`

```dockerfile
```

-	Layers:
	-	`sha256:c0be3a52d505f56d124cefec88a4f382c381e2ece8f3bebb93a5f67a0858662f`  
		Last Modified: Tue, 28 Jan 2025 02:29:05 GMT  
		Size: 2.3 MB (2253644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa7e1a06e0055ce5d5f3a0d16e9a7c623072aa8385f941153504017aaa971de0`  
		Last Modified: Tue, 28 Jan 2025 02:29:04 GMT  
		Size: 9.7 KB (9668 bytes)  
		MIME: application/vnd.in-toto+json
