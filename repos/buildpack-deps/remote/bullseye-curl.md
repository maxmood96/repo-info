## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:b8ce6b353d3341ee7268a2d7b31bfadb96bf53d1c1acd068975332c6100655dd
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

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d46f632af1ce957541db52d3193c01a847e6cf30f0389b6cb5d8dda63e4aecd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69511284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6280c6ef0fc6fbceffeac71b7f184a68b7450ec4c72a7b31c20af1584cee5c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6b9c730ffb87f6966054a3b363768cf2660eedf425fd4cc97470eeeb44da2983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c675e28df764c09caada1b09d0be3cde221b0b5378d26480ddf9e37e77d71`

```dockerfile
```

-	Layers:
	-	`sha256:ce8e54447a965d6bb403a1e208edb6650e424c20e0d54b8258175b757c4f8557`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 4.5 MB (4487595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbcfcd080b20d2c56bd4973791d006372665e89a766b1dac0156a55cdad65599`  
		Last Modified: Mon, 28 Apr 2025 21:55:43 GMT  
		Size: 6.8 KB (6801 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d14988f7c7c894c48c7da779a89f8c532b8e4395080c747d17ba604cc8d927a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63919074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637d5ab9034b7391a56654eef6653d91512dbb54aa6f9197788c3a43c2eb0955`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Mon, 28 Apr 2025 21:16:06 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Tue, 29 Apr 2025 03:37:44 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2846922343e82f242ebb6628c32238c38d795f3b40aeb0b0b490c7150df09e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da6fd7296d29d283b2551f15de22985b4b530782a2feb549941a4bff940000c`

```dockerfile
```

-	Layers:
	-	`sha256:2965beefe878e8f2c79404960ba551f702afe9f0e596bffe23aed63686109875`  
		Last Modified: Tue, 29 Apr 2025 03:37:43 GMT  
		Size: 4.5 MB (4489231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea2885fabfad51fa6993820e91f78f0b7a19758d41981f55ae32fedcd1c53f0a`  
		Last Modified: Tue, 29 Apr 2025 03:37:43 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8e1bebc1a7c7f1a71aab7f1ae5ac7899cab503b2fa6112f4e930552529c4ba4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67995087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4563a8350604a04af5600b62b1d16edccb28d5c97ea5a4395705e324029d47`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:73edacd89346f748ca631980c7d87e425867813036f412fcdd0da331cd7c94fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66432a7d5d046912f35f417488f45297790fe1e6c2a6a3f760efca30a0bb5f8`

```dockerfile
```

-	Layers:
	-	`sha256:36e35f94cc356568286cf0a10f2d3fdb834e31300b5cb9ba2afd931318c3f36a`  
		Last Modified: Tue, 29 Apr 2025 01:47:12 GMT  
		Size: 4.5 MB (4487209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:815b01e92dafaa107d8ec9c574a418507eb81d537f13bce19f109fafd38ab9ba`  
		Last Modified: Tue, 29 Apr 2025 01:47:12 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b1c0cfa8c32d56d8fab9743742ebd5184a5be165352f0d29bce30ed1401d9182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70950501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ea7c3daa707cdf14a3ce4de2fae8455c730f1cf2e5307a1358bd0761cd0105`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb48ef4c334135b55fe5dd328911059bfd41eec15edf03ff0ab96ca44fb6a1`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 16.3 MB (16267399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f56cc8c94d9a7f00f928dd03f18d8d39c453eb65398a61a3b1355f331beaab62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4490815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304dc762690dd477bf58d270ec35ddfa3fb851cd33d18c371250eeb1f713dcee`

```dockerfile
```

-	Layers:
	-	`sha256:fbc6e7d5789639f0a02523cc743a26a849d781abaa63fc9d69c5e2e3a4086322`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 4.5 MB (4484036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b63dfd5e44edaa04e3d1b82b9fc300099b24b1b51c58fe250491a799f3fd801a`  
		Last Modified: Mon, 28 Apr 2025 21:53:51 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json
