## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:1c8b45b39624aac9d3acbdd1454c04311424ab3c2e19327b322d91971e5a733c
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

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1a8ab047a7f353eb4e798fd15fda6464fc5db480fa686bf572258452dcf307ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129792726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99133d70a8e03745e8bb5a2a08bbc57b90e419f26c67dc1ae399ea34ab6db678`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:19:44 GMT
ADD file:daaac4875b34dee73ff062c17a4763b2cf5726753df4e9700bbcefa0f88153e6 in / 
# Wed, 11 May 2022 01:19:45 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:47:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:47:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:47:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d68396ae84f0ca729923a79943893f43492725d77e7b329170777a2bdbb6752b`  
		Last Modified: Wed, 11 May 2022 01:24:08 GMT  
		Size: 52.9 MB (52944400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f77feabfdca5ac1aeded64e65a1943aee6d39af1ab6f3081de4bdd78eb986f`  
		Last Modified: Wed, 11 May 2022 01:56:13 GMT  
		Size: 8.0 MB (7999176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ce0f5a715fdcaa40b523d43006725581030728153a1a16199ef5a3097bd43`  
		Last Modified: Wed, 11 May 2022 01:56:13 GMT  
		Size: 11.3 MB (11264369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834bb0724f857ac407fe281ac6fe1866c2b96d1b631ba15110494e2454e36422`  
		Last Modified: Wed, 11 May 2022 01:56:32 GMT  
		Size: 57.6 MB (57584781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:60fc62babde0f386230f41cf7de9ae275c479609e03c867aa2586be32a253380
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124374767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d0543d7bf8e29ce2442a5e78e1baea7f337eaf28884a429def59f220a6c004`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:02 GMT
ADD file:14b16b308b28ed8604a9f98d47e92522f709988224084eb5d2dfd30d3511e4a4 in / 
# Wed, 11 May 2022 00:49:03 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:01:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:02:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0baf2800ae4e68af843862199b558f14eac2766cea5651c0837cbd8ee827981f`  
		Last Modified: Wed, 11 May 2022 01:03:42 GMT  
		Size: 50.7 MB (50737437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1cacfec2c73325f6ee9727f3ee99a764a10620c61e467c786773e82fac2589`  
		Last Modified: Wed, 11 May 2022 02:26:52 GMT  
		Size: 7.5 MB (7536108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a878bece2839158834198a327d030c397685382713b32bee43b9de34889dc`  
		Last Modified: Wed, 11 May 2022 02:26:52 GMT  
		Size: 10.9 MB (10927476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222936f7ad04c2a63502712adf47f0d5e8415536d3b0815b84016fc8a214d3bc`  
		Last Modified: Wed, 11 May 2022 02:27:43 GMT  
		Size: 55.2 MB (55173746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:371f053741254d942ade0872686c5bb017dfc01443baa5a3169d0d3e5ecb5ef0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119858581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a5a020207e67a1535b4185623647fad9a8affd4badb4c013e4a9b7f6d99c73`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:47:29 GMT
ADD file:ae0b1a579333a3c7912430243fe91f71f32d0e234d52667dd937f7cd23a8d3d2 in / 
# Wed, 11 May 2022 01:47:30 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:18:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:19:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1fdc9e441250146f7b7c78b0264138dc69a0b46d264373157ac1c2cdba7a552d`  
		Last Modified: Wed, 11 May 2022 02:02:37 GMT  
		Size: 48.5 MB (48475916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb8d2e8ff6478f1fc3388064baa5d6e059276c7a093a627bc6dc36d79ed4107`  
		Last Modified: Wed, 11 May 2022 03:43:50 GMT  
		Size: 7.3 MB (7269457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864281f702c002b286df6a1ef302fe0c7cde6323a4e78ec43b18718d930be2b8`  
		Last Modified: Wed, 11 May 2022 03:43:51 GMT  
		Size: 10.9 MB (10933463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f541bea22fba3f321a2207e36d3b3f6d26f89a61dabbd9a1305ed9b9938b15f`  
		Last Modified: Wed, 11 May 2022 03:44:37 GMT  
		Size: 53.2 MB (53179745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0cb81665185969897ff9cfff0c25a786974ac90b50dd0acffaa70f80ea1102e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128542038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae6f9ce600ff58247080926e9e11b0c5c92941a08374e34a4678cf9c186b015`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:46:19 GMT
ADD file:a50b6ecf9ed84e6e3bb43f96fd036c7ebaad7f94df16c3637d6dd19a6dc91701 in / 
# Wed, 11 May 2022 00:46:20 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:23:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:23:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45306f5029ed7ce5685e65dccfaecf3f4a79040520f3ffb65eac76781218fea1`  
		Last Modified: Wed, 11 May 2022 00:52:36 GMT  
		Size: 52.0 MB (52041343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5de1fe22d36e48b637912dbd432cf236f1d956231296b275af61bc5cc951b1a`  
		Last Modified: Wed, 11 May 2022 01:34:36 GMT  
		Size: 7.9 MB (7853647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f57f959274f20ecbbfac9d0dd7e9dcbbc904e7eaf49a4ff37e3149afcbb2247`  
		Last Modified: Wed, 11 May 2022 01:34:37 GMT  
		Size: 11.0 MB (11041680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ec64d54ab363857036338cc3377146eb8961f5b02e14d7ea1b925353b370d6`  
		Last Modified: Wed, 11 May 2022 01:34:57 GMT  
		Size: 57.6 MB (57605368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0facb667030f056b56d5ec0f20138666ea4d9afbcc3a2290bae1ed4c549db899
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132581486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fc36136411b36061fb8c3db105d455b75b670d3c0c1d9f0ff073d1183c759a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:38:49 GMT
ADD file:ba6ab6618a6fab6f0a1d80573b329e26b602c060d940b76c1774ddab96982cd9 in / 
# Sat, 28 May 2022 00:38:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:08:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:08:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 01:09:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1098d76e3f40923a061abc8c2e6697409b0a2428eab6f37ae394a7b491b1cad`  
		Last Modified: Sat, 28 May 2022 00:45:27 GMT  
		Size: 53.9 MB (53948486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052560f7b1294898c71f369cf5ba0727eeecd6b6ba0e30c151347d6333c1f5e7`  
		Last Modified: Sat, 28 May 2022 01:20:08 GMT  
		Size: 8.2 MB (8176480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee8b2d3f9aaae772a2ef7c3c5860d032dcd57b82cbaba04dcf2e741bf9b5895`  
		Last Modified: Sat, 28 May 2022 01:20:08 GMT  
		Size: 11.5 MB (11464416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe8878cdce718f0b7deab1bba8c2471c5e61e909f442fce25f4d619d2ab8be`  
		Last Modified: Sat, 28 May 2022 01:20:31 GMT  
		Size: 59.0 MB (58992104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:013f889790d13ea10162a286705d33385f2dbdf64d6278b44ba91d79409639c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127046586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27c6d348c4b0b44a4f2127a433f2bf379980d63027a083590699d97cea86b1f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:21:42 GMT
ADD file:023ba5f785e781bda7875c3b4c2f163666fe7b1a6a0fde74103b7799380a55c3 in / 
# Wed, 11 May 2022 02:21:47 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:58:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:59:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:01:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1315838dc3fae911b53ad8b9fdb88cdc4a2988e4a4924922837b71b52b18d1fa`  
		Last Modified: Wed, 11 May 2022 02:31:44 GMT  
		Size: 52.1 MB (52066926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2722654f4b60f68f8cf6d835f62f8bbadd36e2eae5b31ec1b4cd273785fa9368`  
		Last Modified: Wed, 11 May 2022 03:34:01 GMT  
		Size: 7.5 MB (7508574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4489d5ecab6698b42b344d5e72df6f74ea21c3b4a125cdee3c103f8e742b642`  
		Last Modified: Wed, 11 May 2022 03:34:02 GMT  
		Size: 11.2 MB (11158255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91735533194b8e27b334d10d7d19e1b7008ace8c9d32869cdf24a530fcd6226`  
		Last Modified: Wed, 11 May 2022 03:34:50 GMT  
		Size: 56.3 MB (56312831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:35093ccb72c291496f9d5197e2b961078fd8debb8b3142017c964d4d88159207
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140020470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf5bda7e72d2939a31926068dc95746f01346cda0893c4fb2541af61f977073`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:30:46 GMT
ADD file:151ed5fad83d0b4f27c9bb34e41c649df7b7b9cbe789e3036c44d12cf1f53a71 in / 
# Wed, 11 May 2022 01:30:51 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:07:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:08:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:11:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:49991d23fb52aaf7937c711b0196364a5011e41402f3ea986702027fadd27e0e`  
		Last Modified: Wed, 11 May 2022 01:41:30 GMT  
		Size: 57.2 MB (57150441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac162b59dc7eb516878ceab4828d006f42ec802f1755cbd5bc3126bf8d03c9e`  
		Last Modified: Wed, 11 May 2022 03:46:29 GMT  
		Size: 8.5 MB (8496430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f4172550a38e5e5676e20f279186dcd1ebf123a9b2693d032e98814590d62a`  
		Last Modified: Wed, 11 May 2022 03:46:29 GMT  
		Size: 12.1 MB (12065559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b1c75bb53e1b4ca0c91d2d1a0d8344e323b723c6a10f2b51bb99bb0cd6f948`  
		Last Modified: Wed, 11 May 2022 03:46:59 GMT  
		Size: 62.3 MB (62308040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1405b4bf7635499493c069de60ab8304cfe51316dadc3c6f7b95c9d42e1da659
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127194662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c360a573465fef70ded115ffcde13e25c588fda2c667486015b0421084779d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:43:27 GMT
ADD file:d38e77e014746a6349342f7d1cb5eada86f6e06423bf095efa6f182b4d038b77 in / 
# Wed, 11 May 2022 00:43:31 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:13:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:13:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:13:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b3467d807091357239fe13d54d3572c25afe85ac06c182eba9268af6bac8f48a`  
		Last Modified: Wed, 11 May 2022 00:49:13 GMT  
		Size: 51.5 MB (51483972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100136ea0fb238c9c9013ef4e514f31fc2bf960000bae26e543ca80d01ae2e12`  
		Last Modified: Wed, 11 May 2022 01:23:52 GMT  
		Size: 7.7 MB (7662307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d34880cfc5b88a3b84c6d27165e8e6e19b4a2668efdb3f9e2b27a5422d12f2`  
		Last Modified: Wed, 11 May 2022 01:23:52 GMT  
		Size: 11.2 MB (11157530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841cf490c32295ead18a8dee0de5c5b2a8c16ae6170f41a3f6b9686186269c5b`  
		Last Modified: Wed, 11 May 2022 01:24:06 GMT  
		Size: 56.9 MB (56890853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
