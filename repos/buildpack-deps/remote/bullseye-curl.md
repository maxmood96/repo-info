## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:29ce8f8f3f705f5df1170d7ef98d4087ef66848f6a94f5d646805bfeb6af7b56
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

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f5e87d761ad51c9625c36282191f83934f8dde0ec200b656c0b4b7dedce7e319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69520158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4d31bcf5d3545a536ab6da2bf21139ffa960179e64f5a76b0c95a2038dd817`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b207d2992cc896d454c9800742e8280616cc273c55d7c7104beed0976369a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8c4ee7d66d43a40b27199a1fdb2a8b7f524df3357c489c7b9abf504ae22990`

```dockerfile
```

-	Layers:
	-	`sha256:5ebb9d1aa1eaae05cc775954f815f6f3788a30fd3053185d1d294c68be870068`  
		Last Modified: Tue, 01 Jul 2025 04:19:57 GMT  
		Size: 4.6 MB (4629093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4589906534b0974f1a4765aebb545fa2d3b85ff2613a357f1702f58404c6f93`  
		Last Modified: Tue, 01 Jul 2025 04:19:57 GMT  
		Size: 6.8 KB (6800 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b9008451d4470a468b67ec19ef2dd4f7cf476eec8a734a2764401ff7e30daff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63924626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e9cc9c03bc387d23923e19cb4ee5df6774a59ceb7e0106beca1dcbda66e170`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc9ba38020b34f4e3f562e110c9ab25e658493eaf95bfc783a633f2d4b036`  
		Last Modified: Wed, 11 Jun 2025 20:11:47 GMT  
		Size: 14.9 MB (14880672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9ea17bd7094a0c2702c4163e2d05ee9f740d03dc9b4b525d4c9a39930b8b78c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9eede969f6f83a3716f751af3d50b0769c48852fe4e1ef10a342c3ded40ee5`

```dockerfile
```

-	Layers:
	-	`sha256:f6c147fb19322348b1521922cae7e1d00eb582c6e9f8b35b8c90e47ce23cf888`  
		Last Modified: Wed, 11 Jun 2025 07:19:50 GMT  
		Size: 4.6 MB (4630729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868e427b47bcb780df552dc621d7cb95f421dcf4897424cbf078b01de94fef0a`  
		Last Modified: Wed, 11 Jun 2025 07:19:51 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c4228ce5e4dfe1a4b02095e5ff1c3e4a99c9e9951ed25079dec21ce1e8e83084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68002970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db933836981df10b588f7f446e82b7cfe83804bd722d1c57aed62b410649241`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5424250d141bf5f4ec62e698bba9b5695482a3015186d3b14a633da8916bf7dd`  
		Last Modified: Tue, 01 Jul 2025 06:52:24 GMT  
		Size: 15.8 MB (15750716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f04207a6c130253857376bedd99c71ffdcd1f6940f96f99d2bafa8c5b1183df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4482c1304bdd3e5ca6887ee49c5b54b6abc4e97b8e35e0c28ca5a6c1c025b0`

```dockerfile
```

-	Layers:
	-	`sha256:50462286d21c4dca8006b1fe19ea5700ad4cca10fd5ae2e0dddbd552986c4fff`  
		Last Modified: Tue, 01 Jul 2025 07:20:14 GMT  
		Size: 4.6 MB (4628707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5622aa18f187f9800af1e3bcbeea93334b921d85e10040c8ec1d96a715ede2e`  
		Last Modified: Tue, 01 Jul 2025 07:20:15 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ba1ad4c8719c5098d09319b8b61c4fa3397c265a1ea4e63c70d228b6e3531b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70958841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ad9fc4e91cca44af3cfe1ec7f31e85d103d033ceb6d69b9a66701b566a6a80`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113be81052ec8e8323c4db158dc9c99295355934e950a6367e5c27038fd1e04c`  
		Last Modified: Tue, 01 Jul 2025 02:24:43 GMT  
		Size: 16.3 MB (16268907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:014edbf4b6215102562f976a2080f440f6110a86e0721d81ba7deb23bb95b953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2860a767453f0573834149310cf4257dae9ada5e3bda5b537dd7899cd1a1365e`

```dockerfile
```

-	Layers:
	-	`sha256:1200646dc248cda6cfed261005b18f66122ae09ff4fda1f8fc41c5bce5a17481`  
		Last Modified: Tue, 01 Jul 2025 04:20:14 GMT  
		Size: 4.6 MB (4625596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd0102821b39e04dbfb7026f5ef48aa7fa8fee03541a0fcbdf4bc7013b577a0`  
		Last Modified: Tue, 01 Jul 2025 04:20:15 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json
