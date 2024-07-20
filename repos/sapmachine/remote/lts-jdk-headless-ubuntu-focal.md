## `sapmachine:lts-jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:732132c97f5b22e51d64905060e6219e00adb54267a708635fac0904f709605e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:db160d8707e84c697d2f4474aabd201a79946b948835243fdca83512f1b8bb1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241067979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6b423e455d3fc96855cb4944b1b95052904d3affec92a365b8c170fc527ce4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1885b5a4ae19c87fc20cec46ed50a06f994749ae89a359fc2b26eee2d804b572`  
		Last Modified: Fri, 19 Jul 2024 18:00:45 GMT  
		Size: 213.6 MB (213556210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:47b8153b0f6da1c03e9979fd0dc680690c684546ebd77144c00c0456f800dac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fcb162e410f2320b59184e366c23713aee3c3911e43bd16d0761add4b70478`

```dockerfile
```

-	Layers:
	-	`sha256:f05610327388ab75a82b120b25adbf4a9fb618f1e89df80967864761909437e6`  
		Last Modified: Fri, 19 Jul 2024 18:00:40 GMT  
		Size: 2.1 MB (2128606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29775c26040a08e36483af60db565d97d10124dc88e94261f074111b1fd01586`  
		Last Modified: Fri, 19 Jul 2024 18:00:40 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2110934021e4dd8ed5fadc78e0a369d60a9b16d6647ffb73e598c647424165a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237624405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28b2eb454c8f930855ebb026f14689697dc21f399ac362273f6bda8593970e4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f092e54933ca29d01066517a6fe056728d76b6d20a29b4656f675d408c7882`  
		Last Modified: Sat, 20 Jul 2024 00:18:42 GMT  
		Size: 211.7 MB (211650188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:096b75f5c5baae844a8f97be90d2dc3d84ec4a16374b165edf55b058c2964a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a3824527dd954ee9279e3f6a9f3ec10ade29ae00684f7945778e93b9dc86e5`

```dockerfile
```

-	Layers:
	-	`sha256:28704b9946eb53094a05c73d910b97af5181e278044b9e25bcecccb10b168ffc`  
		Last Modified: Sat, 20 Jul 2024 00:18:38 GMT  
		Size: 2.1 MB (2128257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5e7969efce365959b8cdba34f54b397cacdbce4ad25502c804c826bb48020ef`  
		Last Modified: Sat, 20 Jul 2024 00:18:37 GMT  
		Size: 9.7 KB (9699 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1e67bbb4d209339507e8eb80aeb1f12e296fd80e238c5ba5f48c1002c966b1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246417116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977c5d497418b91a4906b4623cdabed3b81ec7578718d2501bbf0f2a88a1a77e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a0cc5bc03d1d9ee0bb55d3284f13764d09951041ab7b27eed8178ef0b7edad`  
		Last Modified: Fri, 19 Jul 2024 23:26:45 GMT  
		Size: 214.3 MB (214339976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e2911f86c5f64d1ab23d5e5f873c7839fd74800e31f418a72f45c03fc83647b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4296dd27014ffcc6882533caa31da8d6f40b16625c9b126c96e57af9743fb6`

```dockerfile
```

-	Layers:
	-	`sha256:cb3d4329c0b074dc7fcc61216cafb1e0de269b989c27f8b69045d592dfd26bbc`  
		Last Modified: Fri, 19 Jul 2024 23:26:40 GMT  
		Size: 2.1 MB (2130371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a29ce87cab90887061d5f36e2ae6d366693393dc1f07a3b23826e0d1f5ca6aad`  
		Last Modified: Fri, 19 Jul 2024 23:26:40 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.in-toto+json
