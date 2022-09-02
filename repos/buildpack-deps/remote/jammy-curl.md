## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:5172cc3839a41474139e50c1d84e15439b41fb3eff707528a28d47ba64f40f73
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
$ docker pull buildpack-deps@sha256:8b8f7edeac757b1a514d89c5f6e4082b9f64b1aeb87eeaa31da58dbe9e424ff6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37791656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d70c81850c25c6f5bf209fbcc9e0b2732e5456ebcaf907d4a139b4e73eb4e7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:27:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:28:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728cfcfa2f7739d87ae3efda60d01680593fcb2b55fdb5840721012c19335b9a`  
		Last Modified: Fri, 02 Sep 2022 02:38:25 GMT  
		Size: 3.8 MB (3804276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eda6154af3733cdc766a287039ebbd0d78265b3a7c64ed165045c8849ba1ce`  
		Last Modified: Fri, 02 Sep 2022 02:38:25 GMT  
		Size: 3.6 MB (3560674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4d5dd081b0038052e395515e2ca6703d1e57c62554368d3d2cb63687fab789ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34286694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6129cb72bf260d31e0bf82e24d1444ba54d6a83c741657ebeb73c543f11b6c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 06:08:32 GMT
ADD file:8b109e7521f26505639a07128de43f93636fcc05ecf26c6358f893f22df38acd in / 
# Fri, 02 Sep 2022 06:08:32 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 09:33:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 09:34:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:af25ea170fdc3ef953710312fcb7b9706eae0149cf05cd81c8281f1c511208bb`  
		Last Modified: Fri, 02 Sep 2022 06:10:34 GMT  
		Size: 27.0 MB (27016783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9398b18a454e124e1f9b5c08d3b8e75027704cf5d81734f403a4852babda0c9e`  
		Last Modified: Fri, 02 Sep 2022 09:42:10 GMT  
		Size: 3.6 MB (3556228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19d83ea0962e81d21c528b9d3bcf4646473a26fe96198cbc633813df2ce7583`  
		Last Modified: Fri, 02 Sep 2022 09:42:09 GMT  
		Size: 3.7 MB (3713683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0178fb33c3d226148c4bf4c01d1d7af7995549d4263e44af2da6673ef6604412
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35478581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ee4edf34b38bd4fb5d9c8d2833b2f34145eb1ba7fe01817cc0ea98024a9ce7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:51 GMT
ADD file:550e7da19f5f7cef52c6ea160a33daa482f44df086ddecffca8ec9be6385b848 in / 
# Fri, 02 Sep 2022 00:57:52 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:40:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:40:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:00f50047d6061c27e70588a5aab89adada756e87d782a6c6bd08b4139eb8ea10`  
		Last Modified: Fri, 02 Sep 2022 00:59:40 GMT  
		Size: 28.4 MB (28381340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5013832a9b04a455a3aed1888a43489d8850d9810b8d8fb64744bf814a1d9d`  
		Last Modified: Fri, 02 Sep 2022 04:47:52 GMT  
		Size: 3.8 MB (3776579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00e6a48d7146e6e81a25ce023cb7fb060f7cc202d4d5a9da4bc632e5ac4e05e`  
		Last Modified: Fri, 02 Sep 2022 04:47:52 GMT  
		Size: 3.3 MB (3320662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2d7d4ecc910fbb54f4d2d117583d3eaa890cab38b915d426f8af153408db23c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44231110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89808adffacf39aa02aa62ead292356f796d3ac914b396422ee1ddad9b1c31e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:50:09 GMT
ADD file:39b6fa94f6e1300a6fc4b6094e8250c22ecaa6e7c9f934841765d45b919402c5 in / 
# Thu, 01 Sep 2022 23:50:11 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:40:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:40:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:9ef77d5e46df05bf9f34e5871097fd038295a2aa5e29f1806ac3a96aa2545b5f`  
		Last Modified: Thu, 01 Sep 2022 23:52:34 GMT  
		Size: 35.7 MB (35721187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3136401182e4158ce50b7b80ede159c628447df84c97f8d16a1fdef5ca73f`  
		Last Modified: Fri, 02 Sep 2022 03:57:16 GMT  
		Size: 4.3 MB (4276033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed57522d1a954e636dbd623f4d22053a0339d16dbc9ce851739f5318e9fd3ad`  
		Last Modified: Fri, 02 Sep 2022 03:57:16 GMT  
		Size: 4.2 MB (4233890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:37a6e4bfff70a1d2f2343ec0bc7c5b663942e36f797247df635b8586266c5ce8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35138019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243eb39738059da136ec1fc770b105776ec3d66b623f2e08cb79cfb2b16709fc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:11:51 GMT
ADD file:8cff03722326c5e90e26ae259bde7ddd223c466edfd0d1cd6335b7b550f8156c in / 
# Fri, 02 Sep 2022 00:11:52 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 01:02:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 01:03:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f04a8971a8d913388890f40190f4d3935404b38efd860b235cf5d4de20959061`  
		Last Modified: Fri, 02 Sep 2022 00:29:20 GMT  
		Size: 27.7 MB (27744005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c893dcd3d9a55418817428155b89e044a2ebfddfa13d6945d70f0e2830099015`  
		Last Modified: Fri, 02 Sep 2022 01:49:29 GMT  
		Size: 3.6 MB (3615909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8351e367bac61d27e9f493ab2fdd756510203f5c595c3c81d6b96d2ac3214ca`  
		Last Modified: Fri, 02 Sep 2022 01:49:27 GMT  
		Size: 3.8 MB (3778105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6a7bc5b2496502a65bad30f7cb0b243ced4eed84af1897e94b98cbc971af9aa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35924452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59742e1d75395c6a6342d0534baf73e19ecec72302e69af41dbd4cf5ac64fe0c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 01:03:25 GMT
ADD file:aabc057fd7b1b1f9b4b729222b6dc90e98f846a65bfee1ee57cc899b6cee5a10 in / 
# Fri, 02 Sep 2022 01:03:28 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:07:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a32e6a15a6635185097921b9d08997d505b6b6500b6c142ad8e718d87c45ffad`  
		Last Modified: Fri, 02 Sep 2022 01:05:01 GMT  
		Size: 28.6 MB (28643161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba21c1eef45ab363d5dcc84511ca01cdbbe1e6dfdf54dcd8b108e256251e6e5`  
		Last Modified: Fri, 02 Sep 2022 02:16:20 GMT  
		Size: 3.8 MB (3809432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b26595dd670dde31a9dd83588e0dd3408a0d7f51791314f04652f5117a00332`  
		Last Modified: Fri, 02 Sep 2022 02:16:20 GMT  
		Size: 3.5 MB (3471859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
