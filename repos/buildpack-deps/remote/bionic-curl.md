## `buildpack-deps:bionic-curl`

```console
$ docker pull buildpack-deps@sha256:818e2a65de79d2b1ce895b82dee48f2417f031718be7c817c4222fcaa95d9231
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
$ docker pull buildpack-deps@sha256:a9631241b02c1eefcb2ed9e572d399da035b2d31ba96f4f920890be9f5c25e3e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36377617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab508500278539dcab46cea380406b2f071afc99044b22913e945cdbdd16089`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:49:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:49:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e71f3df86e3a903eda5c8d686f86fe2c6a0d9456f91023cb6d3c167fb0ce09`  
		Last Modified: Tue, 31 Aug 2021 03:11:51 GMT  
		Size: 6.6 MB (6646777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88aedf369e8db7b9d55546c93c9df5a8e9a1fb7a16a0e0bbf55dc096e0d37b6d`  
		Last Modified: Tue, 31 Aug 2021 03:11:50 GMT  
		Size: 3.0 MB (3022329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4de6313c8ce02507698ca93640ec4e1e18f05c5ef8f36d7304a1959577aa390d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30608238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9546a7fe288db39f65011e7434b7fd870c2a71706fa6dda7e1f332a5b1dc22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:30 GMT
ADD file:5e191cb3774eee823ea256e960cb570c8ee5bb1a149dc1bfdaaa2adf7bc64007 in / 
# Tue, 31 Aug 2021 01:40:31 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:11:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:11:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:94f80e8eb1703fb9b4edfd10bf21f9967e116e6692f5dd4363fbe8f3ac04946e`  
		Last Modified: Tue, 31 Aug 2021 01:44:27 GMT  
		Size: 22.3 MB (22306479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3861a2b4b4379b2bb53b663f814026fd5aa82ec17aba9f350a9597ab5273a6`  
		Last Modified: Tue, 31 Aug 2021 03:33:18 GMT  
		Size: 5.7 MB (5717193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decb3fa3c4abd05090e6fe2924b1f9dace9c46f49394e0d3c3fb897ce110a718`  
		Last Modified: Tue, 31 Aug 2021 03:33:15 GMT  
		Size: 2.6 MB (2584566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5d962e80ddffea4d545bda177e9840d262fb1893cdac6acc8cc3863bf9de75bf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32601295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34eb7034c339584e265fb320d1e0d2496baa28988e145f56a72254e7ec081ad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:08:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:08:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4a9b8c6709cd3ea323ffea2dcfa72913a9fdc73837573db0ffa663995a44a8`  
		Last Modified: Tue, 31 Aug 2021 02:18:37 GMT  
		Size: 6.1 MB (6087650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ad199f9143cc4082ab5e445c913e284b9f2ec63abce0b6b1243561e2810a77`  
		Last Modified: Tue, 31 Aug 2021 02:18:36 GMT  
		Size: 2.8 MB (2783046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:77c62e1928a0a02b1eb69d7cda933975816c77ee2ba1e333f2cb8d916bd3bf92
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37349567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e6101ebd52b5a1c60f03a674e775c8fa0244a300cbadc8c8f42793a4f5e1b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:39:08 GMT
ADD file:615269b4e3662feffa9257a896456387554777532f070eae2226fa704e50150e in / 
# Tue, 31 Aug 2021 01:39:08 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 01:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:57:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:01a6f9651a524383d1aac8b05ceaf7a079d305146c6bf120b7ffb27247b18230`  
		Last Modified: Tue, 31 Aug 2021 01:40:06 GMT  
		Size: 27.2 MB (27162437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2c7d08d74fca5ace99c2318c3f53f795d5cd713e8df0f41ea3c071a3583372`  
		Last Modified: Tue, 31 Aug 2021 02:09:50 GMT  
		Size: 6.9 MB (6934539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a486c005ec2b9b98efae8ad7204dd1b1e216eabe229174d28fb5b62c9489ea0`  
		Last Modified: Tue, 31 Aug 2021 02:09:49 GMT  
		Size: 3.3 MB (3252591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1eb162f028cf31cde7114fc0f6bb51f1db2dc03e3176d1153990dbde7931382d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41216524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7639078879437dfa416b3953499bec521d9fff9e701d6679bf281144fd5947`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:11 GMT
ADD file:32c084b07cf88f4b46c2c94d6e8634a245a8ea46f4c166fe98b49a7e3d44a700 in / 
# Tue, 31 Aug 2021 02:10:18 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:24:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:24:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b66177991333478fe4de9a7fc6ee8c546debb78334473278e085735e8a88072d`  
		Last Modified: Tue, 31 Aug 2021 02:13:59 GMT  
		Size: 30.4 MB (30437758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164a2b27f3d3e3338d0cad4aa8917def23b4e4125d8bd35fd92d28d391bd7193`  
		Last Modified: Tue, 31 Aug 2021 05:04:40 GMT  
		Size: 7.1 MB (7059170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c419c8f7c4b804d1eb861ec26eda86aed2a9e66ffe649c93fe1a1729410d58`  
		Last Modified: Tue, 31 Aug 2021 05:04:32 GMT  
		Size: 3.7 MB (3719596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b1f689b30d2ae3be28a65adc94df539028bd0f5346b14cbeb8e12d90f6cc549b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34677158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849662eb467d6d767b9ef21110d9f00f5b75c83c278ee84bef70c174b2e1af68`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:42:06 GMT
ADD file:587feabbf5ad530bb19e438490116110e0c3f5fd5c8b98bcce6767af928c66de in / 
# Tue, 31 Aug 2021 01:42:10 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:34:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8a5845e3ee3e2d93d3bcf0f827afe41d646f59cdf52f107306c232b60ffeb3a4`  
		Last Modified: Tue, 31 Aug 2021 01:43:59 GMT  
		Size: 25.4 MB (25366401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae5daa9a040b93bff6544ad59a003cd958048bef64a9f991a5d3150888fcbed`  
		Last Modified: Tue, 31 Aug 2021 02:45:10 GMT  
		Size: 6.3 MB (6335758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32bbf8f7d5625c28aa637939c7029792a4f3b624e300c59cb77575fe7aa84d14`  
		Last Modified: Tue, 31 Aug 2021 02:45:12 GMT  
		Size: 3.0 MB (2974999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
