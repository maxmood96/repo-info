## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:c8be5056e8b53d44d44a776bbd0489067535324932fc4344bd046ff1773cb71a
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
$ docker pull buildpack-deps@sha256:93c927eb901b2d3fc6b4a53fe4e5f337d7f5de062d8739f7861d5346e0d01a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76124928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e763c18da0a23e9dc6d9435846b1628fa0998440645833a4b33af3077f5312`
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
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e87101798c1c992d7c441a146a64a4a76a20702382a0e0ad72a873e291446`  
		Last Modified: Wed, 02 Jul 2025 03:09:59 GMT  
		Size: 7.1 MB (7103261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a1aa76818dce63f07dd58dd5d43f128f03c6e179946ade2073fc935ecfd682`  
		Last Modified: Wed, 02 Jul 2025 04:11:46 GMT  
		Size: 39.5 MB (39485981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22849b083f500ecbd191ede13e63e460289dafb5dfac851d2e4f2ffb13f1a824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe891798b167cae0e771c6c3818811a772a2aa1ada6f7a052e4f1389f0f7322`

```dockerfile
```

-	Layers:
	-	`sha256:3cb934fe4b5c086fc0aa92e11d7350525774e059e57472c6b5bb22510ff36915`  
		Last Modified: Wed, 02 Jul 2025 07:19:37 GMT  
		Size: 5.8 MB (5812682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fec66f5317ca8e1e71435e89d1b139a44da82cb878c5d9913c3d62b41c3dd886`  
		Last Modified: Wed, 02 Jul 2025 07:19:38 GMT  
		Size: 7.3 KB (7322 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1f1e7af3cd8285843c74cc867e557f764d70f6471e2848782d068cb4c1e459c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75900149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b919b38dcd358fd90dd4b4adff69bd436adbdd409438da9eb323ae8ba933827`
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
ADD file:ae409b4c753aab53fbf5e46b332d29d614f9ed31f53ec79d39ec3fbf2d659151 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:446fe3fba694631d6dbb9bee9d2a2a5c22c79cba078007ea85d822fb4083a291`  
		Last Modified: Wed, 02 Jul 2025 09:16:19 GMT  
		Size: 26.6 MB (26642498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44793a28e493f85253cf4a362d676e8f72bc75cc19d68d009cf83da67ba00b18`  
		Last Modified: Wed, 02 Jul 2025 10:20:37 GMT  
		Size: 7.0 MB (7007547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7985036e44b083c2805969377e41fadbd2c507b1230b2f71ed066da3d08edaa`  
		Last Modified: Wed, 02 Jul 2025 11:10:11 GMT  
		Size: 42.3 MB (42250104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ad652f436e59b02fa5e7135e0e7271c62437c0da427b531cb3e0f1e90c365d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5821346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54218fcca7abcb2bd3ef3c459f7bb31c2ddce87591dadcae5c90f15492e6bcb8`

```dockerfile
```

-	Layers:
	-	`sha256:f47a980059c4a6c6e38f031e3642c3b98399709289fab673ba1956cd172f474f`  
		Last Modified: Wed, 02 Jul 2025 13:19:32 GMT  
		Size: 5.8 MB (5813962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703f7d88b799be27d220376841ac12e356dc8c5b43c8d8f2caf1075ed616e3a8`  
		Last Modified: Wed, 02 Jul 2025 13:19:33 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0c92979aed3534d7d9caa7ae3932a7d41b6020ef76af3d54defa018694fac971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73789061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81faed1c5b844a77648f9a4c8021c78dcba58a6a0a9afb93d175ebe903ac3754`
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
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44131f96e79008ec3b856a988d4d1fc58f4660f7ca12f41dfc747b162fe5ac2b`  
		Last Modified: Wed, 02 Jul 2025 04:18:53 GMT  
		Size: 7.0 MB (7049144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75659a4f0d38b8a15e802e7c5cddf95ad4371c4d4c4360e9c8fc87b7ad6f3f10`  
		Last Modified: Wed, 02 Jul 2025 07:36:17 GMT  
		Size: 39.4 MB (39380645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8a986821f64bff6477a354a208550ab45aac2b2ae2651a36aeebe1642a9db9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5826480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe203cc0f08d64f80b233f9ac0af86cdfed823b9d78f3d7d0dd1bddb3ec473e`

```dockerfile
```

-	Layers:
	-	`sha256:321bc112dd02c6a6c5b4e5a0ddeb6ae08ff75d8c9853b29dc833dc6f1879a5e7`  
		Last Modified: Wed, 02 Jul 2025 10:19:34 GMT  
		Size: 5.8 MB (5819076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10ea9b24522f28a9240241f242fdb4c9e59237abb813bf017598a94cbc49c814`  
		Last Modified: Wed, 02 Jul 2025 10:19:35 GMT  
		Size: 7.4 KB (7404 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8e92a8236e1e958f206bd3009bcf61574103cce95ab181a5b0700e2a4796db77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86390572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7249f85512526dd0a99e60afe0c682885c9bb4bfa4f213448df65221d067c75d`
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
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa2f9318738f3e4745fb8820b87dd05a41b99285bed1820fc6d1741f50edfd6`  
		Last Modified: Wed, 02 Jul 2025 03:09:58 GMT  
		Size: 8.2 MB (8181165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfd2a5f4efcf40a954b3ffecb64526e1b4b9dba6c19488754a9bb57b5ef9e90`  
		Last Modified: Thu, 03 Jul 2025 13:45:37 GMT  
		Size: 43.8 MB (43766786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:62238dc4bb76acbc836237d1ece55d96ce57e72db86b09ce69b584d6bd4cda21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e86e5b3d448ac73eb0329e5bec5645aa426b2d69594982741e9b21e4592f9f5`

```dockerfile
```

-	Layers:
	-	`sha256:fd2d81edc8bf957127d3b4af100ec78221e464dfc049b325b0045c20fe5f15d3`  
		Last Modified: Wed, 02 Jul 2025 07:19:57 GMT  
		Size: 5.8 MB (5820526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9adabdbbcc44c65598e0dd51a63cfadef829d2dc29cdf81fdccbacd4fa4ef59`  
		Last Modified: Wed, 02 Jul 2025 07:19:58 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1ff8626bcd734b4ab04553c807cb8fef461111f582b11a259d03783c6041a304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76460166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf558f2ec383b64a533021ed11430d66f565a78e64a4b03b2d0337436613a25e`
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
ADD file:0ded5e5d9800a3ca1fc6792130ca0e401e0261a23680af38f712027491983279 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dd93a8b5e7738819eda172cffad1b4d261aaf297806a57d80d1554e15f7f974c`  
		Last Modified: Wed, 02 Jul 2025 01:15:23 GMT  
		Size: 27.0 MB (27041006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1bda053366ed50c1b86a21bf7cb4fbc00d26d03ec2e958c6018096098af67d`  
		Last Modified: Wed, 02 Jul 2025 03:11:43 GMT  
		Size: 7.1 MB (7116147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a835443a6dae65841e6a022353da8bbef5344693459fd79d37f5cab1d17cd`  
		Last Modified: Wed, 02 Jul 2025 06:23:08 GMT  
		Size: 42.3 MB (42303013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb53b3e271ecf57d2e6483f08308830f2404272151d1addce84b3fca4e5d0137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88a82d18e31b1c996aa5a02573a277ffda90b7920a57f4cca3c1389c7c267ec`

```dockerfile
```

-	Layers:
	-	`sha256:4f7da3aa10a7e67ee8f56f2e08fb493390f96232f1b6a3045a4ffdb97e6ddc96`  
		Last Modified: Wed, 02 Jul 2025 07:20:03 GMT  
		Size: 5.8 MB (5803068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:171abfc586a90f481da2fc3a85ab68c737721c553004891021a35fafccaf5245`  
		Last Modified: Wed, 02 Jul 2025 07:20:04 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:530ad1ad389204a981d58251df86cf263ff7c67b42854add91aef76e6f0b70e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74438028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d261d0736302644b785eb1b9b582755a83a46853a477ceace6fbc6690c952d4`
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
ADD file:dad9a012cce363ba4f28e2a6f3efa82869330e872362e4867be1bd507ed8963a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8d24804db3a6eaf32ea752d2dd82fb21273e4e2494ca124217c93f38bc823ca5`  
		Last Modified: Wed, 02 Jul 2025 03:43:01 GMT  
		Size: 28.0 MB (28002175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdee4a43a9907ec4877c229f815931c1f4c005f17fb7d5bb41d54c28390815a`  
		Last Modified: Wed, 02 Jul 2025 04:11:58 GMT  
		Size: 7.0 MB (7014175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b2fb90aff9aa834bf3f9bc9e88ea2f6ae42d37f950666624e6bb57f7ca47bb`  
		Last Modified: Wed, 02 Jul 2025 05:18:51 GMT  
		Size: 39.4 MB (39421678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dd665418a743d67ba53a9269f0aa94767fea6f44ddb2f7045320deb319e4098d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5820925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8265aa637ed105530b0e3c0abccd9b658d92c354407f15837f1ce57f6cb4dd09`

```dockerfile
```

-	Layers:
	-	`sha256:c84161c20bf6408fc15dfdb30f91bc5f6d9ba5bafb4e8ab9f3ae887b9ba96df1`  
		Last Modified: Wed, 02 Jul 2025 07:20:10 GMT  
		Size: 5.8 MB (5813601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fdcfec9c92b9447ec701a117c154fba2d3e704122439fd9610f175cb7237df1`  
		Last Modified: Wed, 02 Jul 2025 07:20:10 GMT  
		Size: 7.3 KB (7324 bytes)  
		MIME: application/vnd.in-toto+json
