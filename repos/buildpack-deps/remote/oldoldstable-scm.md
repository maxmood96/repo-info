## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:ba70b711dc8594a942533161fb46d4179fad8440acffc6e66ddad05fe1794559
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

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c013fda918d19330a9b2eb57d9b78e0b8b3366907188aead52b88e2d6bcbe4d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124275333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a0424f64be9a2ce1429957f9201a03a07d84a8dd34a597134e1d89d59297c0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b6f830cd306f01980373f1e0120f2d00018fbe51a9506b7262f5d9e4bbda74f9`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 53.8 MB (53756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa9ab09db8d94503213f634b29be3505174979f2e0c6e3fd46c2acc0716c25`  
		Last Modified: Tue, 21 Oct 2025 04:46:42 GMT  
		Size: 15.8 MB (15764056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e663cb3204c49ebc21b005f5976ee62e4f00b632aaa8000dbe6db86d9cde2a1`  
		Last Modified: Tue, 21 Oct 2025 04:47:30 GMT  
		Size: 54.8 MB (54755162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:82d95079d5e9fe8ac94935e0be36c498e433c000a866ebab253aa46d33c95dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7919519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864f9819c47d089f7cd7d65dab5330bc501cbb61985d4ec12f1241481504e64f`

```dockerfile
```

-	Layers:
	-	`sha256:83c388f91f4a367c9377607ad6cd7739cbaf961fb6eb0b691c04b2d6469b779e`  
		Last Modified: Tue, 21 Oct 2025 10:20:28 GMT  
		Size: 7.9 MB (7912160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8265b31f62b7def42e4355e68b363a8b420d27cf9d6b93f80c991cd0129ae8ed`  
		Last Modified: Tue, 21 Oct 2025 10:20:29 GMT  
		Size: 7.4 KB (7359 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:954bfe5953048ed118aa47068b46219507c3b887b199c21445b53b546494997e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114553880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b8ba6f47973dbc8e6e2933dc94ecc887745f90d2b8d2bbce5e6091f32611af`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:680ed921e0c94a719af1d242eac2d0c1be8482153680a3940f3435ee5598303a`  
		Last Modified: Tue, 21 Oct 2025 00:20:24 GMT  
		Size: 49.0 MB (49046121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c68013a317d7d802bb25c57a724c8753caec2fc7f0e78fc13f9a38fd22ecd4`  
		Last Modified: Tue, 21 Oct 2025 02:44:25 GMT  
		Size: 14.9 MB (14879264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895fddf2807e047e5b02e5418fd04d343d3e9b5b393b2f3f0cd6704cad44b8f0`  
		Last Modified: Tue, 21 Oct 2025 04:10:49 GMT  
		Size: 50.6 MB (50628495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:04a93d9f1422231f6d603d19e7a723508d2382a40b23215a91fd445786ab2b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681ab9e74ffe8e77beecbfe2e8c5c25126af9ed6e99864bfb9aad0d42154b23e`

```dockerfile
```

-	Layers:
	-	`sha256:8fa5a717aa2c037809fe9640d7c2c068ff19060bc513aeb41b5ba9b58a5dedb5`  
		Last Modified: Tue, 21 Oct 2025 07:20:10 GMT  
		Size: 7.9 MB (7913562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3783405965009463f5747e6320466144b7fad44cce63bb9fa8aebe956f4e2758`  
		Last Modified: Tue, 21 Oct 2025 07:20:11 GMT  
		Size: 7.4 KB (7423 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a7d5e88fd5d342f7bb26a18daa58fb680ff48c48e79f8cab83c4f8c483cf1c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122867760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b97c76ddeaed047a0b460b19fa00e233c256ebb2b77fbf0aeaa78057b8e6cf7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f7bdca064e682157394f36dabd112bc9831aff9743216b035e2ccccf704cc3`  
		Last Modified: Tue, 21 Oct 2025 01:46:24 GMT  
		Size: 15.7 MB (15749510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc7a49f7691cb1ac5f0f40edbe6f4beec62021b4fd2544c431d8f694b4b4647`  
		Last Modified: Tue, 21 Oct 2025 02:35:21 GMT  
		Size: 54.9 MB (54860806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b8375c4ab5c589091835b2c592fdafbfeda86ee702b3b8a957df040bf4e17299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd336dd81fdec57660efdc809ffca06349af5dcbf6ae6815cb3e2dac5774beb0`

```dockerfile
```

-	Layers:
	-	`sha256:c1c0be62d93c452948ade1e111c63ca47981d3c9518d2322afe1b08765c44c6a`  
		Last Modified: Tue, 21 Oct 2025 10:20:39 GMT  
		Size: 7.9 MB (7917894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4404266d9c7443b1b22627458a487027ba87da7f2d4917162825463acca2d421`  
		Last Modified: Tue, 21 Oct 2025 10:20:40 GMT  
		Size: 7.4 KB (7438 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7966570f367575c3ab83dff8a13a9fb0764056749d7ebae13e7baf5109ab92f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127015920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ad319755704bec7ee46c1413b7362bc77b3aedadb541af7faa7333390b1d77`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10d430deaa3d2ab4898db053e80d62403503897839bf6efd17ed5412b18d7973`  
		Last Modified: Tue, 21 Oct 2025 00:20:39 GMT  
		Size: 54.7 MB (54699294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453fe6b4c7a680d5464137a3450d263e01a7ec4d491659295432d36b0198bbc`  
		Last Modified: Tue, 21 Oct 2025 01:53:19 GMT  
		Size: 16.3 MB (16267847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96adc169c4af311ffba07fa68db5821d6b9b00d285e00f44dad87eff52496658`  
		Last Modified: Tue, 21 Oct 2025 02:35:42 GMT  
		Size: 56.0 MB (56048779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4c9df0a22b7d3a6724b6b14fe0e48e52fa30e19065d9250f19549d2d785b993d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7382970d08e68ee4e92e287f0629ad33bdfb15e48058e3251dff710a4ee6ca`

```dockerfile
```

-	Layers:
	-	`sha256:765f62082a7704977a6fee61da98b3b442eab5bd0bb3f18f5e2b3deb7ee3fdb8`  
		Last Modified: Tue, 21 Oct 2025 10:20:46 GMT  
		Size: 7.9 MB (7907730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdfee4342b25bbbf25d7a89b499316234c2c01708957cbf204c77def5ea0dd2a`  
		Last Modified: Tue, 21 Oct 2025 10:20:47 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json
