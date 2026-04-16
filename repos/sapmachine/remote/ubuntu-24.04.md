## `sapmachine:ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:2bdd08f3f30d4ec48fb06d137a5b4ab6bdb7d0cde4b770e7f27a4cba61226d95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ea0c6c9122290bb1bdae0b48d5a03442e73416ef942cca5d27f19ba65e20a604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256091353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64694f4cfd3ea0506715954d7e48461300cc04308d5ccb702d759d55f855587b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:56:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:56:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 20:56:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d26625260ee574b572eae3ebd5a287cc9d461ddfec5b3eb5e0d1c772174a37`  
		Last Modified: Wed, 15 Apr 2026 20:57:02 GMT  
		Size: 226.4 MB (226358375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4376c83593acbca942025a62a75c18075173410263995dfc805b3bc4b2409df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2607038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3f7589439b7cb31d322c1b5c16118407459473e4cdc4d26e1cb494d96962a0`

```dockerfile
```

-	Layers:
	-	`sha256:56d366086a4aea8a99d9f87fc67e16dde9a3851435ad7ab76ea286ddc2f8bc40`  
		Last Modified: Wed, 15 Apr 2026 20:56:57 GMT  
		Size: 2.6 MB (2594558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f2c466f07fabdba4de71b700132be120ea73805381f439418bdc954c0bb7bb`  
		Last Modified: Wed, 15 Apr 2026 20:56:57 GMT  
		Size: 12.5 KB (12480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:35e57a0f12598d20151026c7717bbf1b13f22f5be4f2793bb01ba9c27aefa16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253111081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22157d7b9a86b491ca9831d341def8aff64857a770b798ab2f76351b04c2e89e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:06:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:06:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 21:06:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98811f1f7f1b906ec42bbfac81da12f49a09c9edd0bbea284b80e9cd8a244ab`  
		Last Modified: Wed, 15 Apr 2026 21:06:36 GMT  
		Size: 224.2 MB (224235296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:61ac266d170f7d6b3cf03852f5a3089756c21b6a3175eb6e0d01a3d076374a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2607895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7c64fbca8d83eb7e130bfba05840e9a55a57c8164b9606336aba380f9c9e2a`

```dockerfile
```

-	Layers:
	-	`sha256:646f0606ac051f1b2a333392f8e61634f6abed53cb343ddc66e6b6ac12a5a757`  
		Last Modified: Wed, 15 Apr 2026 21:06:26 GMT  
		Size: 2.6 MB (2595167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bca6e44f0ac65007ab29b34de0566fa21cc16cb4b63d85e97f56b771470b7f7c`  
		Last Modified: Wed, 15 Apr 2026 21:06:26 GMT  
		Size: 12.7 KB (12728 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:875fbdcbcc9533e37dec914f814343ea7acc7efd09a910e662c4fd0f5b0809e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.9 MB (261929776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c34d2695382d32e88a55fccf6c7ea4149f108d3abd54f317f463d02aa62c95`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 08:59:00 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 08:59:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 08:59:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aa874c6c717d7685ce22c8aecaac19624a6dc23b2cd3d9efb9fa9bf5766190`  
		Last Modified: Tue, 07 Apr 2026 08:59:43 GMT  
		Size: 227.6 MB (227616442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f26af1bfca4d9ba78fbe7244cb46ab1f17a3775fe6dfd7aedd4db58764bb12e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2604136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c848378b9b4fe099f5aac44250ffa77b64796bc112876fbeb52e4365628fb18c`

```dockerfile
```

-	Layers:
	-	`sha256:e327fff54773a51d2fb44812b46b7a6f6c5867359c6fb01873bca3534e68d49e`  
		Last Modified: Tue, 07 Apr 2026 08:59:38 GMT  
		Size: 2.6 MB (2591540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:676a14dda70a204525eae2604854b652cc11cfd0b2467a7ee4e806215293bbd1`  
		Last Modified: Tue, 07 Apr 2026 08:59:38 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json
