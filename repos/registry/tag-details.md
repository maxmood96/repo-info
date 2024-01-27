<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-alpha.1`](#registry300-alpha1)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:e535dc3e461dc1633f8bd5f186771814206bf18fd4eb0179b634eb3aa65563db
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
$ docker pull registry@sha256:b431349c4c2f56b75f7e551a15c4af971dd1f671d1d0015957b9ae9d8f9810f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e886798f471f2275f732fe99ae66d5f696a782acb6bc58a5098c882b718192`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:11:58 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 09:12:06 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 09:12:06 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 09:12:06 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 09:12:06 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 09:12:06 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 09:12:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:12:06 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e188a559b0747219579caaf85a2f10aeb6074617942ef8702ab2f6268dfb496`  
		Last Modified: Sat, 27 Jan 2024 09:12:15 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afa5d37da916258e9997485f739e3ed596e006a69f4a612339c051ef79674aa`  
		Last Modified: Sat, 27 Jan 2024 09:12:24 GMT  
		Size: 6.0 MB (6024106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04eb69835def6e4a9f20b608828504aa65b841c6bf5396fce00859eb4cc1dfbf`  
		Last Modified: Sat, 27 Jan 2024 09:12:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d203a51d597143e751889c691d81ea84d4e559bac5c3c702885798a89c4abb`  
		Last Modified: Sat, 27 Jan 2024 09:12:23 GMT  
		Size: 214.0 B  
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
$ docker pull registry@sha256:75a845016af111f8d446ec69180c10f270c3c5e57b18c69b1011673094701f0d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9324983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7496ad949ad964cd6da7e749f2092a7c7abe456a8eaab0e5ec39b60cab893ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:55:21 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 06:55:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 06:55:42 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 06:55:43 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 06:55:44 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 06:55:45 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 06:55:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 06:55:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f827b6e2118ce9968e1984f2cc5cc62354b0671a5b35b6dc8fae097b96d80e8`  
		Last Modified: Sat, 27 Jan 2024 06:56:04 GMT  
		Size: 286.7 KB (286669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45dc82869e9d1abe74d7629d389a43c9aafc9cb111d12e72f8bde6589546e092`  
		Last Modified: Sat, 27 Jan 2024 06:56:14 GMT  
		Size: 5.7 MB (5689216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6798c689d38e0777d45be891ecbda3133abb1ab7742fd28a8c15f14200d60d5a`  
		Last Modified: Sat, 27 Jan 2024 06:56:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b0819bc709f3535e158713a0d5ed9c892cf3e11485d77540502aee112bdb92`  
		Last Modified: Sat, 27 Jan 2024 06:56:14 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:9e196f31927aee7bf17a7c22cedc5ce8fee8fcae7663ec05be5bc7ec71da5caf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9663287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4628d24e1681513f46f524cdb0f47b805aab49648be0b2727c3488ecde133ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:12:33 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 04:13:46 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 04:13:47 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 04:13:47 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 04:13:47 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 04:13:47 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 04:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:13:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813257c3028fd62db61fb0983ccca11ba0861cc7b240ae6df02a17d74f929942`  
		Last Modified: Sat, 27 Jan 2024 04:15:08 GMT  
		Size: 285.1 KB (285093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d7e72a7a0823b4acaee8c60bd3f630c48e2b943122fe1a3b6f0c2e50602286`  
		Last Modified: Sat, 27 Jan 2024 04:15:16 GMT  
		Size: 6.2 MB (6160052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cf5f01383f040313ce32d924c2ae2c4ade1276fb54ea1ef5203854d274c4af`  
		Last Modified: Sat, 27 Jan 2024 04:15:14 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ef052af8e58a1e7db6109b8f7cccd835376d0deaee0eb2fa175caa978ad1a3`  
		Last Modified: Sat, 27 Jan 2024 04:15:14 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.8`

```console
$ docker pull registry@sha256:e535dc3e461dc1633f8bd5f186771814206bf18fd4eb0179b634eb3aa65563db
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
$ docker pull registry@sha256:b431349c4c2f56b75f7e551a15c4af971dd1f671d1d0015957b9ae9d8f9810f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e886798f471f2275f732fe99ae66d5f696a782acb6bc58a5098c882b718192`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:11:58 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 09:12:06 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 09:12:06 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 09:12:06 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 09:12:06 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 09:12:06 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 09:12:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:12:06 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e188a559b0747219579caaf85a2f10aeb6074617942ef8702ab2f6268dfb496`  
		Last Modified: Sat, 27 Jan 2024 09:12:15 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afa5d37da916258e9997485f739e3ed596e006a69f4a612339c051ef79674aa`  
		Last Modified: Sat, 27 Jan 2024 09:12:24 GMT  
		Size: 6.0 MB (6024106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04eb69835def6e4a9f20b608828504aa65b841c6bf5396fce00859eb4cc1dfbf`  
		Last Modified: Sat, 27 Jan 2024 09:12:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d203a51d597143e751889c691d81ea84d4e559bac5c3c702885798a89c4abb`  
		Last Modified: Sat, 27 Jan 2024 09:12:23 GMT  
		Size: 214.0 B  
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
$ docker pull registry@sha256:75a845016af111f8d446ec69180c10f270c3c5e57b18c69b1011673094701f0d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9324983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7496ad949ad964cd6da7e749f2092a7c7abe456a8eaab0e5ec39b60cab893ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:55:21 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 06:55:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 06:55:42 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 06:55:43 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 06:55:44 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 06:55:45 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 06:55:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 06:55:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f827b6e2118ce9968e1984f2cc5cc62354b0671a5b35b6dc8fae097b96d80e8`  
		Last Modified: Sat, 27 Jan 2024 06:56:04 GMT  
		Size: 286.7 KB (286669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45dc82869e9d1abe74d7629d389a43c9aafc9cb111d12e72f8bde6589546e092`  
		Last Modified: Sat, 27 Jan 2024 06:56:14 GMT  
		Size: 5.7 MB (5689216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6798c689d38e0777d45be891ecbda3133abb1ab7742fd28a8c15f14200d60d5a`  
		Last Modified: Sat, 27 Jan 2024 06:56:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b0819bc709f3535e158713a0d5ed9c892cf3e11485d77540502aee112bdb92`  
		Last Modified: Sat, 27 Jan 2024 06:56:14 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:9e196f31927aee7bf17a7c22cedc5ce8fee8fcae7663ec05be5bc7ec71da5caf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9663287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4628d24e1681513f46f524cdb0f47b805aab49648be0b2727c3488ecde133ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:12:33 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 04:13:46 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 04:13:47 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 04:13:47 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 04:13:47 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 04:13:47 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 04:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:13:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813257c3028fd62db61fb0983ccca11ba0861cc7b240ae6df02a17d74f929942`  
		Last Modified: Sat, 27 Jan 2024 04:15:08 GMT  
		Size: 285.1 KB (285093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d7e72a7a0823b4acaee8c60bd3f630c48e2b943122fe1a3b6f0c2e50602286`  
		Last Modified: Sat, 27 Jan 2024 04:15:16 GMT  
		Size: 6.2 MB (6160052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cf5f01383f040313ce32d924c2ae2c4ade1276fb54ea1ef5203854d274c4af`  
		Last Modified: Sat, 27 Jan 2024 04:15:14 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ef052af8e58a1e7db6109b8f7cccd835376d0deaee0eb2fa175caa978ad1a3`  
		Last Modified: Sat, 27 Jan 2024 04:15:14 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:2.8.3`

```console
$ docker pull registry@sha256:e535dc3e461dc1633f8bd5f186771814206bf18fd4eb0179b634eb3aa65563db
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
$ docker pull registry@sha256:b431349c4c2f56b75f7e551a15c4af971dd1f671d1d0015957b9ae9d8f9810f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e886798f471f2275f732fe99ae66d5f696a782acb6bc58a5098c882b718192`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:11:58 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 09:12:06 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 09:12:06 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 09:12:06 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 09:12:06 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 09:12:06 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 09:12:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:12:06 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e188a559b0747219579caaf85a2f10aeb6074617942ef8702ab2f6268dfb496`  
		Last Modified: Sat, 27 Jan 2024 09:12:15 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afa5d37da916258e9997485f739e3ed596e006a69f4a612339c051ef79674aa`  
		Last Modified: Sat, 27 Jan 2024 09:12:24 GMT  
		Size: 6.0 MB (6024106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04eb69835def6e4a9f20b608828504aa65b841c6bf5396fce00859eb4cc1dfbf`  
		Last Modified: Sat, 27 Jan 2024 09:12:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d203a51d597143e751889c691d81ea84d4e559bac5c3c702885798a89c4abb`  
		Last Modified: Sat, 27 Jan 2024 09:12:23 GMT  
		Size: 214.0 B  
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
$ docker pull registry@sha256:75a845016af111f8d446ec69180c10f270c3c5e57b18c69b1011673094701f0d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9324983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7496ad949ad964cd6da7e749f2092a7c7abe456a8eaab0e5ec39b60cab893ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:55:21 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 06:55:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 06:55:42 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 06:55:43 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 06:55:44 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 06:55:45 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 06:55:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 06:55:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f827b6e2118ce9968e1984f2cc5cc62354b0671a5b35b6dc8fae097b96d80e8`  
		Last Modified: Sat, 27 Jan 2024 06:56:04 GMT  
		Size: 286.7 KB (286669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45dc82869e9d1abe74d7629d389a43c9aafc9cb111d12e72f8bde6589546e092`  
		Last Modified: Sat, 27 Jan 2024 06:56:14 GMT  
		Size: 5.7 MB (5689216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6798c689d38e0777d45be891ecbda3133abb1ab7742fd28a8c15f14200d60d5a`  
		Last Modified: Sat, 27 Jan 2024 06:56:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b0819bc709f3535e158713a0d5ed9c892cf3e11485d77540502aee112bdb92`  
		Last Modified: Sat, 27 Jan 2024 06:56:14 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:2.8.3` - linux; s390x

```console
$ docker pull registry@sha256:9e196f31927aee7bf17a7c22cedc5ce8fee8fcae7663ec05be5bc7ec71da5caf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9663287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4628d24e1681513f46f524cdb0f47b805aab49648be0b2727c3488ecde133ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:12:33 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 04:13:46 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 04:13:47 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 04:13:47 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 04:13:47 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 04:13:47 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 04:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:13:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813257c3028fd62db61fb0983ccca11ba0861cc7b240ae6df02a17d74f929942`  
		Last Modified: Sat, 27 Jan 2024 04:15:08 GMT  
		Size: 285.1 KB (285093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d7e72a7a0823b4acaee8c60bd3f630c48e2b943122fe1a3b6f0c2e50602286`  
		Last Modified: Sat, 27 Jan 2024 04:15:16 GMT  
		Size: 6.2 MB (6160052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cf5f01383f040313ce32d924c2ae2c4ade1276fb54ea1ef5203854d274c4af`  
		Last Modified: Sat, 27 Jan 2024 04:15:14 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ef052af8e58a1e7db6109b8f7cccd835376d0deaee0eb2fa175caa978ad1a3`  
		Last Modified: Sat, 27 Jan 2024 04:15:14 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:3.0.0-alpha.1`

```console
$ docker pull registry@sha256:584bea721ad0f0be1c859307bb6ec35eabe82c0037c0132b53bfa38b64e77ed8
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
$ docker pull registry@sha256:a8dd2b5e9b6cae685d5bb1bca3d3b4849e5dee041b647b45d98c21bea54c2f7a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13397563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b4e5158d64944a93b9726c11f95e7c586533c76627746a5f4357dcca49eae8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:11:58 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 09:12:01 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 09:12:01 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 09:12:01 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 09:12:01 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 09:12:01 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 09:12:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:12:02 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e188a559b0747219579caaf85a2f10aeb6074617942ef8702ab2f6268dfb496`  
		Last Modified: Sat, 27 Jan 2024 09:12:15 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d77d675d5b051a29dbe52c9e7cd9e3a36f966f93052af1cbb9bd73c88f802a`  
		Last Modified: Sat, 27 Jan 2024 09:12:16 GMT  
		Size: 10.0 MB (9965018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae44bb8bfd8c2289fbb28634f3c8053c62ec85defcc88841b48325d5487c5bef`  
		Last Modified: Sat, 27 Jan 2024 09:12:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d7a743fe55b98c183880ffdea28317aa04a234778fe61f51ccf6f6fbde3fc6`  
		Last Modified: Sat, 27 Jan 2024 09:12:15 GMT  
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
$ docker pull registry@sha256:9e0ffa764db5861e153f03d084c298d3b8f0f7238f995b06a89038cc7751b0c0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13110328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039092b9119f91a644b838f268a16e4205901911a6791caddc1a51db5fa30d85`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:55:21 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 06:55:26 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 06:55:27 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 06:55:28 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 06:55:29 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 06:55:30 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 06:55:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 06:55:32 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f827b6e2118ce9968e1984f2cc5cc62354b0671a5b35b6dc8fae097b96d80e8`  
		Last Modified: Sat, 27 Jan 2024 06:56:04 GMT  
		Size: 286.7 KB (286669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ace6251d133f832431fe1e5cec249d4309a375a6c66d84a63403f834f0a915d`  
		Last Modified: Sat, 27 Jan 2024 06:56:06 GMT  
		Size: 9.5 MB (9474558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ce5c6c024d68846c1699d8c8661e7e53f28b0f91f627ead327556b70b091ea`  
		Last Modified: Sat, 27 Jan 2024 06:56:04 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ed8465597c38b7f0de8382ea060f0d9ae2687a512f29cfa672f23cfdb2b0b9`  
		Last Modified: Sat, 27 Jan 2024 06:56:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:3.0.0-alpha.1` - linux; s390x

```console
$ docker pull registry@sha256:6639af3ee3c4e52e6c4366178d3e1bd547a1425073ae9f9f986e9e807c0860ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13598426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6da63704573a71e313af2754cac298f5baa729ced8ba7ed8c8425500b6997af`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:12:33 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 04:12:35 GMT
RUN set -eux; 	version='3.0.0-alpha.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='968a6dcc648aa842963ae00a28128200b6134732ff73db6fc1e52c6f9099d1f9' ;; 		aarch64) arch='arm64';   sha256='4f0d3ab06b8f77abf5ae39f08a214c2451b9eec4b1b9bb2eb9b9b9da3a3ad4cf' ;; 		armhf)   arch='armv6';   sha256='5ac4ac9cd5c7c658cd719efc44a67a0ef4b03e0618aa359ae726938eade66300' ;; 		armv7)   arch='armv7';   sha256='3c2eb167a162a17453dee0e43fb97b5abb771decf60b492e2867a2354fd0618d' ;; 		ppc64le) arch='ppc64le'; sha256='1e39ce43428437faf31f5df636d94c4dc21958076ebf96c1bd3baf67c3f7199a' ;; 		s390x)   arch='s390x';   sha256='94c53ba2254013b3e38d0c0a8d8005e41681f1f394c23a61db9953d61c134c07' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 04:12:35 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 04:12:35 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 04:12:35 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 04:12:36 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 04:12:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:12:36 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813257c3028fd62db61fb0983ccca11ba0861cc7b240ae6df02a17d74f929942`  
		Last Modified: Sat, 27 Jan 2024 04:15:08 GMT  
		Size: 285.1 KB (285093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c209c7d7ebbc765907044877e31ad962c1781a4ec22ca063a4d80066769c9deb`  
		Last Modified: Sat, 27 Jan 2024 04:15:10 GMT  
		Size: 10.1 MB (10095190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062762efaf6a71ebc91a28364a07610239673c7023030974180c86693c15d5f0`  
		Last Modified: Sat, 27 Jan 2024 04:15:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1884607bb52f7ac742a0cf11ef6cec17ed35d6a26ee40ddb7a56860cc3063c`  
		Last Modified: Sat, 27 Jan 2024 04:15:08 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `registry:latest`

```console
$ docker pull registry@sha256:e535dc3e461dc1633f8bd5f186771814206bf18fd4eb0179b634eb3aa65563db
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
$ docker pull registry@sha256:b431349c4c2f56b75f7e551a15c4af971dd1f671d1d0015957b9ae9d8f9810f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9456651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e886798f471f2275f732fe99ae66d5f696a782acb6bc58a5098c882b718192`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:11:58 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 09:12:06 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 09:12:06 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 09:12:06 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 09:12:06 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 09:12:06 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 09:12:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 09:12:06 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e188a559b0747219579caaf85a2f10aeb6074617942ef8702ab2f6268dfb496`  
		Last Modified: Sat, 27 Jan 2024 09:12:15 GMT  
		Size: 284.9 KB (284874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afa5d37da916258e9997485f739e3ed596e006a69f4a612339c051ef79674aa`  
		Last Modified: Sat, 27 Jan 2024 09:12:24 GMT  
		Size: 6.0 MB (6024106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04eb69835def6e4a9f20b608828504aa65b841c6bf5396fce00859eb4cc1dfbf`  
		Last Modified: Sat, 27 Jan 2024 09:12:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d203a51d597143e751889c691d81ea84d4e559bac5c3c702885798a89c4abb`  
		Last Modified: Sat, 27 Jan 2024 09:12:23 GMT  
		Size: 214.0 B  
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
$ docker pull registry@sha256:75a845016af111f8d446ec69180c10f270c3c5e57b18c69b1011673094701f0d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9324983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7496ad949ad964cd6da7e749f2092a7c7abe456a8eaab0e5ec39b60cab893ab`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:55:21 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 06:55:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 06:55:42 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 06:55:43 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 06:55:44 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 06:55:45 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 06:55:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 06:55:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f827b6e2118ce9968e1984f2cc5cc62354b0671a5b35b6dc8fae097b96d80e8`  
		Last Modified: Sat, 27 Jan 2024 06:56:04 GMT  
		Size: 286.7 KB (286669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45dc82869e9d1abe74d7629d389a43c9aafc9cb111d12e72f8bde6589546e092`  
		Last Modified: Sat, 27 Jan 2024 06:56:14 GMT  
		Size: 5.7 MB (5689216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6798c689d38e0777d45be891ecbda3133abb1ab7742fd28a8c15f14200d60d5a`  
		Last Modified: Sat, 27 Jan 2024 06:56:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b0819bc709f3535e158713a0d5ed9c892cf3e11485d77540502aee112bdb92`  
		Last Modified: Sat, 27 Jan 2024 06:56:14 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:9e196f31927aee7bf17a7c22cedc5ce8fee8fcae7663ec05be5bc7ec71da5caf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9663287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4628d24e1681513f46f524cdb0f47b805aab49648be0b2727c3488ecde133ae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:12:33 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 04:13:46 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 04:13:47 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 04:13:47 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 04:13:47 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 04:13:47 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 04:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 04:13:48 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813257c3028fd62db61fb0983ccca11ba0861cc7b240ae6df02a17d74f929942`  
		Last Modified: Sat, 27 Jan 2024 04:15:08 GMT  
		Size: 285.1 KB (285093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d7e72a7a0823b4acaee8c60bd3f630c48e2b943122fe1a3b6f0c2e50602286`  
		Last Modified: Sat, 27 Jan 2024 04:15:16 GMT  
		Size: 6.2 MB (6160052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cf5f01383f040313ce32d924c2ae2c4ade1276fb54ea1ef5203854d274c4af`  
		Last Modified: Sat, 27 Jan 2024 04:15:14 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ef052af8e58a1e7db6109b8f7cccd835376d0deaee0eb2fa175caa978ad1a3`  
		Last Modified: Sat, 27 Jan 2024 04:15:14 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
