## `sapmachine:11-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:ddb16c0f40479cb3e28ae12568692b0b773fb706210ce8c9942458b3ae7f4f30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:6fbfc92949efd79502cc757458857568f4d5c7839fe630c099474c86b1c76e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229851033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a9544226d62174c9bd0eb735d5012fa5a81f01fa1c2b33de226b0fb19f7af9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:16 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:16 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef891440e595dff70666b4669b092a7c314ef4146a805adc9b96f52f7c6bcca`  
		Last Modified: Thu, 09 Oct 2025 21:27:17 GMT  
		Size: 200.1 MB (200127886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6de4b908dacfa99af38fad0052d8b2d90cb165c4e84adf517e19d73cc8ad4bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdae689d4bac3fd399e7c1ac041d0644128f21d1e7d5631949aac980b46c05e3`

```dockerfile
```

-	Layers:
	-	`sha256:752f3459e2a4ef9cfcd971e69e36061612aa782a656c229b3ad0782a113853fa`  
		Last Modified: Fri, 10 Oct 2025 00:04:24 GMT  
		Size: 2.4 MB (2367212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ce631ff1ad928512d51abef59138f2e1626ba0d50966e6949c2d03f7f16ceb`  
		Last Modified: Fri, 10 Oct 2025 00:04:25 GMT  
		Size: 10.3 KB (10277 bytes)  
		MIME: application/vnd.in-toto+json
