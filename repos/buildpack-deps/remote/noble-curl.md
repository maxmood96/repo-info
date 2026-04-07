## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:27f39d4816cf769939d0badbe2865e85fb7adf06bf2a7315e67467766950f22c
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

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c883521f92ba470c022bafb817a7ba7898836908e3fc881068b2374c008afb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43364803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0845a34d2222ceae84dd73325c3fc623564a7339c4ce55c5c8277f7066da0d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:47:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87036178ad86a6ffffd0bfbc6472da5aebf31ed69c5b3f17251ddb308c41f20`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 13.6 MB (13631344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d17588779cef19a5c6005587256b08daa5cca7acdc7622ecc010a57f84213237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2614753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d8f796b4c0fe4494a61c012bde6daf8a75c7699d393dbbd56b26980c48c458`

```dockerfile
```

-	Layers:
	-	`sha256:de00d1cdd5eb28df072227f4b00fcda38da5ab895557e21fd49f0addc05968c4`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 2.6 MB (2607837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ac304399adf31ff89909c57424a64f0ae20a159e2f057b299af0683627a50dd`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 6.9 KB (6916 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f5fec7226a763ce0cd042206866de3da6552195289921f8efb0625fcd7575bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39647002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ffacf8f22cf9c42a1eae54fff9c971fdda834ad8a163ab134d685ff9d98e99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:14:30 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:14:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:14:31 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:14:34 GMT
ADD file:68e3febb1e8418fa8ce83073bfbf6ec7236d81e7c8781177d7295e5adce34436 in / 
# Fri, 03 Apr 2026 15:14:34 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:02:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d7d21bc3f0364f0d98c41b0bcda87b8f2bfbf1688f75f6322ed679752a149163`  
		Last Modified: Fri, 03 Apr 2026 15:56:43 GMT  
		Size: 26.9 MB (26858365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0da5755f16317e3ae70ab41f8cfd9bfaf9ebcfc807f501bfdf9301feb5834d`  
		Last Modified: Tue, 07 Apr 2026 02:02:19 GMT  
		Size: 12.8 MB (12788637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:660181b65fba59cbe6ea8edcd37adc9470bf9d34258f55e0de1a0f759032b94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32084773537744cbc0daab7afb0de1a3c6ba2856d45f3c861a6eff8daf9252a`

```dockerfile
```

-	Layers:
	-	`sha256:b26a893a03a5b749826f96c105e0c4d36ebeeeac758c945722014eba79962784`  
		Last Modified: Tue, 07 Apr 2026 02:02:18 GMT  
		Size: 2.6 MB (2610141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab7f36872ae57d11b1ff8678d7444e4545c5d36e0576f71d8c170f403a3f333`  
		Last Modified: Tue, 07 Apr 2026 02:02:18 GMT  
		Size: 7.0 KB (6980 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5bcaaf7a7cb4f9a425af48e93f38d1aa2e8919084678fc3337acb865d9ab624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42340093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4072bceea896b0565c7f1576ad7e8cae14d862e9a14134d7323b438a4b759196`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:50:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250898647707f5617f944580836cdb26a429f5b2583cfefd84515874dcc57a45`  
		Last Modified: Tue, 07 Apr 2026 01:50:30 GMT  
		Size: 13.5 MB (13466018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db6f1a25224831cc7788479c2d572a349b9b6c38c6f00478393a0016b8b5eb77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299fa23aabf054ace5b615a3336240101d242e7ce4d732006411f5eeca7c8f89`

```dockerfile
```

-	Layers:
	-	`sha256:a4117e8d9522ff490ee0c5e6617774fcc14fe778f9e20666f22b1d7413145ea0`  
		Last Modified: Tue, 07 Apr 2026 01:50:29 GMT  
		Size: 2.6 MB (2608895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ba6d1dc531d67795b2f99e7b06285561c4f91dec6931d3dfac5c5839ed2d8a`  
		Last Modified: Tue, 07 Apr 2026 01:50:29 GMT  
		Size: 7.0 KB (6996 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:eea04d3cdfc161ed6180aa0352a9770152d0b98ce9ea760e5aa80ffa9eb8760a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50273719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cf8d20b41190eefc1228a3b678ab19fdb4777ad328fb913067af66f704d58a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 04:24:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f8c8315ff69e0ade5c27a5f32668c5ece93dfdbd029e67d7b478a2a133a289`  
		Last Modified: Tue, 07 Apr 2026 04:25:12 GMT  
		Size: 16.0 MB (15960385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c680597197a9cbf30c0ce16e41d6918b64d9a115d34fd123db9bb61a76018a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e59c1164187f831b3d13e1ae48ff4c33f72f515099fa6ef284bfb5a9e95d40a`

```dockerfile
```

-	Layers:
	-	`sha256:24cb74dd80aedc12a2786f4a446b805da1269e33a4e4a849f4d4eae32185aafa`  
		Last Modified: Tue, 07 Apr 2026 04:25:12 GMT  
		Size: 2.6 MB (2612456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b191837a394d41f7a91dd667a9049fea271d48e5bbf2b3efdc1e1a3cc23a1728`  
		Last Modified: Tue, 07 Apr 2026 04:25:11 GMT  
		Size: 6.9 KB (6948 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ae930e2b521063e6400b58ca00d46287bfc6d1a35d1b9b2e3289a36a27b43efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45297023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7878d004c9ac704233c7343cb1a202b742e89464ced8dcf24bc5c4799e95319`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:42:34 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:43:25 GMT
ADD file:1243b7db425cac690d91f87ad37c1beec0d95da6b3942dc8084039fe1cc2baf4 in / 
# Mon, 23 Feb 2026 17:43:30 GMT
CMD ["/bin/bash"]
# Sat, 21 Mar 2026 03:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:866473980fd7aa6ac5a8a995315a35248ab945008a1938bd15f65082df53b2d3`  
		Last Modified: Mon, 23 Feb 2026 17:51:46 GMT  
		Size: 31.0 MB (30960145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee039942c223db7740f8c7ddba0be9d66f5b268eae6ff09af10e8dfe9568a44b`  
		Last Modified: Sat, 21 Mar 2026 03:07:14 GMT  
		Size: 14.3 MB (14336878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f42d1e3229aee1ae47cfa2acd05315c257a6f709a1ed85b2076f52c437a85bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050c66dfdb1697967ead56a11b17d18fd1d903acd50a1d5f26d283936684d2e8`

```dockerfile
```

-	Layers:
	-	`sha256:d5d9ee3c17495a5b17b26a797f3b10df39374f444602896d3bec8913bd1c923f`  
		Last Modified: Sat, 21 Mar 2026 03:07:12 GMT  
		Size: 2.6 MB (2601736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fddca8c363b3474ad0dffb5ea7b5c0dfb3e9a5572a71512ee21ee9150a90c2`  
		Last Modified: Sat, 21 Mar 2026 03:07:11 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8468c446a5f86fdf8145e93f49b4bf82fad48e5f330d0e30900bde8237c9915b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44855049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd3bbc12414ffc87392baba7143facb8098b6273eab06625a02296fed15862a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:12:46 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:12:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:12:46 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:12:48 GMT
ADD file:31d45a66208318e1066130bac8975f44dea6e7e93cbfb2d29b0888e686bb10d5 in / 
# Fri, 03 Apr 2026 15:12:48 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 03:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbc7b0e0dfda4f493fc8f104984fbea17a2f5d7d1345c3463d92d4acdb49dc8`  
		Last Modified: Tue, 07 Apr 2026 03:06:17 GMT  
		Size: 14.9 MB (14943206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:61c52dc2232280fad55b73a7d2c8f625d3913c08df93d12e5e99169b24d64f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519f964c861c0ffd6b6c432d0b9fada5cb6f537a660862729ae5bd17a9eecc4e`

```dockerfile
```

-	Layers:
	-	`sha256:c88bd58a971f2a091ae4ac134c95c1ece7ce67f4659b1d6c2c45c62beaab6365`  
		Last Modified: Tue, 07 Apr 2026 03:06:16 GMT  
		Size: 2.6 MB (2610662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583dbbc4674a57cfacab30fa60e6c02113ebe997e1bc86bda6c99958fe41b8fa`  
		Last Modified: Tue, 07 Apr 2026 03:06:16 GMT  
		Size: 6.9 KB (6916 bytes)  
		MIME: application/vnd.in-toto+json
