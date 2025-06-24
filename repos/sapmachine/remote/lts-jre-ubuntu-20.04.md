## `sapmachine:lts-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:78155d5ef819e1b58580edbed12e83beccf44e0c73e83ae1f49531f382284ec7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:6c38f90a8d0ec94d38d15b436d2ec4806a04d3c54771909b2045084562c27ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86789562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab6b1ac94e46c68f664a426689bc1f2d9d0827d81955801ffd36df8132b2b98`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a08bab333d535d1b1f5b83904dc77cf752c4d8411d1120773d26118a349c0a`  
		Last Modified: Mon, 19 May 2025 15:41:56 GMT  
		Size: 59.3 MB (59279168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8b18e20b8dd5787b1a3d66c37a6dc19498fe9e245b16a88f0250408d34b4bdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a62f681e38eefdf35e5e913f027f01f35bc400479938d9a15f0cd49ab3c13b7`

```dockerfile
```

-	Layers:
	-	`sha256:8dda527c12b8fafd233b0b276d8d035f3de44c049deabf420922ba146bee6955`  
		Last Modified: Tue, 17 Jun 2025 09:53:24 GMT  
		Size: 2.3 MB (2301221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:061adac0a552999cc68cca841c2a61784dfd93910279d7c9f5977b125abcea22`  
		Last Modified: Tue, 17 Jun 2025 09:53:26 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0cbef6b90c7e22d4cb808e6ab71bc49e045b1dc2c0c9f0332997d336a9021921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84428688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e8003d1c56bb554a0a9b33619f87fe9c61b04e52d978113d3b52c34d38194d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15c9691b3fa793644139c3edf8252d43e896bad4caf39da15bf9789fa592005`  
		Last Modified: Tue, 24 Jun 2025 17:58:33 GMT  
		Size: 58.5 MB (58451027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dfefb7890e5d72a167916bf34fd72bdd34fe289ce4484936d24a5b5d81f95708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d6ba392b8275d718c180df9f12b0b95ca897f07f151a54a7ee1f7de09c3548`

```dockerfile
```

-	Layers:
	-	`sha256:53fb181fe2d62e38274d9ff75d0fe5fc86618258114194e9351ec20b1704e860`  
		Last Modified: Tue, 24 Jun 2025 17:59:12 GMT  
		Size: 2.3 MB (2300883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0994bc1737180a9e7537c7b07d74ecaf4cd985a7160b2c5c58cdb8b79b0bec`  
		Last Modified: Tue, 24 Jun 2025 17:59:07 GMT  
		Size: 9.6 KB (9607 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:cf51eaaf0bd1946e2f085481c7eab13efee064d68ba40b7d8ae0f08b926cfcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92554869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4970e3fe533855d2b3047f7c10012a0dd64cdafe0c80b61d532b901c6a3194a3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:47:01 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:47:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:47:04 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Tue, 08 Apr 2025 10:47:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2643e0ebd2c6f4bab50fdcd925c4d548973c6e50e2dcf1eb53005ff23605e8`  
		Last Modified: Tue, 24 Jun 2025 18:00:05 GMT  
		Size: 60.5 MB (60477923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b10abf4498b1e76529bfc2d7e053911924ab75b2f90733c6783fab40a655a3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2418b77cd69b9329e7da5f59a71257c811c01ae7353ced8acf22d2b2d8c69c`

```dockerfile
```

-	Layers:
	-	`sha256:7579be7a31e4454c989c07cb4def2b6585f0d3e90d6460e985bb92d50279bd51`  
		Last Modified: Tue, 24 Jun 2025 18:00:30 GMT  
		Size: 2.3 MB (2305000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a296b46cfd464752a34fe7d2c7642286ef5117ac2893d69486a4a9989c2114f`  
		Last Modified: Tue, 24 Jun 2025 18:00:29 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.in-toto+json
