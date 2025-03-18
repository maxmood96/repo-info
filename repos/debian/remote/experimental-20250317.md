## `debian:experimental-20250317`

```console
$ docker pull debian@sha256:68951fd42547f3f05d02382efad24f7526ca7bec78a0ac75510a96acb57ae8d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `debian:experimental-20250317` - linux; amd64

```console
$ docker pull debian@sha256:ed31a617e786606bc1ed5611a96875e24753d8bfa10d7065d56fdf1b9f0606f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47542856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a9c19dc1559a31f728c02afd6705df67b3407e5cbf7084ef178560f97b2315`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:be50d1a3cd644842f5bac5e93981bb11fbc932dfba02577de8c576395cf05056`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 47.5 MB (47542635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c58d8416fd8b4237216f6817521f00cbd05c6bb40963cf9df51e04102ea5d55`  
		Last Modified: Mon, 17 Mar 2025 23:12:24 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20250317` - unknown; unknown

```console
$ docker pull debian@sha256:cf4e720f1a63d79daeeffea85b93db058ce04c4c4f6b215f620496681ff12e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20729e32e33643920ebbb58e1004a11b1fc276c85104e90143e6aa4e766ff78`

```dockerfile
```

-	Layers:
	-	`sha256:3b75327a77e145c45837615f772c6d3d4317fac557896ec9bef1b01b91e12fbd`  
		Last Modified: Mon, 17 Mar 2025 23:12:24 GMT  
		Size: 3.1 MB (3050726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c743ce79db36552eba882fdb6bdf15e470b01b778615eb57d24eb880872564`  
		Last Modified: Mon, 17 Mar 2025 23:12:23 GMT  
		Size: 6.1 KB (6143 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20250317` - linux; arm variant v5

```console
$ docker pull debian@sha256:766328a95ca7f91b7c15bd72f3089e9fb06d75920bb297788667cc77ddbf4a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45764260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3979cda74490058d7cb1edbe9a0a9a4771dbdc90b028c638a1f59a5852a618e0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'unstable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:492a29252a6f9b312f5a132ad7ff337f64a79ae665e669500f482f05d04fea50`  
		Last Modified: Mon, 17 Mar 2025 22:18:40 GMT  
		Size: 45.8 MB (45764039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa44c27a8fc829ae9b16269f338229647310aac20b6e393339f18e2eb255e7e`  
		Last Modified: Tue, 18 Mar 2025 01:22:28 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20250317` - unknown; unknown

```console
$ docker pull debian@sha256:5d54e7d6f65e50cde2703e56029a3145816ad92380ad9c5a3a8c696d7565cfa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3065153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb35d20898e8799c75303c16033ae96dcb347de6ebc5b6595fc258a153ad09dc`

```dockerfile
```

-	Layers:
	-	`sha256:916bf0d074fd2b02b60999f3738fd113ce486db9c8b5f3d28619fe830d0f3f9e`  
		Last Modified: Tue, 18 Mar 2025 01:22:29 GMT  
		Size: 3.1 MB (3058949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1a217b4f5b2b7d3eaff98152fca7764f6f271bb6cb765d48ea326b7e19aa7c3`  
		Last Modified: Tue, 18 Mar 2025 01:22:29 GMT  
		Size: 6.2 KB (6204 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20250317` - linux; 386

```console
$ docker pull debian@sha256:dd20763a1e5dd49f4a887c3f2bc2760fc7a6f1db5d68bda81aad60a7240a2994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48863381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80404ffac0105fe7b45c6d692dd55b35c4c42fe7c1621816c204576344194f8c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8a8eda04047bfbdd4652b1137ca527913a5aba61c68507b0a21280646646d380`  
		Last Modified: Mon, 17 Mar 2025 22:17:55 GMT  
		Size: 48.9 MB (48863162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee42be05a6614d4c296bc80a12b07f2c9e39cd77d6d65f00022e249a2dcd6274`  
		Last Modified: Mon, 17 Mar 2025 23:24:57 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20250317` - unknown; unknown

```console
$ docker pull debian@sha256:37636542ae6ed26235f30392a7d312dd7acadf8d0223711cd5196ed6990486d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3053376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6421637002c3c4af86d8fadd91bd2c0e2fc81fba65bc03d86876f5619a415e7`

```dockerfile
```

-	Layers:
	-	`sha256:0ac6be62ab1e09110e169335b6d248d5593897f455aa517e1715c6575435d179`  
		Last Modified: Mon, 17 Mar 2025 23:24:57 GMT  
		Size: 3.0 MB (3047254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37eef453684567f501bad82c9130e2bd2f135118b800a044684a89a9693cc282`  
		Last Modified: Mon, 17 Mar 2025 23:24:57 GMT  
		Size: 6.1 KB (6122 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20250317` - linux; riscv64

```console
$ docker pull debian@sha256:8d0cb0148f815411e68914e25bcf67710ca50688676c8859c9f891dc0e56c83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46065646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b500f6bbfc91a2225856e457f264d3512cf50f9a76858515b896b6f4f005096`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:fd1df93facf99bea18e885b88274ce89ce70c9d47da287851c48c0ca674f271f`  
		Last Modified: Mon, 17 Mar 2025 22:43:00 GMT  
		Size: 46.1 MB (46065428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce198f8841bb89c17692e87cb9eee495f831e3aa2a2f9b0f825f74bf8bd84330`  
		Last Modified: Mon, 17 Mar 2025 23:18:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20250317` - unknown; unknown

```console
$ docker pull debian@sha256:69bc9b0008b9e75b2e3e1c06de177250b1897d8807f08369eadd2c2b3a2d88d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256c9855699399d1199003b296583af0447abd398482c738995ca376a0ab0a10`

```dockerfile
```

-	Layers:
	-	`sha256:3cd073ecb6b5ff2df3e0f880cc93de86ee146dd7e18ca72a37395ec4826b1895`  
		Last Modified: Mon, 17 Mar 2025 23:18:14 GMT  
		Size: 3.0 MB (3041961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10441b60865782521214ae68df0ede1290760d125e5f004d3ec2207fa3ddae40`  
		Last Modified: Mon, 17 Mar 2025 23:18:14 GMT  
		Size: 6.2 KB (6176 bytes)  
		MIME: application/vnd.in-toto+json
