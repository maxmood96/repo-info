## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:302de6ccb1237785333412d7d70bdb64edad7f5c5c4bb80ee579b383d6f9319b
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

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a46617c635cf7c885e2f741b3308f1e65c98a1e19515a0954959ef94081812d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125436932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9564ff86d3091c7760338926393f13187612898bbae224360fd36969581b1bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:54:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:55:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b4675e1918dcb7f5c9bfedbb5a8634d2459306d1f3b91f08c7293380f10585`  
		Last Modified: Tue, 12 Mar 2024 06:03:29 GMT  
		Size: 15.8 MB (15763469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f67b1746a83d257a6398cf8eec47bfa1f854670097ea4234f12857cfc7d5932`  
		Last Modified: Tue, 12 Mar 2024 06:03:46 GMT  
		Size: 54.6 MB (54588494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4b82a28618cd428cb303a3b3fed70c1fbaa15e2d7c0ec88a5213f7e5fb324f24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014ab67dc0681bc0aec86fe312177d276bf8643ab040b0b846c51bb075db4fe0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:38 GMT
ADD file:e13a63ed3af4c4dcb74dfa2a2b12a285563b8c905dbac41b538492e1e100f93e in / 
# Tue, 12 Mar 2024 00:48:39 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:36:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57e872a0ca7dbab84f7804705a96154de6b3cffcdb4f8946d4387764bfc1e307`  
		Last Modified: Tue, 12 Mar 2024 00:52:01 GMT  
		Size: 52.6 MB (52586778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6eec0fce74f09fb69d81e686677faf5c980646b0666d9c658371a380575876`  
		Last Modified: Tue, 12 Mar 2024 01:44:24 GMT  
		Size: 15.4 MB (15374813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47860a0c6a6b4af8b3bf2ef7b59f064d37fcf25f1ae20363c633b276713acb2`  
		Last Modified: Tue, 12 Mar 2024 01:44:41 GMT  
		Size: 52.3 MB (52328861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9dac4341f985ba6f6da87a345745251d4e1f1f88f5abbc11ff21dd613f0fbe1b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115478050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd4d99544718ca88c6a40d99f13d278f6c4ab785d0fcac3d99148b6fe4aa000`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:25 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Tue, 12 Mar 2024 00:59:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3dae685361a941719b8f1aafa21f93305a1df032b9e9940f90b7dafabb394d`  
		Last Modified: Tue, 12 Mar 2024 02:20:17 GMT  
		Size: 14.9 MB (14878987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a08f233733bf767f50d39c3e0a1ce20900043f44a7e4df655c1c5556a9e2834`  
		Last Modified: Tue, 12 Mar 2024 02:20:36 GMT  
		Size: 50.4 MB (50357621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:50f9d48738e31a49e12cd8da39a4d5960ebea181dfc08c81fb3eed98f5ba53fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124165603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42ccb34be84e46eb9856d81064e642bfb16e932250605147287fc82f49f772a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b26e715641714983e979229284b3dd79698d1c59197f4e33089c8c196e2956`  
		Last Modified: Tue, 12 Mar 2024 01:35:44 GMT  
		Size: 54.7 MB (54694301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b9d2d1bbeb1a9c7d440ca0bbdce6e3b16fbcde367d9fa13057b28010dee90f63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128253649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f814dcaa1597e9d66a274df2456808589086d74b54a14e03d9c850650bba5ee9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:12 GMT
ADD file:e7e92b37650e4d33c3374ca47bc378c2b4e15f7c7e0a7c7fc659a29c5b3fc583 in / 
# Tue, 12 Mar 2024 00:58:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:42:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:42:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec2ed44737cc768246d63628c6de48f2d223cdb3a6c218bddd11786679e34647`  
		Last Modified: Tue, 12 Mar 2024 01:03:04 GMT  
		Size: 56.1 MB (56057973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e62ee72cfeca9426a0e18adfa8e6b05d9f029372d831f73d3e089ccb16f297`  
		Last Modified: Tue, 12 Mar 2024 07:54:46 GMT  
		Size: 16.3 MB (16267990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e632a01713bf6f27a1de411f14f1e21b375412e471fa832f03dc7ea3c86a0a51`  
		Last Modified: Tue, 12 Mar 2024 07:55:07 GMT  
		Size: 55.9 MB (55927686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5fa1a7821881083e40ead9bf790cb63689f782905b96113519aa764c7b1636bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122348826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245a78fc3d28c1fba5c24a42c04a692d9b60f560c68e5aa3055dc5edfef73ba4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:53 GMT
ADD file:ceaac889009e9d867969b5a568939eb0f6e136303e3438d9747193d6ef4755ab in / 
# Tue, 12 Mar 2024 01:06:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3856c0b5cf8a29fd86ef6fe0c2a36a38020518c2e120457769b9044974ec1ca8`  
		Last Modified: Tue, 12 Mar 2024 01:17:56 GMT  
		Size: 53.3 MB (53303519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acdc20e5c94994c036364331f6d067dbe2215bca100c34dc233aa97abbb88e3`  
		Last Modified: Tue, 12 Mar 2024 02:45:06 GMT  
		Size: 15.7 MB (15734611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4f183b6f40e96072119ab41213733a9079dd8d43cd4a7c36f9f7e3531dd614`  
		Last Modified: Tue, 12 Mar 2024 02:45:50 GMT  
		Size: 53.3 MB (53310696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4ca5ed2831818a94c464ffdf78335acca49d1cd6e75f265e00fee6da1246bed8
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134593742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71d28760fe78cfdc496496e01e97a5dba19414830d62e4ece7deb0bf643ad6f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:37 GMT
ADD file:378e777c8961453a2c8c9a594105395e4a83f5e94a90756bc3eebe9ec18be242 in / 
# Tue, 12 Mar 2024 00:30:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99575d2dfd5e66cfbe10e815aa8a7bfacb8fa923bf112abd5b9334bec5404161`  
		Last Modified: Tue, 12 Mar 2024 00:38:29 GMT  
		Size: 59.0 MB (58954475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce422567beb05db7b6d7eca359e7168a80a58b1c86d36287c6b86c9b76d845f`  
		Last Modified: Tue, 12 Mar 2024 02:21:17 GMT  
		Size: 16.8 MB (16765930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777aef5bbe7e540f91bd63fda95e7f25c0ba803d2a25a532b2f2306c6b2209d1`  
		Last Modified: Tue, 12 Mar 2024 02:21:36 GMT  
		Size: 58.9 MB (58873337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dff51578c019416cba8959947215e6ef4365bc531885e874fb8a3e4d552facc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123036566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200b30cd7082400a7d00f01fa2fff2d45ffcf3f75e979a708c121c5d07fc7ec1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:55:12 GMT
ADD file:acdf6d23a12147f9c8c6eb2c1074e5f2013daaf2ab667c770659494a89e9c8e3 in / 
# Tue, 12 Mar 2024 00:55:14 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:861d490dd592be84c92fb7027a5967a8a2009c66688194260d1c5a413c8aef48`  
		Last Modified: Tue, 12 Mar 2024 01:21:28 GMT  
		Size: 53.3 MB (53319541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb2ab3b8920b4d36bbda5b2807296d8b751492cd2709f164bb76692b98f7dae`  
		Last Modified: Tue, 12 Mar 2024 02:48:21 GMT  
		Size: 15.6 MB (15641294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8050bc0c7be4bc967cc1413b9ab67358c6a153789b08c99737f54df7feafc27`  
		Last Modified: Tue, 12 Mar 2024 02:48:34 GMT  
		Size: 54.1 MB (54075731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
