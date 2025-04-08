## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:e374f11b5986614d1671353e67390d92fb7dba30b4a2f5a4b5040b1103434665
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:800f02d4ad22de4be2ed9339b1a9cf66142bf9766b29732b624d907aa005520f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141838901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d39b5a7e77606f4befc02cd9f0634d596f4eba4fd272135fa6fdab5cb714ce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2aa53e779a14a678b6be0553334055853528ebc9774eaa3e69e5fd71326114f8`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 49.0 MB (48967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505e1c0337e142d28ab6c58fa7e5bf319287c629af695b520d6eb278c386eca`  
		Last Modified: Tue, 08 Apr 2025 01:24:25 GMT  
		Size: 25.3 MB (25273414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68956bba4f38c9a7df8163b678a6e5da9925d8244f2276ad427d279ae2fff2d5`  
		Last Modified: Tue, 08 Apr 2025 02:14:00 GMT  
		Size: 67.6 MB (67597538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:28a3ad8675d0bf30783caa5c32554824d4869e501d82d9fd408545590725bb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7612107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61819005bc59a8b4ca1b5191ca817f02a5d9d5748d4a82028f0648938fe9222c`

```dockerfile
```

-	Layers:
	-	`sha256:dc079a9a58447f24122b33fd415df0e42c13e344f3ca3bfa7fedf507584e14a4`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 7.6 MB (7604810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b22e0d3124642b9ebd62ccfe785cde6be35dfddf6b375e1a2aa56e81479ed2`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4b8cb649885f173add39115c34c1176b822f7c87e24221c88259af5e236e15b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135735094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d1f663b24a5d657c96f1005a115721d655ec2afdadcd3d97816476e191a732`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:181ed5745a356167f17446082e0f91fa4520dec07c3cc08122f73d6e68f0ec6f`  
		Last Modified: Mon, 17 Mar 2025 22:18:17 GMT  
		Size: 45.8 MB (45764033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce18890e4323b22dabb2af5cd6dd6ee47e0cbe22914fe96ed5ec5652746adc9b`  
		Last Modified: Tue, 18 Mar 2025 03:09:17 GMT  
		Size: 25.0 MB (24962637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404f8f7fc411f8ff4d9e0e372fba1e5c10c5194b11ce9185a2da79073a4ac30`  
		Last Modified: Tue, 18 Mar 2025 05:17:45 GMT  
		Size: 65.0 MB (65008424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:730ac9c5a2e1538fa36cd60ff8fecc642c90adbf22911fc099578f36f3f41889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60638d368b2d9d81c0cb70fb38aa5b87dddf35cbe2809a64091735634253f293`

```dockerfile
```

-	Layers:
	-	`sha256:07c7153a4daf4952d41229ae9339de39c3737bbe1a70514bb57f45d87e099b2a`  
		Last Modified: Tue, 18 Mar 2025 05:17:43 GMT  
		Size: 7.6 MB (7594773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96b5e63b0facc4dcc7d63a5fc0aa45bbfe8324c13fe7681aba39180569da9ee7`  
		Last Modified: Tue, 18 Mar 2025 05:17:43 GMT  
		Size: 7.4 KB (7357 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cb6a860df68f240f1080950e46cb2b0a6d7db7052ce4d3173e95deec4a8d8c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130605599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccc27cd999c812354a72b97069f3b97585200566e7e544a16ef1e4c22872980`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d0067c75852db589ec6309ccaa1c2e508a0e7bb3c58863fcadae19a1c1537e18`  
		Last Modified: Mon, 17 Mar 2025 22:21:44 GMT  
		Size: 44.0 MB (43957597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80d864355272bf90fd1144966fdc99f539dd4252af76ad0a5d7e1ee868d856d`  
		Last Modified: Tue, 18 Mar 2025 07:22:02 GMT  
		Size: 24.1 MB (24132404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef046ac7256a24a47a1208d1dca17bc5d10a76b0eec3d2cd94577b18be639d4`  
		Last Modified: Tue, 18 Mar 2025 15:31:50 GMT  
		Size: 62.5 MB (62515598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5e2ba93def939bb93185461c20171b3e35a5d38e267f0c16ca2da5bfeb58a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7595673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af48e9b86ebd9a1a2bcc864f635dd6408e7506545f07d5f25276feed858746d6`

```dockerfile
```

-	Layers:
	-	`sha256:34ee1aaf6e91f0c95e5120862a6bca9679bd1d518ed0a7400abe51d85b4cc8f2`  
		Last Modified: Tue, 18 Mar 2025 15:31:49 GMT  
		Size: 7.6 MB (7588317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dc0887e18c2fae6e74e29401330cfa80b37aeea432c182072ba3e0fc78c93c3`  
		Last Modified: Tue, 18 Mar 2025 15:31:48 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30f194a69a5c5331493f30dac2a24da8056ecbfe88d4c40991519211790a9ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140944992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2f8018a42371e40946c0421052c0b750c0295094acc0cc444949b8ed8e22c0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:94a031aaac55d50c4495d8888a65973ac1a320a931aa0e73e9fb6cef43e2efd2`  
		Last Modified: Mon, 17 Mar 2025 22:20:15 GMT  
		Size: 47.9 MB (47916898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9c585ccfb21ec8756fd9ca6b5b83f6e36d0003a2342f6f55b3087ee0d0f4c`  
		Last Modified: Tue, 18 Mar 2025 04:59:39 GMT  
		Size: 25.7 MB (25697882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6d5c4d521a51c32b5544ee4fd67c57ead31e48e0d9a394edb180d78318d630`  
		Last Modified: Tue, 18 Mar 2025 13:17:35 GMT  
		Size: 67.3 MB (67330212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:617fdf2cc54bf661d8905095c7fc9486960ee733668e180920980e67ceb46be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7603503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd64101264af48e7b16ea79c040ff3ff981a12a211ba4f49ae61ff7aa91b611a`

```dockerfile
```

-	Layers:
	-	`sha256:4ff7d295ab228804ae281aff7f0bf871d5b93f8e1e3fa23667c6595ac435cded`  
		Last Modified: Tue, 18 Mar 2025 13:17:33 GMT  
		Size: 7.6 MB (7596126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7568bca48c62340611dded011153ccde850ea650a89eef9c5c6159c8b00a1615`  
		Last Modified: Tue, 18 Mar 2025 13:17:32 GMT  
		Size: 7.4 KB (7377 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:56d91d6ead2cf54fad200da22908ec75998725d5e6713d2b9d1791eb91b76582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146381595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2eb6edb45a943b8bdabfa6d1bfc4a492fa5d2b8acf42d8be5d3b541721cf7f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a0f0bbaf0e5a890ab90a12e5df307c321a3344fa0accfb31dc895fe008c16f85`  
		Last Modified: Tue, 08 Apr 2025 00:23:19 GMT  
		Size: 50.5 MB (50476501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686927d82bc30ed67f20e1ddfb9d146b7acb12e90c947c73db07541c131a8cd5`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 26.3 MB (26298358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f78585b0ae6a95bc4b41ccaf9f3cb3acfdcca008d5b11330a5414a8ef1b7691`  
		Last Modified: Tue, 08 Apr 2025 02:13:58 GMT  
		Size: 69.6 MB (69606736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:685de755051800d7281f1b3d5486b6ea23ee60ee49cf0de65438969d6acf1964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7608154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e26fbc2312e6c210aae26d028c86782d35e412a9299390a47bd2485fead037`

```dockerfile
```

-	Layers:
	-	`sha256:a1e94ca1c35b7b11db21ddb7a22a29b752ca66a9d8ab61586c471bb246a85149`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 7.6 MB (7600880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71d100c2597b82364be9c9b86f3c50ade3e6a50380c96a16a2b4f04d79bfd672`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 7.3 KB (7274 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e825156523fb1083a70290fdff7870a525d7ca38831c8431414360b4fea7c81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140567265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d620c37c43224ee032bcf67d4a24976bae2687580176f1d728b4c57f1f8449d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e12542a0a53bb97cc352ca7ce416a009a12137a70b8b9c3e736be4923c559ab0`  
		Last Modified: Mon, 17 Mar 2025 22:20:29 GMT  
		Size: 47.8 MB (47750847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e581beb347f24f554e5f2cf2d1525cb47adbd2ebd171f2c46bd47fada5257b`  
		Last Modified: Tue, 18 Mar 2025 16:30:23 GMT  
		Size: 26.3 MB (26282283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f3cc7353bb84ae34c688ff3596f801439d22635390e86e17ef4a03803ec818`  
		Last Modified: Wed, 19 Mar 2025 05:27:01 GMT  
		Size: 66.5 MB (66534135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f39960c4a777e5e9ef8ad79fea822b77aed8a0e3cffed5d79c111db746f782a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3c5d507434849ea49191e80ff85416e7d634f56bddf4d43481a6885d77c195`

```dockerfile
```

-	Layers:
	-	`sha256:ad5da8a3a38e5b37de2a54a8483f372dad8e5f36d9780e831e8063e2b265a275`  
		Last Modified: Wed, 19 Mar 2025 05:26:54 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e42519f34446f7588d389bc3637752554d92126d4456e1352260cf2c96029e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151724962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1349883cf691f5076f40af2d1ffd55de868a46e49f93a81626b0fa400f08d38`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4f7ad9881f20bb4c15e9c02d5c71121438e0f80af4492bc3595dca35345480d6`  
		Last Modified: Mon, 17 Mar 2025 22:22:55 GMT  
		Size: 51.2 MB (51201856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277e01a580518b309bd39ae29e17784505bd4ae5bf702764ef69018aabfb218e`  
		Last Modified: Tue, 18 Mar 2025 00:01:23 GMT  
		Size: 27.8 MB (27793733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1b9cddd723c4c8c3ec8dc918782516b3f18afb7b43c91515f8578d7f2ee55`  
		Last Modified: Tue, 18 Mar 2025 07:11:29 GMT  
		Size: 72.7 MB (72729373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:89b7df5211265aa578760e6bc57d977d8cef3c402c9ccbdc8d1bb183df766137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7608289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a05c7c33dab5f791d2f249714c5c8ab937e48a09adc98af69eb58c018f46245`

```dockerfile
```

-	Layers:
	-	`sha256:2f6d60e49c054c15ef97b5077caf2377e2969a07ba4b646fc2aacf9d3ce48451`  
		Last Modified: Tue, 18 Mar 2025 07:11:27 GMT  
		Size: 7.6 MB (7600960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea4d952c7468ce83328a8304e47d3b8b9837b1fc87ff5300e1b13ac092ab215`  
		Last Modified: Tue, 18 Mar 2025 07:11:26 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d93e840deedb035dfb355ff7e290c5e8f0e9aaf4047732c73b193fd048e493e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138584538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c58088813a450129822a8cd9a3369cea3447e05ffd6091dd282d3b0e9aeb49`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9c53dca7ad1a1783f586e5e01ac8c6a23808333e74dea8e73cb813fed1a625b5`  
		Last Modified: Tue, 08 Apr 2025 00:25:11 GMT  
		Size: 47.5 MB (47479327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe0734c1595d1fe0c36013a6078b10a14e39d1128a06575271e9a043d41f2a`  
		Last Modified: Tue, 08 Apr 2025 01:22:05 GMT  
		Size: 24.6 MB (24613675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6508389986649aabcea20a16ac597e9453899e4f0fcdc57dab93e6abf5afec42`  
		Last Modified: Tue, 08 Apr 2025 02:18:53 GMT  
		Size: 66.5 MB (66491536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c50f8b18b54a9971af2fbd56f3c88d462dfad3703573a42878e0187a5e60e2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84333dcfaf82005208c751114094b195a08635102681a9be89f3431b8244d36`

```dockerfile
```

-	Layers:
	-	`sha256:b47a3ab6ffcc4a5fb2009aa560fe32341dddf8f701c3926f0d1fc20e23f87c9c`  
		Last Modified: Tue, 08 Apr 2025 02:18:44 GMT  
		Size: 7.6 MB (7594732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c800b76168b9a798e494d5dd18238f02e205f0aa7fe5750ba9998ab7558e6617`  
		Last Modified: Tue, 08 Apr 2025 02:18:43 GMT  
		Size: 7.3 KB (7328 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d54984cd29e40cb6efb0ec71ecbdd6f5c5c37ac1e2f3f1404afd02413f268172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143092428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a0f102b754de476a80f9982e445eafb2b4d99fe325bb16081804c3289cfbd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:18840c5918002e02a891410ac8cb796ccc166700f997d1063ab46da46dc721f8`  
		Last Modified: Mon, 17 Mar 2025 22:42:36 GMT  
		Size: 47.6 MB (47571368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d448240a5617efe437620dbc6c199b4b34036766dc8ba22365b81ef5e32d08`  
		Last Modified: Tue, 18 Mar 2025 02:50:47 GMT  
		Size: 27.4 MB (27402692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151e745d023c42b8954a78b55b72c865750f57f9ee36521990f6f841b155c5ea`  
		Last Modified: Tue, 18 Mar 2025 05:56:55 GMT  
		Size: 68.1 MB (68118368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a99534960cc6471e52818fcfb7e2241ac2e4f373d50f904b5c9cdb203c896561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7583324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f06996a7424526efb2bead9dab512bd063ea2edce3d098ecd039982c724417b`

```dockerfile
```

-	Layers:
	-	`sha256:1476c8557ee496cf4107184e6ddfb8e2409a176b6aff9e08e02783b4bc0022aa`  
		Last Modified: Tue, 18 Mar 2025 05:56:54 GMT  
		Size: 7.6 MB (7576028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4b62b6df2696f5eb812954216e52b074e10c19838990566b83ebf739706170`  
		Last Modified: Tue, 18 Mar 2025 05:56:54 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json
