## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:dcaeea42624cf9207f4296137c93a4db4c864310f25192496aed1edc7262422b
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
$ docker pull debian@sha256:de9c4f0eecd33fa2a116d75fd4148810a5c5d9c0bcb1eb5500bd17e2b975cbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48481713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e790aa65146ec560dd27dbd4b469218063e5c07fcfb5423f98e6f23384fd02`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1769990400'
# Tue, 03 Feb 2026 02:15:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:df15f195ee0d72d279cc46eb774ad62d104e474d9facef01b531175464baf2e4`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 48.5 MB (48481489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdf7eac074414506d83e54d6b565929f710cd5bfbf92fe4ae3c864887591f24`  
		Last Modified: Tue, 03 Feb 2026 02:16:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ced732ecccaaf892a0ac51c6fa9b9a364bcbf4550587f168ee30223ecaada939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3aa0bdde514b21d35ba8bf377c36c22e7e52bb7c152bfc0db08a337001387c`

```dockerfile
```

-	Layers:
	-	`sha256:3bed4c5ab203889178224d21351dc66d9abbbf1fba19684b172a4c71832cb0ca`  
		Last Modified: Tue, 03 Feb 2026 02:16:06 GMT  
		Size: 3.7 MB (3734076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ffa892f2f290f12dbc09283554ce5b1398ba6c9d49be2d87d8a347444536d00`  
		Last Modified: Tue, 03 Feb 2026 02:16:06 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9fa251c744a2d644485404a514a67f9b06a943dadd217ec93993d0185cc08abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46016892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1ead86511898834166c950562d66f7c22a315e90436b9f508bcfb8fa8e727b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1769990400'
# Tue, 03 Feb 2026 02:14:55 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6b8d9d8da429c22ece8e9db14e33c70ba99ef6b87849675c5402b6b3162de82b`  
		Last Modified: Tue, 03 Feb 2026 01:13:53 GMT  
		Size: 46.0 MB (46016666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f4ea4ae4dc25fd01129caf44a86163a5b6181fc8e3fd63d63772a9cf536252`  
		Last Modified: Tue, 03 Feb 2026 02:15:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2f0d0498da433edc0bccf70cda525837e7cfd421b506affccf916049828475b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef107ed0beb268cfba72061254fedc7f1288bc13ddd389c7b36b2cf8c98985d`

```dockerfile
```

-	Layers:
	-	`sha256:108a50f7ea40809be831fc9cd887c1995c682232dc41e14ea838e7bc71dc4e86`  
		Last Modified: Tue, 03 Feb 2026 02:15:02 GMT  
		Size: 3.7 MB (3734277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7ef8f4d55427b036dbfb0f3a695d3c3ed355b1278753f5f6e3a8c569fe096d`  
		Last Modified: Tue, 03 Feb 2026 02:15:02 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:17:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:16 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:16:50 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.5 MB (49468598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee065a829ca498ef1b9610bde6374fb370e066cc5417d843b8260bcaa26b1106`  
		Last Modified: Tue, 13 Jan 2026 01:18:00 GMT  
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
		Last Modified: Tue, 13 Jan 2026 01:18:00 GMT  
		Size: 3.7 MB (3731272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49dc6c9745682523b04708288d99fe00c0e1b0c515777d82edf79a72afbd463c`  
		Last Modified: Tue, 13 Jan 2026 01:18:00 GMT  
		Size: 5.8 KB (5792 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ac18cf7a35c623486745ed01888534ee9e66451ea2e4835b5aefa3c3c9f9d24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48763485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581a5ad84a200abcba403af47e338d0a3c5f83db29bf9891036ebd301eea3850`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1769990400'
# Tue, 03 Feb 2026 02:16:15 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:35c59722c959fd9d60a7dfb5956b0e344c5d40af352101814fa06b50da5b1f7c`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 48.8 MB (48763261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6233612c79facabd1d044bbe97739b953353205a79dd6ae3ba1e88511c30cc9`  
		Last Modified: Tue, 03 Feb 2026 02:16:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c789cba0dee6477af4c5eab6636256a9ae2021d67ea8d7cbf4136e04c5f999dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435e03eb2814cf8fee6168dead4d84c3addaab6fd0ddd3ab0ddb89b5ca1e89eb`

```dockerfile
```

-	Layers:
	-	`sha256:42345c0ee9a00209568d8f1ef34dd77884cf5f90cd43ffe4aff86641a0a18b8d`  
		Last Modified: Tue, 03 Feb 2026 02:16:33 GMT  
		Size: 5.6 KB (5633 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:082705accb72b45b6ef7ea9c6f1535463ea74fbb086e892ee657bcb8746c7b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78715193065dee45fe1f07c694c802cc298070aa64edda1467516f7ac252d760`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1769990400'
# Tue, 03 Feb 2026 02:14:48 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fa322c9888557dceee3004049315081e51d7742c7dcbe992cf4823c89612553a`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 52.3 MB (52327290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784df06bfd2f6fe56d97682505082deecae85beaf6a58bb9b9b7f16f80494022`  
		Last Modified: Tue, 03 Feb 2026 02:15:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:94b688a5b3eadd169111c2cab1affe0853e18306d4f0eec704772b1eff28e6cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7234ce1e1b0a4198480a139afa579b59edd8358c36b6f090ec35c0dbc6b266ae`

```dockerfile
```

-	Layers:
	-	`sha256:abab25158618602644a443a43da1e180c35654dc617f57862f6c366b2182bd8b`  
		Last Modified: Tue, 03 Feb 2026 02:15:03 GMT  
		Size: 3.7 MB (3738434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52cf2dd993fe5d240de6008c7f3e3917c12532a899539beeba95ffe30c759d27`  
		Last Modified: Tue, 03 Feb 2026 02:15:02 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:bc48c7f51ce3c9c168145343aa7e0a4f6f593f6d0016a150a6c752eab11b8236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47138571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8ebaf149a744e86c9c29bafc63048fe8828b485ab89a9513d4ac457d26ddb0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1769990400'
# Tue, 03 Feb 2026 02:15:19 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a59a0aca3d5f7f5181deb3b3393bd059b96d8154e5eecb729404a2a46d13ec67`  
		Last Modified: Tue, 03 Feb 2026 01:13:16 GMT  
		Size: 47.1 MB (47138347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce9eb69440571fb6cac45ffd72db23b62b40b36598a2ebb35508e75ab2e5d3`  
		Last Modified: Tue, 03 Feb 2026 02:15:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a8906e7fa3d75195952d0452fb5c24be6003f863b62ddab9b0542370b4fb7ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314b9e32e47099dd4e68a2c290d17e48e2570bc3a57dc0f69a7117db22040a3`

```dockerfile
```

-	Layers:
	-	`sha256:99c88ea01725bf98c383381431a51110cc39029b0cd0575c0c52c7004b28fff0`  
		Last Modified: Tue, 03 Feb 2026 02:15:29 GMT  
		Size: 3.7 MB (3730914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc83c3edf286707ea7a570ce42da67d43fb56416fcd2b7535bb39ee1d3e295e`  
		Last Modified: Tue, 03 Feb 2026 02:15:29 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json
