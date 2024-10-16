## `sapmachine:jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:fc2ea96797f4a7f9f74cb0b75869df7a6d48697d22359c1fbe96f1eeb5977c84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-24.04` - linux; amd64

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

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

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

### `sapmachine:jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a23eb5ff8b1951286f8a66b4f11edcca807bce41c7b0bb2095c9b20a4fd3b74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86498303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf57a6b84a35d40a1302dafa62c469a292f0496d80b7866714b11b6d6a5931f8`
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
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
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
	-	`sha256:0741829382faee1dada646b49acf3f4349f0c757e16139b7bb1874c6339d996e`  
		Last Modified: Thu, 10 Oct 2024 08:59:51 GMT  
		Size: 28.9 MB (28885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f279e962aa9a5646fc29533d41338e7ac31206dfde158192c78bdf056396301`  
		Last Modified: Sat, 12 Oct 2024 02:21:37 GMT  
		Size: 57.6 MB (57612687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5894b4f4c5eb7002cc4c94c1e338606b3555e9e206254c8f6f79c408eeb0973f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595328efc577a373f3c757bf11ac112986c96359496819a21700b2fb034c9555`

```dockerfile
```

-	Layers:
	-	`sha256:f2f239b7a0fe1375780d28b209e12b832a7133ebb8e0d6d7cb98e39274b25a0e`  
		Last Modified: Sat, 12 Oct 2024 02:21:35 GMT  
		Size: 2.1 MB (2130282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b538e3d699e77addaf120a9dcb256b0f8e8423a64280baa62ae74af19bef97`  
		Last Modified: Sat, 12 Oct 2024 02:21:35 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; ppc64le

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

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

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
