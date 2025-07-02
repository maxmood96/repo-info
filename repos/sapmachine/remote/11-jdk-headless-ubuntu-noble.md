## `sapmachine:11-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:e11e419190f43d743cbb40ac70f0359368a843c32f739411fbfa55e06e680f6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:ac7fd5b2bc2b28d060fe142d2daae4af8decad5b55a750d7aa7df02d2b5a2189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229781488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9dbe7164efe7101dfef763b5e49d872554723be6642b721a25c16b1c9aee125`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:44 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:44 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6476489cadbcf498240947d9b3f55964fd484294694fe26b0f3f7e2f116cd7`  
		Last Modified: Wed, 02 Jul 2025 21:26:58 GMT  
		Size: 200.1 MB (200063122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f2cbcbce63f6768f669ba34b04c81af4e9485aac8ba865ce5868b6e00d439f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3c6bf2fccd34984d5b1c9f5a58f9e530b81220f08d3c4f0cbf7a53f94fed86`

```dockerfile
```

-	Layers:
	-	`sha256:fa78ceb3e07357c3e1faa27e95664effd2da5663fd26820c06e0938ee5a61a0f`  
		Last Modified: Wed, 02 Jul 2025 06:04:18 GMT  
		Size: 2.4 MB (2366540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9b7450d485cf31b5b5d86ad8605ac57e5ef1c9b8f3d02ae4ebc28c01bc194c0`  
		Last Modified: Wed, 02 Jul 2025 06:04:19 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json
