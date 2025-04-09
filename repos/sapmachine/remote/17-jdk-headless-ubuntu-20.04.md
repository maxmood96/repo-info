## `sapmachine:17-jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:b5bf2bc6b47096e8d1df99df7e11ed5ac2c9e1efe72fc43114ca0ec32cfa6972
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:fd69cdb18f17bb71149a595e7ffeae2ecc8b9f3f7a6091c3304857a5cd4c612b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.8 MB (225777243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c721fe0d76a18856518c35bd5ac0fe46ba42676cc6bbb9f7b126ad9ce2a4b92b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05406fbaa03843008c8f174f2b1754c657b21435d98b83427efbff890b09407`  
		Last Modified: Wed, 09 Apr 2025 01:22:06 GMT  
		Size: 198.3 MB (198266849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ed24252be0be7ef867101fbabbd908111b0d897cb5c11ec63d26f077db14402a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce645e36dbe61ccfc9ddce1bea2b02f8397675186fdd37bf06d2c1c1b0e49ef0`

```dockerfile
```

-	Layers:
	-	`sha256:c5f810e74ab049b749b557bdf32d9d8e64dca4553d52a1ac07827b008b34070b`  
		Last Modified: Wed, 09 Apr 2025 01:22:02 GMT  
		Size: 2.1 MB (2144334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a5ab86402979c516fa7e216534e191309d1f0f1e3c619c7fdefd212a6a64be2`  
		Last Modified: Wed, 09 Apr 2025 01:22:02 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8353755d9d0f964397a6ea05063587478321a2b4e0ef16c4315c18b859aa5866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222987618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e87afca07a36ba4e368ef6ab064409411d4449cfb9ca28cbcdca58f050f0c5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91785f8a87c92befa3998091af2fc0b4e4100f9be66ba03f25767cf64817c66a`  
		Last Modified: Wed, 09 Apr 2025 09:48:41 GMT  
		Size: 197.0 MB (197009957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6a5fe6e1c4eb3ecb996a065bc7846b2f233f0b8c2fcfe5d87ded525a8bf80eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2495bbd6f7ee93a4c5b0e6a780e3384fde4b9c2d8ec46b2de938eeb0a24791c`

```dockerfile
```

-	Layers:
	-	`sha256:67ebd2af8a4628409e3b6e0f200d7a3af608b9a93be4d282ba4c1d0adeae1123`  
		Last Modified: Wed, 09 Apr 2025 09:48:37 GMT  
		Size: 2.1 MB (2143963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bf562e497515e7893a0680867ee5d82157ce813102e783bf1ae15975253ac46`  
		Last Modified: Wed, 09 Apr 2025 09:48:36 GMT  
		Size: 9.0 KB (9037 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f0b6d42ea2bcfa0fc4263522b733cbec6bdb59bab377a56f1f0511ad3dab2634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230881440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c999886945ab388f63343ead3d83f2e87dc045412c52756385dbcc2f76a01d4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc669c7b4e0f5824f56de4c33403a2ba51efb205a85c876f22c11b255443b628`  
		Last Modified: Wed, 09 Apr 2025 07:25:03 GMT  
		Size: 198.8 MB (198804494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:49163a61e5684c4323c4c410428f38995ba66b2c3922ce4323ae557181a3396b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2155069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de01152049c3b340723720573d8c6fba21d1dfc3f00846bc59d3a03de0e3e369`

```dockerfile
```

-	Layers:
	-	`sha256:99a6fc3eaa436051253b8030b553fc77579b5aff528602733da3dfeea5b76d12`  
		Last Modified: Wed, 09 Apr 2025 07:24:22 GMT  
		Size: 2.1 MB (2146092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5be72a60708c22344f9b8982be692d4105ffef473d8dfb0e2bb07a011f288778`  
		Last Modified: Wed, 09 Apr 2025 07:24:22 GMT  
		Size: 9.0 KB (8977 bytes)  
		MIME: application/vnd.in-toto+json
