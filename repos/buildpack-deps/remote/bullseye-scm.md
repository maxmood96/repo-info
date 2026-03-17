## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:4588c126b5e52682eaada6cee3d0200dbe88119e6a3017b013671a9c403c85a3
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
$ docker pull buildpack-deps@sha256:002a3f47191f4609684fb016dbb7f4574b78de8e7096263858ef54b60e2173ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124313724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095df6d564bcf34ea39bc133c3e532954f20beda664b53a34465015f2fa8044d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:37:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0ff4d4cf746a31c00387c43ae977fe8857c000814b13a0e845ac0ad9512cce`  
		Last Modified: Mon, 16 Mar 2026 22:37:31 GMT  
		Size: 15.8 MB (15790675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faec137085b3e3d42618e8e8e1e58ee7d0a106e862a2d903b6c184338bd17249`  
		Last Modified: Mon, 16 Mar 2026 23:25:34 GMT  
		Size: 54.8 MB (54760568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb73802c4daf3a269f7b3c6ed237dfdcfbd78deab0744a957b21277e5dff7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7928693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8d624788a4652ecc5eaeadb6f6b2021892a91eee0b2ede0ef0b4bd6709d3c9`

```dockerfile
```

-	Layers:
	-	`sha256:f3e8725538e29d4d874284f423a09d682ccbe7c00cfa1eb71679427952e2a7af`  
		Last Modified: Mon, 16 Mar 2026 23:25:33 GMT  
		Size: 7.9 MB (7921377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a98b6e24604ac3bb7de11efec2b9b170f83192c66f827d149a3188fe997bd9e`  
		Last Modified: Mon, 16 Mar 2026 23:25:32 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:31aec6932ab38c4419e6a1e041a81f20cc20c949d29b3c72737e7288575da037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114599911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e48bd7bee9592505dae80b7ce2cbaa3c8095b10d2b201b0653394253390bd7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:19:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 00:51:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3aff03d2e208bd4d9250a4b2e487bb2463ed0509ea4994969b2b335433f11faf`  
		Last Modified: Mon, 16 Mar 2026 21:52:43 GMT  
		Size: 49.1 MB (49053591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20eaadeae5e8dca06784f6e8df6af3749f18ad9c2cad1d317604dc2d3b08d2fd`  
		Last Modified: Mon, 16 Mar 2026 23:19:25 GMT  
		Size: 14.9 MB (14905031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71032861fec9defe9e9c3f8070c31747665de1cb5a459771806bcec6df20a913`  
		Last Modified: Tue, 17 Mar 2026 00:51:37 GMT  
		Size: 50.6 MB (50641289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2c7d78d2ea2cad3e96d8cc52613b9cbb2d5c5cc7fcb0b2f7245a51196c0bc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7930159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e648995cf8fd58c9f4db44047f556e6e83e4c067d1001ab435a5862d7db15eda`

```dockerfile
```

-	Layers:
	-	`sha256:8af0e167b668d8c78d7658dea2a485af9db8630e948c31839f182658c9876559`  
		Last Modified: Tue, 17 Mar 2026 00:51:36 GMT  
		Size: 7.9 MB (7922779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff112610650a4557aef4de5aaa938bbdef2b242732f097d1a473672748439f8`  
		Last Modified: Tue, 17 Mar 2026 00:51:35 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c144b7782f7d0c6f29bc41643dc58ecba8bd9844f49f1b535420df4d5332c838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122897025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98b2f47c61485083c7d6b368caaaf3c9948b2567552be42d1ca386b14a8c465f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:30:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84fbb63fb33355ef8feb355101d06b509baa6abddd911e5e232c23e80b5d767`  
		Last Modified: Mon, 16 Mar 2026 22:39:50 GMT  
		Size: 15.8 MB (15774783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb6d461b58cdd0c5268a71ddb9eec2ce4959e3487059981d8117b3069138ccc`  
		Last Modified: Mon, 16 Mar 2026 23:30:22 GMT  
		Size: 54.9 MB (54874988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e90dfe352ec406ffba308e2a52d160a7322e85aaa66daaf170f0c633d5c3bb8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7934507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f8c05397cabd64f589cf2dd8eb66e025820a6620c8f1e11859dda325cda315`

```dockerfile
```

-	Layers:
	-	`sha256:4658283737558b8e5a0ca776d57e19cae6dba7aaa6a93abb7535065e05c662a0`  
		Last Modified: Mon, 16 Mar 2026 23:30:20 GMT  
		Size: 7.9 MB (7927111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e310c494755955aefb1b12d67424902937be5ee6e77706aa0e78dd0fcdba0778`  
		Last Modified: Mon, 16 Mar 2026 23:30:20 GMT  
		Size: 7.4 KB (7396 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:94e8b7911658089eed994ad34d4f3d52f472a4487258f5d303ee891fa2825a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127057017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd45a7dab1b65466af25fed647027c920dc00988e63ff289080f79980cd48c1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:43:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:41:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ad236c87f3ff6b413233974bf5899e332a9ceee3a606736011b98ba6596c59ea`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 54.7 MB (54702245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acfe19e42191cd08e20b1140d1c12d03ada06096409a1802c622395bda4436f`  
		Last Modified: Mon, 16 Mar 2026 22:44:04 GMT  
		Size: 16.3 MB (16295580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dff001bd2ae96d5b52e166c1481e29711d5ecb13cc3d257a5152666de3e84df`  
		Last Modified: Mon, 16 Mar 2026 23:41:46 GMT  
		Size: 56.1 MB (56059192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ceb17a1e017b3901067666d4f655e74fc9b135cc8503047d9e06f76e4295717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7924241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f69634afd1c98ec86308259625d813aa5bc3714c24d247d0f4bf7171935b93`

```dockerfile
```

-	Layers:
	-	`sha256:c58340af2de6be61075ba1eeeaa0fa2151448cfc54e26634b98f9feca45cf050`  
		Last Modified: Mon, 16 Mar 2026 23:41:44 GMT  
		Size: 7.9 MB (7916947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e1e3165358d5ed1d2b9ab7a6eb87441f78c9c7f22d6a3bef472ef92fdae1dfa`  
		Last Modified: Mon, 16 Mar 2026 23:41:44 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json
