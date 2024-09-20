## `sapmachine:23-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:334e233e353276f620987e5188fb0111614cc57a463834d1e9d93e4da35ad89d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:7823eaee99b8e221af5001aa2e7c36fb596f5724a0af4dc24a0dcd52b5c7d17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253154023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e78acdc5394103bc6c86d81d25bd554352ba713e35e374c012499e4501fa9f0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f85a600e843aa76043c8fc5c6f64863096d4ded82ef4c96126d8e11557dc72`  
		Last Modified: Fri, 20 Sep 2024 16:57:53 GMT  
		Size: 223.4 MB (223404195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7c101bef7674c594ca97879017a35aae152e2d14fcba20578ea8a12af8ec67a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52a273dc69cb456b88a862e02d6802cab639311825602684658ed8f758c9d8b`

```dockerfile
```

-	Layers:
	-	`sha256:1174a91e565e0f8d796511863931b92c3934ddfdaa7e68759d0fa2dfcac554e4`  
		Last Modified: Fri, 20 Sep 2024 16:57:49 GMT  
		Size: 3.1 KB (3101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b897dd24c08dde04c4389cbc641fd70273eda2772c95c711076e5d9ee32f3d63`  
		Last Modified: Fri, 20 Sep 2024 16:57:49 GMT  
		Size: 9.3 KB (9304 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0359e2cdd3ba79c8428b629bbffed848c7d722a3d5117db7d72f5c49e9498915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250074394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae4843841665606f262bc91b398f470a092af7b6796ceb4e3fa81ba445711d5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b16fc82a394e8ca2c51a94c3342639b8bafcf7642d18bb3e11580e0c8e6a6c`  
		Last Modified: Fri, 20 Sep 2024 17:02:20 GMT  
		Size: 221.2 MB (221188795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9128368f8c4b72c8fd7d743f6bfaf32ddd719135bb060e86baaa7e03e3cb9b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2223573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478208bb00f3cee934a435e7b199aef86396bb658e79fa631da6a8e85952b37b`

```dockerfile
```

-	Layers:
	-	`sha256:8a627f34a50b01923c9473b83c19cab697fbe905811e1a5ef149153a58f0aa2a`  
		Last Modified: Fri, 20 Sep 2024 17:02:15 GMT  
		Size: 2.2 MB (2213944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3b9427285c53dd8bc06b5309d59576acdd40a0c73a81ab4b2c1cc21d9a45f93`  
		Last Modified: Fri, 20 Sep 2024 17:02:15 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3bb4262eb774161601f5821c3665cfe48b4db8ae1b64265d1271aef156946f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258921643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54d923ed54dba4542c517bb4ded142da73770dbf5fa1efc42a22d9f4a337438`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837e885cd4f9a009316fa5f80aaabdd4a0722e98025ba6995a7cba15732c53ae`  
		Last Modified: Fri, 20 Sep 2024 17:00:49 GMT  
		Size: 224.5 MB (224529298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5b4c328d5bccd9cb7a1fa1d264daa4939647509e0a27c26553307ec6fe8ae6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2224765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5843a615bd6ac2b1d1b3d2419db17b4b2120a2ffd989064686c207887cd636`

```dockerfile
```

-	Layers:
	-	`sha256:4325b48dd51f6afd2c9ead988e4ad28f35936e193170fe35a8c48c9cb63034f3`  
		Last Modified: Fri, 20 Sep 2024 17:00:43 GMT  
		Size: 2.2 MB (2215411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:863a034c21e95accc5d43e2b35cee99b6accfa3fd4f06ac144e7f1c99f0a2c8a`  
		Last Modified: Fri, 20 Sep 2024 17:00:42 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.in-toto+json
