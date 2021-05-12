## `debian:stretch-backports`

```console
$ docker pull debian@sha256:d4fd17c32bcea3a089a47a26b03f59a083d43fa66cdf00a026c17ef910608200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:60ae00f32561e6184977211d584b59b618879a31efb126c3f87372c786b30bfc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7823654d16eb30d2249d5ffce97b96c9f7c741e698e6331a4c5b6deac66299d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:23:05 GMT
ADD file:d9e4f6f4fc33703b766642a5642cabb2b01675bb55cf6050f2e91507577ff570 in / 
# Wed, 12 May 2021 01:23:06 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:23:10 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bfde2ec33fbca3c74c6e91bca3fbcb22ed2972671d49a1accb7089c9473cac12`  
		Last Modified: Wed, 12 May 2021 01:29:52 GMT  
		Size: 45.4 MB (45380083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcca14c28510adc107670f24bae6780b64c41df50de9d89e9fba0159a7aedffb`  
		Last Modified: Wed, 12 May 2021 01:30:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:593a515767636a3c1abe9792577d6fa2e4c93eb7d3bfb2d93ae33f947f727478
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44092260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b534efc9b571c41f3373cac929952a4278290baffe404485caf13d898725f965`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:01:01 GMT
ADD file:f9987935a0f0d3057590a5bfe45c9d8aefa9e442c57db487f8b67540669b57d4 in / 
# Wed, 12 May 2021 01:01:05 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:01:27 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a6665c6433be6a95f09c5848a9d88c4bccf7d8279967ab968e389649b956be87`  
		Last Modified: Wed, 12 May 2021 01:12:52 GMT  
		Size: 44.1 MB (44092037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377762665c70ed9f24c642e35b3a85bc0f981aae5a1e3c3ac63de1dd8069563d`  
		Last Modified: Wed, 12 May 2021 01:13:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:9354217b4bef4557455a77127a759996d22c0b900a8fb45a9c4771f7839d70a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa7618a8679c5074fe9ae27e1fe363d9f4815d6d8aa6569b5c8e0a6804be907`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:11:51 GMT
ADD file:81cfd4e746bdfcc19847240b77012487652be22dbd5741ccb2485a4207f2b73f in / 
# Wed, 12 May 2021 01:11:56 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:12:28 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:55b9a6b6b2552c5b2eac0a316e75a7bc18092819ee25c4f1d4d54700bcc1d3dc`  
		Last Modified: Wed, 12 May 2021 01:21:23 GMT  
		Size: 42.1 MB (42120307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0337355c69f9ca4dbe1a5f0f5c5e476756aca3834a03b69025bf687e15a8747a`  
		Last Modified: Wed, 12 May 2021 01:21:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c440f8f5eac7d4054f17dfa290d59b62c58d23adba86d656237bc0f82cf0695e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43178045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a909a358fe247556bb2ee6ab0b525e17f7c5c9225fa3c920e21dc7db537be270`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:56:12 GMT
ADD file:9582243afc9973a3708fda530270ae8f23796b20a532a9f07e4faaf245e2cdc0 in / 
# Wed, 12 May 2021 00:56:18 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:56:30 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:41f38ce3010a5142300d74e5e19db4dea7694f4771471c330fff27c633f8ba32`  
		Last Modified: Wed, 12 May 2021 01:04:15 GMT  
		Size: 43.2 MB (43177820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ff9e8fa68ecd5511c4bbe4a9659819bf796d3cb23a780979a54038b5d2becf`  
		Last Modified: Wed, 12 May 2021 01:04:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:de4686262a88c7884f452c6752d587e779ed18342eae1a3a3a9d5b945e6c5b89
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46098965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9e7ebdc908f26ed92fafd525b6ebeb27529e7d786d7744909efcf1ba6aadc1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:41:41 GMT
ADD file:3b26e2f83a0edf42ea62d20102b47011ee41cd2ab349c9da7487f62ff21b8471 in / 
# Wed, 12 May 2021 00:41:42 GMT
CMD ["bash"]
# Wed, 12 May 2021 00:41:49 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2a179d76df60628ca372acea241dbf24d4039a86b7dc2ba920d26f64bded15a1`  
		Last Modified: Wed, 12 May 2021 00:49:13 GMT  
		Size: 46.1 MB (46098744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4485d2a1957ec5d5bcfc787c2a93637d594e7179cda9cc9ffcacc06b4987c58c`  
		Last Modified: Wed, 12 May 2021 00:49:31 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
