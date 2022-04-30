## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:a15c6aa743f533dc5ce892143ee34f4522c95d3e5ad1b232e47b6b3436d3b788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6afe49c43430f189828ec6863461d082fc616e45610b7d3e8918c53a56c9873a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37799117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e7bffa467d1fc5f68733e0d9878861b6343b4a6bf8f86ed33d8c49a01fe5b2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 23:21:15 GMT
ADD file:37744639836b248c88f6e126619829290b45c233309538310e8fffb82e98eaf8 in / 
# Fri, 29 Apr 2022 23:21:15 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:55:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:125a6e411906fe6b0aaa50fc9d600bf6ff9bb11a8651727ce1ed482dc271c24c`  
		Last Modified: Fri, 29 Apr 2022 03:03:30 GMT  
		Size: 30.4 MB (30421006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd42456788d884c562de4649973cbad0ff15b20c71bb817db73e99ba659bd98`  
		Last Modified: Sat, 30 Apr 2022 00:03:38 GMT  
		Size: 3.8 MB (3818745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9eaf54bac42fe111f77299f5bf651ebd4d872700f461e671a8051862ad6f875`  
		Last Modified: Sat, 30 Apr 2022 00:03:38 GMT  
		Size: 3.6 MB (3559366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:45ae32633fbb689a2adad29576a5a76965ae33cf811d480d33104ad0064eee93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34298095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e5a0b82d9c009ece64a5bc9c8c2ab61adca25a238af980eedc27ba40479940`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:59:30 GMT
ADD file:78ae02cb00d8cc788584388eeb9fdc5ca6b45f502d33acd7f6efe7fc2a325683 in / 
# Fri, 29 Apr 2022 22:59:31 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:35:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5a3411c136d8a6da4e9d7d3abcbfc94f59ecb2935fd02cad49be6a79c899fcaa`  
		Last Modified: Fri, 29 Apr 2022 23:03:59 GMT  
		Size: 27.0 MB (27015834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0fc400254e500236c1a1555f53101f3d136a6466afc02b601d41b663424039`  
		Last Modified: Fri, 29 Apr 2022 23:53:01 GMT  
		Size: 3.6 MB (3569862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aff75e9c518264298a148cc4e8d868ef1588d3fbb3eb5a8f37dbc41d393fb89`  
		Last Modified: Fri, 29 Apr 2022 23:52:59 GMT  
		Size: 3.7 MB (3712399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:95db445f475f3173a67abf9811cd9764f751b8224e99a086c58183a3d5966f66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35488221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8101e90791030ea25bf83059013936b4e020b721a1784971e2790b078c9d435`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:52 GMT
ADD file:1e18e22e32f06a7e93275cf3a2eb2a1d3892be27628bdae2de4b2aadb992bd50 in / 
# Fri, 29 Apr 2022 22:49:53 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:19:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b84950154c181a602d2e93b68e84660f96dc78f94ae36f3df2db8d5701abb6a5`  
		Last Modified: Fri, 29 Apr 2022 22:52:07 GMT  
		Size: 28.4 MB (28376457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4779269ba0c40d25a7dc0dce21c857eb6326260eef418a05d8f7ebca0f0b7c52`  
		Last Modified: Fri, 29 Apr 2022 23:27:13 GMT  
		Size: 3.8 MB (3792535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc5ea7b81dce7b5d5da0ca011f59cd030d00e4c8bdb15aa0451b41aa695a056`  
		Last Modified: Fri, 29 Apr 2022 23:27:13 GMT  
		Size: 3.3 MB (3319229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8e09c45ae78c0f74d867dde17a9bc2d81e0abbfa9730b211cfa087af9b50e6be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35134500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd72da736a9a905acb12a3b131e1286df5d8a2caa4ac540a4039bdaf4d343ffb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:18:39 GMT
ADD file:75794a810468b5240ea932e78dd71b552e395323c6ec0cc79d804146f90ee444 in / 
# Thu, 21 Apr 2022 23:18:40 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 00:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 00:24:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4e4d3d9efc57e0160a4c8fd76a93cec2e8274d4660b25de44af6a0831c87634b`  
		Last Modified: Thu, 21 Apr 2022 23:36:51 GMT  
		Size: 27.7 MB (27745140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eaec18e9fe1aa3ca23012ccd477dfb97162ef7d1cc1ff10a7f15de84b624fb`  
		Last Modified: Fri, 22 Apr 2022 01:01:34 GMT  
		Size: 3.6 MB (3612933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e7dfd819c86c7572101432d76daed4fc4e538bae377fee2c79ebfef409c812`  
		Last Modified: Fri, 22 Apr 2022 01:01:32 GMT  
		Size: 3.8 MB (3776427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:36a90e851554607cf3909c58eeb59b3b682382acf4508404e2326f9ec2231850
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35928918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd65b257285e8de8dd5b5fb1a71d7fb1994aed78b3135dc33656b8b398e21e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:50:31 GMT
ADD file:f64deb7af5cd28d502c52ddec5392a74b3a97eec2157bb03a4c0422eafb13c49 in / 
# Fri, 29 Apr 2022 22:50:33 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:14:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:14:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8346d310386430a355c4f3bd23e20115298043169165d7b84d92e3233b6696f4`  
		Last Modified: Fri, 29 Apr 2022 22:52:24 GMT  
		Size: 28.6 MB (28637232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e3da9a8d3319d0121a79a6e6c433b298c51996b294808f5718b06ec206c38f`  
		Last Modified: Fri, 29 Apr 2022 23:21:08 GMT  
		Size: 3.8 MB (3821153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad36c963048b206a25d408e23b027027eda701e952c4b1495d5eb264b7916b5`  
		Last Modified: Fri, 29 Apr 2022 23:21:08 GMT  
		Size: 3.5 MB (3470533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
