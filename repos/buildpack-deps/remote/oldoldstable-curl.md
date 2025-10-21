## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:fe58fbc356d10ecf803bfb740b68e4f6a444a0a25524f3416124e89172c987b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d9798fa16ea7a58155ffb6c3a1318ad1eae5bbde6fcdc2626c8f29b0b6d1258b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69520171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e1398fa2bfdc8657f285426db19471bfe8bd4a4b5913c413f5bf1251ac6e17`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b6f830cd306f01980373f1e0120f2d00018fbe51a9506b7262f5d9e4bbda74f9`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 53.8 MB (53756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa9ab09db8d94503213f634b29be3505174979f2e0c6e3fd46c2acc0716c25`  
		Last Modified: Tue, 21 Oct 2025 04:46:42 GMT  
		Size: 15.8 MB (15764056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d703afce67146a85812cee63f3123baeb519330dfa1080ac92a3d0779d081844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee53a702dc8e2cdfcf6b034c3ca46ec08196ee25f4712565fe90abb621dcb26`

```dockerfile
```

-	Layers:
	-	`sha256:3e6e671fd30f00cf8c628911ad4728f31afcd76cf60a2721de14d458fa382095`  
		Last Modified: Tue, 21 Oct 2025 10:20:17 GMT  
		Size: 4.6 MB (4629099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f16c43e2eca72f39ec104f9494def95c98190a30aa3efe83cfe69c4de1ab038`  
		Last Modified: Tue, 21 Oct 2025 10:20:18 GMT  
		Size: 6.8 KB (6807 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:efd9d38450013df213afb042ff86543a9d78fc331a390ab7436d2d924e11d936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63925385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602302eb50b730594a5b0c7faeb1037db4992733ecd83f6befd0c766c391c43c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:680ed921e0c94a719af1d242eac2d0c1be8482153680a3940f3435ee5598303a`  
		Last Modified: Tue, 21 Oct 2025 00:20:24 GMT  
		Size: 49.0 MB (49046121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c68013a317d7d802bb25c57a724c8753caec2fc7f0e78fc13f9a38fd22ecd4`  
		Last Modified: Tue, 21 Oct 2025 02:44:25 GMT  
		Size: 14.9 MB (14879264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d3f8997f125a72a481a58037c419ef6d35c5c3845da5379337e9b75b774079aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e1880fec037ac6b58a22cde2a6496914fbf16656ca24915dfdda02b48ce759`

```dockerfile
```

-	Layers:
	-	`sha256:cbe776e542c11f8a93527ec60b13f8cad8872e654b453b59c098cfca9f58d349`  
		Last Modified: Tue, 21 Oct 2025 07:20:05 GMT  
		Size: 4.6 MB (4630735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1506fcd98a55b5c8bc71e95c57e618a3c0ce79f2e95cc0335d57a3ce47a68dca`  
		Last Modified: Tue, 21 Oct 2025 07:20:05 GMT  
		Size: 6.9 KB (6871 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:be9edf16b82e41b8903fbbe56a5eb8bfc4e82e3aa94497c49624465044cc96ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68006954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec62035900734dc8fc089f57669f9560d2e97bde2545ef97edaa9c447663afe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f7bdca064e682157394f36dabd112bc9831aff9743216b035e2ccccf704cc3`  
		Last Modified: Tue, 21 Oct 2025 01:46:24 GMT  
		Size: 15.7 MB (15749510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d86d39439f2cbd04011f244fd7522de12b458d29dbd87c23f27409a7d3bcae33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4061f266e6356b6207ae9505005534463ca8c64dedb3e055e005f4a99e3e21`

```dockerfile
```

-	Layers:
	-	`sha256:b8111cf650de100a32aef24fdf423a9c8fe201a47aac875cc512aa514f354c6c`  
		Last Modified: Tue, 21 Oct 2025 10:20:26 GMT  
		Size: 4.6 MB (4628713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3638805a073f9b7d3435c1060b3d6c72b78e8d54c18c53dc0325e59e2163a7ae`  
		Last Modified: Tue, 21 Oct 2025 10:20:26 GMT  
		Size: 6.9 KB (6887 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2e6d3525950fa2cd3179e23d307ee041829488143b3f081899fec5bd6e98ccd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4adcb23583f7071af258c7a97e84a6b3bd22b19f2cc0416ea988f8262d529e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10d430deaa3d2ab4898db053e80d62403503897839bf6efd17ed5412b18d7973`  
		Last Modified: Tue, 21 Oct 2025 00:20:39 GMT  
		Size: 54.7 MB (54699294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453fe6b4c7a680d5464137a3450d263e01a7ec4d491659295432d36b0198bbc`  
		Last Modified: Tue, 21 Oct 2025 01:53:19 GMT  
		Size: 16.3 MB (16267847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a497908bd095f57bacf45f0e2668f9689ce8f9728460edfd9ae598eac2e884dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9a4d1b9df42fd80e80bf4fce1d621e77bf13f42878144b05f73a2486e3b2cf`

```dockerfile
```

-	Layers:
	-	`sha256:0cdc239c181ad85435eea6fd63ecc9862a37f31a5f228b411ec6e43c3f76a0ac`  
		Last Modified: Tue, 21 Oct 2025 10:20:31 GMT  
		Size: 4.6 MB (4625602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd2c67c87d2f4e776d62fd0d9373a7cefa5319a8ce91a4fe75feda09e439902`  
		Last Modified: Tue, 21 Oct 2025 10:20:31 GMT  
		Size: 6.8 KB (6784 bytes)  
		MIME: application/vnd.in-toto+json
