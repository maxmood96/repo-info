<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fedora`

-	[`fedora:39`](#fedora39)
-	[`fedora:40`](#fedora40)
-	[`fedora:41`](#fedora41)
-	[`fedora:latest`](#fedoralatest)
-	[`fedora:rawhide`](#fedorarawhide)

## `fedora:39`

```console
$ docker pull fedora@sha256:120705e07485dcd2b0c6de1d99a0829bdfe14b315b42c2caf8fe6c26bc5910e1
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
$ docker pull fedora@sha256:a7c928bb94d3fb7d370baaff39dd5b477158dd82a741e8c39837ea32acc49b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63453434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e48bcd01fa5d26fd65d7fd592b7d2984c9cbb61d6d595be0f6c1f8ad0aee20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jul 2024 12:52:53 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 12 Jul 2024 12:52:53 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Fri, 12 Jul 2024 12:52:53 GMT
ADD fedora-39-aarch64.tar.xz / # buildkit
# Fri, 12 Jul 2024 12:52:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:593a94da3c36a0b6fcdd0fe3b3a0f429685e739d01894caa1ba84ca25afb0083`  
		Last Modified: Fri, 12 Jul 2024 18:57:50 GMT  
		Size: 63.5 MB (63453434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:39` - unknown; unknown

```console
$ docker pull fedora@sha256:ae53406e829649e1c8eb91558f21f6dd4f29c5c650110c583833360ebacacd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4367392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0488373a2ce389fb13d46ce8bda9e70d26c092f2989e94ffbad75e184f8f3f8`

```dockerfile
```

-	Layers:
	-	`sha256:653a385124343785b83be9a90ae9937b5ac67e95e0559144d51fbeda3e0e4392`  
		Last Modified: Fri, 12 Jul 2024 18:57:48 GMT  
		Size: 4.4 MB (4362436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9034eea9eeabc2fd538803c6c7bfb7daf7042773e6ac944d15b5b471b29e54d2`  
		Last Modified: Fri, 12 Jul 2024 18:57:48 GMT  
		Size: 5.0 KB (4956 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:39` - linux; ppc64le

```console
$ docker pull fedora@sha256:00d4bca022932d366a81802e1ba35c84d5c009beee8c277e73d4a9d43aacbc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71526585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e5474ff44f4cdade6fbcbcc6f9a176287908de3cadfda1a239c330816864cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jul 2024 12:52:53 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 12 Jul 2024 12:52:53 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Fri, 12 Jul 2024 12:52:53 GMT
ADD fedora-39-ppc64le.tar.xz / # buildkit
# Fri, 12 Jul 2024 12:52:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3e323e7ed2fd9520bb93c70d6f80dd865a4c24d3dd41aab50ccaabfe66be604c`  
		Last Modified: Fri, 12 Jul 2024 21:23:54 GMT  
		Size: 71.5 MB (71526585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:39` - unknown; unknown

```console
$ docker pull fedora@sha256:f047eb5ef68459e1abbc7369b1b80043cd4fcf465063a3f1c967614d26464840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4367028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3114f4f3f4708b8be31cb5ddda5e69c2e86a492f028a791d5777e111b78679`

```dockerfile
```

-	Layers:
	-	`sha256:5bccb529f9274472098fd90012afbbe2b830fb81b87cc4f9684ee0eadb9f83a0`  
		Last Modified: Fri, 12 Jul 2024 21:23:52 GMT  
		Size: 4.4 MB (4362084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c07faba5bce0cf94f8e3260893480e333c5f99de39d137353cf090d7a649d55`  
		Last Modified: Fri, 12 Jul 2024 21:23:51 GMT  
		Size: 4.9 KB (4944 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:39` - linux; s390x

```console
$ docker pull fedora@sha256:e48461f39a82bc751ededc668dd5d978ffbad2d78b9ec18202e1fdc48eb3ceac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65334643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2679d8c7c9306e99348657dbe12a1fb5c02b64a18eb7e15dbc9bb51808ada3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jul 2024 12:52:53 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 12 Jul 2024 12:52:53 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Fri, 12 Jul 2024 12:52:53 GMT
ADD fedora-39-s390x.tar.xz / # buildkit
# Fri, 12 Jul 2024 12:52:53 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:28cc3475d52ae8f11edd485b27aee9f3e72cbd9b6f21fcc3c29db58ea67a6ab9`  
		Last Modified: Fri, 12 Jul 2024 18:57:59 GMT  
		Size: 65.3 MB (65334643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:39` - unknown; unknown

```console
$ docker pull fedora@sha256:57297d570dce8f3fd94a531deb389650b62742eeec1e3ad471f71dfa7e4431bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4369705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1316a4ecc7e10254beb91608cacc2d801ce2a9331d68c1821c04685ead90e931`

```dockerfile
```

-	Layers:
	-	`sha256:823d91334a7387c17f854eddf59df919631c6ce4e8d6d314cde8f41948d34ef4`  
		Last Modified: Fri, 12 Jul 2024 18:57:59 GMT  
		Size: 4.4 MB (4364785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5749de950aee165989d89b1c1cdf0f9eab61dc3c8511ce5fa5ebc64f06e492d`  
		Last Modified: Fri, 12 Jul 2024 18:57:58 GMT  
		Size: 4.9 KB (4920 bytes)  
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
$ docker pull fedora@sha256:892b63610a0901710c3fcdd28d11e4a54c85308ef6ee137208be4278ab03b472
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
$ docker pull fedora@sha256:5e5decf541b5a79b480c2750d8c3d50469fd3c0943507f24448c28575411a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55812525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a239af25fdfe7aa7a01afc794f3019990d8abb63e37312d1b3d6e97f7026c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jul 2024 12:51:07 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 12 Jul 2024 12:51:07 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Fri, 12 Jul 2024 12:51:07 GMT
ADD layer.tar / # buildkit
# Fri, 12 Jul 2024 12:51:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e568fdafa1951dedc95ae460922f024bdb34d26b24ee4bdd2b93fc7dafe9d13e`  
		Last Modified: Fri, 12 Jul 2024 18:59:18 GMT  
		Size: 55.8 MB (55812525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:41` - unknown; unknown

```console
$ docker pull fedora@sha256:1afed9164588d5de81afbdaa6f287e6962a2c1c784c23fa9f35337297ffe36cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2817283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a405d24bb444b172e98b97fece438f90d7151c3e315b42897f9511350aec7cc`

```dockerfile
```

-	Layers:
	-	`sha256:0fa357fdd5089a0bf9ab24744cf89d2f63ecee7f1c6ff85a019a22e4e0c40a21`  
		Last Modified: Fri, 12 Jul 2024 18:59:17 GMT  
		Size: 2.8 MB (2811993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d25547ee88ff382520a5f4691e551a9c733eddcda202f9a2ee6f5d855b05f028`  
		Last Modified: Fri, 12 Jul 2024 18:59:16 GMT  
		Size: 5.3 KB (5290 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:41` - linux; ppc64le

```console
$ docker pull fedora@sha256:193c219added61d7a9333a348e2fcd0574d5dd21f78489b42cdb11d0b72a6f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62777587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ef29e3b9c97a08088a2a89205201ba6a5d35a7dd1c0e3d4ddfa1cfd1f6048c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jul 2024 12:51:07 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 12 Jul 2024 12:51:07 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Fri, 12 Jul 2024 12:51:07 GMT
ADD layer.tar / # buildkit
# Fri, 12 Jul 2024 12:51:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:81f0ac86d448a0a23fda0c0c331cda32bcb9b8a02897ad3a79d03adb74ab381a`  
		Last Modified: Fri, 12 Jul 2024 21:25:26 GMT  
		Size: 62.8 MB (62777587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:41` - unknown; unknown

```console
$ docker pull fedora@sha256:23335655dd066fd3c0c2723551bee713fffeb0caa5651485cbe4cf49e07b9769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2817884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3b33cf0167dddfcdef8c5ff66ec713d8428e033a9c534cb0ccbf25a92762cc`

```dockerfile
```

-	Layers:
	-	`sha256:0e6ed2f3663cc5c78efb5626b73c120375d80809e2ba21db35af03fbedda6798`  
		Last Modified: Fri, 12 Jul 2024 21:25:24 GMT  
		Size: 2.8 MB (2812613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf6d330d66e42121ff286dca6d45e1870daa13f8460fbe093109d3e89394920`  
		Last Modified: Fri, 12 Jul 2024 21:25:24 GMT  
		Size: 5.3 KB (5271 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:41` - linux; s390x

```console
$ docker pull fedora@sha256:c15a1499fbed1e88f38d79f1756e9c7e7066029ea11ad9a6a0359fa5c982884f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57861251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234cf128241d808c743082c148af416f356fc11406c92d73d5692576a58a53ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jul 2024 12:51:07 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 12 Jul 2024 12:51:07 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Fri, 12 Jul 2024 12:51:07 GMT
ADD layer.tar / # buildkit
# Fri, 12 Jul 2024 12:51:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:11629c4761dc30206b7b1b8885993b7af1905ee72a0e164efd9c9e253b609821`  
		Last Modified: Fri, 12 Jul 2024 19:00:23 GMT  
		Size: 57.9 MB (57861251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:41` - unknown; unknown

```console
$ docker pull fedora@sha256:39e9c022e1c2cd33840ea8484a3db3a42e708916d95f824cf4656ccf16cfc578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2819712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44c10142d2d25cd0b031912849368244bb030177712e063fd23bcf9af9ae074`

```dockerfile
```

-	Layers:
	-	`sha256:27474315146825f37b376466162761a79205a69e00d05577e608707ee2e86c50`  
		Last Modified: Fri, 12 Jul 2024 19:00:22 GMT  
		Size: 2.8 MB (2814468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e770c7bf980544a6a5e1f76162b21039aa022ed741637288e08e49d818d00e90`  
		Last Modified: Fri, 12 Jul 2024 19:00:22 GMT  
		Size: 5.2 KB (5244 bytes)  
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
$ docker pull fedora@sha256:892b63610a0901710c3fcdd28d11e4a54c85308ef6ee137208be4278ab03b472
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
$ docker pull fedora@sha256:5e5decf541b5a79b480c2750d8c3d50469fd3c0943507f24448c28575411a6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55812525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a239af25fdfe7aa7a01afc794f3019990d8abb63e37312d1b3d6e97f7026c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jul 2024 12:51:07 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 12 Jul 2024 12:51:07 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Fri, 12 Jul 2024 12:51:07 GMT
ADD layer.tar / # buildkit
# Fri, 12 Jul 2024 12:51:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e568fdafa1951dedc95ae460922f024bdb34d26b24ee4bdd2b93fc7dafe9d13e`  
		Last Modified: Fri, 12 Jul 2024 18:59:18 GMT  
		Size: 55.8 MB (55812525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:rawhide` - unknown; unknown

```console
$ docker pull fedora@sha256:1afed9164588d5de81afbdaa6f287e6962a2c1c784c23fa9f35337297ffe36cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2817283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a405d24bb444b172e98b97fece438f90d7151c3e315b42897f9511350aec7cc`

```dockerfile
```

-	Layers:
	-	`sha256:0fa357fdd5089a0bf9ab24744cf89d2f63ecee7f1c6ff85a019a22e4e0c40a21`  
		Last Modified: Fri, 12 Jul 2024 18:59:17 GMT  
		Size: 2.8 MB (2811993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d25547ee88ff382520a5f4691e551a9c733eddcda202f9a2ee6f5d855b05f028`  
		Last Modified: Fri, 12 Jul 2024 18:59:16 GMT  
		Size: 5.3 KB (5290 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:rawhide` - linux; ppc64le

```console
$ docker pull fedora@sha256:193c219added61d7a9333a348e2fcd0574d5dd21f78489b42cdb11d0b72a6f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62777587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ef29e3b9c97a08088a2a89205201ba6a5d35a7dd1c0e3d4ddfa1cfd1f6048c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jul 2024 12:51:07 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 12 Jul 2024 12:51:07 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Fri, 12 Jul 2024 12:51:07 GMT
ADD layer.tar / # buildkit
# Fri, 12 Jul 2024 12:51:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:81f0ac86d448a0a23fda0c0c331cda32bcb9b8a02897ad3a79d03adb74ab381a`  
		Last Modified: Fri, 12 Jul 2024 21:25:26 GMT  
		Size: 62.8 MB (62777587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:rawhide` - unknown; unknown

```console
$ docker pull fedora@sha256:23335655dd066fd3c0c2723551bee713fffeb0caa5651485cbe4cf49e07b9769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2817884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3b33cf0167dddfcdef8c5ff66ec713d8428e033a9c534cb0ccbf25a92762cc`

```dockerfile
```

-	Layers:
	-	`sha256:0e6ed2f3663cc5c78efb5626b73c120375d80809e2ba21db35af03fbedda6798`  
		Last Modified: Fri, 12 Jul 2024 21:25:24 GMT  
		Size: 2.8 MB (2812613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf6d330d66e42121ff286dca6d45e1870daa13f8460fbe093109d3e89394920`  
		Last Modified: Fri, 12 Jul 2024 21:25:24 GMT  
		Size: 5.3 KB (5271 bytes)  
		MIME: application/vnd.in-toto+json

### `fedora:rawhide` - linux; s390x

```console
$ docker pull fedora@sha256:c15a1499fbed1e88f38d79f1756e9c7e7066029ea11ad9a6a0359fa5c982884f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57861251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234cf128241d808c743082c148af416f356fc11406c92d73d5692576a58a53ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jul 2024 12:51:07 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Fri, 12 Jul 2024 12:51:07 GMT
ENV DISTTAG=rawhidecontainer FGC=rawhide FBR=rawhide
# Fri, 12 Jul 2024 12:51:07 GMT
ADD layer.tar / # buildkit
# Fri, 12 Jul 2024 12:51:07 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:11629c4761dc30206b7b1b8885993b7af1905ee72a0e164efd9c9e253b609821`  
		Last Modified: Fri, 12 Jul 2024 19:00:23 GMT  
		Size: 57.9 MB (57861251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fedora:rawhide` - unknown; unknown

```console
$ docker pull fedora@sha256:39e9c022e1c2cd33840ea8484a3db3a42e708916d95f824cf4656ccf16cfc578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2819712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44c10142d2d25cd0b031912849368244bb030177712e063fd23bcf9af9ae074`

```dockerfile
```

-	Layers:
	-	`sha256:27474315146825f37b376466162761a79205a69e00d05577e608707ee2e86c50`  
		Last Modified: Fri, 12 Jul 2024 19:00:22 GMT  
		Size: 2.8 MB (2814468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e770c7bf980544a6a5e1f76162b21039aa022ed741637288e08e49d818d00e90`  
		Last Modified: Fri, 12 Jul 2024 19:00:22 GMT  
		Size: 5.2 KB (5244 bytes)  
		MIME: application/vnd.in-toto+json
