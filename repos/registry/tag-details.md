<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-alpha.1`](#registry300-alpha1)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:e771226e8468b319f6731e201cdfa33addf818edf6e199960e054d6bcfce6ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `registry:2` - linux; amd64

```console
$ docker pull registry@sha256:12202eb78732e22f8658d595bd6e3d47ef9f13ede78e94e90974c020c7d7c1b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10091639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8781fe3b7a280475ac394dc1754b4c08a39cdd400e05869d0da3586ffb82f7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:49:44 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 03:49:51 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 03:49:51 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 03:49:51 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 03:49:51 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 03:49:51 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:49:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:49:51 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba4b87859f504d956d22540c09ee9fe67c4bd339bc483e9797d959fd839adf6`  
		Last Modified: Sat, 27 Jan 2024 03:50:01 GMT  
		Size: 284.7 KB (284698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da701e3b4d6f45ef24a3052bb9757ed1ef19c86e6bf39876941940b4d4847ad`  
		Last Modified: Sat, 27 Jan 2024 03:50:10 GMT  
		Size: 6.4 MB (6403787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a4d5d702c7f9f51f58c6009ae7012859d36ad3f412ffd4de5f3175d4e32fac`  
		Last Modified: Sat, 27 Jan 2024 03:50:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a4f6454cb259d98b1ddc58112e2c8a8053af2455315017573d5c5223b46821`  
		Last Modified: Sat, 27 Jan 2024 03:50:09 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:fb6ae2c1ea0187406fe39a4ce923eb30e74aa9d7d396d2171b3e64e3c535a309
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0dfab1fcd28281b3ab589f36e50194b875ad74b24afef4516dce19e45721658`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 11:13:22 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 11:13:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 11:13:22 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 11:13:22 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 11:13:22 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 11:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 11:13:22 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0121d17a28a917cf8eed6df8437e20307da5470118b339c8d75bf042b7a6a7c`  
		Last Modified: Fri, 01 Dec 2023 11:13:31 GMT  
		Size: 6.0 MB (6024107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7352c67115d13474ebda7aa1eab3aa85f48e3f9870c0b217b3d69bb1df736047`  
		Last Modified: Fri, 01 Dec 2023 11:13:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe926da741926c7f284fc8aa53c4bbab15e4907a25808099b913153ea0ca4f8`  
		Last Modified: Fri, 01 Dec 2023 11:13:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm variant v7

```console
$ docker pull registry@sha256:3166995ffab4033d4400c48a594ca3b2f754825b251b74e2d73e481c58ac612d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9202916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b0c275698e3f8b08827600f629044835f4d8d44e36f46011cc441c8f8630fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 09:08:47 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 09:08:47 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 09:08:48 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 09:08:48 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 09:08:48 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 09:08:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:08:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c2a5c450ad539c19d039de6765a66bcea6ba840416ea012fadf23ab9c48c2d`  
		Last Modified: Fri, 01 Dec 2023 09:08:56 GMT  
		Size: 6.0 MB (6017219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d90b15526d5227036c129e5d6ba476db2c679a642368d75b83379112261aba3`  
		Last Modified: Fri, 01 Dec 2023 09:08:55 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc8b927649fa946b85ca6841783a6cc126af20aba2c528dcce8aaae828f23eb`  
		Last Modified: Fri, 01 Dec 2023 09:08:55 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:ed8c3ebb6f60bda8de0a05f8b61c86029d4c0d655a84d4ce3bf9dced2106a92c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9445002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4a13810e3bee12ed11b0cafb446340bd8e21880291dda3bfc6c937e3bd56f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:43:59 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 03:44:05 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 03:44:05 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 03:44:05 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 03:44:05 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 03:44:05 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:44:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:44:05 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eacdf7fe0f111bca4eddaca4c52cbb62fa8cecebaf8903f9a32bc6f13ecf3d7`  
		Last Modified: Sat, 27 Jan 2024 03:44:13 GMT  
		Size: 286.3 KB (286299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e048c492597ef5a0cf88cf3370fc5187f4f36803e1c5bd915116fd72b5bfd7d`  
		Last Modified: Sat, 27 Jan 2024 03:44:21 GMT  
		Size: 5.8 MB (5824730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5fd32043dedd90e3b321741ecf099cdc390ab58613fc428ccbba3106e09e3b`  
		Last Modified: Sat, 27 Jan 2024 03:44:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9168bc494de5cb681bb46c11bd9395b4eff194190d0651a14c31ebcc715975`  
		Last Modified: Sat, 27 Jan 2024 03:44:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:66ae01fe8c805d611e1890a5d529ba462ccc111e499327033ae16547de7acf1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9324810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed66e38a7ef70eb6cec12254e785fb1cc1d42df29fb9ab327a80ae2d875ac17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 09:20:14 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 09:20:14 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 09:20:15 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 09:20:15 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 09:20:16 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 09:20:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:20:17 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b951cfeed5797587ecf47747da15e3ecd147c4e7b7f3b6de280017b23dcdb896`  
		Last Modified: Fri, 01 Dec 2023 09:20:29 GMT  
		Size: 5.7 MB (5689216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206a7cc025f36aca61a70fbf339c31348236f6a0e1ea75675fa9137989733524`  
		Last Modified: Fri, 01 Dec 2023 09:20:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d608cef607088cf39e2a4f5488511b4dedb6334d165cd0f787794a2ecd83da`  
		Last Modified: Fri, 01 Dec 2023 09:20:27 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:99d58f17ef257c7195dca7084ca24ba9df47fa420ae055198f3a8ac9c3689c56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9663208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294a423956e20e4d65a3ec7d35d38426590c6522c9bb669d1a89bde3b7b9f299`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:23:56 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 08:23:56 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 08:23:56 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 08:23:57 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 08:23:57 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 08:23:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 08:23:57 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df1db0a68aeb6fbac17c638a66dccba8359333f6c239616dfed192320897054`  
		Last Modified: Fri, 01 Dec 2023 08:24:11 GMT  
		Size: 6.2 MB (6160052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c75b818b12c3588dcc656fac631ed2807f821f3b7c594f3b999593ec5dd274d`  
		Last Modified: Fri, 01 Dec 2023 08:24:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951769fe941e528f7e7bf6acd99565734544a47731425ba83011de9f63dd96b2`  
		Last Modified: Fri, 01 Dec 2023 08:24:10 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.8`

```console
$ docker pull registry@sha256:e771226e8468b319f6731e201cdfa33addf818edf6e199960e054d6bcfce6ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `registry:2.8` - linux; amd64

```console
$ docker pull registry@sha256:12202eb78732e22f8658d595bd6e3d47ef9f13ede78e94e90974c020c7d7c1b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10091639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8781fe3b7a280475ac394dc1754b4c08a39cdd400e05869d0da3586ffb82f7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:49:44 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 03:49:51 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 03:49:51 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 03:49:51 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 03:49:51 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 03:49:51 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:49:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:49:51 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba4b87859f504d956d22540c09ee9fe67c4bd339bc483e9797d959fd839adf6`  
		Last Modified: Sat, 27 Jan 2024 03:50:01 GMT  
		Size: 284.7 KB (284698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da701e3b4d6f45ef24a3052bb9757ed1ef19c86e6bf39876941940b4d4847ad`  
		Last Modified: Sat, 27 Jan 2024 03:50:10 GMT  
		Size: 6.4 MB (6403787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a4d5d702c7f9f51f58c6009ae7012859d36ad3f412ffd4de5f3175d4e32fac`  
		Last Modified: Sat, 27 Jan 2024 03:50:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a4f6454cb259d98b1ddc58112e2c8a8053af2455315017573d5c5223b46821`  
		Last Modified: Sat, 27 Jan 2024 03:50:09 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm variant v6

```console
$ docker pull registry@sha256:fb6ae2c1ea0187406fe39a4ce923eb30e74aa9d7d396d2171b3e64e3c535a309
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0dfab1fcd28281b3ab589f36e50194b875ad74b24afef4516dce19e45721658`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 11:13:22 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 11:13:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 11:13:22 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 11:13:22 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 11:13:22 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 11:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 11:13:22 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0121d17a28a917cf8eed6df8437e20307da5470118b339c8d75bf042b7a6a7c`  
		Last Modified: Fri, 01 Dec 2023 11:13:31 GMT  
		Size: 6.0 MB (6024107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7352c67115d13474ebda7aa1eab3aa85f48e3f9870c0b217b3d69bb1df736047`  
		Last Modified: Fri, 01 Dec 2023 11:13:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe926da741926c7f284fc8aa53c4bbab15e4907a25808099b913153ea0ca4f8`  
		Last Modified: Fri, 01 Dec 2023 11:13:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm variant v7

```console
$ docker pull registry@sha256:3166995ffab4033d4400c48a594ca3b2f754825b251b74e2d73e481c58ac612d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9202916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b0c275698e3f8b08827600f629044835f4d8d44e36f46011cc441c8f8630fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 09:08:47 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 09:08:47 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 09:08:48 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 09:08:48 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 09:08:48 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 09:08:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:08:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c2a5c450ad539c19d039de6765a66bcea6ba840416ea012fadf23ab9c48c2d`  
		Last Modified: Fri, 01 Dec 2023 09:08:56 GMT  
		Size: 6.0 MB (6017219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d90b15526d5227036c129e5d6ba476db2c679a642368d75b83379112261aba3`  
		Last Modified: Fri, 01 Dec 2023 09:08:55 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc8b927649fa946b85ca6841783a6cc126af20aba2c528dcce8aaae828f23eb`  
		Last Modified: Fri, 01 Dec 2023 09:08:55 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:ed8c3ebb6f60bda8de0a05f8b61c86029d4c0d655a84d4ce3bf9dced2106a92c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9445002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4a13810e3bee12ed11b0cafb446340bd8e21880291dda3bfc6c937e3bd56f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:43:59 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 03:44:05 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 03:44:05 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 03:44:05 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 03:44:05 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 03:44:05 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:44:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:44:05 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eacdf7fe0f111bca4eddaca4c52cbb62fa8cecebaf8903f9a32bc6f13ecf3d7`  
		Last Modified: Sat, 27 Jan 2024 03:44:13 GMT  
		Size: 286.3 KB (286299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e048c492597ef5a0cf88cf3370fc5187f4f36803e1c5bd915116fd72b5bfd7d`  
		Last Modified: Sat, 27 Jan 2024 03:44:21 GMT  
		Size: 5.8 MB (5824730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5fd32043dedd90e3b321741ecf099cdc390ab58613fc428ccbba3106e09e3b`  
		Last Modified: Sat, 27 Jan 2024 03:44:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9168bc494de5cb681bb46c11bd9395b4eff194190d0651a14c31ebcc715975`  
		Last Modified: Sat, 27 Jan 2024 03:44:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:66ae01fe8c805d611e1890a5d529ba462ccc111e499327033ae16547de7acf1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9324810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed66e38a7ef70eb6cec12254e785fb1cc1d42df29fb9ab327a80ae2d875ac17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 09:20:14 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 09:20:14 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 09:20:15 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 09:20:15 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 09:20:16 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 09:20:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:20:17 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b951cfeed5797587ecf47747da15e3ecd147c4e7b7f3b6de280017b23dcdb896`  
		Last Modified: Fri, 01 Dec 2023 09:20:29 GMT  
		Size: 5.7 MB (5689216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206a7cc025f36aca61a70fbf339c31348236f6a0e1ea75675fa9137989733524`  
		Last Modified: Fri, 01 Dec 2023 09:20:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d608cef607088cf39e2a4f5488511b4dedb6334d165cd0f787794a2ecd83da`  
		Last Modified: Fri, 01 Dec 2023 09:20:27 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:99d58f17ef257c7195dca7084ca24ba9df47fa420ae055198f3a8ac9c3689c56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9663208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294a423956e20e4d65a3ec7d35d38426590c6522c9bb669d1a89bde3b7b9f299`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:23:56 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 08:23:56 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 08:23:56 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 08:23:57 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 08:23:57 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 08:23:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 08:23:57 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df1db0a68aeb6fbac17c638a66dccba8359333f6c239616dfed192320897054`  
		Last Modified: Fri, 01 Dec 2023 08:24:11 GMT  
		Size: 6.2 MB (6160052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c75b818b12c3588dcc656fac631ed2807f821f3b7c594f3b999593ec5dd274d`  
		Last Modified: Fri, 01 Dec 2023 08:24:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951769fe941e528f7e7bf6acd99565734544a47731425ba83011de9f63dd96b2`  
		Last Modified: Fri, 01 Dec 2023 08:24:10 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.8.3`

```console
$ docker pull registry@sha256:e771226e8468b319f6731e201cdfa33addf818edf6e199960e054d6bcfce6ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `registry:2.8.3` - linux; amd64

```console
$ docker pull registry@sha256:12202eb78732e22f8658d595bd6e3d47ef9f13ede78e94e90974c020c7d7c1b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10091639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8781fe3b7a280475ac394dc1754b4c08a39cdd400e05869d0da3586ffb82f7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:49:44 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 03:49:51 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 03:49:51 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 03:49:51 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 03:49:51 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 03:49:51 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:49:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:49:51 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba4b87859f504d956d22540c09ee9fe67c4bd339bc483e9797d959fd839adf6`  
		Last Modified: Sat, 27 Jan 2024 03:50:01 GMT  
		Size: 284.7 KB (284698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da701e3b4d6f45ef24a3052bb9757ed1ef19c86e6bf39876941940b4d4847ad`  
		Last Modified: Sat, 27 Jan 2024 03:50:10 GMT  
		Size: 6.4 MB (6403787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a4d5d702c7f9f51f58c6009ae7012859d36ad3f412ffd4de5f3175d4e32fac`  
		Last Modified: Sat, 27 Jan 2024 03:50:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a4f6454cb259d98b1ddc58112e2c8a8053af2455315017573d5c5223b46821`  
		Last Modified: Sat, 27 Jan 2024 03:50:09 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.3` - linux; arm variant v6

```console
$ docker pull registry@sha256:fb6ae2c1ea0187406fe39a4ce923eb30e74aa9d7d396d2171b3e64e3c535a309
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0dfab1fcd28281b3ab589f36e50194b875ad74b24afef4516dce19e45721658`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 11:13:22 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 11:13:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 11:13:22 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 11:13:22 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 11:13:22 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 11:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 11:13:22 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0121d17a28a917cf8eed6df8437e20307da5470118b339c8d75bf042b7a6a7c`  
		Last Modified: Fri, 01 Dec 2023 11:13:31 GMT  
		Size: 6.0 MB (6024107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7352c67115d13474ebda7aa1eab3aa85f48e3f9870c0b217b3d69bb1df736047`  
		Last Modified: Fri, 01 Dec 2023 11:13:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe926da741926c7f284fc8aa53c4bbab15e4907a25808099b913153ea0ca4f8`  
		Last Modified: Fri, 01 Dec 2023 11:13:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.3` - linux; arm variant v7

```console
$ docker pull registry@sha256:3166995ffab4033d4400c48a594ca3b2f754825b251b74e2d73e481c58ac612d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9202916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b0c275698e3f8b08827600f629044835f4d8d44e36f46011cc441c8f8630fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 09:08:47 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 09:08:47 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 09:08:48 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 09:08:48 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 09:08:48 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 09:08:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:08:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c2a5c450ad539c19d039de6765a66bcea6ba840416ea012fadf23ab9c48c2d`  
		Last Modified: Fri, 01 Dec 2023 09:08:56 GMT  
		Size: 6.0 MB (6017219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d90b15526d5227036c129e5d6ba476db2c679a642368d75b83379112261aba3`  
		Last Modified: Fri, 01 Dec 2023 09:08:55 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc8b927649fa946b85ca6841783a6cc126af20aba2c528dcce8aaae828f23eb`  
		Last Modified: Fri, 01 Dec 2023 09:08:55 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:ed8c3ebb6f60bda8de0a05f8b61c86029d4c0d655a84d4ce3bf9dced2106a92c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9445002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4a13810e3bee12ed11b0cafb446340bd8e21880291dda3bfc6c937e3bd56f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:43:59 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 03:44:05 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 03:44:05 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 03:44:05 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 03:44:05 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 03:44:05 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:44:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:44:05 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eacdf7fe0f111bca4eddaca4c52cbb62fa8cecebaf8903f9a32bc6f13ecf3d7`  
		Last Modified: Sat, 27 Jan 2024 03:44:13 GMT  
		Size: 286.3 KB (286299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e048c492597ef5a0cf88cf3370fc5187f4f36803e1c5bd915116fd72b5bfd7d`  
		Last Modified: Sat, 27 Jan 2024 03:44:21 GMT  
		Size: 5.8 MB (5824730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5fd32043dedd90e3b321741ecf099cdc390ab58613fc428ccbba3106e09e3b`  
		Last Modified: Sat, 27 Jan 2024 03:44:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9168bc494de5cb681bb46c11bd9395b4eff194190d0651a14c31ebcc715975`  
		Last Modified: Sat, 27 Jan 2024 03:44:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.3` - linux; ppc64le

```console
$ docker pull registry@sha256:66ae01fe8c805d611e1890a5d529ba462ccc111e499327033ae16547de7acf1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9324810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed66e38a7ef70eb6cec12254e785fb1cc1d42df29fb9ab327a80ae2d875ac17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 09:20:14 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 09:20:14 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 09:20:15 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 09:20:15 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 09:20:16 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 09:20:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:20:17 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b951cfeed5797587ecf47747da15e3ecd147c4e7b7f3b6de280017b23dcdb896`  
		Last Modified: Fri, 01 Dec 2023 09:20:29 GMT  
		Size: 5.7 MB (5689216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206a7cc025f36aca61a70fbf339c31348236f6a0e1ea75675fa9137989733524`  
		Last Modified: Fri, 01 Dec 2023 09:20:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d608cef607088cf39e2a4f5488511b4dedb6334d165cd0f787794a2ecd83da`  
		Last Modified: Fri, 01 Dec 2023 09:20:27 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.3` - linux; s390x

```console
$ docker pull registry@sha256:99d58f17ef257c7195dca7084ca24ba9df47fa420ae055198f3a8ac9c3689c56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9663208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294a423956e20e4d65a3ec7d35d38426590c6522c9bb669d1a89bde3b7b9f299`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:23:56 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 08:23:56 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 08:23:56 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 08:23:57 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 08:23:57 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 08:23:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 08:23:57 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df1db0a68aeb6fbac17c638a66dccba8359333f6c239616dfed192320897054`  
		Last Modified: Fri, 01 Dec 2023 08:24:11 GMT  
		Size: 6.2 MB (6160052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c75b818b12c3588dcc656fac631ed2807f821f3b7c594f3b999593ec5dd274d`  
		Last Modified: Fri, 01 Dec 2023 08:24:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951769fe941e528f7e7bf6acd99565734544a47731425ba83011de9f63dd96b2`  
		Last Modified: Fri, 01 Dec 2023 08:24:10 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:3.0.0-alpha.1`

```console
$ docker pull registry@sha256:f4741f6bd99d439227398b2dd8778d762feac64b9816ebf8fd81d04ebd4c3d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `registry:3.0.0-alpha.1` - linux; amd64

```console
$ docker pull registry@sha256:f2e59b7b67b060e25ef0d797f035bedfcc379b8d401a84a7b1758791355f2c31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14207387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2307841f57df5d180fb403ee1a816895af37734974d4e46f542ef6343bda5b6d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:49:44 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 03:49:46 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 03:49:46 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 03:49:46 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 03:49:46 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 03:49:46 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:49:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:49:46 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba4b87859f504d956d22540c09ee9fe67c4bd339bc483e9797d959fd839adf6`  
		Last Modified: Sat, 27 Jan 2024 03:50:01 GMT  
		Size: 284.7 KB (284698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6197da558a90d49e923d4e5a9b4045d757495417cb4e0186820aa0379f739416`  
		Last Modified: Sat, 27 Jan 2024 03:50:03 GMT  
		Size: 10.5 MB (10519534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2ab31cd9f931c8d0fd77d49e588df2741e47d02c5d23d09156f29db7ce5bbe`  
		Last Modified: Sat, 27 Jan 2024 03:50:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d552c299f9ca4c67b40d04c8efa7b58c7ea00996bbe06021305d2a51e99125f8`  
		Last Modified: Sat, 27 Jan 2024 03:50:01 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:3.0.0-alpha.1` - linux; arm variant v6

```console
$ docker pull registry@sha256:b9bc48e4f87d57cc7196a94fd8180bdaf1420618e3a6b2c75cdcb3ca4379de3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13397369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11bae78972e152046c730c3f437ee31158a80fa042d6ef4850760afeaecbc0e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Tue, 19 Dec 2023 18:49:31 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 19 Dec 2023 18:49:32 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 19 Dec 2023 18:49:32 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 18:49:32 GMT
EXPOSE 5000
# Tue, 19 Dec 2023 18:49:32 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 19 Dec 2023 18:49:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 18:49:32 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ceb200511104b043198dbf160e1bdca9ba30c9f5ee53b33783eb084472220b3`  
		Last Modified: Tue, 19 Dec 2023 18:49:46 GMT  
		Size: 10.0 MB (9965003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6c32259148b92d8e682121d58a8c7a46137a284795be244a5a6adc9de9a3d`  
		Last Modified: Tue, 19 Dec 2023 18:49:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79647b7c95df044d54f40f022d8d113709fec105f3cac3afe946300b0a64b232`  
		Last Modified: Tue, 19 Dec 2023 18:49:43 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:3.0.0-alpha.1` - linux; arm variant v7

```console
$ docker pull registry@sha256:0f9439b8aa4b197430cf9a670c1868bf052329396a3f1ebb642a021af374c6d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13140225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a57033cce6600ad0d15e89d94b49ec82bda990b5c122e41ca6addfb4642c01`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Tue, 19 Dec 2023 21:53:45 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 19 Dec 2023 21:53:45 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 19 Dec 2023 21:53:45 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 21:53:45 GMT
EXPOSE 5000
# Tue, 19 Dec 2023 21:53:46 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 19 Dec 2023 21:53:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 21:53:46 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5362942bf2e8f101ff844dde2d5bdd7296f99e22a5099fd17f1626e7a96af13f`  
		Last Modified: Tue, 19 Dec 2023 21:53:59 GMT  
		Size: 10.0 MB (9954528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116ec10c6493f87b8ba01602176d954fb262fad0331141c3d179b63f637bb8ea`  
		Last Modified: Tue, 19 Dec 2023 21:53:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52a95e9d88a83c661d01655d3fe46e48342e0273034f6a17eb83f4d2d94ba4d`  
		Last Modified: Tue, 19 Dec 2023 21:53:57 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:3.0.0-alpha.1` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:76717b48571744e04d040e7d5965be2aae098a18a6f010fe53fc145f855a89d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13349777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481227f3af6e23cf0517fb6df33ded4ed64a77f7c32dcb8f0dca00986ed53d5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:43:59 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 03:44:01 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 03:44:01 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 03:44:01 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 03:44:01 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 03:44:01 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:44:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:44:01 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eacdf7fe0f111bca4eddaca4c52cbb62fa8cecebaf8903f9a32bc6f13ecf3d7`  
		Last Modified: Sat, 27 Jan 2024 03:44:13 GMT  
		Size: 286.3 KB (286299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb3c329d6e7228baa1421bab8a4c355c215d5fe77081fc85b9891c67cd7817c`  
		Last Modified: Sat, 27 Jan 2024 03:44:14 GMT  
		Size: 9.7 MB (9729503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9693e28dada6f13a7c84b628f1a8267ce13d12437f1339a019ff73edc6e6dc4c`  
		Last Modified: Sat, 27 Jan 2024 03:44:13 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3483d703b7294328f6fe25feb27f71523e8a46f453e588dd156ecd037c9dc7e4`  
		Last Modified: Sat, 27 Jan 2024 03:44:13 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:3.0.0-alpha.1` - linux; ppc64le

```console
$ docker pull registry@sha256:9c9e9d3afa0d527d31d71d22d202bd01264ca774c5f318f005bd69bbe2ac6180
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13110143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42a799abe88bd3ac864fc19325632cf1eb2aea154d04547831702dadeed3cb7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Wed, 20 Dec 2023 01:13:50 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Wed, 20 Dec 2023 01:13:51 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Wed, 20 Dec 2023 01:13:51 GMT
VOLUME [/var/lib/registry]
# Wed, 20 Dec 2023 01:13:52 GMT
EXPOSE 5000
# Wed, 20 Dec 2023 01:13:52 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Wed, 20 Dec 2023 01:13:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 20 Dec 2023 01:13:52 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f657e79e3fd9f68852eeaeee4ec4aeb899a092ef57f4c9e473f104470e198315`  
		Last Modified: Wed, 20 Dec 2023 01:14:07 GMT  
		Size: 9.5 MB (9474549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc1dedd9dead6914133a992a2afce8447efe905b1f846959eb369dd4d45aa43`  
		Last Modified: Wed, 20 Dec 2023 01:14:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a044360ec66c377480042cf38d560dc70df168d6fb40f05b5128890c6ee6741`  
		Last Modified: Wed, 20 Dec 2023 01:14:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:3.0.0-alpha.1` - linux; s390x

```console
$ docker pull registry@sha256:2e5fb530120c4563ace8293f4e7874cb298f1b5b60f632256dbdeb59f8e539f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13598351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e1e59108675092f7cc4900d265006c9f1c573b7f514d7375249b4e580735e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Tue, 19 Dec 2023 20:26:35 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Tue, 19 Dec 2023 20:26:36 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Tue, 19 Dec 2023 20:26:36 GMT
VOLUME [/var/lib/registry]
# Tue, 19 Dec 2023 20:26:36 GMT
EXPOSE 5000
# Tue, 19 Dec 2023 20:26:37 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Tue, 19 Dec 2023 20:26:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 20:26:37 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a9f15b569239982f8ae6630d9b2def6ddd9030ffb714d8f22fc379a5535969`  
		Last Modified: Tue, 19 Dec 2023 20:26:57 GMT  
		Size: 10.1 MB (10095195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbaaa30c53056c1363b439eb6fac014c8ef78817f2328b54af526d274937b17e`  
		Last Modified: Tue, 19 Dec 2023 20:26:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1308a0f330e41f27686421339e65a605633447d89e32677b61675db025861dd`  
		Last Modified: Tue, 19 Dec 2023 20:26:56 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:latest`

```console
$ docker pull registry@sha256:e771226e8468b319f6731e201cdfa33addf818edf6e199960e054d6bcfce6ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:12202eb78732e22f8658d595bd6e3d47ef9f13ede78e94e90974c020c7d7c1b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10091639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8781fe3b7a280475ac394dc1754b4c08a39cdd400e05869d0da3586ffb82f7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:49:44 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 03:49:51 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 03:49:51 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 03:49:51 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 03:49:51 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 03:49:51 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:49:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:49:51 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba4b87859f504d956d22540c09ee9fe67c4bd339bc483e9797d959fd839adf6`  
		Last Modified: Sat, 27 Jan 2024 03:50:01 GMT  
		Size: 284.7 KB (284698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da701e3b4d6f45ef24a3052bb9757ed1ef19c86e6bf39876941940b4d4847ad`  
		Last Modified: Sat, 27 Jan 2024 03:50:10 GMT  
		Size: 6.4 MB (6403787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a4d5d702c7f9f51f58c6009ae7012859d36ad3f412ffd4de5f3175d4e32fac`  
		Last Modified: Sat, 27 Jan 2024 03:50:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a4f6454cb259d98b1ddc58112e2c8a8053af2455315017573d5c5223b46821`  
		Last Modified: Sat, 27 Jan 2024 03:50:09 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:fb6ae2c1ea0187406fe39a4ce923eb30e74aa9d7d396d2171b3e64e3c535a309
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0dfab1fcd28281b3ab589f36e50194b875ad74b24afef4516dce19e45721658`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:53:48 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 11:13:22 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 11:13:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 11:13:22 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 11:13:22 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 11:13:22 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 11:13:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 11:13:22 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7ba0492eb25e7f21078441d7cdc65088836bc1984bc4a14cd3e9cd75cbf32`  
		Last Modified: Fri, 01 Dec 2023 01:00:23 GMT  
		Size: 284.9 KB (284884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0121d17a28a917cf8eed6df8437e20307da5470118b339c8d75bf042b7a6a7c`  
		Last Modified: Fri, 01 Dec 2023 11:13:31 GMT  
		Size: 6.0 MB (6024107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7352c67115d13474ebda7aa1eab3aa85f48e3f9870c0b217b3d69bb1df736047`  
		Last Modified: Fri, 01 Dec 2023 11:13:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe926da741926c7f284fc8aa53c4bbab15e4907a25808099b913153ea0ca4f8`  
		Last Modified: Fri, 01 Dec 2023 11:13:29 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:3166995ffab4033d4400c48a594ca3b2f754825b251b74e2d73e481c58ac612d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9202916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b0c275698e3f8b08827600f629044835f4d8d44e36f46011cc441c8f8630fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:44:57 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 09:08:47 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 09:08:47 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 09:08:48 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 09:08:48 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 09:08:48 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 09:08:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:08:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a824ff289f1a3c765a444079137b8b7f1cee80348faa53e1ba4c960b73ed2a`  
		Last Modified: Fri, 01 Dec 2023 08:49:42 GMT  
		Size: 284.1 KB (284079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c2a5c450ad539c19d039de6765a66bcea6ba840416ea012fadf23ab9c48c2d`  
		Last Modified: Fri, 01 Dec 2023 09:08:56 GMT  
		Size: 6.0 MB (6017219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d90b15526d5227036c129e5d6ba476db2c679a642368d75b83379112261aba3`  
		Last Modified: Fri, 01 Dec 2023 09:08:55 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc8b927649fa946b85ca6841783a6cc126af20aba2c528dcce8aaae828f23eb`  
		Last Modified: Fri, 01 Dec 2023 09:08:55 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:ed8c3ebb6f60bda8de0a05f8b61c86029d4c0d655a84d4ce3bf9dced2106a92c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9445002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4a13810e3bee12ed11b0cafb446340bd8e21880291dda3bfc6c937e3bd56f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:43:59 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 03:44:05 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 03:44:05 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 03:44:05 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 03:44:05 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 03:44:05 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 03:44:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:44:05 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eacdf7fe0f111bca4eddaca4c52cbb62fa8cecebaf8903f9a32bc6f13ecf3d7`  
		Last Modified: Sat, 27 Jan 2024 03:44:13 GMT  
		Size: 286.3 KB (286299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e048c492597ef5a0cf88cf3370fc5187f4f36803e1c5bd915116fd72b5bfd7d`  
		Last Modified: Sat, 27 Jan 2024 03:44:21 GMT  
		Size: 5.8 MB (5824730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5fd32043dedd90e3b321741ecf099cdc390ab58613fc428ccbba3106e09e3b`  
		Last Modified: Sat, 27 Jan 2024 03:44:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9168bc494de5cb681bb46c11bd9395b4eff194190d0651a14c31ebcc715975`  
		Last Modified: Sat, 27 Jan 2024 03:44:20 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:66ae01fe8c805d611e1890a5d529ba462ccc111e499327033ae16547de7acf1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9324810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed66e38a7ef70eb6cec12254e785fb1cc1d42df29fb9ab327a80ae2d875ac17`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:37:34 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 09:20:14 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 09:20:14 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 09:20:15 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 09:20:15 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 09:20:16 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 09:20:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 09:20:17 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692dbecd5e141c462ab06ef113ec964b525e7564d734890cc1d5b1dbf33ee34e`  
		Last Modified: Fri, 01 Dec 2023 06:43:30 GMT  
		Size: 286.7 KB (286661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b951cfeed5797587ecf47747da15e3ecd147c4e7b7f3b6de280017b23dcdb896`  
		Last Modified: Fri, 01 Dec 2023 09:20:29 GMT  
		Size: 5.7 MB (5689216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206a7cc025f36aca61a70fbf339c31348236f6a0e1ea75675fa9137989733524`  
		Last Modified: Fri, 01 Dec 2023 09:20:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d608cef607088cf39e2a4f5488511b4dedb6334d165cd0f787794a2ecd83da`  
		Last Modified: Fri, 01 Dec 2023 09:20:27 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:99d58f17ef257c7195dca7084ca24ba9df47fa420ae055198f3a8ac9c3689c56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9663208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294a423956e20e4d65a3ec7d35d38426590c6522c9bb669d1a89bde3b7b9f299`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:14:49 GMT
RUN apk add --no-cache ca-certificates
# Fri, 01 Dec 2023 08:23:56 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Fri, 01 Dec 2023 08:23:56 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Fri, 01 Dec 2023 08:23:56 GMT
VOLUME [/var/lib/registry]
# Fri, 01 Dec 2023 08:23:57 GMT
EXPOSE 5000
# Fri, 01 Dec 2023 08:23:57 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Fri, 01 Dec 2023 08:23:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 08:23:57 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab563e8d41683e124df048aa9b564b0e8e1021e85213666971a015df51d5e48`  
		Last Modified: Fri, 01 Dec 2023 08:20:46 GMT  
		Size: 285.1 KB (285090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df1db0a68aeb6fbac17c638a66dccba8359333f6c239616dfed192320897054`  
		Last Modified: Fri, 01 Dec 2023 08:24:11 GMT  
		Size: 6.2 MB (6160052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c75b818b12c3588dcc656fac631ed2807f821f3b7c594f3b999593ec5dd274d`  
		Last Modified: Fri, 01 Dec 2023 08:24:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:951769fe941e528f7e7bf6acd99565734544a47731425ba83011de9f63dd96b2`  
		Last Modified: Fri, 01 Dec 2023 08:24:10 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
