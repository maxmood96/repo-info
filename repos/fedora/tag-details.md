<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fedora`

-	[`fedora:39`](#fedora39)
-	[`fedora:40`](#fedora40)
-	[`fedora:41`](#fedora41)
-	[`fedora:latest`](#fedoralatest)
-	[`fedora:rawhide`](#fedorarawhide)

## `fedora:39`

```console
$ docker pull fedora@sha256:e3a65f75c3be76349557e99bbb6da4f358d1a9c7378cadfb16e7823df6ddba7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fedora:39` - linux; amd64

```console
$ docker pull fedora@sha256:7091dd8cf5989c5037d171e86271deabd666c4d2afd4c8bc24b37a2cea437e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64807226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b04a7d633ed558a29a4224c4fe4d7bf064b7d1afd642323d4b5868dabdbfe78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 10:38:48 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sun, 21 Jul 2024 10:38:48 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Sun, 21 Jul 2024 10:38:48 GMT
ADD fedora-39-x86_64.tar.xz / # buildkit
# Sun, 21 Jul 2024 10:38:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f5752d20f619cb7038bc2c6944238eed3cd82936d6524e72ed7d35fff857f35c`  
		Last Modified: Tue, 23 Jul 2024 18:14:11 GMT  
		Size: 64.8 MB (64807226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:39` - unknown; unknown

```console
$ docker pull fedora@sha256:c1597d9b4adb90c18e7e5e87f1e6fafa0c5f659c508309df9a25dec6804068c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4391293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bbc56bc9a3115c88e5019197521a6f0453e2243b4a1a7f94afa82dd478e0a07`

```dockerfile
```

-	Layers:
	-	`sha256:3d30d5b6686f76e85e9592d613cb72a2d10e7a6800c5b5152c225826c106f61b`  
		Last Modified: Tue, 23 Jul 2024 18:14:10 GMT  
		Size: 4.4 MB (4386367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f832ed48c053985d7019dd1dcf042a8d1a4f90093feb9a47c4a83b9e098d8878`  
		Last Modified: Tue, 23 Jul 2024 18:14:10 GMT  
		Size: 4.9 KB (4926 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:39` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:6b5bdc7faeaacfdc72ae1e6d7f49459196a7bba3d2518dbd102aa613e946cdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63462513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835eb6335e57db4d072bd833a431a7ebf8a651b5757ff6774edd7bab0b94238a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 10:38:48 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sun, 21 Jul 2024 10:38:48 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Sun, 21 Jul 2024 10:38:48 GMT
ADD fedora-39-aarch64.tar.xz / # buildkit
# Sun, 21 Jul 2024 10:38:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:af75d0684bbc67a857141a41625ae073bc353959d2e1f8601cca64c7322b515c`  
		Last Modified: Wed, 24 Jul 2024 12:27:34 GMT  
		Size: 63.5 MB (63462513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:39` - unknown; unknown

```console
$ docker pull fedora@sha256:495059e3034b57e96c9bf01cded550797639585dc88367a8dd094ce67c4cd5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4391410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b1762d757bd22c26befc74a1ccc83e2ab9b7bbb5fb0179af51ff3643ad0618`

```dockerfile
```

-	Layers:
	-	`sha256:4c0e355f75b3a5a3a2a13815ed264c6d25b2d60e89b95346393b5306f153fe19`  
		Last Modified: Wed, 24 Jul 2024 12:27:32 GMT  
		Size: 4.4 MB (4386454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f44a6a09e328230c88d91c5427760e9ff67b719ddb04a2fb9fb65de7c8663a94`  
		Last Modified: Wed, 24 Jul 2024 12:27:32 GMT  
		Size: 5.0 KB (4956 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:39` - linux; ppc64le

```console
$ docker pull fedora@sha256:f0504e385108811ec3b80c4499a05fbc24e0e047196366d05e7946f1cdcf150f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71519453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8ef5507b26f6c3155edc354873b82acba96998a134f0335bcf3abfc9f2af61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 10:38:48 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sun, 21 Jul 2024 10:38:48 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Sun, 21 Jul 2024 10:38:48 GMT
ADD fedora-39-ppc64le.tar.xz / # buildkit
# Sun, 21 Jul 2024 10:38:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:9888bdb508a0c92249f9072ac2558ae2ec6aa8f5992dc938164c34a216b6bcff`  
		Last Modified: Wed, 24 Jul 2024 13:30:30 GMT  
		Size: 71.5 MB (71519453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:39` - unknown; unknown

```console
$ docker pull fedora@sha256:85a3b4889e40f87eef54e092cb976034824757a29b7af866e472dc85a2945df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4391046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d96085dc710c2ac1574236e0775a7a63ad5fe61376c84b9761055cca7ccc79`

```dockerfile
```

-	Layers:
	-	`sha256:6526d9bd5bed34755cbe16100bfcb354fdaf8a6223cc7bf758b9e74959684430`  
		Last Modified: Wed, 24 Jul 2024 13:30:27 GMT  
		Size: 4.4 MB (4386102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:695af6dad656814ae1a9e07373a9351c6b588050d222537032e9ff1069dcd324`  
		Last Modified: Wed, 24 Jul 2024 13:30:27 GMT  
		Size: 4.9 KB (4944 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:39` - linux; s390x

```console
$ docker pull fedora@sha256:2a5d0366e4d6be2d36bca4932c613e209168b1abf56a1a83e27850a288a50d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65341516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abeb404a8377fb508be99d6bb34cb3e1260057e277e2366647277e130d3c1123`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 10:38:48 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sun, 21 Jul 2024 10:38:48 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Sun, 21 Jul 2024 10:38:48 GMT
ADD fedora-39-s390x.tar.xz / # buildkit
# Sun, 21 Jul 2024 10:38:48 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3516cb4dd51bf103919dba081128eb9c2ef101d7266828f120c6186b8514be92`  
		Last Modified: Wed, 24 Jul 2024 13:27:03 GMT  
		Size: 65.3 MB (65341516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:39` - unknown; unknown

```console
$ docker pull fedora@sha256:7930bbf26e0b554466928ce1e9aec6517c7cbed726659312195c627e5bf15ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4393725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada1a3229c7f179e9f34ed51a5041723b4250d41626891833ebb3f6b6183b940`

```dockerfile
```

-	Layers:
	-	`sha256:1420fba81e4ac2d26ae767584238e99faacc202445f1d944a56307fd5b3f8e50`  
		Last Modified: Wed, 24 Jul 2024 13:27:01 GMT  
		Size: 4.4 MB (4388803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cc404e44792840405b6948d88d4ad69fa89187a7165245badd745e85ed1b68f`  
		Last Modified: Wed, 24 Jul 2024 13:27:00 GMT  
		Size: 4.9 KB (4922 bytes)  
		MIME: application/vnd.in-toto+json

## `fedora:40`

```console
$ docker pull fedora@sha256:5ce8497aeea599bf6b54ab3979133923d82aaa4f6ca5ced1812611b197c79eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:40` - linux; amd64

```console
$ docker pull fedora@sha256:a0f4dffd30e0af6e53f57533e79a9e32699d37d8e850132ff89f612d6ea8a300
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80116543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e22da79803c567fceb0e255f1168977259525a4279cb518016a60df025412fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 14 Sep 2023 19:20:17 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Mon, 22 Apr 2024 18:26:20 GMT
ADD file:b8701dca3d7c8dad1562d860440cbee7d19ac10a972b8b2ecb836d955c12fce0 in / 
# Mon, 22 Apr 2024 18:26:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d4df0db66c89d7e6225ce9d3597a045fb95c020f3174af1830df88a37a871db8`  
		Last Modified: Mon, 22 Apr 2024 18:27:27 GMT  
		Size: 80.1 MB (80116543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:40` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:79c6d37cfa65044246e2b7a42e6ac47a71b498c6aaf79ef18ce27b8f1912b1c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79367012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d6fb7e34f429aff9b43a21cb73fa4dbae594ba953bd9fce4ac032a52560e66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 14 Sep 2023 18:40:13 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Mon, 22 Apr 2024 17:40:15 GMT
ADD file:1bf0fdbfbbeb01d9eed9abaaae9674d9776bdb82bd19adc6749241584eae7668 in / 
# Mon, 22 Apr 2024 17:40:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3a7f8330e54b855763da0bc8407ecf81fc62c1dd60505d287531b3137e8d45a8`  
		Last Modified: Mon, 22 Apr 2024 17:41:17 GMT  
		Size: 79.4 MB (79367012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:40` - linux; ppc64le

```console
$ docker pull fedora@sha256:3bd68d5cf17209e3ee142f0b325457a8cb36d2c645c56edff275a28f1822ebc2
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86748745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dde3801e1a2b233149f6aa0cefdf423c8db012ab2ef5b3f9e4cc37d1153ffaa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 14 Sep 2023 19:17:58 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Mon, 22 Apr 2024 18:18:02 GMT
ADD file:bc29a9c4ea3f33c947b886891a3a008e4c32558ed870a0af1301f6c723d78f42 in / 
# Mon, 22 Apr 2024 18:18:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca03069c79e714b54f3c8d35d880f6c70e1462a5fcbd1257b8b059bcef8666e2`  
		Last Modified: Mon, 22 Apr 2024 18:19:24 GMT  
		Size: 86.7 MB (86748745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:40` - linux; s390x

```console
$ docker pull fedora@sha256:f03c7cf07596858ed3f5259faf4b3ecb03a0b4f8561e0ae4a6989c9daee6645c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80560778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4cc45e8b0d3371024e117f507f15fd896d7bb8b1683966a2d8c8d79654f60b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 14 Sep 2023 18:43:30 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Mon, 22 Apr 2024 18:37:47 GMT
ADD file:1dedf8c8a5496e0291db116514bf3c1daad0e9c9706e7dcd29445ad1c47f462e in / 
# Mon, 22 Apr 2024 18:37:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8e0e2cf8122e81a375029bd920b323662954badada0f75595d794ea168d36102`  
		Last Modified: Mon, 22 Apr 2024 18:43:00 GMT  
		Size: 80.6 MB (80560778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:41`

```console
$ docker pull fedora@sha256:3cc404e4736e4c73b234798f6941b4de70ea98087989a3c718d5f6303682447a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fedora:41` - linux; amd64

```console
$ docker pull fedora@sha256:815d788d6610a41d9ed4e1aeb1fed52fc4937a55253be144786f932c01cd45df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57008946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8e1899837eb991c4986bd6bff797b0cdf2e3f7983cda7babccd1e386d361d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jul 2024 11:54:28 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 23 Jul 2024 11:54:28 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Tue, 23 Jul 2024 11:54:28 GMT
ADD layer.tar / # buildkit
# Tue, 23 Jul 2024 11:54:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c5d449bd8afb0471f0a9c3fdd80dda5029dc6021fcc87259be582e783e8ccea`  
		Last Modified: Tue, 23 Jul 2024 18:14:54 GMT  
		Size: 57.0 MB (57008946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:41` - unknown; unknown

```console
$ docker pull fedora@sha256:05f8d8eb6266896728867e1309b82a485990e5018e0c6900e8e5d8b0615e2225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2833970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c358b4bbd8ec156234b40001c1dedf43793d31b46a615092da26086640edfba6`

```dockerfile
```

-	Layers:
	-	`sha256:77fa5dcbefc7de69b4f363046535c317b653c5b3d80bd5a1487ea7c36629d7b3`  
		Last Modified: Tue, 23 Jul 2024 18:14:52 GMT  
		Size: 2.8 MB (2828722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c0586fd13e7be32c0a74c44a0e334c841287e4bbf70dc004c58005e387ff7d`  
		Last Modified: Tue, 23 Jul 2024 18:14:51 GMT  
		Size: 5.2 KB (5248 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:41` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:c608bbfc5ba43610c778540f5677670c929be80b3b7c587a44505eb29f16ab99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55712215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27bf0e0b7219bfa1d41318c4b4d062f0579ffd44b4573fe7d7360a49da419012`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jul 2024 11:54:28 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 23 Jul 2024 11:54:28 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Tue, 23 Jul 2024 11:54:28 GMT
ADD layer.tar / # buildkit
# Tue, 23 Jul 2024 11:54:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0b4d50dc6ddf14e649e789a7c32a9b9c860b37c38fa9a70817e98a683b321474`  
		Last Modified: Wed, 24 Jul 2024 12:29:08 GMT  
		Size: 55.7 MB (55712215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:41` - unknown; unknown

```console
$ docker pull fedora@sha256:e9bcbf3d37261a75f37ecba189743754ff338a0c4fa3be9aaf35f1d28bbe55e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2834042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4d52612b3088cd7d4ecaa5641158d3c4f1e4368dfbcb18bc2031d897a3b6e0`

```dockerfile
```

-	Layers:
	-	`sha256:c20949e312eff729320e6c462f4bfcaf5c2035fee1eaa6b2511f6f2bf4291f4e`  
		Last Modified: Wed, 24 Jul 2024 12:29:07 GMT  
		Size: 2.8 MB (2828752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c16dbdb99d8425131ee4c06025cf28a5e435904998effe360f78603fe74f85`  
		Last Modified: Wed, 24 Jul 2024 12:29:06 GMT  
		Size: 5.3 KB (5290 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:41` - linux; ppc64le

```console
$ docker pull fedora@sha256:cacd3cbbf2a0afd3f537c9cb3b373eba9ca3a6354541504db15315450c5fb299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62746064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1ae2156fc435885078cd6c3b3dbd261b823ea34f7e245c84ef8a2a660c1196`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jul 2024 11:54:28 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 23 Jul 2024 11:54:28 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Tue, 23 Jul 2024 11:54:28 GMT
ADD layer.tar / # buildkit
# Tue, 23 Jul 2024 11:54:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0ed061ec47f98f640d710b647830bfbb59564ce7989461ebb7cb847460a8bd1d`  
		Last Modified: Wed, 24 Jul 2024 13:31:15 GMT  
		Size: 62.7 MB (62746064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:41` - unknown; unknown

```console
$ docker pull fedora@sha256:35bb606a8bb58cd70cc83e85f618637bee00d5bb7a0240bee5f7657e0a24dcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2834643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71616ed39e27a6afde51cbc26b89c510c7cfc4947fb43432d806ee4aabd9c6a`

```dockerfile
```

-	Layers:
	-	`sha256:5f03b9d051186478f61e5012d2e187454fb977a2dffbe2e5899fd684ed66e5c1`  
		Last Modified: Wed, 24 Jul 2024 13:31:13 GMT  
		Size: 2.8 MB (2829372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e41c6bbc873b78f12a09bc36afad4fc432aa61cee4f68d2bd9324fd577aa353`  
		Last Modified: Wed, 24 Jul 2024 13:31:13 GMT  
		Size: 5.3 KB (5271 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:41` - linux; s390x

```console
$ docker pull fedora@sha256:d7736eeda1cff1eb8b3aa19e39bf78e1aec260690f4a98935afb62126e43280f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57833656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fb48f289c832ac650da38f7f6c991e25c927eb9c8d9ed006398228cccf725c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jul 2024 11:54:28 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 23 Jul 2024 11:54:28 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Tue, 23 Jul 2024 11:54:28 GMT
ADD layer.tar / # buildkit
# Tue, 23 Jul 2024 11:54:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:35030d3a4d6447278fbad23fb1c30d67340a6d9e4128617b3f5a2ad6f33558b9`  
		Last Modified: Wed, 24 Jul 2024 13:29:53 GMT  
		Size: 57.8 MB (57833656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:41` - unknown; unknown

```console
$ docker pull fedora@sha256:ae2208e12132224e1b05026974453e4ec615f36f9c603ea678d7955a40abf949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2836472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0e74808e77057cfb78091162bfac4e42d7648e1f9ffd6b85703d14f9bb5739`

```dockerfile
```

-	Layers:
	-	`sha256:aa461b3cfdf7819b921fb2cbc7f1e034f2a0cb6a7734d2d13ec02a9c91b43502`  
		Last Modified: Wed, 24 Jul 2024 13:29:52 GMT  
		Size: 2.8 MB (2831227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68184a2f2188249e84c8d6dda6db72a8abff4c6bf177b81708f07c61cecf5e12`  
		Last Modified: Wed, 24 Jul 2024 13:29:52 GMT  
		Size: 5.2 KB (5245 bytes)  
		MIME: application/vnd.in-toto+json

## `fedora:latest`

```console
$ docker pull fedora@sha256:5ce8497aeea599bf6b54ab3979133923d82aaa4f6ca5ced1812611b197c79eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `fedora:latest` - linux; amd64

```console
$ docker pull fedora@sha256:a0f4dffd30e0af6e53f57533e79a9e32699d37d8e850132ff89f612d6ea8a300
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80116543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e22da79803c567fceb0e255f1168977259525a4279cb518016a60df025412fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Apr 2021 17:59:37 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 14 Sep 2023 19:20:17 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Mon, 22 Apr 2024 18:26:20 GMT
ADD file:b8701dca3d7c8dad1562d860440cbee7d19ac10a972b8b2ecb836d955c12fce0 in / 
# Mon, 22 Apr 2024 18:26:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d4df0db66c89d7e6225ce9d3597a045fb95c020f3174af1830df88a37a871db8`  
		Last Modified: Mon, 22 Apr 2024 18:27:27 GMT  
		Size: 80.1 MB (80116543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:79c6d37cfa65044246e2b7a42e6ac47a71b498c6aaf79ef18ce27b8f1912b1c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79367012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d6fb7e34f429aff9b43a21cb73fa4dbae594ba953bd9fce4ac032a52560e66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Nov 2022 19:58:13 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 14 Sep 2023 18:40:13 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Mon, 22 Apr 2024 17:40:15 GMT
ADD file:1bf0fdbfbbeb01d9eed9abaaae9674d9776bdb82bd19adc6749241584eae7668 in / 
# Mon, 22 Apr 2024 17:40:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3a7f8330e54b855763da0bc8407ecf81fc62c1dd60505d287531b3137e8d45a8`  
		Last Modified: Mon, 22 Apr 2024 17:41:17 GMT  
		Size: 79.4 MB (79367012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; ppc64le

```console
$ docker pull fedora@sha256:3bd68d5cf17209e3ee142f0b325457a8cb36d2c645c56edff275a28f1822ebc2
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86748745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dde3801e1a2b233149f6aa0cefdf423c8db012ab2ef5b3f9e4cc37d1153ffaa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 12:16:45 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 14 Sep 2023 19:17:58 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Mon, 22 Apr 2024 18:18:02 GMT
ADD file:bc29a9c4ea3f33c947b886891a3a008e4c32558ed870a0af1301f6c723d78f42 in / 
# Mon, 22 Apr 2024 18:18:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ca03069c79e714b54f3c8d35d880f6c70e1462a5fcbd1257b8b059bcef8666e2`  
		Last Modified: Mon, 22 Apr 2024 18:19:24 GMT  
		Size: 86.7 MB (86748745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `fedora:latest` - linux; s390x

```console
$ docker pull fedora@sha256:f03c7cf07596858ed3f5259faf4b3ecb03a0b4f8561e0ae4a6989c9daee6645c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80560778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4cc45e8b0d3371024e117f507f15fd896d7bb8b1683966a2d8c8d79654f60b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Jul 2021 02:30:24 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 14 Sep 2023 18:43:30 GMT
ENV DISTTAG=f40container FGC=f40 FBR=f40
# Mon, 22 Apr 2024 18:37:47 GMT
ADD file:1dedf8c8a5496e0291db116514bf3c1daad0e9c9706e7dcd29445ad1c47f462e in / 
# Mon, 22 Apr 2024 18:37:52 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8e0e2cf8122e81a375029bd920b323662954badada0f75595d794ea168d36102`  
		Last Modified: Mon, 22 Apr 2024 18:43:00 GMT  
		Size: 80.6 MB (80560778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fedora:rawhide`

```console
$ docker pull fedora@sha256:3cc404e4736e4c73b234798f6941b4de70ea98087989a3c718d5f6303682447a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fedora:rawhide` - linux; amd64

```console
$ docker pull fedora@sha256:815d788d6610a41d9ed4e1aeb1fed52fc4937a55253be144786f932c01cd45df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57008946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8e1899837eb991c4986bd6bff797b0cdf2e3f7983cda7babccd1e386d361d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jul 2024 11:54:28 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 23 Jul 2024 11:54:28 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Tue, 23 Jul 2024 11:54:28 GMT
ADD layer.tar / # buildkit
# Tue, 23 Jul 2024 11:54:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6c5d449bd8afb0471f0a9c3fdd80dda5029dc6021fcc87259be582e783e8ccea`  
		Last Modified: Tue, 23 Jul 2024 18:14:54 GMT  
		Size: 57.0 MB (57008946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:rawhide` - unknown; unknown

```console
$ docker pull fedora@sha256:05f8d8eb6266896728867e1309b82a485990e5018e0c6900e8e5d8b0615e2225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2833970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c358b4bbd8ec156234b40001c1dedf43793d31b46a615092da26086640edfba6`

```dockerfile
```

-	Layers:
	-	`sha256:77fa5dcbefc7de69b4f363046535c317b653c5b3d80bd5a1487ea7c36629d7b3`  
		Last Modified: Tue, 23 Jul 2024 18:14:52 GMT  
		Size: 2.8 MB (2828722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c0586fd13e7be32c0a74c44a0e334c841287e4bbf70dc004c58005e387ff7d`  
		Last Modified: Tue, 23 Jul 2024 18:14:51 GMT  
		Size: 5.2 KB (5248 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:rawhide` - linux; arm64 variant v8

```console
$ docker pull fedora@sha256:c608bbfc5ba43610c778540f5677670c929be80b3b7c587a44505eb29f16ab99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55712215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27bf0e0b7219bfa1d41318c4b4d062f0579ffd44b4573fe7d7360a49da419012`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jul 2024 11:54:28 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 23 Jul 2024 11:54:28 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Tue, 23 Jul 2024 11:54:28 GMT
ADD layer.tar / # buildkit
# Tue, 23 Jul 2024 11:54:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0b4d50dc6ddf14e649e789a7c32a9b9c860b37c38fa9a70817e98a683b321474`  
		Last Modified: Wed, 24 Jul 2024 12:29:08 GMT  
		Size: 55.7 MB (55712215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:rawhide` - unknown; unknown

```console
$ docker pull fedora@sha256:e9bcbf3d37261a75f37ecba189743754ff338a0c4fa3be9aaf35f1d28bbe55e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2834042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4d52612b3088cd7d4ecaa5641158d3c4f1e4368dfbcb18bc2031d897a3b6e0`

```dockerfile
```

-	Layers:
	-	`sha256:c20949e312eff729320e6c462f4bfcaf5c2035fee1eaa6b2511f6f2bf4291f4e`  
		Last Modified: Wed, 24 Jul 2024 12:29:07 GMT  
		Size: 2.8 MB (2828752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c16dbdb99d8425131ee4c06025cf28a5e435904998effe360f78603fe74f85`  
		Last Modified: Wed, 24 Jul 2024 12:29:06 GMT  
		Size: 5.3 KB (5290 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:rawhide` - linux; ppc64le

```console
$ docker pull fedora@sha256:cacd3cbbf2a0afd3f537c9cb3b373eba9ca3a6354541504db15315450c5fb299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62746064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1ae2156fc435885078cd6c3b3dbd261b823ea34f7e245c84ef8a2a660c1196`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jul 2024 11:54:28 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 23 Jul 2024 11:54:28 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Tue, 23 Jul 2024 11:54:28 GMT
ADD layer.tar / # buildkit
# Tue, 23 Jul 2024 11:54:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0ed061ec47f98f640d710b647830bfbb59564ce7989461ebb7cb847460a8bd1d`  
		Last Modified: Wed, 24 Jul 2024 13:31:15 GMT  
		Size: 62.7 MB (62746064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:rawhide` - unknown; unknown

```console
$ docker pull fedora@sha256:35bb606a8bb58cd70cc83e85f618637bee00d5bb7a0240bee5f7657e0a24dcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2834643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71616ed39e27a6afde51cbc26b89c510c7cfc4947fb43432d806ee4aabd9c6a`

```dockerfile
```

-	Layers:
	-	`sha256:5f03b9d051186478f61e5012d2e187454fb977a2dffbe2e5899fd684ed66e5c1`  
		Last Modified: Wed, 24 Jul 2024 13:31:13 GMT  
		Size: 2.8 MB (2829372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e41c6bbc873b78f12a09bc36afad4fc432aa61cee4f68d2bd9324fd577aa353`  
		Last Modified: Wed, 24 Jul 2024 13:31:13 GMT  
		Size: 5.3 KB (5271 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:rawhide` - linux; s390x

```console
$ docker pull fedora@sha256:d7736eeda1cff1eb8b3aa19e39bf78e1aec260690f4a98935afb62126e43280f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57833656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fb48f289c832ac650da38f7f6c991e25c927eb9c8d9ed006398228cccf725c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Jul 2024 11:54:28 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Tue, 23 Jul 2024 11:54:28 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Tue, 23 Jul 2024 11:54:28 GMT
ADD layer.tar / # buildkit
# Tue, 23 Jul 2024 11:54:28 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:35030d3a4d6447278fbad23fb1c30d67340a6d9e4128617b3f5a2ad6f33558b9`  
		Last Modified: Wed, 24 Jul 2024 13:29:53 GMT  
		Size: 57.8 MB (57833656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:rawhide` - unknown; unknown

```console
$ docker pull fedora@sha256:ae2208e12132224e1b05026974453e4ec615f36f9c603ea678d7955a40abf949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2836472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0e74808e77057cfb78091162bfac4e42d7648e1f9ffd6b85703d14f9bb5739`

```dockerfile
```

-	Layers:
	-	`sha256:aa461b3cfdf7819b921fb2cbc7f1e034f2a0cb6a7734d2d13ec02a9c91b43502`  
		Last Modified: Wed, 24 Jul 2024 13:29:52 GMT  
		Size: 2.8 MB (2831227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68184a2f2188249e84c8d6dda6db72a8abff4c6bf177b81708f07c61cecf5e12`  
		Last Modified: Wed, 24 Jul 2024 13:29:52 GMT  
		Size: 5.2 KB (5245 bytes)  
		MIME: application/vnd.in-toto+json
