## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:f8da7ac40f0c7d37d32cc434bd1d8bcbd40e56c656e4af291459a1beb8866708
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

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d8fb953c17896a8f1945174c17eeff228f56e5c5de70bc98fae05a9e0c3e2a34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127854071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15fafbcbf0d6b9340bb144e935e51f0be56324c4bdede4eaa8ce88faabf9c9a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:01 GMT
ADD file:5498bb69da6f2fdd15556904d80120042d5bb48f73fc9f20a2d1bd5a908e0017 in / 
# Wed, 21 Dec 2022 01:20:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:11:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 11:12:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2eed4289b3de645a7af9bc81fe7c50d50a1c7aae044a61e100a676b9e6224267`  
		Last Modified: Wed, 21 Dec 2022 01:23:37 GMT  
		Size: 50.3 MB (50324468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc1500d65e85ab867b3db6b676beb32077d970bb7793f59060d71a8240aad40`  
		Last Modified: Wed, 21 Dec 2022 11:20:21 GMT  
		Size: 9.0 MB (9017319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c03e4b254700073841f0a48530eb62a4a713656a943febec6a364305347f45`  
		Last Modified: Wed, 21 Dec 2022 11:20:21 GMT  
		Size: 11.4 MB (11369371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02e69323e2f1fc0f4a19c10cb7ea3d4a4cb451944552c97d489e62c80b629c0`  
		Last Modified: Wed, 21 Dec 2022 11:20:38 GMT  
		Size: 57.1 MB (57142913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:295d25738d6f79d8c499d65bbfb3fa3232def25803c9903d97cfd3a591ee02b2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123700795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04d1149cc2918846e87d62ca6f35b8eda2142f63c5f82769d07d4ee712ee0d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:48:28 GMT
ADD file:1a47719ac251c6eab2626d584c016fd54fb5ad1212453da6f254e2977d844ec9 in / 
# Wed, 21 Dec 2022 01:48:29 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:16:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:16:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:16:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a2ba72506fbd85b58dc5575f5616efa7992eac16768aa35e10922a41b5bc83a`  
		Last Modified: Wed, 21 Dec 2022 01:52:47 GMT  
		Size: 49.3 MB (49285345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c480e4f144d3171b1600a48c85c8893cb2e7068df99ac2a593073fc603175c6`  
		Last Modified: Wed, 21 Dec 2022 02:25:19 GMT  
		Size: 8.5 MB (8471399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe5572b5bd2366b9b993844292cd896c430947a32be55f045cd4a552447b46`  
		Last Modified: Wed, 21 Dec 2022 02:25:19 GMT  
		Size: 11.0 MB (11014351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d675c15b2b0af988362a3ff26bc1a95628fe1475e278f83cfe3c315ffa3df3e7`  
		Last Modified: Wed, 21 Dec 2022 02:25:41 GMT  
		Size: 54.9 MB (54929700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3d03fc7843397ab18ad38dd7d946b7e08cb7abea0da9fd8e157b826a3d5316c5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118792618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fd5d55fbff40c5913710d8da06c7c471a71483a12ed1e9e6c76b039218a37e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:57:40 GMT
ADD file:3a39343b0809f063616f72499663466e4a509b48e03fab9262c152a211f015f7 in / 
# Wed, 21 Dec 2022 01:57:41 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:25:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:25:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5d2b0b92caaf35a430a2b891b3ae1c59a6cf60477263bd8e7a30cda427435d63`  
		Last Modified: Wed, 21 Dec 2022 02:03:55 GMT  
		Size: 47.1 MB (47101260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a36589bec34c9187227f581132ae596646abfc864ef9c4f049dcc7cb80d9e3`  
		Last Modified: Wed, 21 Dec 2022 02:36:46 GMT  
		Size: 8.1 MB (8119430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa4da363e919b9e1ffa0593e59ab1b23caa6d60c84b20ebfea4db0863532e5c`  
		Last Modified: Wed, 21 Dec 2022 02:36:47 GMT  
		Size: 10.6 MB (10646191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca23736de3322232278a50330b166e2dc3a96e13bc603c0a868f7c6ed03aed8`  
		Last Modified: Wed, 21 Dec 2022 02:37:07 GMT  
		Size: 52.9 MB (52925737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:48d2f90b64d1658caf2a66ba9e1fc9de751cc5cc5e4f2a15b27a65bad43d0fc1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127642164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6c47f77cc8fd587023c5ca50627c75e6860b80f21e4c39ea861ac64527471d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:25 GMT
ADD file:b83d427ad5bc07aecb363a59c19809d66f1425c1d8df7a4d66eb56624cf5fcf3 in / 
# Wed, 21 Dec 2022 01:39:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:03:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:03:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:04:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:be520eae96ff7c486efeba591ba872089e3b618ce226d23bf2b72f07277fb6fc`  
		Last Modified: Wed, 21 Dec 2022 01:42:15 GMT  
		Size: 50.4 MB (50372842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fd22e8d17dba55cc72a876a3a9244c7b617edbf94a17fdaad2f9d803c02d5f`  
		Last Modified: Wed, 21 Dec 2022 02:11:45 GMT  
		Size: 8.8 MB (8849270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7950c3893d7d3fd9cc5fb052ba3abdcdc532147811125fdba6efec5d9b4efee5`  
		Last Modified: Wed, 21 Dec 2022 02:11:45 GMT  
		Size: 11.3 MB (11325894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d0bb157e7432bcc4ced269bd85ce3c558f9fcefaac7844b601556fd5cffe72`  
		Last Modified: Wed, 21 Dec 2022 02:12:00 GMT  
		Size: 57.1 MB (57094158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d91b395a265a5751195a262b60e5f714a69638cb2c6167c8f11f77450db73c89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130759663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1dd53344fffaf3655d01bc02cbabe2222312cd73fe5872f96b83af7aa6b2be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:38:43 GMT
ADD file:f11f9a6e73a1ba42c97eb037cc53f119df6d6b050eaeb10df2ae716f4eabd8bf in / 
# Wed, 21 Dec 2022 01:38:44 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 09:50:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 09:50:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 09:51:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bce8ae6c08a69b30b85b1e939b782fc4dee31791e21ed3abbf56d1ec1dde0381`  
		Last Modified: Wed, 21 Dec 2022 01:43:40 GMT  
		Size: 51.4 MB (51363529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d633e3250ed10016905229f6d67f3386ceb15eb9d1bc3deb88c518444ced27`  
		Last Modified: Wed, 21 Dec 2022 09:59:17 GMT  
		Size: 9.2 MB (9194506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65f66728bfc6f4d6de6d54692bc94e1c8972c2fb1d47052d38b89b8d33481a2`  
		Last Modified: Wed, 21 Dec 2022 09:59:17 GMT  
		Size: 11.6 MB (11561149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883b0fff1e223e986f26eda6c09aecaf9bf292dbb243e2d42df8aa52d520818a`  
		Last Modified: Wed, 21 Dec 2022 09:59:35 GMT  
		Size: 58.6 MB (58640479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c9ef6742bdc376bb0b803d373d3096d3e258cf82dc0691737e3de1ce8d19dd99
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125817881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f45c032cf531ba1f74c85f022ff64703cefca237002259855de0e40be450a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:53:35 GMT
ADD file:5f771b53cd80db61f6fcf0df30ca6b99cd2c768f57ab1ffdf53d1f646b7db7c2 in / 
# Tue, 06 Dec 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 17:06:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 17:06:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 17:08:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9cc4004cb6d73c258a4d864dabb35e2beb3272eaf0de591430b0bb1af15141c`  
		Last Modified: Tue, 06 Dec 2022 02:01:46 GMT  
		Size: 50.3 MB (50259491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb8986f763b3dee4c5b32d9c82a018159c1bc6452e370fe08635660e89d7fe`  
		Last Modified: Tue, 06 Dec 2022 17:32:55 GMT  
		Size: 8.4 MB (8384079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a60f3afb7af77661e81375d03b106172646d324a7f36dcc156ffe006dd22158`  
		Last Modified: Tue, 06 Dec 2022 17:32:55 GMT  
		Size: 11.1 MB (11118473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc29876f092a179802df5708c39f6d2379d6f42f3ee77ce5ecf099fc21378b58`  
		Last Modified: Tue, 06 Dec 2022 17:33:46 GMT  
		Size: 56.1 MB (56055838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e4cd5249326fe2a87856df8e62965817a2b3fb7175180e4bbfef8ddf42832960
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138101239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0321b17f02c225b1e5ea25a41ea04144a4c1f5e9e851aff96c8bd0c516d34a00`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:16:40 GMT
ADD file:ddf53eeecd4e99f9ac6dd446b84eed33212dae1b2a9476907b99dc988c316e5e in / 
# Wed, 21 Dec 2022 01:16:44 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 04:49:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 04:49:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 04:50:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9a50dadcc8beda7926088df1652aba274c8cf1817cd6956a9342f3b25db470e6`  
		Last Modified: Wed, 21 Dec 2022 01:21:57 GMT  
		Size: 54.4 MB (54373822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9716abced382581cab26adfab0007029a5bb1dda4112dbb4ba74c5cfc7f06ad`  
		Last Modified: Wed, 21 Dec 2022 05:04:22 GMT  
		Size: 9.6 MB (9596165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dbde01939e5586504281eded1dd73c49a0b03f58c2cd890cc840b8267967f3`  
		Last Modified: Wed, 21 Dec 2022 05:04:22 GMT  
		Size: 12.1 MB (12128890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eadf6b46d5863b425edea1179a79cfa53aa4e33b4f2e8df8cfb2127727d75f3`  
		Last Modified: Wed, 21 Dec 2022 05:04:50 GMT  
		Size: 62.0 MB (62002362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2dd9632bdf82808b36390192d8af45cda9d91df8d5973be85c937c953d8cd6a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124929834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ea74233a2a42e351ff5edb7aaa04db84bc896c3e977998b6bb9d4a9bb16a2d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:41:58 GMT
ADD file:607007f7678c66cb1975d361bd26444fe0903e3a9dd7050476438a65264973e4 in / 
# Wed, 21 Dec 2022 01:42:08 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:23:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:23:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 05:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9ac168fec9b2e04c14130a8666b154d956cef535df9b833dd775de5aa941079f`  
		Last Modified: Wed, 21 Dec 2022 01:48:22 GMT  
		Size: 48.7 MB (48719460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a6f1008242d57a186240d9da881689edc71f02db9231b5dc700031a6a45f1`  
		Last Modified: Wed, 21 Dec 2022 05:40:19 GMT  
		Size: 8.7 MB (8650698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96489ea94aa4ff46b604abf252f7c3d707a5044a21c4015e6eeec8ad511daba6`  
		Last Modified: Wed, 21 Dec 2022 05:40:19 GMT  
		Size: 11.2 MB (11227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35888d8608b914d92fb61d6d7e8a43bcf7933bf84d76141fc25d412ff47e6291`  
		Last Modified: Wed, 21 Dec 2022 05:40:34 GMT  
		Size: 56.3 MB (56332405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
