## `sapmachine:jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:db522378f538d0ef0de4bdd655f73368b63cd20253c4f5bd1dcd3724ee5911cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:c5c852de22c571c3c6b188c3cad87344508c4789d46165afb1dc463103e82cf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88332927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc2414ffca868bd8c2b351de6e499a40b440e475923a2c8857aee1f3dcbb244`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6796433a16479bf926828537f603149f515986c68cb2b2446eb925e660c0cfd`  
		Last Modified: Sat, 12 Oct 2024 00:01:14 GMT  
		Size: 58.6 MB (58582470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:949039407535b1677d4bbad538a036b890e668f9699404ceceb388be885d0483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0862c678ce68b23ed9e5ed234c8f134aed594d7b1a8d7601116394551561c6`

```dockerfile
```

-	Layers:
	-	`sha256:84c55ad98859e03856f297e22e3ed2ca8b8a59c7597bb4a4be62ebc03edf20d3`  
		Last Modified: Sat, 12 Oct 2024 00:01:12 GMT  
		Size: 2.1 MB (2130431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a63e04da8622d42b9ce745c9b335a1e925cd6eefbf991e374885cb7a8d2c600`  
		Last Modified: Sat, 12 Oct 2024 00:01:12 GMT  
		Size: 9.3 KB (9340 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu` - linux; arm64 variant v8

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

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

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

### `sapmachine:jre-headless-ubuntu` - linux; ppc64le

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

### `sapmachine:jre-headless-ubuntu` - unknown; unknown

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
