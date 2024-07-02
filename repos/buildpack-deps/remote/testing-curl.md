## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:68ed64592f22aab5c475e9d29a49adf41ff59c0bd8fc8df8d9f2d1e770d9cdcf
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a471b9f5f0195e610360beac865f81e742d8cb57e28d2532fed71471857e34b4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71480045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f26c0be575dc37382ba6ce1648566ddb7895c88cb47d78fc611766e6aed17c3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:26:59 GMT
ADD file:90c4ad8b280b16131f305780a1f2721616642bd4d5b4a26256c760cd8ae98f27 in / 
# Tue, 02 Jul 2024 01:27:00 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:54:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ca828e2fa86974a7bad5159e89a3c4f34921c624322a7fa71026f2a3933ab620`  
		Last Modified: Tue, 02 Jul 2024 01:31:45 GMT  
		Size: 52.5 MB (52458214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687f3d296dd0e92cd772395160b84eeaffb55fa2ffce846bc61595e5e164a5e3`  
		Last Modified: Tue, 02 Jul 2024 02:03:19 GMT  
		Size: 19.0 MB (19021831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:25669415fbcdf1354b3991c4788142680cbf0648133523e0c55c7dacca573595
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67490378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c2548c3385b1db245fa37ce227bec514d361939c525af81608f2f92e757df3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:49:52 GMT
ADD file:c318229166795e4eb716c1fa6af23bbb2d4ecba024b60f621a291810a3a401d4 in / 
# Tue, 02 Jul 2024 00:49:53 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:20:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:000d0bc5723ca659fec8fc6ce252cb52307971eb476903fc3b9275de15df06e8`  
		Last Modified: Tue, 02 Jul 2024 00:54:39 GMT  
		Size: 49.5 MB (49521421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736d7cf5b3e3c6cf6b2dca2768e87625a43b941f89b6406ba80bef82b5dcbee3`  
		Last Modified: Tue, 02 Jul 2024 01:25:57 GMT  
		Size: 18.0 MB (17968957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f6358ff67db1b794c655470070aa7ae2d47b9780302e346db15ddf03b6881917
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64390088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c39f994bfe9f2d34c5b533e85935a39cd2cfe452c61368c68a994c3b01b1b8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:01:43 GMT
ADD file:527e478975b1f859c9421d232809fcdad4ae845a2591655169c3c0cbd9556cb0 in / 
# Tue, 02 Jul 2024 01:01:43 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e4626e10f2b2fa1f8bd684a19417be06dce44506821e68c986c039ebcf444ea1`  
		Last Modified: Tue, 02 Jul 2024 01:06:18 GMT  
		Size: 47.0 MB (47028058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdca2198e49697301427c37393c92e7e2c23045ee43c3f521b70811fad9baacd`  
		Last Modified: Tue, 02 Jul 2024 01:42:27 GMT  
		Size: 17.4 MB (17362030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7e59002f0c5a17bacae57287d22ffb537dbdad7313e5584c0587c37995b68dac
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71456321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0958582e9224f89984a38c8702208aba470365a870911c829cd325bf7962df7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:56 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Tue, 02 Jul 2024 00:40:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9751e3702568b536545773c8a831b25db2876eb1b4d0823a3cfa663395793f96`  
		Last Modified: Tue, 02 Jul 2024 04:04:20 GMT  
		Size: 18.8 MB (18763001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2b635714752d3af7f80a147a9c20541a052b4703145fbfe8e6610410558b1e1e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73362786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f5e2a64a18f982d1dc95e718ad126b7650e01bc02bc3834b63c9729e374fc7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:52 GMT
ADD file:2c79a29515e7dc495de2293d9b08d4b2ecee86e61c2d0adf1658f7b939d57c1c in / 
# Tue, 02 Jul 2024 00:40:53 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:86c6de18cd170a5e610d31625f09596aeecc408fed7171fc8922ae0196331108`  
		Last Modified: Tue, 02 Jul 2024 00:46:09 GMT  
		Size: 53.3 MB (53333176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed3a89daa70bb513739a2ade83fc5f0a43a784f37749e2584d3c335224ae6e7`  
		Last Modified: Tue, 02 Jul 2024 01:17:53 GMT  
		Size: 20.0 MB (20029610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:cd505bf91c12c08a4289625c59bea1475698fd659b06c48b2a5c19121ab040f7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70818997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7897221e27c34623ff76aa798a9658ee576864b8bb7ff73f4bc74a2032ea7a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:15 GMT
ADD file:3db649d00cbcab4f80ae59713bc5516d64748afefc7b50d6ec9b17f007a2d82a in / 
# Tue, 02 Jul 2024 01:25:20 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f6c6179e3393971283f4159a87b337ff64cbda1886dbd0e30fe99b15d1f2b7ec`  
		Last Modified: Tue, 02 Jul 2024 01:36:31 GMT  
		Size: 51.3 MB (51311657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8992fbd14e1b9fc5fdb381b9396a2ccb1f18397cae60807f219afbcf1579ac7b`  
		Last Modified: Tue, 02 Jul 2024 02:39:15 GMT  
		Size: 19.5 MB (19507340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:dd88f62378e80f72d7396599711d68aae701e17cabab2203b17671de6bab0510
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77327748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3904b2f6a4d5b54c4705ea4e96af876b9fb73619f09107e48c00ae700d39eb85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:19:54 GMT
ADD file:2befd9889f7183dff7c3af514af787c529a360a9bdb089a9e9db6dafcd6001c6 in / 
# Tue, 02 Jul 2024 01:19:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:53:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:1562048ab74aa86e6df4a38c0c8f568200759fc4f56abccc22d1df342f206dab`  
		Last Modified: Tue, 02 Jul 2024 01:25:27 GMT  
		Size: 56.3 MB (56345204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dea8d116669b7a9effcef7da51c6a3adb0b03e6013b8bdbdc06106781c822b6`  
		Last Modified: Tue, 02 Jul 2024 02:08:00 GMT  
		Size: 21.0 MB (20982544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:388a81ca3d83150cf7a1f7e88958d44337e71be71c86d8ca97b4757aa228d0a7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72297741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f0762ae32a0147ad85298b71644f95f1ab22d635c3accdcafcf100c350e3fa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:46:19 GMT
ADD file:8bed729fdb05f23c2c9685e4b49aca399cccb129d549ff0cd5178ece57a34073 in / 
# Tue, 02 Jul 2024 00:46:21 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:38:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7663a7e6ec84fcce1d022bfe86b7d77ebcf92e841e95456e76280883841e0985`  
		Last Modified: Tue, 02 Jul 2024 00:51:04 GMT  
		Size: 52.1 MB (52089479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb594591801b3f0f0c97b7761fc4001fd8d788cd8eb1fac03442aa5ccbab471`  
		Last Modified: Tue, 02 Jul 2024 03:47:01 GMT  
		Size: 20.2 MB (20208262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
