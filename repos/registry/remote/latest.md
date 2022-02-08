## `registry:latest`

```console
$ docker pull registry@sha256:c26590bcf53822a542e78fab5c88e1dfbcdee91c1882f4656b7db7b542d91d97
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
$ docker pull registry@sha256:712c58f0d738ba95788d2814979028fd648a37186ae0dd4141f786125ba6d680
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9203396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c97225e83c8c357ca001d70b6627a1b63c714011f8e9f13a23242f51a22f496`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:21:45 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Feb 2022 23:20:26 GMT
RUN set -eux; 	version='2.8.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='7b2ebc3d67e21987b741137dc230d0f038b362ba21e02f226150ff5577f92556' ;; 		aarch64) arch='arm64';   sha256='16b9f497751bd3abe8b75d0f1538e2767ef3c536f4f11d05a312fb1767d43e85' ;; 		armhf)   arch='armv6';   sha256='5021831ba045a3cc409f6f62ab50c04db2c935a058eb53ce9d74a4dd5ba41102' ;; 		armv7)   arch='armv7';   sha256='ff659c577266662edb247d4719399fa1179bfcb90fb6006fc63396b7089c0f70' ;; 		ppc64le) arch='ppc64le'; sha256='46fbd645b415c68222ee0e8043a91c27b6bb2ec2e0a568f663d1e78cc69d8cda' ;; 		s390x)   arch='s390x';   sha256='ebbd08228cf290ceef50ab542ae6087b66173b18fa84868210cbbdb458d11bd3' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Mon, 07 Feb 2022 23:20:26 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Mon, 07 Feb 2022 23:20:27 GMT
VOLUME [/var/lib/registry]
# Mon, 07 Feb 2022 23:20:27 GMT
EXPOSE 5000
# Mon, 07 Feb 2022 23:20:27 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Mon, 07 Feb 2022 23:20:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Feb 2022 23:20:27 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666ba61612fd7c93393f9a5bc1751d8a9929e32d51501dba691da9e8232bc87b`  
		Last Modified: Tue, 30 Nov 2021 04:36:04 GMT  
		Size: 282.2 KB (282159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4642f78634a704fd28b0de9842d9fd84bb575dcb2f75fdd09596d593217c638`  
		Last Modified: Mon, 07 Feb 2022 23:20:40 GMT  
		Size: 6.1 MB (6102213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab650d9906386c9199974d94edfba605964f85f48518da8237eb5fb587ead06`  
		Last Modified: Mon, 07 Feb 2022 23:20:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91dceb018e81eefd8f12f94fce01ae9ad1cbc0c941e38ff897642f97b0954e1c`  
		Last Modified: Mon, 07 Feb 2022 23:20:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:4b81d3a0be8b7aedb5e0520c83c5b8df8803baaefa114efc772514be9be6c793
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8582089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e8adb175a10d1f78ad2bdd146215ece81c59f411dee5896454afaa15deb139`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Nov 2021 21:08:16 GMT
ADD file:61137e0aa49ba06f57ac69466fe2fb116f580b5e6159d56f846b1d72c4a3c814 in / 
# Wed, 24 Nov 2021 21:08:16 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 02:32:18 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Feb 2022 23:08:29 GMT
RUN set -eux; 	version='2.8.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='7b2ebc3d67e21987b741137dc230d0f038b362ba21e02f226150ff5577f92556' ;; 		aarch64) arch='arm64';   sha256='16b9f497751bd3abe8b75d0f1538e2767ef3c536f4f11d05a312fb1767d43e85' ;; 		armhf)   arch='armv6';   sha256='5021831ba045a3cc409f6f62ab50c04db2c935a058eb53ce9d74a4dd5ba41102' ;; 		armv7)   arch='armv7';   sha256='ff659c577266662edb247d4719399fa1179bfcb90fb6006fc63396b7089c0f70' ;; 		ppc64le) arch='ppc64le'; sha256='46fbd645b415c68222ee0e8043a91c27b6bb2ec2e0a568f663d1e78cc69d8cda' ;; 		s390x)   arch='s390x';   sha256='ebbd08228cf290ceef50ab542ae6087b66173b18fa84868210cbbdb458d11bd3' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Mon, 07 Feb 2022 23:08:30 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Mon, 07 Feb 2022 23:08:30 GMT
VOLUME [/var/lib/registry]
# Mon, 07 Feb 2022 23:08:31 GMT
EXPOSE 5000
# Mon, 07 Feb 2022 23:08:31 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Mon, 07 Feb 2022 23:08:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Feb 2022 23:08:32 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:e4a43de54da9e309482f6762f0c11f5f547cd8fd61a49c5f158453066162023e`  
		Last Modified: Wed, 24 Nov 2021 21:09:46 GMT  
		Size: 2.6 MB (2631421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228ad0256439cce3fe9db355991b0557f55241d8cca8690f4f741e1c2d8fb8b9`  
		Last Modified: Tue, 30 Nov 2021 02:47:28 GMT  
		Size: 282.1 KB (282105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f158effa29e8eb09de8055527f43b9989879789793e0e87e9c2a32e39516fff0`  
		Last Modified: Mon, 07 Feb 2022 23:09:09 GMT  
		Size: 5.7 MB (5667953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da0b52ddc44e3818f1ac109da17d6434fc4d53e582f80cae9c80988fc4e3b9d`  
		Last Modified: Mon, 07 Feb 2022 23:09:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a58653643df333f9478014a46a32122ee5087f6c16d2efec3a829791d3a138c`  
		Last Modified: Mon, 07 Feb 2022 23:09:06 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:00356336c4ad69bb60dd052b06912cb2e868ef0d7ab1f2375b2e2ce8631d1117
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8377548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9344e52a81fd3db080bc3351a87dd2a79b990e5532bd4914c218dfa19b9c0035`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Nov 2021 21:42:11 GMT
ADD file:ca436da5b0bfc9c0e2fc685533c6628918000c8fff109fe9a8da625b9a798002 in / 
# Wed, 24 Nov 2021 21:42:11 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:10:37 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Feb 2022 22:58:09 GMT
RUN set -eux; 	version='2.8.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='7b2ebc3d67e21987b741137dc230d0f038b362ba21e02f226150ff5577f92556' ;; 		aarch64) arch='arm64';   sha256='16b9f497751bd3abe8b75d0f1538e2767ef3c536f4f11d05a312fb1767d43e85' ;; 		armhf)   arch='armv6';   sha256='5021831ba045a3cc409f6f62ab50c04db2c935a058eb53ce9d74a4dd5ba41102' ;; 		armv7)   arch='armv7';   sha256='ff659c577266662edb247d4719399fa1179bfcb90fb6006fc63396b7089c0f70' ;; 		ppc64le) arch='ppc64le'; sha256='46fbd645b415c68222ee0e8043a91c27b6bb2ec2e0a568f663d1e78cc69d8cda' ;; 		s390x)   arch='s390x';   sha256='ebbd08228cf290ceef50ab542ae6087b66173b18fa84868210cbbdb458d11bd3' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Mon, 07 Feb 2022 22:58:09 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Mon, 07 Feb 2022 22:58:10 GMT
VOLUME [/var/lib/registry]
# Mon, 07 Feb 2022 22:58:10 GMT
EXPOSE 5000
# Mon, 07 Feb 2022 22:58:11 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Mon, 07 Feb 2022 22:58:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Feb 2022 22:58:11 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:5480d2ca1740c20ce17652e01ed2265cdc914458acd41256a2b1ccff28f2762c`  
		Last Modified: Wed, 24 Nov 2021 21:43:40 GMT  
		Size: 2.4 MB (2434764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f21e2af73375430a6481f93a61f3df4f9de38c985f83b27293f8aace16d6b5`  
		Last Modified: Tue, 30 Nov 2021 04:33:33 GMT  
		Size: 281.2 KB (281248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f937d38d8bc50ccd79ae40eb48fd64fa9b69f5a39e0de259e697db2ac68b23`  
		Last Modified: Mon, 07 Feb 2022 22:58:47 GMT  
		Size: 5.7 MB (5660924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78a6d0fde437c7bcc5255821e26c13227578ecc7f5a95b4020b6338f002a565`  
		Last Modified: Mon, 07 Feb 2022 22:58:43 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5305e8abd186e84d4b7c2fad8ab3540e50f4af75cdd06c07ce0ebe96213edb91`  
		Last Modified: Mon, 07 Feb 2022 22:58:43 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1b640322f9a983281970daaeba1a6d303f399d67890644389ff419d951963e20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8541458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5c239ad23b59ad968992313eac42ffa272ee2584c32e78c3c8601a7e69ab9d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Nov 2021 20:39:20 GMT
ADD file:df53811312284306901fdaaff0a357a4bf40d631e662fe9ce6d342442e494b6c in / 
# Wed, 24 Nov 2021 20:39:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 01:54:59 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Feb 2022 22:40:18 GMT
RUN set -eux; 	version='2.8.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='7b2ebc3d67e21987b741137dc230d0f038b362ba21e02f226150ff5577f92556' ;; 		aarch64) arch='arm64';   sha256='16b9f497751bd3abe8b75d0f1538e2767ef3c536f4f11d05a312fb1767d43e85' ;; 		armhf)   arch='armv6';   sha256='5021831ba045a3cc409f6f62ab50c04db2c935a058eb53ce9d74a4dd5ba41102' ;; 		armv7)   arch='armv7';   sha256='ff659c577266662edb247d4719399fa1179bfcb90fb6006fc63396b7089c0f70' ;; 		ppc64le) arch='ppc64le'; sha256='46fbd645b415c68222ee0e8043a91c27b6bb2ec2e0a568f663d1e78cc69d8cda' ;; 		s390x)   arch='s390x';   sha256='ebbd08228cf290ceef50ab542ae6087b66173b18fa84868210cbbdb458d11bd3' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Mon, 07 Feb 2022 22:40:20 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Mon, 07 Feb 2022 22:40:20 GMT
VOLUME [/var/lib/registry]
# Mon, 07 Feb 2022 22:40:21 GMT
EXPOSE 5000
# Mon, 07 Feb 2022 22:40:23 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Mon, 07 Feb 2022 22:40:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Feb 2022 22:40:24 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9b3977197b4f2147bdd31e1271f811319dcd5c2fc595f14e81f5351ab6275b99`  
		Last Modified: Wed, 24 Nov 2021 20:39:59 GMT  
		Size: 2.7 MB (2715434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a89e8eeedd549875510e5e4e14010906a58878526814e6df25d14009856c6ff`  
		Last Modified: Tue, 30 Nov 2021 02:05:10 GMT  
		Size: 281.9 KB (281899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fd3315a8d8c57e0a9e2735577c48ab5a0b74255db53da352710247d084d3e9`  
		Last Modified: Mon, 07 Feb 2022 22:40:41 GMT  
		Size: 5.5 MB (5543543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ea175683303a3a72cd56099e90a283f395900de24cd39b68718c823d9a2ae`  
		Last Modified: Mon, 07 Feb 2022 22:40:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193b5954b3c963288240dcaf99801c1a24a68a24f5b3ed6fd21c5616389c50cd`  
		Last Modified: Mon, 07 Feb 2022 22:40:40 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:0248606624357eb94aa9d43ec2693d8f5c0cb10c1600438166b9d28c9b5c1e78
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8409398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6e72bdabe43217ed7f879643afe07fd0766d85f016f9b7c6c104255e3d3a5b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Nov 2021 20:20:16 GMT
ADD file:57115dca2eb707f46b6301e75174e6aa316fb02ac28643b91429b75be51bd8c8 in / 
# Wed, 24 Nov 2021 20:20:20 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 03:17:54 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Feb 2022 23:17:20 GMT
RUN set -eux; 	version='2.8.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='7b2ebc3d67e21987b741137dc230d0f038b362ba21e02f226150ff5577f92556' ;; 		aarch64) arch='arm64';   sha256='16b9f497751bd3abe8b75d0f1538e2767ef3c536f4f11d05a312fb1767d43e85' ;; 		armhf)   arch='armv6';   sha256='5021831ba045a3cc409f6f62ab50c04db2c935a058eb53ce9d74a4dd5ba41102' ;; 		armv7)   arch='armv7';   sha256='ff659c577266662edb247d4719399fa1179bfcb90fb6006fc63396b7089c0f70' ;; 		ppc64le) arch='ppc64le'; sha256='46fbd645b415c68222ee0e8043a91c27b6bb2ec2e0a568f663d1e78cc69d8cda' ;; 		s390x)   arch='s390x';   sha256='ebbd08228cf290ceef50ab542ae6087b66173b18fa84868210cbbdb458d11bd3' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Mon, 07 Feb 2022 23:17:22 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Mon, 07 Feb 2022 23:17:24 GMT
VOLUME [/var/lib/registry]
# Mon, 07 Feb 2022 23:17:28 GMT
EXPOSE 5000
# Mon, 07 Feb 2022 23:17:30 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Mon, 07 Feb 2022 23:17:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Feb 2022 23:17:39 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:159b5dcb1717c815c76ff5ea1db730e18e8609c9090238e43282856db9e71f47`  
		Last Modified: Wed, 24 Nov 2021 20:21:14 GMT  
		Size: 2.8 MB (2814780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28be42a6852cc2108ddba1e4252671ae20275780a6ff73b1038699f59da2ac20`  
		Last Modified: Tue, 30 Nov 2021 03:35:16 GMT  
		Size: 284.0 KB (284020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19c65c7c5f61e5f4a6852495a953ee7e430f0043a1a24c6b7dd82e0f9266e3a`  
		Last Modified: Mon, 07 Feb 2022 23:17:58 GMT  
		Size: 5.3 MB (5309986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee42c5947f45d40554ed62975038778f7c98f602780c97ba745f97fba708bac1`  
		Last Modified: Mon, 07 Feb 2022 23:17:57 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0505869d2d876112fd11f578a22f1b9e763d4495d90aea7945d7f69c0fd64fa0`  
		Last Modified: Mon, 07 Feb 2022 23:17:57 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:9d74aa19cda1fb09ce7578b52fc83d83298f0561090e099f3116a7612d7b879e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8698161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d393a7531946d098759c47476905c04a47eca40165dec0852a1cbb286e1f45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 24 Nov 2021 20:41:23 GMT
ADD file:cd24c711a2ef431b3ff94f9a02bfc42f159bc60de1d0eceecafea4e8af02441d in / 
# Wed, 24 Nov 2021 20:41:23 GMT
CMD ["/bin/sh"]
# Tue, 30 Nov 2021 04:07:57 GMT
RUN apk add --no-cache ca-certificates
# Mon, 07 Feb 2022 22:41:55 GMT
RUN set -eux; 	version='2.8.0'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='7b2ebc3d67e21987b741137dc230d0f038b362ba21e02f226150ff5577f92556' ;; 		aarch64) arch='arm64';   sha256='16b9f497751bd3abe8b75d0f1538e2767ef3c536f4f11d05a312fb1767d43e85' ;; 		armhf)   arch='armv6';   sha256='5021831ba045a3cc409f6f62ab50c04db2c935a058eb53ce9d74a4dd5ba41102' ;; 		armv7)   arch='armv7';   sha256='ff659c577266662edb247d4719399fa1179bfcb90fb6006fc63396b7089c0f70' ;; 		ppc64le) arch='ppc64le'; sha256='46fbd645b415c68222ee0e8043a91c27b6bb2ec2e0a568f663d1e78cc69d8cda' ;; 		s390x)   arch='s390x';   sha256='ebbd08228cf290ceef50ab542ae6087b66173b18fa84868210cbbdb458d11bd3' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version
# Mon, 07 Feb 2022 22:41:55 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Mon, 07 Feb 2022 22:41:56 GMT
VOLUME [/var/lib/registry]
# Mon, 07 Feb 2022 22:41:56 GMT
EXPOSE 5000
# Mon, 07 Feb 2022 22:41:56 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Mon, 07 Feb 2022 22:41:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 07 Feb 2022 22:41:56 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:d6baca485f3d0f7c77221be60fbef5db014a5ef9d8f53db4a310c947c690d189`  
		Last Modified: Wed, 24 Nov 2021 20:42:15 GMT  
		Size: 2.6 MB (2605944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66787da5af638f8523e4694d81d38c2ca7c0a262f4cb8d78c46f7d64833bbaa0`  
		Last Modified: Tue, 30 Nov 2021 04:17:43 GMT  
		Size: 282.4 KB (282378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c59fcb2402e6c3d237443bc08ba3758faf4baa41c3b9256ca2bcf921622a71`  
		Last Modified: Mon, 07 Feb 2022 22:42:13 GMT  
		Size: 5.8 MB (5809229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2485b0108d05a6d9d51333dbcfa4c5adb4ea11b4786a8136c07e90f2ed25df42`  
		Last Modified: Mon, 07 Feb 2022 22:42:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a457903db28ddbbe20093068ca7d043084c4d5d137a44639ba031350587c92df`  
		Last Modified: Mon, 07 Feb 2022 22:42:12 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
