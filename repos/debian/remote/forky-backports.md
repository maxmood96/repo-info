## `debian:forky-backports`

```console
$ docker pull debian@sha256:e5c63df3127bcbefaedebd8be697dc47dba21d594540017aa273ba03a47ab776
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:d81e4787785bd3ee22127a4e46dfede9374b657d73bfc94244aab7f77beb2257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48830281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73773f097b92a0ffb2a864601742e844c2c21f086c6a2953b0913ca0ce7d8abf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:16:19 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e1869079ab5cc3b00301445717c112f3ddb9424b5d7b2a41713bc70d9482ee85`  
		Last Modified: Mon, 29 Dec 2025 22:28:05 GMT  
		Size: 48.8 MB (48830058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daddb154b4ed2d28b19d2fd4ff4cbee25d5f74b901cf27e41b22267ca7eca6ae`  
		Last Modified: Mon, 29 Dec 2025 23:16:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5166a016f5f21d137ab1db7165fe75153c4fee7763aced56a8232c0e73e3a70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea985a9c25cf998e2177b1ca74dbf82f09ab189e27fa46b308f7b4a7a1f89f2`

```dockerfile
```

-	Layers:
	-	`sha256:9c7ae08dc9175431c21a582904d07afdb6316eee72cc10023432eb6de01ccac1`  
		Last Modified: Tue, 30 Dec 2025 04:25:40 GMT  
		Size: 3.1 MB (3140078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731bdd016d56b05edb851caf5a1111f090b6f1a132c26af62046d159fe502fcd`  
		Last Modified: Tue, 30 Dec 2025 04:25:41 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d305a20313f3220a2ac7a2befa84c916e340cbb229dc70d30ed69339e6d7a74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45130029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87bdd44ae87dfd0db86ed95f01dbf7cc7b6f5dd8b878e4040a14af625c04e7da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:15:01 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:241c7878eb5bbc21e3d5116dd5ea31832b2d3bc7489b0d564310ab3bd542adee`  
		Last Modified: Mon, 29 Dec 2025 22:25:59 GMT  
		Size: 45.1 MB (45129806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d623ffaf33cd4b362eac4e0b25c23044e706ce83b024e94bab12c40de68d7d7`  
		Last Modified: Mon, 29 Dec 2025 23:15:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:02be48ab4ab979f2201e6a52742bb2dce077f4c7a815763a16f1540ad251f47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3147280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322dd4cc9958566d81d6ebc26ea6e3cf9152729ebcbc65b31f320b70d7c1c0cc`

```dockerfile
```

-	Layers:
	-	`sha256:42b3b9fa6f1d4fdeb7607d0aa3f5594ab43658caab32b38146c7f720886b65dd`  
		Last Modified: Tue, 30 Dec 2025 04:25:44 GMT  
		Size: 3.1 MB (3141446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d7455a0f0ff25b80e06ff9e38a703e6f095b416717f40d1dcbc184a7f922d6`  
		Last Modified: Tue, 30 Dec 2025 04:25:45 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:99f1bbc56cf0cf0346ef4a7331606fdeb1b48c5791cc14c7dc051cbe7402a30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48832215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27f841c30348e0e6b04d9f5994a580d521b27f8aaf55e66e183359aff21d799`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:14:29 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d6ed83950a3f675536ad8634cde3cf4c241d5faea11ae3192ff5909f826256f2`  
		Last Modified: Mon, 29 Dec 2025 22:27:42 GMT  
		Size: 48.8 MB (48831993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656ae667a94662e9bb9709a7f2b301d643f7b9e1d27ddcc4f4820e2fc4fca13d`  
		Last Modified: Mon, 29 Dec 2025 23:14:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7175d5d5baca4390aa1d6bd55c07bdf8875eda1e4c28cccfe100748934bce418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3759bffc4e59640a7f59a12b5e4f04a22f3a8ebf5d1dc6262dbf6639c881620c`

```dockerfile
```

-	Layers:
	-	`sha256:5b7d6199647a82e29988cad63d53d867d81b28b673de3e94939e2bdc03a1f0d9`  
		Last Modified: Tue, 30 Dec 2025 04:25:49 GMT  
		Size: 3.1 MB (3140919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0529993c930cb0286281d8bc3532934892f6b7ec5e31ce538ea96de803e9aa2c`  
		Last Modified: Tue, 30 Dec 2025 04:25:49 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:689c734123a7204a97359e0363744da68cd8042cc0f903d040ed6dd7b54a99a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49956058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c134d5f75180caacb14822c66cbeaea2bffc8559259bad44d0a7a54f4829af99`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:14:44 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a557815b7e39210fb0b4048ae58b1ffddbc8cf0f656a5974b6c3b24f7bdafed8`  
		Last Modified: Mon, 29 Dec 2025 22:25:28 GMT  
		Size: 50.0 MB (49955836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24961865928da32fe7ba75ba750980d8590ff0dc4b6386d14c0f4ba90bb2d249`  
		Last Modified: Mon, 29 Dec 2025 23:14:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:734ac2bbf49fdbe09928b73d06a93d672fe611aa33714c1040e78cb2cd98a984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3143040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8a5a9d962f56034bf51bdf12d84dc81370efa9cb4f9ef653aa10208d763381`

```dockerfile
```

-	Layers:
	-	`sha256:84fec8f76f2443dbc44488feec940f4604cf8972ad5212bb7c6e85a2cecf0d5d`  
		Last Modified: Tue, 30 Dec 2025 04:25:53 GMT  
		Size: 3.1 MB (3137282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff1ef11f62235811a9e613771c9fe23c2c7ecbb307c3729578ca4e0cd9a1f51b`  
		Last Modified: Tue, 30 Dec 2025 04:25:54 GMT  
		Size: 5.8 KB (5758 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:b4d4de8bf8c7069e8eb1252686021650699dd8bfa277525c098bb523b558a96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53414009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aeb2dfa02ed9cb4ff034918cbb99a04aee75a8ee70bb4a86cae0c2d3fa5c288`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:18:13 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ca6b6474de59c13edb40994c0579d1471aee6a7743baa1f84bd96cf0fbd414da`  
		Last Modified: Mon, 08 Dec 2025 22:50:05 GMT  
		Size: 53.4 MB (53413786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d156651c51eda18ac2220d6b39528866fc21e084b081c67837309622e8f2c2d8`  
		Last Modified: Mon, 08 Dec 2025 23:18:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a70ace3bca11cec69d083121c427d4f38133f765a16057065432c266083da119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3142904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c5688a3b95399ddda86ce68559c44c6ab6672869fdfa48988c8cb688a1a102`

```dockerfile
```

-	Layers:
	-	`sha256:aeaf153e4d942548729fbb4adcbb422005f1598caf828b27917b15b19232a12c`  
		Last Modified: Tue, 09 Dec 2025 01:27:30 GMT  
		Size: 3.1 MB (3137100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cc1eb8aa9fb87f53ae9bad34b0f76b5bbb55aa764260fec7f652ed3a6fa9440`  
		Last Modified: Tue, 09 Dec 2025 01:27:31 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:90cca7ea1266ba42e10a8daaf6839a327edbbc693a6de2a7ccca5fcfb5237645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46883720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:318efba530c229b06f3cee188ddfea975273c624ea17069bcdc5c0fe9c16c3bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 01:17:25 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fa050f4b17c5ceeeb0fa97b5cfc16570d13c816d216a6d728fdcd2ef48d6b8d2`  
		Last Modified: Tue, 30 Dec 2025 00:33:03 GMT  
		Size: 46.9 MB (46883497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dfd9b3301084a828f9307ddda420713a55da37d2a9bc0028d9ef805be0c254`  
		Last Modified: Tue, 30 Dec 2025 01:18:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8b57e0e14206641fdc5dc4826bd042d23acfcf61d5c6270dc65a786f453ab9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3137380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd52be131ce849b14fdbc256c1633a4d1f6aa4bbf9449d06af73572f63f77ae2`

```dockerfile
```

-	Layers:
	-	`sha256:581e70a5a1abcdd448cfbdfb44f1b9cd986f43b586a6ef31bb4b51eeedd99cd2`  
		Last Modified: Tue, 30 Dec 2025 01:18:19 GMT  
		Size: 3.1 MB (3131576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e50ee4fd08e606aebaa92b673169ad0b0b833164574aa699a86c002a1af952`  
		Last Modified: Tue, 30 Dec 2025 01:18:18 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:4e47dfde17e3bd99d9c850878612d0256358790c3f2dddc23bc3feb866bdaa43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48397777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b945b8fbbacfb4c3d1d25e96cb7ab6da2b95bff4aaa8b922172ac6e86baaf13d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 03:22:23 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4ed754f864448d0e594994dc11148ccb02da6ea309851c997288e88ce4fa4e08`  
		Last Modified: Tue, 30 Dec 2025 02:08:24 GMT  
		Size: 48.4 MB (48397553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6a0883c59aef5840e9623de88f15f8aa68386c1b5fffd402be146e00dbbc62`  
		Last Modified: Tue, 30 Dec 2025 03:22:40 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:607cce8699f8944d0d5b9026dd08e635ad8400a2633e9a34254da62913f8123d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3147305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e07c6aebb852ddd5d391b41d403d51310b21f8f4bdf08aa2e88673966185c72`

```dockerfile
```

-	Layers:
	-	`sha256:3b13032992c11acef82713e79c02c3aec88b570ad59a333783042dde94172659`  
		Last Modified: Tue, 30 Dec 2025 03:22:36 GMT  
		Size: 3.1 MB (3141527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e588a86a8a993c06103f39e4341cfe1dc329658e44be4fbf6995fc72fb33171`  
		Last Modified: Tue, 30 Dec 2025 03:22:36 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
