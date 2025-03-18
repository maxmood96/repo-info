## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:3ffda0e3887fe5da38c355fa99f77f3afeac8b04bfd310a8046d4388e87536e5
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
$ docker pull buildpack-deps@sha256:05ffb5cfad53eed06c7a2b39f001aa83cbba2477524981ac7db7768c623b32ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69299630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9989d07d1b1cecefde54e5fd90a2683bbdb6d98a9d851c8c311cb8feda7b8a7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae550f4768ad83c7dcc1ef8de6de078a33effa152d846f4604ead4cbb1f414`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 15.6 MB (15558355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ad50238167d3eeaaafbf9c21e20e3bdd2179e8bc34328abdc9c6225ead6ae86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e21d1468b7c2a7851b0d9592cc68764a9d31b1707f1f912b227d4e30dc9d893`

```dockerfile
```

-	Layers:
	-	`sha256:5bf2501c75ff24a3f2593252f824dfd68201c12f8d69bc8ff73ad626a4e7fab5`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 4.5 MB (4485627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5c83905b4b68e848ef45cd089d5e6890e39db97e6958f9bf8c1e81f05dae43`  
		Last Modified: Mon, 17 Mar 2025 23:13:32 GMT  
		Size: 6.8 KB (6801 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:980cb5036fe28323f056442be97e50e5f7f406bfaac6a64f5c528c11487c4d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63700706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36935908306bc83fcc5ed3f8b7597bc6cc391ec67adc1996293cd4d7e3dbc9f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b371c05b17ddc4521fa62e27633ef500c9e18d0922c933dc30ad692d163a6adb`  
		Last Modified: Tue, 25 Feb 2025 01:31:01 GMT  
		Size: 49.0 MB (49026733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7f37fed942ce7eb6947b63b02cebac1a836c49ae19b59c3dfd4d0dafde5e9`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 14.7 MB (14673973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f825d0d4f40316241fe1dc4972626fc738ad42f315280df37eaec16682400cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0de80203df6acea81c3bc88ac27d6a5829e64dd0f2b5540eb16ba40095818c0`

```dockerfile
```

-	Layers:
	-	`sha256:4f5013c38c8227845edc977e621c19c9c996f28a39b5a828567ffae0f493dc4d`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 4.5 MB (4487263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d117a80f010b81ed4a920c2ccdc10549b3f41c798b5ffe5386630d8da0e71eb`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c8ee6187ea3cc91dd6bb40d548257bf6918112c24d15662a38b214191a6cdb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67792398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a95291078f96d17278f56639020d5ee4c92313170ea024c401bea95645076f3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bc92dcf4a3c806f112acf0724041051eab86b13816f8d7286950facb47ec3`  
		Last Modified: Tue, 18 Mar 2025 05:00:00 GMT  
		Size: 15.5 MB (15544004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:87d689a49f90a22c98506df2f84624057188c4660599f2b4b27596be35d7d827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5052c7ee71e6639be55a112e90e711b2be530149c6bbfb88b6c9173d9eace810`

```dockerfile
```

-	Layers:
	-	`sha256:79a3d18eb2a22628a433203d164d6eed64cb7ffbaabc3f2440682659e2518fd5`  
		Last Modified: Tue, 18 Mar 2025 04:59:59 GMT  
		Size: 4.5 MB (4485241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d8d30f571eae89327b9754c1c242a72bbfdbca915694557f2c890e270dc6e45`  
		Last Modified: Tue, 18 Mar 2025 04:59:59 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1e329a86e66a78f5ca6d4e8a21981fc18481ac4b16cfb6d94d707856b30fef28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70740662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df0afe68c64006fd1874372517c98baf2b5dd32c617c141775d2b8ea008beb2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5503af74d5075005e8a2caef8b6b369ec49cf0d7a20dcdd1fe79d68aa4ba6c`  
		Last Modified: Mon, 17 Mar 2025 23:32:34 GMT  
		Size: 16.1 MB (16062045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9c2089c1874aa7a4623416a6fedc3e3b4b236a33595fd9bceeefd017453aca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4488847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fb25bee09ab705c369a51061bf7c3ce6fa2fdad58258feeb83fe3941160d9d`

```dockerfile
```

-	Layers:
	-	`sha256:07c537a9d18b837f84d65bac705e7f9cddd3eb881ca6a4a6a0eb4f2c008c50bc`  
		Last Modified: Mon, 17 Mar 2025 23:32:34 GMT  
		Size: 4.5 MB (4482068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adbffce1b8f52d0fe40323efa1a6b4c690e1d7ce42d84c66ec3d801dbf1b246b`  
		Last Modified: Mon, 17 Mar 2025 23:32:33 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json
