## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:ba3e3a8efa6600ba0227652274aaf1b39200b4eedb949bf98924158b489731a0
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

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:dcd4120a3779119398c93dea4ff5b46cad37892ab1cfcc0de24b938d87f9e93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144442454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df21d4d7095e572014801276f98f4c5bae984ec29e9aa041aa536f07366fe88`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:490e982b5e2060f5a5ea7e5f586ff8bb98bb61a953b4473631a9da94fd85fe11`  
		Last Modified: Mon, 08 Dec 2025 22:17:59 GMT  
		Size: 48.8 MB (48817523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff8ebe9a9fefe126b5d099857127577acadfabc1b7d98ce416ca0faff37c513`  
		Last Modified: Mon, 08 Dec 2025 23:07:36 GMT  
		Size: 27.2 MB (27197450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefa9b0831ef76f3b6f478e168c5a2d244535ebb9ede263a69d319a2cdf5e22b`  
		Last Modified: Tue, 09 Dec 2025 00:06:54 GMT  
		Size: 68.4 MB (68427481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef3a386540fa1df3ae7ac47627dfb8f679165c8bf83c46226175f2ad2d615016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c9fa60b2a7da28882db4d0260365a6d30e592f15cfa7262b9ada37aa1bb92a`

```dockerfile
```

-	Layers:
	-	`sha256:a43baa7c45608289d3141b6ab0ac3b60527f987d5982594e25191cb2bcd4c944`  
		Last Modified: Tue, 09 Dec 2025 02:23:38 GMT  
		Size: 7.8 MB (7767067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9c260dac9fca3c341ada8e8080ffdfaed45576d0f894182cde8abdbb6bab60`  
		Last Modified: Tue, 09 Dec 2025 02:23:39 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6abac234ba4c0c32873d2aaff4b660a0a0ffc8becfe99706da4d4d3848caf831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133356791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e525bd7514d01483c60fbba815f96a6f93f315560a2602978a5169dc50ff19dc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1765152000'
# Tue, 09 Dec 2025 00:06:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:33:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76f9334b2a3a315cfbd527ebf785350ccdf20f285fafcc4cb59b172a12b89d6f`  
		Last Modified: Mon, 08 Dec 2025 22:17:07 GMT  
		Size: 45.1 MB (45118376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a62720547143dbd3a73491454b89436c575e1d06808adc4a4d023be5d9947a`  
		Last Modified: Tue, 09 Dec 2025 00:07:27 GMT  
		Size: 24.9 MB (24911741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4a91d293a2f08420426d89a5e0b168d8395fa90d22b8105ee6e181bae6303c`  
		Last Modified: Tue, 09 Dec 2025 01:33:43 GMT  
		Size: 63.3 MB (63326674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:37763028c822be3f5f7abff80d3eb96168c483de3cc385ef99413365b1d95fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e113770ec9ded7e1bf527232edc3ebd2810ae0c28d68270a00ec2fea7e4da30a`

```dockerfile
```

-	Layers:
	-	`sha256:713855a897140bbfb1da4b586cdc7b4f56354613099e0bd812387d43f60ad1fd`  
		Last Modified: Tue, 09 Dec 2025 02:23:44 GMT  
		Size: 7.8 MB (7767566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:836cb684087a5cdd7e3eef1422149f436636516b9091d8cf964631f506a1a895`  
		Last Modified: Tue, 09 Dec 2025 02:23:45 GMT  
		Size: 7.3 KB (7317 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5db1c335052efddc34be3e0d79b57d47c04dfb6e97655a43231bcb2f99b4bf1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145510111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c61dae184ee194c2963ba392290949ccb10cd0c9e8b3e87f45e77ea2f18eec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:26:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:39:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2b90f6fb16dc868101354a233036d6d70e13cd3477e4df5ab59f2ccc8607c1d4`  
		Last Modified: Tue, 18 Nov 2025 01:13:53 GMT  
		Size: 48.6 MB (48591389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f615e7cb4b13e78f79053e3ff3386cb79b093cd2d91fe819f692264eb1475`  
		Last Modified: Tue, 18 Nov 2025 03:26:37 GMT  
		Size: 26.4 MB (26445334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8961176208fb3c6520aee3a23dd4452025d1885baea507b988ee8fdfe1d8b591`  
		Last Modified: Tue, 18 Nov 2025 05:39:35 GMT  
		Size: 70.5 MB (70473388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9cf4c48b744075677479dcf70b0b8b9ec736e7b8ec6dfc60469f8a0b5ec3b0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8912e552663c641a25e488d55cca29992750711ee2da2d9838b2345ecd183b40`

```dockerfile
```

-	Layers:
	-	`sha256:84331b5373936c022c700d658cfa0f10bdf43ebaa8974aa5427c526999990eda`  
		Last Modified: Tue, 18 Nov 2025 08:23:11 GMT  
		Size: 7.8 MB (7754726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4de930c5145e104e60108f8c1c6fc81309c7a082a5101455be739def90324cb8`  
		Last Modified: Tue, 18 Nov 2025 08:23:12 GMT  
		Size: 7.3 KB (7333 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:303b552f170223bf9a10d8d03c7692ac987d04c78b626440df166bf2e796c480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148785638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ac46fecb9b65a87fc70f34c717eb8099a1d61f4e6112171cd9f5d5dec41730`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:24:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:67f7fae0ea3bb931c627a66604e60b0a242047b0c8f9186d188cf96e0133593f`  
		Last Modified: Mon, 08 Dec 2025 22:16:33 GMT  
		Size: 49.9 MB (49947966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9e94662795a8f26e5463a4bcfcaabfbdeca01c44b799e3fa96524d3ed5ff0a`  
		Last Modified: Mon, 08 Dec 2025 23:14:49 GMT  
		Size: 28.4 MB (28430929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2dcabacda9674c82129e92594c80d843967d7757a07ee38e58f0c8b9e9e24a`  
		Last Modified: Tue, 09 Dec 2025 00:24:37 GMT  
		Size: 70.4 MB (70406743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:37ceaba20566d02201a51fca9b61410cf4f12c806ab95de58609ac397245a547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291547d993414923a6d108e107aa3a9729ad5d9974ea847256bd4a1a520c6076`

```dockerfile
```

-	Layers:
	-	`sha256:c4520896861350f87b208558497785bd255792703aafa425e34a174f8a0f3739`  
		Last Modified: Tue, 09 Dec 2025 02:23:54 GMT  
		Size: 7.8 MB (7763203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad89cc9cefc6e7552e85d382ca22c2db86614c83822afab6799c39aa11a48d8`  
		Last Modified: Tue, 09 Dec 2025 02:23:55 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e585dfa2ae63172c3c543c7589893561ba2ee5b15e0a675c4fd112f85a856cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158743281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4f97f2c11ff5944911441f438b14e033116122adb647d2169919a90f668f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 04:06:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:52:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:233726152393942e1ef6b4533705d6bb3e4142964e6e486a7902cf456eab5151`  
		Last Modified: Tue, 18 Nov 2025 01:56:30 GMT  
		Size: 53.3 MB (53335631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8247117b12d78345474708e2bcd8a4be4ebcad8965145f6ab351c359ba9869b`  
		Last Modified: Tue, 18 Nov 2025 04:07:17 GMT  
		Size: 28.8 MB (28838475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df21c22b8199e396dd68073d81a213289efbf6a3e913789e13269dae310802c`  
		Last Modified: Tue, 18 Nov 2025 06:53:03 GMT  
		Size: 76.6 MB (76569175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b5fcf0f9c52ca1ac58ade10f6d3838cc22eab58a1fee2869564020db1a399819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96458ea08877dde78e78558ece91e859f26e9cf851ac72deccc836df2f27adb5`

```dockerfile
```

-	Layers:
	-	`sha256:6e3d8ba1a3118f585bd0cfad4da5694d4aec2999bfc29c5ef964a199d2cc7150`  
		Last Modified: Tue, 18 Nov 2025 14:30:22 GMT  
		Size: 7.8 MB (7754796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0956bbd86bad46cb6fd675da2ad90df0f4461c2f045a420d0130d94badaf323`  
		Last Modified: Tue, 18 Nov 2025 14:30:20 GMT  
		Size: 7.3 KB (7285 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4bdada01a6aea72f3b6bbbff11ee000ee1442ac85325e9866e1bc320ef701524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142799590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab01b3d0b98f7945d699319913ea29409da9f13c03768d3be5625ef1adfbbbc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1763337600'
# Wed, 19 Nov 2025 19:33:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:22:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed67ff00f4a63ed57f98b299833d8c2bd5b7627bfdca1af20fe366dfb5d9d552`  
		Last Modified: Tue, 18 Nov 2025 01:34:50 GMT  
		Size: 46.8 MB (46807232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12faa2c8d5976c2936626416dbd958b979633ec7e97e5fb377956f757414803`  
		Last Modified: Wed, 19 Nov 2025 19:35:09 GMT  
		Size: 26.4 MB (26394813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c856553cdba1b452f2934482676983f9c2dee9a9410ebeeee2db907f70948a`  
		Last Modified: Thu, 20 Nov 2025 22:25:57 GMT  
		Size: 69.6 MB (69597545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8fa7d9900e837e2086171182d088dd6c1aa73aaab5f41176b129fcbd5aae2907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7744785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dbcb557c00efc04d225cce5b8941ced1f51f35aca079b20a6b672588d2fd49`

```dockerfile
```

-	Layers:
	-	`sha256:eb29ff9110f71ab08cf4addefb9fc41f1134f40e55638c099d049e546b55ae4b`  
		Last Modified: Thu, 20 Nov 2025 23:20:49 GMT  
		Size: 7.7 MB (7737499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:348a9e13434f358e38f921454628d54ee6087a12029a731cae607f24ff91f92c`  
		Last Modified: Thu, 20 Nov 2025 23:20:50 GMT  
		Size: 7.3 KB (7286 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fe89b0da8067110ebeb9583ba3aedef86bc266da03b31cbbf614dc76bb9da79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145876222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd84db59840a707cca4c74df95cc1e80071ca306de057317dbb0e91128368bbf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1765152000'
# Tue, 09 Dec 2025 00:11:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a7cba59687143fa1a3bde49b08caedd4592355c94693db34a36ceebea332a04`  
		Last Modified: Mon, 08 Dec 2025 22:15:38 GMT  
		Size: 48.4 MB (48404077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c41c2bc13ca9c32fc8ea3b0ee8862d2350cf32202664571fd15af30f5ab552`  
		Last Modified: Tue, 09 Dec 2025 00:11:46 GMT  
		Size: 28.3 MB (28311739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5116962aaf70b7ed1f02f2ccd4dc554c6270985ceaf307b1f7833ab499653777`  
		Last Modified: Tue, 09 Dec 2025 01:47:51 GMT  
		Size: 69.2 MB (69160406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b458f6fceb79597a2cd0824315ab538af23b19ad14a90f3e583e63ab61b889ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f360123860a5b31d4db24693cdebceaf01ec3b10b396f2b6c5705c7e28935914`

```dockerfile
```

-	Layers:
	-	`sha256:fe5063963fcd36c834f105ebcf8e36e11f7001ef1e13dfec28d9d60b4a3537a4`  
		Last Modified: Tue, 09 Dec 2025 02:24:09 GMT  
		Size: 7.8 MB (7767980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1fa8fff0c1eaad63a93aeb7d42b4ef63090b82c925487879a794b8b44f8ce20`  
		Last Modified: Tue, 09 Dec 2025 02:24:10 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json
