## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:a9a5ea1b2da7e72046d7dc64625f809b40536ac69770e72cc00a82b47c9389dd
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:548ec7414e5c15347f4763b327831a59c88d83429aa8194c69792009b61ad379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75621319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835dde0a2eb9cddcd0bfaf08eee4f6a41ef8271412df4e84e0dcd190d9321b16`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:46:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a619bb3c1f14c591cc163d929ea3f43df5d6acebdd877fecaacf054d56531b3e`  
		Last Modified: Tue, 07 Apr 2026 00:11:23 GMT  
		Size: 48.6 MB (48587084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bf18cd16b2dae064e3a3c52f418c924e5dbc6ee6c8435f830ab8926bcc861a`  
		Last Modified: Tue, 07 Apr 2026 01:47:08 GMT  
		Size: 27.0 MB (27034235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:31122a4deb27360a3dc8879891d47d4ab55915e06310a2cbcd328822b2f3588b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4075994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29363bbbe7a1183d3e11d3ebd5fc7d215aabea42798ccc3a541f512d6be00caf`

```dockerfile
```

-	Layers:
	-	`sha256:ee87dbe81d5f469e0ff45a2b4f0654d4b4e50cfff204669e93842ca23bfe0b0b`  
		Last Modified: Tue, 07 Apr 2026 01:47:07 GMT  
		Size: 4.1 MB (4069222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6115a3fbb2c80c7f88ac57350a7b2db045c446aa24681ba1bd5bf826cc68ff12`  
		Last Modified: Tue, 07 Apr 2026 01:47:07 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:579126e38a7a81e191240ece146285c819673dff300a66c2b8b45eedaa5e535c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70268018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:060c5c9d3d51eeb24691297445ea44755716a7ff0d10996ce9a7b35d6cc1f9db`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 02:01:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:94c1a7288fb6578b9efe4cfec6d86c90bcbd7f6b3ded72757e8150ba2d22a63b`  
		Last Modified: Tue, 07 Apr 2026 00:59:45 GMT  
		Size: 45.5 MB (45540788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431662b04e5e4d9f2ef3d5f7c7e2caee0a1ec1674e5c8149f9c8cd948a2576c6`  
		Last Modified: Tue, 07 Apr 2026 02:01:50 GMT  
		Size: 24.7 MB (24727230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b399d07c1ef864b68c70a7a2a56da1ac6606d8b3af46a438479e9931413d71f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4077549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7baf226ae0206d8da7597204dabe258edf4f97194129131c4e2d3dc46fdba4c`

```dockerfile
```

-	Layers:
	-	`sha256:39cd5e72916b56a0763560c65a04f9abeac5de114cbea96c8747119edf3699ca`  
		Last Modified: Tue, 07 Apr 2026 02:01:50 GMT  
		Size: 4.1 MB (4070712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37e4c139e56afe80e7cffb4bacbb2b229e4037d6b3e2e451515dd67106c7775c`  
		Last Modified: Tue, 07 Apr 2026 02:01:50 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:86651f98bef175ed69ca4bb6ecf2ff9d77e12e4a1d484f0bcdf9145974f11182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74974106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e424f5e9d73fa7257e5417c71d025ec25c99c342cf01c78edc94d412e6f225`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:50:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8be2228c7df976aa0c1c2333d6e8d72b206ff7533d4625ffeae3663f7240d98e`  
		Last Modified: Tue, 07 Apr 2026 00:11:06 GMT  
		Size: 48.6 MB (48643356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf67292a85a4af897784b09f019ed45150697232130ae9fa282c0d04d42db8bf`  
		Last Modified: Tue, 07 Apr 2026 01:50:18 GMT  
		Size: 26.3 MB (26330750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3389992440c35a6411a5a0e7345b4d13bbc772a38f0116fc5848964e1150b709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4082715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fdaea45862e3225767234d1e1a6878c1809094c541d6e976c195c4718ebbf70`

```dockerfile
```

-	Layers:
	-	`sha256:5bd147f2b693375155e06b6210c904cbf402e80c3342eaf0bbf9c68b7c69a01d`  
		Last Modified: Tue, 07 Apr 2026 01:50:17 GMT  
		Size: 4.1 MB (4075862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96748c974f0efb4be8eb3b4f746beb5bfba01eb2186e450ae80c63f7742db3e0`  
		Last Modified: Tue, 07 Apr 2026 01:50:17 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f51de756ea8307fc039592b64364f9fb0f746e9c03e6c7da8c46ec264f0c6d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78177300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294cfad8d9fcb059e546a7c0dfa42e7394d01e2169c09151ea00749b16ac3925`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:46:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c655e94b1afc0d0a4a69ff26686a8cb9fd0349459a4008b02fd7dcb3e6d3ab8`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 49.9 MB (49878389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74970d6f811b29c802a9f3c8d694bfd2f422255c20b66bcc271ba0c7bcc9dbfc`  
		Last Modified: Tue, 07 Apr 2026 01:46:17 GMT  
		Size: 28.3 MB (28298911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4a59989cdfad3be8ebc844aec5cd89d1027fd7d5316f6847b250f2d88c7ca5e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4073083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad414e49a630ecf1d8cb569182c6c49a651469b7e8196c0429a5308bdc0f5e6`

```dockerfile
```

-	Layers:
	-	`sha256:c953a104f3c70ea8d78cfeae8cd9ca7fa0d70b97e3b99766b86ba08336c3e1d9`  
		Last Modified: Tue, 07 Apr 2026 01:46:17 GMT  
		Size: 4.1 MB (4066333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ccbafea9b64cd15e8bf0ad97f7e7e9e62540f1e3504f167b2e84c258b7b670`  
		Last Modified: Tue, 07 Apr 2026 01:46:16 GMT  
		Size: 6.8 KB (6750 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a3e0d5a8487d4fed364ccdbbaf4f6c4eae82aa3d4eca63349c09285ae541bfba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83169879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47614eb7e8a505a4452711b26abbfe119221b5592d112e3b63b53a585e8eec55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 04:21:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:82a75a893b6c64944c6f9a45687c1a1f96d90f40ac32f7359ffe0b6755458be4`  
		Last Modified: Tue, 07 Apr 2026 00:10:12 GMT  
		Size: 53.9 MB (53851237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b159d77ae23ff0a537f251333a902815f558c4d2eb7e7cb1124f2b5ba37262e`  
		Last Modified: Tue, 07 Apr 2026 04:22:08 GMT  
		Size: 29.3 MB (29318642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bda6ca762081affe9b354e6e88d9c4dab0ac76ff95ec4624021577626b80cd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4079874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ca888256909a5170231f5af3961307d16ac4f29c55964d18c64976fb5cd7ec`

```dockerfile
```

-	Layers:
	-	`sha256:78916060eac2c475ee96b220ed8cf2691914e4a34e7830726e19f7eb40258a69`  
		Last Modified: Tue, 07 Apr 2026 04:22:07 GMT  
		Size: 4.1 MB (4073069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85c404b897d413a82c1ba9c1bba6793bf3e020b836d49a6ce42fd64364462479`  
		Last Modified: Tue, 07 Apr 2026 04:22:07 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:975d9381587ce6aea81d26de04bbb50a01d26e1adbe437e89e6cf01e358cd0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73320869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05038bf99ae775d947eb35f3d5a4f21e3ae5ec9bd4dad1214c5770f3e7b2d6a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:27:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c3fb5c15cbddc0ebbd7afd8ce992f6bfd6f0d5d4b1d5f4e672c5fc7451f1119d`  
		Last Modified: Mon, 16 Mar 2026 21:55:37 GMT  
		Size: 46.7 MB (46721467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059cd42e31b5d0cd1848f67940ca871c5e491654382eb483e7231a6e0aedfb85`  
		Last Modified: Mon, 16 Mar 2026 22:28:45 GMT  
		Size: 26.6 MB (26599402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd807e7bda091ea2ef64187193526d724e60676788a71179d0028b33ea0e37f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4073738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd81c6cac2e374f106f47bf5d5e3a97ad18fea81b38fefab76caabf6d8260cc5`

```dockerfile
```

-	Layers:
	-	`sha256:ffecca908a353bdaa03405b042d507080b131b4b4376a7b34a0c26c5b5cfbc98`  
		Last Modified: Mon, 16 Mar 2026 22:28:42 GMT  
		Size: 4.1 MB (4066934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b8dfbf0d9c3de45f54648517ff279f8e0f690fa91dfa562fe7a99b7beb3f5ac`  
		Last Modified: Mon, 16 Mar 2026 22:28:41 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1ee0d955670aee4d5a1f5ca75de1447ecae1418e673768b336674ee6a3a177e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75107796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c2f0dfc122afdbd894f5eb142aa4e4718f6c90f104aab1530fae875d4fada4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 03:04:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d387cf27b8c74bb29905817ad867265b401af02fdbc21b522a98041e86095a47`  
		Last Modified: Tue, 07 Apr 2026 00:11:00 GMT  
		Size: 48.3 MB (48291595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71640c6f0517962fef2d2cecd2252a1ad50dd36dcdfc5949b497510671693745`  
		Last Modified: Tue, 07 Apr 2026 03:05:15 GMT  
		Size: 26.8 MB (26816201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9c7d0b605b9e92b0ed2f6d328ee6f1a2091fd18fc5f57e0cde18480e405e4de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4077406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1a3c31af55042936ee74d157f8624a8f11d1aef9680d948d516570f1b622f5`

```dockerfile
```

-	Layers:
	-	`sha256:a24741388c6b773160eb472f58f82ba50e30fb2d7e842a5adaadbbe40dfda900`  
		Last Modified: Tue, 07 Apr 2026 03:05:15 GMT  
		Size: 4.1 MB (4070633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dba7d35d34ec4873a00317768fda2f6ac6ecc557b98bdf7bc5ac7fac47bb019`  
		Last Modified: Tue, 07 Apr 2026 03:05:15 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
