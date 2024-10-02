## `sapmachine:11-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:cd291282de1a048f89049f440429cadd9d00b3231a6df1232dc38b32ef2b960f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:d15a4aea767bb79870d5e0fa48fb168743dc25215aa35718581a9f5570369215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229678372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2a4af9b3a6d60e514042d862d1b45f3a2ec65ee8ad2c0b050211f96719636`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21516d4c6096abf0dcfb737d27fb19bca9cc992e29b4e3c7fb1a98d172ca072a`  
		Last Modified: Wed, 02 Oct 2024 02:00:15 GMT  
		Size: 199.9 MB (199928512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:44f5c2f1b5a30233c403376cbd2a5e8c92aeb991719919f7262ea6ddbd3ef3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfb1260239830b7d3bf4c36621ca8647846d701909526f92dbbad54bef374b1`

```dockerfile
```

-	Layers:
	-	`sha256:98e3ae205c520c45eb4f57804fb7e5d76b11c723517767cb41acb8f8ab5ce262`  
		Last Modified: Wed, 02 Oct 2024 02:00:11 GMT  
		Size: 2.2 MB (2227651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa491c76521e71035a3a475d48b52f11f5b7323258fc779298536f047230a81e`  
		Last Modified: Wed, 02 Oct 2024 02:00:10 GMT  
		Size: 9.4 KB (9370 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7c65b3935d43fdd61c8af4f1fe11c77f8d2016e8bfa4421d7ca50b80f57b4b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227319015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2bcfe7e06ed5d064853e69ccff88c7e622d47a79cbea824a149202d64fcb25`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729bf95e02ea7f7cd427218101e37b0a2ecad1c62e3b2f0b2d50604477e934b4`  
		Last Modified: Wed, 02 Oct 2024 04:05:40 GMT  
		Size: 198.4 MB (198433585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c02b4042eaa3e6cb40675f9a8ddce8866b1357f5ec87bfa841cc007b4d8237f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2238253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc0952ae400767a08c6ae29d6e001de7213188972a10f2ff3dc8c5cbf7a0130`

```dockerfile
```

-	Layers:
	-	`sha256:5f83303ffaa32c3af8db9af4dd708d48afb8af06a2e0ef2ae2f9e4c1ff82a5fe`  
		Last Modified: Wed, 02 Oct 2024 04:05:35 GMT  
		Size: 2.2 MB (2228761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f1b80a53ecb09ea6c296b4b510030423b31b6f806b867a705c0fd3a4f6c9c6`  
		Last Modified: Wed, 02 Oct 2024 04:05:35 GMT  
		Size: 9.5 KB (9492 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2dae49c841b2cc716109358bfb53334cef6b60fc5cc95d2fe6315bac4dfd1e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220910479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac68ac4fb1eb47aaec7f30d2c8bbee57c01691bd5c4ee08c60a9e2b163d6583c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879484fd465c58e9317ebe50858f87adfa623be3481623cc7a15183bae370ce5`  
		Last Modified: Wed, 02 Oct 2024 03:22:42 GMT  
		Size: 186.5 MB (186518458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e29b1005a6dd9ca97a6cb4f147bf87ab370b10d7c7d0ce193898d27b84cbea00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2238383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724fbc13de1a3b4b8ffb03714ee87091c25af79bb5ea6fb56fbf9c19692f9775`

```dockerfile
```

-	Layers:
	-	`sha256:8aab524524779248e2cb11da4fe78f5d6b02ad05942898b10afa351b7c108e91`  
		Last Modified: Wed, 02 Oct 2024 03:22:37 GMT  
		Size: 2.2 MB (2228963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b289040f333f1cdbd252f12b4510715c7392ebfa5decad4a510555980f186ef0`  
		Last Modified: Wed, 02 Oct 2024 03:22:36 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.in-toto+json
