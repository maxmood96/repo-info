## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:366815b1f7ae7711cd8ffc660393bb43b9823b0223017e77752447f4d2a9c17e
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
$ docker pull debian@sha256:9e982ede613a367e6816972bb2766958f6c22faeb6e8745dbfb9b21f677e5e7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52725954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5f8928b51a2beb12a753c93f9578b701960aad311ab843a6c211f9db3513de`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:20:15 GMT
ADD file:7507edfdf016128615e9ba278d471fd6d27c96436e543786b691c93b6f94b56b in / 
# Tue, 23 Aug 2022 00:20:16 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:20:23 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5e784af754e1c7855decd29b818520a98b5b539515cd7c199c5dbceb6cc4a45f`  
		Last Modified: Tue, 23 Aug 2022 00:23:57 GMT  
		Size: 52.7 MB (52725730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8871aedc79fdbf621dac8fffcceb6ffc9cbe584472ebda8a5266baa00737a93f`  
		Last Modified: Tue, 23 Aug 2022 00:24:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:ed0009214b2512c26802a7b20945e9e47ce44f558c5be33a0da6fec4977421c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51814269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd23827ca3cdfadc2ea4d33ad56b454fd1696c51a395c281fd9e475fbe5e460`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:16:08 GMT
ADD file:dbc0c48f409cbe73d340bec8639492807b8c28fa6907379a17a958448dca1829 in / 
# Tue, 23 Aug 2022 01:16:08 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:16:17 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3204f8dd2e8fdf47391628664d2c96551393e3e0abd1e471abeb57296519c816`  
		Last Modified: Tue, 23 Aug 2022 01:21:24 GMT  
		Size: 51.8 MB (51814042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8a2e7646711a3ad0206a166b9c5b1880aaa7d8e2a0a463de3ee83a5b4e5a5e`  
		Last Modified: Tue, 23 Aug 2022 01:21:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:bf883eab8c0ae068335982b699ba236d03dfc5a04e88a550bb5661f5396ed1c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49555317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa6d9c9222cf43f22e3e6d4ba26e6a22765f05e46d9b5a059e5505b46022ebb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:42:14 GMT
ADD file:590ff1916ed8a15a7a205153d20c2823a242c228573a1868134df4bdd95f10d8 in / 
# Tue, 23 Aug 2022 01:42:14 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:42:22 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b4a2cf95b2637a1520aeb527ca7569456a3bcf1d740f72cc418357cbe490704d`  
		Last Modified: Tue, 23 Aug 2022 01:48:45 GMT  
		Size: 49.6 MB (49555090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1915b01a40b5fa0a6d70fbbe851c9a3a6d79632d5880f4f6d4349d613c8b8294`  
		Last Modified: Tue, 23 Aug 2022 01:48:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:72794a193365f746305aa344eee1c275109b6662c7913441d09287d260e6df24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53117790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97820cba02c5a46bb226141ee8a37105f389599db6a8fe2a25e02c8f5e8db7d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:51:53 GMT
ADD file:f94a576f262c4fcf5112164145c04850c826787b299878e7e126754d1211a51c in / 
# Tue, 23 Aug 2022 01:51:53 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:51:59 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7dd208a8a7339c037c691e6ace1cd3f94803ee4c17a3211b9ccadf01d1ff2ca9`  
		Last Modified: Tue, 23 Aug 2022 01:56:50 GMT  
		Size: 53.1 MB (53117563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e50667678c3bc818bf4491880eca873f36d1eda574b45d21c34d25ebda6637`  
		Last Modified: Tue, 23 Aug 2022 01:57:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:ebf728c02291865c130d4d8e793f26242f107192f6e1a2462c3b278bb6742668
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54097163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a9e464985766d6cc435b152f3f46ae2250e7b2bbe87d78c9feff0c9f392dd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:01:59 GMT
ADD file:1c8ebe8b69a2d3c236c8a947162fab2e579f4bf01bff01695a3c46557f6c73f4 in / 
# Tue, 23 Aug 2022 01:02:00 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:02:06 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:29bf8f676853094720e43096224f2ec8a31ffa3752cf7a1e52fb9e72ae069480`  
		Last Modified: Tue, 23 Aug 2022 01:07:13 GMT  
		Size: 54.1 MB (54096938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a1f14bf6d32c514540083e07e1d8512a2532b49fd43d6efdfc4633ea932833`  
		Last Modified: Tue, 23 Aug 2022 01:07:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:88a92685f8588e036311c9e1396eb8658be3a205e1c3249a36e74613d6c5e663
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53119576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe2ac5ad32ed3e283a9692d8afa222a7d9366148c7a92dd71a4aad1dac1ffc7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:09:18 GMT
ADD file:2b4a878ee82590d9ee2da01a2501742d21f6d050a0002f9bd484a4d7c8620d2e in / 
# Tue, 23 Aug 2022 00:09:23 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:09:42 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4b18e364c6342ca1244071a2f94edf42b92a5b7997d16df3b26467139f3f0603`  
		Last Modified: Tue, 23 Aug 2022 00:17:33 GMT  
		Size: 53.1 MB (53119349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dd7949df62368fe8995f95aaefbb19714f16174623c9a7e62352db95b7d53f`  
		Last Modified: Tue, 23 Aug 2022 00:17:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:39a3cd3fb1cd9159584cae2feda4d2b63e6772eb80644b997f5fc881256bcbaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57290094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc160c48535921230dd425b13def27152d315f20b5dd3f982bbe278afcb6959`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:23:48 GMT
ADD file:92444ce23c3227ef88446469c37fc41decda1ba975ddfb1be3e1ebb1e694471b in / 
# Tue, 23 Aug 2022 01:23:51 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:24:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a2d2f2c5b4e64eabb8a7632609e67883239433d932129bf478f7614059a9aabe`  
		Last Modified: Tue, 23 Aug 2022 01:29:05 GMT  
		Size: 57.3 MB (57289866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860a9e529b4934b84efffa7e325339ec53cc8207eef318d7e3262eda4c87e3f6`  
		Last Modified: Tue, 23 Aug 2022 01:29:16 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:db5664f9503d207a6d916332383a1e3bd4764eceb3a233d1b18eb1550e523ead
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51559801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6cd220cb466e3007bdc14f2db3b80faf9388d93d58551ed990da7df12e98ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:53:14 GMT
ADD file:e8167229629003ac0dcc7f0bcc35a939121e9b4a88b67483883c2741f5415634 in / 
# Tue, 23 Aug 2022 00:53:16 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:53:23 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bfa0b60dda37e3a2f71f5d19d0259a51a84ce3f8e9deff107720c9868e69769b`  
		Last Modified: Tue, 23 Aug 2022 00:57:59 GMT  
		Size: 51.6 MB (51559576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02491bb90c78343ab3bddcc711d6016d48493fc43c589b0ed05068aa46525798`  
		Last Modified: Tue, 23 Aug 2022 00:59:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
