## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:08705477c89c220d9374266bb43d514ffe7a8bca7535174e2d4fb219ae069ca1
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

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8b4870601c99e26bdb0e9d6cba7c9ef7a1efec911cdfc1f59ca1d087e10afc84
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68291508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5632c1efb61eab5d42fec11ade19c955f613597e5433191c4af806f2ee861243`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:31:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:31:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dae484504b039004d1f23b1777be24e9e8d0f126ee1f38b97544d6343fb9fa`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 7.9 MB (7856401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21739e3ef21a7c9983fdfc82d5a3837c633779965fb0b2cd7b746ec9c260664b`  
		Last Modified: Tue, 29 Mar 2022 17:39:22 GMT  
		Size: 10.0 MB (9997192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d345d0e6bbcd39917820aef59466b6004ad627d6343e31e9e9713cd9ff04c80a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65246421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ac1fa34e52ac613189712d9bd8f7222e6efb3adc980da31741c8530a562bd4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:04 GMT
ADD file:e7d31ee8f990df96d5922feb35173a364a0832e8fce2d32fd4e703aa3b66e1b2 in / 
# Tue, 29 Mar 2022 00:51:05 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:46:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 07:47:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0bbc2517bf9c8d842997ba8f85b59bfd92c5bb6bba79c39047eecda859dcae27`  
		Last Modified: Tue, 29 Mar 2022 01:06:08 GMT  
		Size: 48.2 MB (48158294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1b4a5e78fec7573050b1b9220718c42ec377971effed53f70015af0614fe3d`  
		Last Modified: Tue, 29 Mar 2022 08:08:45 GMT  
		Size: 7.4 MB (7400493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4f39bb570fd924ca89ef560a7dcf08a5b1bdb060fffc39839196ea306860e0`  
		Last Modified: Tue, 29 Mar 2022 08:08:45 GMT  
		Size: 9.7 MB (9687634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7c070c3a35c160408e5ddd669c5a0cd0b6cfa101d99559143663e2f718a3252f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62403380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249bb5194f8b63d20ee9ecb406426ec8f154095cbf8b095ac50eb6dc0176d6eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:19:04 GMT
ADD file:60a690e302d164c569e6f3fc29adb6686618bb728249405f90960835525b0599 in / 
# Tue, 29 Mar 2022 02:19:06 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 20:09:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 20:10:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0cc72482f2e040b686190f2967010d45947924353440070552a298b9f9f81b19`  
		Last Modified: Tue, 29 Mar 2022 02:34:54 GMT  
		Size: 45.9 MB (45914531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ee42f432eca8b10b5cc28da57027f157052392220ed81ab477a06ce1771abe`  
		Last Modified: Wed, 30 Mar 2022 21:33:01 GMT  
		Size: 7.1 MB (7144979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bdeb2a3bd0d310e035553bfd8dca244c71e5c1d7fa33c8e1f19d5912e0be7e`  
		Last Modified: Wed, 30 Mar 2022 21:33:02 GMT  
		Size: 9.3 MB (9343870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:217ecb4923505a4f46b79e92a2db225e8adedd73931192978943b19b586d14f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66712673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cef86240e7fc3a002beaf43baa3571faaf70aa9fe758d690cd500e43e7a965`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:14:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cef8e192150fcb831e585c75b24eb41a0dcf95d4cda95df6289e912e53f228`  
		Last Modified: Wed, 30 Mar 2022 02:25:32 GMT  
		Size: 7.7 MB (7719728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741a7b3bab3cf3ca6820a679882dbe1451b7eff001fd60a3a91126b1e7f39877`  
		Last Modified: Wed, 30 Mar 2022 02:25:31 GMT  
		Size: 9.8 MB (9767049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8e6c357ff29435e2a16bb9e6a5077e0e113e55587d9ecece7969c347f88120f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69350713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc526298aa96723eeb244b4ab53eeef4e521e55b2cde6f6af11e3c7328767e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:12 GMT
ADD file:fb2c1bf394c39b5bf948ceaa00317518326bd846b3f6802dc39cfb7fcf404c69 in / 
# Tue, 29 Mar 2022 00:42:13 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:58:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b86fabf064e35595b9c8543deb0dba50a95e438387a9877ebfe189bbfce3c87b`  
		Last Modified: Tue, 29 Mar 2022 00:49:34 GMT  
		Size: 51.2 MB (51206670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fecf9ef7e2149c926eaf909af17e48d32080f3777447e28017d8277168ef61`  
		Last Modified: Tue, 29 Mar 2022 18:16:16 GMT  
		Size: 8.0 MB (8022197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ba7e132575662e21e001c19449819145d8c04740ee029d58abb3883fa71010`  
		Last Modified: Tue, 29 Mar 2022 18:16:17 GMT  
		Size: 10.1 MB (10121846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:00c26d0e540adb79c57370e8350929192083dddd6f30caf3f6c8e56775ae6ff7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66152937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a46cf9ac853b8c13da1a63df8a38527f1ebb60174f920af3601389504cb3b57`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 07:43:01 GMT
ADD file:c86010b52f782f910842586e6abc81e64c7a659d001b89799314a59f4fb96573 in / 
# Tue, 29 Mar 2022 07:43:06 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:35:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 08:36:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8e0bee9c4b9257c0ad7469830be5e890536feef4e8ffe6c2613b7e8be7e060f6`  
		Last Modified: Tue, 29 Mar 2022 07:53:41 GMT  
		Size: 49.1 MB (49079891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc690a0cd1092524bdd12063c730cdf1df3dfa2f8c5920231d8477654c04b854`  
		Last Modified: Tue, 29 Mar 2022 09:38:05 GMT  
		Size: 7.3 MB (7272773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe0e6a034874e5b70e892d14e911e5aaa7f314b7588616996be6ff22190b1a`  
		Last Modified: Tue, 29 Mar 2022 09:38:06 GMT  
		Size: 9.8 MB (9800273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a82ed0848001a5ce880f824333fb3412dce09bcdfaff66c9e47681e2d8c28d3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73204220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c16db849f7963b1ee9a8f9c57d7bbef15f7a77820de34375f1651d373ae6e93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:25 GMT
ADD file:a600709d679cffd058d04ba0eb0765cc870766fd5de083ada0eeccfd7afc21f8 in / 
# Tue, 29 Mar 2022 00:22:30 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 05:59:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 05:59:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:eb53bdc4c2c6ececbd424b1c643b9877934a5297a5d2db0eca1a175d7a21d32e`  
		Last Modified: Tue, 29 Mar 2022 00:33:53 GMT  
		Size: 54.2 MB (54183100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596f9130bbf698f182cdd8f8965c6d1fb059aff38e309f7dd44db12967d4ab7a`  
		Last Modified: Wed, 30 Mar 2022 06:27:07 GMT  
		Size: 8.3 MB (8293334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf74211bc82c5c0431e1ac0b76c006093e829ef420568923567cb2d6bf07a69`  
		Last Modified: Wed, 30 Mar 2022 06:27:07 GMT  
		Size: 10.7 MB (10727786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8f8bd2a1d7a7f6e9e17b89e2f922d11a95aadc75aad67f61f0fb3deb5a8bafd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66314325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a162a38df2214484b29d79de0b23c173655cc21e12682f750893f6036670456d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:52:09 GMT
ADD file:784894d175880656ac82b485076fb224bde46d379dd634720acf7acd5eee9365 in / 
# Tue, 29 Mar 2022 00:52:11 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:26:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:26:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e3cc532be5698da8ac6589c11495b960fec83fd52aa82617e3218678ff4546d1`  
		Last Modified: Tue, 29 Mar 2022 01:07:20 GMT  
		Size: 49.0 MB (49007755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af67f5247c69c4ea0f2abac4f0d15b87aba276b2900c5741a7c88233a7be56d`  
		Last Modified: Wed, 30 Mar 2022 02:34:32 GMT  
		Size: 7.4 MB (7423528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1254cde0440f5ac2b199af47f310c376960961694f11b68a43cfc6a91c63ff`  
		Last Modified: Wed, 30 Mar 2022 02:34:32 GMT  
		Size: 9.9 MB (9883042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
