## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:9012ca01ed2cbd3b16b4215415eb859eec9d0e7358a74328c58c7bd20143057d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:670a28b8329310e9fd829dab5223994c40e13f804b443f730f6c37f47d789c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142468232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88fd5d5b7024179fd9f747d7c12f444305ae9f8790bb51ddd920ff09609fe54`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073c3e094f775042a2296ed99ca159904c7ae19127cddd6dc0e02dfeff3ac66b`  
		Last Modified: Wed, 21 May 2025 23:20:52 GMT  
		Size: 25.6 MB (25583751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796d3fae0f8d1c689d461da616de1a85e5ade1f7c61c5496c0c3b6b1bf6e722d`  
		Last Modified: Wed, 21 May 2025 23:38:03 GMT  
		Size: 67.6 MB (67637573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ce214589e4104395181191462ac402a858d4e55b14b9d817bdb804f776b37110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7594204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1db18e1c4a4d5f9ae2f8a3c97aaacd9934b6d1b7d1b4bccd928d032e8cf9eeb`

```dockerfile
```

-	Layers:
	-	`sha256:f3216e58376bb04d7525e8e72d81fb486c2feae50c32228bb430a2d336bbef84`  
		Last Modified: Wed, 21 May 2025 23:38:02 GMT  
		Size: 7.6 MB (7586890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f25ff982fd40201daa5df5eab85594ffb798c910d383e5bbee522a229b5d0394`  
		Last Modified: Wed, 21 May 2025 23:38:01 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1412dfc03840fd323b8d2d8f19b7d8355805b5f7c7d532f11e144db422433ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136859904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a888098749d9ffc4df081d0066983b0bffeefed4cfc8ba634b798e10b682246f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:15a0811b2608aa97b4e0811060ffea557de20e605122f0c38825f47469947704`  
		Last Modified: Mon, 28 Apr 2025 21:10:19 GMT  
		Size: 47.4 MB (47428611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b453de73db44edcda29182f13881db794c74b0f335096c735f5f88ffb61b994b`  
		Last Modified: Tue, 29 Apr 2025 06:01:51 GMT  
		Size: 24.5 MB (24474447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e19d072d3ad687af2af376c719bde109abef8c58cb05b32faf7ed3c425f5c84`  
		Last Modified: Tue, 29 Apr 2025 06:25:46 GMT  
		Size: 65.0 MB (64956846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dc679e06c8be5219b394c1eec8cad11ad6b7e8764f232d32ff54213bfc521c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4cf23939981701f244ad0236b28df9016ccc01ba5d3ecfee948fd3528db249`

```dockerfile
```

-	Layers:
	-	`sha256:9712fa778f2f662faa3d0a50fd4885b50b808fb76488f738c4c59a2ec9e215d4`  
		Last Modified: Tue, 29 Apr 2025 06:25:44 GMT  
		Size: 7.6 MB (7598203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9cd8560c288edf38f090d3823998b7c147fa39f6e10fc9e6420d87ddb24521`  
		Last Modified: Tue, 29 Apr 2025 06:25:43 GMT  
		Size: 7.4 KB (7373 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e7b975361342aa99185f100b50088f3a0413107b5be475dc6bb5c77127052a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131905483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2290b97599432737e571625265b8df1f85a3048ede548898f6be19545a8ef4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d877c043ab6ec52d6d4eaeab7dea355ef83893e584af00854b55ca611a3bcd99`  
		Last Modified: Mon, 28 Apr 2025 21:19:08 GMT  
		Size: 45.7 MB (45683821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785865296d03ccb31a01d56e5adab53e0c986bcfdc0c9920d48d9b1d2d93eda8`  
		Last Modified: Tue, 29 Apr 2025 03:39:17 GMT  
		Size: 23.7 MB (23738374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e434d6c9a7d808d76e24daf0efac32e9c61b3a7b5f489a41bb49c2842179975`  
		Last Modified: Tue, 29 Apr 2025 13:26:13 GMT  
		Size: 62.5 MB (62483288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0d8a1672ca937c282e5fe0f56433ae573969f90af495d126b87f6b4ce6fd419e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7599123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d326d1f35b8cc39173d833b1664dabe6107f5675ce4a988a78886c1b37634a`

```dockerfile
```

-	Layers:
	-	`sha256:6bfb0a2a3133b5eaa9baba858dd8d414fa9467aaf769f1f4bdeaa09f972bc0f2`  
		Last Modified: Tue, 29 Apr 2025 13:26:11 GMT  
		Size: 7.6 MB (7591749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f75b222ddad45d341088deedea8f3b3fd5f30207aa8ed0d681484dc900cdf7`  
		Last Modified: Tue, 29 Apr 2025 13:26:10 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e9e46b2f36a23cf45dd5760486ec3c94cd7a2babe22e0813da5774777fdb43bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142007056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2c84d5bab1c16cd6a3d94e1f59c3307651d5ac21ebb7ab81135ecb2076bf14`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Mon, 28 Apr 2025 21:23:23 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6faa4d9377738e3cc52e5d3cadb55bd77d367fb6439d9d14741079130dc9e4e`  
		Last Modified: Tue, 29 Apr 2025 01:48:13 GMT  
		Size: 25.1 MB (25116968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d10b7fbeb9c563c295c91ba384fe4305118a0d8b88117bbf9e5d4d3c3f9787`  
		Last Modified: Tue, 29 Apr 2025 18:39:19 GMT  
		Size: 67.3 MB (67265970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:39ffba9b627d09471c71bb4cfe185589f163e49d0e227227bd50a89e9ae865d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7606306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f67d247c9872d543bc2dcac9c5a5bf9b6f09fde360d86e1876f1cb6499cf89c`

```dockerfile
```

-	Layers:
	-	`sha256:aeecb0922a3b1d3710995c9663bc641ef930cb2caa32b28e538fb91fcbc22b88`  
		Last Modified: Tue, 29 Apr 2025 18:39:18 GMT  
		Size: 7.6 MB (7598913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:597ed807e0f36e840b86a5b5bdacfd74e55217f5708e69126d53a3efdbadbdef`  
		Last Modified: Tue, 29 Apr 2025 18:39:17 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:16b1dbfbf6c19fd740e70f0ea7535a207aec0321f5446324212cb04e5d125dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147162908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83ebf2260c33cf24108549f959103aa24ac4e6dddfdc7a78271459d13a1a728`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7e1acd19dab9f7ab62b7570b85e71035e78cd9d9b9bff975df4b0a635578c7be`  
		Last Modified: Wed, 21 May 2025 22:28:11 GMT  
		Size: 50.8 MB (50761280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24ada90c6b3f67e8ac11f8d9700e1fbeb5f64ed848c2ef5d89e89c3d1161d7e`  
		Last Modified: Wed, 21 May 2025 23:19:58 GMT  
		Size: 26.7 MB (26745816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53475a03e00d0d9a396cb70f6edb89c6daaba7c95e28d935ced8a0100b7b7bc9`  
		Last Modified: Wed, 21 May 2025 23:38:03 GMT  
		Size: 69.7 MB (69655812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:76844c192aa756d088a0cd28f75f2d23ade712e7d3b55328bc3131eb02ca6c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7590328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc7c36ac2ca91fe322dcb854ffd3bb88aff53fe7a214160b0f1ff95293d4729`

```dockerfile
```

-	Layers:
	-	`sha256:4c597acadfbdb2dfe8551ef142270217aeb0e7b6d98007f7887f04b716a73466`  
		Last Modified: Wed, 21 May 2025 23:38:01 GMT  
		Size: 7.6 MB (7583036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a4a31c6d01a15764486d38d9951059a091be429e5e4e420beb11aa0f7b715f`  
		Last Modified: Wed, 21 May 2025 23:38:00 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:88d2be4218236fb2eef3d7dfb081eda2123ed01c0afb31884896b0e1b17008db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152752343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfa5bcc9d6752b022d4db81da3415f38b32fe32bc8a2ce147a71513582b7d60`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed88abda34c2c7766794d61fd8b43cac1ab4eeadc9f85398417820583a09e36d`  
		Last Modified: Tue, 29 Apr 2025 07:48:18 GMT  
		Size: 27.1 MB (27143577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fa77ab766e4eed4e829b6e08390c6a1dc6b2350ee6134f9e56b8061b308247`  
		Last Modified: Tue, 29 Apr 2025 08:30:35 GMT  
		Size: 72.5 MB (72536214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ab36080f6c3c361af82a2d86a977e20106e0990fb4f4542abeef0fc6738ff70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7611730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b010a6d67087304ba741855ac4126845fc1eb73b24697dffdcb65c3a63ae437b`

```dockerfile
```

-	Layers:
	-	`sha256:279c1ae6444f3c665dde4e022a361339957b1ef482fc73b79d2c4f8204a94c79`  
		Last Modified: Tue, 29 Apr 2025 08:30:33 GMT  
		Size: 7.6 MB (7604384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ccd06349b9a6a423f38fa57e22e9f2241541eddb53ae86a6348a143a3db552`  
		Last Modified: Tue, 29 Apr 2025 08:30:32 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:54ba23fa8a5ffcb880b7753b6c1d7ec174d532a6e501bcb1772fc7c88d77af7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139252299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca75d8af1799275f25d0e3c784397cc27370ca737823e538edc5b8f9e71c4ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Wed, 21 May 2025 22:36:51 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd8670e232ca11355ffc7ddcb280e00c712f98c6d6ef1c601d041012816cfa`  
		Last Modified: Wed, 21 May 2025 23:26:24 GMT  
		Size: 24.9 MB (24917594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eab19773c2912f0a6e7295e8a9ea585980b042ba4f201575fb17ac1763bdae3`  
		Last Modified: Thu, 22 May 2025 01:15:24 GMT  
		Size: 66.6 MB (66603294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee1c7757c6ed3dd2a6b693495f2fab7160131ce3c05646e915edb74279a9be7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7584054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfee7396a41fdd371b836ddd8a76222594ddae42f6f5820cd3dd7826b152e069`

```dockerfile
```

-	Layers:
	-	`sha256:90546302bb34affa8b1705430c3f7ee5ecb61eef8167d46ee935d988d7d17a5b`  
		Last Modified: Thu, 22 May 2025 01:15:16 GMT  
		Size: 7.6 MB (7576708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf209c649f27166d4bbc5c5e0d3ceba15670abd3a620960fac1f9eb2f04bd9a`  
		Last Modified: Thu, 22 May 2025 01:15:14 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7599203c83c28f74a5f6dbd6c45154d089670b7a8a6554fcbb5aa46e8f0ca13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144551237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278b8cebe082d42caa4a6222d639ec76b8152f0e91717003b96b438e827285b3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e1ec3b1570f7d822c5a6aa013529484429ad99bde8495d827b56c3603992fd3c`  
		Last Modified: Mon, 28 Apr 2025 21:11:06 GMT  
		Size: 49.3 MB (49316646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2dfe09dce90ef60478379ac93bf4db4640c14411109c4ddd5060ffa49cdfa1`  
		Last Modified: Tue, 29 Apr 2025 00:02:32 GMT  
		Size: 26.9 MB (26932582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683df7242435f0ea9a0034ffcad35c09ebe0ed400dc39d5de0e749bf3bf141b1`  
		Last Modified: Tue, 29 Apr 2025 03:00:34 GMT  
		Size: 68.3 MB (68302009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a2e78066a2a3999c00d11df2d67cbd6d2cd06b2be689b3aed428d8d178e1fb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c868da5307cb540c135b927981f9173febbf221c7cc2d2d7705ec831311ff5a9`

```dockerfile
```

-	Layers:
	-	`sha256:e0eb794b3efd94a295a01ca43ba194ae1519115b8e4563be50f3a405d07b2b0d`  
		Last Modified: Tue, 29 Apr 2025 03:00:32 GMT  
		Size: 7.6 MB (7598370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1646ebe9f132b1fa4bce0cd295eb7f9dec03ea39454778726210cffdea487573`  
		Last Modified: Tue, 29 Apr 2025 03:00:32 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
