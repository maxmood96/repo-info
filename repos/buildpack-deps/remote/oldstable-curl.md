## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:2c800a6e15436a36d90ed3c84bf429aacb3ebfd8f6b5d1188b646009acc854fe
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

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b960e9a35b94d98f8e28b9e7c6902cb6c0b00730da4c43b30bad6b65e1197205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69297534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8497e82cb3900277c279f7b4301f59ecc6cefa8ddfd2ee6cceece3a5d69cb179`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925257a7168ed219a5d7c2a69af3245ca4cd9e376424f7f006535d9714437bd4`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 15.6 MB (15558387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:17c6283204c87400f89a5054443c5bd83c77d1717114cdadc95a10f8743d9c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5e44850ee339d6ee93ec71f2fdcf0bf2391e31821461866209ad64c7411c82`

```dockerfile
```

-	Layers:
	-	`sha256:0d955dfaeae326d60e2abe1818cb737d6839251fcf25ad39f452038fba101b22`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 4.5 MB (4490305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aec84ba0adf96199bf08ed6c2d5fdf57c284d93fe90956bc7b22619c8b75f645`  
		Last Modified: Tue, 03 Dec 2024 02:15:41 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5763e2f5bf1629bec5c9e16d00a72e3dfd8f17b3a5667e72a651d18e71ef39b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64945646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce309396159795b0c45db2909a8559c1303270bf296bbe0f73ab8e2a6054b4c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c18c6ef253e2b87a07739846b10eb333531241b80c23e3aec0643adc1b449e1a`  
		Last Modified: Tue, 12 Nov 2024 00:57:22 GMT  
		Size: 50.3 MB (50272340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907b69db4cf1745187b07df647e4ed72539303d8747c006695c2bc15e5e1e185`  
		Last Modified: Tue, 12 Nov 2024 16:00:17 GMT  
		Size: 14.7 MB (14673306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d1fb45a0a4b3ee70c293b961eb04d26ff1a65af954b91132ee444cb2d991f128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4500675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33537d7ac7b5ad3b240e3e4da843d63123e8c262462e97cfeca2cb40e962ad7d`

```dockerfile
```

-	Layers:
	-	`sha256:87ec50285f2a8b3ca66ab532e7620f2de6bd499824493288de9a55c1fd4f6151`  
		Last Modified: Tue, 12 Nov 2024 16:00:16 GMT  
		Size: 4.5 MB (4493814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9433113985ed5cf511a7ff1fedca93ced3a78d7b8b35ab174e59d410af70d257`  
		Last Modified: Tue, 12 Nov 2024 16:00:16 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:23d2e1f65f73a35eb78b1b28fd68d7c1afb54f666591c04bcd3c16d30c96bc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67790042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b248a8c7acfb43452ba7e26d3295d2ccc04591a6e674dd2d21bdc45de3f447d7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b2279cee7374c65ae079e8ccdceeeb8b20c07ffc727e5b7cd595285b44a3a0`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 15.5 MB (15544048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:81ac6e124e736bf967e063a3be5ee9b9bc7a1db57f6f079af2e4f756295f352c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81d5ecfe36c80b4b6452433e578e91ccf9f1f0fb214f9ce715756e93f6588b0`

```dockerfile
```

-	Layers:
	-	`sha256:95096dac33f7eff76e3eba5f7831fc981095785df44edb3b25fe21023899b42a`  
		Last Modified: Tue, 03 Dec 2024 05:39:10 GMT  
		Size: 4.5 MB (4489917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:831bc2da230f1470d9903f490c7d5b04257b7e79ab6f7c41792d2f326379e813`  
		Last Modified: Tue, 03 Dec 2024 05:39:09 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:79f35d801d1e471f31b46e8499d002d0bb08ba26829b87a89b481e981b8a1a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70738339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081736c16bfcf7e7b6410b208723d39963512d09f222f018031e6b377fdc34fc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:862f429b4105c1e5714d48631896837c3ca6f797479296293b7c33c6699eae95`  
		Last Modified: Tue, 03 Dec 2024 01:27:25 GMT  
		Size: 54.7 MB (54676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ac5b88f14d979c6f071eb85aa8a772f827338af23171657add5b5e4fc91e2e`  
		Last Modified: Tue, 03 Dec 2024 02:14:36 GMT  
		Size: 16.1 MB (16062064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b682a0742c1a6381c26d03803ccca7a0f2619d756c223d42fad73eaf58f7533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4493522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844f4f11fe8d04e3b69e4f23063bf7551dcd49afa2df8b22ff09ab932d85f1a8`

```dockerfile
```

-	Layers:
	-	`sha256:2708918bcd4c0cd8a9295c30d52757ec544382da6221ae3e99b0c308054e3e91`  
		Last Modified: Tue, 03 Dec 2024 02:14:35 GMT  
		Size: 4.5 MB (4486744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d34f64a1c514c02f7b13010a041e7b1c35aa623aff72b601bb643cd6ba4519f5`  
		Last Modified: Tue, 03 Dec 2024 02:14:36 GMT  
		Size: 6.8 KB (6778 bytes)  
		MIME: application/vnd.in-toto+json
