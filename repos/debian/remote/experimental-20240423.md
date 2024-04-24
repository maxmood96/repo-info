## `debian:experimental-20240423`

```console
$ docker pull debian@sha256:f59142ae8cd0e68de264729f46c348118a51aaf52821455f59f0d13eb9547999
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

### `debian:experimental-20240423` - linux; amd64

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

### `debian:experimental-20240423` - linux; arm variant v5

```console
$ docker pull debian@sha256:fdbf1ac8ad5db02d40bb6d16b50a180d67ccdeddbdb65d1027b1f254481d6bc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49688441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b633429753d848d52dba449c7a5eef0e456d26c15b029bfab44997ffbb8dc03`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:55:07 GMT
ADD file:7cebcb353695cd3f692f7a1d2ffe7528f7023e525e9bdaafca1e3af7cebe2f3c in / 
# Wed, 24 Apr 2024 03:55:08 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:55:18 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4318a13bd5cf3e512e9c09910c10a618f4494ff741a0691e4d4adc2b3a22dc87`  
		Last Modified: Wed, 24 Apr 2024 04:00:22 GMT  
		Size: 49.7 MB (49688222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b850e3dce630831809c412abd801e7e0ff574988109c8c6f9b63db165fec4de`  
		Last Modified: Wed, 24 Apr 2024 04:00:46 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240423` - linux; arm variant v7

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

### `debian:experimental-20240423` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6d8e3603bf23c8c73ac4319941b85e50af427a9c67ae7710548436858f41c089
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52861010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55fd3eafe82114d264bdbb0204d91cc7046e108efe4363c7c8e320e0a15cf87`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:12:37 GMT
ADD file:cc6ddc4ebad675128e2b73e6bb15d012042f70099551a25d45ea9fdb62982bb8 in / 
# Wed, 24 Apr 2024 04:12:38 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:47 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:4a6d70ebc71ea30e7f1d5c5f091e32760bb88354aef5fba1b6aeff6cbbbeb075`  
		Last Modified: Wed, 24 Apr 2024 04:18:35 GMT  
		Size: 52.9 MB (52860789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3317cccdbf20a278b5c6cad7233dc22d4c0c3dd50d21cfbf9087c5ab935e685`  
		Last Modified: Wed, 24 Apr 2024 04:18:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240423` - linux; 386

```console
$ docker pull debian@sha256:598473b5cbc92b69e0f325522f5677403f21b17b8bfefc7999d3f44c27e667e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53469410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c058a29a14e330282971fa53d4f21750d8715ab27b18836269741b7cddaa74bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:41:57 GMT
ADD file:64e2f5984e092d024d0d5c46af3ca7d3d11c50df3121a311e8a3574c83cc2d82 in / 
# Wed, 24 Apr 2024 03:41:58 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:42:10 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d5c4d52670db79008d9c47aa1f63b44f18ed1b5b39d7d2487088e3b1c020408c`  
		Last Modified: Wed, 24 Apr 2024 03:49:14 GMT  
		Size: 53.5 MB (53469190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdbede1098245872b37af86e9474390a12141eb62540311333d27c97951f326`  
		Last Modified: Wed, 24 Apr 2024 03:49:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240423` - linux; mips64le

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

### `debian:experimental-20240423` - linux; ppc64le

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

### `debian:experimental-20240423` - linux; riscv64

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

### `debian:experimental-20240423` - linux; s390x

```console
$ docker pull debian@sha256:912e7dcdec82adc25feb709babadcb58f0fbf7bb1cc0171eca638ff7b45e04e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51982112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38e9f19688430ed0b7c7868eb93377f6163dfd6417463e5f04521932ccea04b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:47:28 GMT
ADD file:40076d588a48d42a412d091077febb0691efde75bdf92d8d5153f7ae60108cb6 in / 
# Wed, 24 Apr 2024 03:47:30 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:47:49 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:c4740335723c0c3af514f9148cb683e60ab57cb0bf207ebcd20406c7d4fccf78`  
		Last Modified: Wed, 24 Apr 2024 03:52:12 GMT  
		Size: 52.0 MB (51981894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa40012c6b2fcca6e450053e56ddbb71626f851f9bbd214dbded9a28f213c3d8`  
		Last Modified: Wed, 24 Apr 2024 03:52:28 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
