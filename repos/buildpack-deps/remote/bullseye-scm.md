## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:9e2eb9c77a530c48f81855bd32bfd2cb8edd575677a5bab3da315eaf72cda77e
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

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6dc0248df19fad593ed18278e61d9ba0b4a3af5c64e9c5a174a7f468071fa3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124275778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de5948b4487876e1cf78b0915d25ed5d3f629b2fe394607cb2152b66c2a1651`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:45:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:23:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac758735be4df7bbee87d37924a15ccc254964d763d0b8620fdba9dc6d6774b5`  
		Last Modified: Mon, 29 Dec 2025 23:45:40 GMT  
		Size: 15.8 MB (15764112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6512e35a226296c3166e8ce55b556c5fe6daeebccf71cdb13eccee234e17765e`  
		Last Modified: Tue, 30 Dec 2025 01:23:49 GMT  
		Size: 54.8 MB (54755226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4c1864e62e88d39d39fffbcb4d8b16610d5976672292d547cc8fcf902f041f85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7919476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607e45dcc163b6131497508f46e05f976fefbbedbf7627724ed00861c953cd41`

```dockerfile
```

-	Layers:
	-	`sha256:55f87e71f4db143b64f9b22249fc610527233daf025d430da62731c10ade5415`  
		Last Modified: Tue, 30 Dec 2025 05:20:50 GMT  
		Size: 7.9 MB (7912160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bc4ef940233543d57b183c8a5a8f9dd5b251eb15726ebd0bb0c645d7cb88323`  
		Last Modified: Tue, 30 Dec 2025 05:20:51 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8fb63e6579c44b1d850db75de457945d7db087ac630fa858ba56d92d8e25dcc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114554759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a97787f5cbb63f8d64c0c951a83bb97aecdb8d7f1350db03ff9ba4ef66b6522`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:06:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b46683c1e86f7a120aca01c56dfafa77513b188a88759ff45f42ce118f9a337c`  
		Last Modified: Mon, 29 Dec 2025 22:25:41 GMT  
		Size: 49.0 MB (49046401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2bf8c40ad8b4e8cd6362fd57fbf345b792e3a334f7cfacc579cfaeef4447f6`  
		Last Modified: Tue, 30 Dec 2025 00:34:10 GMT  
		Size: 14.9 MB (14879533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318980c2ab1381876582d11a8701c769d018a68765de938c093203d5fb485b94`  
		Last Modified: Tue, 30 Dec 2025 02:06:57 GMT  
		Size: 50.6 MB (50628825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6ea4173524be70d3204dcd8eeeac4f9dd71b30fb61ed886b059994f8c5293338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083968fd34c2f0c65e699b5e04a1f4c16b272e8cc347761f9aa6256832e6f51b`

```dockerfile
```

-	Layers:
	-	`sha256:d3aa2ccb9dc8235f6aab600271ad9709981b5d3bb8ec75e9928b364dfb15d765`  
		Last Modified: Tue, 30 Dec 2025 05:20:57 GMT  
		Size: 7.9 MB (7913562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd3d0902018f9fcfdfa20100009c8c8bc6c7194a228661233cc8023e974452a7`  
		Last Modified: Tue, 30 Dec 2025 05:20:58 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6a5dd71e5db27a75f436ccbed4ad6682976de4ca62af2124d83a1f3f222d5d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122872586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0f70d506eb00993ba2de64584fed4d8b2455745c48fc92889e45b3f733f17f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:45:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:25:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9549a4595c672d6f3151acb8314dc1cf09736bd0b263013f6ec6856c4c63f19a`  
		Last Modified: Mon, 29 Dec 2025 23:46:10 GMT  
		Size: 15.7 MB (15749381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890aeb16c8cc7bc154fba2dfa61907bbdbcc96a5a7b348a6376fb17c7ab1fe61`  
		Last Modified: Tue, 30 Dec 2025 01:26:00 GMT  
		Size: 54.9 MB (54865435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:216ad49bfbf1851f8d25b82025997af2026bc6e01ee732b4ca52f86f71f7b6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011d931ea7eae6d28a5225250311bfef47297901b1c69cc73fc146448990c609`

```dockerfile
```

-	Layers:
	-	`sha256:868a1fd1cb4b9158ed9530814c3dd9c9574155b0425cc8d2bd959c41c65e67b4`  
		Last Modified: Tue, 30 Dec 2025 04:44:11 GMT  
		Size: 7.9 MB (7917894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ebd8684b5d67fc17f29df29b127685a0caedfa1a6c783c08f696b5a2ec10447`  
		Last Modified: Tue, 30 Dec 2025 04:44:12 GMT  
		Size: 7.4 KB (7396 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:efd9bf6657ea86d578ddb8bc0f4a18fe31df7923bfe325a3014fb77e6be55609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127016328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719ce2448869c3b6b70642d5387276ffd76ba1507ba03d6f29e12af7137f224e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:47:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:32:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:025f128203ca36b1f5bbcf71b38334a935a5d6b64f4bfdd4dee99a843a623eb2`  
		Last Modified: Mon, 29 Dec 2025 22:25:07 GMT  
		Size: 54.7 MB (54699587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3022123a59bc3e9201838d9bb8187e2c0436e8d72f121e714ce751ebf40452d6`  
		Last Modified: Mon, 29 Dec 2025 23:47:31 GMT  
		Size: 16.3 MB (16267837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704bcf14b5c7689619866c7dc5f71300d1fa1b4363f9b2dc0af3c7d5404cad9`  
		Last Modified: Tue, 30 Dec 2025 00:32:39 GMT  
		Size: 56.0 MB (56048904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7dffae10185ad9b6f7c80a258e6446ef14ad83c7973c33dd5c9ec71fbc022ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51339871fb865c8bd157da27245659faf1b274bf651906c8ac85eb6c40dd296`

```dockerfile
```

-	Layers:
	-	`sha256:a2194f25d38a7f3a843b07f30b493329f892f49a1c0bf52997aa30b2a9a561ec`  
		Last Modified: Tue, 30 Dec 2025 05:21:10 GMT  
		Size: 7.9 MB (7907730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9131cee7ba8c42b8e2d86e1152f64210a773429f92feef13079738d97cf050d1`  
		Last Modified: Tue, 30 Dec 2025 05:21:11 GMT  
		Size: 7.3 KB (7293 bytes)  
		MIME: application/vnd.in-toto+json
