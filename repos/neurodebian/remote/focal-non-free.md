## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:338dc7b3a17f69e8044b9b6fca450127540c5a903b62738d0275f55b04b72fc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6af11b8f91c1a72ab168ecc733cdf05682ec84fe424909677f7444517041cc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2773923a12eabf66248c89d3038c5f614157d96249c9515c71931da49b44c5`
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
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
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
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e75c7a65b7f181c600367e7b795f2ec28ccac576cda7fb3aec11e9a2e86292`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 5.4 MB (5360302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e715970f91fb31540499b96725af5116ff4522ca91c5fa45aab0984fa63fbd`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012a6a853bcbc781468c32453ea7f08d0cbf446b023487c8a755e36c2e614afe`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54deb2d52bb8bdab1846b4807802dd24c6f5ff2919e2c4a348f443a82593ec07`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 105.3 KB (105257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693067606a22cfad4fd9f685006963d17c5ee91ec5bc8876a72eb23105e11040`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:eed7c7d0767f4c9c7379afb4406bfdf0e112d2f11af2856e01407139922f4b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f877252e27fa23a05113835795f85e3ef88fa5655ef443533c839c7bdedca7`

```dockerfile
```

-	Layers:
	-	`sha256:ac5945033dc85752c1e4c94b04d2a3ec607a05fb2e3c1229393bd4df8283b354`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 2.0 MB (2002687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3ef73ab5b3c258347d3cd74684999217465ffcfa8275049c86c9935596271ad`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 15.6 KB (15641 bytes)  
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
