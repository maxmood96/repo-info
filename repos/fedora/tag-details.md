<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fedora`

-	[`fedora:31`](#fedora31)
-	[`fedora:32`](#fedora32)
-	[`fedora:33`](#fedora33)
-	[`fedora:34`](#fedora34)
-	[`fedora:35`](#fedora35)
-	[`fedora:latest`](#fedoralatest)
-	[`fedora:rawhide`](#fedorarawhide)

## `fedora:31`

```console
$ docker pull fedora@sha256:444773966064dcc3c268d8b496e76dbbbb49d16586d5a969c4082579e6b77616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:31` - linux; amd64

```console
$ docker pull fedora@sha256:cbe53d28f54c0f0b1d79a1817089235680b104c23619772473f449f20edd37dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61421612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e94ed77b448a8d2ff08b92d3ca743e4e862c744892d6886c73487581eb5863a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 17:59:37 GMT
ENV DISTTAG=f31container FGC=f31 FBR=f31
# Thu, 01 Apr 2021 17:59:42 GMT
ADD file:520f43cfa442b889bb527346a8884bee7826aa59eebf21a68fb40dc437997b24 in / 
# Thu, 01 Apr 2021 17:59:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:854946d575a439a894349addd141568875d7c1e673d3286b08250f3dde002e6a`  
		Last Modified: Fri, 10 Jul 2020 20:14:35 GMT  
		Size: 61.4 MB (61421612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:31` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:bdb7ca281096395c862f43b53fe1d1757de76bb50147b29b90555228a3346b0f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61326786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81935be5540146f7fcdcc4a62ba266867d7d110c5c47c0eca963521f0e67e252`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 22:43:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 30 Apr 2020 23:00:08 GMT
ENV DISTTAG=f31container FGC=f31 FBR=f31
# Fri, 10 Jul 2020 18:51:39 GMT
ADD file:fba344260301351defc3fe45ba9cdc9b780ac0f763c816fa16a386ff7e00f3f5 in / 
# Fri, 10 Jul 2020 18:51:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bb93aca2282a95f8f1f22679075e757bbdb6164204c8af34102864a5b077b7dc`  
		Last Modified: Fri, 10 Jul 2020 18:53:20 GMT  
		Size: 61.3 MB (61326786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:31` - linux; ppc64le

```console
$ docker pull fedora@sha256:50ab81a4619f7e94793aba65f3a40505bdfb9b59dcf6ae6deb8f974723e966d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66741144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22355ce265eba47eecdc70934857cf04e21c5448d13c46fdd16370c6e80f9b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 23:19:06 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 30 Apr 2020 23:38:07 GMT
ENV DISTTAG=f31container FGC=f31 FBR=f31
# Fri, 10 Jul 2020 20:10:43 GMT
ADD file:ffaa97b6a80c56e983576f2bbe88ecb69cc106c4b25a341db33093692a33ab2b in / 
# Fri, 10 Jul 2020 20:10:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3585d1ffff82f8bb34ca6dc4164ba7cd767aa3908177f2c2e636e085cf06f2a8`  
		Last Modified: Fri, 10 Jul 2020 20:11:56 GMT  
		Size: 66.7 MB (66741144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:31` - linux; s390x

```console
$ docker pull fedora@sha256:ed2978edeed403b54400c31280bfa04ecb4cded4d61cf7ce07eceebdd120a8ee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59020687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21d9c3ce449bffd91d868a34c35ce5d30341fc8fc210eccb1efca00f87cf6aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jan 2019 12:43:09 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 30 Apr 2020 22:42:41 GMT
ENV DISTTAG=f31container FGC=f31 FBR=f31
# Fri, 10 Jul 2020 18:41:47 GMT
ADD file:6a0f18efb0aa957642d30e5cb974e17ec968c93c3780e7546b1f3f931f819b11 in / 
# Fri, 10 Jul 2020 18:41:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:29e2a410611a2e285888b2860eb35ce80e55dfde9e1b62d97e8afe9f9ea7ba73`  
		Last Modified: Fri, 10 Jul 2020 18:42:54 GMT  
		Size: 59.0 MB (59020687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:32`

```console
$ docker pull fedora@sha256:614e5d660d422d3c6456d173c1a567724e501acffd91e28840c0a8fa397dbd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:32` - linux; amd64

```console
$ docker pull fedora@sha256:669bd31c9be91f8c744dc33bd68a82b4f9ea30632ae9668a7d2477b3279f979f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71093430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735e636ce47f10b5ec6ac1bc7c1eb1e82d7f49181524400f8f76470c874338f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 17:59:51 GMT
ENV DISTTAG=f32container FGC=f32 FBR=f32
# Thu, 01 Apr 2021 17:59:57 GMT
ADD file:ce86dc7a7dbb541532b7d2660ccebb4f3b37d4993c0abac542633ca0ccdc3f0f in / 
# Thu, 01 Apr 2021 17:59:58 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4ec705285520670639a7b6f34b5e5627bafa57b5b754e498c063e8372e34eb0a`  
		Last Modified: Thu, 18 Feb 2021 22:24:04 GMT  
		Size: 71.1 MB (71093430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:32` - linux; arm variant v7

```console
$ docker pull fedora@sha256:5d1c144ed9e01c79d6065ad4e0b95c556099cffd3b7888c1e19a6a22de779a9a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67029211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971921287306575cba046b41c6b727ea2a7f0e318dff24dc6a2e225509d522fc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Oct 2020 21:02:51 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 09 Oct 2020 21:02:51 GMT
ENV DISTTAG=f32container FGC=f32 FBR=f32
# Thu, 18 Feb 2021 23:04:58 GMT
ADD file:373963eeccc4c86310512745f0c21f874604b529799c43c50f4b8ba04cf1ce4d in / 
# Thu, 18 Feb 2021 23:05:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c6c79777a844cb7c389e338f06072692d5ac7829060ffc56af05587c4c3185be`  
		Last Modified: Thu, 18 Feb 2021 23:06:03 GMT  
		Size: 67.0 MB (67029211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:32` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:9117bd6e0d607c9b035c41028ef9ee43adbbeed6f1257594790ee2fdfe7c21ad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71201289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ab8c011d171dd5cfa27f7f523794fbe742d5850d76732ee07f6ee696612176`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 22:43:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 30 Apr 2020 23:00:50 GMT
ENV DISTTAG=f32container FGC=f32 FBR=f32
# Thu, 18 Feb 2021 22:52:05 GMT
ADD file:6bc97a7bfd2c7ac2e89685dc2f2fbba7926ec019bc5a14ca341f77a10731dfa2 in / 
# Thu, 18 Feb 2021 22:52:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e0941edc01100ecda9c79a2fc6934079bfc3db6aba7fdc7dfe02b46efbbe94ea`  
		Last Modified: Thu, 18 Feb 2021 22:53:54 GMT  
		Size: 71.2 MB (71201289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:32` - linux; ppc64le

```console
$ docker pull fedora@sha256:c56d84655705e9c20cda914c6ab9ccbc2752aadd48e115fbc0fef5a549ded44a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77922753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e655f2c9d0f3d752d7b43fa438cbefd9356f529d79f94a063548e4196f43ce37`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 23:19:06 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 30 Apr 2020 23:39:03 GMT
ENV DISTTAG=f32container FGC=f32 FBR=f32
# Thu, 18 Feb 2021 22:40:38 GMT
ADD file:ba57b647075872b696ee8c0b304dbd020d4846177921357dce8e3202be293701 in / 
# Thu, 18 Feb 2021 22:40:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c51914f769bde25ce0e9f7edf265e2153f8da463461f1b8d97a468164e3d7fc4`  
		Last Modified: Thu, 18 Feb 2021 22:41:59 GMT  
		Size: 77.9 MB (77922753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:32` - linux; s390x

```console
$ docker pull fedora@sha256:e6850738507d3fb9bd657871f340b1fce0a2677669e7a3f3f5e0eae423a66e21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73241794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67238c5a7d3ee6f5937b7bcf5e8d367c55475c29f278d1bc8f9632f94622d7e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jan 2019 12:43:09 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 30 Apr 2020 22:42:59 GMT
ENV DISTTAG=f32container FGC=f32 FBR=f32
# Thu, 18 Feb 2021 22:46:56 GMT
ADD file:1a42b46050b57e01a2c7d790568638148315af4f053844e507f0d4087a546bbd in / 
# Thu, 18 Feb 2021 22:47:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c7e987a5877050ff9df96f2cc385d142a56f9934335506f5c96d152ef2ca7cb4`  
		Last Modified: Thu, 18 Feb 2021 22:47:41 GMT  
		Size: 73.2 MB (73241794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:33`

```console
$ docker pull fedora@sha256:5404c1f9b87f10d8be6c955dba1bebef8b5302549bea23554df7df20802faba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:33` - linux; amd64

```console
$ docker pull fedora@sha256:59adce3a0634717a5a174f6771adb4809e48480f8d0085e4220d152412d47257
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61836994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26056ca25aff8c7c590918e53d38748b880a3f9fa96b386a472375cf66d73fd7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:00:06 GMT
ENV DISTTAG=f33container FGC=f33 FBR=f33
# Thu, 01 Apr 2021 18:00:11 GMT
ADD file:ec10d44a5fa5353fe3f3ba0b3344fa673a1773f4caf455fc023f5258190c0979 in / 
# Thu, 01 Apr 2021 18:00:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:588cf1704268314faec75366da728d1daf3472acc166b50ea6222e87dca9dae0`  
		Last Modified: Thu, 01 Apr 2021 18:01:44 GMT  
		Size: 61.8 MB (61836994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:33` - linux; arm variant v7

```console
$ docker pull fedora@sha256:6c705d7b407dc87a7ac88c2891e8f215eb75e130799b1b61d51e8bf5cb8061bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58415550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0592d0f612adb62167a6b116d7a7651e3feeff0d39af8084e1c462e35fc0c194`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Oct 2020 21:02:51 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 09 Oct 2020 21:03:25 GMT
ENV DISTTAG=f33container FGC=f33 FBR=f33
# Thu, 01 Apr 2021 18:02:49 GMT
ADD file:289f0d5d79201b3509fa0e24621c4dcc3cbdf3d9dc7a466f1a7a6914508bfc13 in / 
# Thu, 01 Apr 2021 18:02:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:32f2b5362df4af9190e5dd3a8303699b6b6260a37020caa8dac0c0815d8ab993`  
		Last Modified: Thu, 01 Apr 2021 18:04:07 GMT  
		Size: 58.4 MB (58415550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:33` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:a65d8f5d98f817eef18fcad46bc4a8e4df4ebeba0d1c513ea5f1b68145d15b0f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61841588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2cc1e871169fabdf597d2b3cbfb5e53e8ba511fcd3936a5dab39c7a25b5eb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 22:43:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 30 Apr 2020 23:01:35 GMT
ENV DISTTAG=f33container FGC=f33 FBR=f33
# Thu, 01 Apr 2021 18:07:11 GMT
ADD file:a126c15cc097e607032d533561f4e232f797ff460daf4f9509a1b2540e968e63 in / 
# Thu, 01 Apr 2021 18:07:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f0155ef3752058a07e4e64f7f2a92d18131bbe5e08293e8da25dc189941700f3`  
		Last Modified: Thu, 01 Apr 2021 18:08:27 GMT  
		Size: 61.8 MB (61841588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:33` - linux; ppc64le

```console
$ docker pull fedora@sha256:89301dcc9da5fc357301f53c0a8a76ec4988d34eb14f117f242704987e9e5800
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67503945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaec9e0c222fc3ef3e997bb87a649d1379884f0cb46e2b184f8a212df837d5c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 23:19:06 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 02 Oct 2020 22:39:42 GMT
ENV DISTTAG=f33container FGC=f33 FBR=f33
# Thu, 01 Apr 2021 18:18:21 GMT
ADD file:6fe7ead64318f1b76b7740dd0a1d95231ea627f71fc611045d0081826fb5f199 in / 
# Thu, 01 Apr 2021 18:18:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:49b37daab364c3b5b051378290822a04aa43388aa699aeeee608225b5b54a983`  
		Last Modified: Thu, 01 Apr 2021 18:19:47 GMT  
		Size: 67.5 MB (67503945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:33` - linux; s390x

```console
$ docker pull fedora@sha256:712f5e3449df38de78934893991f251c85fc7f07207fa893319ec4abf740f685
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63462667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9e2d1688ecea1c9a26f75f93a8d53b924c71283635bb3f17e37698cf396124`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jan 2019 12:43:09 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 08 Oct 2020 16:43:28 GMT
ENV DISTTAG=f33container FGC=f33 FBR=f33
# Thu, 01 Apr 2021 17:58:54 GMT
ADD file:a60f2b2fd034033c78f81c3d14a26b6ff8a4e865a11c6f9600c4781867e71d89 in / 
# Thu, 01 Apr 2021 17:59:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7b75c2e6acde898a79f176b77605e7e087392449b6563ebee997e1eeb38a08a4`  
		Last Modified: Thu, 01 Apr 2021 18:00:16 GMT  
		Size: 63.5 MB (63462667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:34`

```console
$ docker pull fedora@sha256:9d7b83b880f3d553d06c5feaab9c52b58df74828040af951162f1667c3b45850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:34` - linux; amd64

```console
$ docker pull fedora@sha256:e2daaac9dc4de3363bf541908f7a4ad156df7e94794fc515992619eae3eb2344
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64893948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c7cdc902fdd94e1838faff40aaa9a98c71fa9d112ea17004997bdb5f79cbe3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:00:19 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Thu, 01 Apr 2021 18:00:25 GMT
ADD file:42609d2e55bb4591441017ad1df4cea479f019292d593652f3aadec302282c42 in / 
# Thu, 01 Apr 2021 18:00:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:305d856848279583bd7b73605f155c93b3f6439e06442514857e26677d01a4fd`  
		Last Modified: Thu, 01 Apr 2021 18:02:13 GMT  
		Size: 64.9 MB (64893948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:34` - linux; arm variant v7

```console
$ docker pull fedora@sha256:47e831620e17b7af54cf922c4af4b1985d1116b546f332b6879955d8e4d8171d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61355628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e260351533cb24ee920b40610b985a4c2485447564c670790b89e8b3d5cb2aca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Oct 2020 21:02:51 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:03:11 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Thu, 01 Apr 2021 18:03:27 GMT
ADD file:3d3e379a1dbbb9095e642612e69180d230801a5e1bdbabe44c375441a4e97991 in / 
# Thu, 01 Apr 2021 18:03:30 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:52e418649bf3b6dd2781c3e59e543b374d3ce1f40bfdeb3c993936a80b1dbad4`  
		Last Modified: Thu, 01 Apr 2021 18:04:34 GMT  
		Size: 61.4 MB (61355628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:34` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:f443da75d6fb7c92e3970892eb58201ab9f6c5e3596481edc0c0366b0720ad96
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64812992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fddc501168d05e511d69030f54fba130dcafaf74738a912e4e488f8a985023e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 22:43:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 18 Feb 2021 22:52:42 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Thu, 01 Apr 2021 18:07:40 GMT
ADD file:f6eeee4dda3e6c226f8d50cdb87368b2691b896762d607d4966a8a446bf36f77 in / 
# Thu, 01 Apr 2021 18:07:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bc2eef35539164db693c994572d7a9cdf034047b16ab293f559a1931cd68b7d3`  
		Last Modified: Thu, 01 Apr 2021 18:08:53 GMT  
		Size: 64.8 MB (64812992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:34` - linux; ppc64le

```console
$ docker pull fedora@sha256:450bb3f8907e458e747b13d263d32248cbe5c4fdcb6324790d20374ce4493f0e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70774032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad543f6d298ef74320a4fc78a3eef8b5106f0119970d4199e83a7006e3066ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 23:19:06 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:18:48 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Thu, 01 Apr 2021 18:18:56 GMT
ADD file:106b34b0b5a237be60d72efdaf07bc1dfa30d1876b91eddb30417d6e3f217d66 in / 
# Thu, 01 Apr 2021 18:19:11 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5c8aed2cf7272e06bb00e41b670e3d74a5ae3dbbeef44c760c7b4e6bcee0cdad`  
		Last Modified: Thu, 01 Apr 2021 18:20:13 GMT  
		Size: 70.8 MB (70774032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:34` - linux; s390x

```console
$ docker pull fedora@sha256:084a1ec7f1115a5d94e5fd929ada140ad4cfd0be5e4405da2a6dfb792f70de46
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62592300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6549b70e03647786f6e2eee81399e13f222810cac267c1f66b7112c7e0f2b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jan 2019 12:43:09 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 17:59:16 GMT
ENV DISTTAG=f34container FGC=f34 FBR=f34
# Thu, 01 Apr 2021 17:59:30 GMT
ADD file:c35ba44972014403d28affe59c6b6734c283c7a388d73a92f20097859d19e9e5 in / 
# Thu, 01 Apr 2021 17:59:42 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ed52030f70f7ffb69d1c31130708786fc69883f953c48a03bf4a96ea89218005`  
		Last Modified: Thu, 01 Apr 2021 18:00:37 GMT  
		Size: 62.6 MB (62592300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:35`

```console
$ docker pull fedora@sha256:fc37c8d50964f07e209d3c1025df58cce03d5c9919db795589924bc4b16cf8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `fedora:35` - linux; amd64

```console
$ docker pull fedora@sha256:c230f8f601bffc2166d5923ac5dd83c7e331c3925a85ada4b7a5fe59146b3b69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64774359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28f3a8467eead3f9295637c7ec0539d1032e4de15b19a94d418c6f96b49ef05`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:00:32 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Thu, 01 Apr 2021 18:00:38 GMT
ADD file:6cbadecbb078f15f0df3cf49587b2b26c0a1c6b21710b54ccd09f48be0362c97 in / 
# Thu, 01 Apr 2021 18:00:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:de972ee947b83b0929bc384a239aa4f8d69ef801156dd1bd0ed2578a6a21ed14`  
		Last Modified: Thu, 18 Feb 2021 22:24:57 GMT  
		Size: 64.8 MB (64774359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:35` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:53505127f60d80b678137249786b54958a8b3637c44aa3bdd75302583a5dc59c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64754994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623a234e2fce9714c1781bc2469edd4599fd3415147e35b4b56873e5aa1e7863`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 22:43:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 25 Jan 2021 23:41:07 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Thu, 18 Feb 2021 22:53:14 GMT
ADD file:8604e55c9ded0b9d73ecbf93eb87488efc0550fb819a560a5bab97cfe496f30e in / 
# Thu, 18 Feb 2021 22:53:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8437404d345914967894d0a9b568d4c63fd2221346d1f0313ce6f21649c2bdd8`  
		Last Modified: Thu, 18 Feb 2021 22:55:02 GMT  
		Size: 64.8 MB (64754994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:latest`

```console
$ docker pull fedora@sha256:5404c1f9b87f10d8be6c955dba1bebef8b5302549bea23554df7df20802faba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:59adce3a0634717a5a174f6771adb4809e48480f8d0085e4220d152412d47257
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61836994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26056ca25aff8c7c590918e53d38748b880a3f9fa96b386a472375cf66d73fd7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:00:06 GMT
ENV DISTTAG=f33container FGC=f33 FBR=f33
# Thu, 01 Apr 2021 18:00:11 GMT
ADD file:ec10d44a5fa5353fe3f3ba0b3344fa673a1773f4caf455fc023f5258190c0979 in / 
# Thu, 01 Apr 2021 18:00:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:588cf1704268314faec75366da728d1daf3472acc166b50ea6222e87dca9dae0`  
		Last Modified: Thu, 01 Apr 2021 18:01:44 GMT  
		Size: 61.8 MB (61836994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm variant v7

```console
$ docker pull fedora@sha256:6c705d7b407dc87a7ac88c2891e8f215eb75e130799b1b61d51e8bf5cb8061bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.4 MB (58415550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0592d0f612adb62167a6b116d7a7651e3feeff0d39af8084e1c462e35fc0c194`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Oct 2020 21:02:51 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 09 Oct 2020 21:03:25 GMT
ENV DISTTAG=f33container FGC=f33 FBR=f33
# Thu, 01 Apr 2021 18:02:49 GMT
ADD file:289f0d5d79201b3509fa0e24621c4dcc3cbdf3d9dc7a466f1a7a6914508bfc13 in / 
# Thu, 01 Apr 2021 18:02:54 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:32f2b5362df4af9190e5dd3a8303699b6b6260a37020caa8dac0c0815d8ab993`  
		Last Modified: Thu, 01 Apr 2021 18:04:07 GMT  
		Size: 58.4 MB (58415550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:a65d8f5d98f817eef18fcad46bc4a8e4df4ebeba0d1c513ea5f1b68145d15b0f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61841588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2cc1e871169fabdf597d2b3cbfb5e53e8ba511fcd3936a5dab39c7a25b5eb8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 22:43:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 30 Apr 2020 23:01:35 GMT
ENV DISTTAG=f33container FGC=f33 FBR=f33
# Thu, 01 Apr 2021 18:07:11 GMT
ADD file:a126c15cc097e607032d533561f4e232f797ff460daf4f9509a1b2540e968e63 in / 
# Thu, 01 Apr 2021 18:07:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f0155ef3752058a07e4e64f7f2a92d18131bbe5e08293e8da25dc189941700f3`  
		Last Modified: Thu, 01 Apr 2021 18:08:27 GMT  
		Size: 61.8 MB (61841588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:89301dcc9da5fc357301f53c0a8a76ec4988d34eb14f117f242704987e9e5800
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67503945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaec9e0c222fc3ef3e997bb87a649d1379884f0cb46e2b184f8a212df837d5c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 23:19:06 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 02 Oct 2020 22:39:42 GMT
ENV DISTTAG=f33container FGC=f33 FBR=f33
# Thu, 01 Apr 2021 18:18:21 GMT
ADD file:6fe7ead64318f1b76b7740dd0a1d95231ea627f71fc611045d0081826fb5f199 in / 
# Thu, 01 Apr 2021 18:18:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:49b37daab364c3b5b051378290822a04aa43388aa699aeeee608225b5b54a983`  
		Last Modified: Thu, 01 Apr 2021 18:19:47 GMT  
		Size: 67.5 MB (67503945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:712f5e3449df38de78934893991f251c85fc7f07207fa893319ec4abf740f685
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63462667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9e2d1688ecea1c9a26f75f93a8d53b924c71283635bb3f17e37698cf396124`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jan 2019 12:43:09 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 08 Oct 2020 16:43:28 GMT
ENV DISTTAG=f33container FGC=f33 FBR=f33
# Thu, 01 Apr 2021 17:58:54 GMT
ADD file:a60f2b2fd034033c78f81c3d14a26b6ff8a4e865a11c6f9600c4781867e71d89 in / 
# Thu, 01 Apr 2021 17:59:06 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:7b75c2e6acde898a79f176b77605e7e087392449b6563ebee997e1eeb38a08a4`  
		Last Modified: Thu, 01 Apr 2021 18:00:16 GMT  
		Size: 63.5 MB (63462667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:rawhide`

```console
$ docker pull fedora@sha256:fc37c8d50964f07e209d3c1025df58cce03d5c9919db795589924bc4b16cf8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:c230f8f601bffc2166d5923ac5dd83c7e331c3925a85ada4b7a5fe59146b3b69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64774359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28f3a8467eead3f9295637c7ec0539d1032e4de15b19a94d418c6f96b49ef05`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 01 Apr 2021 18:00:32 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Thu, 01 Apr 2021 18:00:38 GMT
ADD file:6cbadecbb078f15f0df3cf49587b2b26c0a1c6b21710b54ccd09f48be0362c97 in / 
# Thu, 01 Apr 2021 18:00:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:de972ee947b83b0929bc384a239aa4f8d69ef801156dd1bd0ed2578a6a21ed14`  
		Last Modified: Thu, 18 Feb 2021 22:24:57 GMT  
		Size: 64.8 MB (64774359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:53505127f60d80b678137249786b54958a8b3637c44aa3bdd75302583a5dc59c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64754994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623a234e2fce9714c1781bc2469edd4599fd3415147e35b4b56873e5aa1e7863`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2019 22:43:26 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Mon, 25 Jan 2021 23:41:07 GMT
ENV DISTTAG=fRawhidecontainer FGC=fRawhide FBR=fRawhide
# Thu, 18 Feb 2021 22:53:14 GMT
ADD file:8604e55c9ded0b9d73ecbf93eb87488efc0550fb819a560a5bab97cfe496f30e in / 
# Thu, 18 Feb 2021 22:53:19 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8437404d345914967894d0a9b568d4c63fd2221346d1f0313ce6f21649c2bdd8`  
		Last Modified: Thu, 18 Feb 2021 22:55:02 GMT  
		Size: 64.8 MB (64754994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
