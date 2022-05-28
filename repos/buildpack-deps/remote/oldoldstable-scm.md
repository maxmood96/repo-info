## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:0bda528aad17958a52daa666e4361f2fa1041060f85a9574d11656455945ee19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7433dd904ad38bd9b145b375c153869c0692bbfbf8d6cfda95ade03edd956d5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110838493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023eb7e0ee69ee4cba21f692939fed53dccd3d31a293a289defc152a7f0f5e86`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:22:05 GMT
ADD file:00f57642edc8479d50e6470a3509ad679eb9353761912deade33251fb3d9daa8 in / 
# Wed, 11 May 2022 01:22:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:53:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:53:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:53:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:06e39e28714dba08fe310ca1aafb43905427729ecf8e9586f811a7e5062fd09b`  
		Last Modified: Wed, 11 May 2022 01:28:34 GMT  
		Size: 45.4 MB (45428005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2141afc44a4cc9b8f9bd9ae1ad4ec8921fdf75b6be9b192b60f1b7f8469919`  
		Last Modified: Wed, 11 May 2022 02:00:35 GMT  
		Size: 11.3 MB (11302273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38533702160421fc5a777d84e162c51816a24426e58139f426e8156fef69d7a7`  
		Last Modified: Wed, 11 May 2022 02:00:34 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f25117aaebc0a8e2452e10a973f1d943fca50b033292ded9826449657fddba`  
		Last Modified: Wed, 11 May 2022 02:00:52 GMT  
		Size: 49.8 MB (49765289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ec954368d900e539ff706601ac4344546b5e9842493ce56abfe124c6af4c0a85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106625836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc5e079c5220207dd4f974b49b607232637719d2f9dbaa9deb0d38b7d71b9f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:55:33 GMT
ADD file:95b054735b431afab54d50818bab5058e711871345ec62ca3036290e76c5002c in / 
# Wed, 11 May 2022 00:55:34 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:20:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:21:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:342be1c547ac3ac45aaed473477b6660f99f4de775e90a96d72de9ed5e557bd3`  
		Last Modified: Wed, 11 May 2022 01:13:02 GMT  
		Size: 44.1 MB (44122855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df88622b0c311b347792d826c7a713552dc6a55e85f400a042412689194e21f4`  
		Last Modified: Wed, 11 May 2022 02:39:28 GMT  
		Size: 10.4 MB (10352440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96711fa1b3f2be5a438d1b5449ea06ee680fc89cbeb7d2d505be78919dba112c`  
		Last Modified: Wed, 11 May 2022 02:39:24 GMT  
		Size: 4.2 MB (4162115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fc8f701b22ecf646596cc0eda0ae31a65167c3fd54dce7465c864a72c9a390`  
		Last Modified: Wed, 11 May 2022 02:40:15 GMT  
		Size: 48.0 MB (47988426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5e26022dbe4f863f07b321e610dc7bd6522d5919983dded5da776f2c0e6573b9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102157850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91cafdceabb1b9854a74f5f2d3d7db29bbac92349847bc1f359030c428076c3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:54:33 GMT
ADD file:c679388ac7a37037465302aea3117354d9746d0c50c056e826b5c8c58aea5138 in / 
# Wed, 11 May 2022 01:54:34 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:33:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:33:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:629c5b996bdb9cea71f1d194d7a244d4aba271133bad4f5b88bfe38c4626349a`  
		Last Modified: Wed, 11 May 2022 02:11:17 GMT  
		Size: 42.2 MB (42151163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbf25ac5d0e3ca11a0fb961c2ac0f897f1982389c85b6e31ee0fa63a0293cc0`  
		Last Modified: Wed, 11 May 2022 03:55:11 GMT  
		Size: 10.0 MB (9956859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a3f9738e27d03b85306ba8927ec41f0ffd375d26fc501906f097e639a1047f`  
		Last Modified: Wed, 11 May 2022 03:55:08 GMT  
		Size: 3.9 MB (3921810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e17eeba6c7bc95de3a6d3399ff5b2580880dcdd7052a29dae70bb9f332a67b`  
		Last Modified: Wed, 11 May 2022 03:55:54 GMT  
		Size: 46.1 MB (46128018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:94dd38047ca6b06ba6663a42dec9c1e57aa1a7c128f5ac90909ba47cad907681
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105040325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bef8c66bd3f48da91f16dac58fe6b17a53b6d07667a8efae4cd917ffd14de2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:08 GMT
ADD file:8949016fba61b18207f5a2309fc974562080c5cc80d1eb82adb35c4fa03f6f05 in / 
# Wed, 11 May 2022 00:49:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:29:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:30:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:139065d8f4553df403babda56f830c32aa1f3e57f18d2145a3179468921a4bb8`  
		Last Modified: Wed, 11 May 2022 00:57:26 GMT  
		Size: 43.2 MB (43212478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0acfd1725613d968a54b7fbfe1f70f24b8a0dad792ad3cb28349035f7736fe`  
		Last Modified: Wed, 11 May 2022 01:39:24 GMT  
		Size: 10.2 MB (10217776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002c314192ef0350d2ac1d1e49b4fddbc49dbcdc609e56e0e2567ee2dd37f0bc`  
		Last Modified: Wed, 11 May 2022 01:39:24 GMT  
		Size: 3.9 MB (3874525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a0592b38ee1d873cc3681a7998f4ccbb2745e34ddf1d93c35a1d299949facb`  
		Last Modified: Wed, 11 May 2022 01:39:44 GMT  
		Size: 47.7 MB (47735546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fe583b5b1ed3c40e806e282814e689210f9408a87ab8a482556dfc085bb53be8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113120085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad491516c9d3bb83d820a30d54e3ab034c06f1a52ac4cdc1aac7bd2d5c96d540`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:50 GMT
ADD file:1a448f874e606582cb67d9369c97c83c78f2327fde8089b8cb6aaf476dc51935 in / 
# Sat, 28 May 2022 00:41:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:16:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:16:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 01:16:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99b3b0cea6c21e2e36bc4c198a72e5aa3b3ab76d26c2c63d9b0c2b0add554135`  
		Last Modified: Sat, 28 May 2022 00:50:28 GMT  
		Size: 46.2 MB (46150199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746cca76d5e15edabc23b8e1a62888ca87b80e71009098aab933b555891ba8af`  
		Last Modified: Sat, 28 May 2022 01:25:03 GMT  
		Size: 11.4 MB (11358709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a795692955c7b33f32b3c1a422a6d1bf8d2d10eea37afa9f414b5ccad00ad0`  
		Last Modified: Sat, 28 May 2022 01:25:00 GMT  
		Size: 4.3 MB (4342253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a4d58f49c17116aca3a038f7654a0f4635eef2069cd5a06232723448d9f23a`  
		Last Modified: Sat, 28 May 2022 01:25:21 GMT  
		Size: 51.3 MB (51268924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
