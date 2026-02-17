## `sapmachine:21-jre`

```console
$ docker pull sapmachine@sha256:81086e9d5ad4313885732e4bb6cd6cffe031c92369238d979228e66adc1ca344
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre` - linux; amd64

```console
$ docker pull sapmachine@sha256:a9327dcfb20f662d97680afdd75c2e37e939ed594e619480eec26f24d18679d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90400245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396fae82ae8fed8d289d593e34c8f2d3b72377ab2dc57fe84f46ee6a27e40d99`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:34:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 20:34:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a5f2fd929fa020a4ee86f53a0a23d3f869ddeae7002a6021a96ae2713ca1a0`  
		Last Modified: Tue, 17 Feb 2026 20:34:34 GMT  
		Size: 60.7 MB (60672634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c612fe9db70ed4044a6fb916aacb8eb6a5fd4ee26ac83ce3fefa187f45f90181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19289e1c03f489dcb8507a5fe7b186a4cdf11fee28c60a376690adecced8ca4`

```dockerfile
```

-	Layers:
	-	`sha256:11a21d51d7abebe0a0cc3d8f829632082b533c14f9eadf245376b60fe30cb965`  
		Last Modified: Tue, 17 Feb 2026 20:34:33 GMT  
		Size: 2.5 MB (2521020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb710caf772dabfcf08eaf88a9a930d1447f645253f8a59db43e0a37a699751`  
		Last Modified: Tue, 17 Feb 2026 20:34:33 GMT  
		Size: 10.0 KB (10042 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:06a4b2ff8234c43f11ad912934e21cb4338149835592aa65857d79551e3691ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88733945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbe1fd993944fd267316a8c959ac3fa32a9e4a224c077e86c28ddce92131a08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:33:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:33:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 20:33:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805bc0f748f95f07c89d6f631651a4e25355cfc6f00b87584e95642ccd7938bf`  
		Last Modified: Tue, 17 Feb 2026 20:33:34 GMT  
		Size: 59.9 MB (59868825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ba62407d390fe7c15509e77c6801375359a235ab5c06e66060d41495c56ed275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2531734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5abe1685420cb6a1c11e4e05f3d1aeb63ea9a682408ba3f143fc8a2691a2c17`

```dockerfile
```

-	Layers:
	-	`sha256:9bbdeb8fb50b7b66e1e89fa1622189cb88a3561b5d677e295be0d1ff8d376765`  
		Last Modified: Tue, 17 Feb 2026 20:33:32 GMT  
		Size: 2.5 MB (2521536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a149bcc83973a79b78aa68c81044147440c83555f0439d90b83a124f5e07c8bc`  
		Last Modified: Tue, 17 Feb 2026 20:33:32 GMT  
		Size: 10.2 KB (10198 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0725f203394e7f1ef02cd3e5e00d2e0048a63b7616dd83ef8eb7ad1c383315ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96306596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b67a1846d2023a6c50aea4fe196a00d9275234c7b9adb34718c13522b96d952`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:27:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:27:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 21:27:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221e60e3045cee4ce668e19a9532450764383c0e1bad15d5a2a9a335d9b86c97`  
		Last Modified: Tue, 17 Feb 2026 21:27:51 GMT  
		Size: 62.0 MB (61999690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0f2986a178b61b298b2ac268f6d3d96cc0cf45db214b86d037945f656b8268c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf63ab41e9a211dcaefd4925afd37c7e1b8c9a2faf1b30bf14cc1d9d809de0f5`

```dockerfile
```

-	Layers:
	-	`sha256:12155ca45e8b0b88934b0617b4443cdec3659f044e90fcce031c38e343b5ef67`  
		Last Modified: Tue, 17 Feb 2026 21:27:49 GMT  
		Size: 2.5 MB (2520518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33fd772d0c1f0b984b61029860a818e9360ef951ba5f971db6fb02eced9ce7ac`  
		Last Modified: Tue, 17 Feb 2026 21:27:49 GMT  
		Size: 10.1 KB (10114 bytes)  
		MIME: application/vnd.in-toto+json
