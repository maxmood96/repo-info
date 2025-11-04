## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:9929ee9000727456db2815f29d31728f73b4df5de9f1dc2a6aa9997d06feb4cd
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

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6af1ee3db434d53b93b0ddf0739f7c3bad5fd332c6c8df9e78fac1fc059713a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124275923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1db84c973f3281f3c5d3fc374cef8cd66fbb921c528fb8b106950cf43a5eee8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:28:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:14:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:54e217875226b0af2272d40b4ff7389d8caf7d0b8c528152c0daa8b5716a1398`  
		Last Modified: Tue, 04 Nov 2025 04:14:47 GMT  
		Size: 54.8 MB (54755157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b731cf23585a8b90e199c4e94bebf9ef9931f9a0e95c1b86c01938a021526527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7919476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47fc33a4d08dcdd048bceb2c6438bb0cb8cf2577c7935e388ae733eda4f71fb`

```dockerfile
```

-	Layers:
	-	`sha256:71f503fb75e22ddc70871a51bac5a02afeaa9de02973eb9d2486d7c3fd1fe410`  
		Last Modified: Tue, 04 Nov 2025 11:20:45 GMT  
		Size: 7.9 MB (7912160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82fca4c2896fc049ccad04271c89e17aae3150a8f0ef7fbc8f2edc3b8cad3064`  
		Last Modified: Tue, 04 Nov 2025 11:20:46 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:11d9e308e81922671b2240322885c4c14a72b14aefc38be079038488e71e4ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114555340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7233fc53c9ed6a49bad0a5feee08aaa4dc79bfae33f29b759c1b4a68504c8e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:39:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:18:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:20c893d382c6a3a387d306503fe98454c488585afdfaacc5bfb4f34dcbbd7816`  
		Last Modified: Tue, 04 Nov 2025 02:18:45 GMT  
		Size: 50.6 MB (50629242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1efa85200eea28cffb6933cfe085063235f0b4db90e26ff479ef9c7a5c7f5dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00e104d6b20630268bb5df3dad5cd2008fce522c709d80e6553452efd6d87e6`

```dockerfile
```

-	Layers:
	-	`sha256:92294b315980cee56093e51f981abd886a7f4a2f41c58187aa5a0892e693d3f3`  
		Last Modified: Tue, 04 Nov 2025 09:49:03 GMT  
		Size: 7.9 MB (7913562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d780445ce3400e1410b1ad1e472e224b423ef2fa34acccf484d4eff945a215f1`  
		Last Modified: Tue, 04 Nov 2025 09:49:04 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b928804a749151536132bd9478c990511f28a215b99c5d99a754f05954b5ac4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122874053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ea4ccf359b030c1417ddd771c35df5b39745c975d93cf91ea4a42318a141a4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:30:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:29:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4a0b5305a450275a04f32f7333d98eb8edca9aa808f9904a4e0eb28b3cf08b52`  
		Last Modified: Tue, 04 Nov 2025 01:29:57 GMT  
		Size: 54.9 MB (54866573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3ca657519aa070b14c600eb415e839fde9cf71ce86cf612e96fdb613ca058699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501fd4e682d8a6f43abeacc82ac5114ba7b21e11bb35ebfe15e314de5252636f`

```dockerfile
```

-	Layers:
	-	`sha256:41c5b794c9d7b4edc2d7e646127c2b30ae04bf3cc8b496b0ed2eab8f925a9566`  
		Last Modified: Tue, 04 Nov 2025 09:48:58 GMT  
		Size: 7.9 MB (7917894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62044a9319185c87fc12ef91b6ba62d4932db7eebd6389dde64508106693696b`  
		Last Modified: Tue, 04 Nov 2025 09:48:59 GMT  
		Size: 7.4 KB (7396 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:553c37d1e0961539b56d82fc3a16c1c994224f230c09fd607df0a00d02cfeba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127016442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1572600ad8f52c7aa1b97d08cd9558aafd05167806b5a1f317a6182e116beeb8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 01:31:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:19:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:f50dec7cb21dfb46a6779e044e96aaf94494596cad5491b67d178fd81fb6029c`  
		Last Modified: Tue, 04 Nov 2025 02:20:12 GMT  
		Size: 56.0 MB (56048770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6bc050acb23889f38d898a318ff0fc4cac97836aa28ac6ba9c24387fb746e208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586894acefe131fb911aeb19802cb9c6389829be7fb8436326164787b0b47b28`

```dockerfile
```

-	Layers:
	-	`sha256:518a262302daa329655fcf91d3443bd7366c1d0f69c66146480958a3f2221f53`  
		Last Modified: Tue, 04 Nov 2025 09:49:00 GMT  
		Size: 7.9 MB (7907730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7224d3b2ac67d9f2c3142c057442d3e183899c3f32265f4c428b594868efa22`  
		Last Modified: Tue, 04 Nov 2025 09:49:01 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json
