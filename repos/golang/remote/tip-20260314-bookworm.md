## `golang:tip-20260314-bookworm`

```console
$ docker pull golang@sha256:e9c063ee64a874f73359ac80014d6417672c80a13676440fd69b5967c1f3c859
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20260314-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:6217a85c9a21db00919f8a9ffe5485a8f32a5f2efc08adeb1dd3f3e54af4d46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.1 MB (323098090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9111957652a93ab6eb999d4c9d4a18dda8d45df553fdac8a648224e1b6a5eec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:28:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 01:28:53 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 01:28:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:28:53 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 01:28:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 01:28:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fa3468d221545a43d2151f3977695a31857f9342ba842627d03c9fa1b2ae02`  
		Last Modified: Mon, 16 Mar 2026 22:37:09 GMT  
		Size: 24.0 MB (24038304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cf051f1897bf7109af670b243c7791c62723fc1ebbfa516af2522da6c8c99a9`  
		Last Modified: Mon, 16 Mar 2026 23:25:05 GMT  
		Size: 64.4 MB (64395521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104b57468660314cf151620aa8ad3d45bd0387c0fec8e240c5a92969bf23eb52`  
		Last Modified: Tue, 17 Mar 2026 01:29:20 GMT  
		Size: 92.4 MB (92448451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4384ef542a16608e9b825ddf3c86dc09e4324c50fc9718c0261655531fdcaac`  
		Last Modified: Mon, 16 Mar 2026 18:05:32 GMT  
		Size: 93.7 MB (93727072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb057a40bf04b6dbfa7eeabb9cfbc80ce24c5bfa3e8e8a71033246010070dd5a`  
		Last Modified: Tue, 17 Mar 2026 01:29:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2bbc3a0633a3404e2400e0b29d7918d108a5ea6f164be52ccff336837f8a4f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb44522b30554819252f66dfb816583af0222dbb1fcf1fe9d6084bc7879dfb8a`

```dockerfile
```

-	Layers:
	-	`sha256:6e82f614e7f4041252846f9850ddcf94be93b368bf828c2a216dd212d99dbbec`  
		Last Modified: Tue, 17 Mar 2026 01:29:18 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a3a405977096f7ccc2663edced8c92fd9282aeaeebebba799892f886102c12e`  
		Last Modified: Tue, 17 Mar 2026 01:29:18 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:7584b3a832f9dfc1de4ed22cd3c5bdd5097275d626ccc63146372e8a95550c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281946193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5214ea193bd79b4c79c132aefd4b7e69b25f5c96538272ab334ec1c27ab7456f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:51:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:19:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:22:13 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 02:22:13 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 02:22:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:22:13 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 02:22:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 02:22:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3e574dbe918dfcf76ab4fd7736cc3c62e552f2465f49a512ed26cfc623807024`  
		Last Modified: Mon, 16 Mar 2026 21:56:33 GMT  
		Size: 44.2 MB (44207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92577caba10dd52b0a4a93a140b02839815621e1e55d6eef1c846ec1932e81`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 21.9 MB (21942056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c259f98025fcc3d44333815b426fe9bea34608d38b537248297aff1482d389`  
		Last Modified: Tue, 17 Mar 2026 00:51:25 GMT  
		Size: 59.7 MB (59652088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c86c8157eabef4115dd7665b0d4509155a5658e7942eb9c314f797d1db74aa5`  
		Last Modified: Tue, 17 Mar 2026 02:22:41 GMT  
		Size: 66.3 MB (66305556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c3549b40c9d6609f7ae376dd04fb2e1ccc5bd7d54b10023e8efe518db570d9`  
		Last Modified: Mon, 16 Mar 2026 18:06:19 GMT  
		Size: 89.8 MB (89838768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfe9057994fee05a0a2760c8e501dd7034c8e5136f07b4a28bf083f9eb9dd7c`  
		Last Modified: Tue, 17 Mar 2026 02:22:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0ad3a0a7267f0471e0a8745b5c488e00c63921e178569dd26c30406d59c3b571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe6917cc57a9b1d2ab03496ed04d0ecf81bf77a9a6f1e4c9535bfca89928812`

```dockerfile
```

-	Layers:
	-	`sha256:8c7f01a596c6849bc3da78da83c554620fdf96cd6f729bc9faef4f28f580e79b`  
		Last Modified: Tue, 17 Mar 2026 02:22:39 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af94b23de31218e323db14920e1e5aef6adc277ee1efff1a9e3619ef3ad4ac07`  
		Last Modified: Tue, 17 Mar 2026 02:22:38 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:599767cca5da03af5e3b202b658ef8c37f0e2eccc1f24c4b36cdcc9f89f12792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311891701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75f28d8423cc5a290ad440fe3e8b166c0d034bb389f93ce4aa9cc3dd6fb3b62a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:29:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:31:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 01:31:01 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 01:31:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:31:01 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 01:31:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 01:31:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbce225727d69d170353500d8834770da849cbdcea48de37e492fe14ef880d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:28 GMT  
		Size: 23.6 MB (23604701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda59add442110ab916af1231a98d110e965b9b107829a3f0920d6789fa955d0`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 64.5 MB (64479442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c7dca5d7f86c8ab8573cf71e155d660b517189865ffe143b7a2f4ab89355e2`  
		Last Modified: Tue, 17 Mar 2026 01:31:31 GMT  
		Size: 86.5 MB (86520904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad36eab247615030277063307261e70ef31ab1fb10cb9e2a3d5ec600c3c4c21e`  
		Last Modified: Mon, 16 Mar 2026 18:05:21 GMT  
		Size: 88.9 MB (88913464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d25a756b69653874e9d574314d84e7f0cedd02a74e2f7622230339fe699604`  
		Last Modified: Tue, 17 Mar 2026 01:31:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f11d6a745d8dc28216ac02c6c726f8c7246fdf00a1927267ef6b022941852f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674f35b09de96e98d34e1d0139b64e74326c9a5b6f0d81046d5d23605a5163cb`

```dockerfile
```

-	Layers:
	-	`sha256:09139dc3de9262febc05c25cec86f7a5e09e7130996b6f51219558fef8458681`  
		Last Modified: Tue, 17 Mar 2026 01:31:26 GMT  
		Size: 10.5 MB (10524857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb353c3ec08cacbb565447930461da0dd9d4a7b6c21d0e0da18d2e60eb595393`  
		Last Modified: Tue, 17 Mar 2026 01:31:26 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-bookworm` - linux; 386

```console
$ docker pull golang@sha256:7e983eb902165c5b8e964fc901d983e5839e94223bcd1860c8fa597fcca5e794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322031702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43df84e87315f712d653417bfb26c1ea7a32c280ffe46b1ec816cb3a83598ac6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:41:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:15:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:17:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 17 Mar 2026 01:17:51 GMT
ENV GOPATH=/go
# Tue, 17 Mar 2026 01:17:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 01:17:51 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 01:17:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 01:17:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:400234fd447028a685a307ac0360522f0cd83d85515ddb6a2bf38049ebfe1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:35 GMT  
		Size: 49.5 MB (49477654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7cf39578e27046e7ba7fa5d4d45df198790a004a9eb86583e977b3b055c88`  
		Last Modified: Mon, 16 Mar 2026 22:43:53 GMT  
		Size: 24.9 MB (24871994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d9d2da3801adad27eefa73bb7b5ab6c0c94f46583823a923caa8e9b995a97b`  
		Last Modified: Mon, 16 Mar 2026 23:41:39 GMT  
		Size: 66.2 MB (66234305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8323a18199a174e3c23f9b1c3d35865facfd57365822997d38b1f6a1a6bcfe`  
		Last Modified: Tue, 17 Mar 2026 01:18:20 GMT  
		Size: 89.9 MB (89871084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7beadfccec3ab6ced574e10800119a7f79c633318e3fc8b60061f1b218729af5`  
		Last Modified: Mon, 16 Mar 2026 18:05:47 GMT  
		Size: 91.6 MB (91576509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75065596b101c9e330ad4d7dadde45abf1625e4eb18196213ae4cc2cad0cde52`  
		Last Modified: Tue, 17 Mar 2026 01:18:16 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5abd5d27a21732ebfbbe6cc418ee711673476e879f6f38e889110effc15f9932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19012ae3298de922fee6d8e51871a2612bf12539d5913938d83e14adeba61223`

```dockerfile
```

-	Layers:
	-	`sha256:0f779ecf0ca6ec97613da210f9d28427e6fb112c7b06e3875794fadad71cc447`  
		Last Modified: Tue, 17 Mar 2026 01:18:17 GMT  
		Size: 10.5 MB (10476613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80cdd62af63c407e531edb2dd37d5844ac043afec704354de5d87ac604588ad6`  
		Last Modified: Tue, 17 Mar 2026 01:18:16 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:a9e31e14eba1fee28b9aff855e646a979d6fd39915537f161e3df34357bf547b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293326203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7bba2011e9036b378b7d9aa963f0a2757d5edbb2ee39d1a14e4033f69ac6f3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 06:07:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 11:29:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 12:18:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:24:48 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:24:48 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:24:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:24:48 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 18:25:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 18:25:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6ec71ee94fb878725e70f6a21c20349985b89066361ee1f753b3854cfa2c839a`  
		Last Modified: Tue, 24 Feb 2026 18:41:37 GMT  
		Size: 48.8 MB (48782510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea2283ea3597dab73b85bc0ebe9635f3297b9d6d4b8ff5df7913003859ba369`  
		Last Modified: Wed, 25 Feb 2026 06:07:50 GMT  
		Size: 23.6 MB (23615315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372ec86799dac23af2f0ffbced98ecf9eceeaa5ddf68be3af3cc474182e97448`  
		Last Modified: Wed, 25 Feb 2026 11:30:27 GMT  
		Size: 63.3 MB (63310148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8358d10d80c9af8f69fd6083cd0982ee261a68e3865c0f029247660744e146`  
		Last Modified: Wed, 25 Feb 2026 12:20:12 GMT  
		Size: 70.1 MB (70053345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff347f6a145f7f93bbfb2eb74f5a1a353cbf6b3881958a27e04c5d6b711e338b`  
		Last Modified: Mon, 16 Mar 2026 18:27:00 GMT  
		Size: 87.6 MB (87564728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b407766a3ae114da28fcc9b1a90384b81c510e9bc6657645365cc48235c14ac6`  
		Last Modified: Mon, 16 Mar 2026 18:26:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:60d950f7a2c9efe6cf0e67744713ccbe84c51b8bf25c1b270ddd4b45f53d34a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d079cfe4f93f19f30ad72a7286e0d017bb8f23a4822a4c66f32a0f6b1dfe9d4`

```dockerfile
```

-	Layers:
	-	`sha256:7eb96918b2aed91f9e0af860166212bede559e527e41add350c0fbe5f78427d8`  
		Last Modified: Mon, 16 Mar 2026 18:26:50 GMT  
		Size: 28.2 KB (28239 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:d5e6ee23803b4950dfcf0cacae11d37c2079a5ce1a2e8fdfa488e253a6341d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328763199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1842a49ee61dc801cd2b006a727471c46296502b35a9a484068d8bba6aa8f7b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 01:48:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 06:03:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 08:42:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:05:42 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:05:42 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:05:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:05:42 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 13:14:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 13:14:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d6053003aae760c21f129e32066714b891ab6bc6ec6abdf0f13ff20cb85ede`  
		Last Modified: Tue, 17 Mar 2026 01:49:00 GMT  
		Size: 25.7 MB (25671576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc763fa93abbd05d9932abad5e62ea754d4d526450c9517c9e5b75b5c914969`  
		Last Modified: Tue, 17 Mar 2026 06:04:00 GMT  
		Size: 69.8 MB (69846151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6def63f9899aff9dec9e9602eb9cdc01aa08dd0545734ab481d2e9c86c5213`  
		Last Modified: Tue, 17 Mar 2026 08:43:26 GMT  
		Size: 90.5 MB (90462652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5ba3f21f31dd88c9cf395edb0e30aca822e3dcde51bd5a6421a6f428d5671b`  
		Last Modified: Mon, 16 Mar 2026 18:06:39 GMT  
		Size: 90.4 MB (90445965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302fe4b275340fb17a04a20f006515b4cf6246613ad323039980056b65ccede4`  
		Last Modified: Tue, 17 Mar 2026 13:15:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c14a4685eb701f2acdb8fbad3ca180314ebf525e401e2ff050cc2d4470c5645f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c6ff24603d29488a7a7dab67b2c0fc776d9c10255c34aef017a7b3ad154e68`

```dockerfile
```

-	Layers:
	-	`sha256:af6ff9869b374fd042da89e32c99820552eacab39a37e45061ca11d72959f3f3`  
		Last Modified: Tue, 17 Mar 2026 13:15:10 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:171880209b462f13b4d132a5892e47191dda85dfc6597c183a73929799701b7e`  
		Last Modified: Tue, 17 Mar 2026 13:15:09 GMT  
		Size: 28.4 KB (28431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260314-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:67bb948c888ab8334d0772a24beb13c12ae0a1d06042990a79c7a53ff153bc11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296663781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351b25ab08806d9f3a4476f3bc9d3e127697f9ef255a790d2daaed3404beab8a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:33:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 18:06:48 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:06:48 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:06:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:06:48 GMT
COPY /target/ / # buildkit
# Tue, 17 Mar 2026 06:48:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 17 Mar 2026 06:48:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7dbc3949555449666cc7651209b926019d3fc7f1511f7ebcd8979762b12d59c1`  
		Last Modified: Mon, 16 Mar 2026 21:51:27 GMT  
		Size: 47.1 MB (47147919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d904b886f0656b8d9f7b2cc64089c6c03aa31b22b97fbf96b0bc6c4e3726e429`  
		Last Modified: Mon, 16 Mar 2026 23:44:29 GMT  
		Size: 24.0 MB (24033614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3244a56b42252330a5ec4502181ecac45b16d96de3113430b375f7d10e72bde6`  
		Last Modified: Tue, 17 Mar 2026 01:33:52 GMT  
		Size: 63.5 MB (63501466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4675b438812902e2c655c94c9327bf3b518e8e27bad47eafbd6877a4c6ebd74`  
		Last Modified: Tue, 17 Mar 2026 02:25:42 GMT  
		Size: 69.1 MB (69055273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e78b174fccd5298debc49ecb6092c7b356413921318c225406833e6427b55a`  
		Last Modified: Mon, 16 Mar 2026 18:06:51 GMT  
		Size: 92.9 MB (92925352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51f3a63bd6df260d4fc9d3e10804215a58a715df4eeadaa544239d8ec6bbc8d`  
		Last Modified: Tue, 17 Mar 2026 06:49:04 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260314-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e3201f02ad9e730f65ad75e2839d4f142ccb7eccf9d232420b169d6d84cc1ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a1b6c3035ce02b2e32cb88d62406a7011103070e8b656910f5db04db9a85fe`

```dockerfile
```

-	Layers:
	-	`sha256:e0b429c5bb63505f5f9d491f00c10d1e9586fbdfd3d83b2f954cd28b6503e4d5`  
		Last Modified: Tue, 17 Mar 2026 06:49:05 GMT  
		Size: 10.3 MB (10328791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbae056cda51d0bb6855f47a5d27d8354cb894ebe0bd98dde1e7769b3e78f7c3`  
		Last Modified: Tue, 17 Mar 2026 06:49:04 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
