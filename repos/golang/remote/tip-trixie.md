## `golang:tip-trixie`

```console
$ docker pull golang@sha256:9316e5dde298d3fd258dc9856bcdfff3e6e43432b2524c8f361aba178c8221de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-trixie` - linux; amd64

```console
$ docker pull golang@sha256:4087cd1392800944794cdda0d16db429ec53835952524b677a0807f1903302d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336371571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41084e0d71a4079bb371635babb7079bc2da3a64a7bcf30ad3ea68e6029c61e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d573bf42b377ce6a5a0451c15388849686fa4058efd68999f3b014daeb5b55`  
		Last Modified: Tue, 21 Oct 2025 01:42:47 GMT  
		Size: 25.6 MB (25615545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dfe2fac1c486e9aaf41d1028ed30be2c442aa84af44462bc7bac8c148ffb13`  
		Last Modified: Tue, 21 Oct 2025 04:47:38 GMT  
		Size: 67.8 MB (67784857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3defadd0879af80d6ba82c0386acd71e1bc150afca897410afcff6b76d6236ac`  
		Last Modified: Mon, 27 Oct 2025 21:07:42 GMT  
		Size: 102.1 MB (102088501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daed0125ec0f9fecb5ad10be0dd03e9fbc038a3da639715455b9acfe33ee37f3`  
		Last Modified: Mon, 27 Oct 2025 21:07:41 GMT  
		Size: 91.6 MB (91597540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91e635f76112ebc5078e655887b1f6952d16f9de51993323f393e1ce30c3206`  
		Last Modified: Mon, 27 Oct 2025 21:07:34 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c962df37ef5208ffe9e6cef2419675d21b14153174d3ad0642a9c265c1e0433b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec92a26664a40b79abb2ad95f202b9e8488797a47ac65508593d636b9898e34`

```dockerfile
```

-	Layers:
	-	`sha256:b3242726564c0956011ec6100fac242cb969b7ef4847c89b2429d2de2b83c878`  
		Last Modified: Mon, 27 Oct 2025 23:23:29 GMT  
		Size: 10.8 MB (10784460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3688bea09ed878739f7e5007e84bb8d2d64e9485cbd2ef611243ceffff195a`  
		Last Modified: Mon, 27 Oct 2025 23:23:30 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:8547210c8d37f85c39041bdc3d083a06dbd4390b185dcf3eccd00d5eb7dbbfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292699680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2099572400bf8bc0bec6b1916b486e68bd75fc169908f5776b2d8b2c572e743`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a7465ac6b2e82f973d43c5065f3695c54c0b7cd73ce5807c08e283981e9b13`  
		Last Modified: Mon, 27 Oct 2025 21:11:34 GMT  
		Size: 72.7 MB (72733644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37e78bce73be399b5f32cb65e0bc936590deb899ee136e761115443ad3660df`  
		Last Modified: Mon, 27 Oct 2025 21:11:33 GMT  
		Size: 87.9 MB (87919319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cf58a5757afc0f82c3cdf892483a522edce130fc16d0a17711790cac4c4fb7`  
		Last Modified: Mon, 27 Oct 2025 21:11:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8ab058dfe83311c070f137cad95f9cd72088950964d51e4afc8c411cea801e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbcb8ebdbcd53b7f46da7ac3514cca1f6b5933f3d75e579c719e51d59c899fb`

```dockerfile
```

-	Layers:
	-	`sha256:a9adffcb8e4eabc9df9ae473242864e79609a7c9b88f5c7c54a8d6c32f702a6b`  
		Last Modified: Mon, 27 Oct 2025 23:23:37 GMT  
		Size: 10.6 MB (10580347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3da2b6db3529e8ad86356380a2d32e9c589bf6c461d43ec61fa7750711b8a8b0`  
		Last Modified: Mon, 27 Oct 2025 23:23:38 GMT  
		Size: 29.1 KB (29135 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8e5710433546aaedcea89b7e62625eee65256bf8b302a44466e078ed03f00f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327340473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6b7b92b3156ebb24d947d64c20e2637770c4397f66b27f0e398a7f5c05dbdd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdaa458e9d705eaf849a0feb582a90201ceaf7d81013659812b52d3a3600780`  
		Last Modified: Mon, 27 Oct 2025 21:07:45 GMT  
		Size: 98.2 MB (98234368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75eb2c973c6fbfd8ad3a7e393b43c7170aa83e9a02eff9c12f176ce891587b5`  
		Last Modified: Mon, 27 Oct 2025 21:07:46 GMT  
		Size: 86.9 MB (86855633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbff25d95cb32bc90ac0e23da169c4864543d4f448a1240536c9c0bc200cfd1`  
		Last Modified: Mon, 27 Oct 2025 21:07:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:0bde190dfd77a337955acc85be49945915980543d189aa6102777f20f5d6af41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1855987bff61a8332a284bb165b52a44c77ab2a3ca32aa455b536931c7a3d63c`

```dockerfile
```

-	Layers:
	-	`sha256:2822aaa25efdb424922bcff79caa8a525dee6bdd76a7e332d9d805b683e9e523`  
		Last Modified: Mon, 27 Oct 2025 23:23:45 GMT  
		Size: 10.9 MB (10904915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cb92b17812b7e29b39544a0ea7f5ba35f6339facbfe2a73d9ff5d7a805a09ce`  
		Last Modified: Mon, 27 Oct 2025 23:23:47 GMT  
		Size: 29.2 KB (29167 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:25a43094c6dc6dfc58c46539c25c11ad7bf7e18535929bbbe21216e34e19a6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.7 MB (337650360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d038f7fc283d6193506f2bfebba1774776b195a3f86bf4bec7ebd08976b7d49`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0c4647ea5bf10ee4302f28d7b05ac3b18ede5c510a3bb65671353e4dc5445f11`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 50.8 MB (50800574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68e11ad5a4fd5be41f07ac93311f8ae1f7dfd6455edf9f5cf950e26d70ee4c6`  
		Last Modified: Tue, 21 Oct 2025 01:53:30 GMT  
		Size: 26.8 MB (26775679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e99453a1ea6755d1a3a58fe6632281db5820c733291dbefe645ffd8397c7e4`  
		Last Modified: Tue, 21 Oct 2025 02:36:27 GMT  
		Size: 69.8 MB (69795039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbea05db910c4cf02f5f6a6441b480fa77768279e2e006d1dc66b3809c42e0b`  
		Last Modified: Mon, 27 Oct 2025 21:08:45 GMT  
		Size: 100.5 MB (100532989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306627769a351c52d3a3779e00eff7152c4e91ea12a59e21b051f7345636c1ed`  
		Last Modified: Mon, 27 Oct 2025 21:08:46 GMT  
		Size: 89.7 MB (89745922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8622218407572b6535d503c2e8f81291eb138d1e7e9c627c7890bc0307fd5b2`  
		Last Modified: Mon, 27 Oct 2025 21:08:36 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:d6781228042a296175a7bb23797853a347eb4ab88c082d364f120613fd7d8769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc70a6652e3afa3c1f2bd367082a885cc4cca8aab7184eed56b7bc4052c5d7d9`

```dockerfile
```

-	Layers:
	-	`sha256:befab8a1157ed0d577ac9a17296cb279a3011216297255842ec42131d722c402`  
		Last Modified: Mon, 27 Oct 2025 23:23:54 GMT  
		Size: 10.8 MB (10755724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32df74520c270267114bced9c5d7c7e4028297cdc07a991d054ec644bee37a72`  
		Last Modified: Mon, 27 Oct 2025 23:23:55 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:9ebe8506162219bb7b9e9e65eb46a817be72fc68566fbd22249a11f5e31e52c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334165001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dabfc22b515e8f06f6c8c0cc1857d0236ce670099ad8637e81f1b70da97386`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dfb88672cf0a942c4fdfcadf1912c35c9d30a3a001b18a9dad505fb960ae8`  
		Last Modified: Tue, 21 Oct 2025 07:47:00 GMT  
		Size: 27.0 MB (26996207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06029381e2f1b3a0885caf1b758b0461bfaf9db7b9642ca0b79ab28ed1dd4ecc`  
		Last Modified: Tue, 21 Oct 2025 17:35:58 GMT  
		Size: 73.0 MB (73029685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039b012bf4389914e42cad2d70023977cf7df6c1b556aa5cc19ea7f3f404c788`  
		Last Modified: Tue, 21 Oct 2025 23:16:23 GMT  
		Size: 92.8 MB (92795212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1f672a68eba01ff6a61528f0b4d6424e083bf2d654ca12da312b3edc3a8b90`  
		Last Modified: Mon, 27 Oct 2025 21:08:47 GMT  
		Size: 88.2 MB (88234264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef29cf7c72439ddb36a88ce546d873ea15707a1fe99c9ad9cc6d2d41dea6fc9`  
		Last Modified: Mon, 27 Oct 2025 21:08:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:99555ae884c9354f36eabb7985dfc7ca07a590bc54b8f8207f83db87b8bbe897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03581466fd42841996a8f6154219ca1f6304132dc2dc7d857eecaf5cbe93e6ce`

```dockerfile
```

-	Layers:
	-	`sha256:b373f9187f81c72cae669ca899cd2903faaff064c1e9c6001df8069bf6b04ca5`  
		Last Modified: Mon, 27 Oct 2025 23:24:02 GMT  
		Size: 10.8 MB (10780246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ebf2907fdd24bc78c7f23081dc8e33b8be193078257d7360bdff0155fe3bf7a`  
		Last Modified: Mon, 27 Oct 2025 23:24:03 GMT  
		Size: 29.1 KB (29065 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:d638dd796f7c020a307df3fa8018d6d4e9f607bbece6c10a4cd3d80fbeb256cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.6 MB (359633424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d1d19b4e0f86b383c1266f8d58d38ad49d344cb8d5e5d7489afd27631274ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 20 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 20 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 20 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb6fec5cd2588ba9a09a9491547b6e7005f3640a81c530cc1f2e651257c901`  
		Last Modified: Fri, 24 Oct 2025 21:34:03 GMT  
		Size: 66.7 MB (66662364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3fb0e7079a4b7a9ec6d9a3b797f899acb3726d9808ef2e02cbb7d243e4a418`  
		Last Modified: Sun, 26 Oct 2025 14:28:28 GMT  
		Size: 131.6 MB (131577542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba33301841d9f0f671dfe6e1858a3107b8e894cdb9a7921f01148f354845cef`  
		Last Modified: Fri, 24 Oct 2025 22:19:23 GMT  
		Size: 88.7 MB (88669180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc81ed4c6a442b20d544d8c1c2c705a05f1227be74ded07c4c8c3876b1e3441`  
		Last Modified: Mon, 27 Oct 2025 09:02:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:ea69acc5dcf0a2eaf45ab94227ab3886bf1371101df1eab3e63cb194dda4581f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddf889725776703f2d816110871311a018fa18370637144a25afb99a0988f67`

```dockerfile
```

-	Layers:
	-	`sha256:5c82105749a291aa7d4b68f7a657e6b49d797ca39d02b33bc08737c1026d80db`  
		Last Modified: Mon, 27 Oct 2025 11:23:40 GMT  
		Size: 10.9 MB (10854079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618230761a02b79897d3a75494c81bcaf6d460e3b2020f2d8e6d2ee372379829`  
		Last Modified: Mon, 27 Oct 2025 11:23:40 GMT  
		Size: 29.1 KB (29070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:0cbad10e9edf70718c21a72e4b9a67dbd5377eb65b90476cfb6e4451c6092483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310481230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e102b892bc44303816b11111a0fd997f2422e0e4796bffbb6bfc27e90fe02e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOTOOLCHAIN=local
# Mon, 27 Oct 2025 05:23:19 GMT
ENV GOPATH=/go
# Mon, 27 Oct 2025 05:23:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Oct 2025 05:23:19 GMT
COPY /target/ / # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 27 Oct 2025 05:23:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb7d34d2ff189fa2150ed8d82914c7669f312817531bbe187965e9d30825d3`  
		Last Modified: Tue, 21 Oct 2025 23:25:03 GMT  
		Size: 68.6 MB (68630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a428a2b54674ae254bfe00b37c676d8a73faab203065274f2abdfea9489339e5`  
		Last Modified: Wed, 22 Oct 2025 06:06:23 GMT  
		Size: 75.9 MB (75900463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a092d1611329304bb10b51ed24c5eb7129e31e22cce2e99b258f719f86a22d0f`  
		Last Modified: Mon, 27 Oct 2025 21:08:13 GMT  
		Size: 89.8 MB (89814961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adeec9a53eb118f80202e81f2ccca88123af9f102c7b37880ab96e8f3668d783`  
		Last Modified: Mon, 27 Oct 2025 21:08:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:05b32024db4ad03ac71c0e4582cd144e7ca7af2be38e457ae4ea926afeea8daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f25c35e3da9f884f65c6e55b64be051836779fd93f92cc285ee353c07220e85`

```dockerfile
```

-	Layers:
	-	`sha256:86d5d1f92b49ae0f02f9793dc2a262cdb80a4bb381ef1bafed933a7c968795b4`  
		Last Modified: Mon, 27 Oct 2025 23:24:10 GMT  
		Size: 10.6 MB (10594860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b93b7fc8154bd052839a93168a41b371b20042464d97d1116e2715a2e4ae7b`  
		Last Modified: Mon, 27 Oct 2025 23:24:11 GMT  
		Size: 29.0 KB (29007 bytes)  
		MIME: application/vnd.in-toto+json
