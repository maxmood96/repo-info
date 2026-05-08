## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:86f7b802afda41d3bf053c0d42bc1f7298bc777fa09b322698aeda3f1c51b732
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
$ docker pull debian@sha256:e9f7dd4649eb486c995fb4a104b7e00026fdb32a284ba54a8ba5a38b611dd46b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48488904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cb6e386ed6bc5e9fb1079abca5c51a645f4db44736b0194c0b6e083aa7fbe9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1777939200'
# Fri, 08 May 2026 19:14:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:645b1e3697c46ac1e254d802f0463fdfe3d401378090d9816699799c21d205f5`  
		Last Modified: Fri, 08 May 2026 18:23:28 GMT  
		Size: 48.5 MB (48488680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998e45db40ecc9c36a08506112c3f20bc4eb526266f691add187cf8c5c3193b1`  
		Last Modified: Fri, 08 May 2026 19:15:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c833f15fc7eb9a0252ec17262fa299ee4f18711488d492d6d9218750ac601608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369998acacbb8a5c623be9b9413a6360c609d03e1bb3e39e6453f8ec5adfc203`

```dockerfile
```

-	Layers:
	-	`sha256:a3c2163f77941aca96896bffde2e8a201a4b74247556db9ce55daa950b2a7f03`  
		Last Modified: Fri, 08 May 2026 19:15:04 GMT  
		Size: 3.7 MB (3734076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7572b48cf9a928ad34e5b818fa32759b4a5c5234ca45ea4c69d1fd1e2914d49a`  
		Last Modified: Fri, 08 May 2026 19:15:03 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:5e423e552c69aaf3796b41ca9493b7a903916f88bf6557f8c382ecc8307e9c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0c6bcbd2538154bc32f05463d53203b91fe4355f18b1f7d9e302a5baa64a5f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1777939200'
# Fri, 08 May 2026 20:25:33 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b1b0c9aa47ddf215e2ffe1a59a8711d75ec022455c81acf8501f0a9da7b810fd`  
		Last Modified: Fri, 08 May 2026 18:33:20 GMT  
		Size: 46.0 MB (46021589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb464f00be3b41014c045b99c6b83d183d92c3bb44e52e06b7134be4ffa9308`  
		Last Modified: Fri, 08 May 2026 20:25:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2052aeeb544b71aacc01b9a2aa5a668bb5e297f523890b67c198619989741694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef273fbabdb95787e148d9498c07be4f58ba812b75266f0b67179ab877e4711e`

```dockerfile
```

-	Layers:
	-	`sha256:101657d5b808af5078ecc63218b593b4cce5fa06b8ef8cb7155c073ace3a4f65`  
		Last Modified: Fri, 08 May 2026 20:25:40 GMT  
		Size: 3.7 MB (3734277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ae5c00daed6d65ea6e6a17e6a9163b9a8b002324c85045f76d11b68778c709`  
		Last Modified: Fri, 08 May 2026 20:25:40 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:642872591b725d50d8e6ea296ea75cf96013f59b9ef1c06abfba61e7cbe810aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44207924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee1cf24d327e0a5d807201fe918be9e00c0d3a4fe453e9719b64a5a365aff01`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1777939200'
# Fri, 08 May 2026 19:14:51 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e6981a7d4985c8f1a29ff2a2aa44ebc49f4e72bcc401163ca6bf21e3c96c7e63`  
		Last Modified: Fri, 08 May 2026 18:37:25 GMT  
		Size: 44.2 MB (44207701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e3ecbd76ae06b7c8fd6d79ca12aa36317c9d1b0859209036e1b9b144f6887c`  
		Last Modified: Fri, 08 May 2026 19:14:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a39842d898cef6225e69ee5f53958ce259a1b0f61cd32e3622d5e2d0c5020897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde798ab399a7e277294c8990fbd844765986d17907c51aa11159238bd6fc765`

```dockerfile
```

-	Layers:
	-	`sha256:357f0f22b94f8dd224f17dd4fa96595b50fd1459ad39c9f70894a7f382acb665`  
		Last Modified: Fri, 08 May 2026 19:14:58 GMT  
		Size: 3.7 MB (3736255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0517271aed42f6f84bf5f83be0e3f1b5dd993ac58ccab4fa0019a93353f50f80`  
		Last Modified: Fri, 08 May 2026 19:14:58 GMT  
		Size: 5.9 KB (5865 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:50af9bffcec04f1f21fd110cbefb02373e54e528edc0bf458f4deb0e480a46d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9128877e48fd203fca3e140df00728d6b8c4aba5d86b2b3d01809750cfb9aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1777939200'
# Fri, 08 May 2026 19:14:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:812b3ec5616894b0c379a85e11b5892f31b65f57f41e50a66c5ca907ab0f467a`  
		Last Modified: Fri, 08 May 2026 18:25:52 GMT  
		Size: 48.4 MB (48373156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29d92e8848085ecf05eb7674b6dd76be078e851df035e3149bff97a3049636d`  
		Last Modified: Fri, 08 May 2026 19:14:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:59db022f5ecf0f74d04e094959cda0964cc358272f8feff8bf99a575d287afe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef951cd66e98abc4fa6d66a7783fb66204cdc561330e2b3905d5b12de294038`

```dockerfile
```

-	Layers:
	-	`sha256:12f325e45c4c6ae4c149dac12857384671a0d8d8dcac8af6783590b4519a7658`  
		Last Modified: Fri, 08 May 2026 19:14:45 GMT  
		Size: 3.7 MB (3734291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d9687f4f5f3ab383652c617653a9c555e97ecb67b44b659d6407f5d197364b4`  
		Last Modified: Fri, 08 May 2026 19:14:46 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:2bd50d6ed7936a3225e5a135699f6eec8f7e190ee0803894e610a3d9cd9d5eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5239212a92774b35d20f5e883e713cedf75b7de2f95c2f501cf32529d3faa7e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1777939200'
# Fri, 08 May 2026 19:14:58 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b927b288058aa4d5d812b3d1f22508880ca3a6c34cdd8ab35f8e5c8b52398020`  
		Last Modified: Fri, 08 May 2026 18:31:44 GMT  
		Size: 49.5 MB (49477800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998e45db40ecc9c36a08506112c3f20bc4eb526266f691add187cf8c5c3193b1`  
		Last Modified: Fri, 08 May 2026 19:15:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6a0bf5b8acde8fdf30096b903122d561531d54e58f2b186c1c4fc67cf35a46cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f260d2f107203f35703e5b74ba278850ccd2771f7a656c008dc702dd9b4ca5e1`

```dockerfile
```

-	Layers:
	-	`sha256:87c24f35383e0e23bcb064fd6705e449e802ce4cb26e376515d7e996cfcc1208`  
		Last Modified: Fri, 08 May 2026 19:15:05 GMT  
		Size: 3.7 MB (3731272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a61325e189989a8667f0090fd9c0a3393f7320de7f7304e83ed073280a579944`  
		Last Modified: Fri, 08 May 2026 19:15:05 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:253dfae5a8e3a5b10ce7ade6893de48a858f82a1e18a468ebd4c333019b9a934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48782740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8ec007a57166a8ab8dcb142ce696a748e76e370f55d0e31a7a3f54c32c3162`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1777939200'
# Fri, 08 May 2026 19:15:23 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:36b0e902bb102cbef4bd7c716577263d6b4efffad6336b549ba104e261c3cb67`  
		Last Modified: Fri, 08 May 2026 18:20:36 GMT  
		Size: 48.8 MB (48782515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710cce78964966e31fe7e7a7020a31f27d8e63b781b46f0184724653aa0cfc48`  
		Last Modified: Fri, 08 May 2026 19:15:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:451f8405dcd4ae733209b4f2681203f2b22241090060aaf4a7f9922397a63cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb44a8c3b2fcf70c0d87988415afa5c3fdbdb1df8d2d6ed769f902f73c8feb0e`

```dockerfile
```

-	Layers:
	-	`sha256:8abe634d6402506d9d4caadc7386a94d72191cb95b2adc2a578a6c7d01ebcdda`  
		Last Modified: Fri, 08 May 2026 19:15:39 GMT  
		Size: 5.6 KB (5634 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:11b7be6bcac038e1846e4c3aaf93d2ac339c90f6f3642a673f82ae08e9737631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52337013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf7572ebe9958ee77a22d8f3e4244c9e548ef0ed846adeb1532116b7131876f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1777939200'
# Fri, 08 May 2026 20:19:15 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2ea70261cbaaffb21fdac08336adc6f09be805084d6e9545b304a01ffbe7323c`  
		Last Modified: Fri, 08 May 2026 19:45:06 GMT  
		Size: 52.3 MB (52336790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7d0834c46aea590ab42b710d36f4ff8cacc5e0dd01edede00055c9107a383b`  
		Last Modified: Fri, 08 May 2026 20:19:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ed6ddb7199f442e3dca0b380f884c96fc2e0ba6f0dc7a33453cae740d7bc8c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e24d33518a3ddfb02929b094550bfa98a36235d279459d40f890a58816e0600d`

```dockerfile
```

-	Layers:
	-	`sha256:4a51fc5aeab980bbb9b3d40204f19dec2066e02d8dfb790c3b6452fad72c1ecf`  
		Last Modified: Fri, 08 May 2026 20:19:31 GMT  
		Size: 3.7 MB (3738434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d19d3ac713f296641576a3f47e183db16f24d4373399613e347bb9bf09006f8`  
		Last Modified: Fri, 08 May 2026 20:19:31 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:fc0d2d5f7030a8bde720bfd3f8f4808a4cdb155316f624b9e1973d4a4f7f8fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47148249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e43d7e3ad3929ac6d406e0db8ba7c355acea73bd25a55fb227fcf708cf27c74`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1777939200'
# Fri, 08 May 2026 19:13:52 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:65e886521f9b7fb315ef93ddb8c8f8ad61b7bd37f4d6f655a5ed3004828135dc`  
		Last Modified: Fri, 08 May 2026 18:28:00 GMT  
		Size: 47.1 MB (47148026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ead5aa3a13db03317404e3a650d7256545b463603197b27278f53dcc8eb2bf`  
		Last Modified: Fri, 08 May 2026 19:14:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:89f848657ed2640d16ffccd7bb35640c1c7d2a2bc8125d97b566fec83784ed31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af88562c2f7ae9dbbd7e647d33c0bbdbc789fcf9e29731f1902b60d18656bba9`

```dockerfile
```

-	Layers:
	-	`sha256:284d8550dba18132ca8386f509c27fbcf138bf60d84bc03083636347d854e038`  
		Last Modified: Fri, 08 May 2026 19:14:03 GMT  
		Size: 3.7 MB (3730914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bf73e2f4ebcd75b469cfa16401141d0cb0ee90aa24aab691fe3c499bc5b70f6`  
		Last Modified: Fri, 08 May 2026 19:14:03 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json
