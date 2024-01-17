## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:f92a612d07107b2b44e7bc2acbb1603f17b79d0bbdea0ed51df6bbff217c743a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:19363edbd2a9dfe1656b4db143381912401905c96f5485deb0504d2f00fd3113
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142070901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eedf4754c3267f7b41b69eafe38345244cc7fddba17988f78745efef9f14ac7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:38 GMT
ADD file:221c5996f1ff4dd71764ca719f363e27bb329a807e397f6654cbb3c478c54c9e in / 
# Thu, 11 Jan 2024 02:40:38 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:38:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5c06b5f92f5d425b6a1eca65d06813d5da1bf325255b6cdab64db03a7ee0d47`  
		Last Modified: Thu, 11 Jan 2024 02:47:11 GMT  
		Size: 49.6 MB (49562052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b14ab6cee5b8a008ac52067ba895976219bd813b8d4aa739a74ba5ce9121594`  
		Last Modified: Thu, 11 Jan 2024 04:48:48 GMT  
		Size: 26.5 MB (26464231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff2dc641f56a664434579c2a3968b944814e7a5a7a1854be341b1aed5c02919`  
		Last Modified: Wed, 17 Jan 2024 02:04:08 GMT  
		Size: 66.0 MB (66044618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4cd28025bb7837b1e27e19db3d308813d759e5f18d45f3c8311ea579c0c84723
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135893523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d165b5d8ba7aa3990b45735abedbee0737375ac9e2a90fb820472f4fa2fd8cac`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:51:35 GMT
ADD file:406477db7977cf7bae3dd986446192c7a9c9187721f800f6414add12009ed4fd in / 
# Thu, 11 Jan 2024 01:51:35 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:02:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:58:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ffe09ad7d6788d69349e61610eec99edf75d529a8f29e51e982f323dd5b39a9`  
		Last Modified: Thu, 11 Jan 2024 01:57:42 GMT  
		Size: 47.3 MB (47275273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dbe43ce8740ef7b4c0109654d60ec4abac22aef1e893ddf0a49dc137bd8ece`  
		Last Modified: Thu, 11 Jan 2024 07:09:58 GMT  
		Size: 24.9 MB (24928594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1fc82fe5ed5b6759b1735e940eae002d9e81d2c36a2ffb7816989a3f4ca2f8`  
		Last Modified: Wed, 17 Jan 2024 02:05:50 GMT  
		Size: 63.7 MB (63689656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:266f11bc38b9e7924525314e63f37932ed7b84f55d8d2b243685f7e70714e877
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130223490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964679ae826b60ffd6272626f475f77ad921d8c7880e1eeca5910b991ac8e08b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:45:43 GMT
ADD file:2578bbd6242f569b630ed2a8dbbe60a6317a1fd910aebe4814313b4c0eb7a482 in / 
# Thu, 11 Jan 2024 02:45:44 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:50:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d77eb11f48fd53e8f4a4cad655e31f2fb5f91177fb35abe347a055a3352eff1b`  
		Last Modified: Thu, 11 Jan 2024 02:53:33 GMT  
		Size: 45.1 MB (45063448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37916331c99d3b698aae6553fb6c2a2c76d2cdb8dea2d3cc6e825c690f03420`  
		Last Modified: Thu, 11 Jan 2024 03:34:33 GMT  
		Size: 24.1 MB (24103233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42358cf09f8f09dfcecaf138e675dbd09b2023d276cc9da817d425c3e1be0638`  
		Last Modified: Wed, 17 Jan 2024 02:23:52 GMT  
		Size: 61.1 MB (61056809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7ad8e9d6e532b13e06349e336aa98c8b366940a5844787d177dafcb1aa0d14ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141771564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b782a214aeb3f0d02d9e90ae147c2d055010e419bf054f1ef6d396cbfb1d21`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:31 GMT
ADD file:8d6ad5a2ffd09b80912ad6e70510597c7fc97adbf4f68d39203c3711ddb56a51 in / 
# Thu, 11 Jan 2024 02:42:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:31:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:30:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e5d062756698b7a985fb1a991d4720ffd4d0a2a6c27002bf3939d178a81e7024`  
		Last Modified: Thu, 11 Jan 2024 02:48:34 GMT  
		Size: 49.6 MB (49594187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0407b18fc98c19c25cb39b17797717f780dc263659c85f55c6b854e1b6aab7d3`  
		Last Modified: Thu, 11 Jan 2024 09:37:41 GMT  
		Size: 26.0 MB (26014238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d5f90a0b648d291dc555ad20c520c021f23bb1b7a8ff034cab96603d3ed3ab`  
		Last Modified: Wed, 17 Jan 2024 03:03:50 GMT  
		Size: 66.2 MB (66163139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bb8bf8fb870a101defac645277e670044c02d44d8d993e9348e765e2ecca968e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145795913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf5b71c7437bea80e375972cda4a7c2a587d0d95415718ff520c08b876a46e7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:24 GMT
ADD file:5564e4ab4c2aca360aa2b99bcb8c9c77e6d97554833ae3cc9bb2f49ed35e25b2 in / 
# Thu, 11 Jan 2024 02:41:24 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:39:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:48:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a827afb392949e39b5beea804bcbbd7be98a07848f45ead6a59e020bce5836dc`  
		Last Modified: Thu, 11 Jan 2024 02:48:52 GMT  
		Size: 50.5 MB (50527068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181d3088fd6488ff4296a6d76024c5ceabebb089069d60b6dcbf62cc62624985`  
		Last Modified: Thu, 11 Jan 2024 04:47:28 GMT  
		Size: 27.5 MB (27453882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457d36b28a2aeba3c1858efb1b7d9b29850cebdf237f46d022041ed8ab768261`  
		Last Modified: Wed, 17 Jan 2024 01:55:31 GMT  
		Size: 67.8 MB (67814963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1cffa5ea8b6d7baafebec1e42d5aca655fa55e9d1160ca4beb362a0107d2a685
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140461390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dffd710a6c3cb41fad93249cfab50066ab8d917565163f18b5d1c11662eeb5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:18:24 GMT
ADD file:f8968c17bd3825e4f058fd68c683a3c699e06368b69577a14d575a0c3ac70e6c in / 
# Thu, 11 Jan 2024 02:18:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:15:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:39:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc5cc64b8a2f7c7d0c78917ac707955e566c39f9c62003870eb7cd32f7b23a5f`  
		Last Modified: Thu, 11 Jan 2024 02:30:01 GMT  
		Size: 49.3 MB (49333270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136a6eeb1b81bae44e0e846833442693a689a375fce576961be0a2c167f5f861`  
		Last Modified: Thu, 11 Jan 2024 03:34:44 GMT  
		Size: 26.2 MB (26204931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2985bddef47ea1dfc27e743db75cb03ec8ee48a2cf011563f6c77a462f0681`  
		Last Modified: Wed, 17 Jan 2024 02:58:41 GMT  
		Size: 64.9 MB (64923189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d0cab60a258488f468e2cef7926a5d8326867ad69fe92468ba6e9cc4edc2a095
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153951879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5057a1390ed613705b108b03eb77025321fff705280ebb36345bacdcbd416019`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:16 GMT
ADD file:d68448f447d4318f3f9fad32f62806e0a419160a92848f345b24ec3a1aa68cf9 in / 
# Thu, 11 Jan 2024 02:37:19 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:18:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:45:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:451fd7c87652550c3d81b74039588f9cc1098943015d72618adc689c50a31de3`  
		Last Modified: Thu, 11 Jan 2024 02:43:06 GMT  
		Size: 53.4 MB (53435762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0721dab59d6faf980a2731617cf00ce4d4f5118003d8d0c3dad0ce0ff7844f94`  
		Last Modified: Thu, 11 Jan 2024 07:27:03 GMT  
		Size: 29.0 MB (28965246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb199702dbdc23cd11d17b5357a05a683047541ed3bd5073c3754b7e13583f00`  
		Last Modified: Wed, 17 Jan 2024 03:28:11 GMT  
		Size: 71.6 MB (71550871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a5a9cdabebaf8d6102ddc4ced4a68009160c237a2adb9a54cab6a255a5b98f76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143421634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bca060e10c2e9bc74dfcead9b297de21fb1d7843d2256c407774f8c06b73b37`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:48:25 GMT
ADD file:3ce2a6c625c267468f6ecc7899fd855c1705b7efb767d466e8b5e859b1047897 in / 
# Thu, 11 Jan 2024 01:48:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:15:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:14c1c69c5e90f50e1791d192ea58f134dbc8ecc231a5b815d4c7ee99ef3a1ff7`  
		Last Modified: Thu, 11 Jan 2024 01:53:03 GMT  
		Size: 49.1 MB (49091863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3694e83d440b396cbb77938e6510f4437f21e56dc3bfaed630e6caab9214d`  
		Last Modified: Thu, 11 Jan 2024 02:23:52 GMT  
		Size: 27.2 MB (27199817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087624ac8ae70d1523e962effa1e411b8630e30b36379a63a875a0971bd10c2f`  
		Last Modified: Wed, 17 Jan 2024 04:06:00 GMT  
		Size: 67.1 MB (67129954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
