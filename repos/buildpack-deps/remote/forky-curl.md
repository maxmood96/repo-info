## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:aaf951e511bf636dc67e2024c3ac42d168ac9f286c73384314d65989883516a2
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

### `buildpack-deps:forky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:42a22e0d7e15f304ec93ac2c59b860f18776dbd136011703ce120a0e5e0c6644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75673590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d6e9df6b700d83a23d66dc1ea67a4a1aedc8405559ee1e5e3a0caf3fe36f87`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e466ee06eaaf7587bf550c70a7fcd7231602b28fa903e3a172b66d9ef28299d4`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 48.6 MB (48625091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2544a38ddd1390105762bdf349d1e32b7cf1a9f82dddf930c31b8042b03c6965`  
		Last Modified: Mon, 16 Mar 2026 22:37:58 GMT  
		Size: 27.0 MB (27048499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d40517680ebc3525e1c18f155e719891a7a59995ccac5e12b7b2e10e9803ab13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4082007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632dd37d9c59762be87ec12b21a5682f4d2afe3cd538bcdfd3e68e27bdb5454a`

```dockerfile
```

-	Layers:
	-	`sha256:a5a0f1d8b6b795d78325dbfa67c32336e3935ee54ae0ece15992b33a87f71fff`  
		Last Modified: Mon, 16 Mar 2026 22:37:58 GMT  
		Size: 4.1 MB (4075236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d4c7a26a062cce8673a32b58edc9f8e8264c88b895ed4c26948d1be4b44571b`  
		Last Modified: Mon, 16 Mar 2026 22:37:58 GMT  
		Size: 6.8 KB (6771 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:87cd5a454968b0dac37f3afc005e5f8c7380c15ef5f8885095cf571a2a2df08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70573408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7682e44ef7c43f8adbdf2e76608e6504f2de19c91efec3e11937199ff6ea96dc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 20:04:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b74010850dba4ef4e0d65d4c6bda126a2de154bff6afcac42cad46a2cbe16fc5`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 45.7 MB (45653048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e2692d078b62360ce66efa48798cce1ada6ffaf0e61c3560fb4e15c2ba9d74`  
		Last Modified: Tue, 24 Feb 2026 20:04:20 GMT  
		Size: 24.9 MB (24920360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8db3c1b402fe118464c0a88a37b181abe079a26f80fe8b864eebac8ab3097370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4135114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c7a934ace96a9f2ac081b048ae570e34acc8193ab4186589d985ca288f4f14`

```dockerfile
```

-	Layers:
	-	`sha256:5a51e874ebc37b9f93233c040a8a53d65d20c2cc3044e05359d17f0fff1b6724`  
		Last Modified: Tue, 24 Feb 2026 20:04:20 GMT  
		Size: 4.1 MB (4128277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f78b35b631bf6b8ef395f600a251feba69a5b1ea83ff70f025c2840fe700678c`  
		Last Modified: Tue, 24 Feb 2026 20:04:20 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:db73609e03c4454f1c75f3d0b1e87d21f277c2d9fa9761307f27ec978255e146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75003649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad1e097203b7e6bb7b436827b48db9dffd243176e51ed7d2dae4e85a1f09e45`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d2254738b23b1e05d3619d906c6e8a67a96280536a5a742eb7d517f2cb33ea0f`  
		Last Modified: Mon, 16 Mar 2026 21:52:20 GMT  
		Size: 48.7 MB (48659061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873916964a227a18ebb04ec1f407f168a33886e300682cbd4848c61bc623f448`  
		Last Modified: Mon, 16 Mar 2026 22:40:19 GMT  
		Size: 26.3 MB (26344588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4fbe20e198c509dc3ae2950d2334dfe583fb852137629bd2a3d506112c91b59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275fa216ab048d7cf2530b0911a65325a7699f78585bf380e1043e81786173c8`

```dockerfile
```

-	Layers:
	-	`sha256:23cdf2792776b8cc1779d0c79c76d80d8e5cbbb6d3545823b532e6333d26459a`  
		Last Modified: Mon, 16 Mar 2026 22:40:18 GMT  
		Size: 4.1 MB (4082692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ada82aa35df6dc3707de9d75a5943ef642f9f0673c506b23278096fa6fcdaf8`  
		Last Modified: Mon, 16 Mar 2026 22:40:18 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9d3fc496d7828b648009589771776854dc88ab6ee1afb2865efb75b640b95d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78230283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8832ec330e80e68084228ccacb4f7299caa9922ca9473ecc9a7edbd71f8b109c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:44:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7e69024476cee0d949af8f266c3d1bb8032a19b46d27960e72964c7d5d99edae`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.9 MB (49919871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63597877e9ce45a8d644c87f2edaa1b6f60b392c0f8a5049196e27710801057`  
		Last Modified: Mon, 16 Mar 2026 22:44:13 GMT  
		Size: 28.3 MB (28310412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8d618b29f6693119cd858d62415fcca5c9abeb56814459e74a25225b1de9d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4079094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabaebb77814f1145520553e0ff100e784830bdada3ea88a7441aad12334b402`

```dockerfile
```

-	Layers:
	-	`sha256:8523515d067a17d6f1e0ebd113e91f28ade49b39788b242aa452c5f6ddf3a2ab`  
		Last Modified: Mon, 16 Mar 2026 22:44:12 GMT  
		Size: 4.1 MB (4072343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827a48fdfd5e27133c8d4f828e68da5a3fdf88519b39565f5f49bc4350069296`  
		Last Modified: Mon, 16 Mar 2026 22:44:12 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ce728342f63f98879feb15fc1ff489b4b9b8c38ec991020b8911c455028d69b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83155720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42191009ad1771f513122370eec45538980134644c627fb7a0fb030c3b9d62c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 21:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f1e7241652efbb83270036a6221c3c25c51e9feb8307ee3c94f7e0d52832e1af`  
		Last Modified: Tue, 24 Feb 2026 18:42:31 GMT  
		Size: 53.6 MB (53641787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa31de94cb423730059f9604b4ef3f6954ef0ad086f5d48144efd62317b2c2e`  
		Last Modified: Tue, 24 Feb 2026 21:20:56 GMT  
		Size: 29.5 MB (29513933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8e416f7529f981ebd4b589eb065c0fda8a006af810df8e9107678d2323be0c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990c15c58c7cc83b1e76609c75229889b352637f81f8e6278e97c0472388947f`

```dockerfile
```

-	Layers:
	-	`sha256:a56dbe4b184c0099498e40e5b379e19ff6537cdf8201acab5c161807d3ead181`  
		Last Modified: Tue, 24 Feb 2026 21:20:55 GMT  
		Size: 4.1 MB (4130660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eded74d17adcedb2f7a5e2d5bba897e9c67520d9679003348a0b2c76f64be5ce`  
		Last Modified: Tue, 24 Feb 2026 21:20:55 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:975d9381587ce6aea81d26de04bbb50a01d26e1adbe437e89e6cf01e358cd0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73320869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05038bf99ae775d947eb35f3d5a4f21e3ae5ec9bd4dad1214c5770f3e7b2d6a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:27:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c3fb5c15cbddc0ebbd7afd8ce992f6bfd6f0d5d4b1d5f4e672c5fc7451f1119d`  
		Last Modified: Mon, 16 Mar 2026 21:55:37 GMT  
		Size: 46.7 MB (46721467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059cd42e31b5d0cd1848f67940ca871c5e491654382eb483e7231a6e0aedfb85`  
		Last Modified: Mon, 16 Mar 2026 22:28:45 GMT  
		Size: 26.6 MB (26599402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd807e7bda091ea2ef64187193526d724e60676788a71179d0028b33ea0e37f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4073738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd81c6cac2e374f106f47bf5d5e3a97ad18fea81b38fefab76caabf6d8260cc5`

```dockerfile
```

-	Layers:
	-	`sha256:ffecca908a353bdaa03405b042d507080b131b4b4376a7b34a0c26c5b5cfbc98`  
		Last Modified: Mon, 16 Mar 2026 22:28:42 GMT  
		Size: 4.1 MB (4066934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b8dfbf0d9c3de45f54648517ff279f8e0f690fa91dfa562fe7a99b7beb3f5ac`  
		Last Modified: Mon, 16 Mar 2026 22:28:41 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:da431ee75ff98f2276497d62620a13ba7393d7ae5f28b312aa15f1e59a04f8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75453605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbc4d851cbca8d9358761f181eafd285aaf3735a622f1d271e3de9abe3d74c0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 20:57:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f21354992e07f04a7de86938f41ff3c72cb8dc33252e2b2320b4169695270de1`  
		Last Modified: Tue, 24 Feb 2026 18:41:36 GMT  
		Size: 48.4 MB (48448352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bc3d23a1ad94963e56617c5ddcf27c1a360185386d60459632a29eefc99c91`  
		Last Modified: Tue, 24 Feb 2026 20:58:20 GMT  
		Size: 27.0 MB (27005253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb4e89aacfc1285e19664c99a7624684e2608a4fdee1bafb27d7abc30916e737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e87a4ddc001799a81a6ffb52bb3e8f233939ba3ee77b5f36d912933b9a9ff6`

```dockerfile
```

-	Layers:
	-	`sha256:8e429e8614aceb56fccb4259f0c93be7d65eed2738d7cedf4ba22b1f89cac8af`  
		Last Modified: Tue, 24 Feb 2026 20:58:19 GMT  
		Size: 4.1 MB (4128190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667e37bbd35f3ddba5c875e6faf2861ffdd901a60126fc43649d3d5d71aa2672`  
		Last Modified: Tue, 24 Feb 2026 20:58:19 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
