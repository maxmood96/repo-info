## `debian:testing-backports`

```console
$ docker pull debian@sha256:6559cc68b74654be89471defeefc322df4cd958283007a413d5150fbe17a9571
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:4e6f8ec3e13475c7447b2141bad7467b11877a8349419fa70022ab19d6cd23aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52332550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c9506043d95696fe427926b32fe5ddb90bd13a168a825edeafc417e1423b95`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:53:13 GMT
ADD file:f52df68480a4f4b019c4ccf809927839b337aee1176e28fc9810a53b1b8146c8 in / 
# Wed, 10 Apr 2024 01:53:14 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:53:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bc5ec5e91c5d709afa0648dd0c8f1a32bfd6cb4361cc16d9e7a6dd966e286c4a`  
		Last Modified: Wed, 10 Apr 2024 01:59:20 GMT  
		Size: 52.3 MB (52332326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e20520f050c58fec79110155fbf0738bbd7965e6dcfd5c9319be9d061d810de8`  
		Last Modified: Wed, 10 Apr 2024 01:59:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b4d17637f70de889743c68422fc81db82433f47303e4f059dd840e50d92a93d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49422335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd75707d77b5f006bba8299ab6ca303f977e407cd2de4ce3fb072ae8d2aa9572`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:51:27 GMT
ADD file:ae1348d798cde702b0166ee65d6c0dda3c44d2472835ef3fd69c4ec9f3126645 in / 
# Wed, 10 Apr 2024 00:51:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:51:36 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c6856860e87bfee7077457fc1ad2f6569b55b8d22214e2695aed9794bf36e6dd`  
		Last Modified: Wed, 10 Apr 2024 00:57:41 GMT  
		Size: 49.4 MB (49422110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf346514449fa2d6dfaccd44eeef520d46f50be87509dcc20494279b05610a8`  
		Last Modified: Wed, 10 Apr 2024 00:57:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:99716f801e94c19f08991e176a40c9f8b291e35ee9d156e17daea329ea6223f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46920270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6f4bb1d001b99c6dcc3a6b8d76fb80e3569bee18aa1d9f06507881d95462aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:01:26 GMT
ADD file:fbc79606f92631343a474a994ddb484cf9226ca7a8f350853a6f57e8ebc08989 in / 
# Wed, 10 Apr 2024 01:01:27 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:01:31 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ddb129906acc6262bdd0bfe82b788f5829bf583b8d2b1d4b18c2a48b4ebe66c1`  
		Last Modified: Wed, 10 Apr 2024 01:08:40 GMT  
		Size: 46.9 MB (46920045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd0cb29774417aa93c045421d716582e115024caa985f0e330f245208d6ef28`  
		Last Modified: Wed, 10 Apr 2024 01:08:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b268b6889dd25c70c89fd9f782e754c1ca81af79fecd2957a1c26a4590f1f6bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52194034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579d478ff5a66a47d79949c7b3a766bd8e00df47e5ea7c7aad91a7796af4aa9f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:59 GMT
ADD file:c1dcd2a0564b0f415e37aec0f860788ea1a7d93297d92334df4a88c427e6a0a5 in / 
# Wed, 10 Apr 2024 00:42:00 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:42:02 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e97907a307822d1fe2c2fb105577bd49075d36f6726aea18395aa29336a73c74`  
		Last Modified: Wed, 10 Apr 2024 00:47:45 GMT  
		Size: 52.2 MB (52193812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea2d1b7831b4c7a6a3568ca3ed3b7bd72ce5b4950382cc29ba96fd50527a435`  
		Last Modified: Wed, 10 Apr 2024 00:47:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:b929ee419e3fb0d719dbbf502b5638e58d69be1a87c9dddfedd7e47622ed143f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53185431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39172515da86eba2eb406d91a9d460c7606363fd67ef6a02b3ef796f4346503a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:59:38 GMT
ADD file:654454bdb08b5293fb8b87b32d408252bd318b903044e4ad5cf1247534c82150 in / 
# Wed, 10 Apr 2024 00:59:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:59:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b5a66ed61e0ef9b676922c64284c85bc1eb432baee2010c9e81b7e8fe0d98105`  
		Last Modified: Wed, 10 Apr 2024 01:06:36 GMT  
		Size: 53.2 MB (53185210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd8f2d810b8cb2397db850709a341f5d54ffa56509df8194f203b2265e6aa4a`  
		Last Modified: Wed, 10 Apr 2024 01:06:45 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:09c8e3794fcf873df524ba5a40a791d6862e7a4ac2f53c909794e72081150748
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51411451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c90b7eb29e2d9e12d914807a49c547044c3753fd0ce6c0489a901598ea13b75`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:16:02 GMT
ADD file:4810fae21d6871813d00b1b390b16c99fe86d5e5b511bc2a2f44d03108830c0f in / 
# Wed, 10 Apr 2024 01:16:07 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:16:19 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f7f1cb94481755b6ac8c1b55d86cfb94a5ea44c390eca305c24c7b4a75494ffe`  
		Last Modified: Wed, 10 Apr 2024 01:27:51 GMT  
		Size: 51.4 MB (51411226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d82688735fafec22e67fe6a5dc5067cdd11efc8ef67c9dd69314c0cadcccb7`  
		Last Modified: Wed, 10 Apr 2024 01:28:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:0439178e5533172266398dfc09889ac8f28342968b63189d543e88843364bd9d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56250332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b752a3553bd2bb61641124643943ec3f0053df69d54e01a61be24f2a2436a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:28:29 GMT
ADD file:193248d1bc625911c89a98335ea79bb3b150c617f0d592617d53111697f46973 in / 
# Wed, 10 Apr 2024 01:28:32 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:28:37 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:462810f8d1325bd2e552b3d4de71c2d19a8d4a6ba90e851363a3edba7e1eebb1`  
		Last Modified: Wed, 10 Apr 2024 01:34:13 GMT  
		Size: 56.3 MB (56250110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c748393c2cc58c8c2d5a6060c0794c219b1d4fe3afa4faffa33d155dd79b935d`  
		Last Modified: Wed, 10 Apr 2024 01:34:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:3cc53a6f38e0cffb13ac4af5f10df2473ea4380b6a38349d21adc964c8d5afa7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51761984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f58823a7debb1a5fe8ca87b90cc019547720e8d68fabe9597985564f4e9fe8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:33:53 GMT
ADD file:19a79084cf1c7ac5a03ae781ebdc7c6d8fe545c99714224979d7e2a0b2fd0ec5 in / 
# Wed, 10 Apr 2024 01:33:56 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:35:18 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f41f30e09b733b618c212c42fd18a7262bc91c28c3663ef65e03b659c16c3e9d`  
		Last Modified: Wed, 10 Apr 2024 01:50:28 GMT  
		Size: 51.8 MB (51761762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a73d011e20acb948caa83d123b7ebace987106319a45b30a7bc636190b278ce`  
		Last Modified: Wed, 10 Apr 2024 01:50:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
