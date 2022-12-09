## `buildpack-deps:bionic-curl`

```console
$ docker pull buildpack-deps@sha256:010fb6ed10396e79a8ce82e3c8e9eb8215ff641785c83f354ac98c45d51d1902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d7f986fa128b7343d47cc564183bc60b6f7ca2fbda644bc0370383208639dc95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36370058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc21d1041d388a5a3976933be2f4e2f4eccf0338a6cd859a9e84d54797a480f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:28:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:29:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e18f180575203448b74fb16d0aec6cc8a6fe99dcdc405bf34bb0fea2f50b543`  
		Last Modified: Tue, 25 Oct 2022 09:50:57 GMT  
		Size: 6.6 MB (6631430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57415bf5e01e168396fa8d1481f967bf0db7da30f9dadc895853e4f14722ca6`  
		Last Modified: Tue, 25 Oct 2022 09:50:57 GMT  
		Size: 3.0 MB (3026128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:da3fee7ecd0b9a840cffbddd49c691b3dfcb72782986bd71117c1fa35dd23cd3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30590146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7b78813be49a25f18a8d4e6e7ba4d21f495573086ec6e7607251e6fff19207`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:06:51 GMT
ADD file:577e89b09dccbe472d77fc02945d56a9eac3a24e20bf618c45074becfa1f49c9 in / 
# Tue, 25 Oct 2022 03:06:52 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:41:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:42:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8cba8250122e011a113a9792b4a631b34b2aa89453e4c04090586d85464707de`  
		Last Modified: Tue, 25 Oct 2022 03:09:09 GMT  
		Size: 22.3 MB (22306283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d8b28205a8881b06da3fd9837aa6ec99179704ef880cc467c7cb0283cb11ce`  
		Last Modified: Wed, 26 Oct 2022 05:14:35 GMT  
		Size: 5.7 MB (5697803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae047a655c1e91f0677ae08f78767ba8fc59a73a355ea6fb2aaa626796d41a7`  
		Last Modified: Wed, 26 Oct 2022 05:14:35 GMT  
		Size: 2.6 MB (2586060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4a7fb4ce2c117e99998cdeef7a19e67cc71055fe3a3e73e8aa9c33ffb9c67d3b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32601440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed643d0aed22b28551913f89b4c72639e5b8faaae70ba0f4501439d38584433`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:56 GMT
ADD file:585011162da73734395f2ef251ad89b72cfed0101c7da2435fac55061f99b516 in / 
# Tue, 25 Oct 2022 05:54:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:03:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:04:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a217cb16e35b382d60a7ab454a8c4db0fbe5e0aeec4b4c346e51eb1e77d34f8c`  
		Last Modified: Tue, 25 Oct 2022 05:55:45 GMT  
		Size: 23.7 MB (23735856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296237f400b08de0ee2566d1d70f0c0fa8e7334ec80823903e2aaf4904c5a49d`  
		Last Modified: Tue, 25 Oct 2022 08:33:20 GMT  
		Size: 6.1 MB (6074795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82de00773434d5186afe917dba4d4a8e731ffb220b4b8b348628c4df9f9e773e`  
		Last Modified: Tue, 25 Oct 2022 08:33:20 GMT  
		Size: 2.8 MB (2790789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a2cae6fb6300c358fda09a3a24258b62b5cf7fba252ccb64391d4b3b6ef08789
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37111835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2201d0aeb4456515a277177161a155873673beef8c586afbb6e453e8a5214fe7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:38:59 GMT
ADD file:ab7098cc4395f87660bf4fef944711c4eae43c22aa2627b09681883a0aeab718 in / 
# Fri, 09 Dec 2022 01:38:59 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:56:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:56:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:7e26b56c479a64877378342636b3b7f2659b9c6a8d68475ff70fb0ba3d5f3ca1`  
		Last Modified: Fri, 09 Dec 2022 01:39:36 GMT  
		Size: 27.2 MB (27165403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74375ec595676a71d010f4d83e5754d4df6b30c689349382cbd3aa19e12b495`  
		Last Modified: Fri, 09 Dec 2022 02:02:35 GMT  
		Size: 6.9 MB (6904390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21556d1054f953a7d355c04af5869d8206ffc7ad3886b4f87a832ca847c4bbb3`  
		Last Modified: Fri, 09 Dec 2022 02:02:35 GMT  
		Size: 3.0 MB (3042042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:45c832bf6c3088da7c40d8e5205cdf1f8357326d9ad8840ddc61343237447345
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41234896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a774524b743b63f11381672077399dd0cdf35bb59695140dc3f5f7e3b3f523b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:34 GMT
ADD file:254e11be9bc865d645aba7c16a39a04f5ce227b7aa4280f7a42baec47b0c6ee0 in / 
# Tue, 25 Oct 2022 03:25:36 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:21:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:21b8f46bc1957ff60412d81678134500cf7a4f0e7f198ba384fedb2e5747d847`  
		Last Modified: Tue, 25 Oct 2022 03:27:21 GMT  
		Size: 30.4 MB (30443225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7a73c0177bc0907d9770e0863fb7f6949a870d385b401421a0817a32cd56be`  
		Last Modified: Tue, 25 Oct 2022 06:52:33 GMT  
		Size: 7.1 MB (7051025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f82d4b01549cae8ea6c3b7e9f210d370b148dd8004af19925715e43994e9ff`  
		Last Modified: Tue, 25 Oct 2022 06:52:32 GMT  
		Size: 3.7 MB (3740646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:171c50890d275551e068fbc231b063d10c68d4f76bb5c113b55893fd0c094898
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34674453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23932295597dc4628240979d04d45ef0bac7ff6e5a0e864ddec4d112b2aa2143`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:02 GMT
ADD file:0843e89b8865a30626cece7a42cf27708a86422aadb28029168b2f159a8768fa in / 
# Tue, 25 Oct 2022 01:23:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:34:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:34:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4cd692a206d359f66e10c4f4f2a37009c4162f022df78a9bb8e8c24def290167`  
		Last Modified: Tue, 25 Oct 2022 01:24:23 GMT  
		Size: 25.4 MB (25371461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1872edbfc35ad376faca8b8da8bfdde0ac95f27652b1188c2036672466ab8233`  
		Last Modified: Tue, 25 Oct 2022 02:51:21 GMT  
		Size: 6.3 MB (6326364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dda90dab707bb33111b66abdc094ed182c70b7a83b6844b6b316ba93a0f779`  
		Last Modified: Tue, 25 Oct 2022 02:51:21 GMT  
		Size: 3.0 MB (2976628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
