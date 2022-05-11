## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:7c2245e46962359a3f5d5f837d8f0b04c6bb129fb54ca9f6cee6e202a50964b3
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:0e15601f2bcc351fe96c59ddcad6bd1588a525a8dcf2b2466b630712b85c8288
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50438180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9418164fe1887ed2f941404c75eeb20096223c32dbbf316abd08f50029693271`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:21:06 GMT
ADD file:8feca9d28a2a8d6126daec12998c85ff78e935d64bc69fbea9fc619031218d02 in / 
# Wed, 11 May 2022 01:21:07 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:21:10 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:121ac68e5d46421809718fa673b83e12dab2f7f5304f1ec020d8d071520ffc52`  
		Last Modified: Wed, 11 May 2022 01:26:52 GMT  
		Size: 50.4 MB (50437957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f7867544b043b157b84fac080e386b2ecab866532309593545d269dc446a1a`  
		Last Modified: Wed, 11 May 2022 01:27:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:315a6620251c0d8971415ca776844472a2c76c48094ad85ec36af949d331c2de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48157746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a491c68c6586cb44460c16bd98e93d2e80f3a73fcc05382f478179a370c274`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:52:55 GMT
ADD file:52714e05eac3ec4a580498eece5bc04180a97c91db34b5f384ad4269e59ca287 in / 
# Wed, 11 May 2022 00:52:56 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:53:08 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d34300cf0b997d5df249ea70a7fa8dedc9c567168af6538af7d2bf1f6a0e2f4a`  
		Last Modified: Wed, 11 May 2022 01:09:20 GMT  
		Size: 48.2 MB (48157519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bf94ce32e17fc2fd6d028ad76b949258e94932a25ca2eab0e18aa18d4e1228`  
		Last Modified: Wed, 11 May 2022 01:09:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ce71e54359a3086262197b78db1974e9ec6896c4e7b9f59116d40daf0221f446
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45910419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342046566dbc00316e633a6237d2157f0ca4cf7121f7cdb409900f94202ee5b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:51:42 GMT
ADD file:bc23b97fd6c65c5c3801548bc21a9307787fd43f930ec52544d47715e005ed79 in / 
# Wed, 11 May 2022 01:51:43 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:51:56 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cc2fa3cda1ed31d10ab5b045cba773f39f43692685819c78f936576e2e072c89`  
		Last Modified: Wed, 11 May 2022 02:07:50 GMT  
		Size: 45.9 MB (45910193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ea8b22c610a1c24a9c31384c01c3de30c406d21ed7530890ffe8ee25471813`  
		Last Modified: Wed, 11 May 2022 02:08:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:23475fc76aaeae0342e45109a133f41030f01a444b8517e9d4474d46e2f3cbc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49228515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4af5b03beda7c39fcd011569a38632211de42705ca3bff83ef453933352637d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:48:00 GMT
ADD file:a19c4cfc91f51500280db6ecfe71d20b71d666d6aff7bd6161a5e25ec4c13f8e in / 
# Wed, 11 May 2022 00:48:01 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:48:07 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:565c068692a23f9c85908d1a5015be980d1002d1cd300e6bf6a95bc2140d5b50`  
		Last Modified: Wed, 11 May 2022 00:55:35 GMT  
		Size: 49.2 MB (49228288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb5b9b34f5092939f99df56a89d451519b9ab41429bf23428d40ecb1a91182c`  
		Last Modified: Wed, 11 May 2022 00:55:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:f1806c0801fd581963d40925c2f28fe6cdfccba8b3b20ea35d6f4091bca8bbf8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51199475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1218876b43f0b03f3a291bc110c00e6e3b98e71da20af22f8bf45e5b887c8ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:40:17 GMT
ADD file:c747ed587d8e11217fa76c62807de5022d30623435b23dddd4f6de239bc585db in / 
# Wed, 11 May 2022 01:40:18 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:40:24 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:835d7dfaf4020ff6300223a88a971a10d095515910a2aad9fe5a29075574ebb2`  
		Last Modified: Wed, 11 May 2022 01:48:27 GMT  
		Size: 51.2 MB (51199253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2082d64d251178349891be345c6893aff6864b00eeab11fe06c3692a09d1fcfa`  
		Last Modified: Wed, 11 May 2022 01:48:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:69feddf1306f18fceea49db6fd151e7e10435c18b8ec59532228c78f160efd24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49074015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5038da7be014f28533d572b367cdb6501b7719157823db5b0d824e9a1df72ebd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:25:15 GMT
ADD file:178e9c4ae0ba73a39c5b219aac7fdf90947e85dfd216f3e6cc755689cb94d01f in / 
# Wed, 11 May 2022 02:25:20 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:25:30 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:530ea5816183e6df78f38b719ae529269973d546d9dfd2215ddc097166ee82ba`  
		Last Modified: Wed, 11 May 2022 02:35:46 GMT  
		Size: 49.1 MB (49073789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438a8be483fb6f9cd16e1ec74e49d785d1a774a59c7266f7c39f3e7491748959`  
		Last Modified: Wed, 11 May 2022 02:35:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a6a18d55340c19a736cb2cf9ce4db66f1ee0b9f04b9c99040c05eed89fd6bc58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54170446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06944a714791d50b91aa20ce9883a7842a4ea7a1706cb200e3b3c3a5e3e55c83`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:33:56 GMT
ADD file:d94963f087ad2000194535dedbddaabeb9aad13ec17d2be7cb40a10331518cb1 in / 
# Wed, 11 May 2022 01:34:06 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:34:29 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fb1dbf946a84c7b646db97d3a663ada35dd5588d1a1df869dd21916fa072de04`  
		Last Modified: Wed, 11 May 2022 01:44:35 GMT  
		Size: 54.2 MB (54170221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465313426012f74e86973acc5f0d93cf319729015129d687767f25fc5a67f5d9`  
		Last Modified: Wed, 11 May 2022 01:44:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:733123e8ca37737557c3b178503d99171ee62490096058821ad712ce579a2a6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49000656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4405ea1c724c37b216ffa0f1e94cbf75795f50a34d4c3f8a997a9d0a0be68c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:44:59 GMT
ADD file:6069472527b01923a4f81598306cc92aeb2d904dc81819d3045755b9563e6534 in / 
# Wed, 11 May 2022 00:45:02 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:45:09 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c890bf64515e35579d8730e47b1bf5a54da4103c035a06dced027b30afeb6153`  
		Last Modified: Wed, 11 May 2022 00:50:59 GMT  
		Size: 49.0 MB (49000432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d583164ad023b821e26155ff0fcc40ed26b3d8e13d89e0608b93f94dac54b6e2`  
		Last Modified: Wed, 11 May 2022 00:51:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
