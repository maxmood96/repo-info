## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:f615188c90f39add4187e8729a287ed25db35ec57ad8b6ac854095e524cceae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f64d7c7c876e05a4b673b90aeaf04a9190b09d24343b15df0553dd01850d5faa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39958217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fda97a5fc7c4ee68367eba22cb81dfc0f7b2fed18237d7e7085e924a61e7746`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 09:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 09:03:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9444ec2d0d74706e9f21c69197f72e2b34056bf07c22e6e0590eeee3746eb75`  
		Last Modified: Wed, 02 Feb 2022 09:36:51 GMT  
		Size: 7.8 MB (7770100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436645f1fdea29a9f32386c234f135e6e775cfbd947ef9430bacbf6e8a1198b1`  
		Last Modified: Wed, 02 Feb 2022 09:36:51 GMT  
		Size: 3.6 MB (3624018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a256c8e14b1ecc5f94e854bbeef30776e930ed5399b11bc31851e55498bf7964
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33931113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2202002a908e5892472f298e9d508936b4f779de3177434012872dc0da4f7a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:25:11 GMT
ADD file:0adc3f597b5ba8c31a9a4d67126166cf067749754e269fe2c3ed43f03457b53c in / 
# Wed, 02 Feb 2022 02:25:12 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:00:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:00:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:42bcffb5d2901aadaedc35f036cf725a537494a5869ae378ec427d313ff41fa6`  
		Last Modified: Wed, 02 Feb 2022 02:29:41 GMT  
		Size: 24.1 MB (24062751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb1391decbd1a7055950e38ea4664bf7847e08ebd8246eb35a44bde06bef523`  
		Last Modified: Wed, 02 Feb 2022 04:43:42 GMT  
		Size: 6.8 MB (6764294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dcf8a50b8a3e14e24ce52b8d84a93c0fbb1e1a8d04ab5ce912119fd30471d25`  
		Last Modified: Wed, 02 Feb 2022 04:43:40 GMT  
		Size: 3.1 MB (3104068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d3bd70b8eee89a5b4a2dd0bd32a840c4975484e41dbe0f2b3d4291ce9d54f370
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38192134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb036a6838462cd322904db7fc89af085d003c891a24c3a29b5a9ab31ba6ad8c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:02:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:04:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e1b3863fbf35e45c4d4d023a1da6ed1aa7aed5516f6fcd69ab2055b56ca492`  
		Last Modified: Wed, 02 Feb 2022 04:34:38 GMT  
		Size: 7.6 MB (7635857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c844ec18710dd62655a852e2ae8898653dd46e1a133b7a8ff3be2bb14d8a85`  
		Last Modified: Wed, 02 Feb 2022 04:34:39 GMT  
		Size: 3.4 MB (3386637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b9ebabfb556eceb9782f6ae52d9156a8f8bea0c411239a3001d18c54f64ead0c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46464947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313279ac25cdce34d2f885d179aacb992f3407387b02f2d858ff84caaa537c04`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:46:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:46:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a7fc330cc755f7ebf906b47323d539b71ccdbb042b5529cd78b8d6450efb40`  
		Last Modified: Wed, 02 Feb 2022 05:24:30 GMT  
		Size: 8.7 MB (8724123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0090b18678377f46ae9667ebae6c3279c4a144fbfef7f922e917917d3d409403`  
		Last Modified: Wed, 02 Feb 2022 05:24:26 GMT  
		Size: 4.5 MB (4456107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f47c714a7249b3493f3c3eaa8a798206e90fb5cffead794f415ff1bdba51e11f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34116556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae58ea5c108b0f4a6f9f568fb928db3a56963a46af830dcc2d2a0ad84f52772`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:15:02 GMT
ADD file:6e0c5699122e0452ab2b2424d34da73a6447915f9c47276d0841d180c21524a6 in / 
# Wed, 02 Feb 2022 02:15:04 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:08:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:09:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a6994ca4576c569732b8a1d88605f325f0b9e4f0f51119178c871a821b9b7407`  
		Last Modified: Wed, 02 Feb 2022 02:33:31 GMT  
		Size: 24.2 MB (24224781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88404836f7314d842380d17f5b6384d7aee27d583599d2f2896913ff943c2a2`  
		Last Modified: Wed, 02 Feb 2022 04:18:14 GMT  
		Size: 6.7 MB (6747229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1edc67a392956f5dd275386887c18265e492c079ce6579bc1282a71e01dba77`  
		Last Modified: Wed, 02 Feb 2022 04:18:09 GMT  
		Size: 3.1 MB (3144546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a2d667b9b45a9018c98b258a18eb746e01b1c7b5b249fffaf5a4022f0d40dfe2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38086739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decff9942d57eaa3c9f462bde8b27e595dcfc08c9a05de71be839dbe082ff886`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:08:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:08:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b0a766c6167afd65d583c5438dddcd9f873ea3775245759cd0304218aa0a91`  
		Last Modified: Wed, 02 Feb 2022 02:19:17 GMT  
		Size: 7.4 MB (7425844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef1757a6c6079edac24632aa0401d1d227238fbffa000315129e65d36b59738`  
		Last Modified: Wed, 02 Feb 2022 02:19:16 GMT  
		Size: 3.5 MB (3542158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
