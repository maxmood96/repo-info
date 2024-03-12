## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:afc33e8810f1d5f99ec8737fef40bfeeaf07a91e529ee068a0e35ad3d180e923
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:54bad33a45b9ca1a12af0e9ddc561c5e8795c704e6aa9dc4a5ed004ddf57f83e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55085201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38415a1a9a1d5e7e88d89b8eff496576ee747a357ed9ef3b8e520ec4a3cffe8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:22:16 GMT
ADD file:31cac24b3aa007d2c837ff4849fde49a8006aca13a8553438d76cf9d87bdd173 in / 
# Tue, 12 Mar 2024 01:22:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:22:20 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e998c6fe3af8009739cdce8af305e5a885b8211d559c77700ea2339c17e9f23b`  
		Last Modified: Tue, 12 Mar 2024 01:27:50 GMT  
		Size: 55.1 MB (55084977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4e0c053e8c1a3dab1b2ef6fb29bd8dda6e890557241acdd26116aa948b65c7`  
		Last Modified: Tue, 12 Mar 2024 01:27:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:955dd1c7b824262f3c1dbcf4dedbb9182eeea32bf64581f031de022a5fd66974
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52587015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc463bc0f65aa7e8a2e2eb21255b0143f8a6b5c89903c93de20cffa01127a99`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:54 GMT
ADD file:fa29daa9f78388d3f2b450fdc74233676b449203c2677e5edb005c829966e6bd in / 
# Tue, 12 Mar 2024 00:48:55 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:48:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c7a42d77bfff00d90b76a3b59027102b4dffa56c7a39997222c53b6751a0cbf5`  
		Last Modified: Tue, 12 Mar 2024 00:52:49 GMT  
		Size: 52.6 MB (52586791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6306e6bda546e210979752ae14bd09b0849b4fe1b43a1974b4f3057ff3ac3e1e`  
		Last Modified: Tue, 12 Mar 2024 00:52:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6afcccad1f0ca0cbd61a8d8b9115d3229227492f853c759688dbb0d020852491
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50241664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8818a68b7bcf480f3495d676c2b3205521d3a6e9646b9f38abe179d4b564920`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:00:26 GMT
ADD file:dca6d554665d7d772c257004b0112d019a5c3d498066eadf4c32a56f3081453d in / 
# Tue, 12 Mar 2024 01:00:26 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:00:29 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cf82f78de4ed3f65b5b672c8b7bcb8e2fa17307358b08e97f4868604b5528296`  
		Last Modified: Tue, 12 Mar 2024 01:06:03 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257cd2b053c46e33fd4d06c2763b9ab571d73e8fd5bf2e0b15cf9c234a2fb13f`  
		Last Modified: Tue, 12 Mar 2024 01:06:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6f70f4e5b293eae63db26aed6ad11905daaf381d4435dc28c2ff72abb6a24901
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53722328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc754d975ac53e46a8bc9b89809760aa95be20e3bdf85d84d0b0d39fd37843a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:27 GMT
ADD file:d833a3e759e6b4133df1f81f885a1452adfd570d7b182379a9214accbd8ef964 in / 
# Tue, 12 Mar 2024 00:46:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:46:30 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ced198c6e739c76e904e8482029dca10ce3dfa4dccd8f60662d89ef4d83de089`  
		Last Modified: Tue, 12 Mar 2024 00:51:05 GMT  
		Size: 53.7 MB (53722104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e5e3a415cf3252bf4ab9fce741d6a535387c289daeabcc09fbe2ee906381c4`  
		Last Modified: Tue, 12 Mar 2024 00:51:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:5fa070431161048591fa1b4f138975582f6fbf5cbc5d9cc28f89c21c1130bd6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56058207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396d652f67cfe3ce8e5e19b500bca3388c9c6c53bf22ea6dfc888ef777e677a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:18 GMT
ADD file:39ca003ccec28fe8b81d45b5798594e20cc28f9689669ab1a58ee9e03149bf4d in / 
# Tue, 12 Mar 2024 00:59:19 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:59:22 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:42de443d1e920b67ca52af496471bbf1d8abf348e757e7c5d2fc0d21a24e43f3`  
		Last Modified: Tue, 12 Mar 2024 01:05:16 GMT  
		Size: 56.1 MB (56057981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18d51242a29426582d8fef61e15b428a256ae0aeb6633761c6c227fb2a48428`  
		Last Modified: Tue, 12 Mar 2024 01:05:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7c0465b03c10616cb13a51bb8ae1fb586c8bf8fc74ec160ed7d4879073d31098
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53303772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638cbb54850cfb8c5e5ae0150309a1394cd938c0544744ea576e3adea5bdc0e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:08:10 GMT
ADD file:097f84896ea46035ff67b3859117e1b11c903de3453d087ac996f7e2cab70188 in / 
# Tue, 12 Mar 2024 01:08:15 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:08:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d0cd2a5f8952ec3c61691d2b20ed671c1ef8c6c62f3dce5b5d37a605a1385656`  
		Last Modified: Tue, 12 Mar 2024 01:19:20 GMT  
		Size: 53.3 MB (53303546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304df6b6b72839605f3da58624bb116605bb3b3b24439721932231cc7e7a0ae8`  
		Last Modified: Tue, 12 Mar 2024 01:19:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:e5e2f0a0133dbabc1d2f6490fc482e073bd1ce5fd72c73165b2d7fe509cd0f30
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58954706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8450ef2b977754e410750d8f5ae3422adfe863b8f25269b0b68c59d918d3715b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:31:23 GMT
ADD file:cab5d18a2f1866d4eaa6515fcfaf4422d857eae48443378a026405fac1ccaf05 in / 
# Tue, 12 Mar 2024 00:31:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 00:31:43 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:34481cd75948ed16301cc6de4328e8e5b4b80aa18408dfe63a305d412ee39550`  
		Last Modified: Tue, 12 Mar 2024 00:39:18 GMT  
		Size: 59.0 MB (58954479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf41a3a960a31f04024f796708473e62825f31655520bf9b3e738a733aef84e`  
		Last Modified: Tue, 12 Mar 2024 00:39:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:59774f34628dee8b27b46e8807f4167ff8cfb289502bae990535ff49b06033d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53319763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d402fd736fa4e9696aba8cbd8c5924669f649027080db525e445dea9d28343e4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:3cb4abfb1cd1d1c9f80227d7fdfce7dd448cc8b044380319700c873b8b5e7f3c in / 
# Tue, 12 Mar 2024 00:59:07 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:00:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a81235c4801df7ed5c004f6dcc8c1e84dc99e8663c3d5e0524c42f342108d9fb`  
		Last Modified: Tue, 12 Mar 2024 01:22:06 GMT  
		Size: 53.3 MB (53319539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed099c05488bc24b8a60e17222ad1b110d81948e96b2fa199516e23897f2c7d`  
		Last Modified: Tue, 12 Mar 2024 01:22:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
