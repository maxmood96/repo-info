## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:62ed259f94398c6303a7c6c21fa9328e1c9c31fa2be33cdee107c62f17ed48ed
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

### `buildpack-deps:testing-curl` - linux; amd64

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

### `buildpack-deps:testing-curl` - linux; arm variant v5

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

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:118cafd918a67b200ccd76ad2e1e398bcf62cd852f37b0da5a931bb157cd5640
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67554066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f06c5e8eeb995e91091f27855327aa695c5a175ce712579ee3ad2d10c8f44de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:58:11 GMT
ADD file:5e1c66e0b3334d725bfb0c7f0d2772c9781b78f01d54756b1924de7abe4abea1 in / 
# Tue, 12 Jul 2022 00:58:12 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 03:24:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 03:24:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:eb8579179b8f8463b05b790bf1566472700d70b08d50d0c6cbc776da788afbb7`  
		Last Modified: Tue, 12 Jul 2022 01:10:35 GMT  
		Size: 48.6 MB (48562934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5ec0a68470d880c05a2e75012ae47d36f57e8e96f491c963000d36a5bd0125`  
		Last Modified: Tue, 12 Jul 2022 03:47:36 GMT  
		Size: 8.4 MB (8405468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b47847e9c4da9d8e5006ac7d60da76d9bf81a4a5b77c355988cbc11285cdbff`  
		Last Modified: Tue, 12 Jul 2022 03:47:35 GMT  
		Size: 10.6 MB (10585664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

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

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6970bdc1ab100b6801de5c99f4eee88a0b4085665fdbd3e8fbf7777c3e6931b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74939557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5674817a9f71a508f198e6d2f1e0cb5bf9e859e47a78bea7595430d239db2402`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:38:44 GMT
ADD file:80ec0e35d6a4c162afe79f40617b47f846a2eb2065f245a230447609d1e7c001 in / 
# Tue, 12 Jul 2022 00:38:45 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 04:24:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 04:24:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ec7f9e3ed305349e742c012dcd142cce637ef3525759fea18f30c5987bf0e2fe`  
		Last Modified: Tue, 12 Jul 2022 00:44:03 GMT  
		Size: 54.0 MB (54004076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4070b35288ac278d35017570259c20c0599ff1459ee03a4492a44fedae6c68f2`  
		Last Modified: Tue, 12 Jul 2022 04:34:48 GMT  
		Size: 9.5 MB (9465776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001cac3991e538096035178065ed3abbfbbd6211f5e8284e24b2095d4e30a6a8`  
		Last Modified: Tue, 12 Jul 2022 04:34:48 GMT  
		Size: 11.5 MB (11469705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

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

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fe7ffcf42b3261a01fffab708692fce02e8832d3cca1e2f14dd619b2c2ef4b1a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79203336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73d02982bac352123ef05283173c0f0cbd156cd2cbabde9a9bc2b69d4e20267`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:24:07 GMT
ADD file:ae1b00e1c53ca0bbd56262f1d2cd742362c7a02eed6214e944b4b4762dda64ff in / 
# Tue, 12 Jul 2022 01:24:11 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 04:13:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 04:14:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8000c6ba1eb02ffb5f03a6b7e7d8f71a864844286f05cb8516ff71014b1cb870`  
		Last Modified: Tue, 12 Jul 2022 01:33:34 GMT  
		Size: 57.2 MB (57237580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0782d166af094f9f70aa8698ba46b6b5692ac871684dc297ee170414ff26f289`  
		Last Modified: Tue, 12 Jul 2022 05:01:04 GMT  
		Size: 9.9 MB (9883912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f130ed867b07b81083e091fe4e20e6b2d5f84eff9836462c4c27d683d698d1f`  
		Last Modified: Tue, 12 Jul 2022 05:01:04 GMT  
		Size: 12.1 MB (12081844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

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
