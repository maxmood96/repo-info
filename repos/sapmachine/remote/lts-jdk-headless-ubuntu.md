## `sapmachine:lts-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:f0dd60bd0c183ec362e40e0b4e17d81055dc57cd6e8f2a33424dc9a08c4cea8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:8c898043e68bb5db397cff5ef34a30f1f90c2a77c915f37aea7977c99efde5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243600492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c964bd412a866dac18788896c5c93c45976232de5a614a81656b13dfd65ff6c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6541462c41f9594c6d0e1187355771634dd4c6165835eaaaae480cbc5b3244bc`  
		Last Modified: Tue, 28 Jan 2025 01:30:34 GMT  
		Size: 213.8 MB (213848524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7f8c299541742627c95a4540b729ea8096d4ffb58c657a7a64a7649e826948cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93b139cc752f998e6e8160dabd272d69af9785afa55e0c949bfdca0c44020ed`

```dockerfile
```

-	Layers:
	-	`sha256:fa46fc73c4702eb38b268aad64519d3919fa90f61e10b307b25b59462930b81d`  
		Last Modified: Tue, 28 Jan 2025 01:30:28 GMT  
		Size: 2.2 MB (2232762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098c10dce5e7aacafbe6ff2806734f28b4cd6ab0829c1f4f1ebfedd5682033c4`  
		Last Modified: Tue, 28 Jan 2025 01:30:28 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6da5fb223e048a42cd63b366f3bc5be68c871e5603bb6531306a1b776546ad23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240975439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37357c9d7ba75ecc6300e7ad8cf9916d1ae4727909ffbdb06b053edbb361ba61`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:45 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:45 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:47 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Tue, 19 Nov 2024 16:18:47 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4c14fac3f518dec329e8cad4d713263537e6fed1758cf2c0b91b96d8ea2182`  
		Last Modified: Tue, 28 Jan 2025 02:35:30 GMT  
		Size: 212.1 MB (212082768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ca309902fdce1fbf3089d7b42b55727cbd96730461d74355facf62e26a0f4fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b4b02ead3b06f620e884b26a0d310914f1b9c06ccc65068df307be7e1a6e74`

```dockerfile
```

-	Layers:
	-	`sha256:032e4189e774112a7e55ef8e555809f8442383a2ff4150bd81a3aa615dd876ab`  
		Last Modified: Tue, 28 Jan 2025 02:35:25 GMT  
		Size: 2.2 MB (2233281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86de9a73b28363a709c6b58423d5c74522867e435186d2f41c3cbceb8601c192`  
		Last Modified: Tue, 28 Jan 2025 02:35:25 GMT  
		Size: 10.8 KB (10816 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:19747808ca8a96148c6b25ea532d33741b9b9a520faf9da847fbe9b1d0a065b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249472783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c42f489bc021297530bbce3dea11d4afcb723bb6a1594b29f0ed93939659b61`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 16:18:47 GMT
ARG RELEASE
# Tue, 19 Nov 2024 16:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 16:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 16:18:50 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Tue, 19 Nov 2024 16:18:50 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147d6e50169fa69c9b6b0112af75733fc93cc4a03f3c6168afee81a81f1181a5`  
		Last Modified: Tue, 28 Jan 2025 05:45:25 GMT  
		Size: 215.1 MB (215083963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:889f8f6b6af78a53aee6cb6b5546c10c8c301eec45b790d2d110f8811aa4d327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee48e502fbc56e4536a59e066ce4a0f5be098b4837c87a37e17566fd11c2537`

```dockerfile
```

-	Layers:
	-	`sha256:965b5f7c3b4b019e8245faaba903490712572a9986dd615243bbc346ae757cc5`  
		Last Modified: Tue, 28 Jan 2025 05:45:19 GMT  
		Size: 2.2 MB (2234722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4203d5c55e6c779dd27bd2bc339d1b21b8dfdb7de379792131404ed19acde0f9`  
		Last Modified: Tue, 28 Jan 2025 05:45:19 GMT  
		Size: 10.7 KB (10726 bytes)  
		MIME: application/vnd.in-toto+json
