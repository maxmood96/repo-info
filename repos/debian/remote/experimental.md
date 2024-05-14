## `debian:experimental`

```console
$ docker pull debian@sha256:cc1006bdd87a14c914ba26724f5bdd92aee240ef48b67e31483bd9f4d9c3cdfa
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
$ docker pull debian@sha256:e6b2af36856b5c2cd3441b663dcb3f7e1f7e999a2e17e3b10517af42a11ba21e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52577372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088a1da5c35404d78fe513bf48bd9efcae20ce80bda838f72dfb4e1dfa6471ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:31:07 GMT
ADD file:9495a8e39a60cc866b680c07a70c970d2fe7c86def9145e9ff4dd626dd866d5f in / 
# Wed, 24 Apr 2024 03:31:08 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:31:20 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0c829912e8a006b4ae08586c3af2fd292880a2e52a2fc84042a4b05229da54f0`  
		Last Modified: Wed, 24 Apr 2024 03:37:21 GMT  
		Size: 52.6 MB (52577151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62f5b046096da29bed6c1cc3ccfc38a754a129af732b62bf70000c84ea8d178`  
		Last Modified: Wed, 24 Apr 2024 03:37:43 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

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

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:b79b514cd907e2ab114acfe6c4835f5caf2b1f9e49daced5f5b8532fe584c17c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47214422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88fc68030d83c8f61975b25e6aaa35b34c57f805bd88598d46b794758528369`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:09:40 GMT
ADD file:74bbcfe04dfaeaef471cfdf1f4c43c5dd4c412f94a0410cdb4e5841e68ae3055 in / 
# Wed, 24 Apr 2024 04:09:40 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:09:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3c87d47ffa594e3697977bd06b36d20aa75491d48c60aaa357afea9b27d0f839`  
		Last Modified: Wed, 24 Apr 2024 04:15:51 GMT  
		Size: 47.2 MB (47214201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6a24707989dcd9b76733cf3506613afd297cb97338b41a2525d0b70bb24809`  
		Last Modified: Wed, 24 Apr 2024 04:16:12 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

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

### `debian:experimental` - linux; 386

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

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:a1cf17ad63a18f9b87edc8ceed722c2a753a097349c6f467751c8d447e116b26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51498696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372cb4725598f205ea5e029d6426fe3f078c146c4516f4e524f097c13ad5d729`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:22:15 GMT
ADD file:a122cfb2c89753566ec6fa3c4fd9387e691c9d1d1585466ea6a9f5499d024a64 in / 
# Wed, 24 Apr 2024 03:22:20 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:23:03 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c59eec5a6fddec84005a2b18d734bbb75865763c7e5b98000be0dbcacf229b76`  
		Last Modified: Wed, 24 Apr 2024 03:33:44 GMT  
		Size: 51.5 MB (51498472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52ecccb2159c94ffcc3946521539ffabe5bcf2c3d95f1838b7b0e094e2ab6fd`  
		Last Modified: Wed, 24 Apr 2024 03:34:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:5f8c4800ccfb8135bf7fc7e149b71f16398984e991b32c01312a7398ba67c158
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56489444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f337c879cbaec1d1a45a2edafe3746b8a15284b71db6b6e6d9a02942e84d4667`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:24:27 GMT
ADD file:93ef1da9d6960e83230304261d3d99aef1a4672ffa8f63c2fbfb784e30bff204 in / 
# Wed, 24 Apr 2024 03:24:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:24:49 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c80edb328db34f5850b6cb7e03ca34bb72fecb27aaa01ac8a1d128ff19e38202`  
		Last Modified: Wed, 24 Apr 2024 03:31:18 GMT  
		Size: 56.5 MB (56489222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4566d25f19dbf51b83ebb399b8c7562e2a333896f34394548b497459a2fad7a`  
		Last Modified: Wed, 24 Apr 2024 03:31:44 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:e45dd5de4890a0ad3a4b9a414b322ff663d137f229ef8793bb8d8d2715d1e015
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50665633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a40fc9c6c0ac1d95b8bccfaa6cce21595290f4646d072982e50d5286c41588`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:10:43 GMT
ADD file:a95faf1f554ae0b300491cecf4c6673ac4513e69d5a04e655b5889bd1c72bd65 in / 
# Wed, 24 Apr 2024 03:10:45 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:11:21 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:aa8b4e50fe262518d117b4f920dcd7ede0214f4a5910bd41e86ba9e6b178aef4`  
		Last Modified: Wed, 24 Apr 2024 03:13:45 GMT  
		Size: 50.7 MB (50665410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704c7c754175ddd831b2168dbb146fde3bf7413c2d95fd24473ebd85a0989740`  
		Last Modified: Wed, 24 Apr 2024 03:14:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

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
