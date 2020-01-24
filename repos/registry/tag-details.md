<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.6`](#registry26)
-	[`registry:2.6.2`](#registry262)
-	[`registry:2.7`](#registry27)
-	[`registry:2.7.1`](#registry271)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:7d081088e4bfd632a88e3f3bcd9e007ef44a796fddfe3261407a3f9f04abe1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2` - linux; amd64

```console
$ docker pull registry@sha256:3a8eef8d0a818b9bbb4bd17667253473e2d99935ccbbd37649af6bcaa064cf0d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9651357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708bc6af7e5e539bdb59707bbf1053cc2166622f5e1b17666f0ba5829ca6aaea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:e38375b009a2e2c9be7c62364fa76d52edf2a80e42d2f52cf80dfb13d578e967 in / 
# Thu, 23 Jan 2020 16:53:27 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:44:16 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 22:44:16 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Thu, 23 Jan 2020 22:44:16 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 22:44:17 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 22:44:17 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 22:44:17 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 22:44:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 22:44:17 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:486039affc0ad0f17f473efe8fb25c947515a8929198879d1e64210ef142372f`  
		Last Modified: Thu, 23 Jan 2020 16:53:49 GMT  
		Size: 2.2 MB (2207101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba51a3b098e65e3b70d5e7bb74b8ed03b84147de3f60bc4669f38fd6c50ceeb2`  
		Last Modified: Thu, 23 Jan 2020 22:44:30 GMT  
		Size: 619.8 KB (619766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb4c43d6c8ef89fd5ca89307155d72078e22c84038706fc9bc3a00cb7248f42`  
		Last Modified: Thu, 23 Jan 2020 22:44:32 GMT  
		Size: 6.8 MB (6823907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f453e5f2dd4156a3470ac7d079ffe78a49411a705a9e6ffb9ab7dcbcdc2c5`  
		Last Modified: Thu, 23 Jan 2020 22:44:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bc10b72f4230b8bc320f52240eec90b28796e0ff8bc052916aaafc1e713082`  
		Last Modified: Thu, 23 Jan 2020 22:44:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:fe84722f6cb061170ef0bd56023035b4cb6115b46e596d37496707809ebb464a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9154116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432bf69f0427b52cad10897342eaf23521b7d973566354118e9a59c4d31b5fae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:49 GMT
ADD file:78bb3e8b6b95733f24b488533a01a73ab9029ca596e5d0d6bdf3c05454406cb8 in / 
# Thu, 23 Jan 2020 16:53:51 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:50:54 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 20:50:55 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 23 Jan 2020 20:50:56 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 20:50:57 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 20:50:57 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 20:50:58 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 20:50:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:50:59 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e99479a55eec4052e95cb33c043fb7cf744165186fae58c09249b79593e2eb50`  
		Last Modified: Thu, 23 Jan 2020 16:54:23 GMT  
		Size: 2.1 MB (2146132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f709aea09540695eba574b0070f6254679510cc1a15a5dbd67f11e44a1d5f8`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 616.3 KB (616285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699e5331de408c653c690d8cd3a9183f90145d4dcc50a38ab79e7335884aa66e`  
		Last Modified: Thu, 23 Jan 2020 20:51:26 GMT  
		Size: 6.4 MB (6391085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405478cb4a379971a506df99fbc524e7384e72fffe7783280589ea35089b5c65`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3408190c5f9d98f70f2f71afd7be5d1776662b53999e750d3a16831b2c78f143`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:11fe928b25e5d30266ad8593443fd89544b437a70baf4fc78f2c8e625b208e39
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8936226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fced626eb2a272e0c0db7df93ae831fa581bb23d2d6bfe36f267e902c0cd165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:55:10 GMT
ADD file:318ca81b0e2f8b930be4b248904c0a60f0497ad722a45d1d7ac74027181fe509 in / 
# Thu, 23 Jan 2020 16:55:10 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 23:04:30 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 23:04:31 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Thu, 23 Jan 2020 23:04:32 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 23:04:33 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 23:04:33 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 23:04:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 23:04:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 23:04:35 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:788aef77d06ba65af872cf0c2da5b49362f6c05a5c8d1f8ceb4fd8b070e56876`  
		Last Modified: Thu, 23 Jan 2020 16:55:39 GMT  
		Size: 2.1 MB (2100002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9b1d117a3a4dd595be333a7ba6d115b0748af1390b4dd1bc18e88299d5db33`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 595.4 KB (595414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6c3ed2e87276696dfd7d07d243af2f1210d92bf3dc93f2ef0ed056ea685d58`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 6.2 MB (6240198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae856e010faa6edbecd57d0dcde06af1b42efeacd7f30b7c11045fd04a61144`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71ca88990271aa2a2a0ce9f0d5edcebe948f476813385f7aa1eadfc6d62ff0d`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.6`

```console
$ docker pull registry@sha256:c4bdca23bab136d5b9ce7c06895ba54892ae6db0ebfc3a2f1ac413a470b17e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2.6` - linux; amd64

```console
$ docker pull registry@sha256:c2748bc237015d14ef65355f03b77f0a7f0566d440f447e670f3333906f0f5da
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9092676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b45af23ff36baa99dda944a461425494a4bd103f3d4361d30e929f13aa8dda`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:e38375b009a2e2c9be7c62364fa76d52edf2a80e42d2f52cf80dfb13d578e967 in / 
# Thu, 23 Jan 2020 16:53:27 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:44:16 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 22:44:21 GMT
COPY file:8c9aab4f95afee2664d9af10e60d1e6241079c267ef6db906c1a8e4d9c327d3e in /bin/registry 
# Thu, 23 Jan 2020 22:44:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 22:44:22 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 22:44:22 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 22:44:22 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 22:44:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 22:44:22 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:486039affc0ad0f17f473efe8fb25c947515a8929198879d1e64210ef142372f`  
		Last Modified: Thu, 23 Jan 2020 16:53:49 GMT  
		Size: 2.2 MB (2207101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba51a3b098e65e3b70d5e7bb74b8ed03b84147de3f60bc4669f38fd6c50ceeb2`  
		Last Modified: Thu, 23 Jan 2020 22:44:30 GMT  
		Size: 619.8 KB (619766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470e22cd431aeb98bea4f3534443641311b029f90b0c3536c745369dcc9ac1af`  
		Last Modified: Thu, 23 Jan 2020 22:44:39 GMT  
		Size: 6.3 MB (6265225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1048a0cdabb074c8d3aa1d29c59656dcc1eb88f1383dbaa2edf18ddc0bb86e6d`  
		Last Modified: Thu, 23 Jan 2020 22:44:38 GMT  
		Size: 371.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5aa9d06321d1d2d784710a6dfdf9f10097d5d3f8664824b67493ab9aab4368`  
		Last Modified: Thu, 23 Jan 2020 22:44:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.6` - linux; arm variant v6

```console
$ docker pull registry@sha256:4ffb67f2e51c4075f79aa005bd5d9d5065d9f889517cdd113aa14dc14a4e84e5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8483688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405bc6e3d1bf47bb92b0e986f90e30569f984affffd4bcd69bb2a7740583d3d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:49 GMT
ADD file:78bb3e8b6b95733f24b488533a01a73ab9029ca596e5d0d6bdf3c05454406cb8 in / 
# Thu, 23 Jan 2020 16:53:51 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:50:54 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 20:51:06 GMT
COPY file:8302079be0274f86692a54ea96e6a85c0358d32eaff7762cad1bfd969ef3b890 in /bin/registry 
# Thu, 23 Jan 2020 20:51:08 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 20:51:09 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 20:51:11 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 20:51:11 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 20:51:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:51:12 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e99479a55eec4052e95cb33c043fb7cf744165186fae58c09249b79593e2eb50`  
		Last Modified: Thu, 23 Jan 2020 16:54:23 GMT  
		Size: 2.1 MB (2146132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f709aea09540695eba574b0070f6254679510cc1a15a5dbd67f11e44a1d5f8`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 616.3 KB (616285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1066781a7d5e3fd871cef0e28add0026d99f3d5fffea34318ac22b8719df6407`  
		Last Modified: Thu, 23 Jan 2020 20:51:40 GMT  
		Size: 5.7 MB (5720659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f83e7895118201b5e8beb10433d1a9edc149d8aceed25087b7079acd8595ca0`  
		Last Modified: Thu, 23 Jan 2020 20:51:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e07dc764e75402c8dcb1b3dd1fe746be330e8a2029cca04d9a570430d05b22`  
		Last Modified: Thu, 23 Jan 2020 20:51:34 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.6` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:9730f50f13e99eaf8c4f2ea0013437b9dfc726bf5eac9f3446294144cd07bcc4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8468745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b425891d739e5290e42a41c83d25e24abf3b44d605b09a808dc2558280b2f4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:55:10 GMT
ADD file:318ca81b0e2f8b930be4b248904c0a60f0497ad722a45d1d7ac74027181fe509 in / 
# Thu, 23 Jan 2020 16:55:10 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 23:04:30 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 23:04:41 GMT
COPY file:1a8b61aae84a4d8472a425e9ca5117d848facaeb3ae652f2c7f74476ecab01ff in /bin/registry 
# Thu, 23 Jan 2020 23:04:42 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 23:04:43 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 23:04:44 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 23:04:45 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 23:04:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 23:04:47 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:788aef77d06ba65af872cf0c2da5b49362f6c05a5c8d1f8ceb4fd8b070e56876`  
		Last Modified: Thu, 23 Jan 2020 16:55:39 GMT  
		Size: 2.1 MB (2100002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9b1d117a3a4dd595be333a7ba6d115b0748af1390b4dd1bc18e88299d5db33`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 595.4 KB (595414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c186c048bb3f1ae54620f0dd76d4d148628c2bb4d42ec0c30714a9e77950536`  
		Last Modified: Thu, 23 Jan 2020 23:05:12 GMT  
		Size: 5.8 MB (5772716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5607b0824cb32add42c3121856a1b2baf1592bf5984105da0ddbe9ad4fc136c`  
		Last Modified: Thu, 23 Jan 2020 23:05:10 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a2a0e6a60e1af39b1b21826a085998eb99c04bb779a1cd19238a1ab02456c9`  
		Last Modified: Thu, 23 Jan 2020 23:05:10 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.6.2`

```console
$ docker pull registry@sha256:c4bdca23bab136d5b9ce7c06895ba54892ae6db0ebfc3a2f1ac413a470b17e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2.6.2` - linux; amd64

```console
$ docker pull registry@sha256:c2748bc237015d14ef65355f03b77f0a7f0566d440f447e670f3333906f0f5da
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9092676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b45af23ff36baa99dda944a461425494a4bd103f3d4361d30e929f13aa8dda`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:e38375b009a2e2c9be7c62364fa76d52edf2a80e42d2f52cf80dfb13d578e967 in / 
# Thu, 23 Jan 2020 16:53:27 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:44:16 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 22:44:21 GMT
COPY file:8c9aab4f95afee2664d9af10e60d1e6241079c267ef6db906c1a8e4d9c327d3e in /bin/registry 
# Thu, 23 Jan 2020 22:44:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 22:44:22 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 22:44:22 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 22:44:22 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 22:44:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 22:44:22 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:486039affc0ad0f17f473efe8fb25c947515a8929198879d1e64210ef142372f`  
		Last Modified: Thu, 23 Jan 2020 16:53:49 GMT  
		Size: 2.2 MB (2207101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba51a3b098e65e3b70d5e7bb74b8ed03b84147de3f60bc4669f38fd6c50ceeb2`  
		Last Modified: Thu, 23 Jan 2020 22:44:30 GMT  
		Size: 619.8 KB (619766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470e22cd431aeb98bea4f3534443641311b029f90b0c3536c745369dcc9ac1af`  
		Last Modified: Thu, 23 Jan 2020 22:44:39 GMT  
		Size: 6.3 MB (6265225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1048a0cdabb074c8d3aa1d29c59656dcc1eb88f1383dbaa2edf18ddc0bb86e6d`  
		Last Modified: Thu, 23 Jan 2020 22:44:38 GMT  
		Size: 371.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5aa9d06321d1d2d784710a6dfdf9f10097d5d3f8664824b67493ab9aab4368`  
		Last Modified: Thu, 23 Jan 2020 22:44:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.6.2` - linux; arm variant v6

```console
$ docker pull registry@sha256:4ffb67f2e51c4075f79aa005bd5d9d5065d9f889517cdd113aa14dc14a4e84e5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8483688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405bc6e3d1bf47bb92b0e986f90e30569f984affffd4bcd69bb2a7740583d3d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:49 GMT
ADD file:78bb3e8b6b95733f24b488533a01a73ab9029ca596e5d0d6bdf3c05454406cb8 in / 
# Thu, 23 Jan 2020 16:53:51 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:50:54 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 20:51:06 GMT
COPY file:8302079be0274f86692a54ea96e6a85c0358d32eaff7762cad1bfd969ef3b890 in /bin/registry 
# Thu, 23 Jan 2020 20:51:08 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 20:51:09 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 20:51:11 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 20:51:11 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 20:51:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:51:12 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e99479a55eec4052e95cb33c043fb7cf744165186fae58c09249b79593e2eb50`  
		Last Modified: Thu, 23 Jan 2020 16:54:23 GMT  
		Size: 2.1 MB (2146132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f709aea09540695eba574b0070f6254679510cc1a15a5dbd67f11e44a1d5f8`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 616.3 KB (616285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1066781a7d5e3fd871cef0e28add0026d99f3d5fffea34318ac22b8719df6407`  
		Last Modified: Thu, 23 Jan 2020 20:51:40 GMT  
		Size: 5.7 MB (5720659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f83e7895118201b5e8beb10433d1a9edc149d8aceed25087b7079acd8595ca0`  
		Last Modified: Thu, 23 Jan 2020 20:51:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e07dc764e75402c8dcb1b3dd1fe746be330e8a2029cca04d9a570430d05b22`  
		Last Modified: Thu, 23 Jan 2020 20:51:34 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.6.2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:9730f50f13e99eaf8c4f2ea0013437b9dfc726bf5eac9f3446294144cd07bcc4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8468745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b425891d739e5290e42a41c83d25e24abf3b44d605b09a808dc2558280b2f4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:55:10 GMT
ADD file:318ca81b0e2f8b930be4b248904c0a60f0497ad722a45d1d7ac74027181fe509 in / 
# Thu, 23 Jan 2020 16:55:10 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 23:04:30 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 23:04:41 GMT
COPY file:1a8b61aae84a4d8472a425e9ca5117d848facaeb3ae652f2c7f74476ecab01ff in /bin/registry 
# Thu, 23 Jan 2020 23:04:42 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 23:04:43 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 23:04:44 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 23:04:45 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 23:04:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 23:04:47 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:788aef77d06ba65af872cf0c2da5b49362f6c05a5c8d1f8ceb4fd8b070e56876`  
		Last Modified: Thu, 23 Jan 2020 16:55:39 GMT  
		Size: 2.1 MB (2100002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9b1d117a3a4dd595be333a7ba6d115b0748af1390b4dd1bc18e88299d5db33`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 595.4 KB (595414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c186c048bb3f1ae54620f0dd76d4d148628c2bb4d42ec0c30714a9e77950536`  
		Last Modified: Thu, 23 Jan 2020 23:05:12 GMT  
		Size: 5.8 MB (5772716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5607b0824cb32add42c3121856a1b2baf1592bf5984105da0ddbe9ad4fc136c`  
		Last Modified: Thu, 23 Jan 2020 23:05:10 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a2a0e6a60e1af39b1b21826a085998eb99c04bb779a1cd19238a1ab02456c9`  
		Last Modified: Thu, 23 Jan 2020 23:05:10 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.7`

```console
$ docker pull registry@sha256:7d081088e4bfd632a88e3f3bcd9e007ef44a796fddfe3261407a3f9f04abe1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2.7` - linux; amd64

```console
$ docker pull registry@sha256:3a8eef8d0a818b9bbb4bd17667253473e2d99935ccbbd37649af6bcaa064cf0d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9651357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708bc6af7e5e539bdb59707bbf1053cc2166622f5e1b17666f0ba5829ca6aaea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:e38375b009a2e2c9be7c62364fa76d52edf2a80e42d2f52cf80dfb13d578e967 in / 
# Thu, 23 Jan 2020 16:53:27 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:44:16 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 22:44:16 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Thu, 23 Jan 2020 22:44:16 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 22:44:17 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 22:44:17 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 22:44:17 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 22:44:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 22:44:17 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:486039affc0ad0f17f473efe8fb25c947515a8929198879d1e64210ef142372f`  
		Last Modified: Thu, 23 Jan 2020 16:53:49 GMT  
		Size: 2.2 MB (2207101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba51a3b098e65e3b70d5e7bb74b8ed03b84147de3f60bc4669f38fd6c50ceeb2`  
		Last Modified: Thu, 23 Jan 2020 22:44:30 GMT  
		Size: 619.8 KB (619766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb4c43d6c8ef89fd5ca89307155d72078e22c84038706fc9bc3a00cb7248f42`  
		Last Modified: Thu, 23 Jan 2020 22:44:32 GMT  
		Size: 6.8 MB (6823907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f453e5f2dd4156a3470ac7d079ffe78a49411a705a9e6ffb9ab7dcbcdc2c5`  
		Last Modified: Thu, 23 Jan 2020 22:44:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bc10b72f4230b8bc320f52240eec90b28796e0ff8bc052916aaafc1e713082`  
		Last Modified: Thu, 23 Jan 2020 22:44:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7` - linux; arm variant v6

```console
$ docker pull registry@sha256:fe84722f6cb061170ef0bd56023035b4cb6115b46e596d37496707809ebb464a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9154116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432bf69f0427b52cad10897342eaf23521b7d973566354118e9a59c4d31b5fae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:49 GMT
ADD file:78bb3e8b6b95733f24b488533a01a73ab9029ca596e5d0d6bdf3c05454406cb8 in / 
# Thu, 23 Jan 2020 16:53:51 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:50:54 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 20:50:55 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 23 Jan 2020 20:50:56 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 20:50:57 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 20:50:57 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 20:50:58 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 20:50:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:50:59 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e99479a55eec4052e95cb33c043fb7cf744165186fae58c09249b79593e2eb50`  
		Last Modified: Thu, 23 Jan 2020 16:54:23 GMT  
		Size: 2.1 MB (2146132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f709aea09540695eba574b0070f6254679510cc1a15a5dbd67f11e44a1d5f8`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 616.3 KB (616285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699e5331de408c653c690d8cd3a9183f90145d4dcc50a38ab79e7335884aa66e`  
		Last Modified: Thu, 23 Jan 2020 20:51:26 GMT  
		Size: 6.4 MB (6391085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405478cb4a379971a506df99fbc524e7384e72fffe7783280589ea35089b5c65`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3408190c5f9d98f70f2f71afd7be5d1776662b53999e750d3a16831b2c78f143`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:11fe928b25e5d30266ad8593443fd89544b437a70baf4fc78f2c8e625b208e39
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8936226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fced626eb2a272e0c0db7df93ae831fa581bb23d2d6bfe36f267e902c0cd165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:55:10 GMT
ADD file:318ca81b0e2f8b930be4b248904c0a60f0497ad722a45d1d7ac74027181fe509 in / 
# Thu, 23 Jan 2020 16:55:10 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 23:04:30 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 23:04:31 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Thu, 23 Jan 2020 23:04:32 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 23:04:33 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 23:04:33 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 23:04:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 23:04:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 23:04:35 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:788aef77d06ba65af872cf0c2da5b49362f6c05a5c8d1f8ceb4fd8b070e56876`  
		Last Modified: Thu, 23 Jan 2020 16:55:39 GMT  
		Size: 2.1 MB (2100002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9b1d117a3a4dd595be333a7ba6d115b0748af1390b4dd1bc18e88299d5db33`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 595.4 KB (595414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6c3ed2e87276696dfd7d07d243af2f1210d92bf3dc93f2ef0ed056ea685d58`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 6.2 MB (6240198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae856e010faa6edbecd57d0dcde06af1b42efeacd7f30b7c11045fd04a61144`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71ca88990271aa2a2a0ce9f0d5edcebe948f476813385f7aa1eadfc6d62ff0d`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.7.1`

```console
$ docker pull registry@sha256:7d081088e4bfd632a88e3f3bcd9e007ef44a796fddfe3261407a3f9f04abe1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:2.7.1` - linux; amd64

```console
$ docker pull registry@sha256:3a8eef8d0a818b9bbb4bd17667253473e2d99935ccbbd37649af6bcaa064cf0d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9651357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708bc6af7e5e539bdb59707bbf1053cc2166622f5e1b17666f0ba5829ca6aaea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:e38375b009a2e2c9be7c62364fa76d52edf2a80e42d2f52cf80dfb13d578e967 in / 
# Thu, 23 Jan 2020 16:53:27 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:44:16 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 22:44:16 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Thu, 23 Jan 2020 22:44:16 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 22:44:17 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 22:44:17 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 22:44:17 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 22:44:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 22:44:17 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:486039affc0ad0f17f473efe8fb25c947515a8929198879d1e64210ef142372f`  
		Last Modified: Thu, 23 Jan 2020 16:53:49 GMT  
		Size: 2.2 MB (2207101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba51a3b098e65e3b70d5e7bb74b8ed03b84147de3f60bc4669f38fd6c50ceeb2`  
		Last Modified: Thu, 23 Jan 2020 22:44:30 GMT  
		Size: 619.8 KB (619766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb4c43d6c8ef89fd5ca89307155d72078e22c84038706fc9bc3a00cb7248f42`  
		Last Modified: Thu, 23 Jan 2020 22:44:32 GMT  
		Size: 6.8 MB (6823907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f453e5f2dd4156a3470ac7d079ffe78a49411a705a9e6ffb9ab7dcbcdc2c5`  
		Last Modified: Thu, 23 Jan 2020 22:44:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bc10b72f4230b8bc320f52240eec90b28796e0ff8bc052916aaafc1e713082`  
		Last Modified: Thu, 23 Jan 2020 22:44:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:fe84722f6cb061170ef0bd56023035b4cb6115b46e596d37496707809ebb464a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9154116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432bf69f0427b52cad10897342eaf23521b7d973566354118e9a59c4d31b5fae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:49 GMT
ADD file:78bb3e8b6b95733f24b488533a01a73ab9029ca596e5d0d6bdf3c05454406cb8 in / 
# Thu, 23 Jan 2020 16:53:51 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:50:54 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 20:50:55 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 23 Jan 2020 20:50:56 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 20:50:57 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 20:50:57 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 20:50:58 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 20:50:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:50:59 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e99479a55eec4052e95cb33c043fb7cf744165186fae58c09249b79593e2eb50`  
		Last Modified: Thu, 23 Jan 2020 16:54:23 GMT  
		Size: 2.1 MB (2146132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f709aea09540695eba574b0070f6254679510cc1a15a5dbd67f11e44a1d5f8`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 616.3 KB (616285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699e5331de408c653c690d8cd3a9183f90145d4dcc50a38ab79e7335884aa66e`  
		Last Modified: Thu, 23 Jan 2020 20:51:26 GMT  
		Size: 6.4 MB (6391085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405478cb4a379971a506df99fbc524e7384e72fffe7783280589ea35089b5c65`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3408190c5f9d98f70f2f71afd7be5d1776662b53999e750d3a16831b2c78f143`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.7.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:11fe928b25e5d30266ad8593443fd89544b437a70baf4fc78f2c8e625b208e39
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8936226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fced626eb2a272e0c0db7df93ae831fa581bb23d2d6bfe36f267e902c0cd165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:55:10 GMT
ADD file:318ca81b0e2f8b930be4b248904c0a60f0497ad722a45d1d7ac74027181fe509 in / 
# Thu, 23 Jan 2020 16:55:10 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 23:04:30 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 23:04:31 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Thu, 23 Jan 2020 23:04:32 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 23:04:33 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 23:04:33 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 23:04:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 23:04:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 23:04:35 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:788aef77d06ba65af872cf0c2da5b49362f6c05a5c8d1f8ceb4fd8b070e56876`  
		Last Modified: Thu, 23 Jan 2020 16:55:39 GMT  
		Size: 2.1 MB (2100002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9b1d117a3a4dd595be333a7ba6d115b0748af1390b4dd1bc18e88299d5db33`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 595.4 KB (595414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6c3ed2e87276696dfd7d07d243af2f1210d92bf3dc93f2ef0ed056ea685d58`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 6.2 MB (6240198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae856e010faa6edbecd57d0dcde06af1b42efeacd7f30b7c11045fd04a61144`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71ca88990271aa2a2a0ce9f0d5edcebe948f476813385f7aa1eadfc6d62ff0d`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:latest`

```console
$ docker pull registry@sha256:7d081088e4bfd632a88e3f3bcd9e007ef44a796fddfe3261407a3f9f04abe1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:3a8eef8d0a818b9bbb4bd17667253473e2d99935ccbbd37649af6bcaa064cf0d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9651357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708bc6af7e5e539bdb59707bbf1053cc2166622f5e1b17666f0ba5829ca6aaea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:e38375b009a2e2c9be7c62364fa76d52edf2a80e42d2f52cf80dfb13d578e967 in / 
# Thu, 23 Jan 2020 16:53:27 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:44:16 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 22:44:16 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Thu, 23 Jan 2020 22:44:16 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 22:44:17 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 22:44:17 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 22:44:17 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 22:44:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 22:44:17 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:486039affc0ad0f17f473efe8fb25c947515a8929198879d1e64210ef142372f`  
		Last Modified: Thu, 23 Jan 2020 16:53:49 GMT  
		Size: 2.2 MB (2207101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba51a3b098e65e3b70d5e7bb74b8ed03b84147de3f60bc4669f38fd6c50ceeb2`  
		Last Modified: Thu, 23 Jan 2020 22:44:30 GMT  
		Size: 619.8 KB (619766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb4c43d6c8ef89fd5ca89307155d72078e22c84038706fc9bc3a00cb7248f42`  
		Last Modified: Thu, 23 Jan 2020 22:44:32 GMT  
		Size: 6.8 MB (6823907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5f453e5f2dd4156a3470ac7d079ffe78a49411a705a9e6ffb9ab7dcbcdc2c5`  
		Last Modified: Thu, 23 Jan 2020 22:44:29 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bc10b72f4230b8bc320f52240eec90b28796e0ff8bc052916aaafc1e713082`  
		Last Modified: Thu, 23 Jan 2020 22:44:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:fe84722f6cb061170ef0bd56023035b4cb6115b46e596d37496707809ebb464a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9154116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432bf69f0427b52cad10897342eaf23521b7d973566354118e9a59c4d31b5fae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:49 GMT
ADD file:78bb3e8b6b95733f24b488533a01a73ab9029ca596e5d0d6bdf3c05454406cb8 in / 
# Thu, 23 Jan 2020 16:53:51 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 20:50:54 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 20:50:55 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 23 Jan 2020 20:50:56 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 20:50:57 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 20:50:57 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 20:50:58 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 20:50:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 20:50:59 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e99479a55eec4052e95cb33c043fb7cf744165186fae58c09249b79593e2eb50`  
		Last Modified: Thu, 23 Jan 2020 16:54:23 GMT  
		Size: 2.1 MB (2146132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f709aea09540695eba574b0070f6254679510cc1a15a5dbd67f11e44a1d5f8`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 616.3 KB (616285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699e5331de408c653c690d8cd3a9183f90145d4dcc50a38ab79e7335884aa66e`  
		Last Modified: Thu, 23 Jan 2020 20:51:26 GMT  
		Size: 6.4 MB (6391085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405478cb4a379971a506df99fbc524e7384e72fffe7783280589ea35089b5c65`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3408190c5f9d98f70f2f71afd7be5d1776662b53999e750d3a16831b2c78f143`  
		Last Modified: Thu, 23 Jan 2020 20:51:24 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:11fe928b25e5d30266ad8593443fd89544b437a70baf4fc78f2c8e625b208e39
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8936226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fced626eb2a272e0c0db7df93ae831fa581bb23d2d6bfe36f267e902c0cd165`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 23 Jan 2020 16:55:10 GMT
ADD file:318ca81b0e2f8b930be4b248904c0a60f0497ad722a45d1d7ac74027181fe509 in / 
# Thu, 23 Jan 2020 16:55:10 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 23:04:30 GMT
RUN set -ex     && apk add --no-cache ca-certificates apache2-utils
# Thu, 23 Jan 2020 23:04:31 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Thu, 23 Jan 2020 23:04:32 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 23 Jan 2020 23:04:33 GMT
VOLUME [/var/lib/registry]
# Thu, 23 Jan 2020 23:04:33 GMT
EXPOSE 5000
# Thu, 23 Jan 2020 23:04:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 23 Jan 2020 23:04:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Jan 2020 23:04:35 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:788aef77d06ba65af872cf0c2da5b49362f6c05a5c8d1f8ceb4fd8b070e56876`  
		Last Modified: Thu, 23 Jan 2020 16:55:39 GMT  
		Size: 2.1 MB (2100002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9b1d117a3a4dd595be333a7ba6d115b0748af1390b4dd1bc18e88299d5db33`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 595.4 KB (595414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6c3ed2e87276696dfd7d07d243af2f1210d92bf3dc93f2ef0ed056ea685d58`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 6.2 MB (6240198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae856e010faa6edbecd57d0dcde06af1b42efeacd7f30b7c11045fd04a61144`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71ca88990271aa2a2a0ce9f0d5edcebe948f476813385f7aa1eadfc6d62ff0d`  
		Last Modified: Thu, 23 Jan 2020 23:05:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
