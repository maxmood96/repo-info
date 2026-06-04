## `traefik:mimolette`

```console
$ docker pull traefik@sha256:05a8a7aa68446b82daea0551a4544d503d1f66d64f8aa4790704f202f6e4bdb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:mimolette` - linux; amd64

```console
$ docker pull traefik@sha256:4c12fccd374880861a9d6601120009ffef257585620e82940c101fc550eb825a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53254046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed06664d8fec89632fc97edd2516970cb7b3672e718c8c28575cfc7cf132fec5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.48/traefik_v2.11.48_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Jun 2026 18:12:52 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Jun 2026 18:12:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:52 GMT
CMD ["traefik"]
# Thu, 04 Jun 2026 18:12:52 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.48 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d025bda3a040bc4de8ca98766f8e62b460595723d256b41bcd6216d11d67f0`  
		Last Modified: Thu, 04 Jun 2026 18:13:17 GMT  
		Size: 455.5 KB (455501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad388da01896d152e2d388c90b11d6448bd3b19d7be22652a500bdaec31a767`  
		Last Modified: Thu, 04 Jun 2026 18:13:19 GMT  
		Size: 48.9 MB (48933988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df148cb5bf6a14a99143188c715f665ffb2d5825f7cc0baabeae6c23de7ca4c7`  
		Last Modified: Thu, 04 Jun 2026 18:13:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:d7755cfa117e3a93c512e93efb16bc4c64e35633ad817ca5f9bf8236eb59d6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **878.3 KB (878317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc87360fedfb95693e27927041697aae93961ba9f35753d21437acb0029601a5`

```dockerfile
```

-	Layers:
	-	`sha256:0584fc2d6a5ae2f87b4fc32471e21ac762c300513ecd2d7f582f8832ddbc8775`  
		Last Modified: Thu, 04 Jun 2026 18:13:18 GMT  
		Size: 865.7 KB (865707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3c5334db52296e84a52a4e0e38d55943c531e8b117e384fd67c0fd6daf972a3`  
		Last Modified: Thu, 04 Jun 2026 18:13:17 GMT  
		Size: 12.6 KB (12610 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:b8e8d724228f0260d0a501a728c2f577f9919f15d896f19d291af26cc0f4ec46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48895228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75e138c2939d98d82444ee41d527022c6ce6f7642a54a76e0871b6dda4d933c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:12:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.48/traefik_v2.11.48_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Jun 2026 18:12:48 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Jun 2026 18:12:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:48 GMT
CMD ["traefik"]
# Thu, 04 Jun 2026 18:12:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.48 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab6b2a73648ef4e4abe9ba3c3344bbcfbc5993266f156ae902ba9ca27751091`  
		Last Modified: Thu, 04 Jun 2026 18:12:56 GMT  
		Size: 456.3 KB (456349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b07d21468410249d53fed73f7c20ce1a9215f07d87070b589d656b93108106`  
		Last Modified: Thu, 04 Jun 2026 18:12:57 GMT  
		Size: 44.9 MB (44866647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fa84ebb0b82f0867809032c3338c46242370a77719560be5905a0a12f0d6ac`  
		Last Modified: Thu, 04 Jun 2026 18:12:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:6dff8ed5f4f3053206ec67e27cea608c4eb441de6f60f27614ecfcb9388de10b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 KB (12511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db29f082e0bd9429f5c94791e65d5850a2b40c401c92e3c6d88474cd8e32976`

```dockerfile
```

-	Layers:
	-	`sha256:e88b34d314006e895b3a8d5559c13c54b7ffbab777063cd194eb9a103f3d4c83`  
		Last Modified: Thu, 04 Jun 2026 18:12:56 GMT  
		Size: 12.5 KB (12511 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5cc8941be988defce979393dca253d7ff7bb897f506e4b58a3022a6c04b59cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48538625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ca07f25f5f9fe62968d743dc716a5b39c5ed1ce05f6f3fc57b8b6698eaf825`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:12:43 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Jun 2026 18:12:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.48/traefik_v2.11.48_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Jun 2026 18:12:46 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Jun 2026 18:12:46 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Jun 2026 18:12:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jun 2026 18:12:46 GMT
CMD ["traefik"]
# Thu, 04 Jun 2026 18:12:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.48 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebe24d8354838d53240930376d5cc1cb09fdf6897b3189516b178efad3e2519`  
		Last Modified: Thu, 04 Jun 2026 18:13:12 GMT  
		Size: 457.8 KB (457751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3924cd3366f57eea09ab70ec7a63c908c9ecf3f938f1592527406f94301f50`  
		Last Modified: Thu, 04 Jun 2026 18:13:13 GMT  
		Size: 43.9 MB (43880635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f270cf14e83a34d1895165474b8638ec04413f706767aff0fa0b59421d424b4`  
		Last Modified: Thu, 04 Jun 2026 18:12:54 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:94a6c54fce424a349d6e762c7c64a11baa20ed2526b3073ab27a9b6577c5bc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.9 KB (877914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27406d6e1a182c9a8874510ce1a3f0828d2e0e6bcf2887f69a2b1d7dd60527e0`

```dockerfile
```

-	Layers:
	-	`sha256:b39486d728be653f695669c03c45751498150c92df139458ab62684c5a7019d1`  
		Last Modified: Thu, 04 Jun 2026 18:13:12 GMT  
		Size: 865.1 KB (865149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1e0f1a20b61a22c54fdcec78a8db43ce52c9b0be55b46f796692df1bfd84ac0`  
		Last Modified: Thu, 04 Jun 2026 18:13:12 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:654cbb88837814255fa8167f078322c630e4feec5db5230aa05e618fe3331f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47067460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4882d5473abb858cff195c684a7eadc4f03115c9557beb1df003a12a2c597c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:14:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Jun 2026 18:15:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.48/traefik_v2.11.48_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Jun 2026 18:15:30 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Jun 2026 18:15:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Jun 2026 18:15:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jun 2026 18:15:30 GMT
CMD ["traefik"]
# Thu, 04 Jun 2026 18:15:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.48 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5c5615b636354b38c6e252f0d91db799b206304dbe496f9997696f5f8b7fcd`  
		Last Modified: Thu, 04 Jun 2026 18:15:05 GMT  
		Size: 458.2 KB (458181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbcdf19c43c26430f4250d53e23a7b487ee6930344da4890fca0a16ffe27f7f`  
		Last Modified: Thu, 04 Jun 2026 18:16:29 GMT  
		Size: 42.8 MB (42777981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64560f32cbd9af449107c052f0fdf4a482615d29ffd654957667c593ae917f4b`  
		Last Modified: Thu, 04 Jun 2026 18:16:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:39917b6ae386c09ff97b5b52b2b3764bdbfdc9730163e97126e7fec5b5e4f3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.8 KB (877781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2984c368a7d4643e0a7e5331b59ce93363240a2de9c4125bf500361dc63038`

```dockerfile
```

-	Layers:
	-	`sha256:10a936cb53cf6f7b9eab3cb13e38c27cf26af41c17fe3268fb45e350db2770b7`  
		Last Modified: Thu, 04 Jun 2026 18:16:28 GMT  
		Size: 865.1 KB (865108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d39f51db701afe12af2fedef46b425af0137d25754d1464bdee7a287e8ab4ee`  
		Last Modified: Thu, 04 Jun 2026 18:16:28 GMT  
		Size: 12.7 KB (12673 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:610bb887ddeccfb7a34e672bf317943238c4e5a046051fa02e0bd145a3ce1b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51622104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edaae53ea793184a865d7e04e16a2b88d7cf8af39e320d7014aac48b9bc8fb65`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 13 May 2026 12:19:16 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 13 May 2026 12:30:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.46/traefik_v2.11.46_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 13 May 2026 12:30:56 GMT
COPY entrypoint.sh / # buildkit
# Wed, 13 May 2026 12:30:56 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 12:30:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 May 2026 12:30:56 GMT
CMD ["traefik"]
# Wed, 13 May 2026 12:30:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.46 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fec3377cecfaabfbad434bb7a79f5b7898b4b04500ba155118bee98bec26258`  
		Last Modified: Wed, 13 May 2026 12:24:36 GMT  
		Size: 455.8 KB (455808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26026d060247ac7e37cd84b95cb78b1dbce548db68c95c6f1b6c4098198436a3`  
		Last Modified: Wed, 13 May 2026 12:36:19 GMT  
		Size: 47.6 MB (47578265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d0f8daeecf260c9c7a36d49980ab49e8bd0e2cb575f942405fa5bde3a8a07`  
		Last Modified: Wed, 13 May 2026 12:36:12 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:2ffee35f48f8a5657d6bce73db059d9d9cde0ffe19cdae039893ca19486b6178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.8 KB (877777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006b46f4eb409a90bcf42fdfc011a85f71160aa3c77c5e879a6462f39751c5b8`

```dockerfile
```

-	Layers:
	-	`sha256:76318477fe5b5dd95e4fde441a1cb74519d935ec3a03c8b7bb66a4117bde669b`  
		Last Modified: Wed, 13 May 2026 12:36:12 GMT  
		Size: 865.1 KB (865104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4d5b66166b7cd65eed166dee97e6ad16bf0bbc164f65ceba8c1dc9d79e2de4a`  
		Last Modified: Wed, 13 May 2026 12:36:12 GMT  
		Size: 12.7 KB (12673 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:78079dd4abc3aee753e0b5bf31d2a67882a8c0a3c80d108450765256198ae0c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51690072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becf08a7770fb6fb26bd4e2adc361dbeb5955293a0655ee5af75b45ec7e006d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Thu, 04 Jun 2026 18:13:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 04 Jun 2026 18:13:23 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.48/traefik_v2.11.48_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 04 Jun 2026 18:13:23 GMT
COPY entrypoint.sh / # buildkit
# Thu, 04 Jun 2026 18:13:23 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Jun 2026 18:13:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 Jun 2026 18:13:23 GMT
CMD ["traefik"]
# Thu, 04 Jun 2026 18:13:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.48 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd843a525eda361ac29b49bfe49b99f8a532bb88914500c38af99cc05831c28`  
		Last Modified: Thu, 04 Jun 2026 18:14:16 GMT  
		Size: 456.5 KB (456472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ed25f24d828083e9b51ae5e0479ce53b90c03fb90d6591db1f33aad8d2be24`  
		Last Modified: Thu, 04 Jun 2026 18:14:17 GMT  
		Size: 47.5 MB (47506699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb70d435aa00465770438f49553f8772f5d0f801deac7a86267930103900d1dd`  
		Last Modified: Thu, 04 Jun 2026 18:14:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:233b7632e65df26dd620582dec836a87f7e5522cb2e11e090d630fb92aa0c099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **877.7 KB (877662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8edff59c23db5a20ce89c15f2499e10ee4c1874cf23e3b3ce0205908ef11c2`

```dockerfile
```

-	Layers:
	-	`sha256:4f8ca271f6c89533532719e816b1bf83f3677faea0bae312924c5809fe6607aa`  
		Last Modified: Thu, 04 Jun 2026 18:14:16 GMT  
		Size: 865.1 KB (865052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90255b46b514893bd7cf386f299a294d5c884bfaa9e1e38ac659ae6beff71b29`  
		Last Modified: Thu, 04 Jun 2026 18:14:16 GMT  
		Size: 12.6 KB (12610 bytes)  
		MIME: application/vnd.in-toto+json
