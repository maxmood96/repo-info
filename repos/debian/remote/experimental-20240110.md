## `debian:experimental-20240110`

```console
$ docker pull debian@sha256:cd4b4b73d773db37c83d249f24594b04f1ca2852fd5e33fc0f1bfe92f890e91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `debian:experimental-20240110` - linux; amd64

```console
$ docker pull debian@sha256:eafdd12db5f089c57f6ed5b2acd2b54e83fb062c20c2457838c67ba8fc4c206d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52268192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543cf72347d18a13a6a4436422ea063f48599d4417241241f39425f48fde366e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:42e039e7431c45e6964a9c1e010c1f27058674fe033b4776a0ff57cf440cf4d4 in / 
# Thu, 11 Jan 2024 02:41:00 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:41:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:5034daaeeacb913210f35d8d0a56db2b63da34113519142a5d7bc899ce3d4499`  
		Last Modified: Thu, 11 Jan 2024 02:47:46 GMT  
		Size: 52.3 MB (52267972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4a39f1f4e6a5fb0ca81fa836f27cd2923093b47a69ca0ea411582f8d3c8277`  
		Last Modified: Thu, 11 Jan 2024 02:48:08 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240110` - linux; arm variant v5

```console
$ docker pull debian@sha256:240891218fb67f7f0881ed2b10310938505ec94fe2e75031961bdfff3d8abedf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49383348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a46ab91b0037b10ba7e56f2f97eb8bd1e8d92bd66d8f65b719bb054b4b909a0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:52:05 GMT
ADD file:6421f10ce23553eb1469fc945a45b66c8ca7f4b875a024021a3fd3ab8cd40ef9 in / 
# Thu, 11 Jan 2024 01:52:06 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 01:52:22 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:726d30ff210a351b8c80ee19035aff7481d590e4f6983745a5822f42af4a70e1`  
		Last Modified: Thu, 11 Jan 2024 01:58:21 GMT  
		Size: 49.4 MB (49383127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ebf7698a49d2a7fd3ac0401b654c6631d4ebe9368411a348141a882a1bed0c`  
		Last Modified: Thu, 11 Jan 2024 01:58:45 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240110` - linux; arm variant v7

```console
$ docker pull debian@sha256:41fe265e9567b7d7ebfd84d8dda1e82d5a92ca3bd4bce96bc6bb25e603fd667e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46880584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab8e8f8951879474ab95f8beca3be671bc18d447c3752f4b50c7baefb212474`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:46:13 GMT
ADD file:4be8ecdd78ddce2c3fa22cbedba684b785d1d7940c7cbfd1394158f462cbd6ca in / 
# Thu, 11 Jan 2024 02:46:13 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:46:28 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:969ccaa70a6af7f4a690192ed2f0fbad5db4a4b2fd0569d8b6e3844eb7d50fe8`  
		Last Modified: Thu, 11 Jan 2024 02:54:10 GMT  
		Size: 46.9 MB (46880363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5604cf088dc67109766556568ab57935daa2e7651f7de2133805f3723b95002`  
		Last Modified: Thu, 11 Jan 2024 02:54:32 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240110` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:01eaee4dcdb3f85b10ba4c41a1697fd2f7cac019ab33e57b1bb891824746f751
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52148961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1d1f39e7116b17e9c4e9dd51e1e995ba377f567007b7746149ec71870b743a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:45 GMT
ADD file:608c704e6e475ac19fe61b7e654046f5e58707f2e07b680dc2dbb04f4a9c5a1e in / 
# Thu, 11 Jan 2024 02:42:46 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:42:54 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b5b5f2db1eaad49e8412d795b8ca56719afc870d79c1f80fec0d16990c82976e`  
		Last Modified: Thu, 11 Jan 2024 02:49:05 GMT  
		Size: 52.1 MB (52148742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2d8a8a55c273d798a0a7affb959cbd32b04dd7b5e991cfc185727732d08bfa`  
		Last Modified: Thu, 11 Jan 2024 02:49:25 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240110` - linux; 386

```console
$ docker pull debian@sha256:315d42cd2c367038a23bcf9b37a4b2f095666a18978a8273eb337a637ddc5f0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53117889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d54697bd07d0d1e03296bf74201e669b65b99f8cb2857ed654a4094cbd2ae0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:46 GMT
ADD file:334f073ceb41a33b4d30066612ad686dc754ef70880c138059c9f47380913548 in / 
# Thu, 11 Jan 2024 02:41:47 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:41:59 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3bc3b266d4a2b9e3cf0959cc2a1b9fd5a698234fdb820d0e7ea3846fe01523b4`  
		Last Modified: Thu, 11 Jan 2024 02:49:31 GMT  
		Size: 53.1 MB (53117666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e628583756f1ee7aac20aaacd40d3e79f614d04877247d12819fe42ce41624`  
		Last Modified: Thu, 11 Jan 2024 02:49:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240110` - linux; mips64le

```console
$ docker pull debian@sha256:85b882aa22ed22b5582b52efaf0861d654a74740b09ed8324aad93e03a013719
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51364574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ed91ac3647ee9c40a02878a01e85bc2d3d2ce77807d302f8f4eba92da138fa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:19:41 GMT
ADD file:a79610f987aa49955031fd8ea184b5e3f20f8897419597396ba2e7335e4257c6 in / 
# Thu, 11 Jan 2024 02:19:47 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:20:28 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:23319e32b692e6922a61864786c14a39d3906b1dd10fc3f87141d5ec2f0b2348`  
		Last Modified: Thu, 11 Jan 2024 02:31:16 GMT  
		Size: 51.4 MB (51364354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f225ec84f9fc6cd8a6050b83ad62fb53ddee4d37593d269c1ccaaf27f251a0`  
		Last Modified: Thu, 11 Jan 2024 02:31:57 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240110` - linux; ppc64le

```console
$ docker pull debian@sha256:d2a74428028412e0335709c2cf9ce5e5345962d680ead571b6e948cafd73ade5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56185903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761421242dbe1812b11a547c36cb6eba597f453cdd29d984e125be2c9fa9b1a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:48 GMT
ADD file:fbef07e112c2123f5772b7c5101f1880745fb49c5d1fa02f6b1b6c9f74a88ecb in / 
# Thu, 11 Jan 2024 02:37:52 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:38:08 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:239f6363ceccb91b1075577f2b8243d250f0a9ac660308c5d60a45f70a66bf2f`  
		Last Modified: Thu, 11 Jan 2024 02:43:46 GMT  
		Size: 56.2 MB (56185681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d95eed545950e7bd86878d5467dee58e009d1c2f942e9067f4dc807fbf5ad3`  
		Last Modified: Thu, 11 Jan 2024 02:44:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240110` - linux; riscv64

```console
$ docker pull debian@sha256:fecbc3d7063858aaea9af150dbc553431c98ec219aa4b34db9b6a3bf9b74458a
```

-	Docker Version: 20.10.25
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50488087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4135e16105b85a749007aa2bc455e3ce0e21a4efaa03a2e140515fb8710b3ece`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:10:00 GMT
ADD file:6d94e2f20f6e0e1e5e2c91117675dcad00b7c8590c93b573935c0a4b16c0e47c in / 
# Thu, 11 Jan 2024 02:10:02 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:10:34 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:6d8bfc8597070f25f5bdba166dd1a89d39e0ba9270fca879186dec0954cf8222`  
		Last Modified: Thu, 11 Jan 2024 02:13:15 GMT  
		Size: 50.5 MB (50487864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158a0dc420216d587d16cc1bc2356e6df4299ecad92327ac654b6815d65f2172`  
		Last Modified: Thu, 11 Jan 2024 02:14:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental-20240110` - linux; s390x

```console
$ docker pull debian@sha256:de4fe7c1d621aa0bc5c1b07803ad5b3b470bbcb3cca9091234c4350961472796
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51672410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d5a7477de6e7ada4d0e033dc842722378540a8d3b8e1c055c3bcfdb6852c08`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:49:05 GMT
ADD file:dc92014fec2fbae8cd1446391e32c3134a1aafb6dd85e0b41cb5238292bde04a in / 
# Thu, 11 Jan 2024 01:49:09 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 01:49:31 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:d6b9ae8cafcbd48118ca1b9c3b8e5d4c9e9784b131af1619d6e28acc6b35a8a4`  
		Last Modified: Thu, 11 Jan 2024 01:53:28 GMT  
		Size: 51.7 MB (51672192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1858ded998553b483c992ce70bb3cebcab6367bfea4370f95fdd1f8dcbead47a`  
		Last Modified: Thu, 11 Jan 2024 01:53:42 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
