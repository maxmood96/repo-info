## `sapmachine:21-jre-headless`

```console
$ docker pull sapmachine@sha256:598b2eff2d3d5db7786835b881b19801a0fb13ac691f491d928323874c8c6655
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:b0cfa5aaa95affbc46f811f5534247e6c086b3849ea3128afca9b26d4c173190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88739017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588639e40cd96e5c5f33f6e61070c332ea06ea601e5bdb0c7847b426ac9b977c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80519fb9a08e907bdeb1ba6d171793a8136674c68255a8aa472afa85492d4287`  
		Last Modified: Mon, 15 Sep 2025 22:27:51 GMT  
		Size: 59.0 MB (59015567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e1fce32f881d41e3e26b1c2ae9f07373cee6e3168f5878436627e3887de1a147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a605bc0cdc1d353196164e3dea25aa7b01428f923152f824521b88a18e0f3cc`

```dockerfile
```

-	Layers:
	-	`sha256:5e06848198493fdf25353584152d6829877cc9bc82e6fdbff221ba7c0279700b`  
		Last Modified: Tue, 16 Sep 2025 00:08:42 GMT  
		Size: 2.3 MB (2273854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d89efdacb4adfffcf0ed0a202c7350406ca70fe2da67249e5a1a2de304135509`  
		Last Modified: Tue, 16 Sep 2025 00:08:43 GMT  
		Size: 11.3 KB (11307 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f65c355b73e702e39ecc1e527dc27f42fbe2210c5213d72b506191221abc3314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87048149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056805b0a5feeaae8be204080ac0947cf7553883d216fde420b30f456b53f4db`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34cd8a72062e6262cbe2b4b3f1119cc5324a9d16401fd68fce59124cd376aa4`  
		Last Modified: Mon, 15 Sep 2025 22:26:37 GMT  
		Size: 58.2 MB (58186832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0bc926d4b58561c9638ca1b96ec95887f5225b76a7ef09181aa705fb1426177c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066dc392362f62ec3f90c937c911f9cabc2380411cae0c702a2f948fa5dbaba2`

```dockerfile
```

-	Layers:
	-	`sha256:302ccd2c8f505a67219ad1eb0fa4c9e827dc6a19834ebb1797aebe5acc28fd97`  
		Last Modified: Tue, 16 Sep 2025 00:08:47 GMT  
		Size: 2.3 MB (2274397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d6746520335e5100c5b902b71233f1e683cc6dac2d0357877267baac8e686f`  
		Last Modified: Tue, 16 Sep 2025 00:08:48 GMT  
		Size: 11.5 KB (11495 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:015069f9033da35f9f15ae9468ad9495334cb092ada5e6995ac8652b3e28b77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94359917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd89f69372eb4fc84568a02541b2c4d4aeec1e9182c27220c1539659b8a8edd3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03c6a9a73c12cfc676640bd3d2777e2a855f6d504610b7bf666b92299652244`  
		Last Modified: Mon, 15 Sep 2025 23:45:44 GMT  
		Size: 60.1 MB (60056790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c2037aed94ce425c3cbace0b4ff0438527511b908c57d4c87dc9539c9f10840c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75fd3a5c891ae8a9606618b9ce9aa00264e35ad06527a78b1cc6b97956b8388`

```dockerfile
```

-	Layers:
	-	`sha256:40a16f7d4420ad9940559b691f3ece30b61ded1d6b650c4d10a917871eed2117`  
		Last Modified: Tue, 16 Sep 2025 00:13:50 GMT  
		Size: 2.3 MB (2271872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:900ed03d3b1e8ee6f05c2a8f060b3eb23ff62c2b48e11406219f6fe4273c740c`  
		Last Modified: Tue, 16 Sep 2025 00:13:51 GMT  
		Size: 11.4 KB (11393 bytes)  
		MIME: application/vnd.in-toto+json
