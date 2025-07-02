## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:3a58fea52178b8a8202a07aeb034a16a361616c6c80ab123ae6ce8f9878518e3
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
$ docker pull buildpack-deps@sha256:197831ceb2691184afa87ec7370610fa4af8d8e6cb70caaf93c1ad790e84994b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75892687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456b57c921193e3391f43d9cf3cb8a371820250bfaf989c5239f62c4b9142112`
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
ADD file:a68d8d0994670732edac30efcee96eec3850856e5c33c1c7fee7fdc59173ac3d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f35c50ead1843adba7d4d13281d31bc17c201a55b8bd1a3961e1bcfd131b762d`  
		Last Modified: Tue, 03 Jun 2025 13:42:56 GMT  
		Size: 26.6 MB (26640475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ade18f0cb153eb0e80505edf909a0b5fb573468108f73d59398826c27dd2252`  
		Last Modified: Tue, 03 Jun 2025 17:26:26 GMT  
		Size: 7.0 MB (7007661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edfc049546e2833bbae11371047122a90cc58851d9baf3c81cf215428e6784f`  
		Last Modified: Tue, 03 Jun 2025 17:26:31 GMT  
		Size: 42.2 MB (42244551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:90676a64dfd35fd0d1bac36f70ae80ce118a481cb527a9cfdea87bd8867117e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5644006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf58996da7e8dc36e9797bcedb13c2411b6d2bca798ef952277d0f78f35964a`

```dockerfile
```

-	Layers:
	-	`sha256:04f0537105580f450aab06f597b8ebc3af42ddc8712662590b4ed5fdf1944e16`  
		Last Modified: Tue, 10 Jun 2025 18:36:46 GMT  
		Size: 5.6 MB (5636622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eeb6abb41c6b50a6efdffb6c118bf2780d5d70f427a82142cf580863f194dfc`  
		Last Modified: Tue, 10 Jun 2025 18:41:18 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5693a5e3ddb4d24abad14095c56faab8d829e06bbc7bcba01091d22625d729f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73784314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968c038421d104e870922d0ccd6ea5bd5a94a93e7bfc6ca5c4691c752b7ee8f2`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc8f9e3619942200ecbccd8a285496c9f5f75c9e60a1de3a2f4dc84b79a25af`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 7.0 MB (7049073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b94abd03e0d697b3738e4aeb08f56794e94f092a06971fd222b20f05caa82e9`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 39.4 MB (39379660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb3d2ba4ea7ddb23149a6c99a6f9a28e6689b973a8a9b550a8c6bb16b73355c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5649140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9960084e308ac6eaf8e9cd2945a2efd652ad64e1494eea9d9261d702f22389`

```dockerfile
```

-	Layers:
	-	`sha256:bbdd013bbe256480bd17ba28462ccdfff19e0e8bae0176cb6d907ba2e6a7e769`  
		Last Modified: Tue, 10 Jun 2025 18:36:52 GMT  
		Size: 5.6 MB (5641736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b16113ca4cd771849cba0618fb7e1ee18d02ed5b9a0ad387613cada60371a72`  
		Last Modified: Tue, 10 Jun 2025 18:41:12 GMT  
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
		Last Modified: Wed, 02 Jul 2025 05:09:09 GMT  
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
