## `debian:stable-backports`

```console
$ docker pull debian@sha256:37174b257fa92afb7a73ddded6e41bbb69a114957c4cbf2859ff51b5c3ba84e7
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
$ docker pull debian@sha256:f9fc17e5c33b0a983f3ee841e840d06664fca3040ad3c45560f04baa0d229a87
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49555216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43103c79b9305d63c3bd1c7699426f157ff34c6f9c4c94c8f6df6415191aaebd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:21:40 GMT
ADD file:5b0b330a1744d2fc462db73ca1ede3057676f55ba9ba4fbd0c8f1dc7f35e4fa5 in / 
# Thu, 17 Oct 2024 00:21:41 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:21:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5f399c0ccf91e64b5bd6c7483b37ef860d40c3b621e2543638d6f73be6022ba5`  
		Last Modified: Thu, 17 Oct 2024 00:25:48 GMT  
		Size: 49.6 MB (49554995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65e296a38f44013ee9025314a88ced58804c4dd1f7ff5dd1633ee7089e333b9`  
		Last Modified: Thu, 17 Oct 2024 00:25:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c08e9ff443a5dc49af27457811995bb4c42980da3bbeabf465de62b8f0d70d8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47330715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddcc408b27a2d00c6d4822da4645f528ab415ddce6dbb2b9fffce15798588e5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:55:06 GMT
ADD file:5a6ca6c398caf783271e97f0e110e9cf53955304db967e78094aa5d4bd1caa04 in / 
# Thu, 17 Oct 2024 00:55:07 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:55:11 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1f19ba83087ea5a419d7d26a8b21cefed9a0e836845908d9c67cf4c0c5cf5ac1`  
		Last Modified: Thu, 17 Oct 2024 00:58:13 GMT  
		Size: 47.3 MB (47330491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1d2e26c5a2b143961c836d642efeeff656ffa40f36daff31ae0c02574cc9f7`  
		Last Modified: Thu, 17 Oct 2024 00:58:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:947454d1bd7645e1fc6e995c31e233da2da66a7e5c1f13e7c666901616a944ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45148170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc57c3dfd90edf547c6a79d39c7eb2b3536a52d4f785cb694127bbc75b9af34`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:04:39 GMT
ADD file:70ed99d815da8b39a01338550d77464aca223371776dfa5027549341579596a6 in / 
# Thu, 17 Oct 2024 03:04:41 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:04:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:45328cf0ec805d9ef287241cd9488b68b9597381c7948a6c0e9c7107723b71a3`  
		Last Modified: Thu, 17 Oct 2024 03:09:25 GMT  
		Size: 45.1 MB (45147948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89ada3694fdf872252f7e066954a2bd9ca068033e105ec6c9d263f7f7abfa81`  
		Last Modified: Thu, 17 Oct 2024 03:09:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:b222ccefe5ad7a6a826865213eabf3e0e2323c7f8b2d8fcf164665347c5b763c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49585224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6cf022d525e8dc5311ec1036af0cd4c8704c1627e84f91ad0298fa3b9e813c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:48 GMT
ADD file:4375adb1a6407ffa1c07c5443866380cf7471b0c8309778a32965d3983405c1e in / 
# Thu, 17 Oct 2024 01:12:49 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:12:51 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f99e0f62e90785fa592bc825c63c1e51537fe8c265b45920d6c0dadf2a77755e`  
		Last Modified: Thu, 17 Oct 2024 01:16:20 GMT  
		Size: 49.6 MB (49585003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0087ce495962148f9df3914ad65f0fb5de0491c14098bff69fc4e82860e6f8ac`  
		Last Modified: Thu, 17 Oct 2024 01:16:28 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:98c0800788b92edfed4c8e4f434d428f5706f1056ab45d76ce2c3fb93e73b785
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50577041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a04b218cda7840aabf69a06f9f19793921acb6025c9b2da4ac3f9dbcc023ea7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:40:11 GMT
ADD file:77a67911f7516e842633ee4e2e8cd8e96a98bdd6df5c6b0a68794aa2e3f0cf7d in / 
# Thu, 17 Oct 2024 00:40:11 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 00:40:15 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0d4f01c14d037e59aeee1b97d0b72f4595f4f68cb8af1dc8909656eed2e4ae16`  
		Last Modified: Thu, 17 Oct 2024 00:44:42 GMT  
		Size: 50.6 MB (50576821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e640e2fade7d18df4dfcc5fe4ea4264a4f25574d8eb6cb157ee76083ef3fa803`  
		Last Modified: Thu, 17 Oct 2024 00:44:50 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:8bf216acf7f0f349ae499c86a44c2c9d57e7847b8aa85c5cb2b74516f6e47d2c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49561762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729a4e44c2fde0b5f7cf98e160306602e6afe82848a1045c108e0bb401414810`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:19 GMT
ADD file:52006529407d690b8b4fd0636a4c6e5bdbebfd579745a5ae72d3d673d574638c in / 
# Thu, 17 Oct 2024 01:11:26 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:11:39 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:007cd58e14e765f02dec6cb16299e8f77041fe3c10ada317c83bec644b15d3b9`  
		Last Modified: Thu, 17 Oct 2024 01:19:53 GMT  
		Size: 49.6 MB (49561539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8408c6cc510c081ccb7256eeb1f9dbf6e5ee6a7005f41fc9d993fd4b593376`  
		Last Modified: Thu, 17 Oct 2024 01:20:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3c7e39521c58e3358c7393757a7dbc134f695d43c2a3c40896baad84a8531d5e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53555798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4eaf1c25b5d5350098fa946302aa92811d46fd32665783cdf8d04c411ec35b6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:19:27 GMT
ADD file:8f1af70f9104723c1cb5b1343c3551d048655028d873f6f94c349d3f2f002f9b in / 
# Thu, 17 Oct 2024 01:19:29 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:19:33 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fb1fe299cc59f94b5fa9f6503de36600a3dbc49c31bef93aa558af9f3db55de2`  
		Last Modified: Thu, 17 Oct 2024 01:22:45 GMT  
		Size: 53.6 MB (53555577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60100940a459158481d1b6429ad6274ceed227a5a6ee0c2fce0ab087dc39749c`  
		Last Modified: Thu, 17 Oct 2024 01:22:53 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:a15948ac3d659d39e2ff9c7e29915e6a7d359b76c9b37f69ab88207a289a7d86
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47938668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a3643ce7d6ab996b759cee1590607846dcb9817a045982f650089a15112438`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:47:01 GMT
ADD file:7080f7e745bc9169b2b16a85dc2d8f9327091396094ba3d187580bf2d70b02d4 in / 
# Thu, 17 Oct 2024 01:47:03 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:47:12 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:183d7535ea9f801f35bde93bcf3c4e624f2015c15f9e4d7a5e9d3c35bad8a5d8`  
		Last Modified: Thu, 17 Oct 2024 01:51:07 GMT  
		Size: 47.9 MB (47938445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf129686f9e49b8eb2e7edf2bdb74b2664ec3a2432e6bec191db037f7f4b0c4`  
		Last Modified: Thu, 17 Oct 2024 01:51:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
