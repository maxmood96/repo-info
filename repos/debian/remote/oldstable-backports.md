## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:321d2e4f9ed47691fab7e79622baf0b11b0d5bce081588d9a93e8a428b59966a
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:99ba24b03d7fc931431bc66154d6503861286d341cff0e8d60b5fbf287ea410e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48481850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f16e1068e157ecfe2a8b88bbeff257be0e1500f37546470e8ce3d991b50c77a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1768176000'
# Tue, 13 Jan 2026 01:16:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fce45e5821dc17513ed6cf9cbefc0f704ba7d14484ecf14cecc4bf83fc34ef28`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 48.5 MB (48481626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7dc1de323ab0b4c0cafabc38580f90883bca1d794de036365439aa7df71098`  
		Last Modified: Tue, 13 Jan 2026 01:16:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e5885033cbbf0af68d9edc9f8b87254659095acccb52a8df821bb5c1ef8c3ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7b949e5262287ee35850222771e6fc82c1c98e9b0d3f831b3d7c1c8e3a1a81`

```dockerfile
```

-	Layers:
	-	`sha256:c0bf7d1febbed3af43d98af0892383f286af4594877dcc214a4e9856558c6d79`  
		Last Modified: Tue, 13 Jan 2026 04:25:59 GMT  
		Size: 3.7 MB (3734076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb2049fcb86e065a0298bf4d622a149d0f7b05d3c3c3c1bef6359d059843a80`  
		Last Modified: Tue, 13 Jan 2026 01:16:32 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:54e0413d7e36543ad5a87f9f5a298e5d6ea2ad26e564c18e652e56f64b54cb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f8b28ea77421f76d233ecb682708aae1b420da3dc78ec685af597d621f2c17`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1768176000'
# Tue, 13 Jan 2026 01:17:28 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5c014182d2fc0a5fbca43930d07924878df2a39dc6ebce3c5a8dd7e290aa6bbd`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 46.0 MB (46016736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016bb3f9982c1a5a487ca5095e92d22788672a2d2e9825139fd27dbb6db8cd93`  
		Last Modified: Tue, 13 Jan 2026 01:17:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2c7c549165144b9e66d78873756f279f3cf599dfcc5b2b112523716fd37bf06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d8c56b9d886087d63457598d1158f20c709338029de1e7f7fa5a292ba84dd2`

```dockerfile
```

-	Layers:
	-	`sha256:949f49cdd0cf71afb94448a7e26cfb5262b25562eb488d5619ca7f06472781bd`  
		Last Modified: Tue, 13 Jan 2026 04:26:06 GMT  
		Size: 3.7 MB (3734277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39fc3f5b72d00ecccd7b720fa0921126d46515b790abf2a46349c6e71df4450f`  
		Last Modified: Tue, 13 Jan 2026 04:26:06 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8a0ed47f7e44424d6454de2d937040379c62a34d3eb1c87665e9b81c6c7b536a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44199071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a5788e0c78471d2f794ab389e5efdd8fe96138bb8566ab51ab2c9bdb014493`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1768176000'
# Tue, 13 Jan 2026 01:17:42 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cd4360f563a94d2a4f62a21d09c0e3b252ec14e6770c48551c91fa8584dc3919`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 44.2 MB (44198848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea1d95489ac337c234a26c0b4c7951d0f61f4049cc345a74a12f7e46b6d91c2`  
		Last Modified: Tue, 13 Jan 2026 01:17:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6f1426898c2d753219f4cbab9e961205a0a2343980d09e3f7fe27e0d58680383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4af0d06cbd9b3031a03b15e289c136374824f0a78a409203efd20437a0b351`

```dockerfile
```

-	Layers:
	-	`sha256:9138f2557effff79f469fa8594c4caed68703513ca4898c8e37d531691e9ae8c`  
		Last Modified: Tue, 13 Jan 2026 04:26:11 GMT  
		Size: 3.7 MB (3736255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025ce74fd597d593bb2bea57ad230ad0982df3552615166d5bdad89e7f8e1a83`  
		Last Modified: Tue, 13 Jan 2026 01:17:49 GMT  
		Size: 5.9 KB (5865 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:73e0e0980060855681c5efe6517e8eede52013b83b8b240819c1afd5dedca88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48366301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca83cf1ebe63380645ac196ec9f63d44665560ba9f6980de1cccf0e7ea2e8740`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1768176000'
# Tue, 13 Jan 2026 01:16:42 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7dd34bf0047563585f014485c722e527ba1225cd1cde42a1738c49a0d8d30e33`  
		Last Modified: Tue, 13 Jan 2026 00:42:26 GMT  
		Size: 48.4 MB (48366078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abd50781a480ac41f4b51b559fbbab7bb5a48e84c8dcbdce06c2bd32541c2e8`  
		Last Modified: Tue, 13 Jan 2026 01:16:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f63f63b789c906a9f87073d41fd02825ef0b01a55af29275d3d0a056634b8933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9db11a9b5863445bb37490828e5bbfef26971c523f71a28951faaf524459e9`

```dockerfile
```

-	Layers:
	-	`sha256:eeeddc61dca569c4dad59e882aa0b0c8d9f182b42c2e23575f4489294c271ab9`  
		Last Modified: Tue, 13 Jan 2026 04:26:17 GMT  
		Size: 3.7 MB (3734291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2de70ecb0da10228403824dc616890ebd5d346c967edb84b1c127e2006ae4eee`  
		Last Modified: Tue, 13 Jan 2026 01:16:50 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:514b8c0876596ebb5a8b40c84e0f0bacba3f30bf4c59d1772297f2200620e064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49468820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282b7b149ee84d30303fcff62d51ffa094f36fb50075f1c7fe22d54ca9ad98d1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1768176000'
# Tue, 13 Jan 2026 01:17:53 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:34f2da61a92312228a079e4890e2f87f3bf41282b013012e46280926284d0277`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.5 MB (49468598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee065a829ca498ef1b9610bde6374fb370e066cc5417d843b8260bcaa26b1106`  
		Last Modified: Tue, 13 Jan 2026 01:18:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:36e7bd7578ef4e832707a627c2098f575b1db361b759285185540429f9570bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d11babd57ef94c9c227827e158b3ac8e7e341c02df614821c57b4a798665d3`

```dockerfile
```

-	Layers:
	-	`sha256:b376343642ff537e1af4f148202109a390f4d5207fad43b5e763606af55cfdee`  
		Last Modified: Tue, 13 Jan 2026 04:26:27 GMT  
		Size: 3.7 MB (3731272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49dc6c9745682523b04708288d99fe00c0e1b0c515777d82edf79a72afbd463c`  
		Last Modified: Tue, 13 Jan 2026 01:18:00 GMT  
		Size: 5.8 KB (5792 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:93a519bd67e74a6026af2f446802296b2dbca3b23ea0b765d79a30082a0d574b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48763622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f13e84a4a0cfac3a44855f77d3d97e3fac404a45340bbce634d4d85c45d1258`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1768176000'
# Tue, 13 Jan 2026 01:17:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6385efd5b11b0d78dffd93f900a434e79f0b28b381f523c771743d3be958c697`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.8 MB (48763395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf663c50fd20ce2afde586432ff1bddad1e5647874814049fd85b8475e2e884f`  
		Last Modified: Tue, 13 Jan 2026 01:17:22 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a40413610302ef6b4486d475a3131de106512eaad928951f61c3296ed120a36b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57fec39fc0db2dcb4d500fc53a715f3783c6b08682d13142e36ca0d13bdc2076`

```dockerfile
```

-	Layers:
	-	`sha256:3a7cb22bfc227dabd18dba5d8c51cac57fc83d87a27f5b01829c32049383cd16`  
		Last Modified: Tue, 13 Jan 2026 01:17:18 GMT  
		Size: 5.6 KB (5634 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:31aa7280cbc2060a3e4b8d49e2672ef380501084ff204176b52e7a1bbbb09215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd81d38d60a980b7d0a8db58a661e3dbc765103a2c26c041b3a8473d01324bf3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1768176000'
# Tue, 13 Jan 2026 01:15:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:acbff0350edd4f7a2f4b02fab643f6c14766672385b6eb92360cd7f44bb7917d`  
		Last Modified: Tue, 13 Jan 2026 00:41:16 GMT  
		Size: 52.3 MB (52327386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948b6a3f67bc6cf668ae6c29e018b868b66f43c7b5c090ea9d6aca7d2f9e7dd9`  
		Last Modified: Tue, 13 Jan 2026 01:15:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a0fbfeaa64acbee9443d5e6d7354e5065865682642f12cc788725fa6e8c692ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc218c8001d05c7c5adfefd5f15d31e725b0cdf95aec69b865a549a83bd2ffd`

```dockerfile
```

-	Layers:
	-	`sha256:83681db39f839712dd10e8adc603d476fd21c199332aad0d30125c8f701bd0ef`  
		Last Modified: Tue, 13 Jan 2026 01:15:34 GMT  
		Size: 3.7 MB (3738434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:430a4fecf792fe5dd7a0966b4fc144ec6712d50451ec4624c8affc88e5692abf`  
		Last Modified: Tue, 13 Jan 2026 01:15:34 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:c3fa323cb9bba0c1b1d3d4c96c77a88e3bf042d9e780e4092e2ef6f78b0feaa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47138661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:286ee4fa1443fe411e753ea1939a7fbb55df82cd1c88f8a9c92c800e2a3cd823`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1768176000'
# Tue, 13 Jan 2026 05:15:23 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b4cca2e808922f7da7d247bded72c17e4d56296527a6c545404fa2b91469163f`  
		Last Modified: Tue, 13 Jan 2026 04:22:20 GMT  
		Size: 47.1 MB (47138436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2202bbdf08b29a8113be8cb803aac4042c6dcedb80bd4d7bce5a3db7d0cbacb`  
		Last Modified: Tue, 13 Jan 2026 05:15:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f338d19c6d314806d66ee44be780cc3e00ca660ec2fc561d15c9e1ed4cd40811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c03a699a18b7b56811327f8679b2874ae8f303f446357d99f209e610a61499`

```dockerfile
```

-	Layers:
	-	`sha256:0f9ed133fb8fc593171d0af6b1e97a96314ad5dd12bf23471920372662f24e7e`  
		Last Modified: Tue, 13 Jan 2026 05:15:35 GMT  
		Size: 3.7 MB (3730914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f21068474bdd6c4c8169181094eeb7a4a12dc5b790784252cbd5d03b610dc24`  
		Last Modified: Tue, 13 Jan 2026 05:15:35 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json
