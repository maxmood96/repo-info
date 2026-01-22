## `debian:forky-backports`

```console
$ docker pull debian@sha256:2e6e0989c909f71636132552eb8f07bff56b20671c5c344156ac808e79729c7a
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

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:e1bed1e4055ce3e2f4ea94487dff544ea40ab6d263c9f8a16228da4e8d3066cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48836719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18a63e130b545c62abeba63b9e72012f41401a270aed6aa6d1177bc9a63414e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 01:16:51 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:743b991b49b557d24658aa3fd7faa6c90234b4433dabd04078e1e4904b8e483b`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 48.8 MB (48836497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a11ca61c95f9024a123798995eed68bf0b668c2f34e072bf2943c446baf33a`  
		Last Modified: Tue, 13 Jan 2026 01:17:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:88802e252808d78db79dbf51ec2d0e8b347561ef0451279422585a2c26c77316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3147817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b794cd7cfd017dfcbd13aeb74e56a2a5e5da146c6067c465c29734b51fdc1e`

```dockerfile
```

-	Layers:
	-	`sha256:f1dbff7bf76dc7925e0f9c03c098db59a3e08b304da36a873df8f860971b1e49`  
		Last Modified: Tue, 13 Jan 2026 04:25:33 GMT  
		Size: 3.1 MB (3142039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1217ceadad5938e22384952c05391bc143884d6f994d57ac8308981439e9a40`  
		Last Modified: Tue, 13 Jan 2026 04:25:34 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:fee82cd3ff2a271dbda12d3eb8e1b0f894bebdd0a8774ef3ce98c2f75d4793a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45128721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5492346972c2e91fe2da1d439a561f1e643ae86b903f3d3ce4bb4c3c6191d7db`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 01:17:39 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a41adf61a59d65bb732f71b8fa9e215ce26d7adaa7742f1d0d7dd0c7dec51f11`  
		Last Modified: Tue, 13 Jan 2026 00:42:25 GMT  
		Size: 45.1 MB (45128498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32db9b4d193840e9fb0ba500a7b05ea5cade2401dc4309375399ce070647a1e5`  
		Last Modified: Tue, 13 Jan 2026 01:17:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b76648d6f6cb8a4cd8d73118557e5d1fbd90e769241b3cbdb773dcad87ffc6e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2253ce13b4da95293ac2a30468abfb7bfd6c33953759adeded52fbc89eedf532`

```dockerfile
```

-	Layers:
	-	`sha256:6d4309342ce4ba9349a14d9762754932560be8b0d9a7da9f9421b4368c8d5a1c`  
		Last Modified: Tue, 13 Jan 2026 01:17:46 GMT  
		Size: 3.1 MB (3143407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:646a0a5925ce00149c9887ea5c41659705ad83610b53d5a5cab2e0c77518cebf`  
		Last Modified: Tue, 13 Jan 2026 01:17:46 GMT  
		Size: 5.8 KB (5833 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3125a1fd3f84ee7cdc5e3418992b6099a24cc7de6e3212c8bcb94569c3a4f5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48821032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac73f2fae5d7a702ff15772a0fb200aca92298dc996d96c6b505a1c24b434a9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 01:16:21 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f0e1c9ce589fdc56e77162978a9037d5d8c63c2e5d6fb4fd4b325ce20394aa61`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 48.8 MB (48820809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270c7bba98969f4ee34dfdf708914620c171291f9d921677b5840e7720194cb4`  
		Last Modified: Tue, 13 Jan 2026 01:16:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9d424337cef918d488099519ff237a5d703be428fdd5955ef97b77d953df280b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6481cae960b51f0c3ee4dd627390058f41dfa85d353ebbd54203e792497035a8`

```dockerfile
```

-	Layers:
	-	`sha256:dc83c98f0f525d08cf36b55423a2a69c0dd8dd87b98ada81e3c0cb46f2792029`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 3.1 MB (3142880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142681315a4baed655fd3b6a8945576a28a73f22d14d69e905235c360110d5cb`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:a596317fad5d442a6ad4642e53a6b5ad76d3307fc925db0945e6bc0870cd80cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49944770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d3b04e3d00a812398031e266acd14556837f8b4ce6668a1ccea1392ec0cb3d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 01:16:29 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0f5a7611eb50e1c295ff4c244485263852c6e6c8f18836cf55dc8b5a4162740c`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 49.9 MB (49944546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c741f2ce2a93d66cb9fa655274b898c2aae57b8774cdfcd943c0c23ba51add`  
		Last Modified: Tue, 13 Jan 2026 01:16:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8d038db0ccb25e0416315099fd436cc2401cecc43a658cdf4b17a5e59eac52d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e544886e1e95cf4de21bb427876c938cf27e89498c59bda3aa9799fc2c241c`

```dockerfile
```

-	Layers:
	-	`sha256:bf95cfb09e8caf75fdd40fb6881755b9b87562e0b0a2ba7f0d8d037685380635`  
		Last Modified: Tue, 13 Jan 2026 01:16:36 GMT  
		Size: 3.1 MB (3139243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9287936192ceb3d37d902fb4931bf7c3a7f963e400420a1caf70c42d9fe16ebc`  
		Last Modified: Tue, 13 Jan 2026 01:16:36 GMT  
		Size: 5.8 KB (5760 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:41e4ac6cbd1455524e50ce5f03c617d07167472a813f3202040ac3821c01db89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53516407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f39f8e79647cbe9e247c287a97b4ca148f5102815f16bf23db816f33864409`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 01:14:30 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7bf02b202abcdb3d6a49a7ce4605beb0852cfcc4e8237bffbef88f800d821593`  
		Last Modified: Tue, 13 Jan 2026 00:56:06 GMT  
		Size: 53.5 MB (53516184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960b3b43d316d0b65e6480de6acc805341cd4f1134bc59e8b91036713d3ba474`  
		Last Modified: Tue, 13 Jan 2026 01:14:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2cc90b6d89636c9e5d936d66413e229911baf1a4ded806b20784d1f82ca05757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26032ac701b42803632c54177f203ce9cbda6b49c1d6927898bc3676876f1b83`

```dockerfile
```

-	Layers:
	-	`sha256:6ee95967519b626e33f49cb95e5b2b81163f1a18bba9f5a8cdccb148e23f6476`  
		Last Modified: Tue, 13 Jan 2026 04:26:07 GMT  
		Size: 3.1 MB (3145542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fba394fa790ad003fddbe8054e919a2947cc5c67deac9d627d587f24ae24f6a`  
		Last Modified: Tue, 13 Jan 2026 04:26:08 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:f451d4695b411f9102ce34de3118930d66c2dc0b6b585df75c9f3792dbf177c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46854686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8557810dfa53da63142a437854fe76ad2fc9597a3761e48249c9f83f293c820d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1768176000'
# Wed, 14 Jan 2026 04:03:34 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0d152d1dcac9b1a7bbc763f3f2f3b2328b12317f387036c0ef1af1b70d3cf327`  
		Last Modified: Tue, 13 Jan 2026 00:52:42 GMT  
		Size: 46.9 MB (46854463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0f696d74d96ec399c468956e1ee94f1fa01dfc59dd3a9f02df83a04f80a517`  
		Last Modified: Wed, 14 Jan 2026 04:04:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fa95fde284364994b8e58f824b53d6c139c212aaaf427800c8c610b463ee438e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06840bac843257cae22e73e27707d99e409029cb194d87fa6f3dca8b74ecf218`

```dockerfile
```

-	Layers:
	-	`sha256:225c4abc6dc48755ab71b9d3b7fa664457807c2e131a22a6f9daad91be15f269`  
		Last Modified: Wed, 14 Jan 2026 04:24:10 GMT  
		Size: 3.1 MB (3133537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d81530a876e6438436c53ebfe68ecf92a6e6da9c189eb58576a3afa74b0cdf`  
		Last Modified: Wed, 14 Jan 2026 04:04:28 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:40a86404913d9a67785719a479786b6ff9818c2192744a574a896174ced580e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48389518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d43ed21541dc03b1bc181e94802a42390609949de08aa25e1bbda7d65d57304`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 03:46:59 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3dcc5871821327b982eb5b773ab24bb0eb85ffa1e8b8f4ae6dd4e94832450146`  
		Last Modified: Tue, 13 Jan 2026 03:09:57 GMT  
		Size: 48.4 MB (48389296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602d69a34b296116b83ea5e670ddedb0a6975725638950d802deff34c825d398`  
		Last Modified: Tue, 13 Jan 2026 03:47:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b3a38d08ba6977ca5f4589f674bb329f59821152a35399f616f66a263588962f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24218dd197fb65f869b088dacb6e9e48a15162ef9cb8c0a10731bc9173772e6d`

```dockerfile
```

-	Layers:
	-	`sha256:a50c009e41730ef67c6551323355af5c8ad522acdce4ea5ae96d55452057906a`  
		Last Modified: Tue, 13 Jan 2026 04:26:15 GMT  
		Size: 3.1 MB (3143488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7787c0dd79eb80e1e7c7bfeebeafaa0b15c3b98134e6f310dfd2a0c658c43723`  
		Last Modified: Tue, 13 Jan 2026 03:47:09 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
