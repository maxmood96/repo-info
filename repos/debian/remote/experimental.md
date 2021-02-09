## `debian:experimental`

```console
$ docker pull debian@sha256:9c049a5186daf00590f3b438f20c020e4bee1d108d128d57782305f451b4bf57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:d8a88f87dd4baeb0d79b9578b3c79015e0d7a57c98f534b69bd5d4b36ed04590
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54793473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9459497426d22daa95117992eb99868abead5e988fdb2ac48bd90cb435243493`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:24:10 GMT
ADD file:5fff7912a33f031e6900fb1ba399f1a2309cfc7a7e9e9b4c0fb66c8a9d5864c5 in / 
# Tue, 09 Feb 2021 02:24:11 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:24:27 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2d2e73cabfecdef537df57471ee55848664babf96442397c65d9d647756fdde3`  
		Last Modified: Tue, 09 Feb 2021 02:30:20 GMT  
		Size: 54.8 MB (54793250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36b4e975c475cf861ea67b2ff7681825b913a4f323a7562f77e7e7b8b740c68`  
		Last Modified: Tue, 09 Feb 2021 02:30:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:b762c8a4175dd393a1019d061783c5781adaf9c428879ef48822f0e741b96408
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52324320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298697b3bf40edf6b92f36ce28edd6343f097ea525d86e765f47904de3bf10a5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:55:49 GMT
ADD file:f5e6b99d8ccfd90ae2118ac6332deb544f993928816090952a294f852576ed91 in / 
# Tue, 09 Feb 2021 02:55:53 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:56:22 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:01d27b91bf4ac6fc4fb4a7916ab9935c54d77bd5073415f26c1fd3fe9c934104`  
		Last Modified: Tue, 09 Feb 2021 03:04:24 GMT  
		Size: 52.3 MB (52324096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb309967c22f188378ca350b44cc26308d4415a1e632c18b9d5369bbcf1cb0`  
		Last Modified: Tue, 09 Feb 2021 03:04:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:642ac550c321c743775b8f292dfce4c8fafa618950f1417f6408a55f094e4655
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49983021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e628bd5d9e77b829008e06bb3a87456c82875a7448e978301c7c3ae1fc7b62ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:06:25 GMT
ADD file:4ab4adcf1598545a22be7cfa27a370966770f6dc07940c6fa28561124e66c918 in / 
# Tue, 09 Feb 2021 03:06:29 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:07:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:715ef43e37291fe5cc1926973d85676f5bbac775d3e6b17cef0ae491dd914037`  
		Last Modified: Tue, 09 Feb 2021 03:14:53 GMT  
		Size: 50.0 MB (49982798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a14b5f34bf5e6b744ecb946e7e591dfa0d7c39710b99d5e38899681a5f98756`  
		Last Modified: Tue, 09 Feb 2021 03:15:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e371fcecaeacc1ba948780af78896de0571877295ea3b86c39ec9f7e319e8c71
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53468031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e3092a6f30cc05e0c4b1cf7fce735ac45ac2c41244fde56cb03ec4aa572b8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:44:34 GMT
ADD file:f97007827802c11dbaf193fa89f53577a767f5d240d08eca24146ae542512127 in / 
# Tue, 09 Feb 2021 02:44:37 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:45:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:8245a9b80b143b81ff085a633ccc874674e1c4780905076472e63a2b55b0c164`  
		Last Modified: Tue, 09 Feb 2021 02:51:33 GMT  
		Size: 53.5 MB (53467807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbef815ed7caa7707ea2be684aebec0a199738b1e916ed29da1028515962d5c`  
		Last Modified: Tue, 09 Feb 2021 02:52:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:17181fa55386550112de828a907a76c0da9a4ab6eaf84b7eced3b5414c03b84b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55792253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495deffe93a09f7fde5565fe40322c42e1681c744078e8e5f0fd4980a7b0e872`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:08 GMT
ADD file:140b3610dc9b8e4a9d627c6f309bac307ab58190e9905085f23c967f31d31225 in / 
# Tue, 09 Feb 2021 02:43:08 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:43:25 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:19ccbe45e211a6b39595370ec661d4d75eeb6d94b75882058212a701b4c54d35`  
		Last Modified: Tue, 09 Feb 2021 02:50:44 GMT  
		Size: 55.8 MB (55792033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72d472c58e3f16c28e8b273d7102aa6970cdadc76a583af961a8781ab809d9d`  
		Last Modified: Tue, 09 Feb 2021 02:51:04 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:9390781c6809cb135c54f64f287105e45b460aae01b9c14f62e88ccb387a7bf1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53039047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb51b399e496371561fc6fc4b899b6c5cd132c9868ccd60eca907312cb4b370`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:12:12 GMT
ADD file:0ad13d56b4c2744bfd395513b9b24ee0d560749c9998a830f4c3f66f3b9d3a25 in / 
# Tue, 09 Feb 2021 03:12:12 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:12:36 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:47974fdc7ffae706fd8db519b261732fd6a710785b60925fd862260604bca2ac`  
		Last Modified: Tue, 09 Feb 2021 03:20:39 GMT  
		Size: 53.0 MB (53038824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d242c7a07b0b9a601e4a4e05a96ee6d348e51fadd4e0b59bc8d2e1e2427e2ba`  
		Last Modified: Tue, 09 Feb 2021 03:21:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:ab8f87c5f8f2e4522b76f29daa2ded3ec9c97b4183acd593f3954cc91a36105c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58695393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca78d63af36e22a03eeab95385e81ff89719fd606e9287da6c19a2ecfdbb3130`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:24 GMT
ADD file:c4a85e55ac3e2bd18e3032a0ab3b21ae13bc2c81065f15e415c7fae123ef26f7 in / 
# Tue, 09 Feb 2021 02:23:44 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:24:34 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:42393ea84fed3b0208be1091ba9327de438e01c4fcf1602a855b2cfa6882ea67`  
		Last Modified: Tue, 09 Feb 2021 02:30:56 GMT  
		Size: 58.7 MB (58695169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3a14ee80d6d6ec00e1f97a26d2659e31190b791a825315e397715da653c2c51`  
		Last Modified: Tue, 09 Feb 2021 02:31:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:75ac3b154643426b6aa8fbcb3eaf308212048fda8e4329cfcce107135e5a4806
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53060348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3004ba106666fcc08ddb42ce1ed02c71d4c38e5894e1e6071f04fcde41bfc34f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:43:32 GMT
ADD file:358da2cc09015996306a0276e0b743a9b00035dd5096961f0184722d2e3de6e5 in / 
# Tue, 09 Feb 2021 02:43:35 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:43:48 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a6edc0c79bff094cea9d99e03f9fb2ce964eecb0a250072e889eaab21bcea021`  
		Last Modified: Tue, 09 Feb 2021 02:47:05 GMT  
		Size: 53.1 MB (53060125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072ec36cfe8f44e1306a2fa820a1d1a214cc3310c87f5c4107f99d2fd7780536`  
		Last Modified: Tue, 09 Feb 2021 02:47:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
