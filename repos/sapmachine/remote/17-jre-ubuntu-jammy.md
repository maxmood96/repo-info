## `sapmachine:17-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:e3fca83c3917fa0ec40081f5fa3e8cb65a4ab6c546445714f8107773c78c278a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:d0bac9f1306281fffe231b0504322f5193c59c389c2a6e30020068b959939da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83347591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b468734089b653a4ae98ef2b8d52101c41262aa702cdafa463e28551215d73`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f5cd7d520f75e3b774450fbeead784faad1a847d3c11a4c4335b42133ed8a8`  
		Last Modified: Tue, 28 Jan 2025 01:30:18 GMT  
		Size: 53.8 MB (53811903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e3356f5b7367ac68909212666eaf5bc7e046a246850464f292cc8aab3d68e871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0e9d59bc2919cb7700d14c899cf0100b59b9db45d94864f8e549dc6583ce5b`

```dockerfile
```

-	Layers:
	-	`sha256:52e86b521ea2484e29b4c3d049b049aaca8edf91c51104416190ca6ff6b1f2f8`  
		Last Modified: Tue, 28 Jan 2025 01:30:21 GMT  
		Size: 2.4 MB (2407332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1039c72f8508678bc53971055a19d1a71bed974b05f4322210b41de32879a49`  
		Last Modified: Tue, 28 Jan 2025 01:30:17 GMT  
		Size: 8.8 KB (8821 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f3987ce6e634087ce8ae27ddb69178e73bc9ba813eecdb6e8262082a3aae2d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80572463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d16cca978dbeeac9d99bc36cd31ec948d0e4fd862f8c98bd88cd8f28410283a`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bd67fee428a59248915de5d5a8c7fcf7cbc2d0fae29ece5ed5979333027aa8`  
		Last Modified: Tue, 28 Jan 2025 02:54:42 GMT  
		Size: 53.2 MB (53214134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c7d694e776e4f47c39cbd47188624345794fd6c9c0b59153c68bdcbb09980e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ca0686c140e46e10d20998d7c75b0d65da083ae1d873a70d3634e4aa370174`

```dockerfile
```

-	Layers:
	-	`sha256:86ad7b1259d345573bfe972fe3c3e891ead25d5a06a3749000b3a678bbed9eb4`  
		Last Modified: Tue, 28 Jan 2025 02:54:40 GMT  
		Size: 2.4 MB (2407014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f14cf65df77928f0d6fe9b6a692781979042825210a34c306b7adfcd7492a47`  
		Last Modified: Tue, 28 Jan 2025 02:54:39 GMT  
		Size: 8.9 KB (8925 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e33fce5eb41ae64d5060692592fea63943e71505582c03927b98af617b119cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89771368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d35fbb8bf4365656e84bca102da07e3872624de949e2738663e4f6314b9e8c`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0fc3b2cd9b81d749b0fdb5929f68e33b6126cd99eff6bb52081572e3e1e736`  
		Last Modified: Tue, 28 Jan 2025 06:21:55 GMT  
		Size: 55.3 MB (55323126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e0097f2da20ef4eae4c967a488aada2c01257a966c161c99608084a61f23bfff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2420178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3beffce89f9a9f741c0d803983593cb4ab64f5d2ef64581763efdfa77ed3e29d`

```dockerfile
```

-	Layers:
	-	`sha256:eacb10a93f253cb604c3896f189e99f8a5317310b1586741e888ad59084e0705`  
		Last Modified: Tue, 28 Jan 2025 06:21:54 GMT  
		Size: 2.4 MB (2411313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e99b6904d70d4a6a8ccf7a14d3ffad8ef7ec21ac78a1a71b63675b2cf0d64550`  
		Last Modified: Tue, 28 Jan 2025 06:21:53 GMT  
		Size: 8.9 KB (8865 bytes)  
		MIME: application/vnd.in-toto+json
