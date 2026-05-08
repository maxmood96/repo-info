## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:fa5bf9afb905a60e6989dd806b6ef3df281f43c4f9eac44cb1ad4afcd0b0ad4c
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:99d6a1d77bff1a8c4a2661bb2ab13ddb6f629a823d7ce6571c2a6c52524be262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48488901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1367db2200cf3725ce1cd56c71d7c5c5a04441374f1cdc9392c28d9a48b50f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:14:20 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cea8e2d498101741e0997c9bb7af8e717c95bf506b8197e93832e075d261fb4`  
		Last Modified: Fri, 08 May 2026 19:14:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9274f94d448ef3c49a43877159e04a2b3a1219a3e2494addd864ea818a089415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80112f14475bb0bc519f04adaec308387d336fa90577f7376e5ea67b878d8640`

```dockerfile
```

-	Layers:
	-	`sha256:bd51f3f26da0125d6713ce0fd2dc68227d2f37e91753eef08e0375c4e131a6d1`  
		Last Modified: Fri, 08 May 2026 19:14:27 GMT  
		Size: 3.7 MB (3734074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd255594357da9651cdde35afb0f45a3a0f5f4a270a023f4ef58fb94399a146c`  
		Last Modified: Fri, 08 May 2026 19:14:26 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:a20344c905ce3217fd9837a2d97375fee49de6f5c9c77c3c9e108bda25beb479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe375daf5a1ac59a40865de7b72e71e46a61c3d260071674e4cf489975c399d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:25:19 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ec18a0651074f3ac740b1a061140a88c16cce1b8118aeae02a5868a4ebdd3ef3`  
		Last Modified: Fri, 08 May 2026 18:33:05 GMT  
		Size: 46.0 MB (46021587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d187ac8ef03858b044d67b07a5818db92dbeb93217a7c4fa4583962ca3a6879`  
		Last Modified: Fri, 08 May 2026 20:25:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5361bf5d18f720692e676121e62308c67583bf2a32878a9293aacefaba3a883a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abcee55700881e5473f541bd8b17f505bb794482912a8759b26c7154336533e4`

```dockerfile
```

-	Layers:
	-	`sha256:b86877060f87500382545f215e4fcd02b69d2f8165b1f197bfdbe32ec9c39351`  
		Last Modified: Fri, 08 May 2026 20:25:26 GMT  
		Size: 3.7 MB (3734275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71dbf378458b5030794944541af6d7ef7b5f71d48597f8ba630a3684317cd9c9`  
		Last Modified: Fri, 08 May 2026 20:25:25 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b2518885f846a3f19dae4588c132f5a94812f7e54339f49f669513ea087d5536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44207919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4261e9db699871b695d14c0cf11935a8f21098d8c35a0cd3db8ff755ce8546f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:14:21 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aab124eb444f8b3c492659015779ec3a06bae852e3f58c2ac53134d16169148`  
		Last Modified: Fri, 08 May 2026 19:14:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ea3b0fcb4ebeb0c0bdbd140d8311371f27c5c07887df4b1f869a3506d98ed73f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2506c67d0a6c2d5486b03eaae7cb7d988ff3a292f99ca867687a495540e75b3`

```dockerfile
```

-	Layers:
	-	`sha256:b1523c212b312f1255a8dfca7694b5bce0b59800a36fc4d809cb4b982c7255c4`  
		Last Modified: Fri, 08 May 2026 19:14:28 GMT  
		Size: 3.7 MB (3736253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed1a3d3af786279c5446e2a1ef69e100018e9e623f71bb7642221ad5e487c04`  
		Last Modified: Fri, 08 May 2026 19:14:28 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:937c6b2dcc45cfa0a6d2b7a1059ccbf7404f1cfdf36bde6e84d41d2deddbadad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf3b3fa2f70b8089865e63160bbcdfb398da45085fb30970b542ee0439b4ba6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:14:18 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc93258f7b8afca5cf3d10687366c3720a3c1e4be520323c5729d5885ca9953a`  
		Last Modified: Fri, 08 May 2026 19:14:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2bbeae0ee49dd721870e83cc3eeaec2d1ce5ef3a4302f2412c8ce08f65e42e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3511ecdc5029ae77193b4b644d4896ca56b3d44cdbab54846cf947ff90832c1`

```dockerfile
```

-	Layers:
	-	`sha256:5c539f9c163170ed072aeb728dddcdf9afebfe42c538f817085fb23bd7ea47c6`  
		Last Modified: Fri, 08 May 2026 19:14:25 GMT  
		Size: 3.7 MB (3734289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42b924cce35d832f6da2e479a16ec63502d930cdc90b0975fcd105f4081b604`  
		Last Modified: Fri, 08 May 2026 19:14:24 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:38216be7d0be1ee4c7d67ec70e7a79cc29cfb99f586d488df59b2040171cbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52cc1ca3305b38f5d11452e5868407907a92934994ee2d7954ff492c8b13ae4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:14:40 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafa9d1ee6276e34b7c198f6178c2614c1cb3114dcb35a00fdb9bed1c8a80082`  
		Last Modified: Fri, 08 May 2026 19:14:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:595eaf5b9b640930d3aad4c8a7dba3397823fed24b440a3f0b94da9e82ba6dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88aed6b9009f26c72fed11c422451d6084256eb3079e3a291a421183f717f7bf`

```dockerfile
```

-	Layers:
	-	`sha256:60e3269c3e0d465ec1d4eba3d1ca914b1abd2b8f36600f31e412a9c7905bdacf`  
		Last Modified: Fri, 08 May 2026 19:14:47 GMT  
		Size: 3.7 MB (3731270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35d323e9ae340f4449917914d4ad0df0228e2be5fce25aa52332e208bec9f7ea`  
		Last Modified: Fri, 08 May 2026 19:14:47 GMT  
		Size: 5.8 KB (5787 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:6e7f95b2b664bce7c3f4639413b352de88746e87ff164d3a2a0cef3a2ea96c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48782739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52680c1a4a4a16414509494a1301a7f533bcae3ce64fcb56f55dc3497da0125`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:14:13 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:08baa8fe1f531703c14c631b772a987ffc44ae832951ae77c2cf756cd9309b97`  
		Last Modified: Fri, 08 May 2026 18:19:35 GMT  
		Size: 48.8 MB (48782513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36704f77658acd30bd7e5a54d551f7f0996ddf866dcf55d9ae246360b944611d`  
		Last Modified: Fri, 08 May 2026 19:14:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:39031c439dac56a4b1f0bbcb0b054f4874e2acbbf3314c233c514996cba9c5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76acc529ee8b76620f011011f6cf16ad676d64d58aba6af759860388162d1034`

```dockerfile
```

-	Layers:
	-	`sha256:4dfeab2b67792179fbe9c8f8647104ed1e739320b038969ffb193432ca51c12c`  
		Last Modified: Fri, 08 May 2026 19:14:29 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f5fe5728f90110d77fd3b7be0ffd7ef76ab46d83361593cbca3cd49097cf2149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52337012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dafb475aadff29bf1dc6a4775690568da6436d8000d19738f3f97d3ea37cb6d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:18:28 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12246a762b7f24bd0c7aaf1da1e882f4c765db07f56ad030977a9a4c89a080ff`  
		Last Modified: Fri, 08 May 2026 20:18:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:efaafd357a587ce6e5462ca047f96b1c95378f3965a760656da6cefec3fac32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457778342d6b47f1e765d69bd70f6e1de0976e282bad4510d933c548a0ff049d`

```dockerfile
```

-	Layers:
	-	`sha256:f9ebcd9975f5d401ca26420a022cc66342a9b95dd68f12f56784627355998952`  
		Last Modified: Fri, 08 May 2026 20:18:46 GMT  
		Size: 3.7 MB (3738432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bccc79c115d5ca48d5cd7297ccf10b7912ff04bd0679ab617203fcd10c62cd98`  
		Last Modified: Fri, 08 May 2026 20:18:46 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:67a52da98317012b5153d3ba0a2482afa39e263d1e93a0a0df0e2ef3499eaa2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47148249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed00d01b5635ea02972389e4f27637bf25e1fc8e8f33fd8edb3ec97fc8cfdcf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:13:43 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5553f1f0b5d326b13650593c90a35bb63e6c7590b5387f349af4cbd50de4f`  
		Last Modified: Fri, 08 May 2026 19:13:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8d96960e6860c8ad933036f4fd0c993e6ae826bbc292c64d92a717267e541738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e632a89e0f7cd2dd003c1abdbe4a412bd7bfe74cdcf6c44ba35173ac1d04f9`

```dockerfile
```

-	Layers:
	-	`sha256:1703292f52c4e5a9e9a2953f4a39cad685ce04ba1a2d81a451d87daf5400bfc5`  
		Last Modified: Fri, 08 May 2026 19:13:54 GMT  
		Size: 3.7 MB (3730912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e50fa8f9678e62dfa4a17aac1510186f9ac583737223e7c4735fadcdab218207`  
		Last Modified: Fri, 08 May 2026 19:13:54 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json
