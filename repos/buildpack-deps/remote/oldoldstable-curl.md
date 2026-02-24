## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:ec5edaa6b241fccdf03ff77f005a0895b4e0abec60b210639cfd5acab8e43f48
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
$ docker pull buildpack-deps@sha256:2e4d01e3d55bfb83b9fe8100df06c302589a075f9eb21d981d73f5cdcb6ce2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69547181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396c6bc8a1db2104eee663f06bca4f375ef6364961314dbae8459f5cd22b9ecc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:19:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe71fa68737bfefafea69e4a0c5b69941285043380076279a4d65e82b5973e`  
		Last Modified: Tue, 24 Feb 2026 19:19:14 GMT  
		Size: 15.8 MB (15790747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2dc9a059860ae12ff513d1619de9eac521287fd15672558f8a079b5615515cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4645907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c21b9e526cc0376e9188a4e8f5865f3c0044afb301abecff95e56a2dfd63c66`

```dockerfile
```

-	Layers:
	-	`sha256:05d9b1b9ac8a6acda7e35283cbdf5a57cccb9d00e078e08e72959af7ecb6db79`  
		Last Modified: Tue, 24 Feb 2026 19:19:13 GMT  
		Size: 4.6 MB (4639143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:844ae77436b095c653cf6cefddfecd8d4c2a1f1ab457bc18c3486710a7be00d8`  
		Last Modified: Tue, 24 Feb 2026 19:19:13 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:bbd5f6a57cbdbacbdc8d775677bae75a84860efab16e03f04645f5375b80b2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63952674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61a3bf0673893285e3ae1cfab0aca552e9eb956f01858efda03f9ed2777d285`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:02:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dada255a3ad6614e8b2a389545f0625a8ca4a68f069cd24789cbdcf7a89bee05`  
		Last Modified: Tue, 24 Feb 2026 18:42:25 GMT  
		Size: 49.0 MB (49047560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6350b59ed962425f695241e787bf8023af23ee4d06b078f82307ec998a697a`  
		Last Modified: Tue, 24 Feb 2026 20:02:14 GMT  
		Size: 14.9 MB (14905114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:794475307a915a157b32b19616e05272a82c4570f71d6ffa30ba284439bc714f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4647606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88dca60cc46e5720281b1fa8395c21fbd38a2e3f3ac8d4efbb16c031a89d1cf`

```dockerfile
```

-	Layers:
	-	`sha256:efe6e59f200c609424fecc39d03f802d509c154c6e5e14a318b3f279d2efc5fb`  
		Last Modified: Tue, 24 Feb 2026 20:02:14 GMT  
		Size: 4.6 MB (4640779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c09cd3ae87d03b8b439b57d67948984d367c9833d874d9c14aee707eb984a0ff`  
		Last Modified: Tue, 24 Feb 2026 20:02:14 GMT  
		Size: 6.8 KB (6827 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0a5d0335edf2ef3f5cf4d057158f4f49482a4a7f6938e657a5f8f949d5b39330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68033205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646a82ae180bf46d1a762af278b2f9cd74dadb7a38c0366c9b0f057a2d3d4a61`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:24:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6dd0e9da832194c696500da7078d1cd12126c89f2a0283b7c424f7ffb55413`  
		Last Modified: Tue, 24 Feb 2026 19:24:15 GMT  
		Size: 15.8 MB (15774813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00dca9f6d0a537641dcd081982fdd8f39cd0393517946782a50bd7bd4539f04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4645601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d8e6ba0482e8cff52f5bb97dc9f4b04ad1548232e43ea11cc506039b5198aa`

```dockerfile
```

-	Layers:
	-	`sha256:460ec222098feb8eb262a76eb23c114cbe414a97a2e31e4b9f5fe8aae2afbdab`  
		Last Modified: Tue, 24 Feb 2026 19:24:14 GMT  
		Size: 4.6 MB (4638757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c7201b3cc53d845a5d7648da8fbe7563ddb64c83e83f9859c65342fd4938797`  
		Last Modified: Tue, 24 Feb 2026 19:24:14 GMT  
		Size: 6.8 KB (6844 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5f182d7335acfd1ed580394fb941d2fe7425664de962a4b44cc429dafdfae5a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70995325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e358863015c678e48bc703dc0e51ca624c0257151198d5799116fa5ac4186e34`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:24:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:be7de57c5a292b6137b558f622789891088c38f02c67ce301a1559809fbe8ae2`  
		Last Modified: Tue, 24 Feb 2026 18:42:22 GMT  
		Size: 54.7 MB (54699784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ba919300e8846f159f61d3dad9bc45f102d2250de1dac9da8674f83e4e628`  
		Last Modified: Tue, 24 Feb 2026 19:24:44 GMT  
		Size: 16.3 MB (16295541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e17b215b71ad4d9df944ea1a2c725968708fb12a9bc0144fa5e583c52993701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4642388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436eb868d36d8f9615c15d89787370f880d64b42f25275eda34549dcfee7a74f`

```dockerfile
```

-	Layers:
	-	`sha256:ee8eb6c488f6e5d323fd94eb39bb78e0a71a44ec59c55ecb48c944110431cac4`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 4.6 MB (4635646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0dfffb7b3501b675999ac33bb2f5a3217493e89555e24f3de1fda3628f8f3a1`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
