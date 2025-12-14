## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:6139893ec70180bf290a64b5f5ae0181bcb2995dab9438cd455ce8dd6d2dcc02
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
$ docker pull buildpack-deps@sha256:784f2a957acbba4b00cf880d0615f21d40effb912cc954480f2359a7f35a2288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143490882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3473f437843f0148a34299aa74c2cc1bf1d43a002ef75cb48c710a973cf7daf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:10:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2e5b290b66ba04e2259d84d677cc1c79191dcc391b2b9af44fa26a4735123220`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.8 MB (48838607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e861ca4e0892270da154f93f8077287d4c0bd0913eed59fe54c6514a5d7f1c`  
		Last Modified: Mon, 08 Dec 2025 23:11:15 GMT  
		Size: 26.5 MB (26498040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa12addd0a7e2c939e7bcef4cd81464734e92119acd190fd47b096280916d8c`  
		Last Modified: Tue, 09 Dec 2025 00:12:02 GMT  
		Size: 68.2 MB (68154235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e868d73687ec3687102768ef57d7dbf017441054d97acb002078aa1207af66c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0836aa2b7a9b4d455f68d65f1208b674c682801df0891f1029bb873ed55897e`

```dockerfile
```

-	Layers:
	-	`sha256:c22b1afc8dd7c5b29a37d461f151dfe41a90b4373b272a97dc66e90eb39d6b1b`  
		Last Modified: Tue, 09 Dec 2025 05:22:14 GMT  
		Size: 7.8 MB (7774092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f2484cbcfb45af36d88aa9846e2330377051ffcd913dab5a7875d8b4a90ab58`  
		Last Modified: Tue, 09 Dec 2025 05:22:18 GMT  
		Size: 7.3 KB (7334 bytes)  
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
$ docker pull buildpack-deps@sha256:e0ff53c3f807889b5a28e9ae65c38fb7b4dda955e797971d74e7232592132911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156300372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133d0da785a92a06bde6cec06816ef1e95f9b320dfa81d9f81a85395bb7fa286`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:22:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:91f19749139bb2193587558635e0a320b0f29835fa1325bcb8c73b48ad8b72df`  
		Last Modified: Mon, 08 Dec 2025 22:50:49 GMT  
		Size: 53.5 MB (53494424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a82bf53318ee9ff50934cd5a455b97b8549b92db55df72cf410249ca6112c7`  
		Last Modified: Mon, 08 Dec 2025 23:23:07 GMT  
		Size: 28.9 MB (28884607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03e0f90ac822b83290c4938a8d44e3bfd579a2891eac5e11b8dec4f3a80cf68`  
		Last Modified: Tue, 09 Dec 2025 02:11:35 GMT  
		Size: 73.9 MB (73921341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:da8eaecb02afb86ed4776ac879c2afdc4d0d5e7ac54a0e211f5255cbb570cb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf2b2813fd2508cee53489d7c5150dd30f629d7a61d2460b520818e6bb8a133`

```dockerfile
```

-	Layers:
	-	`sha256:05ff2f047cffa4b6ce0b062d3fb5b3b640783d4c60b453636674b0145c3ec6e9`  
		Last Modified: Tue, 09 Dec 2025 05:22:28 GMT  
		Size: 7.8 MB (7774196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58cf7ba0c983a220bcc3ff6620e342bc4bbad99c28791ab40942955ba05907a4`  
		Last Modified: Tue, 09 Dec 2025 05:22:29 GMT  
		Size: 7.3 KB (7286 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:053b1dfc126481e5d725d600168c18abc0a939baffab6aee3edbee52dd5e771e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140564449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114580fc7d172397f566cf45872f1b986da29c7f523350051b7a98b2f15982fd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1765152000'
# Thu, 11 Dec 2025 08:35:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:40:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:109a9388fb2c93203e12f30aeaef237cc88f26bdfe719e6c75ba4b856571d621`  
		Last Modified: Tue, 09 Dec 2025 01:53:48 GMT  
		Size: 46.9 MB (46917024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c6713d289f87fadfcb1cc49dc5c1255a2e68dec8f35d177d80c213c8c3d375`  
		Last Modified: Thu, 11 Dec 2025 08:37:29 GMT  
		Size: 26.4 MB (26413809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3a6f1c36dc6239a02beb52306b77dfb11edb7a5a71763ffc22541d84875bb0`  
		Last Modified: Sun, 14 Dec 2025 08:44:39 GMT  
		Size: 67.2 MB (67233616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:901c5110763d511343a8b974ee06e4a2b9eb265733ad651c2a4eb90c81dc9f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7758496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002dbde31a99e8f49c3416b0527616e4a69537c884d643b232709f127dd4cb83`

```dockerfile
```

-	Layers:
	-	`sha256:3af57aada69d51dc50f1466a7640291a87e2ff2dd97821c37b95fe90488a6bdb`  
		Last Modified: Sun, 14 Dec 2025 11:20:45 GMT  
		Size: 7.8 MB (7751210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7acb74a6b8325e38c2383603fa35e82ef5b3ee052c3f53e8e6231d760b0163`  
		Last Modified: Sun, 14 Dec 2025 11:20:46 GMT  
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
