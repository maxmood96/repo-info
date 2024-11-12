## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:b188fb8b7ec61aa9eee91c8c8db52946ce31eff16d4b8e9e3a6cb32a0df1d0b3
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:2fb71d10ec46a08f1b2d0b642c1cdf69a295707b2d7f431ddaa9ae28637a7424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55108966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e051bf257d501a26d0d673db6e32d6ab97119991402b2bc7839c0db005858a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0cfa9829d4a96980bd6dfd8386d530379e46e08fe925a8c3649d30f7aa1d19d9`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fab2327bc7499add8ef077f46655dadd1daac1a753c402110a364e4ac967e5e`  
		Last Modified: Tue, 12 Nov 2024 02:01:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f2d5cb71fba95fd03fd2fbcc5195adbb2a870b49578d978d685490371b595d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13451394150cda0859e6b2d52dfec0618681543efae6f3725f165b00a8d380c5`

```dockerfile
```

-	Layers:
	-	`sha256:11df6fa4b4b4f7265c7b1744983973dff8b1f9234d6b74cdf9b9ce9e84c8bf15`  
		Last Modified: Tue, 12 Nov 2024 02:01:53 GMT  
		Size: 3.9 MB (3923886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1021945391be76b7c402318064b5d12c6bbb3fe6060d2dc9edb9b3819347bc08`  
		Last Modified: Tue, 12 Nov 2024 02:01:53 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:abddbee82ccb8e836abbf4ad40bf854ac2866f5c9ea8344273437201824f2ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50272511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8df2a31cacbe97ec47bf3290856d98bd6437dfbacf438418b9fc9b1f1cba555`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:130d96ac1c9b0265b665ddde025df25a7535a506f9f7eaa6238f657b3c674ff7`  
		Last Modified: Tue, 12 Nov 2024 00:58:28 GMT  
		Size: 50.3 MB (50272287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc7e4da9772796a89783392c76c7e1d41f82dfdd31e592f6d4af511b895ca63`  
		Last Modified: Tue, 12 Nov 2024 02:20:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c89ad4dfdb067e422a9a9510b57ca439b3be1abd56658f981c0870553f8607ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3b0f12d5057224480c1fa709442b0ce812aa0a404192e98364dfb210f0eda5`

```dockerfile
```

-	Layers:
	-	`sha256:870b23b88fc44c662806c6929d2a1214dd818f5fb95d61d589578badfa91baae`  
		Last Modified: Tue, 12 Nov 2024 02:20:43 GMT  
		Size: 3.9 MB (3925446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb06af96fb9e63ff80b07628fd17060caf94b93d3a80676951233b0f5c42506f`  
		Last Modified: Tue, 12 Nov 2024 02:20:42 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:55e33cbc3ce6e3ebc01afbeadb05b226a5b300e35e095f80ae1d32e268d3dd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53757307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2511e93411e535431e6a8baa48deb495b690dbf617734b69c91803c86abc760`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2e616e88a36231e3087e38b9a06519efe115abc097770fefb1d13ba8a2374f06`  
		Last Modified: Tue, 12 Nov 2024 00:58:47 GMT  
		Size: 53.8 MB (53757085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ef84c52af761c1739e50deed410365ff0cdd2c93ddaef68609a5301e30953b`  
		Last Modified: Tue, 12 Nov 2024 02:22:44 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d32c89a299af40e8ab681eef56218f8ff48b239257dcbdd65e92498c2857dbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ce45e8b9ec4b6503de0be7a112ab529058a690b54aede9889778512c15386e`

```dockerfile
```

-	Layers:
	-	`sha256:79f9ae613025cb503fe7c6d00b46716d5901bab1c721c76e927b7f839a638c04`  
		Last Modified: Tue, 12 Nov 2024 02:22:44 GMT  
		Size: 3.9 MB (3923464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:208b5e5a0b2195d553feae52778c06a6d6a98a8348d2bce585d90df588a62735`  
		Last Modified: Tue, 12 Nov 2024 02:22:44 GMT  
		Size: 5.9 KB (5921 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:34917a44872127e0fd713370b7aea6a7fe863e7724b59afd6905fe1dfcc2c88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56093896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8aaf57e3793d5359f6b0d89fbedd591d60c2fbbf977ce58444ec3e7bb13a4f4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c99b77c10702b09e0f451cfccfac1e921661c363f1b0a9afa6bba7c9a2832573`  
		Last Modified: Tue, 12 Nov 2024 00:55:03 GMT  
		Size: 56.1 MB (56093672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b533e07f3c2c45cdd09bba1a48f853d5978c15a7a400aa0df455b6425685702`  
		Last Modified: Tue, 12 Nov 2024 02:02:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:45d77459a78a9a102465c6756b1566a2e9f70ee806f6e387eb307d8af4d77106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706fd622b58dfa4fb30ff31b345b3beb8cded3bc70b7bc68c350eb9032a51dcd`

```dockerfile
```

-	Layers:
	-	`sha256:bc88b4f5ccb74edc924295ed776c8e2f35d27e90a9154ec9c5d75d7b45fa45ce`  
		Last Modified: Tue, 12 Nov 2024 02:02:02 GMT  
		Size: 3.9 MB (3920391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7359a1540482dc88256f94a101fc14bf207f724770e3253252eb58f61bf4e06d`  
		Last Modified: Tue, 12 Nov 2024 02:02:01 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
