## `sapmachine:17-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:3ff8aa9c0d7af461b7326a29e45f8db4d39e88726d7d356964348b5481b85fc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ca14f00efeda3bbbc6963908e6dfeaf79910a18245ac5a5d1dfeafdc32fd0fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84119371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17778d80d1cef86d4c77af315c1889bee2ddf1e8e5ac7d276f811a3866746ce0`
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
# Wed, 15 Apr 2026 21:00:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:00:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 21:00:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932fb4ac8674f589765c9bb2963e77e51ed56aed82759ef9ba9b1952ead5507f`  
		Last Modified: Wed, 15 Apr 2026 21:00:33 GMT  
		Size: 54.4 MB (54382873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9f665a8a17b8deb9722558d5142177685e5d434d654860ab5665a6bcc7b3a9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2430d72c669dd7baacc17ccb10cac987e440f3cf4293ad669dd80831e86a1fb`

```dockerfile
```

-	Layers:
	-	`sha256:0c356aed3f6927cca17055cde5b0b9acc8d2a481b04f54a3584fc86cdc6fdd15`  
		Last Modified: Wed, 15 Apr 2026 21:00:29 GMT  
		Size: 2.5 MB (2546027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f9194bea1e914a674eed5356bc629838d7c4a10db808d64083252b8da1c291`  
		Last Modified: Wed, 15 Apr 2026 21:00:29 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8fb62b374d6043ac9706a1d8b1a52444f2181911ea7138da0a3cbb76aacee387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81376899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd9f5f934419a68d0ecffd23c2efa88e74923b0743674766cd1e1f405268c36`
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
# Wed, 15 Apr 2026 21:11:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:11:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 21:11:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939c4498162662b73cc33b6a41fe3ead837e6e599c474618b0523788486dd3e6`  
		Last Modified: Wed, 15 Apr 2026 21:11:27 GMT  
		Size: 53.8 MB (53770356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0d9df4f5c269ed7279b3ea2137344ed5ffc5f106e767c120e3148a902553d664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92b37ba7c1c39da5e7aa63c9f38ac43a7644a1b5977246aef2b16a49241af14`

```dockerfile
```

-	Layers:
	-	`sha256:af7fdb6d97dd5f8a149f7fd840f6cecc83fdb9f7259c81d1954cc82f7ea8f576`  
		Last Modified: Wed, 15 Apr 2026 21:11:25 GMT  
		Size: 2.5 MB (2545709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab1db5f68d1b7aa2e50e68ee01fd8dc2c3628b11e4773b1d54b0d79bfe87ae22`  
		Last Modified: Wed, 15 Apr 2026 21:11:25 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:79722c9b450f9a0549bf807a56d8a9f5f8c0690eec687c130d2a2cbf6902bc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90215744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde974db47bd0ec1a3ef06004c020e2a5ee5995bfc4a2e0d93a07399d849f797`
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
# Wed, 01 Apr 2026 20:52:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:52:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Apr 2026 20:52:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16e4cf854191d65a9624f29e8354a7d90437b9bb9dbffcd309f7b08c844abb7`  
		Last Modified: Wed, 01 Apr 2026 20:53:05 GMT  
		Size: 55.6 MB (55566084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:844f600a1a9b2466f2ad4faf611e2cb2944cbbd0d2f5aec96d13f5a5adcdfd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0925811579710ce708ebdc6fb07a8e26e0e81cef27776213b1996bcd97a90e68`

```dockerfile
```

-	Layers:
	-	`sha256:41ea685ce9b874391ff0bb71997510714350636010f46a317012c4c3f75e0365`  
		Last Modified: Wed, 01 Apr 2026 20:53:04 GMT  
		Size: 2.5 MB (2545559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6336ab3340c15e6f3b24150610cbc3d27717ce73d1132bf817c34c4f780567f4`  
		Last Modified: Wed, 01 Apr 2026 20:53:03 GMT  
		Size: 8.8 KB (8818 bytes)  
		MIME: application/vnd.in-toto+json
