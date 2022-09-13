## `debian:experimental`

```console
$ docker pull debian@sha256:adf9243e9c02c8acd2e5b35317b614556979318379605d208eb2c2374265c4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:b543cd094edd0c9271c9b5fca680344af2fc418a057b0d63276b7e07cfa744f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52643827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8726d4a11d5a96a53b643c2295a1091d3ab5e77655e107f20885a1950835405a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:58:12 GMT
ADD file:6ddd5244833a0a8b71e79b85b68064bd5b09f430b1b0ed8db07d6855ad470c39 in / 
# Tue, 13 Sep 2022 00:58:12 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:58:23 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d48fb30607a31176a332991b7110d4b196c3564594e7aab632b9662094ec885a`  
		Last Modified: Tue, 13 Sep 2022 01:03:54 GMT  
		Size: 52.6 MB (52643603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8feed5ae45c9f1637fd673679cd602a43eda6d5645f8656d5220cb52bd1cd905`  
		Last Modified: Tue, 13 Sep 2022 01:04:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:92cef5e5007a0834e3ff2301cad38e5fa5ffaa802f02bd29642f4170f15d3b66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51786153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89292022e7fa88d2015b754dd03457cbe7a8b265b040d276bc7042b5b32623eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:16 GMT
ADD file:e7ec9bef12457f73465a8b9b0d10d2ee3fdcf244d19625f58ba4ffc2fcab0a1d in / 
# Tue, 13 Sep 2022 00:56:17 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:56:42 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2ea2e84f45a0dfa7c04aa60a28b638e9696ca74b5f08fff59842aa2fadadbc5e`  
		Last Modified: Tue, 13 Sep 2022 01:04:36 GMT  
		Size: 51.8 MB (51785933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e1d1040164c9b35fe18a10cf8b6b71419e3fad3fb828ca0d3e407b584c0818`  
		Last Modified: Tue, 13 Sep 2022 01:05:10 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:af8076ae62308d45f0d44ac330e1b2a7acd22704c0545d9ca86d3f94a10da23b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a806d67f22387e69819c7297dbc2ddac1db6d659eb34f1f834256b8c6fe7bba6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 03:45:38 GMT
ADD file:316de447e7e9f6f5bba29c81e4a849e7ee538e8cd9d987c533d7d708a57dc926 in / 
# Tue, 13 Sep 2022 03:45:38 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:45:57 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:48f63bc69a50dce66c69dbfa1843b773a3f97c12ee8c30aa82238c3e89720c05`  
		Last Modified: Tue, 13 Sep 2022 03:54:31 GMT  
		Size: 49.5 MB (49523984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f6a998b855afc1a0d7c41db45ede1885989870abc1234e82bcc3403a174801`  
		Last Modified: Tue, 13 Sep 2022 03:55:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:81eb5592dbe07e190d9930b20fd1ad29a7023805f6b9fdfd0fc733b0c70cbed1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53103866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da7755575056c1db111299b2d73745cdc2638a666dffad32662ebddc9363cf0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 02:13:00 GMT
ADD file:d357f92d2e6059b34d5c7465364ff9f56bc2c57e1ada96abeafbee42232442e5 in / 
# Tue, 13 Sep 2022 02:13:01 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 02:13:15 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:a732c342fd5bd9e297c3826e5ffede2bb1ec74240be2eb95bbc01ddab67f5c1c`  
		Last Modified: Tue, 13 Sep 2022 02:20:01 GMT  
		Size: 53.1 MB (53103646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0caf5bc7812ed1d38eea16ddb4a8c15a6c9f26ea78279afa3044fe76f0e10a57`  
		Last Modified: Tue, 13 Sep 2022 02:20:26 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:ea070a79a636fb3938f2c36055d424254e571d21eca1809bc38df3b453b9a43d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54012226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e941bd7adf4000aa38cd788c96fe2916b5441d545037e58e3eb9296b671af6b0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 01:42:00 GMT
ADD file:0b8e235621603ab2fb8d8bd454110314664257b33c9bdb576b8e9beeb56a554a in / 
# Tue, 13 Sep 2022 01:42:00 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:42:15 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:2b00d003a10dff7f0b5e7669d0e79c7db1087d585ac955fda6fedd57c17b5a90`  
		Last Modified: Tue, 13 Sep 2022 01:49:06 GMT  
		Size: 54.0 MB (54012003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f65e87a97f1000d2866b4b95725e067c239091aae4776d2a2ee3a37eca32f96`  
		Last Modified: Tue, 13 Sep 2022 01:49:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:de458c8c759c5fe8c1008bd3f828f55590f0736d10aaf59944d9911c92ac5b4d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53078993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d84bf906799c78d04ecf6474c0a6543f31f3308149424866774c9b89408c7ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 01:14:45 GMT
ADD file:77c56c6e050c1b05ab9501baad2287db6a16694b54c343827a15e0f2b8eb74c3 in / 
# Tue, 13 Sep 2022 01:14:52 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:15:31 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d4c0c91bac4c2b1030403ac7f21391e49a31f19c38be32a354ce4a0b2dc3c24e`  
		Last Modified: Tue, 13 Sep 2022 01:23:22 GMT  
		Size: 53.1 MB (53078770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f1295aaee08c7c36bd3300a28dd028c6503ee0bd7d3c44635a360230348cd8`  
		Last Modified: Tue, 13 Sep 2022 01:24:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:46360b7a842adf7451d728eb20593a6ccb8caf2b63bf31c22141929667e03b56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57189799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e0ba861aade11c9cf86c55fca1c978e8d1442482a2c14b5adda2a08c73b91d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:02 GMT
ADD file:d1634b63d2bd1f30b1ae24a7c858899fdfd81e39b052ab7224ca5992031a1dfa in / 
# Tue, 13 Sep 2022 02:10:05 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 02:10:26 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:799b92af2b316da8115da1a82f8d630cd0f39feb7f577a029f1731209e077140`  
		Last Modified: Tue, 13 Sep 2022 02:16:44 GMT  
		Size: 57.2 MB (57189579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c47797493c10788f0a73b8cc87259e2c558d9f8f5a7913cebdc4741e7afb9c7`  
		Last Modified: Tue, 13 Sep 2022 02:17:17 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:15814716e2bf56a900293fcf617fbeb55ad8e95ad0da9ad58e901fc7147f5b8b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49268485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605454f3ff125eccc5af3040a27437fa2d4a3c528fd3b6806ca0326010d3d183`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 01:15:34 GMT
ADD file:c24a06026da1c3034a3f1a56f5442ddfbccc49c2c5a41417a310008f4a9f7861 in / 
# Tue, 13 Sep 2022 01:15:37 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:19:10 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ffff872507fadc561776e433e62758c0c30c21b8c17996b023e1a3702994ce3a`  
		Last Modified: Tue, 13 Sep 2022 01:33:54 GMT  
		Size: 49.3 MB (49268257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd5262f8b239640c85057c6121c5ce27b9dbad0093350c0eb86bc698505e80b`  
		Last Modified: Tue, 13 Sep 2022 01:36:57 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:5be8b87514dd868479dc2731fda809a9f08f777df173fcb0af703500e4eb3f5c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51537223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f517eb61c1d8e9b97f0c76d87e074b3f23f21666d093fd138daffee9db97d66b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:49:41 GMT
ADD file:218a929c0b84eeef4dd935bbc23ec1a4c9fc02f06cf5c86ca6c8e94e78c5f927 in / 
# Tue, 13 Sep 2022 00:49:44 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:50:04 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:ee6e329c518cbd235ab8d38fbd5ffb98ffe45bfb2874fa69e7084eb6ecd09ca1`  
		Last Modified: Tue, 13 Sep 2022 00:54:17 GMT  
		Size: 51.5 MB (51537001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e60677fa0219710676fe7d6c382b68d19f4d901be63afc7e617ba536f3dea5`  
		Last Modified: Tue, 13 Sep 2022 00:54:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
