## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:a1a6f2596791d711c63d7ea6b52b64292f9406c195ef6ad31ab56c13cf7df937
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:6819cd90bf297447fea08ec7b49866c07804ea3992679d1669db49dcab588ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53747963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1c042b7038db6e2afd0e86a827bf74094d4ce884e512729347f9dd7eb12b50`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cd57768b1c18471666f79c96dd9638da1aebd359e0991692553ec25b7923a21b`  
		Last Modified: Thu, 08 May 2025 17:05:29 GMT  
		Size: 53.7 MB (53747739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a5ea3851f3f650f40ad94976f2ccc097172b8bf1c0f5386be17312d299e6e5`  
		Last Modified: Fri, 16 May 2025 19:52:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:897b8f19ccb71700f6e1d1eead0cf7cecf6154476cd3090eb2349a99de08141a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b9bbea5902c95fe56886c2884a75cf8fbc302c9fe2028b571b74f159fc6322`

```dockerfile
```

-	Layers:
	-	`sha256:0de4e6fe3f8e960932368e58da9341505c7f53c76f762118df0028cd0371aed7`  
		Last Modified: Mon, 28 Apr 2025 21:42:15 GMT  
		Size: 3.9 MB (3919486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e05bde95483d206b22488985202b1cd13afd9b0e31ccc1da6d6bfe45754f4a46`  
		Last Modified: Mon, 28 Apr 2025 21:42:15 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a024b4cc22f77c27704190d27453d5ebc515da34490c2644368de414623b0706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49040273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94d3af1f63ce0d22ed6f8f78b68fd92691187dd3987169eb64b282f873c0ad6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:365d93ec09490d2a4c51b62f1cc289885d4537cbc2e404e3bf5241f4de09762d`  
		Last Modified: Fri, 09 May 2025 11:25:12 GMT  
		Size: 49.0 MB (49040050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78521e2ac167fe1e0a398428c2b7c70e834a4b135fc715147e05164eb9545539`  
		Last Modified: Mon, 28 Apr 2025 21:42:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6edf3cdec1ff6e13b20204d6c817446596b62293d6e24336db1f5c1bfb432cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128cbd31eb6947803f90fb563c61bfa322c6f669ce1f8ed2fd5c10ca60ab13fd`

```dockerfile
```

-	Layers:
	-	`sha256:2486f4f4231b8d132cde393a4c1f1fb04b7106b68598d9e2dd110405f4bdb26b`  
		Last Modified: Mon, 28 Apr 2025 21:42:56 GMT  
		Size: 3.9 MB (3921048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05a2b7808d4eb92546fe22b6ad2626f112a0d8aac1e4530d52b3ca020086ddaf`  
		Last Modified: Mon, 28 Apr 2025 21:42:55 GMT  
		Size: 5.9 KB (5903 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:dd109e68f15679f0611a84c53dcc485d23914187549a20ac9ea9b75d74c742b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52246205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baadbf8b1d72952b42c35579c5d9185581f9e2eb6269ff5b9d8ce5d76aee731c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a72b49eaa728af0e27c4b3eb094f86b3c23d721373e168a0e4bfcd5a2c74936c`  
		Last Modified: Fri, 09 May 2025 09:59:46 GMT  
		Size: 52.2 MB (52245980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bace05d963a6e837a3de3f2b3feaa1a8c3e7f3fa4f7e93388aa972dbec4a0e4`  
		Last Modified: Mon, 28 Apr 2025 21:42:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:60d2940dc708d26445ae8780b409aacefe264266ed47ce1fc3ff9b5ee9a2728c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf3a86b2f02650b4a4cfeb6682fde358b8eb480346a34aa2c512602d4321ff9`

```dockerfile
```

-	Layers:
	-	`sha256:1d31050223ae3bb22299c3d6ee893125b22121f2916539d02f5f492b7f4bfa2a`  
		Last Modified: Mon, 28 Apr 2025 21:42:23 GMT  
		Size: 3.9 MB (3919066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba045ea641f1edf1d357c247348b1d05dd84771193fdce86883ec21fb3ac0b69`  
		Last Modified: Mon, 28 Apr 2025 21:42:23 GMT  
		Size: 5.9 KB (5921 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:0c14c4deb6a433a055ce82829ccedd7f2cc7fff3c2a9fc5cfd1d27684d65dc09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54683330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0764d1a496b63483db90400d52f27ba3503f05dd36a2fa621aacc7a5fa5f0b63`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8894ea465466ea0cd4c3d0e9ed7670a66ede8a1870013e24b8f3b0a94ef420b6`  
		Last Modified: Fri, 09 May 2025 05:17:22 GMT  
		Size: 54.7 MB (54683106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b85e5ee118120b3238cec7d8f829bb22e0bebcafc59ee8c5c03744fc266a2fc`  
		Last Modified: Mon, 28 Apr 2025 21:42:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:52d9aabfe3b80a223596314775bb3f904cd41a2e7ad1d8a413e055fab22158a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60c4fa8c9f319feea726bd30d69867aeb160ce62a8242d37096469035917590`

```dockerfile
```

-	Layers:
	-	`sha256:0b87bb84cebc41931c1202ed7926a51747c55533e7b843f0968a8f4396debbe9`  
		Last Modified: Mon, 28 Apr 2025 21:42:07 GMT  
		Size: 3.9 MB (3915993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30123dba0eff2b34fb73d31cfd79e253ca96bdfc42d95976e2f8599c0f58984c`  
		Last Modified: Mon, 28 Apr 2025 21:42:07 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
