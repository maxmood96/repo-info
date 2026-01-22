## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:0c491fe223bc1a9a8d1261bc6fb726e067091f27783e5132f2b257dca928202a
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
$ docker pull buildpack-deps@sha256:7b2a550c7b3f097f449478d1325fe09c4fbcf1425a382e8eaac5c33aa22df434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69520762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f37f7de10078e1791264cd95f3823cbcaf59cfdb31975ff4f96d00f66d09552`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24af405f2300f6988a2a2eaae4ec7393c0f9119fea3a400a1864fa5905a9bb66`  
		Last Modified: Tue, 13 Jan 2026 02:09:22 GMT  
		Size: 15.8 MB (15764316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cd6843c53aeaaaf8a019f53199a3a144e52b7912b43cc82da6515694339893bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bda746e0663d54a6df96abb6bc37f567455f177571a874f664bba6f282c8ea`

```dockerfile
```

-	Layers:
	-	`sha256:6a42f4179c36175ce18c9d4f82e97f9ed8385c3db3857d83088908868124f332`  
		Last Modified: Tue, 13 Jan 2026 02:09:16 GMT  
		Size: 4.6 MB (4629099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1cd08c55aaf762e3efd7fa9e0ed76f32eb71bad7741af1ec294d4d4eb698c`  
		Last Modified: Tue, 13 Jan 2026 05:22:24 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dc057dcea601046af98db5861af526dbefba73bd96d7f15533467ff0496fca0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63926114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f584f2f69ecb5db9079e4b043318c71775d61b038f3da563df5a8cc92d25bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:57:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5d86a038b54ede2ada385178a3a13e9fc7833f9952c07b251c404c3aa117dcd4`  
		Last Modified: Tue, 13 Jan 2026 00:41:24 GMT  
		Size: 49.0 MB (49046458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd38532089c34c92931050565b084061d36d5f2907633b524122c2d6f089b42a`  
		Last Modified: Tue, 13 Jan 2026 02:57:35 GMT  
		Size: 14.9 MB (14879656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:99a4f0efa4445d5cbccb9f2b57c5da0eba665dc404a13c10d63fd8f391b3ecaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0b968369ddf06cc85af23d1ce0e6634d0b17cf65c42bfa25221619162fc50e`

```dockerfile
```

-	Layers:
	-	`sha256:d531016f2fe01ebd1c0ef0010b3c8ec7832c8f790d540eb4095574e5c903dbaf`  
		Last Modified: Tue, 13 Jan 2026 05:22:29 GMT  
		Size: 4.6 MB (4630735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b483b0f3532e0ae37ffa822b2e95ca8585bed599c708d51864f6fda94ab78ce`  
		Last Modified: Tue, 13 Jan 2026 05:22:29 GMT  
		Size: 6.8 KB (6828 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3a497c2ad686b90072ee0404e562c9570cc7267ad0ab9ed7960dc48259bf5edf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68007436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40bf61a4679eb655da3c7921b4bad8bf0068d209742ab525e5d2c7adc4484eda`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:13:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6280b099c5251ca1a2b55e8af5af4da252bad1f89325ba7a8344f2dea14e67`  
		Last Modified: Tue, 13 Jan 2026 02:13:33 GMT  
		Size: 15.7 MB (15749667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4b2cb26b5e36037d126851e701de3b28a0f697d9a534d3b1997d8a03425c1847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a53220007c88c78b60ef492d2bb1801a4925db25d5b5d7063252431c7d951e`

```dockerfile
```

-	Layers:
	-	`sha256:0cbb97c355289f9805fd529fda00ae92e456a1a22982f728ac6481c34f596ae1`  
		Last Modified: Tue, 13 Jan 2026 05:22:34 GMT  
		Size: 4.6 MB (4628713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06fc353ab783d32a699b1e8abc265efad09517483d8f5b137f1e0ca9f38345f1`  
		Last Modified: Tue, 13 Jan 2026 05:22:50 GMT  
		Size: 6.8 KB (6844 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4fda28655f211d6ad0cb9d1025f654c03b4f6eb1fb4ce33e2668b2f2e9cf4a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8204ce9bb5ca17ce4e9b771a1ae2501a49abe3f776f776215c10379cd609e1f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e115d265636fc6da528c1f4977e22baefb0bae7061ada6dba677a290e83b246`  
		Last Modified: Tue, 13 Jan 2026 00:41:26 GMT  
		Size: 54.7 MB (54699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed43d5d71f701abde2a62df95258edf0ac9ef3046d49ca25c0f30e57af2985`  
		Last Modified: Tue, 13 Jan 2026 02:02:38 GMT  
		Size: 16.3 MB (16267780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b0dd976b87c1b3f7a33dea3a83dec4d040b5ca699496bfbc19a692c1b9925160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c031f354f312c4abd6e35fab2def2c2abbda48c670cf8fdc99996f89b766b78`

```dockerfile
```

-	Layers:
	-	`sha256:9bc718526a6f7077da7542e875bf55ed1a11e2dc4868b2e058cf47570769b885`  
		Last Modified: Tue, 13 Jan 2026 05:22:55 GMT  
		Size: 4.6 MB (4625602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e0c4bd3ba74ccf785e640ddb2aa587c2168efb87a86da1ada59c432d2862fb`  
		Last Modified: Tue, 13 Jan 2026 05:22:55 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
