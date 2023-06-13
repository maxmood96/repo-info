## `debian:testing-backports`

```console
$ docker pull debian@sha256:c3fc0856ac20d4c11c8ce9d8dff449bf6c93578237000c28267635a3903f6080
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:ad44ce21476bdc3413c59e267f3b876c83dce135c717a721e5497ea8d1db0db2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49552333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23c96d04fe8ef5db0b0e6f7392791a72d2b67bc5f727e15e52b144ed2103e6e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:23:22 GMT
ADD file:418560b5057bb018516c119e87b040f82c7dce4d4961e8bf73268adb278e1635 in / 
# Mon, 12 Jun 2023 23:23:23 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:23:27 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dfaac2cc63fd541e1c2e3738569929f032b19fa4217d0885ba3920b8a4e9e69d`  
		Last Modified: Mon, 12 Jun 2023 23:29:32 GMT  
		Size: 49.6 MB (49552114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a0cc64ae67aaa051a092beb142cc5e0a3bd6692808014c6f10eb35a783a92d`  
		Last Modified: Mon, 12 Jun 2023 23:29:40 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:7648dd154d7dcbb20c1a937e134787e976d775a8c4738c63280fc26bb3305d8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47403455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350b70005bda1837555e203cc078b5f4548aa5a85c04dd0648c7cae564f2df5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:49:39 GMT
ADD file:35030d9d4624a1a802acfb4bc440ed2f55b7993fbe0bf5b2792190de725c633b in / 
# Mon, 12 Jun 2023 23:49:39 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:49:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2384ad9b3804a19403d23168d3fca6dcc9be198493eb4cb1dd0bdba8f7cfc839`  
		Last Modified: Mon, 12 Jun 2023 23:53:58 GMT  
		Size: 47.4 MB (47403232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9b59de89a20535c1b038c48550dc28808412649595f65c9507e409acb1c29a`  
		Last Modified: Mon, 12 Jun 2023 23:54:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:aa53d8c74f66d41efd8598b2bfa6fe55230dbadbb781219afc7e9083d036c132
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45236393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f47c028ff26d547c33ae2a296b3678cc5c7dae5e754759f118052e44cdd5a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jun 2023 00:01:27 GMT
ADD file:b64c67ba0e28271141124bab3303d56c809b801ee29f7f6620de1c8a1de21b89 in / 
# Tue, 13 Jun 2023 00:01:28 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 00:01:32 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b2ce7d8b1c0598c2e67a91cf379ce592bfe21db85460aaa797339e82750d3319`  
		Last Modified: Tue, 13 Jun 2023 00:07:31 GMT  
		Size: 45.2 MB (45236173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f55427d67232dfb48f4fb4454483c99e94000e1c4b5f47d77bc642785c8b51d`  
		Last Modified: Tue, 13 Jun 2023 00:07:39 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:22b86a48f0f1d071e29e4c2dcb7d12c2e86bf0720d9da6c583c2d2d8292046cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49573381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702a4e3a935b382e27d8bbf73ae4fb97213a4413e978abb65ec59245af9c7497`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:42:15 GMT
ADD file:9538b10221306d569a3379a42ad14f6a04e3400effaf2e6093c219ad3ed820ff in / 
# Mon, 12 Jun 2023 23:42:16 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:42:19 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7f36dd606efeffdc09debbf5d2f9a2a9f9cc7b769ef21cc6ade380d05fc0bc8e`  
		Last Modified: Mon, 12 Jun 2023 23:47:29 GMT  
		Size: 49.6 MB (49573160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df6782ebeffaadec7aaa82de0a63099438deb7916ee4e26fee93e1bce399c5c`  
		Last Modified: Mon, 12 Jun 2023 23:47:37 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:fc30249799e61e937c89665f31eb3c9276c79052e245cbdc31e47cbbe7bdddca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50562617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac193aa9c4f727eabab408d298c4739d569a8bee63c95458e3e184cb0f9ba4c0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:43:23 GMT
ADD file:f24049f634b6590eed9ed3e10420c4d00579a880a5a561c7ef5c6f03611f432a in / 
# Mon, 12 Jun 2023 23:43:24 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:43:29 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9879a6f3c670f447138db14564ed395b00d6f91ed6887a41bbd0e84282f11130`  
		Last Modified: Mon, 12 Jun 2023 23:50:36 GMT  
		Size: 50.6 MB (50562395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4489f332182d9e27b163e16c834ffed4169dc5fc8703841b6a427d5d538f7e7`  
		Last Modified: Mon, 12 Jun 2023 23:50:44 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:54100d71c786d8db8d8562af7023a5d293aadb4d410d3a25ebd7f2ca8a41ae3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49304464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2ec23af9bedb49503f1dd78d6f8af5dc7a0785c3677d4f39471e93eea43367`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:13:46 GMT
ADD file:7dc98d86d0fc624f9d3bdb025637a3999c222454b159557cd5c010871a74836d in / 
# Tue, 23 May 2023 01:13:51 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:14:05 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8119bb11dde1051309b0b2b2d7fcdf8ca913220682229258d5650bb2ec33b863`  
		Last Modified: Tue, 23 May 2023 01:22:23 GMT  
		Size: 49.3 MB (49304240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261c33ef7caed46449ba2a1064f434b2a842459be15a6f8b935f4393bd365bb2`  
		Last Modified: Tue, 23 May 2023 01:22:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:db71c86aedfb43273383f9b4f0d360e9f17a5dc1a278512899df622de181e583
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53536978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa43df3a03754d00f193191cf5a7b567f9d5669899712ee090aee9722987e78`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:50 GMT
ADD file:c800eebe5b5256d5f3eb9d436f7401634618c397b30f31d8beee6daa24772dee in / 
# Mon, 12 Jun 2023 23:20:54 GMT
CMD ["bash"]
# Mon, 12 Jun 2023 23:21:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:da363b5a528e02b2ccc2452bd956ac683fa34d495ffdfd1407ffd0bd41cb001a`  
		Last Modified: Mon, 12 Jun 2023 23:27:36 GMT  
		Size: 53.5 MB (53536756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e23b368c7284e37b37c0671c043a33f1458cf8106cead436a2ce1315c3460a`  
		Last Modified: Mon, 12 Jun 2023 23:27:46 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:778bda3594123edabff13e3e31a198185c1733491e2d01eeb7cf0bff4a37d005
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47673699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd56d7f88324543692eb5a3696d99abce18b523e21bd366d992a576f04d50aeb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:47 GMT
ADD file:6dfd7d21cdfe9dee2a7cad47d8e2e22e6e56bd924f036cb45c183fe31efe66cc in / 
# Tue, 23 May 2023 00:43:49 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:43:54 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:af4d11b0c6366f32a980344976c0622adf11030b727c114fcc65377cb3f44688`  
		Last Modified: Tue, 23 May 2023 00:46:43 GMT  
		Size: 47.7 MB (47673474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913ea609cdd6a96e8cf48c4709c1519473bb0da85b3446ab5f8de88a50de77ec`  
		Last Modified: Tue, 23 May 2023 00:46:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
