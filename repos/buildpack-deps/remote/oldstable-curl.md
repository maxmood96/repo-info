## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:e12cc200eb5a9d13ffb2385b6378f5ee56e6e070b08c6d0fbd097d9a5eb18c04
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
$ docker pull buildpack-deps@sha256:9f05b801245865e03fdc913501b6467ffeda1a1531108c4d9a76c1cd2617b1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69297250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152266dcccb51266dc8095bb3b6448832c4ba9308d6195c269e03003fd917b4b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2377065f3b700cf1b5e391d26c572c8b91892dd44acd75deebdab5e403b23175`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 15.6 MB (15558293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:54bd79c59ac63e754ae8609c3a63c7092daf7510b78a230984d463debb56c65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d52563b5535769963ee8723c777a3335b168e3f53f2bb5b47392af8cfb18a9`

```dockerfile
```

-	Layers:
	-	`sha256:8bbd3f7886f96209b3509f4786600e51b9c3a65b8cb277d385ae371606660860`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 4.5 MB (4485627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3898fa5b0ce10f7bdce2b255187d512d1d82461941b32250e31b6ad7140c5a5f`  
		Last Modified: Tue, 24 Dec 2024 22:15:26 GMT  
		Size: 6.8 KB (6801 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3bc819fb65ff39d8d6d3c29cf7feadd21b3c518e9a129cf12a4d137d765b2a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63698604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aba920290612b71739e7f66654b2824689756bf1e97973bf0f2bfad2c81357`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 24 Dec 2024 21:34:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:709fbc835081f3d738aefdb318cb058ebdd40a4f2868ac5c5605b614336082cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118f311b73d58cd869f276c771003f99ad619d08e755f7fd695933405c3ce3aa`

```dockerfile
```

-	Layers:
	-	`sha256:1ec0b08d0b6d41a5248c133c7763f4bf635d3e822f0cafe655cea8b68518ed15`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 4.5 MB (4487263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8244277bb9dd34ce818dcebd94b67d3965917748d6b78dc1004c7b49000dbf2b`  
		Last Modified: Wed, 25 Dec 2024 03:44:14 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0cd6bb85842e1f1b6673cce1a956c951f6cf82bf93842a0a932d784c2f50dd8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67789715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123ec5e4a187b2914acdd51c638b3d67de9daac3210c4f7cbdd457d10c45a95c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:929d94da80b37d7ef4fa809ea9dc8b949810de3728f2964e69f918fbb9bd4dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f40d156c1d4539234d3b90db4cc68e535172ceb21a68d28542e645a0fa08e16`

```dockerfile
```

-	Layers:
	-	`sha256:2439bef66bed2ae0fad69de5d5a58b9c93e7c5745fcc9cad4f95fe08a72b681e`  
		Last Modified: Wed, 25 Dec 2024 01:49:43 GMT  
		Size: 4.5 MB (4485241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ce80fa4a2fbdf02158d83f301532f7da473e8b34a99d974e26a070d58320877`  
		Last Modified: Wed, 25 Dec 2024 01:49:43 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0f92fcd74736dbb2107826d004713c8aa8e9b82dbe18b5b93ee22144fbd97eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70738009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e18773d3d6b6827daffcf05b3138aba171c0dc9114b96337ab12b93cee80f74`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a55e8c1d476cce2b4e35296e308f64a29659366cc595b7e6019851c3e8bbe7cf`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 54.7 MB (54676016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30483a4cb9e6228b018657587065a3e6487de3276661a2330332744722b7a439`  
		Last Modified: Tue, 24 Dec 2024 22:14:51 GMT  
		Size: 16.1 MB (16061993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d10421d92e57972d8c53dd19130102918a8dcfc57d92feeca836659e5f933fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4488847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c78bea6855f07b9920ca334f7e11f67c93d7134e44abac421ad728ac715ad41`

```dockerfile
```

-	Layers:
	-	`sha256:a1afa6cd8cd235caa2e12ad4b6dba747b5de8e36b7f7f30d5fa8e98be8dd2ee8`  
		Last Modified: Tue, 24 Dec 2024 22:14:50 GMT  
		Size: 4.5 MB (4482068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f6db7dc7e8d09cea83d9577a7b897e65be5e1becae24e1afd60ef49ebf22b46`  
		Last Modified: Tue, 24 Dec 2024 22:14:49 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json
