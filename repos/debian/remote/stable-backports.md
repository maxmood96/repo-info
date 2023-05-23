## `debian:stable-backports`

```console
$ docker pull debian@sha256:a0b895ef38367294183dadac52ddc0b9847a477e365a9f2c1d4d3c36a6eefddb
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
$ docker pull debian@sha256:2d06dd1889e83c523bf94814fb2e07c51f7d2e09937d50751de03ef25a303151
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55049295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c122435768d49c87ab83c56afa4d4d91d8d875d93c6a2fc6e00de90d73eb865`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:58 GMT
ADD file:aca9ba794e6ed1062dbb831089b8d9c18bf7bb6c8194581cd3e1fb5e80e527bb in / 
# Tue, 02 May 2023 23:47:59 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:48:01 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6a918b9b11d0639c4549e67523a135bcc5e27da3087ddd02fa97bf8c8e71ec24`  
		Last Modified: Tue, 02 May 2023 23:52:21 GMT  
		Size: 55.0 MB (55049073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94b7325148dace42761b8c59bcda56128837c69bc252354ced5471bb9500888`  
		Last Modified: Tue, 02 May 2023 23:52:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:48f4ec2339c2ecf5b6d39e9ff185d648548e05b9f94656b60813b2bf2cc1e140
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52546751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf192883cfe1c289f7b18e82ee81f5e2acf2e79983c89d9c9e7f54221be70ecf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:49:04 GMT
ADD file:a7ce6daffcaab5e86d1b065b79e5f6d5b62ac6924e9ebb3af3840a4cd16c9145 in / 
# Tue, 23 May 2023 00:49:04 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:49:07 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b7c04128060bdb0b7fc5c5b5c8a1ae38a46b52bb129b9cdf2a6ef3166e944f54`  
		Last Modified: Tue, 23 May 2023 00:52:05 GMT  
		Size: 52.5 MB (52546528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a4e9dca4b95c38f856b701a6f976e5112c447e8055884eee9a41332298511f`  
		Last Modified: Tue, 23 May 2023 00:52:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:584d878ef566d9406062f739bc1126baf103a4231786355f66a76e32a5375923
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50210203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b84c2eb2c13b94db716abc698525cfe1b21ac36880956dc070da19783d5d478`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:59:11 GMT
ADD file:ed8252176a553415d5fe0be311fb0c14bbd7dd30a1d6e91360641aff08332acd in / 
# Tue, 23 May 2023 00:59:12 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:59:14 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ad5885f07f90761e7d44492551043940755ce32a3c3549879ea062a09fb8ee01`  
		Last Modified: Tue, 23 May 2023 01:03:40 GMT  
		Size: 50.2 MB (50209980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f038725c63c75235eb235f0f6345ec4d6a0acad85d0d9460cee4199a4dc6bae`  
		Last Modified: Tue, 23 May 2023 01:03:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:27c615f410e7d491e2686e209046ec1ecfa9dc7e3d44a103ef916d73fdd3f4a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53692901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8bb3c304a4b418802efe162e027189164ff90b0915f8a33821a2cd104d16a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:44:00 GMT
ADD file:8c39761e06e93a81c2bdcb82b2b7e2587f0d2d72c919e58b40bd84dcc35021a8 in / 
# Tue, 23 May 2023 00:44:00 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:44:02 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6b0080b5d62a6667c11d7b5d4e8631ae1eb401a9089242439f2a81b9b4fe8ff3`  
		Last Modified: Tue, 23 May 2023 00:47:55 GMT  
		Size: 53.7 MB (53692679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a997c4bd43e6e1d8bd8a06376fa3fdadeb71d0cae238ba5d12a3e0faec78ca`  
		Last Modified: Tue, 23 May 2023 00:48:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:38723bd26de84ee904466d725bb00dc6d2a6bedbd268958a2390d40845ea85ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56029431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d0e96bb396cba89a98707d9647e39279f373641c3cfbb7b9905943a99c53a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:41:17 GMT
ADD file:b793d97c39d3a4f52d78e32584d687c505fe466e9afb27a364417df9492dcb93 in / 
# Tue, 23 May 2023 00:41:18 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:41:22 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9e0d6f08419f92a8b89daf9a7e2ab2c0ed4a8f425f071667edd00506f57f94cf`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 56.0 MB (56029209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69734504f3c92b17946bfaeafc265a7ed728801b5a4b842d140b7bd1d2ff0842`  
		Last Modified: Tue, 23 May 2023 00:46:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:6303e9021d2e6a75f8383e2210bb74769e6d894c5aba560ad3046840879ee0fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53261373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950b07931a05e5f22102791ecd553798859dd1fd62dba965e2c0902b12e23df8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:12:22 GMT
ADD file:ffe0bed4346e6ccbd360dd605c9f24a359bd59781035dd0b065103bdf71704c7 in / 
# Tue, 23 May 2023 01:12:27 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:12:40 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ba9420f91add5f9bd924f2c32a77e3913c8d41961e14c7a0b84dd7eb0f19f4aa`  
		Last Modified: Tue, 23 May 2023 01:21:11 GMT  
		Size: 53.3 MB (53261147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c23a12cbabbdc645b8cac7c383caf683535d67ed477f0399720318af9a7f792`  
		Last Modified: Tue, 23 May 2023 01:21:21 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ac32071d00bb9d963372fad8a90b08a120b772dcda81165032dc37225d3ffc17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58924154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f767b95527cc0a6f06e9a84bac13a78a5a980ab418fc4a87be1b018a95308ef0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:18:24 GMT
ADD file:4d188face69b4e5955e341e5e82b1f6ec7abd69da2a905d9f71f7b16f94e7e27 in / 
# Tue, 23 May 2023 01:18:27 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:18:34 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:98f484a6f9171457e3a7c2a8cd6aa3f88cacdf3b9f0f34679091bebcd681594c`  
		Last Modified: Tue, 23 May 2023 01:23:08 GMT  
		Size: 58.9 MB (58923932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa575747802634070903692a1072634faaccd5e457eb683ffe6b00744e578d40`  
		Last Modified: Tue, 23 May 2023 01:23:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:5785882c5c12cf9f1bd9f7146f62f027f549fcf8862024f59e244ee1bd622e6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53282260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6dbaa64f5b0ef67b68f533fdb9d117b4e96d7ff6ac2a35c743c0960473d345f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:23 GMT
ADD file:d6a29277043d384025e8e48c8f9906c7701c5d7f83df2052bc67135d4ff27c90 in / 
# Tue, 23 May 2023 00:43:26 GMT
CMD ["bash"]
# Tue, 23 May 2023 00:43:30 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f04651182dc3dc56cac1369f338027ba72d56d2efc5a0674946fcfb139e58559`  
		Last Modified: Tue, 23 May 2023 00:46:16 GMT  
		Size: 53.3 MB (53282037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d4f2dfb9774cf46d36c2643c04719d719c0d9e63bdf343a20ad371c38aa380`  
		Last Modified: Tue, 23 May 2023 00:46:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
