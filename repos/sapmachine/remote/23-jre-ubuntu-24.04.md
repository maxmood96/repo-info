## `sapmachine:23-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:7a663412c31e15e1a3c7d8e8e074736fe44d6be2a4a7784aaa530556dbb95dde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:0be31af2dcd2f8496bce2dde6e40e55556e4f4a610f045514f55a7bf9d1e82b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91900594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feff68585513d5772509b1ebff602f0b49a877f1a0d97a6161d1a2da5a158470`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a4324d1ba54181808bcd74f4dedeefa71e8b649635396aeccabfbebf50a415ea`  
		Last Modified: Fri, 20 Sep 2024 16:57:33 GMT  
		Size: 62.2 MB (62150766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d25b0148db4959dcb176e6bbd6ea901a28deab29d66cd0fb320e2042c4528d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 KB (12149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fad1a9f5f92427e8faad5595047b44181c933ad03df9458af8839db3ab389`

```dockerfile
```

-	Layers:
	-	`sha256:9404e6c02e02dcefdd8c23b4e1f97615248820d079a01f07301f8b4fc300c84c`  
		Last Modified: Fri, 20 Sep 2024 16:57:32 GMT  
		Size: 3.0 KB (2993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67e9ebeae4294455b5a32bb89ec3aa3249075fc30d4da099918bb936c43ebb7`  
		Last Modified: Fri, 20 Sep 2024 16:57:32 GMT  
		Size: 9.2 KB (9156 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:30b616473d87a33398271e6433244df1c72afaecefee08479cc82270f8968465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89921635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cfc56912442e1f51e4aebeec565cab5d17d54284fa44e4eaeab4f6db8806785`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:55e7defcfc0b8886cb2158baa2434e93780a2826d3cd3d745c35e032ccc49c4c`  
		Last Modified: Fri, 20 Sep 2024 17:03:21 GMT  
		Size: 61.0 MB (61036036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3f8c7854228a0d5db6ab0399d37e27386cc98dd6f6369ed664898557fdad3c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886df8e89a3da7f62ce100254fceab491ec6e9fe0a152112df4e8adc14e95a2f`

```dockerfile
```

-	Layers:
	-	`sha256:68e02f302e8e0037d92d77f69df90be4ae57a1322a62a3ce750d4e4d535d1d22`  
		Last Modified: Fri, 20 Sep 2024 17:03:20 GMT  
		Size: 2.4 MB (2365734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03cf11056e585a75e573d9856bb1b85f8e9d7c492b9e0f2c7a50400346ce488a`  
		Last Modified: Fri, 20 Sep 2024 17:03:20 GMT  
		Size: 9.5 KB (9481 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:007c4cd05d9c03c284c203df0084fb4f783671e2f194cf03d03e1dfa8ed5f6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98300066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c449a25ffa0f2816b889f479023e33eeab90930a07758ef241c6be07638dc538`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:013186b3185ad18d6ad20c8ee1874b1ac6f2da7244e0ce978c9cae5d7f8bf31b`  
		Last Modified: Fri, 20 Sep 2024 17:02:23 GMT  
		Size: 63.9 MB (63907721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:35714872c59f4ffbd7e2b4a4a62b3321df61c49f9e0534eb1494c10e2c13a80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0286353987e429edcee57fac8408c9f136ebceedc4f46226b25f6d99e683b85`

```dockerfile
```

-	Layers:
	-	`sha256:64080903c4073e4864978fc3f85ce026b9c4349fa8ba5f672b6273a62a2f80f5`  
		Last Modified: Fri, 20 Sep 2024 17:02:22 GMT  
		Size: 2.4 MB (2369192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e045113acd3acde719d68a8555152fde453ed40a0aa9099ae3e3146545282c9`  
		Last Modified: Fri, 20 Sep 2024 17:02:21 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.in-toto+json
