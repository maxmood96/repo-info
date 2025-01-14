## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:8b184156c095393a9346e435517cfdeed3f6b65670a9543e412c40f00ed39327
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:185277620d21cca71d9049fbfe57e4d0a0861665835c1f5643922eff3f78fb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74248263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b448276c6947d117e941929ea20529eb1405f37e78de5e7e955fc1b98a8cc3ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9146d6057920f25892ed3e631287d1e0e740bd11f7e3dd39c76c478675de8456`  
		Last Modified: Tue, 14 Jan 2025 01:33:33 GMT  
		Size: 48.3 MB (48276092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b2bf2fe5435a7871b88dbb724a93352983bdb5ad01681e2165e7056a7fbf25`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 26.0 MB (25972171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b23bcf663941e84dedeba50130583de1c1f9a9c29634c799f9221906ac8dd757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f867974e1bc4c7627ae4b5bbee069a0714bce3710ee0f30e8aca039ccecaf34`

```dockerfile
```

-	Layers:
	-	`sha256:ff944ab972c616ca3404889427eff6543a1486ca8a039534e1431c234bbb96b1`  
		Last Modified: Tue, 14 Jan 2025 02:33:07 GMT  
		Size: 4.0 MB (4029111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b011f3b2887db0f8e934462d977b6bf8f939f29b3f2c584bd49cf67e854f024`  
		Last Modified: Tue, 14 Jan 2025 02:33:07 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cf90a40ffbeadbcaa0a1ac3347286485bfa625f9d61e65817e01f9fa07ebf6d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69038417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b7ba50c7de61a169cd950ac362c122e745ddcf4ceb56bde78f359525e07f7f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b5a5271e09aab30795789f051d2425121101b650637f36e772bdb80c62bb4833`  
		Last Modified: Tue, 24 Dec 2024 21:35:34 GMT  
		Size: 48.7 MB (48738917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd230c08c2a8f220f4a7754708d43b365ecaa32d038ae6429f10953c7ef0284c`  
		Last Modified: Wed, 25 Dec 2024 01:32:00 GMT  
		Size: 20.3 MB (20299500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5249a9b6c3225b7cdd92a20607cfe1c3c47147a8c556224dcf8f18266746d1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4040866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ef255eb764189742600222ae5d4ce706c14c6112bb0d3826e2ed72f005ed3a`

```dockerfile
```

-	Layers:
	-	`sha256:34870fbae21e0b6883d924cc25487991f18011694db6d982b0a7c0cc5abfa967`  
		Last Modified: Wed, 25 Dec 2024 01:31:59 GMT  
		Size: 4.0 MB (4033985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65217ace5608b04cfdb7be0856011ef54d34ca4d2e7593975e3f984a30f50b12`  
		Last Modified: Wed, 25 Dec 2024 01:31:58 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1fcca48ae7c05a96daeda760fea171cbc55db912ba39bc5421576503f2e2a09d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66365736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bb11b75b7df6218c688a74c3398e9e0b70fee80ca1be8b3ba1519c34169db3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7dbbd0b59e8fd2a826bed9f5cfe195c9cb61ad138accd85ab45d8f8eb5e53a51`  
		Last Modified: Tue, 24 Dec 2024 21:37:24 GMT  
		Size: 46.8 MB (46767965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1a49163ae7afb92f788f8101a5f0b57af46d0766372255bb4e15ef002eddc2`  
		Last Modified: Wed, 25 Dec 2024 03:45:38 GMT  
		Size: 19.6 MB (19597771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:96e94323b016304465d31ac9caa755db2cbf4891842fd60f23a0f42e5d429f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2b10d85e4e55a16379718079639911f576e62e79d855e0750915071459779e`

```dockerfile
```

-	Layers:
	-	`sha256:44b298c50a8949ed08e71aa924bde810da5402f2fe8e8a43ad73fad83cdf1e27`  
		Last Modified: Wed, 25 Dec 2024 03:45:38 GMT  
		Size: 4.0 MB (4032790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb310becc5110dafc3e2ac7faadf7e6a7d7a47af43762c7f4b9613f7c60ecda`  
		Last Modified: Wed, 25 Dec 2024 03:45:37 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ef07a9d30111ac3611c08cd20dd490ecddf084f557d291f50b057bf903127d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73459077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18cee9ed3442d786921b9ad79870a90ead3007c3cdc39981e78dfcc029cce11`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:655b7ff6f79a823125a6f22dacb056ef3cd9ab7e8eb5ffc6594ff4745e276b8b`  
		Last Modified: Tue, 24 Dec 2024 21:37:11 GMT  
		Size: 52.4 MB (52425570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0f4612c729fd6c76a1191b59daef982c8369d9881af926e8193cfc3d012f9`  
		Last Modified: Wed, 25 Dec 2024 01:50:48 GMT  
		Size: 21.0 MB (21033507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a579cbea935a69fb687f89f5e3acb0b5edc1e725a5003432a86ceba58d05589c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4042278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f23b47966724feccaad8ae071f7da9df541f19a849ab9917c6b0b457922df41`

```dockerfile
```

-	Layers:
	-	`sha256:51007d37d7b0b1264abf36f1bfc563b67ca6688b32c0682f9e6a07c056717f33`  
		Last Modified: Wed, 25 Dec 2024 01:50:48 GMT  
		Size: 4.0 MB (4035380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe3f286bbed366523c1913afbb751a107c0776f07bcfb200401bfd1bd870605`  
		Last Modified: Wed, 25 Dec 2024 01:50:47 GMT  
		Size: 6.9 KB (6898 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:829e0f497253cee04547b28332edc9d885bfda4c11a53c910d33a8b29aa32126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76789778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57f21450060e26690bec7359488005c87bea5b3c4aa8697e752584fc87c0616`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0b7bebb3fb62b18c851bbf703cf6a1caa57f7ffda09b0b23b4e4cf1051c666c9`  
		Last Modified: Tue, 14 Jan 2025 01:33:38 GMT  
		Size: 49.7 MB (49675708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628707934f13167c16796e4cf79505bf1ee994868dc399d6e208f3c459420999`  
		Last Modified: Tue, 14 Jan 2025 02:17:30 GMT  
		Size: 27.1 MB (27114070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d49eba8ba68664136b4744e925652ce87b63c61bc0b1ecca1481c7b95c5a9b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5172433a86bc8705b59a3f63bfa5f1ab9fa909a7585f8bed96c1dbc703d54a48`

```dockerfile
```

-	Layers:
	-	`sha256:7a990eb1d51e78b6bf87a1c0fd93531f580b703ee8d5b66d8b57eb3221e2c714`  
		Last Modified: Tue, 14 Jan 2025 02:17:30 GMT  
		Size: 4.0 MB (4024870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9916a90caa8ff4f61d2a1f1ce52ccfd88cd8941ddf570cd7e603ef21a5b912ae`  
		Last Modified: Tue, 14 Jan 2025 02:17:30 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2ac5c14f2cb752c150b9d9aebaf78bb331d32a3e38f814d05bb6be547d684f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73444593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258d4de2a286b7e91edab5cae2d1892a062992ac6a352977614ccbd3447220d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3c43db2a2d96e4b42b073ee755704e1052dfc08d2fed2bad739906e6663926d9`  
		Last Modified: Tue, 24 Dec 2024 21:35:59 GMT  
		Size: 51.7 MB (51716844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb196cc5b6a238393d49fa4e93d6bc6fb9d8eb10a08514c2266839519f9d3f69`  
		Last Modified: Wed, 25 Dec 2024 11:49:41 GMT  
		Size: 21.7 MB (21727749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0c0245c9efd926a10b24354f10e357f1d4f5614e347d55146a35cc8c58d0ca85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717fb87c467fca95dac52ff53bf5c7b829036f30723182309075918eb452b192`

```dockerfile
```

-	Layers:
	-	`sha256:a2abdccc39257298682e89f41abebb61dfea8a2b9231fb5168a0655b2018602b`  
		Last Modified: Wed, 25 Dec 2024 11:49:38 GMT  
		Size: 6.7 KB (6654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1d56170abe3d22caffe0cc6392034c5ae14062c9eab9a75958b85a2c058ccbe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78828512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185d74cb2e8f2d9c34358e4a4f131a2539b8049a64487836c4c733ca2dc0aab5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7d0c0062851cd41c4b765bee1eaa246592e96d9c4a0268bfea5c5d2a73be0e62`  
		Last Modified: Wed, 25 Dec 2024 00:36:18 GMT  
		Size: 56.0 MB (56044104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e488722a9275f087219fc61d856ea4c4ed4b328a7554350726557ef4cf4353e`  
		Last Modified: Wed, 25 Dec 2024 06:15:57 GMT  
		Size: 22.8 MB (22784408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8167f88b5b2f0edc2126acfb9fede58e66515e1eb9457f4b80ab6fc2c1a448e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4041887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2454d243f643a1b6a324a456011b55e192cdf6eeb92e7f20159f19e35ce0d857`

```dockerfile
```

-	Layers:
	-	`sha256:0ffbfd05d8ce927c2cb1a37b7a54dfbc2219a40ed922695f45e76c2395eb0130`  
		Last Modified: Wed, 25 Dec 2024 06:15:57 GMT  
		Size: 4.0 MB (4035035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f318973cbadc4c4e9ed3cec306383915974799fb721ec605663411af882352dd`  
		Last Modified: Wed, 25 Dec 2024 06:15:56 GMT  
		Size: 6.9 KB (6852 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fcd7c18f6e3e05d45801df17936e7b836aea620f527a13bbc906700d7559dddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71510089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392ee0a15b9f87f1e7fe24ec10c3f60bfd0eff664cc2c34d829c02c7123595d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4a3888858b6d8f90bca9f8a3e822fec0d117f600035c0bd5f303435214a719f0`  
		Last Modified: Tue, 24 Dec 2024 21:42:18 GMT  
		Size: 50.7 MB (50704572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ab35313b79d2c2c495a88d3b26927a4185ab2c8c24561540dc9e6a1e77ba9e`  
		Last Modified: Tue, 24 Dec 2024 22:29:42 GMT  
		Size: 20.8 MB (20805517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fbb90592bdd3214c8e2f0b09e8ab9095321a05fe9334a2e6ecac61d8cb357fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fdb134b1e78e4c8ba4756444b19886785195d6dbac031f1db79946318bb780`

```dockerfile
```

-	Layers:
	-	`sha256:30acd2fbe1bc37bbf990df720028dd37938ceaab937108f9afff0ca238462f74`  
		Last Modified: Tue, 24 Dec 2024 22:29:40 GMT  
		Size: 4.0 MB (4024608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c389947547ae257dc1bbd00ecc6843f98740de854978cf081b04f5574af5b4ae`  
		Last Modified: Tue, 24 Dec 2024 22:29:39 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d450a6ca2180bcca9a10d0c73c31b9e209c287ce2b69bc025e52e16cd8bbe408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74771310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e27c9fc1620a11aa3e9c1ecae6612272e1b18b84134b7da16cd2d635993c4ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e1fe280a5056c1901421b5598ff050c78aa067b752ad527583fba85c589bb647`  
		Last Modified: Tue, 24 Dec 2024 21:37:42 GMT  
		Size: 52.2 MB (52167537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb20153a9b4c7c97b49477bb7e12772fe5782559f417bb6517d244a48d7108`  
		Last Modified: Wed, 25 Dec 2024 00:18:28 GMT  
		Size: 22.6 MB (22603773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2dc67f66fe046c155fb71c93d30202fd59a19df0e192df446318f65739abc1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6c35b8359aebdf789aba0f01178bf17e6223f24048df6b5f2734d31d6249ef`

```dockerfile
```

-	Layers:
	-	`sha256:7e814020747a7761e7643be79e26631bda0a3b058850c08076c37cd5b49f68f6`  
		Last Modified: Wed, 25 Dec 2024 00:18:27 GMT  
		Size: 4.0 MB (4032691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37e662e524479a0b85ce1f92804eac9a3174bc13e2a19f8008170fe8989d229b`  
		Last Modified: Wed, 25 Dec 2024 00:18:27 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
