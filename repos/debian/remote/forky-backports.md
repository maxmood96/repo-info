## `debian:forky-backports`

```console
$ docker pull debian@sha256:1f337c5be14d9ce1e7665bda96b1a45bae907e736943aac6db149a537ed130ce
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
$ docker pull debian@sha256:f111407cd608e9795fcad581eb9b3451a6396530a4a646f3cfbff613aa13fc5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48512733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df13c181547c5003468cf977907b6450a4f9787d0cd7661821befd400b51bd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 22:30:37 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c7cbbee3050ecd826301596e459f3fa12ca32f5ba2b65d33b56172341d2cd3ff`  
		Last Modified: Mon, 08 Dec 2025 22:17:14 GMT  
		Size: 48.5 MB (48512511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb65f218c184abb0b8712301d5cca83ed171ddba4fd91fd25bacb3b15505600`  
		Last Modified: Mon, 08 Dec 2025 22:30:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b79d043e94008901427c3c0c2765064ffd2ccb6cad080f0e99a81a1256e5b062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03069414f320443538175e68c4a25246d3539bde8ed0e88faf1317a5e3ed83b2`

```dockerfile
```

-	Layers:
	-	`sha256:fa65f7a539bdf0b53d196dfddd385fa77340a00aef25a77ae46530a08bc36e6b`  
		Last Modified: Tue, 09 Dec 2025 01:27:08 GMT  
		Size: 3.1 MB (3133601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1beece1bec4648db029b0f74decca932e5e335aed65d49c532466d4b508949b`  
		Last Modified: Tue, 09 Dec 2025 01:27:09 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:c79cc0234ceb638e43602f0c4005ae91c162adff121ca3db37316b99ecb96fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45048265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a8f856d107db810b4e90fa290570ea8e865ed12ead00443f54db2275c1281f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 22:31:09 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:97c0e703f22fcbdd1717c90c9c81bde96e65c1c3051ad73d18fbc908c8b17e4d`  
		Last Modified: Mon, 08 Dec 2025 22:15:47 GMT  
		Size: 45.0 MB (45048041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec00adbfe798f60356ffe43c1b6a5b10c3f71ca87df9b6cf9eee292a2d65604e`  
		Last Modified: Mon, 08 Dec 2025 22:31:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:92db31551e0cc7113b622036e723cd03eb08e025e9d6e19c4c38e286e467371b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3d1d56f160d2ae001d4357ae12486943190ceeae18aca10ecacec4022846d4`

```dockerfile
```

-	Layers:
	-	`sha256:95932806c552175279096e5d44d6ac01484684814e9c532e987bf27cd3dcf517`  
		Last Modified: Tue, 09 Dec 2025 01:27:13 GMT  
		Size: 3.1 MB (3134969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:259a74646b46b8aab3a83db1d8a39d2959268b32e046caeaf83464b1a38617ab`  
		Last Modified: Tue, 09 Dec 2025 01:27:14 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a66053fdc072986c2efe37f3ca02196d65e176c8d87bfec586a0ee6eaa137414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48599559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b998a13423259adf717cf035a8d220e4ed364ca01a7686954a0ca1275573a10b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 22:31:12 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:60db063fe1f6101cd454be84b0b672c499625ca27e05c40ddaf285db3af29997`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 48.6 MB (48599337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b566c37421bce7fb49979c0ef77729754e9bd9b0aa6ee05cd2ce33d81c51273`  
		Last Modified: Mon, 08 Dec 2025 22:31:31 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9548de39bee0189f025515200c87f5c4f494982c3a5e5b6a087debc430659d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d4ef83a12ee83a0a4d6daa405b0daf070cf5321230b21a08db68982a5bbec9`

```dockerfile
```

-	Layers:
	-	`sha256:ca6fbb447f0cbce47b350724c1a33800d8d92b3dcd9a529643ebb6b653ba30c0`  
		Last Modified: Tue, 09 Dec 2025 01:27:18 GMT  
		Size: 3.1 MB (3134442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4216638d69c8a93ef7db722066e67d14919f5599d85403ab1a3bd75587f90096`  
		Last Modified: Tue, 09 Dec 2025 01:27:19 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:fc9aa8aabbe7b4b6651742d5c116b2bc163de4fc865c8712cfb811656aae6ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49874802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bef16423a110548632da35d03e4a02823f554cb54576ecaeb7c471bb670803`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 22:29:17 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a5d3e60f8c1eac1ccb5aac1ab5735dd586fe448287d7c7d1d7f59a687bd9b9b1`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 49.9 MB (49874580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914896556992e5e4c6935931b781a7f99371d616eb86d6405b088dbb3629be1c`  
		Last Modified: Mon, 08 Dec 2025 22:29:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a2571b3b8de0cb32ecc7b01accd493092510ce3f6bb91f8aa40d5c942f6ac6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a470028d3e9013ae2f1e30eb581e5d937c5d3f283b601a7a6f3050f730afd9`

```dockerfile
```

-	Layers:
	-	`sha256:396e857bc45c34cdcc35934db89b33cc7a262358146ba79151e171efd78b87b7`  
		Last Modified: Tue, 09 Dec 2025 01:27:24 GMT  
		Size: 3.1 MB (3130805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd1a3fc627d58d717ec66c97cd32a506e7e0a248376254f93dd80105096945dd`  
		Last Modified: Tue, 09 Dec 2025 01:27:25 GMT  
		Size: 5.8 KB (5761 bytes)  
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
$ docker pull debian@sha256:38d58bc0eaed5e23c8719078b57105fd66dd1fb823edbe036160d7b2e0b245c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46840579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b660d53c1cc19e41939e3d9394dae5ea00d8b29dc531d5e62b3fade6ac87dce8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1765152000'
# Tue, 09 Dec 2025 03:05:18 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:002664050c13ca9d4571d9c24b2cd8235785825417d0a59db3d16cec4b277530`  
		Last Modified: Tue, 09 Dec 2025 01:49:57 GMT  
		Size: 46.8 MB (46840355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22bbfb35d4b89a8d6ca8d5f881fda6dbe3bc09a030df2b466f622e3d2ab8d81`  
		Last Modified: Tue, 09 Dec 2025 03:06:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3febcddfbd3fcea94d5841d03269d8297dc3afefe520ce391baf0018d12110d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3130092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba64ff28733a1003099aba95d41f3e4c0d724b889e546c1724d9c033d99425a7`

```dockerfile
```

-	Layers:
	-	`sha256:50886036db685fe1c0c48c92fc596d32b714ed96e16873b6d699a2187dad71d9`  
		Last Modified: Tue, 09 Dec 2025 04:24:47 GMT  
		Size: 3.1 MB (3124288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e481ce234501d529d23f07c9ceeef6dbe079149a1b8ef8f9501300f273c49cb7`  
		Last Modified: Tue, 09 Dec 2025 04:24:47 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:d301428550d5bd3d28170edc3c7769812bc5f9a58d0b35a690662819991e5a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48320060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:912e563ba4ea45c3b5b4f5c6276fe9e758072ec8c22519ac352488af059e0a3a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 22:29:01 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:88e5ed2f2b5ebe4c22b20536e853aae0963f42dcc4ff80e14e14172e983096b3`  
		Last Modified: Mon, 08 Dec 2025 22:20:13 GMT  
		Size: 48.3 MB (48319837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7613aa0eef75b3de0ba35d74ec12b879ebc2759f3e47b32a5fd164f7e2eb29cf`  
		Last Modified: Mon, 08 Dec 2025 22:29:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:efa7d72b02c3767e6cc4d76a37b829c5eb63cf3bceaaea8fa83da86562c5e0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68492e8fd32e7f2f928af214573b4c2ccd054fd3afbf0369b1356bcf1f73152b`

```dockerfile
```

-	Layers:
	-	`sha256:3ca12b0f65111f2f4952f9685ab033f997b7bce704ce771b4715e229f37548c9`  
		Last Modified: Tue, 09 Dec 2025 01:27:38 GMT  
		Size: 3.1 MB (3135050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16eb9e398b7aa0d3937cfc439851841abe33fd9249ea8aa4a2ab33466ba2fbe6`  
		Last Modified: Tue, 09 Dec 2025 01:27:39 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
