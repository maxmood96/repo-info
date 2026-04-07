## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:3b4580d0a86f08f0bf40f21144bda643c016483aad7c2ba1e844741c74b45ce3
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
$ docker pull buildpack-deps@sha256:4ce640be480d76a40f42f631058d68bd7fc3207b8f4943420081ae45dc86e629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69553469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7ced37feba289b8050808976607ffccec900ef3926416bac4de015cc1c1305`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d9f854f908f28a433fd2d5b08b5e68ee58c9ec953dac233ca6864ced59f24`  
		Last Modified: Tue, 07 Apr 2026 01:47:01 GMT  
		Size: 15.8 MB (15790676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8f8c3704afcfc6c450e0174829e637c2b2ec22a1e1593831b6f9e4fbdda3f05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4644283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da02bc154a554e4dddd900a8f3bb044a3afa592e62ac482566c984f52d6161c2`

```dockerfile
```

-	Layers:
	-	`sha256:16099c8f5d568ca38cb5a0fadb25e143f6e3a9bd9167df847333511606496bb8`  
		Last Modified: Tue, 07 Apr 2026 01:47:01 GMT  
		Size: 4.6 MB (4637519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1aad672199ed0b2190764685a285b3d2bb9db601d661a9243eaf4570d753e9e`  
		Last Modified: Tue, 07 Apr 2026 01:47:00 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b772594a94c4ce7b9f9e809fbcd7940e4ab37cb97ab95878e0a7780396d5954c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63959025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e822005a4819a0f1379156bc13519ed63b7da30dc764f3601319b5918f5e183`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:00:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dc8695d526078f14ae00d8def0c6b77226df91b02937f7fe93806b494d0eed07`  
		Last Modified: Tue, 07 Apr 2026 00:59:40 GMT  
		Size: 49.1 MB (49053930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2f7a30a3127c8f109eb33c9b6e0a069dc1bbaf940f09c9ad55a2749c25bb59`  
		Last Modified: Tue, 07 Apr 2026 02:00:52 GMT  
		Size: 14.9 MB (14905095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb25f0ab281ec7b4f21503771d76320ae9b9ed54a6ae48af59e590c3c4d08802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4645983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca48e21c81dfa04ae8e9ba76ee0f9e4169691a736c165eb1ad9e5218a103499`

```dockerfile
```

-	Layers:
	-	`sha256:29f2cfaee64b2bd9e2eedaef8208d0bba093c37702e69f95309aeb23c79572d4`  
		Last Modified: Tue, 07 Apr 2026 02:00:58 GMT  
		Size: 4.6 MB (4639155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e630da9615fb9f5d4f73ad770bf7acdf0280099bd9eaf8af8a7a861b8db3a1ec`  
		Last Modified: Tue, 07 Apr 2026 02:00:51 GMT  
		Size: 6.8 KB (6828 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3bd49701c2e84fcdb0173b90bb596b86643a67fb04c9f35ca26cef94b5abf007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68022477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521117a4bc96f355c9e81a41078eccf2206b8bca5295cfd035c2aea4fb43b93a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:50:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345eb533c7aeb250dbac747a6aa1b325697577f8ad9955a623ef30caa4570d0e`  
		Last Modified: Tue, 07 Apr 2026 01:50:17 GMT  
		Size: 15.8 MB (15774862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2688628261181a301ffd60af313685a809cf935ca689e9f0ec5fa850be0f2192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4643977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d830298e0220512f2efed81d88090481f940f2ebae18d58aebee638bcd23c929`

```dockerfile
```

-	Layers:
	-	`sha256:501f8149a0b3f51d3d779a5497819d8bc9452a4ba52224cd4022b15f93f58612`  
		Last Modified: Tue, 07 Apr 2026 01:50:16 GMT  
		Size: 4.6 MB (4637133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018c13c193b1dde9c8f3c15aee5c486b8fd288eead93b109f40ff9611ac24512`  
		Last Modified: Tue, 07 Apr 2026 01:50:16 GMT  
		Size: 6.8 KB (6844 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6b880b11f35c35c60f65ee0dca15efebe9ad51b04d8d94cf60b73b5bc9355b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70998248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fcda4bc8e14438b86e8181356eca7b3615d306d104f07fed3d16c80b21400e5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:46:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:17c3ebdef14b8265937ec7a01f6bd551a86fc0903b2144405f77b14942f88fac`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 54.7 MB (54702589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7d7ea2b68c41d012b622a11d60c4b7330f09ed012ac9774c3894afce154803`  
		Last Modified: Tue, 07 Apr 2026 01:46:11 GMT  
		Size: 16.3 MB (16295659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7a8257eccafbbe56178a7458911c43a4ea05bbe38b19fe92cac6e33b57ffe1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4640763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8837395334e162d6f955063ea7ba8e226c2899b6ba704023321456a0732d2ce0`

```dockerfile
```

-	Layers:
	-	`sha256:ad006909ff315e8695b187222dcb2a02fb0040a880e495bdf9a1601bbbbf0e68`  
		Last Modified: Tue, 07 Apr 2026 01:46:11 GMT  
		Size: 4.6 MB (4634022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ad3125b07c502e0991f3600cc27cc675e566fcceae41b22b47dd4ce9b39450`  
		Last Modified: Tue, 07 Apr 2026 01:46:10 GMT  
		Size: 6.7 KB (6741 bytes)  
		MIME: application/vnd.in-toto+json
