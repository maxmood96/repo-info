## `registry:latest`

```console
$ docker pull registry@sha256:f4e1b878d4bc40a1f65532d68c94dcfbab56aa8cba1f00e355a206e7f6cc9111
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
$ docker pull registry@sha256:d74784798988458122eab9f7a1900731508ecd15326e9068a5ca42eccc4092d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9203305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2e7be006cc483d70fc3f8607f8d31c0ca26b98bb6bbbae2eee4d5f28682a82`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:00:02 GMT
RUN apk add --no-cache ca-certificates
# Sat, 27 Jan 2024 10:00:10 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Sat, 27 Jan 2024 10:00:10 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Sat, 27 Jan 2024 10:00:10 GMT
VOLUME [/var/lib/registry]
# Sat, 27 Jan 2024 10:00:10 GMT
EXPOSE 5000
# Sat, 27 Jan 2024 10:00:10 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Sat, 27 Jan 2024 10:00:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 10:00:10 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87211d705a3ce8a22a978c28a90fc3276d09f9806c211d467f4bd0146bb38695`  
		Last Modified: Sat, 27 Jan 2024 10:00:19 GMT  
		Size: 284.1 KB (284081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedcaf4bb75ec503b2e91979c312d629a3a7b66d254a27ab697a9a42844a2d41`  
		Last Modified: Sat, 27 Jan 2024 10:00:28 GMT  
		Size: 6.0 MB (6017218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789923e23857324f34973b4468925279783cfcfc18e75caafe130865a36df5ea`  
		Last Modified: Sat, 27 Jan 2024 10:00:27 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f300ea7f2d10e924f61d739098a0f43b5bd87852e2ca972a1fc352820e5ef075`  
		Last Modified: Sat, 27 Jan 2024 10:00:27 GMT  
		Size: 214.0 B  
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
