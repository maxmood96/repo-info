## `sapmachine:lts-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:9e95ee9aa02673ba43bbe6124713331d43ff096ed79c1f1054b2634400298014
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:6635791f038e127ee9333f0bebd05fff7b4a431b84e624a798daf7674b58d6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87083358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0499d366d0ebf3cae77d83b437ef48b8a1b773425ec446a39ed63452bd1f7f4`
-	Default Command: `["bash"]`

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
# Wed, 15 Apr 2026 20:58:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:58:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 20:58:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104567ca1bc0d1caa64b7954594a2845ffe3bec876d5279e61ecd2296f53b742`  
		Last Modified: Wed, 15 Apr 2026 20:58:38 GMT  
		Size: 57.3 MB (57346860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f5d39fdd917f025a656b4a0d14b20cad2e24c20edb5e3c79245b7204c6b31393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2562518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9172d7fa05c777f5c81e9ba2fec7c03e6a42291ea972e1064f97107ce2b0e460`

```dockerfile
```

-	Layers:
	-	`sha256:82709a62cf716e0a96c861146777b448bd5ed6f730ddc0ac3b056f9a89fc0bbb`  
		Last Modified: Wed, 15 Apr 2026 20:58:36 GMT  
		Size: 2.6 MB (2553081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b98d4887470a3a72309e7a3fbc9a2dd52c7dcb4149f2a8a0932b9857200ebd4b`  
		Last Modified: Wed, 15 Apr 2026 20:58:36 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:98d924f01d530e35c94a38b1dd5d0ca4d561c8720aa9e0d848fd58b7d18e860f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83867848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384c82359592454281416b980cb978f851973a2fbf9b0cb7dfa3fa9d0c218941`
-	Default Command: `["bash"]`

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
# Wed, 15 Apr 2026 21:08:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:08:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 21:08:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae43ff49025df516af99e35bddda78d0fe234614cf18ae4f17ae8560f6ae90b`  
		Last Modified: Wed, 15 Apr 2026 21:08:46 GMT  
		Size: 56.3 MB (56261305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e2133dbda12fd3abafe9b0a39b1c6482f178cdae20e65f59b39c371c860b0747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2562348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3d2871b1cb19ddc51575aadde5796d0b8ae6f07d82a6bdc928604e066e491a`

```dockerfile
```

-	Layers:
	-	`sha256:5c966d56a00c65aec55fea02163ab966629d69c0c251577132e10d50863aa115`  
		Last Modified: Wed, 15 Apr 2026 21:08:44 GMT  
		Size: 2.6 MB (2552784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60e765e98e6ac3367ceb51dbbc9b7f6e6ddde2cb123ac35c1c6076a058ae6531`  
		Last Modified: Wed, 15 Apr 2026 21:08:44 GMT  
		Size: 9.6 KB (9564 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c41bc5d78f3c03b71ce817a50b05ba0e3ad8227d01172c16f8f2b7923b6f52d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92873788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0305b391f38c642bdaf9d5d23859800bbb1345c079b9802a4608342dbb1db274`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:45:46 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:45:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 01 Apr 2026 20:45:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8f87dc4b0d2e9002cbd31c12f64b21963f42f01858922b649e8d10cac80f20`  
		Last Modified: Wed, 01 Apr 2026 20:46:15 GMT  
		Size: 58.2 MB (58224128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bfd0ea592104f09b1012116ca7ee9940e13eb9fe390bf03d562aea48dbe4d4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64633fe8669be48aa5fc89f0e3aa5b8f9028e563b6b297e334c56d6699fc143`

```dockerfile
```

-	Layers:
	-	`sha256:fb3df36bab19eb1bccd62ff6963c7e2c3e77c78eafafcfb066326fda6e1fa91e`  
		Last Modified: Wed, 01 Apr 2026 20:46:14 GMT  
		Size: 2.6 MB (2551995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4065864972c05a2429e2922f86d110637f26b583855ed9031c0ad1b65a260f`  
		Last Modified: Wed, 01 Apr 2026 20:46:13 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.in-toto+json
