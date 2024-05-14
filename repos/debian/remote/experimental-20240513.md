## `debian:experimental-20240513`

```console
$ docker pull debian@sha256:9baf8a9511f18a637518475ebc024e54b1f41b54d0725708117d19056e53d4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; arm variant v5
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `debian:experimental-20240513` - linux; arm variant v5

```console
$ docker pull debian@sha256:0668ccf49cabed88a3a04714b45376759b03c54f650998b214b1345937cb7c15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49745382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2eab483a0e3f8b1e7ab3659f7994fe80371ecea29e2c899a49d820b1358bfd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:50:17 GMT
ADD file:521734357b4e269a7cccf4adccbbd4daa760954a4b217aeeb9b49671638b4235 in / 
# Tue, 14 May 2024 00:50:17 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:50:26 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:f8921a756223f341386642e5fc17db8ecb3053a0e841396e2b5311ea042f7c6a`  
		Last Modified: Tue, 14 May 2024 00:55:21 GMT  
		Size: 49.7 MB (49745162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c7cb0c0879088932709c672d68ed25f600eb0ac62ebb65f6af6ba46776f3ae`  
		Last Modified: Tue, 14 May 2024 00:55:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240513` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:688a66c857e765546e689221c11e0d9af5ce3e2f55be7027636c13490896a76a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52930506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a93b5e7ea55995bf1b4608e3cfdfc5702c534239930ebae2ce83da77188235`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:41:38 GMT
ADD file:6c54381ec578a9f57036074fb948edeef7611c02bf29d34f212fab376078813a in / 
# Tue, 14 May 2024 00:41:39 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:41:47 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:cbcdfed4b85cce0d6fb37326a97d75504908bc768ddb092ec6e95591b57c661d`  
		Last Modified: Tue, 14 May 2024 00:47:13 GMT  
		Size: 52.9 MB (52930286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb740826b14f0c7b180aa4cfbfc572ae080489b009f988724508f60ceb2d216`  
		Last Modified: Tue, 14 May 2024 00:47:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240513` - linux; 386

```console
$ docker pull debian@sha256:a29e952638bf01085cd342437b605f89ccf62efae9f54c4b475a02f9f38adcfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53540159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db527ea6f0a5cb0ae3962b5e202681591085d6e419927be52b48fc5cff2da8a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:50:17 GMT
ADD file:826e7bcbf08f9ff2dc0b9ce63104c53184d5d6387c42ada2162d2ec51e68f4b3 in / 
# Tue, 14 May 2024 00:50:17 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:50:30 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3edf4a10c208a633ebd0b77ce4c2cacf895ebc393e6d0e36e5939cfc8f4595ad`  
		Last Modified: Tue, 14 May 2024 00:57:35 GMT  
		Size: 53.5 MB (53539939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9f5e64cd5d43f05ebf956f9dd4c6a7aafadeaa9daef41e8fec628947916037`  
		Last Modified: Tue, 14 May 2024 00:58:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240513` - linux; s390x

```console
$ docker pull debian@sha256:b70285bcbc25e852120e5e01e2135d1e410f20bdc60b6a0271a3f6fe2ffc0c27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52293504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deff9e019300f92f74f2ff2798b12905e8d654a26729885ab213bdaa03e2fef0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:45:53 GMT
ADD file:39996ceefd01e3c041f2eca344ee84f600a0ab67c058a6eaf088784805639943 in / 
# Tue, 14 May 2024 00:45:55 GMT
CMD ["bash"]
# Tue, 14 May 2024 00:46:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d46d86ebff408f9c6b07805c1a092479e08885dd71224f34f876559c9a617552`  
		Last Modified: Tue, 14 May 2024 00:50:31 GMT  
		Size: 52.3 MB (52293285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc0f7651df0162097faa37eb635cc874945e76c4a279f2a98395f42c1e6391a`  
		Last Modified: Tue, 14 May 2024 00:50:48 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
