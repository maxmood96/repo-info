## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:9f3058004e1ac3935bbbe6d3651d0b849aa79158d2bfc3ce65e7949a6aaa6ffd
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:9af5b53b6f5524d8940f34d785b4c139f17009ce04152c63c7cfacbce824b0ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52983836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f20a0bf770ed055921cb80566f987e2b44171da90a662aab932cad3755168d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:55:59 GMT
ADD file:3b3b943815afcac58f0e8a49af9b3ab289e32cdd69d4c6bb0c64665439c8619d in / 
# Tue, 13 Sep 2022 00:56:00 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:56:03 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:97357bf36a88b062ffcf42d1d32358484d7f104afddf68a27fc780d5e4b35747`  
		Last Modified: Tue, 13 Sep 2022 00:59:24 GMT  
		Size: 53.0 MB (52983612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b8c76f392ce2428816319f1a73aac900a2f46825c08e9957c1a1ac3e9584c0`  
		Last Modified: Tue, 13 Sep 2022 00:59:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:452fb96912ae9d536ffceba237d340fdb6df659d945b8c9f45782bb824fba381
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52122766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c5f9813646fb6f77f6a1100dd2c6d3266fa13ad6c88981864bfa720ccfff59`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:52:16 GMT
ADD file:fafc9bc142e136ee85605d8e97e30de6b77737818f595795657169b6296c2106 in / 
# Tue, 13 Sep 2022 00:52:16 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:52:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7ac1aef77561a09b4a507bdfee90352851c4c589691168642e1962feeb17f470`  
		Last Modified: Tue, 13 Sep 2022 00:59:23 GMT  
		Size: 52.1 MB (52122539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd577085d4fc2867ef390534184ca3693f7977930392b8a5a3563035d93670a8`  
		Last Modified: Tue, 13 Sep 2022 00:59:37 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:54a6594a3baacd726200d9de8db31a41628a531d4bccb06439530bc4e1be1247
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49856375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa1f0af8dff44662ec27c50258df5a84ed9cf467024914af408cb752cd5e250`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 03:41:41 GMT
ADD file:08a45295cc01bc25ae6c0bee004d66cebbd39b1063d32645343bea01d625c89b in / 
# Tue, 13 Sep 2022 03:41:41 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:41:48 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0fe4907198754eba3e4eb94a429c1d51a16b13e54532966f7e63095561ccc26e`  
		Last Modified: Tue, 13 Sep 2022 03:48:21 GMT  
		Size: 49.9 MB (49856149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2d2ecdeb663978d75388f7dea74c0a8138dac06ec910751f23503229ca16fe`  
		Last Modified: Tue, 13 Sep 2022 03:48:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a0b53698d358cfda962991db3c6c694bb087629e13cf3d7e0e8460ce7f215610
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53446094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c684d3346140bab11dd0985c0f613e1ec52736a353b20b7aa7cf07186f252f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:16 GMT
ADD file:eeca8a92b00b852cd39f0abd34d39f9d03f4559200a531fc30b095517809ccae in / 
# Tue, 13 Sep 2022 02:10:18 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 02:10:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fe69ceee3eeb1b19bdce7ce202b8955dd4b3a0d59f4585e141d537a96e025cca`  
		Last Modified: Tue, 13 Sep 2022 02:15:09 GMT  
		Size: 53.4 MB (53445867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb4de200fa6d2f4487f3585b099257941f7322eaf3fdb1fb06f913b6d09cb48`  
		Last Modified: Tue, 13 Sep 2022 02:15:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:16cbdf63ade6bd95872a4f09cfd8d877b8c09545f7202d406b65e701a1f544fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54342119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3805316d592e4753db8316f5bd6895e4aab6bf309d67ff31cfcaaf88e1988d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:02 GMT
ADD file:017ab146b2bdfc1a02848a9c381369cfc30fdf39ab4fe2050ddecd000ae22219 in / 
# Tue, 13 Sep 2022 01:39:03 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:39:09 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e4789d73ea79dddf7755bc7b1a512d5c038ace080bd9396a1ad89a757d1273fc`  
		Last Modified: Tue, 13 Sep 2022 01:44:11 GMT  
		Size: 54.3 MB (54341895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657f6c4694ad7fc17b6aa86e87d39f9f2f6b9a7d98afa85f9657bf1100e3dc79`  
		Last Modified: Tue, 13 Sep 2022 01:44:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:0767f4f67ef4b5943379f4695010d3482300d46755973b04e2f97f31e9d5cbbf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53424532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4c38821923a99e3d51b6be45fad53a5ee003b48ecb3d1bd966439e3cc36299`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 01:09:11 GMT
ADD file:3491a858e0f5d7985f9d29ad3567a39b0271d5794db146892787053625c3b44c in / 
# Tue, 13 Sep 2022 01:09:16 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 01:09:31 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b94700b51ec501e09ccd1e3b3962175f6110497a6ce43a01932cb0ca2718f356`  
		Last Modified: Tue, 13 Sep 2022 01:16:48 GMT  
		Size: 53.4 MB (53424305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3348c0064247c99e99d9e9878c21e4894c6a392486934c659c28b1269dc0d5`  
		Last Modified: Tue, 13 Sep 2022 01:16:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:eee126b473bc0b3c41fc8b0d069e4941103ac2c4ad178725fdbe87b3dac17189
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57546101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa079ad2f698dc0936b369127920539c6d39b4977eeeb508e78e47ebf7f5166c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 02:06:57 GMT
ADD file:953c3e24c2166fd8c69fa244bfdab95a8235a25af714160bc89f208a156d37a4 in / 
# Tue, 13 Sep 2022 02:06:59 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 02:07:05 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b7c4a0b69d3e0c34047cf77031a6316bf181afd76639e65cfc6f654271ea6f10`  
		Last Modified: Tue, 13 Sep 2022 02:12:09 GMT  
		Size: 57.5 MB (57545876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5099730f8925a9c33d0bed4297741c6a8c913921892e36225dd1f6be7dd3594a`  
		Last Modified: Tue, 13 Sep 2022 02:12:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:a2c63f586d8bf640ce02fc71973543b7a62eb43762d70c0d479206409d5319e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51793961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c05a821067f2f9f5194546712b8cd36b35457bec95f605406057b79ee1e2bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Sep 2022 00:47:18 GMT
ADD file:b7771dfd52d59914f02d6a960a15a002d38a4ce20bcf17ccc9e77d105dcc970f in / 
# Tue, 13 Sep 2022 00:47:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 00:47:27 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7aeb98a659275cb80ecf5c5010e17e1f9dbaeb66dc78b0b9547e7d2cef3ccbed`  
		Last Modified: Tue, 13 Sep 2022 00:51:49 GMT  
		Size: 51.8 MB (51793736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9947cfdd569edb2e6807c07964af3f63cdd2f0706430ed865c2d5898145e10bc`  
		Last Modified: Tue, 13 Sep 2022 00:51:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
