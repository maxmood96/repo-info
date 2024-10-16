## `sapmachine:23-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:b47f2419d31d0169d1671fc74e51c78e00e741c18b5555ba44b1ca8f0eca57fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:6d2be71d720a26961d332b487801f6bfc3df02037570c5980309b3dcc201fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88332827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d94c4d68438a565d0ac70e5b5ee2348466811dc33d3d21e894ced102c11b02`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21cf467b2ee099faf867135901880c863c1576e6f99bb65308b445c3721c3be`  
		Last Modified: Wed, 16 Oct 2024 16:17:41 GMT  
		Size: 58.6 MB (58582464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a57e848f5cbcb12a9c302c54f879dfa4a3bd9fdc4a193a066ecca9c63f8051ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5655fe27df5a4a0cce2ac09e36644ac3f2e4998cbbb3cf52062dcb81cd6e3e34`

```dockerfile
```

-	Layers:
	-	`sha256:45d880f7135a61a9d5de23c7fe19d0b748701a01f5f82f96067b8f6d2d622b6f`  
		Last Modified: Wed, 16 Oct 2024 16:17:40 GMT  
		Size: 2.1 MB (2130431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58254723bf980add8befe426427aac24df6104bce24c06dec18f91e2b15c5b08`  
		Last Modified: Wed, 16 Oct 2024 16:17:40 GMT  
		Size: 9.3 KB (9340 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9a3c3bbbc7e5f2c4033bc19cf63d91292cc9b60a5de5009ffcf1e44f3e89fbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86498493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7af1c732f5efc4ce4f2b5ff946b3928f26d557a68cfd06aad090a716b84e033`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e293da8953421a90cca5640625a31aa66fc40ea630ffa2eed1abab2b35581b`  
		Last Modified: Wed, 16 Oct 2024 04:21:38 GMT  
		Size: 57.6 MB (57612648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4b94e0a2737a7d7c67a9578b4a7fe81993ece7fc6065a781763c9ed09b74a781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0d37bb78c31718bfb6f6bfc56377da1e40574d212df866a5ff5bb507eb4285`

```dockerfile
```

-	Layers:
	-	`sha256:8f1e477373bac96e855467e62bfa42bdd6165578cbb11a4029b436885dc24df7`  
		Last Modified: Wed, 16 Oct 2024 04:21:36 GMT  
		Size: 2.1 MB (2130282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c1cbddc7bbc78863c96a31a367deb7c8950550db3e09487723b882284f79591`  
		Last Modified: Wed, 16 Oct 2024 04:21:36 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:37d80833614c1b6327d2121ad9ba62c0ab1cfea54ad98a5d0b4b2094e1532c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94280445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082a0f7bb13cd5aeaf0ee1826df7958d17819bf00dd55309a5cfd3cb646e925`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3722afa8721bce384bcbbb8ce3be1fbf22ea0b2863b729bb7ee44a73b00816b3`  
		Last Modified: Wed, 16 Oct 2024 02:37:30 GMT  
		Size: 59.9 MB (59891476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:97cb23d7bc1aa5599880a52b74ac90723fc047f523a200831344c94e0a8b0f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418ec272583275229823626c6cccb3e80a52c97e28027b44d148d64c248c9f53`

```dockerfile
```

-	Layers:
	-	`sha256:c40cc0d5df154eb057da78e1b4ea783886cb4a64b3ea0baba314759cb4598790`  
		Last Modified: Wed, 16 Oct 2024 02:37:28 GMT  
		Size: 2.1 MB (2133686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f476f44234cc37e5d277f256578f8d8f476f6923497811f78d401558b2521899`  
		Last Modified: Wed, 16 Oct 2024 02:37:28 GMT  
		Size: 9.4 KB (9389 bytes)  
		MIME: application/vnd.in-toto+json
