## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:3656f68829b2a5609535626496a1f55d42f92f6ad8471692486fd8334d870e22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:77fb9130fe78863108f7f501050ece1197ec6cf54602ff9569dd579ec57a995d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4287e443009a9cf9c2c9cfa86bc4745d2830cc3142226f9126a0bbf43aaa68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378948ec170b4d8a3013772e2b302e397bab4c44a11f0249dede601a785f45d`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 5.4 MB (5360101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edee4f8a5435dcf4efe8aacde9bf929bc80f51622561ec15161b5d4c39394aca`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64d92368b359bd4d2c8c5c9a1192171b7b95942fbdf86d66157667501827e00`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e974ec6725aeedacccfdc674af6fa00d862b362ac3de6d22e82ca6bf916d81a`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 105.2 KB (105186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0057b985c6f43e1e74cae2ce0577e1ad0efe4aeb67f205e93d151a20eac4ed03`  
		Last Modified: Sat, 17 Aug 2024 02:01:34 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14cd61596e92f159e820332529cdb62730d33f911883b4e531f9e077d0774eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e6bbd7493a8f0b17e450b95e56e5c0278a13b6bf21b0844d5ae3659ba50029`

```dockerfile
```

-	Layers:
	-	`sha256:5aa75864d011ddfe1d301412abd7aef31ee304f67b8490199d6b10e8c4a3e67e`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 2.0 MB (2002674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bf80141cecef2fdf0bce1f92a0b845f40570df4d34b50dc495bc6a80235db9a`  
		Last Modified: Sat, 17 Aug 2024 02:01:33 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d11bf39deaf7de11ad41c96cf537df477ed85d0488ffa697612bb126b5d753e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdae2cf2d82494d1a3621947569a205d1774d1d85071b3844ba1efabb720655b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0639d72092b592b944940eaba5264bbabebedc923c867d5cef204e3869370ef7`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 5.3 MB (5340388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e7d1c2d83050467ab223500a26d141bdd407ae0e6e93886431805ca3d5c22`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f6e4e6a296c9284d095ca5915669b150327bff81a93c81da40429350457fa4`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6afbc297c547eebfdff6b788637e32acc191d56ab28e1b571477510a8ca5b`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 105.2 KB (105231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c21685943f244b1d8bc574a86763d24baf01d135736926254f4bf33003932ab`  
		Last Modified: Sat, 17 Aug 2024 03:26:54 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bd4d294f2b44f3421f9a91359180bad3483318ab42326f1f3d80b7b49255005e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e2060d6c33f98e63c1d617787975ff356a667c174713e3c991f12be90bd367`

```dockerfile
```

-	Layers:
	-	`sha256:87d77a954395223ffbab79c701033297186c31614e438db57959086ac47e7690`  
		Last Modified: Sat, 17 Aug 2024 03:26:54 GMT  
		Size: 2.0 MB (2002902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:250b5817ba7362a6358206761a137e7ef32ace96b20f593c8fbc72b107287182`  
		Last Modified: Sat, 17 Aug 2024 03:26:54 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json
