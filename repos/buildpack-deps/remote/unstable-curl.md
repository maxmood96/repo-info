## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:6185be1b4e38d9e00532be35d15e2e3d2a4586adfa9cade80ad3355d26b917e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:17d5f19cb2f75712e579d4bbaf4dd688d7f48d3174a26217533df8289934aad1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69795449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ef9136713b641beebf227dd0d1f6c4067ddb04b3877e71c275fb7c90d1c1bd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:31:25 GMT
ADD file:8efef3fd1e16c5994e0b27af5c19056cc369818d299aaf62b89b89ad82426fe3 in / 
# Thu, 23 Mar 2023 01:31:25 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:04:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:05:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:ddb08f6d450933d22f98a93a56726ec0491dcd496caf4455cfe7066900409348`  
		Last Modified: Thu, 23 Mar 2023 01:35:52 GMT  
		Size: 49.3 MB (49291637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b67c216879c602a3357a3e051406068e953242d0d7b402dd7e6671d414199c7`  
		Last Modified: Thu, 23 Mar 2023 06:09:55 GMT  
		Size: 9.1 MB (9081298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184c8a28afd4da0484a1f9c3cc7e52748726daac5cac85bc0fc702f666f1939e`  
		Last Modified: Thu, 23 Mar 2023 06:09:56 GMT  
		Size: 11.4 MB (11422514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b130af12e26d3c5dbafb04dcbcf75f0e751bb8327318a85a088aa317ab591e69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67673709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa3339472cc907f434562326764e3c0a37312ea0c737ab2fe67f577e10abf020`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:49:01 GMT
ADD file:4fadb88d3ead8d91349c79d7e903bbb8f6130b292bda6cb8099131210a815bc1 in / 
# Wed, 01 Mar 2023 01:49:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:21:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:21:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a03e1abdb2ebe924d64faf35eb6563891039999ec54a62f65419caf539ba6a88`  
		Last Modified: Wed, 01 Mar 2023 01:53:21 GMT  
		Size: 48.1 MB (48107781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d446d9cfc1201a906803d21a6e36423e22e9bebf24cf64bd16a4a3a73af61a2`  
		Last Modified: Wed, 01 Mar 2023 02:26:11 GMT  
		Size: 8.5 MB (8514426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dc22595c5f06cd6d232ff8a3594b9aadef31095cb355dffad2b48a861717bf`  
		Last Modified: Wed, 01 Mar 2023 02:26:11 GMT  
		Size: 11.1 MB (11051502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f45638145f3049bdd8569f5e3e37f9012b169c009beecbf423abcfede1b90b6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64783911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfccb40ab0d880192527f3c9058b284e721f369d3a6a86d097ac545f40dc846c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:28:43 GMT
ADD file:628ac1300ca273dba23c7d617164bc6e664cdebb4106910020d7b3dcb39429c8 in / 
# Thu, 23 Mar 2023 01:28:43 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:42:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:42:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:53d7f1f008e91cd29c47c933b404c16fc1d4cf64b8699ad1269e882f53ca6e2d`  
		Last Modified: Thu, 23 Mar 2023 01:34:10 GMT  
		Size: 45.9 MB (45911196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61016f9e9c2f44cda61da9f54267fbafe7fef3695caec3c87c6d5ae9eb452ae4`  
		Last Modified: Thu, 23 Mar 2023 12:46:05 GMT  
		Size: 8.2 MB (8168245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4226b16c6b7093dc765001b6e5615e8150c8d19be6c96ea1171e1ad13654f5`  
		Last Modified: Thu, 23 Mar 2023 12:46:04 GMT  
		Size: 10.7 MB (10704470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d849bed703600c57a5cf46b9d6dee8db2b6fbec05610ff4f7b339ad75cac0ab6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69621832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13631a3a6f5857416ec5f0f2843c3e555733cdbe82a7417b1bf99e8a24cf5e23`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:42 GMT
ADD file:56248f74ca6cf497dee2c80a5824447bf5ee5e730a9c092f440d9c666ec1c076 in / 
# Thu, 23 Mar 2023 00:45:43 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:14:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:14:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:3a84baeeebe4b5ede833105ba5c2fe8b6102a8c47c386cc79b5833fea9489c99`  
		Last Modified: Thu, 23 Mar 2023 00:49:34 GMT  
		Size: 49.3 MB (49318983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0d42af9a92d82ccbe90040ec3d71455dfd1d92426d7f302766baf42eb07f8b`  
		Last Modified: Thu, 23 Mar 2023 07:18:50 GMT  
		Size: 8.9 MB (8914256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb28b2a98fb7b8844969dec5b68c7cfa2df0d77f1ab1a55bbfac387493184004`  
		Last Modified: Thu, 23 Mar 2023 07:18:50 GMT  
		Size: 11.4 MB (11388593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:96efd45cce16d1abf5f45addfab9763443a1b133191ddc775466b38cc35f4bfc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71402074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04375e26c4498505d17b88588c8323cb1b7fbf8da0e0d2a17878602b6fdd7c17`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:40:10 GMT
ADD file:b6719d98d83dc3affc1d45dd9bc533456f19b9fbedf5369cde4c632f24f6146c in / 
# Thu, 23 Mar 2023 00:40:11 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:49:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:50:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1dab6ed4b4dcc22cec1b58fa38e2c22941443603bb1cb3a1f4025cca4556556b`  
		Last Modified: Thu, 23 Mar 2023 00:44:54 GMT  
		Size: 50.3 MB (50314549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693b9d83c0fac98a0803452b66e1b3479deb5c3bf2327160262a3795816c2626`  
		Last Modified: Thu, 23 Mar 2023 13:55:40 GMT  
		Size: 9.3 MB (9261739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1b6a0d96c4a9175530cdacdc798d12c89c8a0fcb3e61704e44e229b4d6db16`  
		Last Modified: Thu, 23 Mar 2023 13:55:42 GMT  
		Size: 11.8 MB (11825786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1cb13e8dab0a14d667e4d9b265c749ae59a611e6862763377f1c8e34e0112c01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68902391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54d7ab7b13f29c59bc95210628c83870c56bc3b074d787b15d305d64a13d17d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 05:18:32 GMT
ADD file:2d913f7b6c2e804834958b3d144bd7b5150a438e2aaa73cdf2f1be1c64d10100 in / 
# Thu, 23 Mar 2023 05:18:38 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:22:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:23:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:83c1a140184ad386a37a5446dba474a2a8498dff7ae8d2ccd2957aaf8dc1682e`  
		Last Modified: Thu, 23 Mar 2023 05:26:35 GMT  
		Size: 49.3 MB (49291603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaeb19ea7953e3c0a2cce0d76910d46a1fc5e289c90379ecb81b3e5ba2a0c16`  
		Last Modified: Thu, 23 Mar 2023 07:37:04 GMT  
		Size: 8.4 MB (8439874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecc4eca24f781c1e786d1fc88cb24202f1248f85adc06cf1b375f5607ec2d93`  
		Last Modified: Thu, 23 Mar 2023 07:37:04 GMT  
		Size: 11.2 MB (11170914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:85bf0cae57000ef766ea7ed7d8f16d94925cfc5dfe0ffdef79a82c81cfdb0bd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75136981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f95dec386d645db16ef52d1d12753c4acc5e8cd37261e08c733828e13efe122`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:20:05 GMT
ADD file:3534cf3f10dae5b70c64865fd70cf5b9aa6ace6be9caa2d69518d6d59c4943fa in / 
# Thu, 23 Mar 2023 01:20:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:18:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:19:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8de2c12bac6cdfac096a845424e637222b157d221d8080dfc0e3cd14581716d5`  
		Last Modified: Thu, 23 Mar 2023 01:24:47 GMT  
		Size: 53.3 MB (53290173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ffcd14b130bc950e2e794bcf2e09ddffa8e18668803aa384fc8de743e9d8d2`  
		Last Modified: Thu, 23 Mar 2023 13:26:33 GMT  
		Size: 9.7 MB (9661589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecca2a654e1b66be833e49110ac475ae4995f36d83ba12ad0396e8f4cf953872`  
		Last Modified: Thu, 23 Mar 2023 13:26:33 GMT  
		Size: 12.2 MB (12185219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:38e030092f73454aae7e3c85ef48d181ce6df61868218658349179aedaf2e493
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64375224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485e2b054979fdf7251a21d7f0469c928ebb13ec41c80f89184fb68ecf81d44d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:09:07 GMT
ADD file:0ead2f17f27ee13f553b88d07f59f56840fc40a7d668942a261c1a8714543b00 in / 
# Thu, 23 Mar 2023 01:09:09 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 01:31:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 01:32:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:94da1857a4ca1e8976329ef725087fbbe73af98bd925fbca65400b32537f3178`  
		Last Modified: Thu, 23 Mar 2023 01:12:27 GMT  
		Size: 45.5 MB (45471889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c96232283bbd760cb6134bc51d0a8713ce646f72c2f26103aecffb6f0744dc`  
		Last Modified: Thu, 23 Mar 2023 01:44:11 GMT  
		Size: 8.1 MB (8115301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58559086b64d3108c9d17e9f17b13d71448a05197854524491ba5f1c5889ab5`  
		Last Modified: Thu, 23 Mar 2023 01:44:11 GMT  
		Size: 10.8 MB (10788034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3211f9b0f5b6f75fe74c6f652a103010f906280b23726e73b4d09dc490b2630b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67647445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e64983b030d31241ace816b6735cc1e6c667ab5201171f91099ef1e094a8a92`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:17 GMT
ADD file:f722c963bb9fb9eed0d7ba7fa5de1fdaf0fac91107cd71702d55f0cc074cd6ee in / 
# Thu, 23 Mar 2023 00:44:20 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:17:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:866ca1f7e7197a336b8f05cbbb9eb6e6a32a17ade3068f3bd62dd93f926293d6`  
		Last Modified: Thu, 23 Mar 2023 00:47:32 GMT  
		Size: 47.6 MB (47648043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a6b4cd67d490a2c70edebe1070c48db7a7451d2f3907f036960fa85459f9f4`  
		Last Modified: Thu, 23 Mar 2023 07:22:03 GMT  
		Size: 8.7 MB (8713413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ea7fdd8644a777c3ecd69ea57c24497971eabba7d4f9f5d7a151239348da4c`  
		Last Modified: Thu, 23 Mar 2023 07:22:03 GMT  
		Size: 11.3 MB (11285989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
