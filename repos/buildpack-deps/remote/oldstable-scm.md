## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:5acc34cfc9d03148db00f1bdeb42e7db630b8f900a48836d4945ff29993478f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a190dcf237edf93c30be63bfe0cf79dee6fa19316913b892888353e276d2e061
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110796148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e018e675d0ee30a331d73fcaf1e1afd47068daaec551a694fb465ad34d376476`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:08:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae835e2c68ef1d48a4ffef72547a79926019aec6a2bbeb5372f1e832ef453dd`  
		Last Modified: Tue, 30 Mar 2021 23:17:49 GMT  
		Size: 49.8 MB (49787075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:427df0275f11e78da44c198864c2fcdf7118fee77cecb23a9456e0222d288bf4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106575055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee0c9cf5ed3eb7f317261badde77503cffb75cd1ab0fdd7bfbcbb8f256199dd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:53:43 GMT
ADD file:471d7a5419df3b812f9a1b0b14c1bfbc2b8fc88652b66cca395a28af61a77f4d in / 
# Tue, 30 Mar 2021 21:53:46 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:55:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:55:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:56:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a6404a8305ff6dab0e0a06c0c4291401369422bb5ba3e2b49d5447049a0928d7`  
		Last Modified: Tue, 30 Mar 2021 22:01:23 GMT  
		Size: 44.1 MB (44091975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0455c93c80b72e9e001eb0738f044aaf49d57cdee5c4621e362ecc2ceebd6ae3`  
		Last Modified: Wed, 31 Mar 2021 00:04:47 GMT  
		Size: 10.3 MB (10333990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3d70057a6c48834905e9f7b2f91c1c66f824e2665b9704c701c726bdbf572e`  
		Last Modified: Wed, 31 Mar 2021 00:04:42 GMT  
		Size: 4.2 MB (4161473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db4f5b94a18ebcb6b470aa3e8c715877970ee1cae520160603b88c5ed2b2988`  
		Last Modified: Wed, 31 Mar 2021 00:05:15 GMT  
		Size: 48.0 MB (47987617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:64d7065bcd3b3c6d053666878c88d95fe93852330af2b5cb63f5287e29b36bac
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102108752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477338dd10f65b2e4d7ecce939d9da5ad9f440259b8c1002b98fccb19d9f10d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:11:31 GMT
ADD file:65b5cf73b0b90f1f459a64d5706f2420deed7cdc5a9e13abacf5bcb05cc3138d in / 
# Tue, 30 Mar 2021 23:11:34 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:29:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:29:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 01:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80ad3ae4821828f32ce9b3e0f76c3c8f157a7f111e64ffad3ba40287904dfc63`  
		Last Modified: Tue, 30 Mar 2021 23:18:47 GMT  
		Size: 42.1 MB (42120250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b448d9cdc0300784b14c4a254300d86c316aca568d8b068cdc585ff456ccca`  
		Last Modified: Wed, 31 Mar 2021 01:39:43 GMT  
		Size: 9.9 MB (9939722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3845e857248fe8de10609204e4eb4db8efcbb33c6a2f9e10b7d3efe4c3c625be`  
		Last Modified: Wed, 31 Mar 2021 01:39:41 GMT  
		Size: 3.9 MB (3921214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2026eb34d858c1a9d59647eb6a6d3c28cd258eaa588cf3b99b35ac0d590fab2a`  
		Last Modified: Wed, 31 Mar 2021 01:40:05 GMT  
		Size: 46.1 MB (46127566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b05dc56040c86530e2348c7ef2d30d2807264486f0cb876a9963ff9de0459676
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105210483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29406c0332089eb7e0eec5b404816c5c6fa15decf7ea7526962f6b0812575f0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:45 GMT
ADD file:0546f28e5d1be54699d1e0756275203da731735b3212f2ff1a87cd7f8dcc9049 in / 
# Tue, 30 Mar 2021 21:49:50 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:22:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 00:23:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9317dc7ea567b49ade0ea730b5530d1363b065549e8b75a198e0b60bdde1f1d7`  
		Last Modified: Tue, 30 Mar 2021 21:56:46 GMT  
		Size: 43.2 MB (43177588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaf1b7b1bdfdc23af33da7d1fc9670524e63a8408bb04de9aebdf95979c5635`  
		Last Modified: Wed, 31 Mar 2021 00:33:12 GMT  
		Size: 10.2 MB (10201033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4446041554682b465ef9a0e853a5067e7d794fa1c840946d140beab2ddeb51`  
		Last Modified: Wed, 31 Mar 2021 00:33:09 GMT  
		Size: 4.1 MB (4096741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0b477e68dd7171c7df2dfc66cd994be553e0679dd5c2083048d10d5a29363a`  
		Last Modified: Wed, 31 Mar 2021 00:33:40 GMT  
		Size: 47.7 MB (47735121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b08fdf3bce7e9feb772f8e95527bd2f17933b51d353bd1b7aea74002f805ea46
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113264980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e003e0e3dc34e123c513c95e90c2f6d5659510bacc6cd4b2f4d4f26e7b1378`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:41:30 GMT
ADD file:1df7a35a36c49061902cf634a894b34a55a9c020976547cf6d2dda96879854bc in / 
# Tue, 30 Mar 2021 21:41:30 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:01:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:01:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 00:02:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:667bc6614d317ea77075a4e2f4ee7ef7d7b696f50d426cec38048d3ca20f1aa1`  
		Last Modified: Tue, 30 Mar 2021 21:49:28 GMT  
		Size: 46.1 MB (46098556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51d5e0a8886ebed26c676639259bf05d50ff3b0285ea4b8afd1492ea424e7ff`  
		Last Modified: Wed, 31 Mar 2021 00:11:48 GMT  
		Size: 11.3 MB (11336592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cd0bba69d5c567fef7e770351f3ae71bdff83884b1d5af86d4dcd6ea6ff7a9`  
		Last Modified: Wed, 31 Mar 2021 00:11:48 GMT  
		Size: 4.6 MB (4564997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a10652cecac951d9def7d54e1fc469edee3b96dde5d603ef1275742ca7280b`  
		Last Modified: Wed, 31 Mar 2021 00:12:18 GMT  
		Size: 51.3 MB (51264835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
