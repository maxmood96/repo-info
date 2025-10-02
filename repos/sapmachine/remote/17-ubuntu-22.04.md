## `sapmachine:17-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:3ec27b2657cccee7df068ac56aa22689909917e2f96aa43a4ad1921b0acfacde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:4623beddb2354a307f51d631800ef9df48775b0ee21cc43a0a9fd5a8eab3d6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229635554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3795efef6bfaae9c68e3245d8a86f08e58fd295eabbdbc6d11c711f1f6b22a8d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b07367f6435014b229f4babe0555cb83c03b193cfe5d79c755b07136bc8885`  
		Last Modified: Tue, 02 Sep 2025 03:18:59 GMT  
		Size: 200.1 MB (200098619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7126455be00e52aa7ce117677d887462707f356d45d61049062286c700f9f60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5ae2698d2fe0f1a3a203e40a5f613317f28e9565080b89c9c7ae00f129ed37`

```dockerfile
```

-	Layers:
	-	`sha256:4037d61d524f541ed1eeee84ad4eaf18ce373a8f1677177dcca9393f9e9c214a`  
		Last Modified: Tue, 02 Sep 2025 03:05:45 GMT  
		Size: 2.6 MB (2627863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0648555c3fca7f0627dcf1f31d0c697e54a68dbfff1b71cb769c818cd6b9eda2`  
		Last Modified: Tue, 02 Sep 2025 03:05:46 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e7c8ae2a4afa51fa3337415370090bc3d41cf5dd0f80da7778eb15d6292c5f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226155253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45404b7ec02c6e4a1fd5c9e5585ba305f6216776f48c71ff35378a26c1292fa`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a4eb5832b98780877e12265ab6d91cca886627f445acb98103f85d163f5e68`  
		Last Modified: Thu, 02 Oct 2025 01:35:33 GMT  
		Size: 198.8 MB (198772146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f8b617be73702b6f6d4a5b6b9916e1394c7541ed55183b30bde7deb934b0d791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e93795654220b3f57ddfc1583cbd42a74124b541bb735e871d813622b4e7816`

```dockerfile
```

-	Layers:
	-	`sha256:7e482815c8ddaa7c5247e4558292585359e5b7aae187c4af5f4bfa934e4612aa`  
		Last Modified: Thu, 02 Oct 2025 03:05:05 GMT  
		Size: 2.6 MB (2627593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9455819d3a7ce8c484ba2824830f27d0bd7142c59c9941067f05a4b1c692a497`  
		Last Modified: Thu, 02 Oct 2025 03:05:06 GMT  
		Size: 10.3 KB (10290 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9ea5cf3b62a5cdb8e634865637c371a5ba5553ee95ef2598d4679c8c81238ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235214032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b380bc4b0c0f7431ce6b25c0107bbb625e46240b2a28ace593e2ea34e28d9afd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4090fd090ce96f2f32daa2bc757c0bdb7c90e3223dc64050ae77d4ca5c8bf05`  
		Last Modified: Thu, 02 Oct 2025 04:48:53 GMT  
		Size: 200.8 MB (200767243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:01fb63e06069747a5a394579714164cb00b66611f3c060975cf22702b3e2b944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f20d4a522fa4a72465d81aebb2c67381c3232b4cd4e05bc446deadb3a5409b`

```dockerfile
```

-	Layers:
	-	`sha256:0f9d1fe8de321b665942bb91a1fe40157a9f069cc0a6d658e18c0802cc7ccf02`  
		Last Modified: Thu, 02 Oct 2025 06:05:12 GMT  
		Size: 2.6 MB (2624056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:652de9e4f46f68555f0a1f662265a28ae15f8ea3785a87e16f42c9e06bb48044`  
		Last Modified: Thu, 02 Oct 2025 06:05:13 GMT  
		Size: 10.2 KB (10206 bytes)  
		MIME: application/vnd.in-toto+json
