## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:851eb6e7711e74321e26b450f313331b290fa06f3e3434faf1d79c3fc015d384
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
$ docker pull buildpack-deps@sha256:4c2c3d8f36a72c460b9271b3a3a0ca6b774675cfbce6280018d0643b1b0c780b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69520766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5612c473b433797e3474da98e8edbbddfd950215ebee530f0e980a53008d5c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:28:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba74ac44652a153d2c2058f766703586a059b3775323934bb7195c47e2f7244`  
		Last Modified: Tue, 04 Nov 2025 00:28:27 GMT  
		Size: 15.8 MB (15764072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1d00e8c9f1e91e00bc809eb6158e61ddc62613d78dac2ac3cf2a92ab4324ca45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160f9f0db338ce197bdf7900c474203a90af467c0fc9419768a64b433e3125e9`

```dockerfile
```

-	Layers:
	-	`sha256:287f21975c553edd5a7cb1fd770d7c13b07664db51d25282293e5336cf40e48d`  
		Last Modified: Tue, 04 Nov 2025 11:20:31 GMT  
		Size: 4.6 MB (4629099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06f1b9db4c655ff4293141e1605067317eeee3b94120943d9f83c64d0fc1173c`  
		Last Modified: Tue, 04 Nov 2025 11:20:32 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2ee952b0de2bca46480797ee02d61057fa7c212fbc4042f15eb959695c132511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63926098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a066c07422088ac00ae4092160bf099ee85ca7406740a9d4732e128a88cb5c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:39:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5c1506f20ad482dc397205cd3591be6cba02d9c91b672e522a63c2a72e7a905b`  
		Last Modified: Tue, 04 Nov 2025 00:12:38 GMT  
		Size: 49.0 MB (49046665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f1b30eac0dfe5f0a5d3317a044901048aa4a6ad0dad80db659db81872ce4ee`  
		Last Modified: Tue, 04 Nov 2025 00:39:44 GMT  
		Size: 14.9 MB (14879433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:55d95402090f85bc069bc9959bce12feadd2d4851e1bca553958ff0a639170dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3981cafb21f22680fe0b1309dee94dc091ec89419d85d10d0a61cc39fb188279`

```dockerfile
```

-	Layers:
	-	`sha256:c537c38b80d9e632442cc311615bdb3e3f21d8df5f96a852844f0ab54f174be3`  
		Last Modified: Tue, 04 Nov 2025 09:49:44 GMT  
		Size: 4.6 MB (4630735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3da013cd418bca7b13f7d94bfe902c7d6b13288a7d01592b5399ccc99b5297f5`  
		Last Modified: Tue, 04 Nov 2025 09:49:44 GMT  
		Size: 6.8 KB (6828 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:675cbbd7c3300e8d57a67e14302fae84d5f559aa80206709a839f895fa22b74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68007480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a63b965fdf847071dafaa8b29273c8a328a21dbf2f2a9a4faab377857969f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:30:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4de5de87e4df8d0116d41cc30ea033d913f47280433132cdf3c66653327716`  
		Last Modified: Tue, 04 Nov 2025 00:30:31 GMT  
		Size: 15.7 MB (15749511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d0f3fa11d854556893cc65e33d797af9c2a87c9c20d830530d3bc03c42449801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f233f3477dcd659d0e71c258472382d2242cf90d0f22104c8f8287de71263c9`

```dockerfile
```

-	Layers:
	-	`sha256:65e5c66b3c1f3fe55fe2fb0406d77b559659c4308502843ddae5d93abb400ec7`  
		Last Modified: Tue, 04 Nov 2025 09:49:40 GMT  
		Size: 4.6 MB (4628713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f857f9c138768d6383dafd4d9e5fadc12d1dce30159c77fb9f92f19e55a0bc`  
		Last Modified: Tue, 04 Nov 2025 09:49:43 GMT  
		Size: 6.8 KB (6844 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fe9c7dfa75f35ee80d000b134939b02923a0c9b50e42a317aa8b872385fd777a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008757b22448adea6f8bb7b7c069d47db59d41e98fdf4433c462fd5240a958bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 01:31:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e60c3e4fbf8c19df439b90c2a7f7bbd43579378a671c1afe66083570c61159f0`  
		Last Modified: Tue, 04 Nov 2025 00:13:43 GMT  
		Size: 54.7 MB (54699883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026a2729c1c9b0b37b2452459d485034dac315dc6282574bd782d47cc731213b`  
		Last Modified: Tue, 04 Nov 2025 01:31:50 GMT  
		Size: 16.3 MB (16267789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ea38dac56a6a07b407e2411ee84b7e56bf5b076edee535e20d143225ade39a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9e2c3b717d07722ef5f6707957dd4e0eff31bc95ae20c15fb3963c6852f910`

```dockerfile
```

-	Layers:
	-	`sha256:23082e3795588cb070e539aa3c2fe9cb5608ad6c5289f2914e3b2e943ee0f514`  
		Last Modified: Tue, 04 Nov 2025 09:49:34 GMT  
		Size: 4.6 MB (4625602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ccec8837c174e2b4c6e193711aa490be14b1b6051c60c223b06d40efe0a8fae`  
		Last Modified: Tue, 04 Nov 2025 09:49:35 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
