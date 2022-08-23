## `debian:stable-backports`

```console
$ docker pull debian@sha256:00fc26e26ce10b2221c5841d0713a067e66419fb89d03bb1c7f7e4b96a8ea025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:a9a79fbfae1729ada9d52bd5dfb0f8e4e29449e29b27bd26c20ed57fc7c5c56a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55007780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d444c22564565736c6ad1dee5b14c7e5df8ae90481dd745d28f12f8cbc2c4456`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:57 GMT
ADD file:44c550a883e90ed6f9256847f2e0b7d03dfa87361c0c0256d3f7eb40580d78c7 in / 
# Tue, 23 Aug 2022 00:21:57 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:22:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0b5aea898977d2f7786116d9cb106042377e6221d2552a75ded2f040beb2c24d`  
		Last Modified: Tue, 23 Aug 2022 00:27:11 GMT  
		Size: 55.0 MB (55007556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4293a17c1b49faa7fbc0c8d2e57b39228458076fce2cc2a85f795a527ff8d46f`  
		Last Modified: Tue, 23 Aug 2022 00:27:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:fc17e5e4d402f9a35b4764c79e6f30a1bcba6f8e564e53906b5e15081af643b1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52548081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329568cb87411b3442c36d6e1fbcf372f9449218a294df0eebe1a9968665e941`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:18:04 GMT
ADD file:93ffbf1e4b456e1a2d7e8c23b36b52482b3ef4612c86ea149b9bf398c9b06c4a in / 
# Tue, 23 Aug 2022 01:18:05 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:18:11 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:63ca4c957526976799732f5d92f1e3d2a0a69d492b2a50a1a2e033747eb24c3f`  
		Last Modified: Tue, 23 Aug 2022 01:23:58 GMT  
		Size: 52.5 MB (52547856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e9be2de7188f915474c25b5606fb40e663de977b2f3c2aa8105a48acaf23f9`  
		Last Modified: Tue, 23 Aug 2022 01:24:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f39724a7b04ce1e11dd52676e10209fd12be2b51d205e8c56868d3ffbd6ea87b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50205158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6ef7117b84917e2dbdc37f3e6287cd55164c04f7413889720ccb6af3e3dcc5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:45:01 GMT
ADD file:8258337dfc0645ce426d6dd6af19232978c467688d3ce0eb4e074cfcb6814b7d in / 
# Tue, 23 Aug 2022 01:45:02 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:45:08 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a199ba1ecb719e70e77944caf4b212401d467cfa213206824647570f8212a0fe`  
		Last Modified: Tue, 23 Aug 2022 01:52:45 GMT  
		Size: 50.2 MB (50204936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4207e552841c66bbb04456beb89a442fa55fe7be88f41519228c6adfbc82e6f4`  
		Last Modified: Tue, 23 Aug 2022 01:52:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b43cfc61594a77219dd1ae85065d250158cf4c5e1228f04820528ddf8bf2f080
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53691077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b6e083357bba07df7dbc64d2720a0846a0dd549be367b480fa4a503185c817`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:53:52 GMT
ADD file:a2d566809c5b419e9db89df55459a7395fef51ca1219fc7208c6f85ec1563fb4 in / 
# Tue, 23 Aug 2022 01:53:53 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:53:59 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8de130993eadd6b4f6351b9cb731d73c9d4ef04db732eb615c12093f56a958ee`  
		Last Modified: Tue, 23 Aug 2022 02:00:24 GMT  
		Size: 53.7 MB (53690855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04acf260827b0883f1ce4f6b92f0331b115421768e5cca0356ffaac834f94811`  
		Last Modified: Tue, 23 Aug 2022 02:00:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:45ef29c2790182012d00dae9dd827d058a6fd68f42c290ebebe458038bc68243
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56012831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d67c9769fe692d62fdd0b82c86279bf75a02daed41bd5031ac4b35acce4db2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:04:04 GMT
ADD file:718525d7041ff4b05a60d23e77526cebc9f1b62915e7037d43558e579f5639c7 in / 
# Tue, 23 Aug 2022 01:04:04 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:04:10 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a36b3bf017cfe2e2756db405980ea7d3b435ef2a1eba38e958b5ff8b7f06f9dc`  
		Last Modified: Tue, 23 Aug 2022 01:11:00 GMT  
		Size: 56.0 MB (56012605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b2e0ca117559ce735210ace40c22e5db70dbf301ae62f0acf52158ddc85c01`  
		Last Modified: Tue, 23 Aug 2022 01:11:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:18a313441151e284921b989423c23549c7392422ceb9575fe2e137ec8632b00f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53273243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2285b7b159e6be701f33d3da71a027868c38b059f65b264ad12a622702b239e8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:12:57 GMT
ADD file:f111219fa55c5df38672bb7b42040526beb6baca250e4ad4ee724c1a9090f961 in / 
# Tue, 23 Aug 2022 00:13:03 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:13:17 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d3836c0ff2a3ebbcf11d16fdfef0948db59cc812e579ab311b2e3b198b373427`  
		Last Modified: Tue, 23 Aug 2022 00:21:30 GMT  
		Size: 53.3 MB (53273019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93507289598b4214668e787ef501a02c71d8721717fcfc4b2ae725fcf4a8af93`  
		Last Modified: Tue, 23 Aug 2022 00:21:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a6ec25eb68eca4f66ececfca129684115b4e0b612f94b07f76c87f31001c1adf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58909370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ad47b147e8ea2bec49a3627887b7ecdb3c2a432b6eb46bc938e55a359b58f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:25:43 GMT
ADD file:f474fd83b474b41171768e552a1993f3b7da37a522012724f0d46c2f863e8b82 in / 
# Tue, 23 Aug 2022 01:25:46 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:25:52 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a4bc0955a358c8291f574ae20699fd39fa4f20a382cc3bbdd6b74f39d40534de`  
		Last Modified: Tue, 23 Aug 2022 01:31:52 GMT  
		Size: 58.9 MB (58909148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c89325e1696407059cf407349030f0706ddc97cff7ee197388507b4e9e7cabe`  
		Last Modified: Tue, 23 Aug 2022 01:32:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:0f7c83bd033c04f5881d86783b9c67aeae813017a1f2b47d12e705b46fd14878
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53279370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0569388c442287df4f8917e50f743955b9838538354334304107260987570b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:54:36 GMT
ADD file:9d113fcd340351f914b9de464bb96c13184e614768715dac9d86638fe8c3cfec in / 
# Tue, 23 Aug 2022 00:54:39 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:54:45 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c809cd38aa237539241e2d35a9e9e68aa93b4932de8c51236d3c94ac872b4799`  
		Last Modified: Tue, 23 Aug 2022 01:09:57 GMT  
		Size: 53.3 MB (53279148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73be2b09f754df476522f21b1669ba34dd2fdc1467636d1c36cd5464f73dac26`  
		Last Modified: Tue, 23 Aug 2022 01:11:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
