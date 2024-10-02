## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:a7973bf466790b8143043a176b3091e833236acf366247067448fe76903bc28d
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
$ docker pull neurodebian@sha256:286183413af81badc42fff3f1c2c214b8e8380bc918faf10b56c7c7cfe3fb2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695fac297d77ea2b21f8c7b53fbbea39564422ecba2f82c08c2686b366931d5c`
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
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
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
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5841415efed23c119a8469194131c18b87ee67753517a99d8fc01f06cf966fb8`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 5.3 MB (5340450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954c9f376345cca87bb2306dc082bd633d25c1c0b7a51281e45f302caa307554`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72af8df908af1001e54236b76d58c51b3eea7a5c7a3619097d305d4f775eac99`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c55ac7fc0e12deb1a3c7a55803df01877dbd826510bb33faf283e7a8300e28`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 105.3 KB (105291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e2477417bfa5f2fc5d0d63f9edff178409808de0c35bc34a1a757cfd524b4b`  
		Last Modified: Wed, 02 Oct 2024 03:26:53 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:493435274faa21682794a4be271b392285df984c551ddf0ef2741788492ede79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733485ab064e66c3a9f58370711f69892507e10abaf72855a6398b005916abaf`

```dockerfile
```

-	Layers:
	-	`sha256:a91ff4a74015d47addfa03915b086097cd2d93574003f5e670f729a8a494f445`  
		Last Modified: Wed, 02 Oct 2024 03:26:53 GMT  
		Size: 2.0 MB (2002915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b91e53da7f867d443449320933fcf94640d01084aaa5509e655b8ba07395ff`  
		Last Modified: Wed, 02 Oct 2024 03:26:52 GMT  
		Size: 15.8 KB (15775 bytes)  
		MIME: application/vnd.in-toto+json
