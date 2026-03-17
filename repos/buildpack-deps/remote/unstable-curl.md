## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:cd9e0e391c925a3a6d36ab4ed4dfe18e20022f3f6aa4624de7fc8629e343ac97
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6cffb4ab9fb3c7825c5c53c7120b140aaebcf8c7c99245e1e8f43066babcdf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75729381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5ffc4c3efe45793c5935c5aaf254461c4c27dd7e66ec7383b1fd42a8a350f6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:38:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:224b32b461470cab0a5b83292cf42319369c28ec8beae34418e705d6d0530bb2`  
		Last Modified: Mon, 16 Mar 2026 21:52:47 GMT  
		Size: 48.7 MB (48676470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a66b0373915b5b0ff298f6d01930222275f988f068d5fcb313d283986e46e2`  
		Last Modified: Mon, 16 Mar 2026 22:38:20 GMT  
		Size: 27.1 MB (27052911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e230c5c65685771e59a4d83c274f7c397eecd5c6f8dffda628406b50fa6bf5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4079260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211fd6faa859f851a65f625cfbf004346d976cb30670a09bf46cb0627310bca5`

```dockerfile
```

-	Layers:
	-	`sha256:f597c61e8cdcb5924fdedc94577e4437b73acf88875761bae24626ccb5a9e723`  
		Last Modified: Mon, 16 Mar 2026 22:38:20 GMT  
		Size: 4.1 MB (4072499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a55a2a04c7042fe87207fc209d10d75b5aa2bd5fd2d9b6efe3b5fb85accd92a1`  
		Last Modified: Mon, 16 Mar 2026 22:38:19 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2bce98d8d83dd0c72e9883d8b6574b13de90e0d5f663659dee78703c0cabd5e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70341387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053d9ec93d9af1b911c5b16e6e99113f7ede61278bfd8d54fa45ed3d759a2429`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 23:20:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f1150d74d9a03ef5fc137e050707adbd0a633a512d7e857d5d41c0f52ed63b6`  
		Last Modified: Mon, 16 Mar 2026 21:53:06 GMT  
		Size: 45.6 MB (45603619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1259f6d3d9e33f08f57016f1004a7104b71912ae731e4bade14636fa859034`  
		Last Modified: Mon, 16 Mar 2026 23:20:59 GMT  
		Size: 24.7 MB (24737768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:43195f96c1be863717a1d458cbdea54201137870a1df0f35f4e985fc301c13d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4080813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932ec77a0df479bf4fc25599cb357fe27f3602d3dbee8a5d691dc7b9e5d862f8`

```dockerfile
```

-	Layers:
	-	`sha256:b48f2492435231a9ccd5a64f03e694841b88211c46dcc5183eb77bd0a20583de`  
		Last Modified: Mon, 16 Mar 2026 23:20:58 GMT  
		Size: 4.1 MB (4073989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b54366f75d04276fa34b992aed3c4b1ff2117d32b67aadf3aab8e7bc8c4d271`  
		Last Modified: Mon, 16 Mar 2026 23:20:58 GMT  
		Size: 6.8 KB (6824 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e887b24168f5193a108871d37089f70975f4b5c43eb97d1f949fcf56d22791f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75063903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9adbe533a18eaade58b1160eebfea46be3dce12ce8bbefc1c8eccf8be2b504d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:40:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f8aa045b0b46f2987d2dfdc549957d53bf9eb7148b1452027f1bbe82759ee08b`  
		Last Modified: Mon, 16 Mar 2026 21:58:00 GMT  
		Size: 48.7 MB (48715175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4752dba1929fbf2811a63d55454ace7a1b8ccade962d6236fbef7e09ca8fde84`  
		Last Modified: Mon, 16 Mar 2026 22:40:42 GMT  
		Size: 26.3 MB (26348728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d92fa958ee897c2396eae4efcca7e48d1ed5565a7a03a2929cdde33a7cc03ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4086795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbc166d3581b0a23a7460f6508b5975694e26eeb033d26c451a765ac7276adb`

```dockerfile
```

-	Layers:
	-	`sha256:b272e3e22fb4f65bce2c9f16cd48e1debcc3a12e8bf1dd31354f6b1f823d070b`  
		Last Modified: Mon, 16 Mar 2026 22:40:41 GMT  
		Size: 4.1 MB (4079955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8294899ccbac9bb02b60b6a6edeb6fef563a8c9734c8f9744822c23dca40b891`  
		Last Modified: Mon, 16 Mar 2026 22:40:41 GMT  
		Size: 6.8 KB (6840 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f570ce47355ff39f0fbff37fe469e079fcdb21520bbdc15c4aac12ae1b1e4ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78266372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e56514ff99b50522f96199990cfa310cb6f419914ab04723646a38f7b4dbcba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:44:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d910d8b21d9682e89de3d97b422096e3120f61049a143cd139a1c42e9bb8b77e`  
		Last Modified: Mon, 16 Mar 2026 21:53:09 GMT  
		Size: 49.9 MB (49948047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981595a3cf9f38cbe3488cf7a822683f9aa76478cc3b84d65d23eeca02df1f21`  
		Last Modified: Mon, 16 Mar 2026 22:44:21 GMT  
		Size: 28.3 MB (28318325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:adbd91a0e9e52377cf7535b11a092f3ef28b3fd455fe8ab9314553847b0a67a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4076346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113b1a379f77ae4ced4d545dd061bc71518932f0265f57fe4df74c220ceeb29f`

```dockerfile
```

-	Layers:
	-	`sha256:3d961d8fbd2a3bd99fa63ada6697dd31da76eb6797263c17a5d0333b7f4af288`  
		Last Modified: Mon, 16 Mar 2026 22:44:20 GMT  
		Size: 4.1 MB (4069607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b3e3935d5dde25a14e31abc7acb5fa4149f8ae9b92394045c1959e9928d467`  
		Last Modified: Mon, 16 Mar 2026 22:44:20 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:820c40589769232c721e4ff63828eb6e69904194d764fac09c3c3c9ff0acd6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83218578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f649895638300b2ddd04c309e0940997f8bed273485988768a0f9ff5756075ab`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 21:21:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:98cf99f8e5f75111e243f4d3c092140d6c7618c5cce72eba92c5c2c4d8f97f2a`  
		Last Modified: Tue, 24 Feb 2026 18:43:36 GMT  
		Size: 53.7 MB (53670202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c9c8da854a9fd9a96b0f203229509ae404e6f58b91c885234945a59771f957`  
		Last Modified: Tue, 24 Feb 2026 21:22:11 GMT  
		Size: 29.5 MB (29548376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:17f8aef41cb08316602a527774f261a5afd0805e40bd60f93fc239d3bbe3e089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab3150a32c194aaf60537454bad0faa84d1633b4d4f8978ac0dc7e8009ccb8a`

```dockerfile
```

-	Layers:
	-	`sha256:3f56b00fd40839c9deffc52b5240bd0917de28f3f4a590e9fd8f0b442a5b1d2b`  
		Last Modified: Tue, 24 Feb 2026 21:22:11 GMT  
		Size: 4.1 MB (4127856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9e3ca729cb83d6bfe72cf97b3453d380d07373e88c4e9c32606b87b928e5bda`  
		Last Modified: Tue, 24 Feb 2026 21:22:10 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3abecce4a09efb3bd3d5e04188b1d9b7b87fc3e593c95d1fe76f3759abda0250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73383777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef67b61e50a26b0ba6c07d131feab2f90f512d88ec86bdc013f7403ef22c965f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:841ba95affedab9f4249c4c606ebf4cc415dddd1f44cb3edeed8f5199c8d1168`  
		Last Modified: Mon, 16 Mar 2026 21:58:56 GMT  
		Size: 46.8 MB (46778346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550401bf99e797417727d38582b31e96ea6704ee9ebdabb221407d77e3831412`  
		Last Modified: Mon, 16 Mar 2026 22:32:13 GMT  
		Size: 26.6 MB (26605431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d6b0ffa894f9decfa2b28ac0c0f5bc5ce504dfc60d89af7790e5f4869a9892d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4070988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b48be4467fb6fe91cd23243f073cf02c501d0d59e1c86a0d7c51eff85d4e70c`

```dockerfile
```

-	Layers:
	-	`sha256:da2c67c2dd75bea79fcd9b5a51e3052e9f706a7a09010da81c10fe8181f45a4f`  
		Last Modified: Mon, 16 Mar 2026 22:32:10 GMT  
		Size: 4.1 MB (4064195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6108eb082eac32fb7873769df182d22ef41dc355bfbd19dc80125e628a79eef5`  
		Last Modified: Mon, 16 Mar 2026 22:32:09 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f43d85e73f6ec029ea6b4d484ead89b6f4bf536633f9ec7ee06744f950777a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75497831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74f114769cdf6bcdc02f7b513a410a6de38fe6921520edd07e94edbf848b080`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1771804800'
# Tue, 24 Feb 2026 20:57:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b79b6ca78edd108b2b500a1c2abe8a5f5b6dee5dce46c5bd663b643e7c568362`  
		Last Modified: Tue, 24 Feb 2026 18:42:12 GMT  
		Size: 48.4 MB (48447710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694122fd04e83fa7d8372df97237755c6e7de35a0f627724e622c594e1610bc1`  
		Last Modified: Tue, 24 Feb 2026 20:58:22 GMT  
		Size: 27.1 MB (27050121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a5e1f920730f165fd889d405c384cbebdc5f03b6378e401bae5bb3f69cd1435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4d18fbec994aed316f64df6e6e6bbcf7bb5ffa540440ebab8ea3b6c14dcc1c`

```dockerfile
```

-	Layers:
	-	`sha256:95f975649d9871890b84930c3ef64b462b47c1057f5c8ddfcf66636fdfab45fd`  
		Last Modified: Tue, 24 Feb 2026 20:58:22 GMT  
		Size: 4.1 MB (4125390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b7eb85000f15cef803d0ff3acc4924a23150e7d955026c2320e0aabf9dca3f`  
		Last Modified: Tue, 24 Feb 2026 20:58:22 GMT  
		Size: 6.8 KB (6760 bytes)  
		MIME: application/vnd.in-toto+json
