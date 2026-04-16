## `sapmachine:21-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:e9f80ce38a03f32410d82cb52e3b8bc61c890eb2f4223d5ce8db93ef10e83100
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d0f3f1406f621896525ed2f46d1f3b6957e0e9249c7817e8519d76c944d42ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245845842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f254eae4a2a91bf8671f6dfe0f0f29a18f20d83794193bfb6e9aeb7bbcf3e3a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:24 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 20:59:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5068b08c0ce571edbfc24a30344c7d828ceb6dbe760bae77ea1aae1de52c006`  
		Last Modified: Wed, 15 Apr 2026 20:59:49 GMT  
		Size: 216.1 MB (216109344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2b2c147ee657e9a0af5a0ff1413e4cecb7afc74e29224bfc2a482459616d8e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978b932e6a1000c090adda6c61d5b6227cf7c2397a325f0d2b1fc7fa4cf6ea44`

```dockerfile
```

-	Layers:
	-	`sha256:750a5aea45d1c3679eaed1951237bc494bdfb027c8b28c525586db32d2838578`  
		Last Modified: Wed, 15 Apr 2026 20:59:44 GMT  
		Size: 2.6 MB (2632170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3e3c409d1bfe749dabdfba5b8d596583b1a5cbad7770edb19758c54b0f393b`  
		Last Modified: Wed, 15 Apr 2026 20:59:43 GMT  
		Size: 10.1 KB (10135 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:614dd578c3b0c16782de2f390a356d934a6647661e682d8e7a581eeff67fd846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241929216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71192b56ae77cd5cf93ce9c0055405cfe8071e9ec5373c3889a0def5b1f3e59`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 21:09:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0e7bd975e8deaa14b5b9b9747877f5a9b197d9d0d8492512ebdfcbaafac85d`  
		Last Modified: Wed, 15 Apr 2026 21:09:56 GMT  
		Size: 214.3 MB (214322673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e622c9f7e6fb671c8c85e039269165e3138c6d069c49678216b0fc7c022f7f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2642187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7134d423ed19b310060e16d2b4d87c14d07d17256ffbcb65f5928fe154e8318`

```dockerfile
```

-	Layers:
	-	`sha256:50dfa184449a5a7fd5d0867f8e70a3414bd9bd1181ba34f15e872cfcd141e47a`  
		Last Modified: Wed, 15 Apr 2026 21:09:51 GMT  
		Size: 2.6 MB (2631900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6df903756ae5bf02620732811600ec92435966642b1602871b1bd23a2a62dd5b`  
		Last Modified: Wed, 15 Apr 2026 21:09:51 GMT  
		Size: 10.3 KB (10287 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a6bdb230af02359ec325a5086ae358f8b998f570a70043481a2114a268aff870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251721785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6936bd61137a27450f1d84d26d9509e6878dab297d7177e9615d1c10e339ae7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:36:09 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:36:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 23:36:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b9f4b3a454372f627011343d9499f3e44fb2447b1a6f3011a86352f1394e06`  
		Last Modified: Wed, 15 Apr 2026 23:36:52 GMT  
		Size: 217.1 MB (217073387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8c8e51408b4fd42ab77db528c622594f048a5e0c5125eb9dbc2f87d5198d5c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2639982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84612286c760f9d3494876e1055c90bcb1552de98f4e6297dce38497294a4365`

```dockerfile
```

-	Layers:
	-	`sha256:1a709a482ef193afdc75fddae01d2199a10887face762dcc7870738b6ebeeac8`  
		Last Modified: Wed, 15 Apr 2026 23:36:47 GMT  
		Size: 2.6 MB (2629780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d1fa58b5afa13293630bea8469ccd5f4ef0891417e4d35cf54e9c93fc0afe3`  
		Last Modified: Wed, 15 Apr 2026 23:36:47 GMT  
		Size: 10.2 KB (10202 bytes)  
		MIME: application/vnd.in-toto+json
