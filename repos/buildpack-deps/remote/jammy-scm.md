## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:e13920e6521c3c793bfecf771ef1b1584fd8895ff5fb2c6cc930befb38189f75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e78485a90f0527022882b4bd1adae2ed1114c0dad49e44abeb4648a15e45774a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76120734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c473dc8c73da30fd5cc0326d7f992ffd8e1115026bd2244582df37eccfab2d01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4340d07249a0b63b75c4a83ce1639f4f99213cb0868bed6fe3ee40cc7d6ba08d`  
		Last Modified: Wed, 09 Apr 2025 01:11:28 GMT  
		Size: 7.1 MB (7102787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adc8f2734bf52dafa222e8dd003ab8b181bb0d921af2f753577e4bd1fcd6cef`  
		Last Modified: Wed, 09 Apr 2025 02:12:01 GMT  
		Size: 39.5 MB (39485582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cbe71ef82e5b8eba8722ed51d48a83a692d79c4f4dcbf503f35311ae97c58681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5609674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc889f46d3b45f195b499c2c8d14092d16ba4d662f892c9300e0b6dca8aa911d`

```dockerfile
```

-	Layers:
	-	`sha256:aadb9a0caafabea4a1511398a3ddc492d40286e245505713dc4d88f154f2cca1`  
		Last Modified: Wed, 09 Apr 2025 02:12:00 GMT  
		Size: 5.6 MB (5602351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb86da3f6c876148be30f6a32e1166d6f7ae46a2407189ed2b0f5153a931db9`  
		Last Modified: Wed, 09 Apr 2025 02:11:59 GMT  
		Size: 7.3 KB (7323 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5f3bac89871123296d110a512aa7559dc0436de7f2ad45da401d4db6df577781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75891903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3049e25bdb3e8dfe2799d700ce453a690f490347751b97f912460ccafff9211`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:b27bdc0157c0d964026ea411ed5874766d804b491dfc3d5ac10188c76746bbb0 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f3e10eb95482b14d0f5a969fafb71afd541d5efd38890d551e27c957ed3ae84e`  
		Last Modified: Mon, 07 Apr 2025 08:26:39 GMT  
		Size: 26.6 MB (26640334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a0257b47dee685d7e368ffe92af1b42f13635d0924dcc224cb1f47bec5da76`  
		Last Modified: Wed, 09 Apr 2025 11:33:42 GMT  
		Size: 7.0 MB (7007063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6dbfaad53355b6176070aab12deb5d8897de1af47dfe9f182209d36eb0d042`  
		Last Modified: Wed, 09 Apr 2025 12:18:47 GMT  
		Size: 42.2 MB (42244506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:08a7b9f3824b667b77db4aa2c002306864394f9f5c79359f2086710b3e5a6e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e8ec22b5c2a6c75f8e805fd05b84a0575cd03cf7efcb63eebd38ba5da20c69`

```dockerfile
```

-	Layers:
	-	`sha256:469cb081b7eaece72589851eb7ddbc043384ebaa0e7f87eaa39ac93215c9dc6b`  
		Last Modified: Wed, 09 Apr 2025 12:18:46 GMT  
		Size: 5.6 MB (5603631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34314e721a6e4ba1505b382890d7526f0162af1d136a9e0cd11f9b4df8ef002a`  
		Last Modified: Wed, 09 Apr 2025 12:18:46 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0deb582f233f5b2afbb4ce119463f0b822e744d4cbbc4d47decf71c46cdc3dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73784148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60682b02722290fa29ce93ca158c707fcb750cc68cc41b59d3026673facdd518`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1e987316bb6701bafa74dadea41ea57299699f23daacaaeafa9fa05f6213`  
		Last Modified: Tue, 04 Feb 2025 09:02:41 GMT  
		Size: 7.0 MB (7040539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4d40d9b4a2a385703a53f399708272fe0719e35d402c2b48c88c4f929e5ab9`  
		Last Modified: Tue, 04 Feb 2025 19:04:54 GMT  
		Size: 39.4 MB (39385427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:130b2c19eaf13fb90c8ebfa020d2983dfbb0db8dad74f1e3d7105235978a45f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb91bdacf014e99685467b964b41b5603d75b9e68913687e56dc0fe64b835aa`

```dockerfile
```

-	Layers:
	-	`sha256:2a1d6cf5f1d7d8ca8c91236c24f36cf6f129b64385f5cace9aef8b6bf1c9c81b`  
		Last Modified: Tue, 04 Feb 2025 19:04:53 GMT  
		Size: 5.6 MB (5606159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6700f27722c736af24a0d12c4e2ed0a43ab883bf3275e5506797c50b85709714`  
		Last Modified: Tue, 04 Feb 2025 19:04:52 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:37e819862b9dda03328e4fe0b4c4ab8bb6208b3f8f23c1c5f3a44e36f78cfb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86393397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523630e11337ef6db2a5a30ee7e8218c8c8e4078ebd9ea853140f0f622c5bf5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ffa4d0393caf877e61e6700b1ae1bbad96ecd37d30084744cf639ecf44dc94`  
		Last Modified: Wed, 09 Apr 2025 04:28:15 GMT  
		Size: 8.2 MB (8180692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6724ff28bda7ad2e376dd3bef073c1d3b35864c1981604a9b4cf8d5a1cc2cbf7`  
		Last Modified: Wed, 09 Apr 2025 07:35:52 GMT  
		Size: 43.8 MB (43770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:211ffad71962afd2bb5664f8d727839fca71f1b48f46e524daeca18956f0ce1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5617375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bd5c6a193ddc5dfb08c38328fc1e6db2445f9daf1a3bf6e5a99e1b53cf4a43`

```dockerfile
```

-	Layers:
	-	`sha256:83f4c74c9dfffce716a65b57da0f836fbf34ce566a10defc063076c9321c0462`  
		Last Modified: Wed, 09 Apr 2025 07:35:51 GMT  
		Size: 5.6 MB (5610019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a8d4000c52717c9d39acd47b4802144e7e31a9a209425571355aab2aa740694`  
		Last Modified: Wed, 09 Apr 2025 07:35:50 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:7e2002fb607c426213a163d7ce7b523b7033f3f5f177de425773c95a40553b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76459937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4443687a55d72c91a2b7c75e81b02c6c20abf2b70211ea5cb56f062cd6752504`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:438dc93fcaaee8b419e6a993c9ac3f3b30ca2c5b6b0c14df470faabc73e2a987 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e243dbf3d7e76afa075ed871906b2ada05fe2b8fdf244d349ead2e46f8b1c53`  
		Last Modified: Mon, 07 Apr 2025 08:26:52 GMT  
		Size: 27.0 MB (27039440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6701cae8eb10ef3d43e8f7780239a93a4d57d7d57a697ef28cf34010815ea34`  
		Last Modified: Wed, 09 Apr 2025 05:15:22 GMT  
		Size: 7.1 MB (7115660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a187c768583ebe0f244a5e81aae2e21f3010f7e5794a6d0c5abf7fc0fa2f062`  
		Last Modified: Wed, 09 Apr 2025 08:36:03 GMT  
		Size: 42.3 MB (42304837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5c404a998715dba582c3ec6f7c351fd8f2d21b311771565ddce9cec42b3446b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5600209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0b0c8b5f532c0de7b345cd97901c620f046d23e4dec4566f5373addf05d5bb`

```dockerfile
```

-	Layers:
	-	`sha256:1635603e5ddc985f38ae6ac7fb691ff551d61a8ec32d372364d30280164a7369`  
		Last Modified: Wed, 09 Apr 2025 08:35:57 GMT  
		Size: 5.6 MB (5592853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4023a5af4005dfb78c6aafaf630b5edd323b2d7b8559174589f85be489660dd6`  
		Last Modified: Wed, 09 Apr 2025 08:35:56 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0eab31458c8f530552b7e8f7cb850ee3c9ce8377e7a52480dba3a1d3400ba4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74445445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a4fa11d2edba3e9e565b7b698996d505e77214f06c6b1a758abe73e8915642`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:5d8d436f6811fd1894d694e7df7d347b9bd021b38bd57e01718331911c43a656 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:25cf79adc8d2979d397edb23d9d8f0127bc0edfd1addfa501b8a0cc74338576b`  
		Last Modified: Mon, 07 Apr 2025 08:26:58 GMT  
		Size: 28.0 MB (28000118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fb272dbfe25822659e29ed1a2882170147c9ba32a1f6b7176ba8ce67d75b2`  
		Last Modified: Wed, 09 Apr 2025 04:11:42 GMT  
		Size: 7.0 MB (7013519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644f5178f783b290fa66dcb2e00f3ad5b0cb5d5ffbb5b1059668ed73480674a8`  
		Last Modified: Wed, 09 Apr 2025 07:08:04 GMT  
		Size: 39.4 MB (39431808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e033989fe8dd51dc952e5b8d0038ce650c4bb916402e681e18607c2b47ff50e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5610594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d508f9e5afc8fafa8fd420348917d729914521aa24d38caac857c793399f6021`

```dockerfile
```

-	Layers:
	-	`sha256:18d06d57429a5925e2e2907e2e280dacfadb29bba7fcf9775a9bd93483fa2246`  
		Last Modified: Wed, 09 Apr 2025 07:08:03 GMT  
		Size: 5.6 MB (5603270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04e882e8c9f1ab02a58aa1fd5e9eafa124a7d99f22bce6a8fe59ace06593c815`  
		Last Modified: Wed, 09 Apr 2025 07:08:03 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json
