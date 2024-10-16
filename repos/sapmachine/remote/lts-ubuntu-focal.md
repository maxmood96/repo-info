## `sapmachine:lts-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:946c5315d6c155f9f70ab7be7f3b2122b17d7d1c3e784c71310b57665f215b59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:fa4dedd785c03cca9818cdff3f1d859b82887b27210c4eac1c92864c33f279d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242271711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5c33f604e2e1dfe3f8433c3c68f3bc24b4e4f636d21b80f7371e1d0640423b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a79af9d199370aab838800d558be9d1dedf353a3d329743bbdb0c50dc78cba`  
		Last Modified: Wed, 16 Oct 2024 16:18:19 GMT  
		Size: 214.8 MB (214760651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3d810bcb745e2899683cfcd5fe10947139434867dcc1d6e7443bf96975b9116b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc3cb7790e6afe2a41b474fe6bd35935c2bee1332413324e58c13defcadc40a`

```dockerfile
```

-	Layers:
	-	`sha256:43984d84c9ebbc1cee699624eb76e00c263605a322fff5697e06b3f798c03b7a`  
		Last Modified: Wed, 16 Oct 2024 16:18:14 GMT  
		Size: 2.4 MB (2367834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:862643e87450fa8a4de6aad76c7c42afea50e2b09e2db35dd7d772d4aef6ac4c`  
		Last Modified: Wed, 16 Oct 2024 16:18:13 GMT  
		Size: 11.2 KB (11228 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:643e08f016c4c7c35e16fed6494c9b596fcee4bed53f7d1b12169942f57a3701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238812561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dad11fdc47dc18668acdb6ab47d63a0d49dec2dec3b2c618828ede68f668a06`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b70b32660320885bc3c5e8ecc4c2fbc2e18c21da7f79d596579036b70a9588a`  
		Last Modified: Wed, 16 Oct 2024 04:34:04 GMT  
		Size: 212.8 MB (212838733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b06c7b1c94ef596a1204ebba70973a5fec94ad6af46eec373f4e8b764da72ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44649b32650debbe1232c2cf83235ce9005835e7c9163ac14cef619882aeefb4`

```dockerfile
```

-	Layers:
	-	`sha256:8895d16cbbb13d06e7882f573e9076cc06a87b99562f8eb685215d8b94a23a39`  
		Last Modified: Wed, 16 Oct 2024 04:34:00 GMT  
		Size: 2.4 MB (2367566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074ce3153f29a2dda75428d08d4c8481a1cda238f1b0bcf3330398249159bf37`  
		Last Modified: Wed, 16 Oct 2024 04:33:59 GMT  
		Size: 11.4 KB (11423 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:89c4005d9ff060fe1c73e3003e58f9aa2ce69a8a4183b64dbad77483681960a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247779815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf2c1a2c7993ef967e5d5c88c809a77b37f08794b9e7a971faf8650fa84ab50`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d2bdf25fb326eabaa2f64450216d72858a6138c8883cc764e2186e5832ebc1`  
		Last Modified: Wed, 16 Oct 2024 02:51:07 GMT  
		Size: 215.7 MB (215703309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:adac0efc8b4859911e9c9a3e46e81afa62c9fbff082ac9a5100f7a6592c69725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624309c357f82cd5ee82afe4e9fdaa13a3fa5becacd4c508bd27970328cf8790`

```dockerfile
```

-	Layers:
	-	`sha256:6bb9f8d9963e7b6b3b40cfa424359666739eff5b7823dfef3db3a7be2ea2cf7c`  
		Last Modified: Wed, 16 Oct 2024 02:51:02 GMT  
		Size: 2.4 MB (2369698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d339c0562cec4ede7321ad2ad3b3dff3927c03caaf1b122e1fd196b64f9f24d1`  
		Last Modified: Wed, 16 Oct 2024 02:51:01 GMT  
		Size: 11.3 KB (11314 bytes)  
		MIME: application/vnd.in-toto+json
