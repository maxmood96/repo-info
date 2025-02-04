## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:b1cd57fe6482ca6848831e1847fd8d8632e360c1976475d8464c36eabdd01c0e
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
$ docker pull buildpack-deps@sha256:91718149b4f53576557b3a5645fcb54ed8cfe681b6c1f734380f470ec388f8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76119776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0645d0ba933cbe9b814b1dfb1bd138139346974f8753b21f2b8e3bc651919ba4`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee445cc5e2b6b7936777d1af58476890507382191edc76cf636f7e69381a0f7`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 7.1 MB (7095774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c481194f5cf954d821c9180450bf9cbfe7d778d31dd54b13e0f37be46d837e`  
		Last Modified: Tue, 04 Feb 2025 05:20:43 GMT  
		Size: 39.5 MB (39488061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:913d6f77f627a5bf919be07bda166a50763665912c67c95de1a7a0c2eddf56fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837e383278b13cc069dd1f374210c432d5da73fd03f906048d2a1c86bafd3ed4`

```dockerfile
```

-	Layers:
	-	`sha256:a4523ac5f5958d30b606668facc78038341dc66d269f673e094bed9cc3df3951`  
		Last Modified: Tue, 04 Feb 2025 05:20:42 GMT  
		Size: 5.6 MB (5599765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c7a1e41537563d3da2abde7ffa18474777946269f533ae09dd1ebddfecd36f3`  
		Last Modified: Tue, 04 Feb 2025 05:20:42 GMT  
		Size: 7.3 KB (7324 bytes)  
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
$ docker pull buildpack-deps@sha256:3b4dc315b2f43492a8caf18705f18b4ecf52ef4f30ae0b852c5b43bd83f1edcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73790198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0040e9b18bab25e40c4dc3bcb25bbeff1e6e35d6c4156e9559e032772c502f6e`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2b4e5eab18cf336bf82b89529f3587544f710c5e1a0aa67e5ed1fdec85146`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 MB (7049559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b264c39c10afdefb042a206e923fa9957e0be85910e8e5065516f128089520da`  
		Last Modified: Sat, 19 Oct 2024 06:24:51 GMT  
		Size: 39.4 MB (39382310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:457c35d342663a69ec383a5df6b75820fdfb7f2dd8d5d94169416d8320c0143c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5622847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22210069278fbb79bfaf97a95dcaac2c228a24e7481e7d2f350821064c3e2c1c`

```dockerfile
```

-	Layers:
	-	`sha256:c4f843d61bcf7f9c51d7e2a70cbfda18a9a4dce752481ec5d0da09f4a91f0682`  
		Last Modified: Sat, 19 Oct 2024 06:24:50 GMT  
		Size: 5.6 MB (5615443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49eec21858e105c95bdf207c9a3a4473510b952446b3cdeb902fbcfbc1d5574e`  
		Last Modified: Sat, 19 Oct 2024 06:24:50 GMT  
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
