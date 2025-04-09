## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:19d3883010017a62ab39d0c689f73a55f1e4e9a535c83f351027d4d25369ee59
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
$ docker pull buildpack-deps@sha256:3d81ea86816f56ad7c394a21ad1d1ddaf0f8af3eedc1b956bc3550a64d7384fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75883508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5798be91045125fde167648c1aa3d66bc7a087af07beacbf39623f621098d303`
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
ADD file:7e9e4d557a66a31de2a39930803dbe849ba710af36b4731e9cbc856f55c10018 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:eeaefd3c974dfe1d5e1b8eb1929496ae7befe434399b37e601701f6d012e3169`  
		Last Modified: Sun, 26 Jan 2025 07:02:14 GMT  
		Size: 26.6 MB (26639267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03a59df32a3c278c1a8e1b5a42ec5159ca064a182a7ceee73e4ebe1d86afa12`  
		Last Modified: Tue, 04 Feb 2025 10:44:17 GMT  
		Size: 7.0 MB (6998537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29d430e6e7df77b4a0c661b16f2f8366b006b35a623d472b34c14652775512b`  
		Last Modified: Tue, 04 Feb 2025 16:24:21 GMT  
		Size: 42.2 MB (42245704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a1e96608596943ff41ec6b718e5c768a2417ecb279f77cf16e946377426847a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d3a53dd690b45071fe80c195af55a9b1564637c7164fb8f2ee249626b0734d`

```dockerfile
```

-	Layers:
	-	`sha256:25af7052ba979d72219f9331970e3db455665cd6933408c5e0b43ddcc8dbf70f`  
		Last Modified: Tue, 04 Feb 2025 16:24:20 GMT  
		Size: 5.6 MB (5601045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f8ea58ee4c3ca68b2a31edb24237033974a5b3c467f19731c1384cc25aa287`  
		Last Modified: Tue, 04 Feb 2025 16:24:19 GMT  
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
$ docker pull buildpack-deps@sha256:dd92a1650b30a76126bdd7688f27cad359f7e325ff9e28c7ccb8b6977e7b90ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86412740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9403391651bf07f739ab79966f17421b317b61631b9356df7b91b2371aff44`
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
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c3f11d98bfde7b2d484e86a27f312061b41c7e65028517cbad025bac990450`  
		Last Modified: Tue, 04 Feb 2025 07:27:33 GMT  
		Size: 8.2 MB (8197665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e478e008c5d6761fb7b668913245a2e7b1eb03ac82bfd5b3dca2c5c60cacb60e`  
		Last Modified: Tue, 04 Feb 2025 15:51:13 GMT  
		Size: 43.8 MB (43767140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0efdae542543ed6a5b51a78003087ffe1cbb8b74e905565e74dcaf2169afb005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ba4966c6ff3d9004805330494eb646166177b7149f0a17614b6f60f36916d7`

```dockerfile
```

-	Layers:
	-	`sha256:a4efc30a1ec0e7420850c97bc015f3f7f1a649a251431a74d21a23601cff5b21`  
		Last Modified: Tue, 04 Feb 2025 15:51:12 GMT  
		Size: 5.6 MB (5607433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b007e3bf752ccc56738d576196f41ac22db95886c54e46de697d72503d3611`  
		Last Modified: Tue, 04 Feb 2025 15:51:11 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:057096cc3c93f1f8fb66031507a66e3964e19ebf13ba1506c10185bcd3d680df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76454330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d30085e843b181c9d6f4f2db62a64f5abc2075b8becfb389d85b5c26010172`
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
ADD file:c95ac39f820c01b1c0a2d18f3df09346a389f9989c91cb636f75de0e3d63c97d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cfa2d73aa16649863373431bec34ae49863b8b03f19e2c1fa29af96b0ea254fc`  
		Last Modified: Sun, 26 Jan 2025 07:02:26 GMT  
		Size: 27.0 MB (27039007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247fcfe5b002f706b4c9b3a78341f202606a547ef405c7ad03e2e33f28fec027`  
		Last Modified: Tue, 04 Feb 2025 04:44:46 GMT  
		Size: 7.1 MB (7108060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb811904a9072aa1e8962df9982276480172376fb423cfcf8aaec3ebb4f9f8ca`  
		Last Modified: Tue, 04 Feb 2025 08:14:03 GMT  
		Size: 42.3 MB (42307263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db7959de9f0bbc7f117458f02e843839a036cecd8be06014481d54e3e65988d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5597655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576c72a4fdb601de9b844fe21519fdf8a6175dedd057cee5a5aedb19f9ca8df2`

```dockerfile
```

-	Layers:
	-	`sha256:0f25233e0d3c13d7ff6ec6d10bf9d28c99eade027cb6b2c16f932fb3d4593f81`  
		Last Modified: Tue, 04 Feb 2025 08:13:58 GMT  
		Size: 5.6 MB (5590299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bba3b78cb50e20ecbdff1ccf6fa4223854971f17408346d0efc034f2c824f27`  
		Last Modified: Tue, 04 Feb 2025 08:13:56 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6102c2a37e0c3ad300dff3483bdad8123d61076b7a324ba074b7c9b0b65d3ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74429734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e92079504e248aa3e1839d4474b3d926c07679ced29323feb51c42b3841b82`
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
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e0e0eba9503675f1ef20409d7abb0dc538cffb5361ed38070285248d79ca72`  
		Last Modified: Tue, 04 Feb 2025 07:33:18 GMT  
		Size: 7.0 MB (7007841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ceb4257b5f6dbcfe0b6e240c36bcdefe3066bed00810364bb9111fc2b142678`  
		Last Modified: Tue, 04 Feb 2025 11:41:04 GMT  
		Size: 39.4 MB (39420962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:150da59697f1fda4ccd2b151d902b5463a708a5b5b4f918b4cacbda4ab3ea8e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8acfd7255776abc5b50d08c625a299c1efb593b61475984c2f4253c647aefdd`

```dockerfile
```

-	Layers:
	-	`sha256:3b20d61e305f63b842292fddab5a24a44dd99d12e07539a87853a780cdc97c4c`  
		Last Modified: Tue, 04 Feb 2025 11:41:02 GMT  
		Size: 5.6 MB (5600684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f48cc83a24245e928a33854befaeb67bfc51d8a7139f4f7d39f930180822cfd`  
		Last Modified: Tue, 04 Feb 2025 11:41:02 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json
