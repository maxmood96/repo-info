## `debian:experimental-20241111`

```console
$ docker pull debian@sha256:423208c9a7d0f2b8a113d1af3a53f451e5b5d070646671e3c7b69b4eff67026a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:experimental-20241111` - linux; amd64

```console
$ docker pull debian@sha256:86c30d6a83b0efa0083f13e33755baebaf85eab939273837cc4e85985a835357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53319668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af992bd5f57f2d212bc311764b3f19fbb83ec530bbe6206b3f068bad11e8ab4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:2f80ddb01eaf779b94e89eab305fce369f582614a3e5ee6aeb78e8c3534f9f41`  
		Last Modified: Tue, 12 Nov 2024 00:55:18 GMT  
		Size: 53.3 MB (53319447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bca7fbfe17f311d6b4d15d2973e7755112531e12a314056c9731eca4d548572`  
		Last Modified: Tue, 12 Nov 2024 02:01:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20241111` - unknown; unknown

```console
$ docker pull debian@sha256:9bd6a207b7b4ef58fa4631ac2582aa9efb7df22a19bcb49d0a526ee3dbca5424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3255263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac29de8b6c555e7ba4ee54904f90610eeef1036cb352bf2bcd3ce64e341dc8b6`

```dockerfile
```

-	Layers:
	-	`sha256:f17a519186db56d3b2e90503cec1ac592fe42849a47c7f58d78f0f0038e71e8e`  
		Last Modified: Tue, 12 Nov 2024 02:01:54 GMT  
		Size: 3.2 MB (3249119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d01c24a17c0ef58ead7c148099d5e1866bc7b1a8962f4bce0b08884948a32caa`  
		Last Modified: Tue, 12 Nov 2024 02:01:54 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20241111` - linux; arm variant v5

```console
$ docker pull debian@sha256:ee5e1501a8f900f228b288e31de0143e3d7c12acd0197937e2799680c867c801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50178529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7277d3509f01859bc9da009b5607d806e3258205302b0c53d74f2d61376c1889`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:97fe43a529c2fc75cfd34bd7a10f0d86c2940d24c66b40a35db185fd2ed321f5`  
		Last Modified: Tue, 12 Nov 2024 01:00:02 GMT  
		Size: 50.2 MB (50178308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60a34c304edf09cdb95a0fc19428a69a60e57485c25096d37e2854b0b737a29`  
		Last Modified: Tue, 12 Nov 2024 02:02:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20241111` - unknown; unknown

```console
$ docker pull debian@sha256:07b6f42fdac9f63128c82f66e14c50b37323ad59f5383ade1efcfcf174d4264c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3258153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67f5d59e750f6d733997ccca89f9581f0007c958596c18ed4093435261bd312`

```dockerfile
```

-	Layers:
	-	`sha256:3755094e0689e83051ce8506cd06ddde74600fbfd7ee87fd7d7704045c359c7f`  
		Last Modified: Tue, 12 Nov 2024 02:02:53 GMT  
		Size: 3.3 MB (3251949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e21daa621a4274a63f9a1c80503260ad1334a9aaa85d25618eabc639a9c6c7c`  
		Last Modified: Tue, 12 Nov 2024 02:02:53 GMT  
		Size: 6.2 KB (6204 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20241111` - linux; arm variant v7

```console
$ docker pull debian@sha256:5bb2e1ea2ad2757e416106212699eb40f366f0a8d2aa25a96cd7a8cb1fd31a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47763082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832befbc5359ef779cf534205713bf63356a547db877147be96a321b8ef8ec97`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:e74ca0e5eebbb633d484df0a8dad86c29c902e188f7b0ce8d7d529e4d881ce67`  
		Last Modified: Tue, 12 Nov 2024 01:03:49 GMT  
		Size: 47.8 MB (47762861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7ab44e40e90872591ee9edc77aa657f98cca1ba4d051a6841a4fdaea6f3a77`  
		Last Modified: Tue, 12 Nov 2024 02:22:23 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20241111` - unknown; unknown

```console
$ docker pull debian@sha256:cef563a338b4bb6c33d221b92cb59cf79467e3c65224fcf531b8623b2e684d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3256889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6ccb03f5d2121a57f832b625ef633b3fb10f595e5083c4e858d4e60a29743b`

```dockerfile
```

-	Layers:
	-	`sha256:ce75c78b002ab2ecba0da718ec20adebf5430821df3cd5c5c7a43ae2a9512606`  
		Last Modified: Tue, 12 Nov 2024 02:22:24 GMT  
		Size: 3.3 MB (3250685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98faa698150cef12aef85cad90efc216280f7a525ec0e2ce928e26f858246b59`  
		Last Modified: Tue, 12 Nov 2024 02:22:23 GMT  
		Size: 6.2 KB (6204 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20241111` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8a07d22fc42467f6ed7f5742076819cd90e8a0357cd2744354c9e11bde1fe61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53759971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2277967fda828efe6f90442edfc390cb47194cb178f72d50d99f2b94023e1982`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:04654b29097554dc2e8bf1682dbe241275b2956d56d2a74a0b67cc2d887a4e49`  
		Last Modified: Tue, 12 Nov 2024 01:04:21 GMT  
		Size: 53.8 MB (53759750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b547b830a37317f71b5dcf45728cc0cec08a10075c37d33f3ffb3893cf6e59`  
		Last Modified: Tue, 12 Nov 2024 02:24:24 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20241111` - unknown; unknown

```console
$ docker pull debian@sha256:10994359a2c1213186055cfcb576d0020c8ca5ef839e6885ba0261f3621d6bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3260845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2eec83b4e0d77bc615a71980e3c62294ad17e081b4ac26b541e5f512f4d0d3`

```dockerfile
```

-	Layers:
	-	`sha256:d3f05aab84730cb4e944eb5490e10f53a2b20547df6d59757b425440d3d3d748`  
		Last Modified: Tue, 12 Nov 2024 02:24:24 GMT  
		Size: 3.3 MB (3254622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be32220321f3701929eae66b1ab4f6be1f9a936bbeace66e8aa294c0c4acec54`  
		Last Modified: Tue, 12 Nov 2024 02:24:24 GMT  
		Size: 6.2 KB (6223 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20241111` - linux; 386

```console
$ docker pull debian@sha256:00e9ade893be2bc71be174f1d3cc5bbad9d0c2828adc14a1498e5576078b908b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54192270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7dfbffdc4cc0afcd7643f477f7a321e0f9c6ae57d013c1ef049fca83a6c5a11`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:076bcafb9bbb1cd5a8a6b272b37b18561b6f4cfbb161482c7ebebce28baf32e5`  
		Last Modified: Tue, 12 Nov 2024 00:55:06 GMT  
		Size: 54.2 MB (54192049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bca7fbfe17f311d6b4d15d2973e7755112531e12a314056c9731eca4d548572`  
		Last Modified: Tue, 12 Nov 2024 02:01:54 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20241111` - unknown; unknown

```console
$ docker pull debian@sha256:17c404a9861d099fcc591e20103f4ff23f16dcd6feee04924473002f9798b9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3251713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4053f8f8680f4711ed87fb6e694a2c1a9af71a365a933c8f6cbeb35ab15c6af`

```dockerfile
```

-	Layers:
	-	`sha256:5b9a77d473c101adac536fcb6e0171bc93662578bbc9dc86d0e616bea846caf8`  
		Last Modified: Tue, 12 Nov 2024 02:01:54 GMT  
		Size: 3.2 MB (3245592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aaf6e82d80ba9b092751737daf959a1fa6fbbbd8aed28cf7e0b2efce1f7b6ea`  
		Last Modified: Tue, 12 Nov 2024 02:01:53 GMT  
		Size: 6.1 KB (6121 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20241111` - linux; mips64le

```console
$ docker pull debian@sha256:e29f4febb29c4beda0030aa4dcee1633595e6f52b901cc72d0778f76a43dec20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52275458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85d1ee888e4636ca955366c2ed52763ea8203ec9bd718ad85050597b787df46`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:059babba596f27a6123bd6de0a6663fed702e5345af41d218d46c6954e976c88`  
		Last Modified: Tue, 12 Nov 2024 01:10:49 GMT  
		Size: 52.3 MB (52275238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddefaf8b04a2331806d38a3a05077de8dab30b00a95e3ea9be69a307b19d8621`  
		Last Modified: Tue, 12 Nov 2024 02:05:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20241111` - unknown; unknown

```console
$ docker pull debian@sha256:6c0d16d1a8a3e45ed4dd1b6fa9b817913864314306a15ffbb59c82b2c02a25e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 KB (5977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6553869bb9db94ae3431f031a526b608bd4fa777c03267783e030de1be7444ec`

```dockerfile
```

-	Layers:
	-	`sha256:c835687008edd61a39dacd42df735639b3a8ad67fad1dbd604a0c24ea2c8f5a8`  
		Last Modified: Tue, 12 Nov 2024 02:05:21 GMT  
		Size: 6.0 KB (5977 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20241111` - linux; ppc64le

```console
$ docker pull debian@sha256:e6010cf4491fd763c533c4259a4a1931d826a1df9aa60b9db1c1fac138a26a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57309578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4cab0f45cbcd3661105486fbed9831391a274167207bf9a84cc96239c30030a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:199edab65b0119947e067796586796b400d93ee7a6235c36156c04f476f5d59b`  
		Last Modified: Tue, 12 Nov 2024 01:08:40 GMT  
		Size: 57.3 MB (57309358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4572c428ddc829e9bb5e35aa7cc55a0da14f21d34e3fb7624ee6d696fc28a31d`  
		Last Modified: Tue, 12 Nov 2024 02:25:51 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20241111` - unknown; unknown

```console
$ docker pull debian@sha256:9f6b3115e78d6213bc24fc16dc314d3450f796947c199ffbc9b7c2e31b1ee361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3258999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18483d3d5721cd8097545281898beee9ff343a976c89af0729ebd5e5f8577e58`

```dockerfile
```

-	Layers:
	-	`sha256:d921e22db2a7118dc05680febb7a1de981b3fc8662c28bbadbf0925d2a1cfafc`  
		Last Modified: Tue, 12 Nov 2024 02:25:52 GMT  
		Size: 3.3 MB (3252824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfa68e195a86293a01a2ef27aefafbfe8a649edaceb69df069c86b93d4e2588`  
		Last Modified: Tue, 12 Nov 2024 02:25:51 GMT  
		Size: 6.2 KB (6175 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20241111` - linux; riscv64

```console
$ docker pull debian@sha256:f8a898287a4d5e240c088876a2022ee653ab388623abfad46b7e81fc237245c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51741266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442792d75059158a594d6f794c0fad35380d51f92c01cb4f85408e86ea8b667e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:0011b7399911f3d20c606828ee651c30e6b18c77c9c1344290c0fac2e8696ce7`  
		Last Modified: Tue, 12 Nov 2024 01:12:10 GMT  
		Size: 51.7 MB (51741045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48db7155ebeab8089637295b2283011ea1efeb382c52a5c9a939f9f025e3cc1d`  
		Last Modified: Tue, 12 Nov 2024 03:45:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20241111` - unknown; unknown

```console
$ docker pull debian@sha256:7b011ba95d0d4f59f778f8821b4265162d4fcbc6486d6897a06397255b822bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3247891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68614b13bcadefdc920a6be7e32db2ca258cb1f7c884893b1158011246b5be96`

```dockerfile
```

-	Layers:
	-	`sha256:803861b83a14a07060d71c0f5d137e092d04418efbc4f07c191245a901e878b5`  
		Last Modified: Tue, 12 Nov 2024 03:45:43 GMT  
		Size: 3.2 MB (3241715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdeaa8edafd02d0c3533eb1108838ef66283aa35d3864d777f545fc252c75f8b`  
		Last Modified: Tue, 12 Nov 2024 03:45:42 GMT  
		Size: 6.2 KB (6176 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20241111` - linux; s390x

```console
$ docker pull debian@sha256:9308c908e88b4ea36c657ba5a23cfcb8a2ac81f617100a08753e8268c1f7f488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52981135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bceb9e5c7de89a12239f8f1417692ef5eb80f81e1e54f65279db1c359b0119`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:b39482106d170cd93ccc7819cd07b03fbcda5bdb4d8983e7bbdc0569f38f3bba`  
		Last Modified: Tue, 12 Nov 2024 01:07:42 GMT  
		Size: 53.0 MB (52980915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca27150cc394901f296ddd8eb5563958dddfac557ef87f65a4022f564d94f4b`  
		Last Modified: Tue, 12 Nov 2024 02:23:36 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20241111` - unknown; unknown

```console
$ docker pull debian@sha256:6f234830f7156596d2dd8f8eaa05ab282e579e15324c69467f55e082ef6a3324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3256859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb36d6efd031e677018352dbf7c916e84e85b403ad0163bb6d633905e11940b`

```dockerfile
```

-	Layers:
	-	`sha256:5f0f3bf9959fb68be4a93ae96d1603bc916441d1512c78b0807f5bde999433fd`  
		Last Modified: Tue, 12 Nov 2024 02:23:36 GMT  
		Size: 3.3 MB (3250715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84996a0db05de2441bc5ce0092988b3de34efae188c62e5c52bf9509152bff2`  
		Last Modified: Tue, 12 Nov 2024 02:23:36 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json
