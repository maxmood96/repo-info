## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:a0a25d2e317c3f9be72a43bddcb6c70daa6f0d5887f9bc2448617c1c5a7cd3c5
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:42767b409e08aefede925540fd05dced7d67d117c9516e3c5e6af0a322780fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53755008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4e798e4400d65df5a9bfe9fee3979687837d164a55ace5b0004f8adfeb1ee6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689e3d92809bafbea28040a3692cbd00780642dd3a26aa55be976ea7429c6d2b`  
		Last Modified: Tue, 10 Jun 2025 23:24:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:94121a30180ee1e6c882b3265be7682b982bc5481a85ad0c8aaf6d8b643a2828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4030147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7980efe98586b11c9f5355461e6aad34f77f36cfa5b955ea111f29b0bcd23c42`

```dockerfile
```

-	Layers:
	-	`sha256:f185fc326081221e0442d9713030f2b779cd6eb17194c555a2314be5686bd840`  
		Last Modified: Wed, 11 Jun 2025 00:24:57 GMT  
		Size: 4.0 MB (4024301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1fd1925914d5cd46514ec21e5923bae27be82cb8036b11cece61e3050cf1d52`  
		Last Modified: Wed, 11 Jun 2025 00:24:58 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f44fe1cb81fe77e1c3a9b420e3e3606afa76bb8e6451eaeb13b2bae4f3e57282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49044184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f64d7179ecbb38655bb4782fb49cd3e9d76c363dddbd6af65cbb7f0954d9fdb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:efcf40eae0046ccd92d3b47ff685e1e9cf7a34d0a92f6de893078f115e01f20f`  
		Last Modified: Tue, 01 Jul 2025 01:15:14 GMT  
		Size: 49.0 MB (49043960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4c530dfe3c35890c2d16d3a1a22455e03c47be1b00fb701632f8885439d0c1`  
		Last Modified: Tue, 01 Jul 2025 02:12:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6e6a4ae4a4bd5c80b7967d7c7fb3c8352f40605a74542d4be36c23b87223aab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd10165940f5a8aae02efe7098cf357fde2ff9bc9122bf1065ce7c82a362113d`

```dockerfile
```

-	Layers:
	-	`sha256:a778796094a93f7534313f0b2071a5a92731d59b2134530360d00766b8d392b0`  
		Last Modified: Tue, 01 Jul 2025 03:24:55 GMT  
		Size: 4.0 MB (4025863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a84db63f8f4a36f5f29197bbd15488f50fb01d7de1f863a720bb18968145b6c`  
		Last Modified: Tue, 01 Jul 2025 03:24:56 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:1168b6b669e9cc6afbf352519ee04a4233f0c39e17e5bbcb7a434f9c207793de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52252480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581835b95178eeec00a3123246b6870153553fae5c52abc44b5f80ba73d8f3ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Mon, 30 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60048776700cb99ca6cda3cda3ef3818ac460e2ceda318768e72e2b01602c543`  
		Last Modified: Tue, 01 Jul 2025 02:12:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a7fd40656efe41b910397c66972974afe95bafbbe036ec828cd4438f48385c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4029796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2b63df745a44211670c646928fbb3f44af1a3840673d306370d3fedca193ef`

```dockerfile
```

-	Layers:
	-	`sha256:07800634365333d86df3f578f31ae63646e336970069d7982e4c5c9e074f8f46`  
		Last Modified: Tue, 01 Jul 2025 03:25:01 GMT  
		Size: 4.0 MB (4023881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b559d2a951d29f1d3fc317d3e489036de89d88595ef46b07a1565b9e854231`  
		Last Modified: Tue, 01 Jul 2025 03:25:02 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:f0276b278cb9d3ee08494cdee8354e97af6b4e9d4134f785078eba0e19aa23c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54690238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6063ec240da3c41bf38d5cb5b5e8f8653242deea91911a62efbc950c2a0914c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5144c301fec2775c4d4f45dd22d7f475eea9f2543e9a1f54cebc79b253f98fe4`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1d332e97488f55dd1a8e71c98a7bb683152452306ccdf4764928dd7283f4e852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757fdf4b9a2d551a6552d193dd5adf8c2c440bb89cccb6d930e117a8ace4bd4f`

```dockerfile
```

-	Layers:
	-	`sha256:ebb304e3bfd78be53e21dca2dfca379ccbe5f81520898c8f49f4e0101e343882`  
		Last Modified: Wed, 11 Jun 2025 00:25:15 GMT  
		Size: 4.0 MB (4020855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11e4572497d7137771bfb222aecde4e47ff2716410bcf3745d1b705a4d81e4a`  
		Last Modified: Wed, 11 Jun 2025 00:25:16 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json
