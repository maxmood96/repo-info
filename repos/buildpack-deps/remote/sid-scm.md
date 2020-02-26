## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:a89faa3e551ea286db375e97c25260ffa4a9b4dda44eb0e337951538005c272f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5dc86e27860ded32525d666822429ae0640923aa182ae919d5e5417d4d40fd3b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125288125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4874fbd401accf81e6b2260d2b4cacb601f7941a6ad8b512a6cb2fe25d233bc6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:40:05 GMT
ADD file:bec180e92743e5024fcf273019085a4de227f49fe65e76828b9c7f740fafacce in / 
# Wed, 26 Feb 2020 00:40:05 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:15:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:15:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 01:15:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8ea0d19362f06fe2b59b222ce913ba48c67c375897c1011c35ae714403602dae`  
		Last Modified: Wed, 26 Feb 2020 00:46:06 GMT  
		Size: 51.9 MB (51852485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dd00a16259f5ef437d658e1c9a35286e86c1b1e57ee707e76e7f633f9addcf`  
		Last Modified: Wed, 26 Feb 2020 01:22:25 GMT  
		Size: 7.9 MB (7923560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd95542fd67b65c74ba330b9fbc3a0338708e71af91f677f4c837e08e89f590c`  
		Last Modified: Wed, 26 Feb 2020 01:22:25 GMT  
		Size: 10.3 MB (10259454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040bc7d271e35c9971c628f49f18ba318438168e369228977edd9f27c6c65cbb`  
		Last Modified: Wed, 26 Feb 2020 01:22:43 GMT  
		Size: 55.3 MB (55252626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6c4167c38ea49be53d627b1057f46e053088bb1e61578357c5ef364f3635b0b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119604414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b0afa7f71c6f0cacf05178c853926efa760afe4888827a83e7b203db855f07`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:52:33 GMT
ADD file:e863dd2efdd5f4a6e29a4da391218d83cf13d07b263a55c438361d48079dd528 in / 
# Sat, 01 Feb 2020 16:52:35 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:34:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:35:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:35:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25551be68c42d4da1cad9359e21cdc842a69363b035a77721ddf9ad7db276105`  
		Last Modified: Sat, 01 Feb 2020 16:59:21 GMT  
		Size: 49.5 MB (49540705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718af626bdc2f1b7d5facec6b5ba8016afa8bb5d691f4ead7274c55588a7bf48`  
		Last Modified: Sat, 01 Feb 2020 17:47:57 GMT  
		Size: 7.5 MB (7494164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19493feb9c608ccc1c197cb34c49c8902d9e560ef999db9500a91a6244e10e0d`  
		Last Modified: Sat, 01 Feb 2020 17:47:57 GMT  
		Size: 10.0 MB (9974015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9e0dd91a0c5d9c8d98b8511ad3af8cf0d03337280a36a0032e81abf0aaedfc`  
		Last Modified: Sat, 01 Feb 2020 17:48:25 GMT  
		Size: 52.6 MB (52595530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9a2a64d5d856987da91089c4ebc223f4327313d505609c00ff14a14173884e71
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114490528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c953777e8b7c1b98b198a7a8dd190a6945bdb32af64215377dca1220645661`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:02:49 GMT
ADD file:a4c8ca5f07a6e213b314bd30a4cd27bba9df71ed8ad4f5f82c07878e8cf99f39 in / 
# Sat, 01 Feb 2020 17:02:51 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:14:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:14:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 18:15:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:983ca3edff7a1184ea4165bcc490182822501d698a99e9d6bc8d6c042881bb97`  
		Last Modified: Sat, 01 Feb 2020 17:09:51 GMT  
		Size: 47.3 MB (47282209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087eb801e68fecc5e62e530d27b51862c664c2f3864a49a5de683335fe76ff32`  
		Last Modified: Sat, 01 Feb 2020 18:29:32 GMT  
		Size: 7.2 MB (7233892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39dcb92a180a0696b4e0192f43515454f02db1da2f7c7eb7d2fab9f7fc58fb75`  
		Last Modified: Sat, 01 Feb 2020 18:29:34 GMT  
		Size: 9.6 MB (9637780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ae46ffceb2e8839ed8010b48cee3ddc26b851befbdc6df6e9346dc543dc581`  
		Last Modified: Sat, 01 Feb 2020 18:29:56 GMT  
		Size: 50.3 MB (50336647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2070060cb2ee835dcb802dba2fca6aab04e8da311fc33641af9addb30efeb5cd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123675555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66e710292cb076fa6bbf8256932e4ded0bd0de3255936a50bc14c3ab033f75d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:58 GMT
ADD file:636edb6845120aa418f3291c0858ab38c7d658cb2790c08b113e8068fe152a32 in / 
# Sat, 01 Feb 2020 16:42:00 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:26:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:26:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:27:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a3f06cbd9a524c44b9b8c92922dc9c06d87668d76af414bd34aeb7238502e475`  
		Last Modified: Sat, 01 Feb 2020 16:47:18 GMT  
		Size: 50.5 MB (50505966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66da598f357ac8ab4c813dc7a16cf57b1d0fdc7579b59a9a2cee24efb09f057d`  
		Last Modified: Sat, 01 Feb 2020 17:37:33 GMT  
		Size: 7.8 MB (7793001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a8f172b9e64796699f56dc5a838982165c0591f68740791b1d1e8971e09602`  
		Last Modified: Sat, 01 Feb 2020 17:37:50 GMT  
		Size: 10.3 MB (10252714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48a71f1808040c4e34e7856e42f28683335784039b75aa3cc9c48c178a2bced`  
		Last Modified: Sat, 01 Feb 2020 17:38:15 GMT  
		Size: 55.1 MB (55123874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8c70fa19bb82c2267554d37db9f5d137324573a4890b880b4d9a786be94b9e13
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128859180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f762e7baada3f8b7e98980045bd62ae5d95616b7fdd64d3a96d45f7bc24ec56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:34:15 GMT
ADD file:527aa2259b2366e4270d004b42a2eeebcb49adafed28b5a8e91d2e1eeb66191a in / 
# Wed, 26 Feb 2020 00:34:16 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:21:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 01:21:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:00a1553babb601009b2783a2a5321157baa25a79030b9f4ec05a591f0ab4dc19`  
		Last Modified: Wed, 26 Feb 2020 00:40:36 GMT  
		Size: 53.0 MB (52999556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dcfea1de6377d5d7b7f4a8dd9386ef6919ed23af5811eca5c9cd495f45c97b`  
		Last Modified: Wed, 26 Feb 2020 01:29:48 GMT  
		Size: 8.1 MB (8103631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6adb539590202db492bc8bd3bc0c15f73c1afdfc2c040ace64c75cb8cfa048e`  
		Last Modified: Wed, 26 Feb 2020 01:29:47 GMT  
		Size: 10.6 MB (10623153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a72cc05db9c9b0ba5991e0e4db1e43d82c1e2b2ab8e931d481e161308c139b2`  
		Last Modified: Wed, 26 Feb 2020 01:30:11 GMT  
		Size: 57.1 MB (57132840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d324c6bdc5b536c8d9f8816603529808b20daa8ba1ec07b454ac3ddbe3930a12
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134885422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9861482997203b816a86c66a713895b74cb8bd1df35b205bfba5bf51c09757`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 17:19:01 GMT
ADD file:2546930304b6d429e56e56557d14acb509152fb02a657d195dc0595d0f5a4523 in / 
# Sat, 01 Feb 2020 17:19:07 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:54:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:55:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 18:56:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9186c7a47276773316addd180b90c065065663e993fe107956ff3f68e5245ad`  
		Last Modified: Sat, 01 Feb 2020 17:28:20 GMT  
		Size: 55.3 MB (55349044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4e183e934f7fe63d5cc430bc444d8bc8d74f0c7a34d5c296a7ec8ed6818544`  
		Last Modified: Sat, 01 Feb 2020 19:22:41 GMT  
		Size: 8.4 MB (8352504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a69e974fc4af43c554b35a2c9f65fd85b3aaa73f605838d1eb693c55f6553a`  
		Last Modified: Sat, 01 Feb 2020 19:22:40 GMT  
		Size: 10.9 MB (10935015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05df67ad4f3bb0a431528d60fb40ff04a1b6211584456971eb2df58fe84abdb2`  
		Last Modified: Sat, 01 Feb 2020 19:23:21 GMT  
		Size: 60.2 MB (60248859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:13af4ed89c69b84cce31ed33494e5f9dccb5b0505dd4c9f399234bb77fb97568
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121922667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4960fea22e83a927da7129c140ca946e87515ea22b2fe4244c97cb4c1de7057`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:00 GMT
ADD file:967a85341ab042321428ced1b4d7f5dbdbb8d9f2356b825a4904ac635fd3d22d in / 
# Sat, 01 Feb 2020 16:43:03 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:58:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0f7573b6b276747f41f68da62a4262a7441ff49e4c1231d18c674b31be00a6d0`  
		Last Modified: Sat, 01 Feb 2020 16:46:30 GMT  
		Size: 50.2 MB (50192313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08d4727245007c4f9adee1b2b8d19c1edb9dfd3fcee5a9e21f17b775626c570`  
		Last Modified: Sat, 01 Feb 2020 18:05:30 GMT  
		Size: 7.6 MB (7592458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04f6008c2ca1d93fb6eade84d84b0c35dcd4e6b6d056df78a2babcda2d74dbc`  
		Last Modified: Sat, 01 Feb 2020 18:05:35 GMT  
		Size: 10.1 MB (10146865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64e0b150ed4e4ec6000e21e1b26ed6ebf9e97d500c59f1fae814fbe0e3f7bbd`  
		Last Modified: Sat, 01 Feb 2020 18:05:47 GMT  
		Size: 54.0 MB (53991031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
