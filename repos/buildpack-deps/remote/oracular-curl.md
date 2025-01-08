## `buildpack-deps:oracular-curl`

```console
$ docker pull buildpack-deps@sha256:5a54dd814c6322f357e43081a669e905c192ed0e4c17cd27e064d0def5fa804c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:oracular-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ea60a237b355b924d37dfe9aac67a3852d8b7c482233cb73265efeb09ae05ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45975452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c44578c4539dd052a272af1de7f824a2b22957771ec3454116fb0e0cdf6b203`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:08360137caccff53ccad4b814b2e19f27aa9fe2a71175550a7f6b13fe243924d in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:31734b193a814b7d6f96f0d11a89c942ca61ac79d819105323c548bf31f98613`  
		Size: 30.6 MB (30601312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb3a0dc114c54fd18d42d481f5d85eb84000d5cd297bd2f753d1290eb36719c`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 15.4 MB (15374140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:957effd5c0cfdec1d2236e1c818d395fb9708f82fde1c0159a51006c10c4db0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b38744fcc95f8c64b212f80dbbf264a20abc2d1a16ea8ec9ae244f28dd1540`

```dockerfile
```

-	Layers:
	-	`sha256:8a09e8f1e8d49e683c807fbae21bec087375e537be6f69b9ce9487ac6f62914e`  
		Last Modified: Tue, 03 Dec 2024 02:29:09 GMT  
		Size: 2.5 MB (2458673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e22805520c08d0bf06b9f9f7cb9b9d661114bc018017f25a45245d6f198ab7`  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:73c945b3d503d44be0dd39a8a3f5396dc07aa17344ef7f13d50dc5a35233c306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2428ec7695bd98edafe42303b40ca4ba3bd6cb2cd70a531dc2778e08123a19af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:5cf848783aed3abcaefd540a7a70f443ef2bead6c50d01e0a72cd1aa6f542081 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c553618cfeea14cb253bd7777b2e3299019b3065e1cb073744b43353379582a7`  
		Size: 27.5 MB (27546971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a00677e72221e7026f8e6b0ed5b47e7316c84195a5d85d7c2cf005d741e670`  
		Last Modified: Tue, 03 Dec 2024 07:40:05 GMT  
		Size: 14.1 MB (14060900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:64158a88b94a807bc6c406afd30c1103e0a1f68b5ac32de7806d44a2139a2b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9439d1914bedbefbf8318533d3206dff74db23f82d6ecd51cc21da18bbb6242e`

```dockerfile
```

-	Layers:
	-	`sha256:b009ed268a6a16395e4b189138dfb01b08a1e04b7a9716b204143d5a7732e0e0`  
		Last Modified: Tue, 03 Dec 2024 07:40:05 GMT  
		Size: 2.5 MB (2460973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6749341c5939dcf0a0a5bfddb6738504b32558cb0fcd532ec7cfe233188ea4f2`  
		Last Modified: Tue, 03 Dec 2024 07:40:04 GMT  
		Size: 7.0 KB (7038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f09db2479b3d7468d20c049a2ea861604f9a93f92357f5556e5953ada059807a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45432259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d138568e5d92a875546b89405710cf9c20c0cb837387f6e522e2dd6d78552a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:11edc0b5b8a0810c86ff8de1ece47e84856118afa9f296152b12c0bdabf33154 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d229850a7784435237486a1406ffb5a4f0a4ac3b993928d18b30ad6853c6845`  
		Last Modified: Wed, 20 Nov 2024 04:18:26 GMT  
		Size: 30.3 MB (30284785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c08bcb2cbebb6d9db3a5ad2c52e975d21aa32088786303f6c521a0bb1f93f0`  
		Last Modified: Tue, 03 Dec 2024 05:41:40 GMT  
		Size: 15.1 MB (15147474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:302f64a92207589244d087350938653e787432e5ec6c888242a21c9244d5d2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5084369ecb31ed6773a085b710f5afb7f8303a0ea405410a36fce2bbadc1fd91`

```dockerfile
```

-	Layers:
	-	`sha256:9b2a5e54b80389f06a288d3c2d31dd9785df28e6b3e45c1c02bb41ec2f5f7e0d`  
		Last Modified: Tue, 03 Dec 2024 05:41:40 GMT  
		Size: 2.5 MB (2459730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10471618780d2cd17e1eb02c1f75d997b02047f3a6cce0d7ddabbb9a94ed840`  
		Last Modified: Tue, 03 Dec 2024 05:41:39 GMT  
		Size: 7.1 KB (7058 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:afcf6137703d492a678411153ac8bf0b6e55855e6d12c748e94ee79e57c7daed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52313161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e08b55ac61d2952ce86a0a9078c907bcae065e32f2b400770ed5b6a16d5bae4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:c92b611280c7d224d58f2a2a7dfdc19380dda99a38e10495643ec0b43d2f3cac in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2039ab37391bfea5163cf2545fcb585344c981096040149e81aec9301f35f97b`  
		Last Modified: Wed, 08 Jan 2025 04:29:06 GMT  
		Size: 35.1 MB (35063190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335ed3d865eafcfc72459a536871a40009d4a399d947a0418657fd44f442c19d`  
		Last Modified: Tue, 03 Dec 2024 04:41:29 GMT  
		Size: 17.2 MB (17249971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7fbed868bdfb8c0fa54ac0a7279ca61b33eeed3c2a9e726ae9bb38d573e0b530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f7fe4f05dc1680e076f9aef3d1bc2134faee073b9ba0bc18b05119256d2fcb`

```dockerfile
```

-	Layers:
	-	`sha256:023e9cee20e6331d60b57fb976920eb158cbbd04e0fd5b4e078a377c498a3564`  
		Last Modified: Tue, 03 Dec 2024 04:41:29 GMT  
		Size: 2.5 MB (2463156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e962bf2a789e982d8814853042d4eae3e2593e723f80be215416b6b2339747f3`  
		Last Modified: Tue, 03 Dec 2024 04:41:28 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:935ce885aaf07bbae20dbdde74e64c6259174a52c31411d4d72246b46db888f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47678420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049e555341f0ccf882cd39e4a089dd2ca7abf815adc24e9ecd509f2c07e2dd03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:76a233bff3b463f93cb832f44963527276c1cd491cd0a75c9c5d2eac75da2380 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d51f6335bdd76dd9dcfd4d3eaa2272acccc262c17300716acd3ffb0ec5f5846`  
		Last Modified: Wed, 20 Nov 2024 04:19:07 GMT  
		Size: 31.8 MB (31787958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e90448070e192152f471d2c8fd1cfc67ec60c6cb742a212ead9de030d94d6`  
		Last Modified: Tue, 03 Dec 2024 06:47:45 GMT  
		Size: 15.9 MB (15890462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4d2b49e90550c9c246be3d0a4bf462f6acedb554909b1dfcb1a519d9c36d4559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f301393f12913e8c6105d70130106fd53d8bdce15d8a7c4363bce194005f44`

```dockerfile
```

-	Layers:
	-	`sha256:96472992941cb5871f2eec833e53855a80be80e7b2a9db41e05de788c055a6c6`  
		Last Modified: Tue, 03 Dec 2024 06:47:43 GMT  
		Size: 2.5 MB (2452760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba079d972f1aa5b3c65cf4d4c0a20c942d9a5a9872a12ec2394241b40fa083b3`  
		Last Modified: Tue, 03 Dec 2024 06:47:43 GMT  
		Size: 7.0 KB (7010 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oracular-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:474003861666c2558971d1f219ca0cf541319c9cc0ae74cec1f095764456d6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47712515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbdf4934968526ebef31cbef00996bd1644b8b673488498fe04ef2f4ae2a03d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 17:58:12 GMT
ARG RELEASE
# Tue, 13 Aug 2024 17:58:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 17:58:12 GMT
LABEL org.opencontainers.image.version=24.10
# Tue, 13 Aug 2024 17:58:12 GMT
ADD file:d8a0fd6e6a1b5571de35cb60b4e05523a0290523534ad63464fdf47dfbe0b041 in / 
# Tue, 13 Aug 2024 17:58:12 GMT
CMD ["/bin/bash"]
# Tue, 13 Aug 2024 17:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8ccad27fc3ed57037242d8c7dde5d5ce195749a63f65f7d9a663f7b822c4429a`  
		Last Modified: Wed, 20 Nov 2024 04:19:18 GMT  
		Size: 30.8 MB (30775034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6a6da1657d09f717e7f94493d3e0563278583e47322d423316da636b93135`  
		Last Modified: Tue, 03 Dec 2024 04:11:01 GMT  
		Size: 16.9 MB (16937481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oracular-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9ccdc5a771ad4d7e34fba168ad55fa04ffbdc5e1cd4d33921e18e2bfc7cfe988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e46556e422491046164719725145041e108a986a7b989584413193fdb296ff3`

```dockerfile
```

-	Layers:
	-	`sha256:1392030aa2010eab698fd29006239c1c0ace7587f2c6563790bc468c30ba86b0`  
		Last Modified: Tue, 03 Dec 2024 04:11:00 GMT  
		Size: 2.5 MB (2461504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3873b36bfe6641bfeee779ada1358ed661c445aaa055118aaf947bd635bea5f`  
		Last Modified: Tue, 03 Dec 2024 04:10:59 GMT  
		Size: 7.0 KB (6978 bytes)  
		MIME: application/vnd.in-toto+json
