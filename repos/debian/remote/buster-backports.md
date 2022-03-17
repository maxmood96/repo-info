## `debian:buster-backports`

```console
$ docker pull debian@sha256:971ee35fca632afa96362ec237b901501c9cd019eb9e08d54ea13c0c2749abed
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

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:9747745ff9df8b12a2c3a7394ae8be2d9fa4acb391e4e1b6f164b3196400dda9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50437515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fbad2555a1d45d486f9d446842272489c5deda84662b13b8f5b68a5f49f26b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 04:04:14 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d466b40f8ff785c2a0dee08f01ce7d40b26aa2dc5e83ade87437a76b216e19`  
		Last Modified: Thu, 17 Mar 2022 04:10:43 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:612b575ae9a2efa83954d384e00e246037fd774c0d72eeedb6ccfb5c2a49021f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48154474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d305020b6424514fea95b4798a557fcbd07a914f614f9ad0d0443afa58fdb7ce`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:20:13 GMT
ADD file:730b9bc3596fff58668f18193a6ea2255ca145eaf1b34fa9d8810bdc685868ba in / 
# Thu, 17 Mar 2022 05:20:14 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 05:20:29 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:32f373add1937d0609f8db562b840e805dfcbf8545b161486c2b18b6752b249d`  
		Last Modified: Thu, 17 Mar 2022 05:35:48 GMT  
		Size: 48.2 MB (48154250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59629f3f26e0edc76d9ef7ac936f6e518ed89923db0b2c7dd45609e9d4d7d049`  
		Last Modified: Thu, 17 Mar 2022 05:36:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b67e319d10dab4ae7a31143ab358dde10602b0a3521dae3b8505043e45f24706
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45918386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35577b3a819757817227b98911a143b247aeea4af3d8d1797b02e23577e5482e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:31:32 GMT
ADD file:7fe62421fc35de4e6311d22de22ded33c729d98a51fa41d57e04c76ec092827a in / 
# Thu, 17 Mar 2022 09:31:33 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:31:48 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f82e094db40ddc4d9b2e16ec4c7f28c689bdd532358e18ab566e90aa5975838c`  
		Last Modified: Thu, 17 Mar 2022 09:47:22 GMT  
		Size: 45.9 MB (45918162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c8c923f511adeee2ca9d969fd3744f24b101ef1608cf183f09d1fd52dad6bd`  
		Last Modified: Thu, 17 Mar 2022 09:47:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:fc4e36745648449c9a62b5797e2c2f141e6ef7bf6efcde505391f3dd8cad74dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49223215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10241f800d96cdf6d66a9ae8509c390dd5dc26b5fa3c28b00dc01ae0cae4cde0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:08 GMT
ADD file:37cabd1fec04269c22fc158f62ce5bc655934f2e58fb1ff3a1e366a33ba9bc18 in / 
# Thu, 17 Mar 2022 03:22:09 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:22:15 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3996f04b7c6c17d8b25c04c7287353b896b4a0b10ab440f47d00573a7d5c3e17`  
		Last Modified: Thu, 17 Mar 2022 03:28:59 GMT  
		Size: 49.2 MB (49222993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4227b32f36e3f83eedf9729ac76e297625150f83c46cedc2b9c667a234520d33`  
		Last Modified: Thu, 17 Mar 2022 03:29:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:4e44b7b5ece19773f55d0a5e91efbe93b3958cc29ce654063ce17308aa94af55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c037d2041a1f08212533f8e9d6369fa900ca9a9e2f05a68e6026e651b80657c1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:16:13 GMT
ADD file:c069a284517c64971f8c4fc783f45ed7af57d809cb522e4c6ab745beb6d28f46 in / 
# Thu, 17 Mar 2022 08:16:14 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:16:20 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:be983526b2135a371db2ed9c61f4a8fae0b68ae32011ead5c236b381aaa90b93`  
		Last Modified: Thu, 17 Mar 2022 08:24:25 GMT  
		Size: 51.2 MB (51207701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d5df3d33c55aa3de01dcc81a97ccb827deae9becfaabbd8ccc302aacf33c9`  
		Last Modified: Thu, 17 Mar 2022 08:24:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; mips64le

```console
$ docker pull debian@sha256:748e57613ee0a85251b495192ca0be7b8ce0b162827a3410930450dd6373b3fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49079685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0b306f6331622c0276853d2f22734d15bc8b6e657f50b09e7e1ed303a8fca3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:53:34 GMT
ADD file:a0b3ac9e4bfb39c253a8a7a55fb55d0b908af833cdcc9931837698ec5f55b989 in / 
# Thu, 17 Mar 2022 08:53:39 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 08:53:51 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:047b7fb675b6ff99fd7dedbd4d0b0a3242855acbf0be0e3a69b39ea19852bf7f`  
		Last Modified: Thu, 17 Mar 2022 10:44:02 GMT  
		Size: 49.1 MB (49079461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebf4134930b5b2738775b3830de7c70e6eea012e3661559644a85f27e7fffd5`  
		Last Modified: Thu, 17 Mar 2022 10:44:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:b9aa560b1ba5a54d403c1d5ebc8784b4940d86786b1d4ba244dde38b2e654085
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54184061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73155c03d3c89f733f2d17a922804a4478908d8dbf4d15bc08637e6b8b1be0a4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 11:18:17 GMT
ADD file:f75a960e2412d5d93ea52573154078e69481bda1da84f66aac3871c0c0776bfd in / 
# Thu, 17 Mar 2022 11:18:29 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 11:18:54 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c525619180c8f2ab5210413380ee35a9d0855c7e877e0ebe8841a1724e9605fd`  
		Last Modified: Thu, 17 Mar 2022 11:28:49 GMT  
		Size: 54.2 MB (54183837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e724002d16db510ec5a0c75f8ffa4ec1a964fdb14cc405be88ee72e361499a3`  
		Last Modified: Thu, 17 Mar 2022 11:29:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; s390x

```console
$ docker pull debian@sha256:ad28eb5a9372c5fed7864c8deb6e84413a18d8ed89ea9ced8e3933d1cae6908b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49005749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1652897502fcbabb53ccf259de67ea8e1c0e0594e0221a3ee170cbf1ea6a99e1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:07:11 GMT
ADD file:6505b8e134084dbb9f879838b24cf47cd265cfdc5952f50ba2ddc63ff4553145 in / 
# Thu, 17 Mar 2022 03:07:14 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 03:07:22 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1e9fa32475c4074341da88d0325d6e125bf7587795cba4bef553a90bf7472c7b`  
		Last Modified: Thu, 17 Mar 2022 03:13:01 GMT  
		Size: 49.0 MB (49005525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f4e2f8d906fed8d0e36c657efad0d2a602fd655372942712ef268292052d7c`  
		Last Modified: Thu, 17 Mar 2022 03:13:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
