## `debian:stable-backports`

```console
$ docker pull debian@sha256:f549c87ef1f36c7418b7a320466654bcebb354bda3cf9d68e7ad831aacbab1b5
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
$ docker pull debian@sha256:f7b25fb232fe9eb77a48a790d4e3dad273018b5213e1761c563f73ec323547cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54917307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35bd4c99fda4b6a46501fa6b4ac657ccce761f5a36a6660acc1a64c0e01c0224`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:15:26 GMT
ADD file:42365299314a35b06f4264252a3b47649e419c84aa75863ce42687f9191122ad in / 
# Tue, 01 Mar 2022 02:15:27 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:15:31 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:758b3507a6c88f0adf404b592d034acf4e19473cbb87eda20ac2d5b215558b5c`  
		Last Modified: Tue, 01 Mar 2022 02:22:12 GMT  
		Size: 54.9 MB (54917083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4487ca0286c73db6330d1ab93aa02e9a71f793212002c2a730f9b38d9764358d`  
		Last Modified: Tue, 01 Mar 2022 02:22:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:b3788b68ce4b4a270755f53ffcf10f0375000c1e0786911509a054111bf349ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52466469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776e06e17b45db76f658f7c5128da4cd22053f0d1bc287c73c0ded3106a2ef18`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:14 GMT
ADD file:469c326184a4d621f2f4416355450e46d5d0dbb0f3039c50186598504cb86735 in / 
# Tue, 01 Mar 2022 02:07:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:07:27 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:81ea8ee331e035c5149c50c0c970c0561ff513f5978d67cb82bd7ff059a62fc3`  
		Last Modified: Tue, 01 Mar 2022 02:24:22 GMT  
		Size: 52.5 MB (52466247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba68c0f76c396bd4c13334318e4f8ac7dbbb75c6f2531de8c83fb5db8efc4b79`  
		Last Modified: Tue, 01 Mar 2022 02:24:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6961324e2f392b6c4fae1e24417aa596d91c7d29e5da813f1df5882a4fa8663a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50117307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:085162751bb80c3daaa795e5d5ee263772eb5de7c4fca71777a4fb35072cae09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:47 GMT
ADD file:1254c2f5c9b5269f2ef420a2aff04fd540d610a207969f5ed36afd1fd62b11a1 in / 
# Tue, 01 Mar 2022 02:07:48 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:08:00 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a48fa07b0a28c8de26026838054ed7534e1f50c4510b96e46397e86a31d140be`  
		Last Modified: Tue, 01 Mar 2022 02:24:30 GMT  
		Size: 50.1 MB (50117083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9827039e3af52a85e154293de5dc230ea385c94924e5ce0e25ef6ff28937ada3`  
		Last Modified: Tue, 01 Mar 2022 02:24:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:13c3c18eb5d10368a938370dcf1351236560855da5be34ce34802244e38a3c28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53609019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67dbd733cfcfa17bbc68f07efebfc5809bfd7a9620ae6278773add3040e27622`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:20 GMT
ADD file:6b279724d645e9f194ab4a859f3e0262b416106a987e88babec88ba2c016fbc0 in / 
# Tue, 01 Mar 2022 02:13:22 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:13:27 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:21b136e402696d987fccf9981f6d99860b4311e450c311afbe1a5c1483c94e7e`  
		Last Modified: Tue, 01 Mar 2022 02:21:28 GMT  
		Size: 53.6 MB (53608797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f520c5e847f0ea1b49c7146d5ce07c5f975b9cdf0145f640301f9aff44efdca9`  
		Last Modified: Tue, 01 Mar 2022 02:21:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:00532e88c70557e8457199d3372c060d759ea358457100c611c7206cf2443d56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55938975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c372ffed3a9eaf689e51e52004ac21958d8c7fbbe0a6e79938f3c76df40f9c4d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:09:42 GMT
ADD file:795c8af9997c38216ed85923827f4ed1201efaac56215b3989462c033c142934 in / 
# Tue, 01 Mar 2022 02:09:43 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:09:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e47a088083863258fc58908b0b4d83890c4dabd1d002e4c900958852bfc40f42`  
		Last Modified: Tue, 01 Mar 2022 02:19:27 GMT  
		Size: 55.9 MB (55938749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5a7bd88ae0d6659aeb44e22324efb43ef68811e10886c55b5a2ea20b357447`  
		Last Modified: Tue, 01 Mar 2022 02:19:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:c07b98f5a5dfa70508ea40dff4cbb793df7c5613845ae3d5298996169c9955d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53180172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff7b61fe4cb752694e2fd4c5778bcfc5714278ed48e36e6aa87963b0164e828`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:21 GMT
ADD file:22446ccb92b020a34bb4fa578062e94a7e776313998cdbb8743e41442ba7ab18 in / 
# Tue, 01 Mar 2022 02:06:22 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:06:29 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:db3e6adecc9ec8995a8ed05a9d749b28d4de14d32f51c9d679541304d9030af7`  
		Last Modified: Tue, 01 Mar 2022 02:16:45 GMT  
		Size: 53.2 MB (53179948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4303b4b714a209c56828d9cc135e13903d71dfa9f193f5edfe34910d91e60f65`  
		Last Modified: Tue, 01 Mar 2022 02:16:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:210bc19cbfeb9aeeeab355404dd42b933e1e2bf3dd6ba987978ba461a0c5a78c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58834342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6578e654be9d46b1d985259b13667fb89efca0c0085383de7dec6b26d32aa791`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:08:25 GMT
ADD file:c6e5b056c4ecb473fcbc63681d88f2f87b0934c9ba037863e9da9b370f087079 in / 
# Tue, 01 Mar 2022 02:08:32 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:08:46 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9023d75dd894dc3a0ea6919a2f19f70fe20c23ca26106693ba19f113162b3cfa`  
		Last Modified: Tue, 01 Mar 2022 02:18:19 GMT  
		Size: 58.8 MB (58834118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11b75eebff70246db2cf542c2ee6b89a7e7f4c7dabbc0a83c9b221f2cc737d3`  
		Last Modified: Tue, 01 Mar 2022 02:18:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:ec75a8bf48854917734daf8e8bedf3616c973103feb44e0bb7d197910aa96057
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53210867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfbf40c3fcad7f5630b2589df99be5dd86bc4efa0d8b140aff5262684749280`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:03:31 GMT
ADD file:2563cc4d4f85cf86b17211e99875c1a499432b1f0db0d7226a6fce466d6d93a9 in / 
# Tue, 01 Mar 2022 02:03:33 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:03:40 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1cb5e622570607a49ba3dfdc8ab334cae7b0fa543c8b1e5964c1433a802ff1b5`  
		Last Modified: Tue, 01 Mar 2022 02:09:06 GMT  
		Size: 53.2 MB (53210642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61eb5c3fe8d5affb4f6e6728de815f5875584ef8e1131d8d3f8c845efeae6eea`  
		Last Modified: Tue, 01 Mar 2022 02:09:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
