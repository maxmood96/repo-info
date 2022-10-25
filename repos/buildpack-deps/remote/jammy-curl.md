## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:799e1c17f183d75a891c1e73695a852c768b68f7fcfbf3ca7c08bae21c3d8241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7f03939a1825e0b82b228c6a317a55a4b9c02b51dbbf1eb191ab33d0cda9216e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37792219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9cd9f7a916c169cff09707538fc5afc9772b268a10a2aa79bbc985d2756f4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:37:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:38:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5960f4cc2f4ee9a7344c315f226d539b57228b7cb255d5792b5269869d8263`  
		Last Modified: Tue, 25 Oct 2022 09:52:55 GMT  
		Size: 3.8 MB (3804701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8611d4a626ec9a284b2add0e552d72e6fd4898799678363fc7c66d6bca0a5a51`  
		Last Modified: Tue, 25 Oct 2022 09:52:55 GMT  
		Size: 3.6 MB (3561144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:89e3caec70fda990f819f3531875b9b314c843b4dd840be4234868015633048e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34286770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce49fd48b1ba4f7396facd63ca2177d567b41ea796aae1f686d42df955bc0e9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:57 GMT
ADD file:11e25fc4812528219464289700bb0495bf9298918899103c33d7ef9022690eb0 in / 
# Wed, 05 Oct 2022 00:13:57 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:44:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:45:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:99b9c73338a7c0dbe41f9fc543fae706650a616453e1e330f870e20916c18a11`  
		Last Modified: Wed, 05 Oct 2022 00:16:02 GMT  
		Size: 27.0 MB (27018632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c337b77409c2e34b5e69df73a11e0ef62cd00b8b23e7d6776235d6491726ac80`  
		Last Modified: Wed, 05 Oct 2022 01:00:37 GMT  
		Size: 3.6 MB (3555370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a1dc485f1a7e2433bb9a4501dac3fb4727fb7708715e743277a50ba4933ca1`  
		Last Modified: Wed, 05 Oct 2022 01:00:37 GMT  
		Size: 3.7 MB (3712768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cde36d71bbe4425cd9a8fb5d75a26f77d01d71b9e6d658f8784a56d78df99760
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35694165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a2b15ea2ec567cdf8db58cf77a502d8fe85f3a84932dc89b54aafc94a6d716`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:14:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:14:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c75d65daee139419e66b36968af1443c6839bbfa07f1ff10f41c14059531f8`  
		Last Modified: Tue, 25 Oct 2022 08:35:08 GMT  
		Size: 3.8 MB (3776223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b571e5291fabe657fef93ed4c8e7109c81e0538a58853a65f33d52b4aa5a9f`  
		Last Modified: Tue, 25 Oct 2022 08:35:08 GMT  
		Size: 3.5 MB (3535453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e149ccd1fd8c23ad674ee2e9cb1640264f96480646dce6134a50c9e1f1e2755a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44220306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1727c427b596139f4521abd4689b24bbfa286d1a6220a86f3a1705080d7778`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:26:00 GMT
ADD file:766b7743de4ed1a194fc749b7649d245b0cd545b03cc2c81f16a6c15e91c87e7 in / 
# Tue, 25 Oct 2022 03:26:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:33:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:33:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:aa33126e789290559dc146af02cbf168119ed23be1e30fd99fe8572956e50616`  
		Last Modified: Tue, 25 Oct 2022 03:28:08 GMT  
		Size: 35.7 MB (35709401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6373837e7f2a85c7283b43d7d1a07f2541140a0a6287dc704fdf1df6ed09c5e`  
		Last Modified: Tue, 25 Oct 2022 06:55:38 GMT  
		Size: 4.3 MB (4276445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847050f2ae34b2e1019b09f2bdbac09fd4a3c7efcaf4545aa162094c15b7f016`  
		Last Modified: Tue, 25 Oct 2022 06:55:38 GMT  
		Size: 4.2 MB (4234460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:674baad7923a60a55b6a139740aa1dd03ec351bca096cec8eef67d577490dce6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35123746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165bda599f3c7984f6273e3a5eccf5326245110c5394238add81f83ae779e6e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:14:15 GMT
ADD file:e1fa146cf8e97dd6a2f3ebb2dacba539556ef4a1e87dc53bd745a3cf0ba10aef in / 
# Wed, 05 Oct 2022 00:14:16 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:46:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:47:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:cbeff255552ba792be63b343113968df42de6f599d1372edd4c7346d08dfeace`  
		Last Modified: Wed, 05 Oct 2022 00:31:39 GMT  
		Size: 27.7 MB (27747416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6129e2d138d3d5141f87ef04090f82aeeb874b1d1e3c6f6e94d843cd2447826`  
		Last Modified: Wed, 05 Oct 2022 03:43:29 GMT  
		Size: 3.6 MB (3598134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a1ba2d60715be154c4f520ac4f1ef149f66b921651ab2726a809c14316e55a`  
		Last Modified: Wed, 05 Oct 2022 03:43:27 GMT  
		Size: 3.8 MB (3778196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c9f438fe30404f17ac10a8f79981bf6ab4f788d3706b23e99b92133fa1133a58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35924036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ac7d74d18b331d205348291551e18d9bd7010f18fc44d6f55875b60652fdf1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:21 GMT
ADD file:d9af7670f58e9478e400dac85a0fcb07a4209846dbd1ea560fdc6de6e2cb5e4e in / 
# Tue, 25 Oct 2022 01:23:22 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:40:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9aed974aece14dd3aed00810d58a89e87eb5be9ad1c6fbb1ed077dc3f145dccc`  
		Last Modified: Tue, 25 Oct 2022 01:24:48 GMT  
		Size: 28.6 MB (28641668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0474dffae2d1e16bb420718a81adc05c65e7cf46cfec815544e0ed630334ee45`  
		Last Modified: Tue, 25 Oct 2022 02:52:51 GMT  
		Size: 3.8 MB (3809925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdff4ace6c098f616aa6e4ddee394e5472cdf30f97f3b22e0dc26d42d42e234`  
		Last Modified: Tue, 25 Oct 2022 02:52:50 GMT  
		Size: 3.5 MB (3472443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
