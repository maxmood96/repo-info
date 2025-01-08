## `sapmachine:17-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:90aefcce92b64af7f8ff2dea76c327a0c95af83a62d98c54861a54078d5b6e3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:7be2ae053d0f5b790513c9a9730a0c550669962ec639927e8c8c52e1256fede8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82685737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f00dcf300400489c97bcf3798f38965f0f2bb9341ace9bf03cabaef761f983`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:12 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:12 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:12 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Wed, 08 Jan 2025 01:47:07 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad605eabcde67ff8799a57b7de2f48bba31c03e32892d5aafdd57919629650f`  
		Last Modified: Tue, 03 Dec 2024 02:36:25 GMT  
		Size: 52.9 MB (52933769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eeeac204ceb3e5c7af6e729996d22f93ddf43465665c8b2d982db47786009427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696937cd8a93ae770f8d506ccfcc8ce1235efc1543ead24b983009dee121e0c6`

```dockerfile
```

-	Layers:
	-	`sha256:63b9c48e77a0b5a81d8ffdebaed56af2d9d0a2ba46f6c97e6d7cb263bf4efc03`  
		Last Modified: Tue, 03 Dec 2024 02:36:24 GMT  
		Size: 2.1 MB (2147757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2a865d458322242315c4a3c24625ac6a6e0dc31b6014c5f41e0ddf0023fc440`  
		Last Modified: Tue, 03 Dec 2024 02:36:24 GMT  
		Size: 9.6 KB (9617 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f6b34c35d3a9d778d275d71cd80e3e92497c4f5c1a6b36d6e35f263be339e04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81255402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fdcfe9375ae13c28a009260263b4f93185ad809d7cb799edc0200f02abb88f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:12 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:12 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:12 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Wed, 08 Jan 2025 03:22:49 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e65a1cfe512cbdf8eb74bd855246102a64335947f8879b3f05072b48d0cb868`  
		Last Modified: Tue, 03 Dec 2024 10:54:28 GMT  
		Size: 52.4 MB (52362731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a452f7930a1d3932df3d18f8249ca492c2a0724ea123b8b96cd1b3f0f652d117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c5209da2c05765b4af5c28c64ba71e4e611ebabce13aba6124ce5c32482964`

```dockerfile
```

-	Layers:
	-	`sha256:645b70541d87717bbf50d1487536af98c35fafaef88d25d9cf1d5d08f4479f7c`  
		Last Modified: Tue, 03 Dec 2024 10:54:27 GMT  
		Size: 2.1 MB (2148239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e5ed6a07d093c8e00e16da618910226e307c1cd44751b202b14c8f69b718d44`  
		Last Modified: Tue, 03 Dec 2024 10:54:26 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5dfaa0c5dd8f837313506391f9e59bb7e3674f82f2b51d243a1316a0e1ec5b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88765389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e962f4c6b377351d66da0667e0ae113f02504626c56f8be566e55975814c3af4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:12 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:12 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:12 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2371f99c00c3221988de9077fda6a937fe19fb620ee5d8e2eae2302a8450e2`  
		Size: 54.4 MB (54376569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8322ef95cc212de59bf000bf5fe8a3881f940ef08f0b58ada6cc6e5cdf41ee8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5421c9ad2a8cb198eaf808fd8cc7ca540c55a90e392ea27a91d0af82cff34a`

```dockerfile
```

-	Layers:
	-	`sha256:56ff17229c01ac21a0b1e381f843296cdfbaf726584ef05bcd950cf457057885`  
		Size: 2.2 MB (2151643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bc1771e982689e054bf34e017fe5d4f5398f9e7c764888be3742d1349fa116`  
		Last Modified: Tue, 03 Dec 2024 08:43:40 GMT  
		Size: 9.7 KB (9673 bytes)  
		MIME: application/vnd.in-toto+json
