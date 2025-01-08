## `debian:stable-backports`

```console
$ docker pull debian@sha256:7c29cfc752c175695f3c8de4d306a9c3822d93b95e4f784319fa0c19659f1677
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:4dc81fb9db28cbde3f5726a3d92f8a759796a35c421b4baa59ed496d35250304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48497285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502e1c82c88579e45e09925d3d462ae2dcf0ca843a1fbc11aa1a3bb059cfc8d8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5fdd5f9704b8380a279c157119836b830d418cf9cb10aeb2366056cc72f7f189`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 48.5 MB (48497064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e869e26ab55c8ba620078956675f6cc7c0419bcac0ac9722bc7dddcec32d176`  
		Last Modified: Tue, 24 Dec 2024 22:13:41 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6c705d04e79c95254b9d069e3bdfe3e5840dec6adf3ff5917b44e03338492c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa20d73c2b4fcd7bb902965d9e50f72045684ffd57c502e9e04d778cb77cbb6`

```dockerfile
```

-	Layers:
	-	`sha256:6af04bed5652b2533df105bb06e2a3e4bece8336d5407fa1264d3a29cb18f65d`  
		Last Modified: Tue, 24 Dec 2024 22:13:41 GMT  
		Size: 3.6 MB (3619206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30f3e51dc3997a775a45bcfa3dd8918761d7d128b1110f3132c5039375965cfb`  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c6e6b3e3e8452d80c57d742c7663a1a81415ea4fb268af3a06b32ad1e60958c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46024468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072250f28f594ea43bd0881de3c81bcb08ac62c9526bb669b8c8eb7f825a6e66`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7c50581b6105f93d6e44bad0c83b1892194b7fb14d90ca037464df2975ae2f97`  
		Last Modified: Wed, 08 Jan 2025 04:31:39 GMT  
		Size: 46.0 MB (46024246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435211f31840bcfcadcff5379f6f6567fcf00d6327eef67892bbc8cfbf7ba218`  
		Last Modified: Tue, 24 Dec 2024 22:20:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:51e648f69ca77f9b966968faa815ce80727c4c5183bb64c4228377d7da543b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6198a01d1acba5670989218263658231fc340435e67fbaa252028f940668f6ad`

```dockerfile
```

-	Layers:
	-	`sha256:cd963db57d3665e942ca2a7af01a14cfb18429ac9fa2bd838d9c0702a940bfb8`  
		Last Modified: Tue, 24 Dec 2024 22:20:54 GMT  
		Size: 3.6 MB (3619407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b65606ef21b1038d31f4ed7a06a04fa9c23cdf43201d14fa5b20db9267b2e6e4`  
		Last Modified: Tue, 24 Dec 2024 22:20:53 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4b40e3ebffda8e339a97e64d111bbdf38e9813ca8d4f6bdc74dda633ca78ffd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44200192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7aca2c28a3b18476bcdc0e7ec9275e7e9fc31ec59f9eb4676db4e5febd3cd62`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:346045c0fa70494340ef6537a3e28483ca2cc712c5573d65ca1ae05afcf583e1`  
		Last Modified: Tue, 24 Dec 2024 21:36:10 GMT  
		Size: 44.2 MB (44199970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41044aa5a969fa1f2e72639e677d2a7ac7144069418eef8fda7f6917336ac123`  
		Last Modified: Tue, 24 Dec 2024 22:17:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e262c2093457c190c457006f96e0570c20bcdc340fec7fd8f5cec8bdad6ff955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4369f2b96fde63295e7c40adcea267430d3e89aa183158ca2efa92a6acf36c`

```dockerfile
```

-	Layers:
	-	`sha256:51b3e742f69d664eaf79b86e73d7ba56905e2412e80ef85e809a4677a9b7d108`  
		Last Modified: Tue, 24 Dec 2024 22:17:36 GMT  
		Size: 3.6 MB (3621385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa905001b12db335185fff50cc0158a717a359ac2f15d399d0b39b914e5b4840`  
		Last Modified: Tue, 24 Dec 2024 22:17:36 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:fe0ca544a3694a1def376711ac26030608431de46126bb1cc93663228d98c076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48325702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8f53502568d01f51c8bf501568ad4b15b05d4536f533c834073a07ebee1b88`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3bd7181085554d05d43bf545914b4a327772466961c05f7e01ed4e13a6cfbc8a`  
		Last Modified: Tue, 24 Dec 2024 21:36:09 GMT  
		Size: 48.3 MB (48325482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d014e82e2e07741679f4b7c02481216b59e1a05b0a9d904a44e39cb904312`  
		Last Modified: Tue, 24 Dec 2024 22:18:20 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3a3de052c0bf24bc260dd83385cbaebd208326878706889c8d9165d2843856b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba5c9017190cce483f4d21f03b7ce754bf6908c2ded59d01f3e988100aa17ba`

```dockerfile
```

-	Layers:
	-	`sha256:14cfe210ed20eb9760246d7962258488279b411b15558814d1c85d39bbad16da`  
		Last Modified: Tue, 24 Dec 2024 22:18:20 GMT  
		Size: 3.6 MB (3619421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35388834281caa1124eeb728e2954a934e8a7812770dd9b1e6c79090d4b7c36e`  
		Last Modified: Tue, 24 Dec 2024 22:18:20 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:d90355296d752cea05b0c4f4c5233d0475ad60cd7f28bd21fe29e7f436eb91d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49476144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f63b16208190ccee14b55e7f7b4da32ea3b552852a8fa57d4af0961a51e751`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f029448567e0d98114d98b90e4c569f38b83a491ee83cb8d26972a72146cb624`  
		Last Modified: Tue, 24 Dec 2024 21:32:37 GMT  
		Size: 49.5 MB (49475924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5214a5bbcb57ef4995318806df4343509e316b40822bae261a17d2d0cd99a3e`  
		Last Modified: Tue, 24 Dec 2024 22:13:52 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:25b17d5ca61c57053ac4a9704d48a633f7d182efc2f0dac1cc58c85981c81f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3622177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b33a91184671bac8fd764d7c0dddcc9d1185229685211f8f4bd896b325e8b85`

```dockerfile
```

-	Layers:
	-	`sha256:c11f6153c9083fc0f83d62e6a4646ff76de72c08a4cb889af2e9c44e0fdceb78`  
		Last Modified: Tue, 24 Dec 2024 22:13:52 GMT  
		Size: 3.6 MB (3616367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a486c369d9f5f430487e6a9d1da783d379552e9779c5dfa8d2e0a0ba0f86968`  
		Last Modified: Tue, 24 Dec 2024 22:13:52 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:02a8c4397c555e7c9c604cf0bc36b5e819f849725006bf368c3c5b38e765e27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48771867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb1d08f6b97a4dce0631057c5b131996ad3d2828bc9a29336dc6f53544a8268`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'stable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8c095f130f39b9bb9ad24f3f3210e6f2b01d9bdc28318de8dcc226a566278902`  
		Last Modified: Tue, 24 Dec 2024 21:34:38 GMT  
		Size: 48.8 MB (48771645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93d48b9729d4d86fd5a0843e22ed91969fe58895d04c5134d1b20f9d810dff9`  
		Last Modified: Tue, 24 Dec 2024 22:17:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a699233e14d2fa7b3d2ab776f504c23617f1d19aa3e16e7a250225f26788a9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6a3d4d15831983b32b460bef874c1d6ce29f614c1e0323239a273860b9426e`

```dockerfile
```

-	Layers:
	-	`sha256:367bcbb590eb0b4b6b37dcc10bd13e5aebabe0c22a7caa9cbc1c217831dafb42`  
		Last Modified: Tue, 24 Dec 2024 22:17:33 GMT  
		Size: 5.7 KB (5650 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c5c64453638f058ef7142f910ae4c9e0b002db83a363b9f1cddcf1913a117171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52328303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f739d06edf2244f337137768dca80a07351f77e13b88682e28a8d3f603a47b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b63b4acaad3d7af53c2a06e1f8c908f32beed4fd980dd0e05f3e16c9d019aa4d`  
		Last Modified: Wed, 25 Dec 2024 00:34:21 GMT  
		Size: 52.3 MB (52328081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef11553842a58ffffe50aa4e892b7f09be3bb6a23f7ee67172f050497a196418`  
		Last Modified: Wed, 25 Dec 2024 03:51:26 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4d2acddba5a7863cec26475b6ac7ce8c3b6894e1e31a08097d820969bfc4790e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70edd27804dcf4dec0723a09ce106711849db0e2d23c638afddbf53b476770c`

```dockerfile
```

-	Layers:
	-	`sha256:00bc4c681e025590d92cbc8a1b021ba3d987de4f4ea07b41cb674699f0a9e701`  
		Last Modified: Wed, 25 Dec 2024 03:51:27 GMT  
		Size: 3.6 MB (3623466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:137abfd414e425f4ce98f62216b4a2f473d861ce39099d995f292e7fddc4da66`  
		Last Modified: Wed, 25 Dec 2024 03:51:26 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:6a1e9e8dd2337f60d9fc12238ed054a1514c967f89ae2ee2ff2bd7b47f6bfc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47149851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63111a7c66c372e1da5a3353e63af6964acc1dc5af17403a24af82fec7e9d7ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a1fd59012c9e52490bcf2324684b34f5c4d1762b6daaacea75e37a2d9238ba2d`  
		Last Modified: Tue, 24 Dec 2024 21:35:08 GMT  
		Size: 47.1 MB (47149631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17b76118e40bf2319b84b8541b3f9db4a524322fe749f4dfdbac5f7851a312d`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:11e322b24ae78c17ae100ee6347957da8d286628507258239ec6ff515847f650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3624763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52266d1b17c5c626e4c3212224c55f60668e33b219206f8b04989977e6f6c67b`

```dockerfile
```

-	Layers:
	-	`sha256:8d89b9fd5f3a3fc1b084e6b18015e45ab53868fb9c165fa111e84d2c75741c87`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 3.6 MB (3618936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f127124a9b2611ce368f410730a605f1da6e9b8ab35f0d6c2ccedd1893893c2`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
