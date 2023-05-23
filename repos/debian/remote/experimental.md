## `debian:experimental`

```console
$ docker pull debian@sha256:42ae5d5105657b43d5d934fb9fa8a04e5ed49d472cbd872c22074c78812dea63
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:dde1617d7748bb57ba85a784bf30ba18879bbb19716af321fb0da1f1999638aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49299496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992fbf71860210a94838145a5d1647dbc879b30ae0b92daf39fd8eb758ae7f50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:48:33 GMT
ADD file:3bb0dbe1e0e6f100e1b1bf234d8abb124cb76a74c0a6534b96944aae00f2d783 in / 
# Tue, 02 May 2023 23:48:33 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:48:43 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b09d7a954016db203b7b9a15bce1153fb2a053c8ceeb27b62838c6a42b01e46e`  
		Last Modified: Tue, 02 May 2023 23:53:24 GMT  
		Size: 49.3 MB (49299275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c05a75dcc93de27a408b593d23b740952d152e3d644127ad318762a50f877e`  
		Last Modified: Tue, 02 May 2023 23:53:43 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:92e8a98cd450eb9990a43907ad64e8e208a8ea022c7db9b6823d15c4a4de35e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47154842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6d1b9c54675ebe8bcb614b978888db67533f1e1f2b94065d808cf75a44f23f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:49:37 GMT
ADD file:06d5b7eb037ca70ff6e0d5ff9f3b010eb10bcc4a5b00394ab4f9a246411741aa in / 
# Tue, 23 May 2023 00:49:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:49:45 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:cfe1aac17e16a426fa89ea12b89a503245fa4f59f7839f7b14f036bca90f216a`  
		Last Modified: Tue, 23 May 2023 00:53:10 GMT  
		Size: 47.2 MB (47154621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ba7d3712a5ff65b11b85dc26e818ad5216bb60db193573a65cded9f00280f`  
		Last Modified: Tue, 23 May 2023 00:53:30 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:3673c15db4ae7a9a7cec7436484f35da2696f02d65fa45d03fc7ad1b910540b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44981520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d7849acf7a73b003b8fb8bb369cff9b63a164a8de207a13a5f29e6d1b1e5b2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:59:55 GMT
ADD file:5c960c8b5b368fa82ba5a43d4520fe55acbe494297500cd45382691a14565305 in / 
# Tue, 23 May 2023 00:59:55 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:00:08 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:fd8c437aebcd42ecb5fafa2f0020b4a9b7456b306c763c5f18ae67495887099a`  
		Last Modified: Tue, 23 May 2023 01:04:44 GMT  
		Size: 45.0 MB (44981302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee5a22e9af0e6fe5429613ab1bba0085ef132496c7ef44cca0e41e2c632e424`  
		Last Modified: Tue, 23 May 2023 01:05:05 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:78bf4035b0816588889f36b95f8c165bb359d1b8d01b4cefcdbc9b8a6103bc2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49336508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8feef3cccdae01c0afc338cca950634c715009b3beec5d019c6104cad9e702e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:44:26 GMT
ADD file:ebd526e2961989ea15e17f6a59d4f726b04e4f9d9090b7c7c2ab6d8cfcfbad9c in / 
# Tue, 23 May 2023 00:44:27 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:44:34 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:dcfec3ec3c72f5fefa749b865b88c0e1a15e954476a08c211a0b1f8c54f5e9bf`  
		Last Modified: Tue, 23 May 2023 00:48:57 GMT  
		Size: 49.3 MB (49336287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016237f70c27d7739de2b310417ebd84f259a6c7525a0cb5638f7daaa25a91f8`  
		Last Modified: Tue, 23 May 2023 00:49:18 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:80cc70e41f8bed37267ad513b97c8c7b9309b4fefdc5971e33de641a3bc65dec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50311711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd62d04e96f5e3ef7d0174f239ede25b51c282aeafdfe2dcc46206bed059969`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:42:19 GMT
ADD file:ae4f2bc5b817fffef4493eb16903755b84ad67bb02bb591d0e3a570691d4c118 in / 
# Tue, 23 May 2023 00:42:20 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:42:38 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:e66ada6b4cc88233b31e97de30566f45c333e11f5bd3c68305dec1b405eb8347`  
		Last Modified: Tue, 23 May 2023 00:47:58 GMT  
		Size: 50.3 MB (50311489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d755ed4be60fcbdf77161f203bbad61366ee8f2ab4ffe9c43f019eac5a5d77b`  
		Last Modified: Tue, 23 May 2023 00:48:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:6691a30206d8af0061a1e30fcb3fe172024ad5b6d58a7d02b1e214d3d5c34553
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49301655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5612453c73a88f32734de438592cbb9257d4b80baf15075844255e8f2e441509`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:54:16 GMT
ADD file:5acf41935c7e4664ad9eaffb8eb6ff951f25e96188c7bb68c05b3beb4a05ecfa in / 
# Tue, 02 May 2023 23:54:21 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:55:07 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0f41ec9c841e5471c15b435f5869be0c4ddab2c10b732664d56c272673169ad2`  
		Last Modified: Wed, 03 May 2023 00:02:28 GMT  
		Size: 49.3 MB (49301431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599a125a54fcfe85549f7fe92ec5b299bd3ae7d296e67bea9051dbb9f99ec94a`  
		Last Modified: Wed, 03 May 2023 00:03:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:4c866810823c62a7844c2495b3eb75eccc17a8dad679e713b890bdade7d29d9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53307458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ffef5b9d82037088e3feb5777b034256afdbb7d86accb2ae20652ad3b2548`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:34:17 GMT
ADD file:d498e75413458f1c6bdd385979e04f5e5085f37e00fdcb059e44f1639a29d1c9 in / 
# Wed, 03 May 2023 00:34:21 GMT
CMD ["bash"]
# Wed, 03 May 2023 00:34:49 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:3b82d74fe886bdecd3c7d8ffac00d0f6edf10e6cd5283660a7d9482dd7e47b05`  
		Last Modified: Wed, 03 May 2023 00:39:36 GMT  
		Size: 53.3 MB (53307236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275de5e09bc2d486f0a16375ad4b92a68f76e48e0f9a2075fcad79241febac5e`  
		Last Modified: Wed, 03 May 2023 00:40:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:38e3817d7cbbb1af3c31a9af2f8cc212c89dea301cf288b381929ce328939e7b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45503602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc229240670f80e5613000ae27ce177561eb21abf2d4e9a6b2caab58de183477`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:10:36 GMT
ADD file:e496023e002786078fa69af53f91ea5969cb992f9613c2c02ee5829f1e274c1d in / 
# Tue, 23 May 2023 01:10:39 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:11:24 GMT
RUN echo 'deb http://deb.debian.org/debian-ports experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:0bedc13cc51520ede5618d51c5f5b80761d859b702542f47677b538b9f89a408`  
		Last Modified: Tue, 23 May 2023 01:14:00 GMT  
		Size: 45.5 MB (45503373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71f4945848e06792887630a5bf0d3832fae64533624ef53a89bc21341dea423`  
		Last Modified: Tue, 23 May 2023 01:14:48 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:f0c63346e7a5532e20a840c4655d55bb32a182ee9e9a3c353561883550605d4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47664855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8119c4cf855cdc6946e158f9a067475268d7ead872383b6301d365b3993c3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:44:10 GMT
ADD file:0c9e972d544fe6e81eb953543682ec7d8375b62d3f07d186dbc7328d396e3f64 in / 
# Tue, 23 May 2023 00:44:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:44:29 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
```

-	Layers:
	-	`sha256:b2d77b4930e933cff097e4824d35c62331e60c1e124301fd6700bd7a8cfe7df1`  
		Last Modified: Tue, 23 May 2023 00:47:06 GMT  
		Size: 47.7 MB (47664631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e7c86d2e476f9b038eae711e85502870ced7066de6194e49fa5ba8d2ee268e`  
		Last Modified: Tue, 23 May 2023 00:47:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
