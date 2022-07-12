## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:56121a26b78f4b15137b9da0c334dd3b9f639d262051f1e136105799561666f6
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7f672cb94a21b691b5622eceee7146ff9d63c09cf9b9a615468cda4982bce031
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73586402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52a3576a74b27fbdc9ee30a6d3bcd8a47de0d620783f4f3237a349f712bf5f7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:19:34 GMT
ADD file:e413c7d61ecdc96ab067e1f8bff6ce03c792c94b9d1f54e80cf633052c5d975a in / 
# Tue, 12 Jul 2022 01:19:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:46:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7c7a32fcf1e30b18b7a9a032acf892763291bef7159859a35297bf81217bbee4`  
		Last Modified: Tue, 12 Jul 2022 01:23:29 GMT  
		Size: 53.0 MB (53022393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00146b6ba9670f0b5362fb1ea6716d934ae0d1545d85efb6e7d9871f449ed7f`  
		Last Modified: Tue, 12 Jul 2022 02:53:57 GMT  
		Size: 9.3 MB (9292245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed5201b04ed0ec80bf5f970e6e10f4e241d58bfbeff69ec15faa4c6a34f01b6`  
		Last Modified: Tue, 12 Jul 2022 02:53:57 GMT  
		Size: 11.3 MB (11271764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e102c8175db9e940a2f314c870c4ad9721d38bcb78562236ec5b0f46f690f0d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70487955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5990cd30edcf6798ed6dad6deccd86ce57b88a9316da67967ce35a05272fbf76`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:48:59 GMT
ADD file:211648cfc211d73b6facf8b4f6762e1b45f5894d43880d7bf0a7822be746ad58 in / 
# Tue, 12 Jul 2022 00:49:00 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:33:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 01:34:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e06063f979dbe8242191c248c95f1840e27b65404e59a60f54bfc1575fabed87`  
		Last Modified: Tue, 12 Jul 2022 01:00:53 GMT  
		Size: 50.8 MB (50821602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc41e44fbad79261bf0a50b7500c64ccd7e7f8b3209de9bb0165c595e95914f3`  
		Last Modified: Tue, 12 Jul 2022 01:54:32 GMT  
		Size: 8.7 MB (8725587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac530a424b46c790de63a633c7ffebf87465fa20a427e8389d6bcaf6ae81028a`  
		Last Modified: Tue, 12 Jul 2022 01:54:33 GMT  
		Size: 10.9 MB (10940766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cec99b356856c9867b8814f565bb3eed4778ed225c2aa632a14ba17fb356050d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67476367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecade07de1a96c6f49299b77a358afd85fbdfdb208a95a9e7f39eca06c89a5b1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:58:08 GMT
ADD file:485670bbc3d21c74d06e079229d1c74d05970c4bdf8c5d25692ab1464f0acfce in / 
# Thu, 23 Jun 2022 00:58:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:42:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:42:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:da5c76d2fa54760a1e859c83968ea6d7dfee1c43064fb6f34c27f8d639859b07`  
		Last Modified: Thu, 23 Jun 2022 01:13:19 GMT  
		Size: 48.5 MB (48506514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231adce49f6a983a4cfa3f3683a6c276af5ef432ea37e705272135b3a56084b1`  
		Last Modified: Thu, 23 Jun 2022 02:10:23 GMT  
		Size: 8.4 MB (8397133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8487327d153dbcbea96feb013bca9efcd1fa6319396003a967515da5f4ab1d6a`  
		Last Modified: Thu, 23 Jun 2022 02:10:23 GMT  
		Size: 10.6 MB (10572720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:76765d24e1a88b8ea01779c253df01b952c3eb7da98866bd3d3be38685b56b0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72319163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e101ec5fbde3de51bfdb7fcc486ce8cae1ffe0f7f97054c5a852a43c11c83d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:39:53 GMT
ADD file:56a82a6c91d29741aef57453822e5502a13bd7841a1b3c8936a6f7b5c0b80bb6 in / 
# Tue, 12 Jul 2022 00:39:55 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:31:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:31:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:73d3feb17dc47282a9451cf8832ac9c5a707630877cc6c832d9f5cf4d3e2d202`  
		Last Modified: Tue, 12 Jul 2022 00:45:00 GMT  
		Size: 52.1 MB (52128620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3f77295745c94527eef3df84e5f089d7404a40e8f243f00fb8ede9cd04cda4`  
		Last Modified: Tue, 12 Jul 2022 02:41:22 GMT  
		Size: 9.1 MB (9132573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22eb759abcb3de672cf64ccea22ebac1e035560b83ba8bbbd82b3c274ccbbf9e`  
		Last Modified: Tue, 12 Jul 2022 02:41:22 GMT  
		Size: 11.1 MB (11057970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:65cf46d760f73749c7674db469da8436e0de488df7fd77368da8d6046d635cfe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74892536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b856c9b31c533e0b1f9d5b60b96fbb7daebbdb6ec5368fa60d7896aaac101f32`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:38:52 GMT
ADD file:d8108af9af2f3fb7f3dd905a9b4dd8391d568ba8dd590a9ca2bbeecd44354e03 in / 
# Thu, 23 Jun 2022 00:38:54 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:08:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:08:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0120d80f9ec3d96114e34087bd467cf9989c9c723cf7622bb16fb3675443565c`  
		Last Modified: Thu, 23 Jun 2022 00:45:18 GMT  
		Size: 54.0 MB (53963635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a0c1f242a443b42292f09b23bf00a038a40230b125f2d832ff706e0b0fd009`  
		Last Modified: Thu, 23 Jun 2022 01:21:05 GMT  
		Size: 9.5 MB (9464738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d2c7e9a858ffdd4f52faf3fc1e4e080485c9024f299858237d4b3961f4e27d`  
		Last Modified: Thu, 23 Jun 2022 01:21:05 GMT  
		Size: 11.5 MB (11464163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:40c37bc6cdf6cddfb29a76ef7e74ad2f1187f868292f0062b9255023b25adbd5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71766462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e24a8cf4b182495fa008fa59c75741eb00eec064cace5d891954e37258a4987`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:08:42 GMT
ADD file:8bc6b496d7debb22306bce782f6b34ee75efae7151dc19314b45a9751b8fbdb4 in / 
# Thu, 23 Jun 2022 01:08:47 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:44:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:44:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:25ef8061366d5e6abd7ca324b8c1f08ba96be6bd0e55fd310e046a1e4becfdb6`  
		Last Modified: Thu, 23 Jun 2022 01:18:17 GMT  
		Size: 52.1 MB (52089294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8d0efe31fb7f6ccd1d5334126a57a6651ed1009e9a6eb93f4fb51019078cf1`  
		Last Modified: Thu, 23 Jun 2022 02:16:45 GMT  
		Size: 8.7 MB (8657797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d342e8e78e8778dab632125fd70a05b026d9c29cfed07832f8527747409a8a67`  
		Last Modified: Thu, 23 Jun 2022 02:16:45 GMT  
		Size: 11.0 MB (11019371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e1944d3105905a9346fc89b32171c042ce5ddde9160ae5c968b06b747b690553
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79146572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab721b3b86bee7065c7a4c4ba25785bb41a6cfd197e38169fbde7626e2c431f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:00:58 GMT
ADD file:d857864fffea40faaeec8c9492ef1805e6c891ebf06f1427f02398a3824debce in / 
# Thu, 23 Jun 2022 02:01:01 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 03:43:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 03:43:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8afb6214160c68cb540431e94c7bfe898f1a094dc45a834aa07634d34b1505a3`  
		Last Modified: Thu, 23 Jun 2022 02:12:13 GMT  
		Size: 57.2 MB (57198049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a70dd21016ae34b7615f4f27bc039c2c609a2ac123e43b625424da683ee24b3`  
		Last Modified: Thu, 23 Jun 2022 04:54:13 GMT  
		Size: 9.9 MB (9883483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb14a4d02ea4ebe3ab1ddfc7a7bfdc8945f0478c8c9592495931e4a0a21b69d`  
		Last Modified: Thu, 23 Jun 2022 04:54:12 GMT  
		Size: 12.1 MB (12065040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:23d7545e6602fe8443607b9d32a9b3a9decc2f89a0af1239732d5fd1ed391b71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71655983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9359b5dead00a52de8c2035125d1623990f3c10c2b0cff55e4da228ab68b7c49`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:42:21 GMT
ADD file:affba659885c7b0f365e0fe6df963322452d3a11e8c5d1f1d1908cadb57c33eb in / 
# Tue, 12 Jul 2022 00:42:27 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:35:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4819cb6cd77746b912d22ae402922254d55d38be97967a6c3851624256c8a8cb`  
		Last Modified: Tue, 12 Jul 2022 00:52:08 GMT  
		Size: 51.6 MB (51554170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167df8c8442dcbc38170fd2782ed9a5c4e450b990c5d3f5bc8f1e960393fe12b`  
		Last Modified: Tue, 12 Jul 2022 02:52:43 GMT  
		Size: 8.9 MB (8939224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca0453a18e7c0e72daadbe03c9a6c56fb34dc6db87af258b576918425f6bbef`  
		Last Modified: Tue, 12 Jul 2022 02:52:44 GMT  
		Size: 11.2 MB (11162589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
