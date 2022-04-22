## `buildpack-deps:bionic-scm`

```console
$ docker pull buildpack-deps@sha256:b9ad01fde093e8d662a91a201dc8c542a559af06456a5e245c51cc619963296a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7c6411505ec24355f3f1d22fcf734dd56f3c7eb22c89b8e219d8f33d5ede02f9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81853467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf527bb4f5235efad1f6727bffd1499e2506a6953d97b044fab25a473d8ade6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 22:39:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 22:39:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 05 Apr 2022 22:39:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a47fecd0167fa8860c53b97b993d4cdd955581b4a4cb77aad837a5946f76c7`  
		Last Modified: Tue, 05 Apr 2022 22:57:06 GMT  
		Size: 6.6 MB (6641629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f33f66947c23947cadf3607dae800cdba6a21e6952f10580b47120bb32b3731`  
		Last Modified: Tue, 05 Apr 2022 22:57:06 GMT  
		Size: 3.0 MB (3022350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe583c0e2a1cd4186717cf987182d6f5bfecc174a734d030e99649993906f79`  
		Last Modified: Tue, 05 Apr 2022 22:57:22 GMT  
		Size: 45.5 MB (45480550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:92ac596d0bbbc990c4a0a9b4ea99b1bb9fd38d7da2ed01956e37d964449adcee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71275328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f0e6126641560442e4a8d14eee386bf0c9cabdf70c5d8d16fcad1111651faa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 06 Apr 2022 03:25:38 GMT
ADD file:3230d8a499e37ff816595cbac3892a80005afccf8a55053c28e24989d52de08b in / 
# Wed, 06 Apr 2022 03:25:38 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 05:03:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 05:03:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 06 Apr 2022 05:04:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:419a71fa3c92c7dd0e8cfbfdf694362de1c27dafed508aeb2e5bc9ff8376fc98`  
		Last Modified: Tue, 05 Apr 2022 13:12:06 GMT  
		Size: 22.3 MB (22301415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da9b34da99841919b0af9f447099b7d6b004654e1f27cb9822534950a1f44bc`  
		Last Modified: Wed, 06 Apr 2022 05:23:44 GMT  
		Size: 5.7 MB (5711821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b36893f5a19e981da33035ae9e385a11b6213d3c677e36b6da86f20b55b167`  
		Last Modified: Wed, 06 Apr 2022 05:23:42 GMT  
		Size: 2.6 MB (2584515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa75840a85e1cccff64ce7108a91815978c6e514231ea0effcaa49c218259bd5`  
		Last Modified: Wed, 06 Apr 2022 05:24:23 GMT  
		Size: 40.7 MB (40677577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:71cdf4687db6b27bc6cb821e3939961502ab9a13b2e54966e10a01f72162b9c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75665925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f997dc9665a7c6e999e31069836f601493412fee7a5c5e653f57eeceeae58476`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:40:51 GMT
ADD file:bb36cf2c131b65fcf3f10eac5cb640ad749d77110482b30bff982a284aa9e9ec in / 
# Tue, 05 Apr 2022 22:40:51 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:05:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 05 Apr 2022 23:05:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d35feac4abe85b38af36ec148f2c2dc7a795f9862a0b6dcf2a1511b752a44996`  
		Last Modified: Tue, 05 Apr 2022 13:11:37 GMT  
		Size: 23.7 MB (23730866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d801162d026edfcca58a7cb8496fef045e4a4d9b8a9222ddd9150ea3a76c0e`  
		Last Modified: Tue, 05 Apr 2022 23:14:45 GMT  
		Size: 6.1 MB (6082517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d8ec603557719433228d854af4b6ccc8cee23ff6b03fd8959265858f5cf59c`  
		Last Modified: Tue, 05 Apr 2022 23:14:44 GMT  
		Size: 2.6 MB (2570299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ce66dfa8c40a0964942205c958821e28adb988717b46cd891aba76429257a`  
		Last Modified: Tue, 05 Apr 2022 23:15:03 GMT  
		Size: 43.3 MB (43282243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:94166da72e77bc7918bd3c870e15de97672e11dd1b5e0d012f8768754e615316
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84215943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a39a5b76b70e3761ed95913efab532bc9d09d2c0b0db0512f02eacdebe3fa6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:53:57 GMT
ADD file:164f0ee7842870b8f94ab2ee8f9151b49e08f461b99fdfa1b7586fa864d4a320 in / 
# Thu, 21 Apr 2022 23:53:57 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 00:16:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 00:16:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Apr 2022 00:17:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57fda0d035c311017871931fe2f2a2c241e46b4bc95d2a87dbf533afd8e72668`  
		Last Modified: Tue, 19 Apr 2022 13:11:34 GMT  
		Size: 27.2 MB (27163453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80020c29fe6d0575254dda040fc655dfaa84bca26136ce9b29f390d4fbb29b6`  
		Last Modified: Fri, 22 Apr 2022 00:22:15 GMT  
		Size: 6.9 MB (6929643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cdf0da60441cb8fc028c8ef1f25bf94a0e154a9fe189221f99d9d7e17e0579`  
		Last Modified: Fri, 22 Apr 2022 00:22:14 GMT  
		Size: 3.0 MB (3038571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e7e0cc8bbbca0f6e3c427507a389d0fa1ede6bdc4b6510939e3a64d6efa643`  
		Last Modified: Fri, 22 Apr 2022 00:22:35 GMT  
		Size: 47.1 MB (47084276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fc5e54e88ef64b6643276fb2e8a1a83421556fd2e2f0425df1c13072ca3e4791
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94934009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9dd19bc1e3cdfb8a980367b9f8c9df37622a45e8b0fb042087d7393f84f8de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:14 GMT
ADD file:1dc494089c70f6414b0a1f5e2e09605266508bf5ec19e1e2fb17028253f8953d in / 
# Wed, 06 Apr 2022 03:35:17 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:15:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 06 Apr 2022 04:17:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:74c6ac89233d470993bd9d67b39dc7ccb63096b55dc274e26eb50345bbecdcd8`  
		Last Modified: Tue, 05 Apr 2022 13:13:08 GMT  
		Size: 30.4 MB (30438429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563966e866b8408203dd947bd37b2f758861f63028138d65cc64046803ebd89e`  
		Last Modified: Wed, 06 Apr 2022 04:48:34 GMT  
		Size: 7.1 MB (7056771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c684f920d2f0aebaf225cb6f750b185a3aa32bbc6ce9e0f72a1a80702b33ea9c`  
		Last Modified: Wed, 06 Apr 2022 04:48:34 GMT  
		Size: 3.7 MB (3719613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b006dab4a242b603ac94e57148375c558727ba9347736957af2d8ab4933eaea`  
		Last Modified: Wed, 06 Apr 2022 04:48:58 GMT  
		Size: 53.7 MB (53719196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:853a981b76f685b501a09058fe9c80432a97a2a2b21af49f1dfb830d2deba7d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79689270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c4d09513eb95f89e58e354172b125964d00dc23295349b1add3ac7eb62ce5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Apr 2022 22:41:55 GMT
ADD file:7da6edcff7f600bf3a5d740cd585065c6b3748ff587c0627def91686d1bfe54d in / 
# Tue, 05 Apr 2022 22:41:57 GMT
CMD ["bash"]
# Tue, 05 Apr 2022 23:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Apr 2022 23:17:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 05 Apr 2022 23:18:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4b0f8a5e4614be4866f08e8772b57664127164f512df03d05a52607176caa02f`  
		Last Modified: Tue, 05 Apr 2022 13:13:37 GMT  
		Size: 25.4 MB (25365860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8129cd0a5659bbabc817a4bd1c8756c0b31fe290cc223c764308d08599353d`  
		Last Modified: Tue, 05 Apr 2022 23:26:57 GMT  
		Size: 6.3 MB (6332585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff6bd647de512734584c4049c7a22c880934ffb49b09b9dbebf9f93233154f4`  
		Last Modified: Tue, 05 Apr 2022 23:26:56 GMT  
		Size: 3.0 MB (2975107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e728913bc70babc58a8fda48f3bfae0255e918c7559f8a685bbcbb5e1e6eb8`  
		Last Modified: Tue, 05 Apr 2022 23:27:10 GMT  
		Size: 45.0 MB (45015718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
