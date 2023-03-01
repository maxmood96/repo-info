## `debian:stable-backports`

```console
$ docker pull debian@sha256:2f009f56c72a94a74f5e0c1cf7494f6bf167da3b8c20558864f245c030e15fdc
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:fe191261248867971848f3bb51dc5b384ed4a7b9eebc56f986f3af490d008f49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55046204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fa63c7a9bce28bd07f0e7b10baac4eb97eae10d3cc001273864df945999ea4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:11:18 GMT
ADD file:4902855598159d0e8097c7927725e57b89a4bfd7e1793fc0dafdd508a11c4986 in / 
# Wed, 01 Mar 2023 04:11:19 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:11:23 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f4adb3bdd5c92354e9a5bbb61245c02e97a7f4cb20e49c20844defd9c5cf66ce`  
		Last Modified: Wed, 01 Mar 2023 04:16:25 GMT  
		Size: 55.0 MB (55045981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea8bf4fb12ed6deef654e7d2709cae829fc73669de550293e0fd7ec02ab12d4`  
		Last Modified: Wed, 01 Mar 2023 04:16:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:258ca5d9301dae8847c46c645edfbc083bc987d54411a44599a737f9ff24e592
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52550083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f6bc019945173b3d5ecd9acfa97c8e6108fac84b6cf842130c8232d65bdf06`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:49:16 GMT
ADD file:bad8a3eb985558e32de17b6b7121afc340470d655c3b08489a077f98053cc37f in / 
# Wed, 01 Mar 2023 01:49:16 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:49:20 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:54c6387de315154f0c06420043cbd076f0c142eac6eda8dd70a4d02085792016`  
		Last Modified: Wed, 01 Mar 2023 01:53:54 GMT  
		Size: 52.5 MB (52549861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648dc579297df79872055021b611256fd3578914f40cb6f6559c989cb05edbc8`  
		Last Modified: Wed, 01 Mar 2023 01:54:05 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:21a3334fcfc5de15f3f8d447869015a287d7cf6b95e2e764df07684957842d87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50212260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dedae90b3626ea168959f524d1745db6347f1dbbf1a3a563edb6996734e581`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:58:53 GMT
ADD file:0bbb7a30608fd2703237856965ffd2844f6b30d88b0c6f59e29ce3cd307724bd in / 
# Wed, 01 Mar 2023 01:58:53 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:58:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0ad252180deb3803ff4fa886cc353753ff347b34e8bfcdd293dbf3e459e00d47`  
		Last Modified: Wed, 01 Mar 2023 02:05:25 GMT  
		Size: 50.2 MB (50212037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afffd1eb52dfcd8d0752869842e37a3eec357b79462a5ff91ae6c9439477cf21`  
		Last Modified: Wed, 01 Mar 2023 02:05:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:774466fb884912cba350c337f610eecc2274db937202d199d87da0441aca84fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53703435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f13719347a0a556f9e952aaf9ce2a3fbd114e4b5e974eb2fbedfa346551546`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:21:34 GMT
ADD file:aaa99e7de5941a1db01329990cb6b6e62192df6a742770321dd9e32f99f1a3ad in / 
# Wed, 01 Mar 2023 02:21:34 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:21:38 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3526e920d13f30b8e15703eb886a2f880388bca9c4e695f3f0aee1faaf8326a5`  
		Last Modified: Wed, 01 Mar 2023 02:26:12 GMT  
		Size: 53.7 MB (53703213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a35681479f355166d9f7efd9d94e3a72e5e5bfa9755810060b22f0a1921f26`  
		Last Modified: Wed, 01 Mar 2023 02:26:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:884fc3a61a8aed9bcac4f7517340dcc0acd6da93723db8859dd23d3c57ee6c4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56028288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71529efc66d7ed73edad707b8fc6b56ed4a7da5a18fe9ef46d77946dc3aed96f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:40:22 GMT
ADD file:737daa3f168882138edb625c83ff9e8170eca878410c7f13b49e886473eabbae in / 
# Wed, 01 Mar 2023 01:40:23 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 01:40:27 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7ee655a77adad1d23ab429e0247a2216accee870f111810a4276c60e43dd46f3`  
		Last Modified: Wed, 01 Mar 2023 01:47:18 GMT  
		Size: 56.0 MB (56028063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f106d0186b576e07adeabd3c20d20a83fda44cce93c65c3bd73961919694223`  
		Last Modified: Wed, 01 Mar 2023 01:47:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:ce0c024eddce8bc6b7665809bd5b37e5c0f3ad2b60d09bc7fdf9c0dba4b8c307
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53265359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a217b35f825783e2e9c9b60e52a0695692975af5daa78b5f667f979b0cc17d5f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:12:31 GMT
ADD file:292d4f2b6a8c55cc444ae52ea2812d03ff2cb0364b433d839cf6eaed1ef271b5 in / 
# Wed, 01 Mar 2023 02:12:36 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:12:48 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b309c4036eed767322c90d4ba6830bf2e6f25df909b4b9309ce8f0b85efc718c`  
		Last Modified: Wed, 01 Mar 2023 02:20:40 GMT  
		Size: 53.3 MB (53265133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084316f8e187ec49e91333fe55b597a5b4d01a7e24b3c4a5131cd738ada5948b`  
		Last Modified: Wed, 01 Mar 2023 02:20:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:10f7cd17f83bf858c1c80d3e51e79bb62f231556bc6333e90ecd779a2602e5b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58921498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7774771f4d5cc2e4dc705a45b01baa919e8c06b58dda52b443ff190822f311`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 04:48:33 GMT
ADD file:6e66d6df3e12f245e1d02beb5f0f838b9e40f5ccd5cdcb4f6c5e3a9461f2a3f5 in / 
# Wed, 01 Mar 2023 04:48:37 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:48:46 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d2e550d2bbbbe1ef1a174ed14bdebf17a9a5e786b62dce6f59cef72731bb0045`  
		Last Modified: Wed, 01 Mar 2023 04:55:12 GMT  
		Size: 58.9 MB (58921275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b6d54ebb9025f13a38cd8d6797c99a842dd5bf07976dc6f28550abfed59bfe`  
		Last Modified: Wed, 01 Mar 2023 04:55:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:02291a04725fb469e6fa44d17d26fc7b3a23cc89aee3a7848207cafe47bda505
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53277880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e526bc39bc568a3216a96d0878b64c5fd0b8a514a0e917fa4205ae6cb4c31b42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:51:09 GMT
ADD file:6be46c69515fd486f32dbdeba5f6f35471edf2e9880beeac32c8c8c2cebec956 in / 
# Wed, 01 Mar 2023 02:51:12 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:51:18 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9e589b9595471bedcb4024d4e655af7af462cfd4c5eb57cce7fcf83848664816`  
		Last Modified: Wed, 01 Mar 2023 02:55:27 GMT  
		Size: 53.3 MB (53277658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8afa3d0e6044b28df884722568b372a1de1e52efead4c234271ccc15afd36e3`  
		Last Modified: Wed, 01 Mar 2023 02:55:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
