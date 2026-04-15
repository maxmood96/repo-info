<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.22`](#nats2-alpine322)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-ltsc2022`](#nats2-nanoserver-ltsc2022)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-ltsc2022`](#nats2-windowsservercore-ltsc2022)
-	[`nats:2.11`](#nats211)
-	[`nats:2.11-alpine`](#nats211-alpine)
-	[`nats:2.11-alpine3.22`](#nats211-alpine322)
-	[`nats:2.11-linux`](#nats211-linux)
-	[`nats:2.11-nanoserver`](#nats211-nanoserver)
-	[`nats:2.11-nanoserver-ltsc2022`](#nats211-nanoserver-ltsc2022)
-	[`nats:2.11-scratch`](#nats211-scratch)
-	[`nats:2.11-windowsservercore`](#nats211-windowsservercore)
-	[`nats:2.11-windowsservercore-ltsc2022`](#nats211-windowsservercore-ltsc2022)
-	[`nats:2.11.16`](#nats21116)
-	[`nats:2.11.16-alpine`](#nats21116-alpine)
-	[`nats:2.11.16-alpine3.22`](#nats21116-alpine322)
-	[`nats:2.11.16-linux`](#nats21116-linux)
-	[`nats:2.11.16-nanoserver`](#nats21116-nanoserver)
-	[`nats:2.11.16-nanoserver-ltsc2022`](#nats21116-nanoserver-ltsc2022)
-	[`nats:2.11.16-scratch`](#nats21116-scratch)
-	[`nats:2.11.16-windowsservercore`](#nats21116-windowsservercore)
-	[`nats:2.11.16-windowsservercore-ltsc2022`](#nats21116-windowsservercore-ltsc2022)
-	[`nats:2.12`](#nats212)
-	[`nats:2.12-alpine`](#nats212-alpine)
-	[`nats:2.12-alpine3.22`](#nats212-alpine322)
-	[`nats:2.12-linux`](#nats212-linux)
-	[`nats:2.12-nanoserver`](#nats212-nanoserver)
-	[`nats:2.12-nanoserver-ltsc2022`](#nats212-nanoserver-ltsc2022)
-	[`nats:2.12-scratch`](#nats212-scratch)
-	[`nats:2.12-windowsservercore`](#nats212-windowsservercore)
-	[`nats:2.12-windowsservercore-ltsc2022`](#nats212-windowsservercore-ltsc2022)
-	[`nats:2.12.7`](#nats2127)
-	[`nats:2.12.7-alpine`](#nats2127-alpine)
-	[`nats:2.12.7-alpine3.22`](#nats2127-alpine322)
-	[`nats:2.12.7-linux`](#nats2127-linux)
-	[`nats:2.12.7-nanoserver`](#nats2127-nanoserver)
-	[`nats:2.12.7-nanoserver-ltsc2022`](#nats2127-nanoserver-ltsc2022)
-	[`nats:2.12.7-scratch`](#nats2127-scratch)
-	[`nats:2.12.7-windowsservercore`](#nats2127-windowsservercore)
-	[`nats:2.12.7-windowsservercore-ltsc2022`](#nats2127-windowsservercore-ltsc2022)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.22`](#natsalpine322)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-ltsc2022`](#natsnanoserver-ltsc2022)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-ltsc2022`](#natswindowsservercore-ltsc2022)

## `nats:2`

```console
$ docker pull nats@sha256:fd76fc5a1fd3e8e1b8c14ef1ddd04f9b379df11bb73e48ff417eb12b07e4c387
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5020; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:ecb873658a349d84b05ab89ccdc9dc3d3153e45b1c32f344c56383cfe78090ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0247f7685ff68b4ae975febd9a287b05bfd142373a9ddeb8c2dac6bfbc859`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040b24667adc09216d21ad3439155962ccadd3d91a63d56b7da7fc06ee4af8d`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:248f347c9c2745bce92c2706cb33a87211172a8f8e92087fdc501d07f7b8de4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43eac3eec77ccc736e40ad70b7026f77225ac7e5837afeb1a08f32fdd7d0b93`

```dockerfile
```

-	Layers:
	-	`sha256:d702fbcd1bfaedd00e8319117145a6389d6ea5e0c82a9d42f3162b728faeb4e5`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:6b0b00a37ddb7979ca235c35428c360669c9da2bcfa9233ae1ac9be85d0d4345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444254e21a5a8780d3528d8d19efbf156e2c5abdbb0cfe9788f1d1eedab18e2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:38 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1a6f37e82fee0dcce9cf7e8571403adb7ce8ca76666035b362c31649f4b2e`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:550334371afd2696f12dac3fd3739eea092ac27f6b0b773744e87d63aae577e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63dfea61fd8fa9fa90c1a671898c3ff2dc3edfc998eb6478ee5c9b3e5f33d7f`

```dockerfile
```

-	Layers:
	-	`sha256:958b223cfdb0c6fadea45187b0bf34bd7314cdb490d8581c32cd73f85ef90ae5`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:88aeaaa7e2045ccc03915e3f388f392216411e3fa768956ec3b12003643e8697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e37b72ad4a2af972471eebaedf8daa75a569452f35b1ab43ebe86fab23da376`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79c24a16cb2f9ad04dc2e860c74b6a0c8653d0340378eda7c4a9db7fac2f355`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:b8ac0ce4a3228e54e91056d63c0aad4573821af86e16530e157710c2c2f48ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e7d98c930153daa0f647ce1a34edcfacc5ba63ac0cdbfab10485093d0fc0fa`

```dockerfile
```

-	Layers:
	-	`sha256:070f2bbece5473f2c0c55e418b792510a0febdefaba18480714cf7dc0da44524`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:00ace04168cdf245f42a3b4e51001be65d57b2688ba37ceb571c858367f82091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942ee14c16718cb6b226080a269139173f826f4c57756120cbabb10a04312a41`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831958881aa7c7363f4962a6a305dd34529b5a3b6f9fe34ea0c550a9a93123a`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:04f4203ae702f8e1b57048b7f4a4562fadedd65a9a8052c10c5da32881a66567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ade1f2cedf562271f325ad67e73e55747b1a3765d3cfc1376e87cfa671e8d4`

```dockerfile
```

-	Layers:
	-	`sha256:29172cfd963721f0ae26556bb1349dee2b0977a97ef6c34ef44f7ad4eeb9a594`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:fdf8115b60259ac2622bdde6924f704a6275feb0d6cd65e38f4aa7a571791656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd15e3d70e85b851f5786bcc5592cef3d495bd850f8f7cbcdc0ca7c700408b2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47da5cb15f63124b6ff2f092feb178a9029685c93134a876733691494c5cf9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:c2a87cab23bdc37d169c93959e3ec821a456c1680a6551a7f5cf61acf16280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86a55fa4e6f66b879978374fa109f719ada684dd8a92f7ccda530fcbc8737`

```dockerfile
```

-	Layers:
	-	`sha256:7568c1ce7de6a041e52b780d3fd8b6872d5da377f7ac920fca57449c782c748c`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:7baa159ac707369edf5af5b2c2b7c240c82bd34149b3260dceee7ad5638d53cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d4acd870d3458242a8422ca0164de8903a47ffd0780a6b728485e25dac57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:08 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df52bd1462bfd4be75daf7de0a883ef6e005cb317917ea033fc18ee8368eb7`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:5ff7a0dfeaa6f2d4722d44dd6c709280ee35981ac7914b9dbfe21f57553e8a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c64e47e3edc168434146e3dec0c50abffdc23b6ec839ab026d2b9f10ce86c8`

```dockerfile
```

-	Layers:
	-	`sha256:8c8467bb933eef06e5af049586ab2e9b851e9f07b23dc34a6533b00f8f1ddeff`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:eafac85ab07d22f58da852c2be738ffebf9a426771ae0f6bc3d77cc58818f398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:2a575d676756410fc6468bfc0cc88a737ca244f800345756bbfe3f51df7a26f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7a8652ac9a57d88b7b40e3468f37e97a13c6f83fdb55e5b3f4d501ed10cbba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f79ffd9ff103bc84a4800bd77e3a21a2b8aa5283bb96c8971b80bc0f0b1325`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 7.1 MB (7104675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7565af587bddcdc18a03e6d18c244de584dbbee0a1345791c5f92af76834e52f`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fd907441994b474d09f8910bae025fe95188bfac1759e8191422eb0806c011`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d9b67e61825abfcca68a09f5f2217e3f9f0795bcfd5ae6b25f56d4a4d76244de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e9861b72a9f751c02868a963b26d866e3ed901dc51bc7adcf8c2d2988ef18f`

```dockerfile
```

-	Layers:
	-	`sha256:3638b25e681bd6c5f215250ca0fdd8b3af5c729dcecee3cf902cc5377613f375`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1493f7a8377a4c8f6aa2255676a9abf26baa6454afe853563c3226fb29ee24f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f53595b626382736d722114880915656af1c69519b90cb0f988cccbe55e502e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81a6c31c98e9d23f13c3e1f907bead88c63e1da172c607f1cf5e98bf39b2cfb`  
		Last Modified: Tue, 14 Apr 2026 19:18:19 GMT  
		Size: 6.8 MB (6824527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e93485e87180b419b674b3eaaefe0fb6cb8149f771a85b32884d318565c5b0d`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab1cdedb45964719fb488c1020b53f079ddd692ec19aa9224bcd4185b2f44cf`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a55de7e7cbe420676cde9540a343d1477bea77e79079b607e4ed24f48a7f3ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3362d5291b6a280bab2b1508a6cd3d6d0f5dc5beafa83a4cd908c971e0c2dbc9`

```dockerfile
```

-	Layers:
	-	`sha256:b608191e207ea42ead772d1c93799d794f7bcaf6248843f91721426b28e54576`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:43d26a2a5012f9e5cbb5f3a569bec60a0f31caff9241f2bea12c55576b20b43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b907f2c013544f942a4b8eb34f5dd75ec12f99e82cd0354ff8076468f5bd4a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a506cbdb04d5f850a7e6d7efad2de37c9281f87153355ae9f158463b8863c16`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 6.8 MB (6813977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f012309da8651a720251bebe8d821117e4af8a880054b044d6f9b77cb9bbd`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30097ae043c1bed74c22084b0906018b9e291c295790a03eb6e3c9be52d0585d`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b21ee8f249ab3c650417c4b20f0a8f05ef07196d420c9f2c03ff12d4f870dc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b6611241f2f57bb7846e1cc9646e70116cfb3b87ea4b5edffbaf1fcefe58a`

```dockerfile
```

-	Layers:
	-	`sha256:dd1462a37a47fe62aa5690e6fd6caccf9edd80f3b23d4f1537ff421f2c1db1b2`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ddfc383507987a61ec6ad0842ce9bedfa1c0dc8b0b61e20bf66f4ea1891c963f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10651943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e62a2c6d295007873d27b02e9bfb4b0d35219b9d38537a45aafe2a781a7ef8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75374d2efd25789f733679c46deb8015d53a34ffc525b1a5be14458cfaa7c572`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 6.5 MB (6511455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0469dd7527f8e826ccbde70f8429eb6445d7f986f67412ce5e6fe4f5efe762a`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fd106169b64170292228a08cc598dd7086fd77cb227d8b493a9442da8f2f03`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c7745ae505e872b9e322bfc8b2f28d8d6f912d9cb77ef8fa4800676ff12f3e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040e174862b564526a86b8abfa14447199c7b3218c59218d695b784bff14213c`

```dockerfile
```

-	Layers:
	-	`sha256:c6ee43bf4bf2b5f9d032ec8ac9655bf3944c1926ec48a04662fddfe77bbba8d5`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:8177663ab814155404ddd225210e864a8db5f5bab6524fcd538e1c50e95b5ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c112147b37f5f3a82942b342ae66fbac493141594055744e01168da49832e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:23:16 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:23:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:23:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3016f09e58e2224328d6b41bb77318fceda5b54269054dde87e90e5c78a5850`  
		Last Modified: Tue, 14 Apr 2026 19:23:32 GMT  
		Size: 6.6 MB (6561426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac87bfa474f24897ae62b339e8d3e99d2477339cb9c7b9c9c27fe53e05575a`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5caa4d61a9b6f6e771c2817dc9c2d7f2b7737c8d5ba3352063ae308e6ba4bb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1076c83f11053262280ca29e78934d54c350126d3bf945008131c45e30051279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2883b8d290089c7ecab48a7da59f92c662d33b5b0eb9d670e0b0f444447fe585`

```dockerfile
```

-	Layers:
	-	`sha256:56648b6f8b6b7d991ee9afea4af9d02a29fed6e3de695d2669ff6a10e1c66ad2`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:0382580cb171a9ef5220b58d8f8476e825dd541e23ddd9261c83fe81077c687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10593579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbff052312601b8843e5c7f71ffd689bab23a0bbc6c559f906df56d2ab3ad4cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe3d8c0011da8faf0966aa9995120fdc77207edbfce2a78a12b7ffa0e66cdee`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 6.9 MB (6942178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db786c0b404f3ce6941db702d0a29b1f7f7a2da1f5178eb375ae02a6864fb69`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaae1336b66f9d4544d0dada462003e4b60143899cc7d520d196916b4b2a931`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6bfbfebce9888aad4a527e1f5b945818e5241836164846ce875432b1e6bba4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d469341abe6fbb7b778259a810bc75cf066eabd0da34b49bac83dc9b756113`

```dockerfile
```

-	Layers:
	-	`sha256:25df845b450fa255e51db23f7115c4c5986bcc435fb73ff38329d7f8bcebbd2e`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:eafac85ab07d22f58da852c2be738ffebf9a426771ae0f6bc3d77cc58818f398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:2a575d676756410fc6468bfc0cc88a737ca244f800345756bbfe3f51df7a26f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7a8652ac9a57d88b7b40e3468f37e97a13c6f83fdb55e5b3f4d501ed10cbba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f79ffd9ff103bc84a4800bd77e3a21a2b8aa5283bb96c8971b80bc0f0b1325`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 7.1 MB (7104675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7565af587bddcdc18a03e6d18c244de584dbbee0a1345791c5f92af76834e52f`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fd907441994b474d09f8910bae025fe95188bfac1759e8191422eb0806c011`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d9b67e61825abfcca68a09f5f2217e3f9f0795bcfd5ae6b25f56d4a4d76244de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e9861b72a9f751c02868a963b26d866e3ed901dc51bc7adcf8c2d2988ef18f`

```dockerfile
```

-	Layers:
	-	`sha256:3638b25e681bd6c5f215250ca0fdd8b3af5c729dcecee3cf902cc5377613f375`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:1493f7a8377a4c8f6aa2255676a9abf26baa6454afe853563c3226fb29ee24f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f53595b626382736d722114880915656af1c69519b90cb0f988cccbe55e502e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81a6c31c98e9d23f13c3e1f907bead88c63e1da172c607f1cf5e98bf39b2cfb`  
		Last Modified: Tue, 14 Apr 2026 19:18:19 GMT  
		Size: 6.8 MB (6824527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e93485e87180b419b674b3eaaefe0fb6cb8149f771a85b32884d318565c5b0d`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab1cdedb45964719fb488c1020b53f079ddd692ec19aa9224bcd4185b2f44cf`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a55de7e7cbe420676cde9540a343d1477bea77e79079b607e4ed24f48a7f3ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3362d5291b6a280bab2b1508a6cd3d6d0f5dc5beafa83a4cd908c971e0c2dbc9`

```dockerfile
```

-	Layers:
	-	`sha256:b608191e207ea42ead772d1c93799d794f7bcaf6248843f91721426b28e54576`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:43d26a2a5012f9e5cbb5f3a569bec60a0f31caff9241f2bea12c55576b20b43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b907f2c013544f942a4b8eb34f5dd75ec12f99e82cd0354ff8076468f5bd4a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a506cbdb04d5f850a7e6d7efad2de37c9281f87153355ae9f158463b8863c16`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 6.8 MB (6813977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f012309da8651a720251bebe8d821117e4af8a880054b044d6f9b77cb9bbd`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30097ae043c1bed74c22084b0906018b9e291c295790a03eb6e3c9be52d0585d`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b21ee8f249ab3c650417c4b20f0a8f05ef07196d420c9f2c03ff12d4f870dc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b6611241f2f57bb7846e1cc9646e70116cfb3b87ea4b5edffbaf1fcefe58a`

```dockerfile
```

-	Layers:
	-	`sha256:dd1462a37a47fe62aa5690e6fd6caccf9edd80f3b23d4f1537ff421f2c1db1b2`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ddfc383507987a61ec6ad0842ce9bedfa1c0dc8b0b61e20bf66f4ea1891c963f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10651943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e62a2c6d295007873d27b02e9bfb4b0d35219b9d38537a45aafe2a781a7ef8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75374d2efd25789f733679c46deb8015d53a34ffc525b1a5be14458cfaa7c572`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 6.5 MB (6511455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0469dd7527f8e826ccbde70f8429eb6445d7f986f67412ce5e6fe4f5efe762a`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fd106169b64170292228a08cc598dd7086fd77cb227d8b493a9442da8f2f03`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c7745ae505e872b9e322bfc8b2f28d8d6f912d9cb77ef8fa4800676ff12f3e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040e174862b564526a86b8abfa14447199c7b3218c59218d695b784bff14213c`

```dockerfile
```

-	Layers:
	-	`sha256:c6ee43bf4bf2b5f9d032ec8ac9655bf3944c1926ec48a04662fddfe77bbba8d5`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:8177663ab814155404ddd225210e864a8db5f5bab6524fcd538e1c50e95b5ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c112147b37f5f3a82942b342ae66fbac493141594055744e01168da49832e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:23:16 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:23:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:23:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3016f09e58e2224328d6b41bb77318fceda5b54269054dde87e90e5c78a5850`  
		Last Modified: Tue, 14 Apr 2026 19:23:32 GMT  
		Size: 6.6 MB (6561426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac87bfa474f24897ae62b339e8d3e99d2477339cb9c7b9c9c27fe53e05575a`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5caa4d61a9b6f6e771c2817dc9c2d7f2b7737c8d5ba3352063ae308e6ba4bb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:1076c83f11053262280ca29e78934d54c350126d3bf945008131c45e30051279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2883b8d290089c7ecab48a7da59f92c662d33b5b0eb9d670e0b0f444447fe585`

```dockerfile
```

-	Layers:
	-	`sha256:56648b6f8b6b7d991ee9afea4af9d02a29fed6e3de695d2669ff6a10e1c66ad2`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:0382580cb171a9ef5220b58d8f8476e825dd541e23ddd9261c83fe81077c687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10593579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbff052312601b8843e5c7f71ffd689bab23a0bbc6c559f906df56d2ab3ad4cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe3d8c0011da8faf0966aa9995120fdc77207edbfce2a78a12b7ffa0e66cdee`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 6.9 MB (6942178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db786c0b404f3ce6941db702d0a29b1f7f7a2da1f5178eb375ae02a6864fb69`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaae1336b66f9d4544d0dada462003e4b60143899cc7d520d196916b4b2a931`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6bfbfebce9888aad4a527e1f5b945818e5241836164846ce875432b1e6bba4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d469341abe6fbb7b778259a810bc75cf066eabd0da34b49bac83dc9b756113`

```dockerfile
```

-	Layers:
	-	`sha256:25df845b450fa255e51db23f7115c4c5986bcc435fb73ff38329d7f8bcebbd2e`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:d2b16b7517a2dd973e0999b071e016485a9a08c82b5369cc1ce858af54587e93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:ecb873658a349d84b05ab89ccdc9dc3d3153e45b1c32f344c56383cfe78090ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0247f7685ff68b4ae975febd9a287b05bfd142373a9ddeb8c2dac6bfbc859`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040b24667adc09216d21ad3439155962ccadd3d91a63d56b7da7fc06ee4af8d`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:248f347c9c2745bce92c2706cb33a87211172a8f8e92087fdc501d07f7b8de4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43eac3eec77ccc736e40ad70b7026f77225ac7e5837afeb1a08f32fdd7d0b93`

```dockerfile
```

-	Layers:
	-	`sha256:d702fbcd1bfaedd00e8319117145a6389d6ea5e0c82a9d42f3162b728faeb4e5`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6b0b00a37ddb7979ca235c35428c360669c9da2bcfa9233ae1ac9be85d0d4345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444254e21a5a8780d3528d8d19efbf156e2c5abdbb0cfe9788f1d1eedab18e2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:38 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1a6f37e82fee0dcce9cf7e8571403adb7ce8ca76666035b362c31649f4b2e`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:550334371afd2696f12dac3fd3739eea092ac27f6b0b773744e87d63aae577e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63dfea61fd8fa9fa90c1a671898c3ff2dc3edfc998eb6478ee5c9b3e5f33d7f`

```dockerfile
```

-	Layers:
	-	`sha256:958b223cfdb0c6fadea45187b0bf34bd7314cdb490d8581c32cd73f85ef90ae5`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:88aeaaa7e2045ccc03915e3f388f392216411e3fa768956ec3b12003643e8697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e37b72ad4a2af972471eebaedf8daa75a569452f35b1ab43ebe86fab23da376`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79c24a16cb2f9ad04dc2e860c74b6a0c8653d0340378eda7c4a9db7fac2f355`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b8ac0ce4a3228e54e91056d63c0aad4573821af86e16530e157710c2c2f48ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e7d98c930153daa0f647ce1a34edcfacc5ba63ac0cdbfab10485093d0fc0fa`

```dockerfile
```

-	Layers:
	-	`sha256:070f2bbece5473f2c0c55e418b792510a0febdefaba18480714cf7dc0da44524`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:00ace04168cdf245f42a3b4e51001be65d57b2688ba37ceb571c858367f82091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942ee14c16718cb6b226080a269139173f826f4c57756120cbabb10a04312a41`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831958881aa7c7363f4962a6a305dd34529b5a3b6f9fe34ea0c550a9a93123a`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:04f4203ae702f8e1b57048b7f4a4562fadedd65a9a8052c10c5da32881a66567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ade1f2cedf562271f325ad67e73e55747b1a3765d3cfc1376e87cfa671e8d4`

```dockerfile
```

-	Layers:
	-	`sha256:29172cfd963721f0ae26556bb1349dee2b0977a97ef6c34ef44f7ad4eeb9a594`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:fdf8115b60259ac2622bdde6924f704a6275feb0d6cd65e38f4aa7a571791656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd15e3d70e85b851f5786bcc5592cef3d495bd850f8f7cbcdc0ca7c700408b2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47da5cb15f63124b6ff2f092feb178a9029685c93134a876733691494c5cf9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c2a87cab23bdc37d169c93959e3ec821a456c1680a6551a7f5cf61acf16280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86a55fa4e6f66b879978374fa109f719ada684dd8a92f7ccda530fcbc8737`

```dockerfile
```

-	Layers:
	-	`sha256:7568c1ce7de6a041e52b780d3fd8b6872d5da377f7ac920fca57449c782c748c`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:7baa159ac707369edf5af5b2c2b7c240c82bd34149b3260dceee7ad5638d53cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d4acd870d3458242a8422ca0164de8903a47ffd0780a6b728485e25dac57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:08 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df52bd1462bfd4be75daf7de0a883ef6e005cb317917ea033fc18ee8368eb7`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5ff7a0dfeaa6f2d4722d44dd6c709280ee35981ac7914b9dbfe21f57553e8a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c64e47e3edc168434146e3dec0c50abffdc23b6ec839ab026d2b9f10ce86c8`

```dockerfile
```

-	Layers:
	-	`sha256:8c8467bb933eef06e5af049586ab2e9b851e9f07b23dc34a6533b00f8f1ddeff`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:d2b16b7517a2dd973e0999b071e016485a9a08c82b5369cc1ce858af54587e93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:ecb873658a349d84b05ab89ccdc9dc3d3153e45b1c32f344c56383cfe78090ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0247f7685ff68b4ae975febd9a287b05bfd142373a9ddeb8c2dac6bfbc859`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040b24667adc09216d21ad3439155962ccadd3d91a63d56b7da7fc06ee4af8d`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:248f347c9c2745bce92c2706cb33a87211172a8f8e92087fdc501d07f7b8de4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43eac3eec77ccc736e40ad70b7026f77225ac7e5837afeb1a08f32fdd7d0b93`

```dockerfile
```

-	Layers:
	-	`sha256:d702fbcd1bfaedd00e8319117145a6389d6ea5e0c82a9d42f3162b728faeb4e5`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:6b0b00a37ddb7979ca235c35428c360669c9da2bcfa9233ae1ac9be85d0d4345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444254e21a5a8780d3528d8d19efbf156e2c5abdbb0cfe9788f1d1eedab18e2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:38 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1a6f37e82fee0dcce9cf7e8571403adb7ce8ca76666035b362c31649f4b2e`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:550334371afd2696f12dac3fd3739eea092ac27f6b0b773744e87d63aae577e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63dfea61fd8fa9fa90c1a671898c3ff2dc3edfc998eb6478ee5c9b3e5f33d7f`

```dockerfile
```

-	Layers:
	-	`sha256:958b223cfdb0c6fadea45187b0bf34bd7314cdb490d8581c32cd73f85ef90ae5`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:88aeaaa7e2045ccc03915e3f388f392216411e3fa768956ec3b12003643e8697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e37b72ad4a2af972471eebaedf8daa75a569452f35b1ab43ebe86fab23da376`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79c24a16cb2f9ad04dc2e860c74b6a0c8653d0340378eda7c4a9db7fac2f355`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b8ac0ce4a3228e54e91056d63c0aad4573821af86e16530e157710c2c2f48ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e7d98c930153daa0f647ce1a34edcfacc5ba63ac0cdbfab10485093d0fc0fa`

```dockerfile
```

-	Layers:
	-	`sha256:070f2bbece5473f2c0c55e418b792510a0febdefaba18480714cf7dc0da44524`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:00ace04168cdf245f42a3b4e51001be65d57b2688ba37ceb571c858367f82091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942ee14c16718cb6b226080a269139173f826f4c57756120cbabb10a04312a41`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831958881aa7c7363f4962a6a305dd34529b5a3b6f9fe34ea0c550a9a93123a`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:04f4203ae702f8e1b57048b7f4a4562fadedd65a9a8052c10c5da32881a66567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ade1f2cedf562271f325ad67e73e55747b1a3765d3cfc1376e87cfa671e8d4`

```dockerfile
```

-	Layers:
	-	`sha256:29172cfd963721f0ae26556bb1349dee2b0977a97ef6c34ef44f7ad4eeb9a594`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:fdf8115b60259ac2622bdde6924f704a6275feb0d6cd65e38f4aa7a571791656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd15e3d70e85b851f5786bcc5592cef3d495bd850f8f7cbcdc0ca7c700408b2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47da5cb15f63124b6ff2f092feb178a9029685c93134a876733691494c5cf9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c2a87cab23bdc37d169c93959e3ec821a456c1680a6551a7f5cf61acf16280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86a55fa4e6f66b879978374fa109f719ada684dd8a92f7ccda530fcbc8737`

```dockerfile
```

-	Layers:
	-	`sha256:7568c1ce7de6a041e52b780d3fd8b6872d5da377f7ac920fca57449c782c748c`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:7baa159ac707369edf5af5b2c2b7c240c82bd34149b3260dceee7ad5638d53cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d4acd870d3458242a8422ca0164de8903a47ffd0780a6b728485e25dac57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:08 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df52bd1462bfd4be75daf7de0a883ef6e005cb317917ea033fc18ee8368eb7`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5ff7a0dfeaa6f2d4722d44dd6c709280ee35981ac7914b9dbfe21f57553e8a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c64e47e3edc168434146e3dec0c50abffdc23b6ec839ab026d2b9f10ce86c8`

```dockerfile
```

-	Layers:
	-	`sha256:8c8467bb933eef06e5af049586ab2e9b851e9f07b23dc34a6533b00f8f1ddeff`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:184cb774079b425716c5507364372954c455f9142c93d1bc466677ac2cc75ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:7790fa4d3db94cf7c89a7688f3f84537bb75287e452f1e554c1588a661d15cb1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077873124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a342bd15d69991f8343f2d756a7638e87fdfa2d5562cb647249e12b2bc09ae8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:06:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:06:25 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:06:26 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 21:06:26 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 21:06:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.7/nats-server-v2.12.7-windows-amd64.zip
# Tue, 14 Apr 2026 21:06:29 GMT
ENV NATS_SERVER_SHASUM=4e7880619018ccebe2aa9372a9a8bc362081a7414f93638143ea6d8049892146
# Tue, 14 Apr 2026 21:06:33 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Apr 2026 21:06:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Apr 2026 21:06:49 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:06:50 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:06:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:06:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234f0c5dc55953d98e0d13e9e881a65f871f8e0476a39dc8074be17e88c96ab`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e8f504a62653497a194c864fb383113d6df01412a46e631c3118b188201760`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d82249fabc12bddf45ee14ee15697a564705a6bae958426abd5f4e10bb35ed`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fce0a83450991329209dbbba5426b504eb424ca3c01086d950fe682844645f`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313c950879461faccbfdbe49b49b7ae9078f4f5f4440ac5d858ef0957df5ed6`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae88d9973cc6300fad7210fd6ceec8ad6f50c2a3521ea7a13d0dbd3039da44d6`  
		Last Modified: Tue, 14 Apr 2026 21:06:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5cbd1df81d61159af069584f9c11905a89d3b37b3bf4c04d8824003ec45c0`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 476.1 KB (476100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d18ee910801df31fa7a1ce17acaac50b7ec97bad952d423d008642554a5ebd9`  
		Last Modified: Tue, 14 Apr 2026 21:07:00 GMT  
		Size: 7.2 MB (7172018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd64f7fcdcc6dc03c3975a663297e49a35d229c0406f0ee49d954c76c7becb45`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.9 KB (1896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd424273b8b84b6ff389aa4eef9af352a6544807e63270647cc147eb2965112d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca72c491cc10f7581d8eb027dc3737bd51ab476833369bb5c2e9d80865d9521`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d050d88a8b0417554b75e53d2839e21fe0c82d7e9104c71eeb8648e9600fbe6d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:184cb774079b425716c5507364372954c455f9142c93d1bc466677ac2cc75ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:7790fa4d3db94cf7c89a7688f3f84537bb75287e452f1e554c1588a661d15cb1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077873124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a342bd15d69991f8343f2d756a7638e87fdfa2d5562cb647249e12b2bc09ae8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:06:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:06:25 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:06:26 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 21:06:26 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 21:06:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.7/nats-server-v2.12.7-windows-amd64.zip
# Tue, 14 Apr 2026 21:06:29 GMT
ENV NATS_SERVER_SHASUM=4e7880619018ccebe2aa9372a9a8bc362081a7414f93638143ea6d8049892146
# Tue, 14 Apr 2026 21:06:33 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Apr 2026 21:06:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Apr 2026 21:06:49 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:06:50 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:06:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:06:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234f0c5dc55953d98e0d13e9e881a65f871f8e0476a39dc8074be17e88c96ab`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e8f504a62653497a194c864fb383113d6df01412a46e631c3118b188201760`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d82249fabc12bddf45ee14ee15697a564705a6bae958426abd5f4e10bb35ed`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fce0a83450991329209dbbba5426b504eb424ca3c01086d950fe682844645f`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313c950879461faccbfdbe49b49b7ae9078f4f5f4440ac5d858ef0957df5ed6`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae88d9973cc6300fad7210fd6ceec8ad6f50c2a3521ea7a13d0dbd3039da44d6`  
		Last Modified: Tue, 14 Apr 2026 21:06:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5cbd1df81d61159af069584f9c11905a89d3b37b3bf4c04d8824003ec45c0`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 476.1 KB (476100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d18ee910801df31fa7a1ce17acaac50b7ec97bad952d423d008642554a5ebd9`  
		Last Modified: Tue, 14 Apr 2026 21:07:00 GMT  
		Size: 7.2 MB (7172018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd64f7fcdcc6dc03c3975a663297e49a35d229c0406f0ee49d954c76c7becb45`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.9 KB (1896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd424273b8b84b6ff389aa4eef9af352a6544807e63270647cc147eb2965112d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca72c491cc10f7581d8eb027dc3737bd51ab476833369bb5c2e9d80865d9521`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d050d88a8b0417554b75e53d2839e21fe0c82d7e9104c71eeb8648e9600fbe6d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11`

```console
$ docker pull nats@sha256:cbc2a07dfd6bc22f6dbadcb898666368dc58c5ec00f69b5aac0b72895f7e3647
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11` - linux; amd64

```console
$ docker pull nats@sha256:c2110151e63b453119fbd17e9fa64e44ab4ce07ed8a033c76a62946ddf6b614d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6497606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0910ab9e623cf3c8c8b450f1a8998c5a5d65ec923e9f5eae99682d370b0b7186`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:12 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9f0ebe5f9a1ae3ad639c8afca45fb722413353ade56a44dcf62bcfef80217dbb`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.5 MB (6497097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3aa31a58f3732fef628ef5de608085bbd9fd3cdd9ae1bc38476cd77e2a9f71`  
		Last Modified: Tue, 14 Apr 2026 20:10:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:b471dfd5308d245d31473ef6fb9a44d04609d7084d1f6435db514ae5b19507ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6307fe453094ab6bf3dce0a1a57c4de4ed82d0f95f3d7c2a3cbf20f5c340fdbd`

```dockerfile
```

-	Layers:
	-	`sha256:2fb63ea3ab9f0be3fad75526a8a808b092a7b8f97002d57208e5baebb694ae55`  
		Last Modified: Tue, 14 Apr 2026 20:10:17 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4be3c3c3593bfb53295d26f82732a468b64c6b3617882d3d2fc62e330c34de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d75ed8e27c246ac51767267210e1c5640347bbbd5ffee5b012eae91162ed0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:50 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:50 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:50 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:50 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ac4c14b3f8076df43f73c9299994bae9134a062823f58d1140353085aa0b300`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.2 MB (6218951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9a6f4ed2afcfd3f5f084fe6e276fb037b60aa6590560929719b278e20d99ce`  
		Last Modified: Tue, 14 Apr 2026 20:08:54 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:6e94f7dcea2fef9d27a13db5b1216d7d60556e18b11a035cc312a38cc1a6d778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c4d4fd8ad8fd7cfe4a5f9c7b009ed245033ce376e5e9d7823b2cac668c1d57`

```dockerfile
```

-	Layers:
	-	`sha256:fbb355648bd431a8b0977dfabf60aa9069152a7fb369e1753dcdf5e52f4fda24`  
		Last Modified: Tue, 14 Apr 2026 20:08:54 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:20c43ada29aca6f237ce383386788f0d32d50fc126ed43cbc1724d9567af8e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ff6e38918165fe195fd75349e870b96ce5ba4040e58d7f8f1ceb913da191ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:44:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:44:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:44:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:44:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:44:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:44:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2a83fab97c651eacbf830fb7bd159907e5e14fda32f73c5628adf6899c32f67f`  
		Last Modified: Tue, 14 Apr 2026 16:12:11 GMT  
		Size: 6.2 MB (6208591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa15cae9b1157772879677c602f41156691045d5965ccb813916810df1fe4bb4`  
		Last Modified: Tue, 14 Apr 2026 20:44:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:335859fd4ccfc83d33e49af0abb39046cb66161f6cb41b1d297e18185ed2d82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a3335340d60b379757a5475817b6f11fd4228353746af920b898da1d4f0c90`

```dockerfile
```

-	Layers:
	-	`sha256:380d6911889112f6fb63ea5b38cc214ae0c36fa9103d5b53716e58a52597aadd`  
		Last Modified: Tue, 14 Apr 2026 20:44:44 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abbaf279400efe50c75c001cadf65397a0d36585ee13cd93fa4c674f9f334610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c88001ed291a311398596c738f3953e284046e8cfb5a6fb942c2e6095fce1e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:16 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53e14ebbec1f96d7732d422be8ee7b587c333a423ac37b45d8cbe989c7ffe1ed`  
		Last Modified: Tue, 14 Apr 2026 16:12:13 GMT  
		Size: 5.9 MB (5915332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d21c1e4bfb6845681b40f88f6c360fd74dddbb4be86f32deb7bb7c967ed0b7`  
		Last Modified: Tue, 14 Apr 2026 20:10:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:028d2be5c52a686b2e055ce4b7a524268ad13fc1b2d441001a76941f17aad07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd94cfc134986b016c708bcfb838242037df4f5e4edf95655265bee2d16a4bd6`

```dockerfile
```

-	Layers:
	-	`sha256:95d6c9956af48d4e05152e7126a70c0a732bff4992493102b84da32c69ce796b`  
		Last Modified: Tue, 14 Apr 2026 20:10:20 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; ppc64le

```console
$ docker pull nats@sha256:1ebc5c2cf6b0fc3b0e50cc38afab77cfa688f8da4024fa99681f7611d8ac0f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8278b7cc91b73cd95f65829f426b3a56b62948c201cb02fc5939d2802f4cc8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b63ce4825759431170974b945ec1ddea7f5665ed75cc067dc0285b5ece42ed12`  
		Last Modified: Tue, 14 Apr 2026 16:12:12 GMT  
		Size: 6.0 MB (5964595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143e5f30d6fc7c65fa53e947ac6769436eb6e2dcc5c1a981230be9abadf9237e`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:e4fa323ebd6292cc230c999c0c58bb8e756bbcb73acdbe9be3dc2582f850b14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e1c8b35cc1455b27a2ad77da671aca7bec71cd4469a53bf630e9274c649c2f`

```dockerfile
```

-	Layers:
	-	`sha256:1719e1239afd7235ebf11aab5e250649cfa41f29f15712a458ade3c61492cd9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; s390x

```console
$ docker pull nats@sha256:a2cfef35bf670a3475a15ef1169a8f4f477958b389305df32f46ed369ffbc709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b772fdee82b6cf590b45d94f0cd27b548914f71d08ebb473f1ec4a387fca92f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:12 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7da88b0130848f05398873a2b9335b6391d3a2040acd810dc06d9574dbb2bb8`  
		Last Modified: Tue, 14 Apr 2026 20:09:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:6dc7f690e56d56df808c8db0ba100e6a24552f0896701b2a36567d46d6e23a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895583c3c619bee0ff187e28a90b2c58804aed9d323fc34f0ddd9fe29f40dbc0`

```dockerfile
```

-	Layers:
	-	`sha256:0d02a41a21d1ae4a3f92949bfa5bcdec8304d824bd5b40042199a8779d25bc7d`  
		Last Modified: Tue, 14 Apr 2026 20:09:20 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:5ffa3167d5e3e3fd4258586b3e58689d9ca02a145f6b5cbc6a82f8416b7c61e3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133637234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29654dc94df41eabc4fec5c6267f3e71846d39bd31cc97f52dd46404020ce98`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:52 GMT
RUN cmd /S /C #(nop) COPY file:f1ed4e18be63052ebd2a9f8f87593bf079db370ff176ea712b36dc2ac83ea376 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:54 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed04d46136c3797ba3fc4ddcaceedae8a6fc3fd40e4f77f0929591c7b645a51`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db2f5a47ed51a8fd3b8ccbc37ae5b9d89766a7cd30ac5138fc1abab63a8917e`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 6.7 MB (6675280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd0b5b898034b9675ff6aa86b1a3b107c8ca3cc2788fca25c8f4f1ff65c4840`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823643c2dcd9d2a19ef822365ba3d59a932d0f663749945aec1c1fb74a7fff98`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2286cfe5bab4a54ba713d5f92768b2ecfd0a029b275ba96d7b2c6dcca57056c6`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4274ef274b88859bdfe852c4c36f18d9eca26a752f7d521c3ee89749b253221`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:7f94277277e89fc16f3f5a4633786b700679170007dad41cfdef0a0d458181cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-alpine` - linux; amd64

```console
$ docker pull nats@sha256:b63d3a4c4b096a5b8aee698ffccf8ca001a857480d17dfecfb2acedfa331dd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10761772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0da8c22287d4e8c8b517b9964eabae67ee0490bf659766a6243afc39202b424`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:55 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:17:55 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:17:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f4d65993bf1d7a5b112c64d702118106b5745f06c6aec17b9b9c128a72b0b`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 7.0 MB (6955927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507d1402650f69b68b2e36b453f5aab0b2b8db1a4f8bb739ae03d4fafeb0e1ff`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b06ed42e02408e874a121a6e7e3e71875595a58ce02f8f0e4f3864138aeccb5`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:58330e58d92710af2e527e0f53719594416285eea76656f1ca4151399b34fd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b02aacc3dc69202e57431ff1dc33441decf3731fc9b1f53ed32ad43d1e972a7`

```dockerfile
```

-	Layers:
	-	`sha256:2ca807165446d4e9d1d6a6d55c43a4b45bedf2e726f767d73acca2788652a923`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:2c1a54648ee8363c187d7e9cd4906eb5e84b6cf1c8f52909fe63bed73f0d3415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10181356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6d7718f62effe9f15c7d396f4385a3aa5688b1cb038df30365cc902714b0c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:41 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:18:41 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:18:41 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:41 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:41 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b21e1551199aaabe96bd6470249e52fe24403fa35c793649ffaf57e2be3afda`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 6.7 MB (6675341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f736f2cddf61123f514302e6c81c49f18254a1a43288596e04166fda82e301`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27c4f6c7e2706bcd0356aed93cf8ab1b5284438519aee8fcbc357511b770657`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ec48a5a37c3c6e64d467e1a5d89dacae513127fda305853965de4ecd82ca22c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa91d0c123eb472e3619e73cc11c2c58c0856355eedaede9dea2fa8a506921a`

```dockerfile
```

-	Layers:
	-	`sha256:e40bb7eea2e90b7b0f6a52b11d4c9347be60d3e47e0c30dbe4161676c8d3d535`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:31a6e7deb249b86a8f878129462563f8cf0af0c0873a79bcc29a64c02e3ec244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9892913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad532990e4c0ecfddc9989329e28af97213b9060533f8065296b959af1352ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:44 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:18:44 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:18:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:44 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:44 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86089bb885556e0e27177c70e0e8f24d65dfd9c1f056a24d1dda1f23fad18bd`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 6.7 MB (6668316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a59172091a849e6b576bb25e5049f3c5b7a211845bd0a3ea5d9e6bb6ad55569`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca319357a73b41fa3d463244c39665508ac9efbdb21773f3cc22b9816e522cdc`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:38d16725794fb492177bd3f9a9111b4bb20683fa9a166f5186818159ff5be989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d7f09af972d51fc935e39738db1d4a8caefa8b885a8f75e87e59cecb19dd5f`

```dockerfile
```

-	Layers:
	-	`sha256:ab214d3d1838f37d03cc24cbb0d3f9b6d2a56e90bf57f1e354739af2e261d46f`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1d9049ae318c5ca83b7685a8e94df86dc1c10ad858bf90759c8fae8019da9906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce88ba66d2a0276da1939f036514e6ca0ef90e98f221bf589f5b51afae026e7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:39 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:18:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:18:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:39 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7566471ec2e31f581c1fa6cf70bc93bf2a5a83568ef458a6eccdcc18295829f2`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 6.4 MB (6376343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819bc5a8128d9ecefa58495dc2001c47adc63afb013680d86ad71f524d49fb9a`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b4d9008cd0aed6dfd8dfd2fdaee1ab5cde830217b117405b388e6ef086a507`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1a40022484327e18ecdb0d1cbcf301fe7a04e0adb9bfaa596744cfdf7999d634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de9fa3beefafe36b5b72f66f11d4394dff2966172cf342e1764da19456d7a09`

```dockerfile
```

-	Layers:
	-	`sha256:ab7a33235df45e0b1bf6d870b24254b5c242d74e824ac98ce0b4e4777382b804`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:bfd9ed6c2e3965b057b674b17430c808399842287e23c9ab829ca30ce0c99369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10161835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0688bcfd19c4c883dfd4b52ef841748aa4f6d677900eead71540a330b20a600b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:23:16 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:23:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:23:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:23:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:23:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eedd38afc716f975cb2e891febac979941155f68a06f2ce2837de197955b813`  
		Last Modified: Tue, 14 Apr 2026 19:23:32 GMT  
		Size: 6.4 MB (6426566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac87bfa474f24897ae62b339e8d3e99d2477339cb9c7b9c9c27fe53e05575a`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5caa4d61a9b6f6e771c2817dc9c2d7f2b7737c8d5ba3352063ae308e6ba4bb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:dab9fcf5b55a32afb30979fa8c0cff63488786bcfdf5ae87d615ec7a7ed315c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f71f7de20b524e074c54be6fec078361d34a0f7686f583ef1242033283c2eaf`

```dockerfile
```

-	Layers:
	-	`sha256:64634cc116b7317798b65dd8d668d7b2b361f349320365d7bec44b08760d0aeb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:0033b9a24a893eaa753fa356652316843d45167ac6f338fa3097cce110bc9b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10449885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e5287372a06705e1befee77a0e18b289b4e0adf15ed3331209105dff253a90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:17:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:17:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:38 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb45f6557a69c491c09b306884852b4012fc69ad197a919c63e020f9569a591`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 6.8 MB (6798483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0285f9e4fa1fd20d08ae7535e92e1bccca5487085129b19e2911596c22c06b`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908a1c7e17ce2f5731370d6d0f0ae8ed31a1763953ab3b68105604dab44a56f7`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:411ec8a8b2e7dafef4400f8b7f3dac28d374d80bec9a94772de6cb73533ca9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aafbbd6fcc4a17826f55623e55cc67c9523de3a312fa7078052f20630abe2f`

```dockerfile
```

-	Layers:
	-	`sha256:fc6cd0442a0cf11748f61eedb8eb8009c2c2cbd966e458c5a8b5e1c82ff20891`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.22`

```console
$ docker pull nats@sha256:7f94277277e89fc16f3f5a4633786b700679170007dad41cfdef0a0d458181cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:b63d3a4c4b096a5b8aee698ffccf8ca001a857480d17dfecfb2acedfa331dd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10761772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0da8c22287d4e8c8b517b9964eabae67ee0490bf659766a6243afc39202b424`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:55 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:17:55 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:17:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f4d65993bf1d7a5b112c64d702118106b5745f06c6aec17b9b9c128a72b0b`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 7.0 MB (6955927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507d1402650f69b68b2e36b453f5aab0b2b8db1a4f8bb739ae03d4fafeb0e1ff`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b06ed42e02408e874a121a6e7e3e71875595a58ce02f8f0e4f3864138aeccb5`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:58330e58d92710af2e527e0f53719594416285eea76656f1ca4151399b34fd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b02aacc3dc69202e57431ff1dc33441decf3731fc9b1f53ed32ad43d1e972a7`

```dockerfile
```

-	Layers:
	-	`sha256:2ca807165446d4e9d1d6a6d55c43a4b45bedf2e726f767d73acca2788652a923`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:2c1a54648ee8363c187d7e9cd4906eb5e84b6cf1c8f52909fe63bed73f0d3415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10181356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6d7718f62effe9f15c7d396f4385a3aa5688b1cb038df30365cc902714b0c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:41 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:18:41 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:18:41 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:41 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:41 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b21e1551199aaabe96bd6470249e52fe24403fa35c793649ffaf57e2be3afda`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 6.7 MB (6675341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f736f2cddf61123f514302e6c81c49f18254a1a43288596e04166fda82e301`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27c4f6c7e2706bcd0356aed93cf8ab1b5284438519aee8fcbc357511b770657`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ec48a5a37c3c6e64d467e1a5d89dacae513127fda305853965de4ecd82ca22c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa91d0c123eb472e3619e73cc11c2c58c0856355eedaede9dea2fa8a506921a`

```dockerfile
```

-	Layers:
	-	`sha256:e40bb7eea2e90b7b0f6a52b11d4c9347be60d3e47e0c30dbe4161676c8d3d535`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:31a6e7deb249b86a8f878129462563f8cf0af0c0873a79bcc29a64c02e3ec244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9892913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad532990e4c0ecfddc9989329e28af97213b9060533f8065296b959af1352ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:44 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:18:44 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:18:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:44 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:44 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86089bb885556e0e27177c70e0e8f24d65dfd9c1f056a24d1dda1f23fad18bd`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 6.7 MB (6668316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a59172091a849e6b576bb25e5049f3c5b7a211845bd0a3ea5d9e6bb6ad55569`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca319357a73b41fa3d463244c39665508ac9efbdb21773f3cc22b9816e522cdc`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:38d16725794fb492177bd3f9a9111b4bb20683fa9a166f5186818159ff5be989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d7f09af972d51fc935e39738db1d4a8caefa8b885a8f75e87e59cecb19dd5f`

```dockerfile
```

-	Layers:
	-	`sha256:ab214d3d1838f37d03cc24cbb0d3f9b6d2a56e90bf57f1e354739af2e261d46f`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1d9049ae318c5ca83b7685a8e94df86dc1c10ad858bf90759c8fae8019da9906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce88ba66d2a0276da1939f036514e6ca0ef90e98f221bf589f5b51afae026e7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:39 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:18:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:18:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:39 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7566471ec2e31f581c1fa6cf70bc93bf2a5a83568ef458a6eccdcc18295829f2`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 6.4 MB (6376343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819bc5a8128d9ecefa58495dc2001c47adc63afb013680d86ad71f524d49fb9a`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b4d9008cd0aed6dfd8dfd2fdaee1ab5cde830217b117405b388e6ef086a507`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:1a40022484327e18ecdb0d1cbcf301fe7a04e0adb9bfaa596744cfdf7999d634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de9fa3beefafe36b5b72f66f11d4394dff2966172cf342e1764da19456d7a09`

```dockerfile
```

-	Layers:
	-	`sha256:ab7a33235df45e0b1bf6d870b24254b5c242d74e824ac98ce0b4e4777382b804`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:bfd9ed6c2e3965b057b674b17430c808399842287e23c9ab829ca30ce0c99369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10161835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0688bcfd19c4c883dfd4b52ef841748aa4f6d677900eead71540a330b20a600b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:23:16 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:23:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:23:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:23:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:23:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eedd38afc716f975cb2e891febac979941155f68a06f2ce2837de197955b813`  
		Last Modified: Tue, 14 Apr 2026 19:23:32 GMT  
		Size: 6.4 MB (6426566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac87bfa474f24897ae62b339e8d3e99d2477339cb9c7b9c9c27fe53e05575a`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5caa4d61a9b6f6e771c2817dc9c2d7f2b7737c8d5ba3352063ae308e6ba4bb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:dab9fcf5b55a32afb30979fa8c0cff63488786bcfdf5ae87d615ec7a7ed315c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f71f7de20b524e074c54be6fec078361d34a0f7686f583ef1242033283c2eaf`

```dockerfile
```

-	Layers:
	-	`sha256:64634cc116b7317798b65dd8d668d7b2b361f349320365d7bec44b08760d0aeb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:0033b9a24a893eaa753fa356652316843d45167ac6f338fa3097cce110bc9b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10449885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e5287372a06705e1befee77a0e18b289b4e0adf15ed3331209105dff253a90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:17:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:17:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:38 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb45f6557a69c491c09b306884852b4012fc69ad197a919c63e020f9569a591`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 6.8 MB (6798483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0285f9e4fa1fd20d08ae7535e92e1bccca5487085129b19e2911596c22c06b`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908a1c7e17ce2f5731370d6d0f0ae8ed31a1763953ab3b68105604dab44a56f7`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:411ec8a8b2e7dafef4400f8b7f3dac28d374d80bec9a94772de6cb73533ca9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aafbbd6fcc4a17826f55623e55cc67c9523de3a312fa7078052f20630abe2f`

```dockerfile
```

-	Layers:
	-	`sha256:fc6cd0442a0cf11748f61eedb8eb8009c2c2cbd966e458c5a8b5e1c82ff20891`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

```console
$ docker pull nats@sha256:7a65060f41a558780b2bc5ec0049838bf914fff16361174609c1bf69ff240fe6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-linux` - linux; amd64

```console
$ docker pull nats@sha256:c2110151e63b453119fbd17e9fa64e44ab4ce07ed8a033c76a62946ddf6b614d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6497606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0910ab9e623cf3c8c8b450f1a8998c5a5d65ec923e9f5eae99682d370b0b7186`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:12 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9f0ebe5f9a1ae3ad639c8afca45fb722413353ade56a44dcf62bcfef80217dbb`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.5 MB (6497097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3aa31a58f3732fef628ef5de608085bbd9fd3cdd9ae1bc38476cd77e2a9f71`  
		Last Modified: Tue, 14 Apr 2026 20:10:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b471dfd5308d245d31473ef6fb9a44d04609d7084d1f6435db514ae5b19507ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6307fe453094ab6bf3dce0a1a57c4de4ed82d0f95f3d7c2a3cbf20f5c340fdbd`

```dockerfile
```

-	Layers:
	-	`sha256:2fb63ea3ab9f0be3fad75526a8a808b092a7b8f97002d57208e5baebb694ae55`  
		Last Modified: Tue, 14 Apr 2026 20:10:17 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4be3c3c3593bfb53295d26f82732a468b64c6b3617882d3d2fc62e330c34de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d75ed8e27c246ac51767267210e1c5640347bbbd5ffee5b012eae91162ed0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:50 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:50 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:50 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:50 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ac4c14b3f8076df43f73c9299994bae9134a062823f58d1140353085aa0b300`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.2 MB (6218951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9a6f4ed2afcfd3f5f084fe6e276fb037b60aa6590560929719b278e20d99ce`  
		Last Modified: Tue, 14 Apr 2026 20:08:54 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6e94f7dcea2fef9d27a13db5b1216d7d60556e18b11a035cc312a38cc1a6d778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c4d4fd8ad8fd7cfe4a5f9c7b009ed245033ce376e5e9d7823b2cac668c1d57`

```dockerfile
```

-	Layers:
	-	`sha256:fbb355648bd431a8b0977dfabf60aa9069152a7fb369e1753dcdf5e52f4fda24`  
		Last Modified: Tue, 14 Apr 2026 20:08:54 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:20c43ada29aca6f237ce383386788f0d32d50fc126ed43cbc1724d9567af8e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ff6e38918165fe195fd75349e870b96ce5ba4040e58d7f8f1ceb913da191ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:44:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:44:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:44:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:44:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:44:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:44:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2a83fab97c651eacbf830fb7bd159907e5e14fda32f73c5628adf6899c32f67f`  
		Last Modified: Tue, 14 Apr 2026 16:12:11 GMT  
		Size: 6.2 MB (6208591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa15cae9b1157772879677c602f41156691045d5965ccb813916810df1fe4bb4`  
		Last Modified: Tue, 14 Apr 2026 20:44:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:335859fd4ccfc83d33e49af0abb39046cb66161f6cb41b1d297e18185ed2d82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a3335340d60b379757a5475817b6f11fd4228353746af920b898da1d4f0c90`

```dockerfile
```

-	Layers:
	-	`sha256:380d6911889112f6fb63ea5b38cc214ae0c36fa9103d5b53716e58a52597aadd`  
		Last Modified: Tue, 14 Apr 2026 20:44:44 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abbaf279400efe50c75c001cadf65397a0d36585ee13cd93fa4c674f9f334610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c88001ed291a311398596c738f3953e284046e8cfb5a6fb942c2e6095fce1e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:16 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53e14ebbec1f96d7732d422be8ee7b587c333a423ac37b45d8cbe989c7ffe1ed`  
		Last Modified: Tue, 14 Apr 2026 16:12:13 GMT  
		Size: 5.9 MB (5915332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d21c1e4bfb6845681b40f88f6c360fd74dddbb4be86f32deb7bb7c967ed0b7`  
		Last Modified: Tue, 14 Apr 2026 20:10:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:028d2be5c52a686b2e055ce4b7a524268ad13fc1b2d441001a76941f17aad07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd94cfc134986b016c708bcfb838242037df4f5e4edf95655265bee2d16a4bd6`

```dockerfile
```

-	Layers:
	-	`sha256:95d6c9956af48d4e05152e7126a70c0a732bff4992493102b84da32c69ce796b`  
		Last Modified: Tue, 14 Apr 2026 20:10:20 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:1ebc5c2cf6b0fc3b0e50cc38afab77cfa688f8da4024fa99681f7611d8ac0f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8278b7cc91b73cd95f65829f426b3a56b62948c201cb02fc5939d2802f4cc8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b63ce4825759431170974b945ec1ddea7f5665ed75cc067dc0285b5ece42ed12`  
		Last Modified: Tue, 14 Apr 2026 16:12:12 GMT  
		Size: 6.0 MB (5964595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143e5f30d6fc7c65fa53e947ac6769436eb6e2dcc5c1a981230be9abadf9237e`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e4fa323ebd6292cc230c999c0c58bb8e756bbcb73acdbe9be3dc2582f850b14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e1c8b35cc1455b27a2ad77da671aca7bec71cd4469a53bf630e9274c649c2f`

```dockerfile
```

-	Layers:
	-	`sha256:1719e1239afd7235ebf11aab5e250649cfa41f29f15712a458ade3c61492cd9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:a2cfef35bf670a3475a15ef1169a8f4f477958b389305df32f46ed369ffbc709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b772fdee82b6cf590b45d94f0cd27b548914f71d08ebb473f1ec4a387fca92f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:12 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7da88b0130848f05398873a2b9335b6391d3a2040acd810dc06d9574dbb2bb8`  
		Last Modified: Tue, 14 Apr 2026 20:09:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6dc7f690e56d56df808c8db0ba100e6a24552f0896701b2a36567d46d6e23a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895583c3c619bee0ff187e28a90b2c58804aed9d323fc34f0ddd9fe29f40dbc0`

```dockerfile
```

-	Layers:
	-	`sha256:0d02a41a21d1ae4a3f92949bfa5bcdec8304d824bd5b40042199a8779d25bc7d`  
		Last Modified: Tue, 14 Apr 2026 20:09:20 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-nanoserver`

```console
$ docker pull nats@sha256:8369f10fa05d956de0096a7a744a1b1d55175a37c2841087081423b4165fae7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:5ffa3167d5e3e3fd4258586b3e58689d9ca02a145f6b5cbc6a82f8416b7c61e3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133637234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29654dc94df41eabc4fec5c6267f3e71846d39bd31cc97f52dd46404020ce98`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:52 GMT
RUN cmd /S /C #(nop) COPY file:f1ed4e18be63052ebd2a9f8f87593bf079db370ff176ea712b36dc2ac83ea376 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:54 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed04d46136c3797ba3fc4ddcaceedae8a6fc3fd40e4f77f0929591c7b645a51`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db2f5a47ed51a8fd3b8ccbc37ae5b9d89766a7cd30ac5138fc1abab63a8917e`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 6.7 MB (6675280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd0b5b898034b9675ff6aa86b1a3b107c8ca3cc2788fca25c8f4f1ff65c4840`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823643c2dcd9d2a19ef822365ba3d59a932d0f663749945aec1c1fb74a7fff98`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2286cfe5bab4a54ba713d5f92768b2ecfd0a029b275ba96d7b2c6dcca57056c6`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4274ef274b88859bdfe852c4c36f18d9eca26a752f7d521c3ee89749b253221`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:8369f10fa05d956de0096a7a744a1b1d55175a37c2841087081423b4165fae7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:5ffa3167d5e3e3fd4258586b3e58689d9ca02a145f6b5cbc6a82f8416b7c61e3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133637234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29654dc94df41eabc4fec5c6267f3e71846d39bd31cc97f52dd46404020ce98`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:52 GMT
RUN cmd /S /C #(nop) COPY file:f1ed4e18be63052ebd2a9f8f87593bf079db370ff176ea712b36dc2ac83ea376 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:54 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed04d46136c3797ba3fc4ddcaceedae8a6fc3fd40e4f77f0929591c7b645a51`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db2f5a47ed51a8fd3b8ccbc37ae5b9d89766a7cd30ac5138fc1abab63a8917e`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 6.7 MB (6675280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd0b5b898034b9675ff6aa86b1a3b107c8ca3cc2788fca25c8f4f1ff65c4840`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823643c2dcd9d2a19ef822365ba3d59a932d0f663749945aec1c1fb74a7fff98`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2286cfe5bab4a54ba713d5f92768b2ecfd0a029b275ba96d7b2c6dcca57056c6`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4274ef274b88859bdfe852c4c36f18d9eca26a752f7d521c3ee89749b253221`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-scratch`

```console
$ docker pull nats@sha256:7a65060f41a558780b2bc5ec0049838bf914fff16361174609c1bf69ff240fe6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-scratch` - linux; amd64

```console
$ docker pull nats@sha256:c2110151e63b453119fbd17e9fa64e44ab4ce07ed8a033c76a62946ddf6b614d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6497606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0910ab9e623cf3c8c8b450f1a8998c5a5d65ec923e9f5eae99682d370b0b7186`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:12 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9f0ebe5f9a1ae3ad639c8afca45fb722413353ade56a44dcf62bcfef80217dbb`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.5 MB (6497097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3aa31a58f3732fef628ef5de608085bbd9fd3cdd9ae1bc38476cd77e2a9f71`  
		Last Modified: Tue, 14 Apr 2026 20:10:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b471dfd5308d245d31473ef6fb9a44d04609d7084d1f6435db514ae5b19507ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6307fe453094ab6bf3dce0a1a57c4de4ed82d0f95f3d7c2a3cbf20f5c340fdbd`

```dockerfile
```

-	Layers:
	-	`sha256:2fb63ea3ab9f0be3fad75526a8a808b092a7b8f97002d57208e5baebb694ae55`  
		Last Modified: Tue, 14 Apr 2026 20:10:17 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4be3c3c3593bfb53295d26f82732a468b64c6b3617882d3d2fc62e330c34de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d75ed8e27c246ac51767267210e1c5640347bbbd5ffee5b012eae91162ed0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:50 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:50 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:50 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:50 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ac4c14b3f8076df43f73c9299994bae9134a062823f58d1140353085aa0b300`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.2 MB (6218951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9a6f4ed2afcfd3f5f084fe6e276fb037b60aa6590560929719b278e20d99ce`  
		Last Modified: Tue, 14 Apr 2026 20:08:54 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6e94f7dcea2fef9d27a13db5b1216d7d60556e18b11a035cc312a38cc1a6d778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c4d4fd8ad8fd7cfe4a5f9c7b009ed245033ce376e5e9d7823b2cac668c1d57`

```dockerfile
```

-	Layers:
	-	`sha256:fbb355648bd431a8b0977dfabf60aa9069152a7fb369e1753dcdf5e52f4fda24`  
		Last Modified: Tue, 14 Apr 2026 20:08:54 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:20c43ada29aca6f237ce383386788f0d32d50fc126ed43cbc1724d9567af8e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ff6e38918165fe195fd75349e870b96ce5ba4040e58d7f8f1ceb913da191ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:44:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:44:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:44:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:44:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:44:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:44:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2a83fab97c651eacbf830fb7bd159907e5e14fda32f73c5628adf6899c32f67f`  
		Last Modified: Tue, 14 Apr 2026 16:12:11 GMT  
		Size: 6.2 MB (6208591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa15cae9b1157772879677c602f41156691045d5965ccb813916810df1fe4bb4`  
		Last Modified: Tue, 14 Apr 2026 20:44:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:335859fd4ccfc83d33e49af0abb39046cb66161f6cb41b1d297e18185ed2d82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a3335340d60b379757a5475817b6f11fd4228353746af920b898da1d4f0c90`

```dockerfile
```

-	Layers:
	-	`sha256:380d6911889112f6fb63ea5b38cc214ae0c36fa9103d5b53716e58a52597aadd`  
		Last Modified: Tue, 14 Apr 2026 20:44:44 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abbaf279400efe50c75c001cadf65397a0d36585ee13cd93fa4c674f9f334610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c88001ed291a311398596c738f3953e284046e8cfb5a6fb942c2e6095fce1e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:16 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53e14ebbec1f96d7732d422be8ee7b587c333a423ac37b45d8cbe989c7ffe1ed`  
		Last Modified: Tue, 14 Apr 2026 16:12:13 GMT  
		Size: 5.9 MB (5915332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d21c1e4bfb6845681b40f88f6c360fd74dddbb4be86f32deb7bb7c967ed0b7`  
		Last Modified: Tue, 14 Apr 2026 20:10:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:028d2be5c52a686b2e055ce4b7a524268ad13fc1b2d441001a76941f17aad07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd94cfc134986b016c708bcfb838242037df4f5e4edf95655265bee2d16a4bd6`

```dockerfile
```

-	Layers:
	-	`sha256:95d6c9956af48d4e05152e7126a70c0a732bff4992493102b84da32c69ce796b`  
		Last Modified: Tue, 14 Apr 2026 20:10:20 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:1ebc5c2cf6b0fc3b0e50cc38afab77cfa688f8da4024fa99681f7611d8ac0f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8278b7cc91b73cd95f65829f426b3a56b62948c201cb02fc5939d2802f4cc8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b63ce4825759431170974b945ec1ddea7f5665ed75cc067dc0285b5ece42ed12`  
		Last Modified: Tue, 14 Apr 2026 16:12:12 GMT  
		Size: 6.0 MB (5964595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143e5f30d6fc7c65fa53e947ac6769436eb6e2dcc5c1a981230be9abadf9237e`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e4fa323ebd6292cc230c999c0c58bb8e756bbcb73acdbe9be3dc2582f850b14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e1c8b35cc1455b27a2ad77da671aca7bec71cd4469a53bf630e9274c649c2f`

```dockerfile
```

-	Layers:
	-	`sha256:1719e1239afd7235ebf11aab5e250649cfa41f29f15712a458ade3c61492cd9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:a2cfef35bf670a3475a15ef1169a8f4f477958b389305df32f46ed369ffbc709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b772fdee82b6cf590b45d94f0cd27b548914f71d08ebb473f1ec4a387fca92f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:12 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7da88b0130848f05398873a2b9335b6391d3a2040acd810dc06d9574dbb2bb8`  
		Last Modified: Tue, 14 Apr 2026 20:09:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6dc7f690e56d56df808c8db0ba100e6a24552f0896701b2a36567d46d6e23a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895583c3c619bee0ff187e28a90b2c58804aed9d323fc34f0ddd9fe29f40dbc0`

```dockerfile
```

-	Layers:
	-	`sha256:0d02a41a21d1ae4a3f92949bfa5bcdec8304d824bd5b40042199a8779d25bc7d`  
		Last Modified: Tue, 14 Apr 2026 20:09:20 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-windowsservercore`

```console
$ docker pull nats@sha256:0fab64367d01a89d9933f0c222c927c5b6199e3ededca344283d796b7ff2afa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:3b61953057c6c60d9800b8453169f6396d3cf533fe54e4c48ef7158413042717
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077722942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef93dc3bf8a5885439b286e78880586afe506977de79802da64c1fff0455078`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:06:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:06:25 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:07:15 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 21:07:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 21:07:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.16/nats-server-v2.11.16-windows-amd64.zip
# Tue, 14 Apr 2026 21:07:16 GMT
ENV NATS_SERVER_SHASUM=8371464b7c604e45a21efd0fb754849defcf86419994d79b5d0f2547b39171b7
# Tue, 14 Apr 2026 21:07:21 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Apr 2026 21:07:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Apr 2026 21:07:37 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:07:38 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:07:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:07:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234f0c5dc55953d98e0d13e9e881a65f871f8e0476a39dc8074be17e88c96ab`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e8f504a62653497a194c864fb383113d6df01412a46e631c3118b188201760`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a25322b4e8a70bd21a23374e7a44f4d3e0bf91d86a709f87c1e0e41b5c34630`  
		Last Modified: Tue, 14 Apr 2026 21:07:48 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6508587f65ad7bc80506629c5050f641a67b576390527bd50028d116a6e59e`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7e4b16927cdba1f56bfd47ee4f0ec91f03eb4d54665950de0e690a8cf591a7`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1e6f397ed251ea4fa0fb49b33654ae0a4f21051946b31de5b6298d957e07df`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bd7d3b9f81e641b929a92168f2988f89f7d48ff296f269386fa26ee6004909`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 479.0 KB (479045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a93be0fe778d54bf31dbf755152bca8e716fe3b4a6a26a6363bf6eefb86f0c`  
		Last Modified: Tue, 14 Apr 2026 21:07:48 GMT  
		Size: 7.0 MB (7018960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6f1157c852a3b84dc8acc8da41f4341b89ad594de182595b028d6cfc5cc59`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b986f7ba00c261673bec4ea3a233599f672f19ee33681b8e984c027d03cf366`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfefa8af6da8003b32230316fcacc30569cbe0a4231b6f6e19a2b68fe7ba5ae8`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f7ff6f050a295adfee7c011b0dee2b54a41677aa16389632062d6bb6b5a6ee`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:0fab64367d01a89d9933f0c222c927c5b6199e3ededca344283d796b7ff2afa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:3b61953057c6c60d9800b8453169f6396d3cf533fe54e4c48ef7158413042717
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077722942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef93dc3bf8a5885439b286e78880586afe506977de79802da64c1fff0455078`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:06:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:06:25 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:07:15 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 21:07:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 21:07:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.16/nats-server-v2.11.16-windows-amd64.zip
# Tue, 14 Apr 2026 21:07:16 GMT
ENV NATS_SERVER_SHASUM=8371464b7c604e45a21efd0fb754849defcf86419994d79b5d0f2547b39171b7
# Tue, 14 Apr 2026 21:07:21 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Apr 2026 21:07:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Apr 2026 21:07:37 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:07:38 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:07:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:07:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234f0c5dc55953d98e0d13e9e881a65f871f8e0476a39dc8074be17e88c96ab`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e8f504a62653497a194c864fb383113d6df01412a46e631c3118b188201760`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a25322b4e8a70bd21a23374e7a44f4d3e0bf91d86a709f87c1e0e41b5c34630`  
		Last Modified: Tue, 14 Apr 2026 21:07:48 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6508587f65ad7bc80506629c5050f641a67b576390527bd50028d116a6e59e`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7e4b16927cdba1f56bfd47ee4f0ec91f03eb4d54665950de0e690a8cf591a7`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1e6f397ed251ea4fa0fb49b33654ae0a4f21051946b31de5b6298d957e07df`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bd7d3b9f81e641b929a92168f2988f89f7d48ff296f269386fa26ee6004909`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 479.0 KB (479045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a93be0fe778d54bf31dbf755152bca8e716fe3b4a6a26a6363bf6eefb86f0c`  
		Last Modified: Tue, 14 Apr 2026 21:07:48 GMT  
		Size: 7.0 MB (7018960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6f1157c852a3b84dc8acc8da41f4341b89ad594de182595b028d6cfc5cc59`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b986f7ba00c261673bec4ea3a233599f672f19ee33681b8e984c027d03cf366`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfefa8af6da8003b32230316fcacc30569cbe0a4231b6f6e19a2b68fe7ba5ae8`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f7ff6f050a295adfee7c011b0dee2b54a41677aa16389632062d6bb6b5a6ee`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.16`

```console
$ docker pull nats@sha256:cbc2a07dfd6bc22f6dbadcb898666368dc58c5ec00f69b5aac0b72895f7e3647
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11.16` - linux; amd64

```console
$ docker pull nats@sha256:c2110151e63b453119fbd17e9fa64e44ab4ce07ed8a033c76a62946ddf6b614d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6497606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0910ab9e623cf3c8c8b450f1a8998c5a5d65ec923e9f5eae99682d370b0b7186`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:12 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9f0ebe5f9a1ae3ad639c8afca45fb722413353ade56a44dcf62bcfef80217dbb`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.5 MB (6497097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3aa31a58f3732fef628ef5de608085bbd9fd3cdd9ae1bc38476cd77e2a9f71`  
		Last Modified: Tue, 14 Apr 2026 20:10:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16` - unknown; unknown

```console
$ docker pull nats@sha256:b471dfd5308d245d31473ef6fb9a44d04609d7084d1f6435db514ae5b19507ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6307fe453094ab6bf3dce0a1a57c4de4ed82d0f95f3d7c2a3cbf20f5c340fdbd`

```dockerfile
```

-	Layers:
	-	`sha256:2fb63ea3ab9f0be3fad75526a8a808b092a7b8f97002d57208e5baebb694ae55`  
		Last Modified: Tue, 14 Apr 2026 20:10:17 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4be3c3c3593bfb53295d26f82732a468b64c6b3617882d3d2fc62e330c34de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d75ed8e27c246ac51767267210e1c5640347bbbd5ffee5b012eae91162ed0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:50 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:50 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:50 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:50 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ac4c14b3f8076df43f73c9299994bae9134a062823f58d1140353085aa0b300`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.2 MB (6218951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9a6f4ed2afcfd3f5f084fe6e276fb037b60aa6590560929719b278e20d99ce`  
		Last Modified: Tue, 14 Apr 2026 20:08:54 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16` - unknown; unknown

```console
$ docker pull nats@sha256:6e94f7dcea2fef9d27a13db5b1216d7d60556e18b11a035cc312a38cc1a6d778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c4d4fd8ad8fd7cfe4a5f9c7b009ed245033ce376e5e9d7823b2cac668c1d57`

```dockerfile
```

-	Layers:
	-	`sha256:fbb355648bd431a8b0977dfabf60aa9069152a7fb369e1753dcdf5e52f4fda24`  
		Last Modified: Tue, 14 Apr 2026 20:08:54 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:20c43ada29aca6f237ce383386788f0d32d50fc126ed43cbc1724d9567af8e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ff6e38918165fe195fd75349e870b96ce5ba4040e58d7f8f1ceb913da191ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:44:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:44:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:44:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:44:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:44:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:44:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2a83fab97c651eacbf830fb7bd159907e5e14fda32f73c5628adf6899c32f67f`  
		Last Modified: Tue, 14 Apr 2026 16:12:11 GMT  
		Size: 6.2 MB (6208591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa15cae9b1157772879677c602f41156691045d5965ccb813916810df1fe4bb4`  
		Last Modified: Tue, 14 Apr 2026 20:44:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16` - unknown; unknown

```console
$ docker pull nats@sha256:335859fd4ccfc83d33e49af0abb39046cb66161f6cb41b1d297e18185ed2d82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a3335340d60b379757a5475817b6f11fd4228353746af920b898da1d4f0c90`

```dockerfile
```

-	Layers:
	-	`sha256:380d6911889112f6fb63ea5b38cc214ae0c36fa9103d5b53716e58a52597aadd`  
		Last Modified: Tue, 14 Apr 2026 20:44:44 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abbaf279400efe50c75c001cadf65397a0d36585ee13cd93fa4c674f9f334610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c88001ed291a311398596c738f3953e284046e8cfb5a6fb942c2e6095fce1e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:16 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53e14ebbec1f96d7732d422be8ee7b587c333a423ac37b45d8cbe989c7ffe1ed`  
		Last Modified: Tue, 14 Apr 2026 16:12:13 GMT  
		Size: 5.9 MB (5915332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d21c1e4bfb6845681b40f88f6c360fd74dddbb4be86f32deb7bb7c967ed0b7`  
		Last Modified: Tue, 14 Apr 2026 20:10:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16` - unknown; unknown

```console
$ docker pull nats@sha256:028d2be5c52a686b2e055ce4b7a524268ad13fc1b2d441001a76941f17aad07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd94cfc134986b016c708bcfb838242037df4f5e4edf95655265bee2d16a4bd6`

```dockerfile
```

-	Layers:
	-	`sha256:95d6c9956af48d4e05152e7126a70c0a732bff4992493102b84da32c69ce796b`  
		Last Modified: Tue, 14 Apr 2026 20:10:20 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16` - linux; ppc64le

```console
$ docker pull nats@sha256:1ebc5c2cf6b0fc3b0e50cc38afab77cfa688f8da4024fa99681f7611d8ac0f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8278b7cc91b73cd95f65829f426b3a56b62948c201cb02fc5939d2802f4cc8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b63ce4825759431170974b945ec1ddea7f5665ed75cc067dc0285b5ece42ed12`  
		Last Modified: Tue, 14 Apr 2026 16:12:12 GMT  
		Size: 6.0 MB (5964595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143e5f30d6fc7c65fa53e947ac6769436eb6e2dcc5c1a981230be9abadf9237e`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16` - unknown; unknown

```console
$ docker pull nats@sha256:e4fa323ebd6292cc230c999c0c58bb8e756bbcb73acdbe9be3dc2582f850b14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e1c8b35cc1455b27a2ad77da671aca7bec71cd4469a53bf630e9274c649c2f`

```dockerfile
```

-	Layers:
	-	`sha256:1719e1239afd7235ebf11aab5e250649cfa41f29f15712a458ade3c61492cd9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16` - linux; s390x

```console
$ docker pull nats@sha256:a2cfef35bf670a3475a15ef1169a8f4f477958b389305df32f46ed369ffbc709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b772fdee82b6cf590b45d94f0cd27b548914f71d08ebb473f1ec4a387fca92f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:12 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7da88b0130848f05398873a2b9335b6391d3a2040acd810dc06d9574dbb2bb8`  
		Last Modified: Tue, 14 Apr 2026 20:09:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16` - unknown; unknown

```console
$ docker pull nats@sha256:6dc7f690e56d56df808c8db0ba100e6a24552f0896701b2a36567d46d6e23a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895583c3c619bee0ff187e28a90b2c58804aed9d323fc34f0ddd9fe29f40dbc0`

```dockerfile
```

-	Layers:
	-	`sha256:0d02a41a21d1ae4a3f92949bfa5bcdec8304d824bd5b40042199a8779d25bc7d`  
		Last Modified: Tue, 14 Apr 2026 20:09:20 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:5ffa3167d5e3e3fd4258586b3e58689d9ca02a145f6b5cbc6a82f8416b7c61e3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133637234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29654dc94df41eabc4fec5c6267f3e71846d39bd31cc97f52dd46404020ce98`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:52 GMT
RUN cmd /S /C #(nop) COPY file:f1ed4e18be63052ebd2a9f8f87593bf079db370ff176ea712b36dc2ac83ea376 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:54 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed04d46136c3797ba3fc4ddcaceedae8a6fc3fd40e4f77f0929591c7b645a51`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db2f5a47ed51a8fd3b8ccbc37ae5b9d89766a7cd30ac5138fc1abab63a8917e`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 6.7 MB (6675280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd0b5b898034b9675ff6aa86b1a3b107c8ca3cc2788fca25c8f4f1ff65c4840`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823643c2dcd9d2a19ef822365ba3d59a932d0f663749945aec1c1fb74a7fff98`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2286cfe5bab4a54ba713d5f92768b2ecfd0a029b275ba96d7b2c6dcca57056c6`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4274ef274b88859bdfe852c4c36f18d9eca26a752f7d521c3ee89749b253221`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.16-alpine`

```console
$ docker pull nats@sha256:7f94277277e89fc16f3f5a4633786b700679170007dad41cfdef0a0d458181cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11.16-alpine` - linux; amd64

```console
$ docker pull nats@sha256:b63d3a4c4b096a5b8aee698ffccf8ca001a857480d17dfecfb2acedfa331dd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10761772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0da8c22287d4e8c8b517b9964eabae67ee0490bf659766a6243afc39202b424`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:55 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:17:55 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:17:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f4d65993bf1d7a5b112c64d702118106b5745f06c6aec17b9b9c128a72b0b`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 7.0 MB (6955927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507d1402650f69b68b2e36b453f5aab0b2b8db1a4f8bb739ae03d4fafeb0e1ff`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b06ed42e02408e874a121a6e7e3e71875595a58ce02f8f0e4f3864138aeccb5`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:58330e58d92710af2e527e0f53719594416285eea76656f1ca4151399b34fd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b02aacc3dc69202e57431ff1dc33441decf3731fc9b1f53ed32ad43d1e972a7`

```dockerfile
```

-	Layers:
	-	`sha256:2ca807165446d4e9d1d6a6d55c43a4b45bedf2e726f767d73acca2788652a923`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:2c1a54648ee8363c187d7e9cd4906eb5e84b6cf1c8f52909fe63bed73f0d3415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10181356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6d7718f62effe9f15c7d396f4385a3aa5688b1cb038df30365cc902714b0c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:41 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:18:41 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:18:41 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:41 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:41 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b21e1551199aaabe96bd6470249e52fe24403fa35c793649ffaf57e2be3afda`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 6.7 MB (6675341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f736f2cddf61123f514302e6c81c49f18254a1a43288596e04166fda82e301`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27c4f6c7e2706bcd0356aed93cf8ab1b5284438519aee8fcbc357511b770657`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ec48a5a37c3c6e64d467e1a5d89dacae513127fda305853965de4ecd82ca22c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa91d0c123eb472e3619e73cc11c2c58c0856355eedaede9dea2fa8a506921a`

```dockerfile
```

-	Layers:
	-	`sha256:e40bb7eea2e90b7b0f6a52b11d4c9347be60d3e47e0c30dbe4161676c8d3d535`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:31a6e7deb249b86a8f878129462563f8cf0af0c0873a79bcc29a64c02e3ec244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9892913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad532990e4c0ecfddc9989329e28af97213b9060533f8065296b959af1352ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:44 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:18:44 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:18:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:44 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:44 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86089bb885556e0e27177c70e0e8f24d65dfd9c1f056a24d1dda1f23fad18bd`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 6.7 MB (6668316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a59172091a849e6b576bb25e5049f3c5b7a211845bd0a3ea5d9e6bb6ad55569`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca319357a73b41fa3d463244c39665508ac9efbdb21773f3cc22b9816e522cdc`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:38d16725794fb492177bd3f9a9111b4bb20683fa9a166f5186818159ff5be989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d7f09af972d51fc935e39738db1d4a8caefa8b885a8f75e87e59cecb19dd5f`

```dockerfile
```

-	Layers:
	-	`sha256:ab214d3d1838f37d03cc24cbb0d3f9b6d2a56e90bf57f1e354739af2e261d46f`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1d9049ae318c5ca83b7685a8e94df86dc1c10ad858bf90759c8fae8019da9906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce88ba66d2a0276da1939f036514e6ca0ef90e98f221bf589f5b51afae026e7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:39 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:18:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:18:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:39 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7566471ec2e31f581c1fa6cf70bc93bf2a5a83568ef458a6eccdcc18295829f2`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 6.4 MB (6376343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819bc5a8128d9ecefa58495dc2001c47adc63afb013680d86ad71f524d49fb9a`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b4d9008cd0aed6dfd8dfd2fdaee1ab5cde830217b117405b388e6ef086a507`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1a40022484327e18ecdb0d1cbcf301fe7a04e0adb9bfaa596744cfdf7999d634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de9fa3beefafe36b5b72f66f11d4394dff2966172cf342e1764da19456d7a09`

```dockerfile
```

-	Layers:
	-	`sha256:ab7a33235df45e0b1bf6d870b24254b5c242d74e824ac98ce0b4e4777382b804`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:bfd9ed6c2e3965b057b674b17430c808399842287e23c9ab829ca30ce0c99369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10161835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0688bcfd19c4c883dfd4b52ef841748aa4f6d677900eead71540a330b20a600b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:23:16 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:23:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:23:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:23:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:23:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eedd38afc716f975cb2e891febac979941155f68a06f2ce2837de197955b813`  
		Last Modified: Tue, 14 Apr 2026 19:23:32 GMT  
		Size: 6.4 MB (6426566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac87bfa474f24897ae62b339e8d3e99d2477339cb9c7b9c9c27fe53e05575a`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5caa4d61a9b6f6e771c2817dc9c2d7f2b7737c8d5ba3352063ae308e6ba4bb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:dab9fcf5b55a32afb30979fa8c0cff63488786bcfdf5ae87d615ec7a7ed315c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f71f7de20b524e074c54be6fec078361d34a0f7686f583ef1242033283c2eaf`

```dockerfile
```

-	Layers:
	-	`sha256:64634cc116b7317798b65dd8d668d7b2b361f349320365d7bec44b08760d0aeb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine` - linux; s390x

```console
$ docker pull nats@sha256:0033b9a24a893eaa753fa356652316843d45167ac6f338fa3097cce110bc9b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10449885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e5287372a06705e1befee77a0e18b289b4e0adf15ed3331209105dff253a90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:17:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:17:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:38 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb45f6557a69c491c09b306884852b4012fc69ad197a919c63e020f9569a591`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 6.8 MB (6798483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0285f9e4fa1fd20d08ae7535e92e1bccca5487085129b19e2911596c22c06b`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908a1c7e17ce2f5731370d6d0f0ae8ed31a1763953ab3b68105604dab44a56f7`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:411ec8a8b2e7dafef4400f8b7f3dac28d374d80bec9a94772de6cb73533ca9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aafbbd6fcc4a17826f55623e55cc67c9523de3a312fa7078052f20630abe2f`

```dockerfile
```

-	Layers:
	-	`sha256:fc6cd0442a0cf11748f61eedb8eb8009c2c2cbd966e458c5a8b5e1c82ff20891`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.16-alpine3.22`

```console
$ docker pull nats@sha256:7f94277277e89fc16f3f5a4633786b700679170007dad41cfdef0a0d458181cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11.16-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:b63d3a4c4b096a5b8aee698ffccf8ca001a857480d17dfecfb2acedfa331dd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10761772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0da8c22287d4e8c8b517b9964eabae67ee0490bf659766a6243afc39202b424`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:55 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:17:55 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:17:55 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:55 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:55 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2f4d65993bf1d7a5b112c64d702118106b5745f06c6aec17b9b9c128a72b0b`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 7.0 MB (6955927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507d1402650f69b68b2e36b453f5aab0b2b8db1a4f8bb739ae03d4fafeb0e1ff`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b06ed42e02408e874a121a6e7e3e71875595a58ce02f8f0e4f3864138aeccb5`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:58330e58d92710af2e527e0f53719594416285eea76656f1ca4151399b34fd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b02aacc3dc69202e57431ff1dc33441decf3731fc9b1f53ed32ad43d1e972a7`

```dockerfile
```

-	Layers:
	-	`sha256:2ca807165446d4e9d1d6a6d55c43a4b45bedf2e726f767d73acca2788652a923`  
		Last Modified: Tue, 14 Apr 2026 19:17:59 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:2c1a54648ee8363c187d7e9cd4906eb5e84b6cf1c8f52909fe63bed73f0d3415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10181356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6d7718f62effe9f15c7d396f4385a3aa5688b1cb038df30365cc902714b0c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:41 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:18:41 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:18:41 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:41 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:41 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:41 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b21e1551199aaabe96bd6470249e52fe24403fa35c793649ffaf57e2be3afda`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 6.7 MB (6675341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f736f2cddf61123f514302e6c81c49f18254a1a43288596e04166fda82e301`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27c4f6c7e2706bcd0356aed93cf8ab1b5284438519aee8fcbc357511b770657`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ec48a5a37c3c6e64d467e1a5d89dacae513127fda305853965de4ecd82ca22c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa91d0c123eb472e3619e73cc11c2c58c0856355eedaede9dea2fa8a506921a`

```dockerfile
```

-	Layers:
	-	`sha256:e40bb7eea2e90b7b0f6a52b11d4c9347be60d3e47e0c30dbe4161676c8d3d535`  
		Last Modified: Tue, 14 Apr 2026 19:18:46 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:31a6e7deb249b86a8f878129462563f8cf0af0c0873a79bcc29a64c02e3ec244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9892913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad532990e4c0ecfddc9989329e28af97213b9060533f8065296b959af1352ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:44 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:18:44 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:18:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:44 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:44 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86089bb885556e0e27177c70e0e8f24d65dfd9c1f056a24d1dda1f23fad18bd`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 6.7 MB (6668316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a59172091a849e6b576bb25e5049f3c5b7a211845bd0a3ea5d9e6bb6ad55569`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca319357a73b41fa3d463244c39665508ac9efbdb21773f3cc22b9816e522cdc`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:38d16725794fb492177bd3f9a9111b4bb20683fa9a166f5186818159ff5be989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d7f09af972d51fc935e39738db1d4a8caefa8b885a8f75e87e59cecb19dd5f`

```dockerfile
```

-	Layers:
	-	`sha256:ab214d3d1838f37d03cc24cbb0d3f9b6d2a56e90bf57f1e354739af2e261d46f`  
		Last Modified: Tue, 14 Apr 2026 19:18:48 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1d9049ae318c5ca83b7685a8e94df86dc1c10ad858bf90759c8fae8019da9906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce88ba66d2a0276da1939f036514e6ca0ef90e98f221bf589f5b51afae026e7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:39 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:18:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:18:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:39 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:39 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7566471ec2e31f581c1fa6cf70bc93bf2a5a83568ef458a6eccdcc18295829f2`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 6.4 MB (6376343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819bc5a8128d9ecefa58495dc2001c47adc63afb013680d86ad71f524d49fb9a`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b4d9008cd0aed6dfd8dfd2fdaee1ab5cde830217b117405b388e6ef086a507`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:1a40022484327e18ecdb0d1cbcf301fe7a04e0adb9bfaa596744cfdf7999d634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de9fa3beefafe36b5b72f66f11d4394dff2966172cf342e1764da19456d7a09`

```dockerfile
```

-	Layers:
	-	`sha256:ab7a33235df45e0b1bf6d870b24254b5c242d74e824ac98ce0b4e4777382b804`  
		Last Modified: Tue, 14 Apr 2026 19:18:43 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:bfd9ed6c2e3965b057b674b17430c808399842287e23c9ab829ca30ce0c99369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10161835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0688bcfd19c4c883dfd4b52ef841748aa4f6d677900eead71540a330b20a600b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:23:16 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:23:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:23:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:23:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:23:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eedd38afc716f975cb2e891febac979941155f68a06f2ce2837de197955b813`  
		Last Modified: Tue, 14 Apr 2026 19:23:32 GMT  
		Size: 6.4 MB (6426566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac87bfa474f24897ae62b339e8d3e99d2477339cb9c7b9c9c27fe53e05575a`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5caa4d61a9b6f6e771c2817dc9c2d7f2b7737c8d5ba3352063ae308e6ba4bb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:dab9fcf5b55a32afb30979fa8c0cff63488786bcfdf5ae87d615ec7a7ed315c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f71f7de20b524e074c54be6fec078361d34a0f7686f583ef1242033283c2eaf`

```dockerfile
```

-	Layers:
	-	`sha256:64634cc116b7317798b65dd8d668d7b2b361f349320365d7bec44b08760d0aeb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:0033b9a24a893eaa753fa356652316843d45167ac6f338fa3097cce110bc9b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10449885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e5287372a06705e1befee77a0e18b289b4e0adf15ed3331209105dff253a90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 19:17:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 19:17:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:38 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:38 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb45f6557a69c491c09b306884852b4012fc69ad197a919c63e020f9569a591`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 6.8 MB (6798483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0285f9e4fa1fd20d08ae7535e92e1bccca5487085129b19e2911596c22c06b`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908a1c7e17ce2f5731370d6d0f0ae8ed31a1763953ab3b68105604dab44a56f7`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:411ec8a8b2e7dafef4400f8b7f3dac28d374d80bec9a94772de6cb73533ca9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59aafbbd6fcc4a17826f55623e55cc67c9523de3a312fa7078052f20630abe2f`

```dockerfile
```

-	Layers:
	-	`sha256:fc6cd0442a0cf11748f61eedb8eb8009c2c2cbd966e458c5a8b5e1c82ff20891`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.16-linux`

```console
$ docker pull nats@sha256:7a65060f41a558780b2bc5ec0049838bf914fff16361174609c1bf69ff240fe6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11.16-linux` - linux; amd64

```console
$ docker pull nats@sha256:c2110151e63b453119fbd17e9fa64e44ab4ce07ed8a033c76a62946ddf6b614d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6497606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0910ab9e623cf3c8c8b450f1a8998c5a5d65ec923e9f5eae99682d370b0b7186`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:12 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9f0ebe5f9a1ae3ad639c8afca45fb722413353ade56a44dcf62bcfef80217dbb`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.5 MB (6497097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3aa31a58f3732fef628ef5de608085bbd9fd3cdd9ae1bc38476cd77e2a9f71`  
		Last Modified: Tue, 14 Apr 2026 20:10:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b471dfd5308d245d31473ef6fb9a44d04609d7084d1f6435db514ae5b19507ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6307fe453094ab6bf3dce0a1a57c4de4ed82d0f95f3d7c2a3cbf20f5c340fdbd`

```dockerfile
```

-	Layers:
	-	`sha256:2fb63ea3ab9f0be3fad75526a8a808b092a7b8f97002d57208e5baebb694ae55`  
		Last Modified: Tue, 14 Apr 2026 20:10:17 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4be3c3c3593bfb53295d26f82732a468b64c6b3617882d3d2fc62e330c34de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d75ed8e27c246ac51767267210e1c5640347bbbd5ffee5b012eae91162ed0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:50 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:50 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:50 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:50 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ac4c14b3f8076df43f73c9299994bae9134a062823f58d1140353085aa0b300`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.2 MB (6218951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9a6f4ed2afcfd3f5f084fe6e276fb037b60aa6590560929719b278e20d99ce`  
		Last Modified: Tue, 14 Apr 2026 20:08:54 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6e94f7dcea2fef9d27a13db5b1216d7d60556e18b11a035cc312a38cc1a6d778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c4d4fd8ad8fd7cfe4a5f9c7b009ed245033ce376e5e9d7823b2cac668c1d57`

```dockerfile
```

-	Layers:
	-	`sha256:fbb355648bd431a8b0977dfabf60aa9069152a7fb369e1753dcdf5e52f4fda24`  
		Last Modified: Tue, 14 Apr 2026 20:08:54 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:20c43ada29aca6f237ce383386788f0d32d50fc126ed43cbc1724d9567af8e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ff6e38918165fe195fd75349e870b96ce5ba4040e58d7f8f1ceb913da191ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:44:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:44:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:44:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:44:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:44:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:44:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2a83fab97c651eacbf830fb7bd159907e5e14fda32f73c5628adf6899c32f67f`  
		Last Modified: Tue, 14 Apr 2026 16:12:11 GMT  
		Size: 6.2 MB (6208591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa15cae9b1157772879677c602f41156691045d5965ccb813916810df1fe4bb4`  
		Last Modified: Tue, 14 Apr 2026 20:44:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-linux` - unknown; unknown

```console
$ docker pull nats@sha256:335859fd4ccfc83d33e49af0abb39046cb66161f6cb41b1d297e18185ed2d82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a3335340d60b379757a5475817b6f11fd4228353746af920b898da1d4f0c90`

```dockerfile
```

-	Layers:
	-	`sha256:380d6911889112f6fb63ea5b38cc214ae0c36fa9103d5b53716e58a52597aadd`  
		Last Modified: Tue, 14 Apr 2026 20:44:44 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abbaf279400efe50c75c001cadf65397a0d36585ee13cd93fa4c674f9f334610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c88001ed291a311398596c738f3953e284046e8cfb5a6fb942c2e6095fce1e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:16 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53e14ebbec1f96d7732d422be8ee7b587c333a423ac37b45d8cbe989c7ffe1ed`  
		Last Modified: Tue, 14 Apr 2026 16:12:13 GMT  
		Size: 5.9 MB (5915332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d21c1e4bfb6845681b40f88f6c360fd74dddbb4be86f32deb7bb7c967ed0b7`  
		Last Modified: Tue, 14 Apr 2026 20:10:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-linux` - unknown; unknown

```console
$ docker pull nats@sha256:028d2be5c52a686b2e055ce4b7a524268ad13fc1b2d441001a76941f17aad07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd94cfc134986b016c708bcfb838242037df4f5e4edf95655265bee2d16a4bd6`

```dockerfile
```

-	Layers:
	-	`sha256:95d6c9956af48d4e05152e7126a70c0a732bff4992493102b84da32c69ce796b`  
		Last Modified: Tue, 14 Apr 2026 20:10:20 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:1ebc5c2cf6b0fc3b0e50cc38afab77cfa688f8da4024fa99681f7611d8ac0f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8278b7cc91b73cd95f65829f426b3a56b62948c201cb02fc5939d2802f4cc8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b63ce4825759431170974b945ec1ddea7f5665ed75cc067dc0285b5ece42ed12`  
		Last Modified: Tue, 14 Apr 2026 16:12:12 GMT  
		Size: 6.0 MB (5964595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143e5f30d6fc7c65fa53e947ac6769436eb6e2dcc5c1a981230be9abadf9237e`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-linux` - unknown; unknown

```console
$ docker pull nats@sha256:e4fa323ebd6292cc230c999c0c58bb8e756bbcb73acdbe9be3dc2582f850b14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e1c8b35cc1455b27a2ad77da671aca7bec71cd4469a53bf630e9274c649c2f`

```dockerfile
```

-	Layers:
	-	`sha256:1719e1239afd7235ebf11aab5e250649cfa41f29f15712a458ade3c61492cd9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-linux` - linux; s390x

```console
$ docker pull nats@sha256:a2cfef35bf670a3475a15ef1169a8f4f477958b389305df32f46ed369ffbc709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b772fdee82b6cf590b45d94f0cd27b548914f71d08ebb473f1ec4a387fca92f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:12 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7da88b0130848f05398873a2b9335b6391d3a2040acd810dc06d9574dbb2bb8`  
		Last Modified: Tue, 14 Apr 2026 20:09:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6dc7f690e56d56df808c8db0ba100e6a24552f0896701b2a36567d46d6e23a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895583c3c619bee0ff187e28a90b2c58804aed9d323fc34f0ddd9fe29f40dbc0`

```dockerfile
```

-	Layers:
	-	`sha256:0d02a41a21d1ae4a3f92949bfa5bcdec8304d824bd5b40042199a8779d25bc7d`  
		Last Modified: Tue, 14 Apr 2026 20:09:20 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.16-nanoserver`

```console
$ docker pull nats@sha256:8369f10fa05d956de0096a7a744a1b1d55175a37c2841087081423b4165fae7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11.16-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:5ffa3167d5e3e3fd4258586b3e58689d9ca02a145f6b5cbc6a82f8416b7c61e3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133637234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29654dc94df41eabc4fec5c6267f3e71846d39bd31cc97f52dd46404020ce98`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:52 GMT
RUN cmd /S /C #(nop) COPY file:f1ed4e18be63052ebd2a9f8f87593bf079db370ff176ea712b36dc2ac83ea376 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:54 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed04d46136c3797ba3fc4ddcaceedae8a6fc3fd40e4f77f0929591c7b645a51`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db2f5a47ed51a8fd3b8ccbc37ae5b9d89766a7cd30ac5138fc1abab63a8917e`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 6.7 MB (6675280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd0b5b898034b9675ff6aa86b1a3b107c8ca3cc2788fca25c8f4f1ff65c4840`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823643c2dcd9d2a19ef822365ba3d59a932d0f663749945aec1c1fb74a7fff98`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2286cfe5bab4a54ba713d5f92768b2ecfd0a029b275ba96d7b2c6dcca57056c6`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4274ef274b88859bdfe852c4c36f18d9eca26a752f7d521c3ee89749b253221`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.16-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:8369f10fa05d956de0096a7a744a1b1d55175a37c2841087081423b4165fae7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11.16-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:5ffa3167d5e3e3fd4258586b3e58689d9ca02a145f6b5cbc6a82f8416b7c61e3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133637234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29654dc94df41eabc4fec5c6267f3e71846d39bd31cc97f52dd46404020ce98`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:51 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:52 GMT
RUN cmd /S /C #(nop) COPY file:f1ed4e18be63052ebd2a9f8f87593bf079db370ff176ea712b36dc2ac83ea376 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:54 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed04d46136c3797ba3fc4ddcaceedae8a6fc3fd40e4f77f0929591c7b645a51`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db2f5a47ed51a8fd3b8ccbc37ae5b9d89766a7cd30ac5138fc1abab63a8917e`  
		Last Modified: Tue, 14 Apr 2026 21:47:59 GMT  
		Size: 6.7 MB (6675280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd0b5b898034b9675ff6aa86b1a3b107c8ca3cc2788fca25c8f4f1ff65c4840`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823643c2dcd9d2a19ef822365ba3d59a932d0f663749945aec1c1fb74a7fff98`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2286cfe5bab4a54ba713d5f92768b2ecfd0a029b275ba96d7b2c6dcca57056c6`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4274ef274b88859bdfe852c4c36f18d9eca26a752f7d521c3ee89749b253221`  
		Last Modified: Tue, 14 Apr 2026 21:47:58 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.16-scratch`

```console
$ docker pull nats@sha256:7a65060f41a558780b2bc5ec0049838bf914fff16361174609c1bf69ff240fe6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11.16-scratch` - linux; amd64

```console
$ docker pull nats@sha256:c2110151e63b453119fbd17e9fa64e44ab4ce07ed8a033c76a62946ddf6b614d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6497606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0910ab9e623cf3c8c8b450f1a8998c5a5d65ec923e9f5eae99682d370b0b7186`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:12 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9f0ebe5f9a1ae3ad639c8afca45fb722413353ade56a44dcf62bcfef80217dbb`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.5 MB (6497097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3aa31a58f3732fef628ef5de608085bbd9fd3cdd9ae1bc38476cd77e2a9f71`  
		Last Modified: Tue, 14 Apr 2026 20:10:16 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b471dfd5308d245d31473ef6fb9a44d04609d7084d1f6435db514ae5b19507ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6307fe453094ab6bf3dce0a1a57c4de4ed82d0f95f3d7c2a3cbf20f5c340fdbd`

```dockerfile
```

-	Layers:
	-	`sha256:2fb63ea3ab9f0be3fad75526a8a808b092a7b8f97002d57208e5baebb694ae55`  
		Last Modified: Tue, 14 Apr 2026 20:10:17 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:a4be3c3c3593bfb53295d26f82732a468b64c6b3617882d3d2fc62e330c34de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d75ed8e27c246ac51767267210e1c5640347bbbd5ffee5b012eae91162ed0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:50 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:50 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:50 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:50 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ac4c14b3f8076df43f73c9299994bae9134a062823f58d1140353085aa0b300`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.2 MB (6218951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9a6f4ed2afcfd3f5f084fe6e276fb037b60aa6590560929719b278e20d99ce`  
		Last Modified: Tue, 14 Apr 2026 20:08:54 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6e94f7dcea2fef9d27a13db5b1216d7d60556e18b11a035cc312a38cc1a6d778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c4d4fd8ad8fd7cfe4a5f9c7b009ed245033ce376e5e9d7823b2cac668c1d57`

```dockerfile
```

-	Layers:
	-	`sha256:fbb355648bd431a8b0977dfabf60aa9069152a7fb369e1753dcdf5e52f4fda24`  
		Last Modified: Tue, 14 Apr 2026 20:08:54 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:20c43ada29aca6f237ce383386788f0d32d50fc126ed43cbc1724d9567af8e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ff6e38918165fe195fd75349e870b96ce5ba4040e58d7f8f1ceb913da191ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:44:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:44:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:44:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:44:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:44:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:44:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2a83fab97c651eacbf830fb7bd159907e5e14fda32f73c5628adf6899c32f67f`  
		Last Modified: Tue, 14 Apr 2026 16:12:11 GMT  
		Size: 6.2 MB (6208591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa15cae9b1157772879677c602f41156691045d5965ccb813916810df1fe4bb4`  
		Last Modified: Tue, 14 Apr 2026 20:44:44 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:335859fd4ccfc83d33e49af0abb39046cb66161f6cb41b1d297e18185ed2d82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a3335340d60b379757a5475817b6f11fd4228353746af920b898da1d4f0c90`

```dockerfile
```

-	Layers:
	-	`sha256:380d6911889112f6fb63ea5b38cc214ae0c36fa9103d5b53716e58a52597aadd`  
		Last Modified: Tue, 14 Apr 2026 20:44:44 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:abbaf279400efe50c75c001cadf65397a0d36585ee13cd93fa4c674f9f334610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c88001ed291a311398596c738f3953e284046e8cfb5a6fb942c2e6095fce1e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:16 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53e14ebbec1f96d7732d422be8ee7b587c333a423ac37b45d8cbe989c7ffe1ed`  
		Last Modified: Tue, 14 Apr 2026 16:12:13 GMT  
		Size: 5.9 MB (5915332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d21c1e4bfb6845681b40f88f6c360fd74dddbb4be86f32deb7bb7c967ed0b7`  
		Last Modified: Tue, 14 Apr 2026 20:10:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:028d2be5c52a686b2e055ce4b7a524268ad13fc1b2d441001a76941f17aad07c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd94cfc134986b016c708bcfb838242037df4f5e4edf95655265bee2d16a4bd6`

```dockerfile
```

-	Layers:
	-	`sha256:95d6c9956af48d4e05152e7126a70c0a732bff4992493102b84da32c69ce796b`  
		Last Modified: Tue, 14 Apr 2026 20:10:20 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:1ebc5c2cf6b0fc3b0e50cc38afab77cfa688f8da4024fa99681f7611d8ac0f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8278b7cc91b73cd95f65829f426b3a56b62948c201cb02fc5939d2802f4cc8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b63ce4825759431170974b945ec1ddea7f5665ed75cc067dc0285b5ece42ed12`  
		Last Modified: Tue, 14 Apr 2026 16:12:12 GMT  
		Size: 6.0 MB (5964595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143e5f30d6fc7c65fa53e947ac6769436eb6e2dcc5c1a981230be9abadf9237e`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:e4fa323ebd6292cc230c999c0c58bb8e756bbcb73acdbe9be3dc2582f850b14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e1c8b35cc1455b27a2ad77da671aca7bec71cd4469a53bf630e9274c649c2f`

```dockerfile
```

-	Layers:
	-	`sha256:1719e1239afd7235ebf11aab5e250649cfa41f29f15712a458ade3c61492cd9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-scratch` - linux; s390x

```console
$ docker pull nats@sha256:a2cfef35bf670a3475a15ef1169a8f4f477958b389305df32f46ed369ffbc709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b772fdee82b6cf590b45d94f0cd27b548914f71d08ebb473f1ec4a387fca92f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:12 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:12 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:12 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7da88b0130848f05398873a2b9335b6391d3a2040acd810dc06d9574dbb2bb8`  
		Last Modified: Tue, 14 Apr 2026 20:09:20 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6dc7f690e56d56df808c8db0ba100e6a24552f0896701b2a36567d46d6e23a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895583c3c619bee0ff187e28a90b2c58804aed9d323fc34f0ddd9fe29f40dbc0`

```dockerfile
```

-	Layers:
	-	`sha256:0d02a41a21d1ae4a3f92949bfa5bcdec8304d824bd5b40042199a8779d25bc7d`  
		Last Modified: Tue, 14 Apr 2026 20:09:20 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.16-windowsservercore`

```console
$ docker pull nats@sha256:0fab64367d01a89d9933f0c222c927c5b6199e3ededca344283d796b7ff2afa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11.16-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:3b61953057c6c60d9800b8453169f6396d3cf533fe54e4c48ef7158413042717
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077722942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef93dc3bf8a5885439b286e78880586afe506977de79802da64c1fff0455078`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:06:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:06:25 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:07:15 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 21:07:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 21:07:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.16/nats-server-v2.11.16-windows-amd64.zip
# Tue, 14 Apr 2026 21:07:16 GMT
ENV NATS_SERVER_SHASUM=8371464b7c604e45a21efd0fb754849defcf86419994d79b5d0f2547b39171b7
# Tue, 14 Apr 2026 21:07:21 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Apr 2026 21:07:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Apr 2026 21:07:37 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:07:38 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:07:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:07:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234f0c5dc55953d98e0d13e9e881a65f871f8e0476a39dc8074be17e88c96ab`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e8f504a62653497a194c864fb383113d6df01412a46e631c3118b188201760`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a25322b4e8a70bd21a23374e7a44f4d3e0bf91d86a709f87c1e0e41b5c34630`  
		Last Modified: Tue, 14 Apr 2026 21:07:48 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6508587f65ad7bc80506629c5050f641a67b576390527bd50028d116a6e59e`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7e4b16927cdba1f56bfd47ee4f0ec91f03eb4d54665950de0e690a8cf591a7`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1e6f397ed251ea4fa0fb49b33654ae0a4f21051946b31de5b6298d957e07df`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bd7d3b9f81e641b929a92168f2988f89f7d48ff296f269386fa26ee6004909`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 479.0 KB (479045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a93be0fe778d54bf31dbf755152bca8e716fe3b4a6a26a6363bf6eefb86f0c`  
		Last Modified: Tue, 14 Apr 2026 21:07:48 GMT  
		Size: 7.0 MB (7018960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6f1157c852a3b84dc8acc8da41f4341b89ad594de182595b028d6cfc5cc59`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b986f7ba00c261673bec4ea3a233599f672f19ee33681b8e984c027d03cf366`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfefa8af6da8003b32230316fcacc30569cbe0a4231b6f6e19a2b68fe7ba5ae8`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f7ff6f050a295adfee7c011b0dee2b54a41677aa16389632062d6bb6b5a6ee`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.16-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:0fab64367d01a89d9933f0c222c927c5b6199e3ededca344283d796b7ff2afa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.11.16-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:3b61953057c6c60d9800b8453169f6396d3cf533fe54e4c48ef7158413042717
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077722942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef93dc3bf8a5885439b286e78880586afe506977de79802da64c1fff0455078`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:06:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:06:25 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:07:15 GMT
ENV NATS_SERVER=2.11.16
# Tue, 14 Apr 2026 21:07:15 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Tue, 14 Apr 2026 21:07:16 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.16/nats-server-v2.11.16-windows-amd64.zip
# Tue, 14 Apr 2026 21:07:16 GMT
ENV NATS_SERVER_SHASUM=8371464b7c604e45a21efd0fb754849defcf86419994d79b5d0f2547b39171b7
# Tue, 14 Apr 2026 21:07:21 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Apr 2026 21:07:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Apr 2026 21:07:37 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:07:38 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:07:38 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:07:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234f0c5dc55953d98e0d13e9e881a65f871f8e0476a39dc8074be17e88c96ab`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e8f504a62653497a194c864fb383113d6df01412a46e631c3118b188201760`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a25322b4e8a70bd21a23374e7a44f4d3e0bf91d86a709f87c1e0e41b5c34630`  
		Last Modified: Tue, 14 Apr 2026 21:07:48 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6508587f65ad7bc80506629c5050f641a67b576390527bd50028d116a6e59e`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7e4b16927cdba1f56bfd47ee4f0ec91f03eb4d54665950de0e690a8cf591a7`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1e6f397ed251ea4fa0fb49b33654ae0a4f21051946b31de5b6298d957e07df`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14bd7d3b9f81e641b929a92168f2988f89f7d48ff296f269386fa26ee6004909`  
		Last Modified: Tue, 14 Apr 2026 21:07:46 GMT  
		Size: 479.0 KB (479045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a93be0fe778d54bf31dbf755152bca8e716fe3b4a6a26a6363bf6eefb86f0c`  
		Last Modified: Tue, 14 Apr 2026 21:07:48 GMT  
		Size: 7.0 MB (7018960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d6f1157c852a3b84dc8acc8da41f4341b89ad594de182595b028d6cfc5cc59`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b986f7ba00c261673bec4ea3a233599f672f19ee33681b8e984c027d03cf366`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfefa8af6da8003b32230316fcacc30569cbe0a4231b6f6e19a2b68fe7ba5ae8`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f7ff6f050a295adfee7c011b0dee2b54a41677aa16389632062d6bb6b5a6ee`  
		Last Modified: Tue, 14 Apr 2026 21:07:44 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12`

```console
$ docker pull nats@sha256:fd76fc5a1fd3e8e1b8c14ef1ddd04f9b379df11bb73e48ff417eb12b07e4c387
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12` - linux; amd64

```console
$ docker pull nats@sha256:ecb873658a349d84b05ab89ccdc9dc3d3153e45b1c32f344c56383cfe78090ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0247f7685ff68b4ae975febd9a287b05bfd142373a9ddeb8c2dac6bfbc859`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040b24667adc09216d21ad3439155962ccadd3d91a63d56b7da7fc06ee4af8d`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:248f347c9c2745bce92c2706cb33a87211172a8f8e92087fdc501d07f7b8de4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43eac3eec77ccc736e40ad70b7026f77225ac7e5837afeb1a08f32fdd7d0b93`

```dockerfile
```

-	Layers:
	-	`sha256:d702fbcd1bfaedd00e8319117145a6389d6ea5e0c82a9d42f3162b728faeb4e5`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:6b0b00a37ddb7979ca235c35428c360669c9da2bcfa9233ae1ac9be85d0d4345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444254e21a5a8780d3528d8d19efbf156e2c5abdbb0cfe9788f1d1eedab18e2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:38 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1a6f37e82fee0dcce9cf7e8571403adb7ce8ca76666035b362c31649f4b2e`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:550334371afd2696f12dac3fd3739eea092ac27f6b0b773744e87d63aae577e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63dfea61fd8fa9fa90c1a671898c3ff2dc3edfc998eb6478ee5c9b3e5f33d7f`

```dockerfile
```

-	Layers:
	-	`sha256:958b223cfdb0c6fadea45187b0bf34bd7314cdb490d8581c32cd73f85ef90ae5`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:88aeaaa7e2045ccc03915e3f388f392216411e3fa768956ec3b12003643e8697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e37b72ad4a2af972471eebaedf8daa75a569452f35b1ab43ebe86fab23da376`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79c24a16cb2f9ad04dc2e860c74b6a0c8653d0340378eda7c4a9db7fac2f355`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:b8ac0ce4a3228e54e91056d63c0aad4573821af86e16530e157710c2c2f48ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e7d98c930153daa0f647ce1a34edcfacc5ba63ac0cdbfab10485093d0fc0fa`

```dockerfile
```

-	Layers:
	-	`sha256:070f2bbece5473f2c0c55e418b792510a0febdefaba18480714cf7dc0da44524`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:00ace04168cdf245f42a3b4e51001be65d57b2688ba37ceb571c858367f82091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942ee14c16718cb6b226080a269139173f826f4c57756120cbabb10a04312a41`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831958881aa7c7363f4962a6a305dd34529b5a3b6f9fe34ea0c550a9a93123a`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:04f4203ae702f8e1b57048b7f4a4562fadedd65a9a8052c10c5da32881a66567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ade1f2cedf562271f325ad67e73e55747b1a3765d3cfc1376e87cfa671e8d4`

```dockerfile
```

-	Layers:
	-	`sha256:29172cfd963721f0ae26556bb1349dee2b0977a97ef6c34ef44f7ad4eeb9a594`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; ppc64le

```console
$ docker pull nats@sha256:fdf8115b60259ac2622bdde6924f704a6275feb0d6cd65e38f4aa7a571791656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd15e3d70e85b851f5786bcc5592cef3d495bd850f8f7cbcdc0ca7c700408b2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47da5cb15f63124b6ff2f092feb178a9029685c93134a876733691494c5cf9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:c2a87cab23bdc37d169c93959e3ec821a456c1680a6551a7f5cf61acf16280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86a55fa4e6f66b879978374fa109f719ada684dd8a92f7ccda530fcbc8737`

```dockerfile
```

-	Layers:
	-	`sha256:7568c1ce7de6a041e52b780d3fd8b6872d5da377f7ac920fca57449c782c748c`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; s390x

```console
$ docker pull nats@sha256:7baa159ac707369edf5af5b2c2b7c240c82bd34149b3260dceee7ad5638d53cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d4acd870d3458242a8422ca0164de8903a47ffd0780a6b728485e25dac57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:08 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df52bd1462bfd4be75daf7de0a883ef6e005cb317917ea033fc18ee8368eb7`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:5ff7a0dfeaa6f2d4722d44dd6c709280ee35981ac7914b9dbfe21f57553e8a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c64e47e3edc168434146e3dec0c50abffdc23b6ec839ab026d2b9f10ce86c8`

```dockerfile
```

-	Layers:
	-	`sha256:8c8467bb933eef06e5af049586ab2e9b851e9f07b23dc34a6533b00f8f1ddeff`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-alpine`

```console
$ docker pull nats@sha256:eafac85ab07d22f58da852c2be738ffebf9a426771ae0f6bc3d77cc58818f398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-alpine` - linux; amd64

```console
$ docker pull nats@sha256:2a575d676756410fc6468bfc0cc88a737ca244f800345756bbfe3f51df7a26f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7a8652ac9a57d88b7b40e3468f37e97a13c6f83fdb55e5b3f4d501ed10cbba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f79ffd9ff103bc84a4800bd77e3a21a2b8aa5283bb96c8971b80bc0f0b1325`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 7.1 MB (7104675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7565af587bddcdc18a03e6d18c244de584dbbee0a1345791c5f92af76834e52f`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fd907441994b474d09f8910bae025fe95188bfac1759e8191422eb0806c011`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d9b67e61825abfcca68a09f5f2217e3f9f0795bcfd5ae6b25f56d4a4d76244de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e9861b72a9f751c02868a963b26d866e3ed901dc51bc7adcf8c2d2988ef18f`

```dockerfile
```

-	Layers:
	-	`sha256:3638b25e681bd6c5f215250ca0fdd8b3af5c729dcecee3cf902cc5377613f375`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1493f7a8377a4c8f6aa2255676a9abf26baa6454afe853563c3226fb29ee24f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f53595b626382736d722114880915656af1c69519b90cb0f988cccbe55e502e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81a6c31c98e9d23f13c3e1f907bead88c63e1da172c607f1cf5e98bf39b2cfb`  
		Last Modified: Tue, 14 Apr 2026 19:18:19 GMT  
		Size: 6.8 MB (6824527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e93485e87180b419b674b3eaaefe0fb6cb8149f771a85b32884d318565c5b0d`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab1cdedb45964719fb488c1020b53f079ddd692ec19aa9224bcd4185b2f44cf`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a55de7e7cbe420676cde9540a343d1477bea77e79079b607e4ed24f48a7f3ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3362d5291b6a280bab2b1508a6cd3d6d0f5dc5beafa83a4cd908c971e0c2dbc9`

```dockerfile
```

-	Layers:
	-	`sha256:b608191e207ea42ead772d1c93799d794f7bcaf6248843f91721426b28e54576`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:43d26a2a5012f9e5cbb5f3a569bec60a0f31caff9241f2bea12c55576b20b43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b907f2c013544f942a4b8eb34f5dd75ec12f99e82cd0354ff8076468f5bd4a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a506cbdb04d5f850a7e6d7efad2de37c9281f87153355ae9f158463b8863c16`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 6.8 MB (6813977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f012309da8651a720251bebe8d821117e4af8a880054b044d6f9b77cb9bbd`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30097ae043c1bed74c22084b0906018b9e291c295790a03eb6e3c9be52d0585d`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b21ee8f249ab3c650417c4b20f0a8f05ef07196d420c9f2c03ff12d4f870dc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b6611241f2f57bb7846e1cc9646e70116cfb3b87ea4b5edffbaf1fcefe58a`

```dockerfile
```

-	Layers:
	-	`sha256:dd1462a37a47fe62aa5690e6fd6caccf9edd80f3b23d4f1537ff421f2c1db1b2`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ddfc383507987a61ec6ad0842ce9bedfa1c0dc8b0b61e20bf66f4ea1891c963f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10651943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e62a2c6d295007873d27b02e9bfb4b0d35219b9d38537a45aafe2a781a7ef8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75374d2efd25789f733679c46deb8015d53a34ffc525b1a5be14458cfaa7c572`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 6.5 MB (6511455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0469dd7527f8e826ccbde70f8429eb6445d7f986f67412ce5e6fe4f5efe762a`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fd106169b64170292228a08cc598dd7086fd77cb227d8b493a9442da8f2f03`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c7745ae505e872b9e322bfc8b2f28d8d6f912d9cb77ef8fa4800676ff12f3e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040e174862b564526a86b8abfa14447199c7b3218c59218d695b784bff14213c`

```dockerfile
```

-	Layers:
	-	`sha256:c6ee43bf4bf2b5f9d032ec8ac9655bf3944c1926ec48a04662fddfe77bbba8d5`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:8177663ab814155404ddd225210e864a8db5f5bab6524fcd538e1c50e95b5ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c112147b37f5f3a82942b342ae66fbac493141594055744e01168da49832e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:23:16 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:23:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:23:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3016f09e58e2224328d6b41bb77318fceda5b54269054dde87e90e5c78a5850`  
		Last Modified: Tue, 14 Apr 2026 19:23:32 GMT  
		Size: 6.6 MB (6561426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac87bfa474f24897ae62b339e8d3e99d2477339cb9c7b9c9c27fe53e05575a`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5caa4d61a9b6f6e771c2817dc9c2d7f2b7737c8d5ba3352063ae308e6ba4bb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1076c83f11053262280ca29e78934d54c350126d3bf945008131c45e30051279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2883b8d290089c7ecab48a7da59f92c662d33b5b0eb9d670e0b0f444447fe585`

```dockerfile
```

-	Layers:
	-	`sha256:56648b6f8b6b7d991ee9afea4af9d02a29fed6e3de695d2669ff6a10e1c66ad2`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:0382580cb171a9ef5220b58d8f8476e825dd541e23ddd9261c83fe81077c687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10593579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbff052312601b8843e5c7f71ffd689bab23a0bbc6c559f906df56d2ab3ad4cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe3d8c0011da8faf0966aa9995120fdc77207edbfce2a78a12b7ffa0e66cdee`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 6.9 MB (6942178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db786c0b404f3ce6941db702d0a29b1f7f7a2da1f5178eb375ae02a6864fb69`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaae1336b66f9d4544d0dada462003e4b60143899cc7d520d196916b4b2a931`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6bfbfebce9888aad4a527e1f5b945818e5241836164846ce875432b1e6bba4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d469341abe6fbb7b778259a810bc75cf066eabd0da34b49bac83dc9b756113`

```dockerfile
```

-	Layers:
	-	`sha256:25df845b450fa255e51db23f7115c4c5986bcc435fb73ff38329d7f8bcebbd2e`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-alpine3.22`

```console
$ docker pull nats@sha256:eafac85ab07d22f58da852c2be738ffebf9a426771ae0f6bc3d77cc58818f398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:2a575d676756410fc6468bfc0cc88a737ca244f800345756bbfe3f51df7a26f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7a8652ac9a57d88b7b40e3468f37e97a13c6f83fdb55e5b3f4d501ed10cbba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f79ffd9ff103bc84a4800bd77e3a21a2b8aa5283bb96c8971b80bc0f0b1325`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 7.1 MB (7104675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7565af587bddcdc18a03e6d18c244de584dbbee0a1345791c5f92af76834e52f`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fd907441994b474d09f8910bae025fe95188bfac1759e8191422eb0806c011`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d9b67e61825abfcca68a09f5f2217e3f9f0795bcfd5ae6b25f56d4a4d76244de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e9861b72a9f751c02868a963b26d866e3ed901dc51bc7adcf8c2d2988ef18f`

```dockerfile
```

-	Layers:
	-	`sha256:3638b25e681bd6c5f215250ca0fdd8b3af5c729dcecee3cf902cc5377613f375`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:1493f7a8377a4c8f6aa2255676a9abf26baa6454afe853563c3226fb29ee24f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f53595b626382736d722114880915656af1c69519b90cb0f988cccbe55e502e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81a6c31c98e9d23f13c3e1f907bead88c63e1da172c607f1cf5e98bf39b2cfb`  
		Last Modified: Tue, 14 Apr 2026 19:18:19 GMT  
		Size: 6.8 MB (6824527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e93485e87180b419b674b3eaaefe0fb6cb8149f771a85b32884d318565c5b0d`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab1cdedb45964719fb488c1020b53f079ddd692ec19aa9224bcd4185b2f44cf`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a55de7e7cbe420676cde9540a343d1477bea77e79079b607e4ed24f48a7f3ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3362d5291b6a280bab2b1508a6cd3d6d0f5dc5beafa83a4cd908c971e0c2dbc9`

```dockerfile
```

-	Layers:
	-	`sha256:b608191e207ea42ead772d1c93799d794f7bcaf6248843f91721426b28e54576`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:43d26a2a5012f9e5cbb5f3a569bec60a0f31caff9241f2bea12c55576b20b43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b907f2c013544f942a4b8eb34f5dd75ec12f99e82cd0354ff8076468f5bd4a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a506cbdb04d5f850a7e6d7efad2de37c9281f87153355ae9f158463b8863c16`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 6.8 MB (6813977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f012309da8651a720251bebe8d821117e4af8a880054b044d6f9b77cb9bbd`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30097ae043c1bed74c22084b0906018b9e291c295790a03eb6e3c9be52d0585d`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b21ee8f249ab3c650417c4b20f0a8f05ef07196d420c9f2c03ff12d4f870dc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b6611241f2f57bb7846e1cc9646e70116cfb3b87ea4b5edffbaf1fcefe58a`

```dockerfile
```

-	Layers:
	-	`sha256:dd1462a37a47fe62aa5690e6fd6caccf9edd80f3b23d4f1537ff421f2c1db1b2`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ddfc383507987a61ec6ad0842ce9bedfa1c0dc8b0b61e20bf66f4ea1891c963f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10651943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e62a2c6d295007873d27b02e9bfb4b0d35219b9d38537a45aafe2a781a7ef8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75374d2efd25789f733679c46deb8015d53a34ffc525b1a5be14458cfaa7c572`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 6.5 MB (6511455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0469dd7527f8e826ccbde70f8429eb6445d7f986f67412ce5e6fe4f5efe762a`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fd106169b64170292228a08cc598dd7086fd77cb227d8b493a9442da8f2f03`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c7745ae505e872b9e322bfc8b2f28d8d6f912d9cb77ef8fa4800676ff12f3e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040e174862b564526a86b8abfa14447199c7b3218c59218d695b784bff14213c`

```dockerfile
```

-	Layers:
	-	`sha256:c6ee43bf4bf2b5f9d032ec8ac9655bf3944c1926ec48a04662fddfe77bbba8d5`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:8177663ab814155404ddd225210e864a8db5f5bab6524fcd538e1c50e95b5ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c112147b37f5f3a82942b342ae66fbac493141594055744e01168da49832e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:23:16 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:23:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:23:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3016f09e58e2224328d6b41bb77318fceda5b54269054dde87e90e5c78a5850`  
		Last Modified: Tue, 14 Apr 2026 19:23:32 GMT  
		Size: 6.6 MB (6561426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac87bfa474f24897ae62b339e8d3e99d2477339cb9c7b9c9c27fe53e05575a`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5caa4d61a9b6f6e771c2817dc9c2d7f2b7737c8d5ba3352063ae308e6ba4bb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:1076c83f11053262280ca29e78934d54c350126d3bf945008131c45e30051279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2883b8d290089c7ecab48a7da59f92c662d33b5b0eb9d670e0b0f444447fe585`

```dockerfile
```

-	Layers:
	-	`sha256:56648b6f8b6b7d991ee9afea4af9d02a29fed6e3de695d2669ff6a10e1c66ad2`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:0382580cb171a9ef5220b58d8f8476e825dd541e23ddd9261c83fe81077c687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10593579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbff052312601b8843e5c7f71ffd689bab23a0bbc6c559f906df56d2ab3ad4cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe3d8c0011da8faf0966aa9995120fdc77207edbfce2a78a12b7ffa0e66cdee`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 6.9 MB (6942178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db786c0b404f3ce6941db702d0a29b1f7f7a2da1f5178eb375ae02a6864fb69`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaae1336b66f9d4544d0dada462003e4b60143899cc7d520d196916b4b2a931`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6bfbfebce9888aad4a527e1f5b945818e5241836164846ce875432b1e6bba4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d469341abe6fbb7b778259a810bc75cf066eabd0da34b49bac83dc9b756113`

```dockerfile
```

-	Layers:
	-	`sha256:25df845b450fa255e51db23f7115c4c5986bcc435fb73ff38329d7f8bcebbd2e`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-linux`

```console
$ docker pull nats@sha256:d2b16b7517a2dd973e0999b071e016485a9a08c82b5369cc1ce858af54587e93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-linux` - linux; amd64

```console
$ docker pull nats@sha256:ecb873658a349d84b05ab89ccdc9dc3d3153e45b1c32f344c56383cfe78090ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0247f7685ff68b4ae975febd9a287b05bfd142373a9ddeb8c2dac6bfbc859`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040b24667adc09216d21ad3439155962ccadd3d91a63d56b7da7fc06ee4af8d`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:248f347c9c2745bce92c2706cb33a87211172a8f8e92087fdc501d07f7b8de4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43eac3eec77ccc736e40ad70b7026f77225ac7e5837afeb1a08f32fdd7d0b93`

```dockerfile
```

-	Layers:
	-	`sha256:d702fbcd1bfaedd00e8319117145a6389d6ea5e0c82a9d42f3162b728faeb4e5`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6b0b00a37ddb7979ca235c35428c360669c9da2bcfa9233ae1ac9be85d0d4345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444254e21a5a8780d3528d8d19efbf156e2c5abdbb0cfe9788f1d1eedab18e2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:38 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1a6f37e82fee0dcce9cf7e8571403adb7ce8ca76666035b362c31649f4b2e`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:550334371afd2696f12dac3fd3739eea092ac27f6b0b773744e87d63aae577e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63dfea61fd8fa9fa90c1a671898c3ff2dc3edfc998eb6478ee5c9b3e5f33d7f`

```dockerfile
```

-	Layers:
	-	`sha256:958b223cfdb0c6fadea45187b0bf34bd7314cdb490d8581c32cd73f85ef90ae5`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:88aeaaa7e2045ccc03915e3f388f392216411e3fa768956ec3b12003643e8697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e37b72ad4a2af972471eebaedf8daa75a569452f35b1ab43ebe86fab23da376`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79c24a16cb2f9ad04dc2e860c74b6a0c8653d0340378eda7c4a9db7fac2f355`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b8ac0ce4a3228e54e91056d63c0aad4573821af86e16530e157710c2c2f48ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e7d98c930153daa0f647ce1a34edcfacc5ba63ac0cdbfab10485093d0fc0fa`

```dockerfile
```

-	Layers:
	-	`sha256:070f2bbece5473f2c0c55e418b792510a0febdefaba18480714cf7dc0da44524`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:00ace04168cdf245f42a3b4e51001be65d57b2688ba37ceb571c858367f82091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942ee14c16718cb6b226080a269139173f826f4c57756120cbabb10a04312a41`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831958881aa7c7363f4962a6a305dd34529b5a3b6f9fe34ea0c550a9a93123a`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:04f4203ae702f8e1b57048b7f4a4562fadedd65a9a8052c10c5da32881a66567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ade1f2cedf562271f325ad67e73e55747b1a3765d3cfc1376e87cfa671e8d4`

```dockerfile
```

-	Layers:
	-	`sha256:29172cfd963721f0ae26556bb1349dee2b0977a97ef6c34ef44f7ad4eeb9a594`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:fdf8115b60259ac2622bdde6924f704a6275feb0d6cd65e38f4aa7a571791656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd15e3d70e85b851f5786bcc5592cef3d495bd850f8f7cbcdc0ca7c700408b2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47da5cb15f63124b6ff2f092feb178a9029685c93134a876733691494c5cf9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c2a87cab23bdc37d169c93959e3ec821a456c1680a6551a7f5cf61acf16280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86a55fa4e6f66b879978374fa109f719ada684dd8a92f7ccda530fcbc8737`

```dockerfile
```

-	Layers:
	-	`sha256:7568c1ce7de6a041e52b780d3fd8b6872d5da377f7ac920fca57449c782c748c`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; s390x

```console
$ docker pull nats@sha256:7baa159ac707369edf5af5b2c2b7c240c82bd34149b3260dceee7ad5638d53cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d4acd870d3458242a8422ca0164de8903a47ffd0780a6b728485e25dac57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:08 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df52bd1462bfd4be75daf7de0a883ef6e005cb317917ea033fc18ee8368eb7`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5ff7a0dfeaa6f2d4722d44dd6c709280ee35981ac7914b9dbfe21f57553e8a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c64e47e3edc168434146e3dec0c50abffdc23b6ec839ab026d2b9f10ce86c8`

```dockerfile
```

-	Layers:
	-	`sha256:8c8467bb933eef06e5af049586ab2e9b851e9f07b23dc34a6533b00f8f1ddeff`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-nanoserver`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-scratch`

```console
$ docker pull nats@sha256:d2b16b7517a2dd973e0999b071e016485a9a08c82b5369cc1ce858af54587e93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12-scratch` - linux; amd64

```console
$ docker pull nats@sha256:ecb873658a349d84b05ab89ccdc9dc3d3153e45b1c32f344c56383cfe78090ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0247f7685ff68b4ae975febd9a287b05bfd142373a9ddeb8c2dac6bfbc859`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040b24667adc09216d21ad3439155962ccadd3d91a63d56b7da7fc06ee4af8d`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:248f347c9c2745bce92c2706cb33a87211172a8f8e92087fdc501d07f7b8de4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43eac3eec77ccc736e40ad70b7026f77225ac7e5837afeb1a08f32fdd7d0b93`

```dockerfile
```

-	Layers:
	-	`sha256:d702fbcd1bfaedd00e8319117145a6389d6ea5e0c82a9d42f3162b728faeb4e5`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:6b0b00a37ddb7979ca235c35428c360669c9da2bcfa9233ae1ac9be85d0d4345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444254e21a5a8780d3528d8d19efbf156e2c5abdbb0cfe9788f1d1eedab18e2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:38 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1a6f37e82fee0dcce9cf7e8571403adb7ce8ca76666035b362c31649f4b2e`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:550334371afd2696f12dac3fd3739eea092ac27f6b0b773744e87d63aae577e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63dfea61fd8fa9fa90c1a671898c3ff2dc3edfc998eb6478ee5c9b3e5f33d7f`

```dockerfile
```

-	Layers:
	-	`sha256:958b223cfdb0c6fadea45187b0bf34bd7314cdb490d8581c32cd73f85ef90ae5`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:88aeaaa7e2045ccc03915e3f388f392216411e3fa768956ec3b12003643e8697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e37b72ad4a2af972471eebaedf8daa75a569452f35b1ab43ebe86fab23da376`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79c24a16cb2f9ad04dc2e860c74b6a0c8653d0340378eda7c4a9db7fac2f355`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b8ac0ce4a3228e54e91056d63c0aad4573821af86e16530e157710c2c2f48ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e7d98c930153daa0f647ce1a34edcfacc5ba63ac0cdbfab10485093d0fc0fa`

```dockerfile
```

-	Layers:
	-	`sha256:070f2bbece5473f2c0c55e418b792510a0febdefaba18480714cf7dc0da44524`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:00ace04168cdf245f42a3b4e51001be65d57b2688ba37ceb571c858367f82091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942ee14c16718cb6b226080a269139173f826f4c57756120cbabb10a04312a41`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831958881aa7c7363f4962a6a305dd34529b5a3b6f9fe34ea0c550a9a93123a`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:04f4203ae702f8e1b57048b7f4a4562fadedd65a9a8052c10c5da32881a66567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ade1f2cedf562271f325ad67e73e55747b1a3765d3cfc1376e87cfa671e8d4`

```dockerfile
```

-	Layers:
	-	`sha256:29172cfd963721f0ae26556bb1349dee2b0977a97ef6c34ef44f7ad4eeb9a594`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:fdf8115b60259ac2622bdde6924f704a6275feb0d6cd65e38f4aa7a571791656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd15e3d70e85b851f5786bcc5592cef3d495bd850f8f7cbcdc0ca7c700408b2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47da5cb15f63124b6ff2f092feb178a9029685c93134a876733691494c5cf9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c2a87cab23bdc37d169c93959e3ec821a456c1680a6551a7f5cf61acf16280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86a55fa4e6f66b879978374fa109f719ada684dd8a92f7ccda530fcbc8737`

```dockerfile
```

-	Layers:
	-	`sha256:7568c1ce7de6a041e52b780d3fd8b6872d5da377f7ac920fca57449c782c748c`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; s390x

```console
$ docker pull nats@sha256:7baa159ac707369edf5af5b2c2b7c240c82bd34149b3260dceee7ad5638d53cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d4acd870d3458242a8422ca0164de8903a47ffd0780a6b728485e25dac57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:08 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df52bd1462bfd4be75daf7de0a883ef6e005cb317917ea033fc18ee8368eb7`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5ff7a0dfeaa6f2d4722d44dd6c709280ee35981ac7914b9dbfe21f57553e8a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c64e47e3edc168434146e3dec0c50abffdc23b6ec839ab026d2b9f10ce86c8`

```dockerfile
```

-	Layers:
	-	`sha256:8c8467bb933eef06e5af049586ab2e9b851e9f07b23dc34a6533b00f8f1ddeff`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-windowsservercore`

```console
$ docker pull nats@sha256:184cb774079b425716c5507364372954c455f9142c93d1bc466677ac2cc75ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:7790fa4d3db94cf7c89a7688f3f84537bb75287e452f1e554c1588a661d15cb1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077873124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a342bd15d69991f8343f2d756a7638e87fdfa2d5562cb647249e12b2bc09ae8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:06:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:06:25 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:06:26 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 21:06:26 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 21:06:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.7/nats-server-v2.12.7-windows-amd64.zip
# Tue, 14 Apr 2026 21:06:29 GMT
ENV NATS_SERVER_SHASUM=4e7880619018ccebe2aa9372a9a8bc362081a7414f93638143ea6d8049892146
# Tue, 14 Apr 2026 21:06:33 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Apr 2026 21:06:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Apr 2026 21:06:49 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:06:50 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:06:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:06:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234f0c5dc55953d98e0d13e9e881a65f871f8e0476a39dc8074be17e88c96ab`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e8f504a62653497a194c864fb383113d6df01412a46e631c3118b188201760`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d82249fabc12bddf45ee14ee15697a564705a6bae958426abd5f4e10bb35ed`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fce0a83450991329209dbbba5426b504eb424ca3c01086d950fe682844645f`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313c950879461faccbfdbe49b49b7ae9078f4f5f4440ac5d858ef0957df5ed6`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae88d9973cc6300fad7210fd6ceec8ad6f50c2a3521ea7a13d0dbd3039da44d6`  
		Last Modified: Tue, 14 Apr 2026 21:06:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5cbd1df81d61159af069584f9c11905a89d3b37b3bf4c04d8824003ec45c0`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 476.1 KB (476100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d18ee910801df31fa7a1ce17acaac50b7ec97bad952d423d008642554a5ebd9`  
		Last Modified: Tue, 14 Apr 2026 21:07:00 GMT  
		Size: 7.2 MB (7172018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd64f7fcdcc6dc03c3975a663297e49a35d229c0406f0ee49d954c76c7becb45`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.9 KB (1896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd424273b8b84b6ff389aa4eef9af352a6544807e63270647cc147eb2965112d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca72c491cc10f7581d8eb027dc3737bd51ab476833369bb5c2e9d80865d9521`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d050d88a8b0417554b75e53d2839e21fe0c82d7e9104c71eeb8648e9600fbe6d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:184cb774079b425716c5507364372954c455f9142c93d1bc466677ac2cc75ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:7790fa4d3db94cf7c89a7688f3f84537bb75287e452f1e554c1588a661d15cb1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077873124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a342bd15d69991f8343f2d756a7638e87fdfa2d5562cb647249e12b2bc09ae8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:06:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:06:25 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:06:26 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 21:06:26 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 21:06:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.7/nats-server-v2.12.7-windows-amd64.zip
# Tue, 14 Apr 2026 21:06:29 GMT
ENV NATS_SERVER_SHASUM=4e7880619018ccebe2aa9372a9a8bc362081a7414f93638143ea6d8049892146
# Tue, 14 Apr 2026 21:06:33 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Apr 2026 21:06:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Apr 2026 21:06:49 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:06:50 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:06:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:06:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234f0c5dc55953d98e0d13e9e881a65f871f8e0476a39dc8074be17e88c96ab`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e8f504a62653497a194c864fb383113d6df01412a46e631c3118b188201760`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d82249fabc12bddf45ee14ee15697a564705a6bae958426abd5f4e10bb35ed`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fce0a83450991329209dbbba5426b504eb424ca3c01086d950fe682844645f`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313c950879461faccbfdbe49b49b7ae9078f4f5f4440ac5d858ef0957df5ed6`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae88d9973cc6300fad7210fd6ceec8ad6f50c2a3521ea7a13d0dbd3039da44d6`  
		Last Modified: Tue, 14 Apr 2026 21:06:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5cbd1df81d61159af069584f9c11905a89d3b37b3bf4c04d8824003ec45c0`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 476.1 KB (476100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d18ee910801df31fa7a1ce17acaac50b7ec97bad952d423d008642554a5ebd9`  
		Last Modified: Tue, 14 Apr 2026 21:07:00 GMT  
		Size: 7.2 MB (7172018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd64f7fcdcc6dc03c3975a663297e49a35d229c0406f0ee49d954c76c7becb45`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.9 KB (1896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd424273b8b84b6ff389aa4eef9af352a6544807e63270647cc147eb2965112d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca72c491cc10f7581d8eb027dc3737bd51ab476833369bb5c2e9d80865d9521`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d050d88a8b0417554b75e53d2839e21fe0c82d7e9104c71eeb8648e9600fbe6d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.7`

```console
$ docker pull nats@sha256:fd76fc5a1fd3e8e1b8c14ef1ddd04f9b379df11bb73e48ff417eb12b07e4c387
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12.7` - linux; amd64

```console
$ docker pull nats@sha256:ecb873658a349d84b05ab89ccdc9dc3d3153e45b1c32f344c56383cfe78090ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0247f7685ff68b4ae975febd9a287b05bfd142373a9ddeb8c2dac6bfbc859`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040b24667adc09216d21ad3439155962ccadd3d91a63d56b7da7fc06ee4af8d`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7` - unknown; unknown

```console
$ docker pull nats@sha256:248f347c9c2745bce92c2706cb33a87211172a8f8e92087fdc501d07f7b8de4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43eac3eec77ccc736e40ad70b7026f77225ac7e5837afeb1a08f32fdd7d0b93`

```dockerfile
```

-	Layers:
	-	`sha256:d702fbcd1bfaedd00e8319117145a6389d6ea5e0c82a9d42f3162b728faeb4e5`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7` - linux; arm variant v6

```console
$ docker pull nats@sha256:6b0b00a37ddb7979ca235c35428c360669c9da2bcfa9233ae1ac9be85d0d4345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444254e21a5a8780d3528d8d19efbf156e2c5abdbb0cfe9788f1d1eedab18e2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:38 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1a6f37e82fee0dcce9cf7e8571403adb7ce8ca76666035b362c31649f4b2e`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7` - unknown; unknown

```console
$ docker pull nats@sha256:550334371afd2696f12dac3fd3739eea092ac27f6b0b773744e87d63aae577e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63dfea61fd8fa9fa90c1a671898c3ff2dc3edfc998eb6478ee5c9b3e5f33d7f`

```dockerfile
```

-	Layers:
	-	`sha256:958b223cfdb0c6fadea45187b0bf34bd7314cdb490d8581c32cd73f85ef90ae5`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7` - linux; arm variant v7

```console
$ docker pull nats@sha256:88aeaaa7e2045ccc03915e3f388f392216411e3fa768956ec3b12003643e8697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e37b72ad4a2af972471eebaedf8daa75a569452f35b1ab43ebe86fab23da376`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79c24a16cb2f9ad04dc2e860c74b6a0c8653d0340378eda7c4a9db7fac2f355`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7` - unknown; unknown

```console
$ docker pull nats@sha256:b8ac0ce4a3228e54e91056d63c0aad4573821af86e16530e157710c2c2f48ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e7d98c930153daa0f647ce1a34edcfacc5ba63ac0cdbfab10485093d0fc0fa`

```dockerfile
```

-	Layers:
	-	`sha256:070f2bbece5473f2c0c55e418b792510a0febdefaba18480714cf7dc0da44524`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:00ace04168cdf245f42a3b4e51001be65d57b2688ba37ceb571c858367f82091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942ee14c16718cb6b226080a269139173f826f4c57756120cbabb10a04312a41`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831958881aa7c7363f4962a6a305dd34529b5a3b6f9fe34ea0c550a9a93123a`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7` - unknown; unknown

```console
$ docker pull nats@sha256:04f4203ae702f8e1b57048b7f4a4562fadedd65a9a8052c10c5da32881a66567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ade1f2cedf562271f325ad67e73e55747b1a3765d3cfc1376e87cfa671e8d4`

```dockerfile
```

-	Layers:
	-	`sha256:29172cfd963721f0ae26556bb1349dee2b0977a97ef6c34ef44f7ad4eeb9a594`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7` - linux; ppc64le

```console
$ docker pull nats@sha256:fdf8115b60259ac2622bdde6924f704a6275feb0d6cd65e38f4aa7a571791656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd15e3d70e85b851f5786bcc5592cef3d495bd850f8f7cbcdc0ca7c700408b2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47da5cb15f63124b6ff2f092feb178a9029685c93134a876733691494c5cf9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7` - unknown; unknown

```console
$ docker pull nats@sha256:c2a87cab23bdc37d169c93959e3ec821a456c1680a6551a7f5cf61acf16280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86a55fa4e6f66b879978374fa109f719ada684dd8a92f7ccda530fcbc8737`

```dockerfile
```

-	Layers:
	-	`sha256:7568c1ce7de6a041e52b780d3fd8b6872d5da377f7ac920fca57449c782c748c`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7` - linux; s390x

```console
$ docker pull nats@sha256:7baa159ac707369edf5af5b2c2b7c240c82bd34149b3260dceee7ad5638d53cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d4acd870d3458242a8422ca0164de8903a47ffd0780a6b728485e25dac57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:08 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df52bd1462bfd4be75daf7de0a883ef6e005cb317917ea033fc18ee8368eb7`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7` - unknown; unknown

```console
$ docker pull nats@sha256:5ff7a0dfeaa6f2d4722d44dd6c709280ee35981ac7914b9dbfe21f57553e8a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c64e47e3edc168434146e3dec0c50abffdc23b6ec839ab026d2b9f10ce86c8`

```dockerfile
```

-	Layers:
	-	`sha256:8c8467bb933eef06e5af049586ab2e9b851e9f07b23dc34a6533b00f8f1ddeff`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.7-alpine`

```console
$ docker pull nats@sha256:eafac85ab07d22f58da852c2be738ffebf9a426771ae0f6bc3d77cc58818f398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12.7-alpine` - linux; amd64

```console
$ docker pull nats@sha256:2a575d676756410fc6468bfc0cc88a737ca244f800345756bbfe3f51df7a26f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7a8652ac9a57d88b7b40e3468f37e97a13c6f83fdb55e5b3f4d501ed10cbba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f79ffd9ff103bc84a4800bd77e3a21a2b8aa5283bb96c8971b80bc0f0b1325`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 7.1 MB (7104675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7565af587bddcdc18a03e6d18c244de584dbbee0a1345791c5f92af76834e52f`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fd907441994b474d09f8910bae025fe95188bfac1759e8191422eb0806c011`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d9b67e61825abfcca68a09f5f2217e3f9f0795bcfd5ae6b25f56d4a4d76244de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e9861b72a9f751c02868a963b26d866e3ed901dc51bc7adcf8c2d2988ef18f`

```dockerfile
```

-	Layers:
	-	`sha256:3638b25e681bd6c5f215250ca0fdd8b3af5c729dcecee3cf902cc5377613f375`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1493f7a8377a4c8f6aa2255676a9abf26baa6454afe853563c3226fb29ee24f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f53595b626382736d722114880915656af1c69519b90cb0f988cccbe55e502e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81a6c31c98e9d23f13c3e1f907bead88c63e1da172c607f1cf5e98bf39b2cfb`  
		Last Modified: Tue, 14 Apr 2026 19:18:19 GMT  
		Size: 6.8 MB (6824527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e93485e87180b419b674b3eaaefe0fb6cb8149f771a85b32884d318565c5b0d`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab1cdedb45964719fb488c1020b53f079ddd692ec19aa9224bcd4185b2f44cf`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a55de7e7cbe420676cde9540a343d1477bea77e79079b607e4ed24f48a7f3ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3362d5291b6a280bab2b1508a6cd3d6d0f5dc5beafa83a4cd908c971e0c2dbc9`

```dockerfile
```

-	Layers:
	-	`sha256:b608191e207ea42ead772d1c93799d794f7bcaf6248843f91721426b28e54576`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:43d26a2a5012f9e5cbb5f3a569bec60a0f31caff9241f2bea12c55576b20b43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b907f2c013544f942a4b8eb34f5dd75ec12f99e82cd0354ff8076468f5bd4a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a506cbdb04d5f850a7e6d7efad2de37c9281f87153355ae9f158463b8863c16`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 6.8 MB (6813977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f012309da8651a720251bebe8d821117e4af8a880054b044d6f9b77cb9bbd`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30097ae043c1bed74c22084b0906018b9e291c295790a03eb6e3c9be52d0585d`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b21ee8f249ab3c650417c4b20f0a8f05ef07196d420c9f2c03ff12d4f870dc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b6611241f2f57bb7846e1cc9646e70116cfb3b87ea4b5edffbaf1fcefe58a`

```dockerfile
```

-	Layers:
	-	`sha256:dd1462a37a47fe62aa5690e6fd6caccf9edd80f3b23d4f1537ff421f2c1db1b2`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ddfc383507987a61ec6ad0842ce9bedfa1c0dc8b0b61e20bf66f4ea1891c963f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10651943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e62a2c6d295007873d27b02e9bfb4b0d35219b9d38537a45aafe2a781a7ef8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75374d2efd25789f733679c46deb8015d53a34ffc525b1a5be14458cfaa7c572`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 6.5 MB (6511455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0469dd7527f8e826ccbde70f8429eb6445d7f986f67412ce5e6fe4f5efe762a`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fd106169b64170292228a08cc598dd7086fd77cb227d8b493a9442da8f2f03`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c7745ae505e872b9e322bfc8b2f28d8d6f912d9cb77ef8fa4800676ff12f3e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040e174862b564526a86b8abfa14447199c7b3218c59218d695b784bff14213c`

```dockerfile
```

-	Layers:
	-	`sha256:c6ee43bf4bf2b5f9d032ec8ac9655bf3944c1926ec48a04662fddfe77bbba8d5`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:8177663ab814155404ddd225210e864a8db5f5bab6524fcd538e1c50e95b5ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c112147b37f5f3a82942b342ae66fbac493141594055744e01168da49832e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:23:16 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:23:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:23:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3016f09e58e2224328d6b41bb77318fceda5b54269054dde87e90e5c78a5850`  
		Last Modified: Tue, 14 Apr 2026 19:23:32 GMT  
		Size: 6.6 MB (6561426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac87bfa474f24897ae62b339e8d3e99d2477339cb9c7b9c9c27fe53e05575a`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5caa4d61a9b6f6e771c2817dc9c2d7f2b7737c8d5ba3352063ae308e6ba4bb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1076c83f11053262280ca29e78934d54c350126d3bf945008131c45e30051279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2883b8d290089c7ecab48a7da59f92c662d33b5b0eb9d670e0b0f444447fe585`

```dockerfile
```

-	Layers:
	-	`sha256:56648b6f8b6b7d991ee9afea4af9d02a29fed6e3de695d2669ff6a10e1c66ad2`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine` - linux; s390x

```console
$ docker pull nats@sha256:0382580cb171a9ef5220b58d8f8476e825dd541e23ddd9261c83fe81077c687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10593579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbff052312601b8843e5c7f71ffd689bab23a0bbc6c559f906df56d2ab3ad4cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe3d8c0011da8faf0966aa9995120fdc77207edbfce2a78a12b7ffa0e66cdee`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 6.9 MB (6942178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db786c0b404f3ce6941db702d0a29b1f7f7a2da1f5178eb375ae02a6864fb69`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaae1336b66f9d4544d0dada462003e4b60143899cc7d520d196916b4b2a931`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6bfbfebce9888aad4a527e1f5b945818e5241836164846ce875432b1e6bba4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d469341abe6fbb7b778259a810bc75cf066eabd0da34b49bac83dc9b756113`

```dockerfile
```

-	Layers:
	-	`sha256:25df845b450fa255e51db23f7115c4c5986bcc435fb73ff38329d7f8bcebbd2e`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.7-alpine3.22`

```console
$ docker pull nats@sha256:eafac85ab07d22f58da852c2be738ffebf9a426771ae0f6bc3d77cc58818f398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12.7-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:2a575d676756410fc6468bfc0cc88a737ca244f800345756bbfe3f51df7a26f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7a8652ac9a57d88b7b40e3468f37e97a13c6f83fdb55e5b3f4d501ed10cbba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f79ffd9ff103bc84a4800bd77e3a21a2b8aa5283bb96c8971b80bc0f0b1325`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 7.1 MB (7104675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7565af587bddcdc18a03e6d18c244de584dbbee0a1345791c5f92af76834e52f`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fd907441994b474d09f8910bae025fe95188bfac1759e8191422eb0806c011`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d9b67e61825abfcca68a09f5f2217e3f9f0795bcfd5ae6b25f56d4a4d76244de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e9861b72a9f751c02868a963b26d866e3ed901dc51bc7adcf8c2d2988ef18f`

```dockerfile
```

-	Layers:
	-	`sha256:3638b25e681bd6c5f215250ca0fdd8b3af5c729dcecee3cf902cc5377613f375`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:1493f7a8377a4c8f6aa2255676a9abf26baa6454afe853563c3226fb29ee24f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f53595b626382736d722114880915656af1c69519b90cb0f988cccbe55e502e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81a6c31c98e9d23f13c3e1f907bead88c63e1da172c607f1cf5e98bf39b2cfb`  
		Last Modified: Tue, 14 Apr 2026 19:18:19 GMT  
		Size: 6.8 MB (6824527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e93485e87180b419b674b3eaaefe0fb6cb8149f771a85b32884d318565c5b0d`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab1cdedb45964719fb488c1020b53f079ddd692ec19aa9224bcd4185b2f44cf`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a55de7e7cbe420676cde9540a343d1477bea77e79079b607e4ed24f48a7f3ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3362d5291b6a280bab2b1508a6cd3d6d0f5dc5beafa83a4cd908c971e0c2dbc9`

```dockerfile
```

-	Layers:
	-	`sha256:b608191e207ea42ead772d1c93799d794f7bcaf6248843f91721426b28e54576`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:43d26a2a5012f9e5cbb5f3a569bec60a0f31caff9241f2bea12c55576b20b43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b907f2c013544f942a4b8eb34f5dd75ec12f99e82cd0354ff8076468f5bd4a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a506cbdb04d5f850a7e6d7efad2de37c9281f87153355ae9f158463b8863c16`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 6.8 MB (6813977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f012309da8651a720251bebe8d821117e4af8a880054b044d6f9b77cb9bbd`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30097ae043c1bed74c22084b0906018b9e291c295790a03eb6e3c9be52d0585d`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b21ee8f249ab3c650417c4b20f0a8f05ef07196d420c9f2c03ff12d4f870dc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b6611241f2f57bb7846e1cc9646e70116cfb3b87ea4b5edffbaf1fcefe58a`

```dockerfile
```

-	Layers:
	-	`sha256:dd1462a37a47fe62aa5690e6fd6caccf9edd80f3b23d4f1537ff421f2c1db1b2`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ddfc383507987a61ec6ad0842ce9bedfa1c0dc8b0b61e20bf66f4ea1891c963f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10651943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e62a2c6d295007873d27b02e9bfb4b0d35219b9d38537a45aafe2a781a7ef8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75374d2efd25789f733679c46deb8015d53a34ffc525b1a5be14458cfaa7c572`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 6.5 MB (6511455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0469dd7527f8e826ccbde70f8429eb6445d7f986f67412ce5e6fe4f5efe762a`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fd106169b64170292228a08cc598dd7086fd77cb227d8b493a9442da8f2f03`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c7745ae505e872b9e322bfc8b2f28d8d6f912d9cb77ef8fa4800676ff12f3e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040e174862b564526a86b8abfa14447199c7b3218c59218d695b784bff14213c`

```dockerfile
```

-	Layers:
	-	`sha256:c6ee43bf4bf2b5f9d032ec8ac9655bf3944c1926ec48a04662fddfe77bbba8d5`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:8177663ab814155404ddd225210e864a8db5f5bab6524fcd538e1c50e95b5ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c112147b37f5f3a82942b342ae66fbac493141594055744e01168da49832e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:23:16 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:23:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:23:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3016f09e58e2224328d6b41bb77318fceda5b54269054dde87e90e5c78a5850`  
		Last Modified: Tue, 14 Apr 2026 19:23:32 GMT  
		Size: 6.6 MB (6561426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac87bfa474f24897ae62b339e8d3e99d2477339cb9c7b9c9c27fe53e05575a`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5caa4d61a9b6f6e771c2817dc9c2d7f2b7737c8d5ba3352063ae308e6ba4bb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:1076c83f11053262280ca29e78934d54c350126d3bf945008131c45e30051279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2883b8d290089c7ecab48a7da59f92c662d33b5b0eb9d670e0b0f444447fe585`

```dockerfile
```

-	Layers:
	-	`sha256:56648b6f8b6b7d991ee9afea4af9d02a29fed6e3de695d2669ff6a10e1c66ad2`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:0382580cb171a9ef5220b58d8f8476e825dd541e23ddd9261c83fe81077c687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10593579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbff052312601b8843e5c7f71ffd689bab23a0bbc6c559f906df56d2ab3ad4cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe3d8c0011da8faf0966aa9995120fdc77207edbfce2a78a12b7ffa0e66cdee`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 6.9 MB (6942178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db786c0b404f3ce6941db702d0a29b1f7f7a2da1f5178eb375ae02a6864fb69`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaae1336b66f9d4544d0dada462003e4b60143899cc7d520d196916b4b2a931`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6bfbfebce9888aad4a527e1f5b945818e5241836164846ce875432b1e6bba4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d469341abe6fbb7b778259a810bc75cf066eabd0da34b49bac83dc9b756113`

```dockerfile
```

-	Layers:
	-	`sha256:25df845b450fa255e51db23f7115c4c5986bcc435fb73ff38329d7f8bcebbd2e`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.7-linux`

```console
$ docker pull nats@sha256:d2b16b7517a2dd973e0999b071e016485a9a08c82b5369cc1ce858af54587e93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12.7-linux` - linux; amd64

```console
$ docker pull nats@sha256:ecb873658a349d84b05ab89ccdc9dc3d3153e45b1c32f344c56383cfe78090ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0247f7685ff68b4ae975febd9a287b05bfd142373a9ddeb8c2dac6bfbc859`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040b24667adc09216d21ad3439155962ccadd3d91a63d56b7da7fc06ee4af8d`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-linux` - unknown; unknown

```console
$ docker pull nats@sha256:248f347c9c2745bce92c2706cb33a87211172a8f8e92087fdc501d07f7b8de4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43eac3eec77ccc736e40ad70b7026f77225ac7e5837afeb1a08f32fdd7d0b93`

```dockerfile
```

-	Layers:
	-	`sha256:d702fbcd1bfaedd00e8319117145a6389d6ea5e0c82a9d42f3162b728faeb4e5`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6b0b00a37ddb7979ca235c35428c360669c9da2bcfa9233ae1ac9be85d0d4345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444254e21a5a8780d3528d8d19efbf156e2c5abdbb0cfe9788f1d1eedab18e2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:38 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1a6f37e82fee0dcce9cf7e8571403adb7ce8ca76666035b362c31649f4b2e`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-linux` - unknown; unknown

```console
$ docker pull nats@sha256:550334371afd2696f12dac3fd3739eea092ac27f6b0b773744e87d63aae577e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63dfea61fd8fa9fa90c1a671898c3ff2dc3edfc998eb6478ee5c9b3e5f33d7f`

```dockerfile
```

-	Layers:
	-	`sha256:958b223cfdb0c6fadea45187b0bf34bd7314cdb490d8581c32cd73f85ef90ae5`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:88aeaaa7e2045ccc03915e3f388f392216411e3fa768956ec3b12003643e8697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e37b72ad4a2af972471eebaedf8daa75a569452f35b1ab43ebe86fab23da376`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79c24a16cb2f9ad04dc2e860c74b6a0c8653d0340378eda7c4a9db7fac2f355`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b8ac0ce4a3228e54e91056d63c0aad4573821af86e16530e157710c2c2f48ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e7d98c930153daa0f647ce1a34edcfacc5ba63ac0cdbfab10485093d0fc0fa`

```dockerfile
```

-	Layers:
	-	`sha256:070f2bbece5473f2c0c55e418b792510a0febdefaba18480714cf7dc0da44524`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:00ace04168cdf245f42a3b4e51001be65d57b2688ba37ceb571c858367f82091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942ee14c16718cb6b226080a269139173f826f4c57756120cbabb10a04312a41`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831958881aa7c7363f4962a6a305dd34529b5a3b6f9fe34ea0c550a9a93123a`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-linux` - unknown; unknown

```console
$ docker pull nats@sha256:04f4203ae702f8e1b57048b7f4a4562fadedd65a9a8052c10c5da32881a66567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ade1f2cedf562271f325ad67e73e55747b1a3765d3cfc1376e87cfa671e8d4`

```dockerfile
```

-	Layers:
	-	`sha256:29172cfd963721f0ae26556bb1349dee2b0977a97ef6c34ef44f7ad4eeb9a594`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:fdf8115b60259ac2622bdde6924f704a6275feb0d6cd65e38f4aa7a571791656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd15e3d70e85b851f5786bcc5592cef3d495bd850f8f7cbcdc0ca7c700408b2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47da5cb15f63124b6ff2f092feb178a9029685c93134a876733691494c5cf9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-linux` - unknown; unknown

```console
$ docker pull nats@sha256:c2a87cab23bdc37d169c93959e3ec821a456c1680a6551a7f5cf61acf16280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86a55fa4e6f66b879978374fa109f719ada684dd8a92f7ccda530fcbc8737`

```dockerfile
```

-	Layers:
	-	`sha256:7568c1ce7de6a041e52b780d3fd8b6872d5da377f7ac920fca57449c782c748c`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-linux` - linux; s390x

```console
$ docker pull nats@sha256:7baa159ac707369edf5af5b2c2b7c240c82bd34149b3260dceee7ad5638d53cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d4acd870d3458242a8422ca0164de8903a47ffd0780a6b728485e25dac57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:08 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df52bd1462bfd4be75daf7de0a883ef6e005cb317917ea033fc18ee8368eb7`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-linux` - unknown; unknown

```console
$ docker pull nats@sha256:5ff7a0dfeaa6f2d4722d44dd6c709280ee35981ac7914b9dbfe21f57553e8a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c64e47e3edc168434146e3dec0c50abffdc23b6ec839ab026d2b9f10ce86c8`

```dockerfile
```

-	Layers:
	-	`sha256:8c8467bb933eef06e5af049586ab2e9b851e9f07b23dc34a6533b00f8f1ddeff`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.7-nanoserver`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12.7-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.7-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12.7-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.7-scratch`

```console
$ docker pull nats@sha256:d2b16b7517a2dd973e0999b071e016485a9a08c82b5369cc1ce858af54587e93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.12.7-scratch` - linux; amd64

```console
$ docker pull nats@sha256:ecb873658a349d84b05ab89ccdc9dc3d3153e45b1c32f344c56383cfe78090ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0247f7685ff68b4ae975febd9a287b05bfd142373a9ddeb8c2dac6bfbc859`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040b24667adc09216d21ad3439155962ccadd3d91a63d56b7da7fc06ee4af8d`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:248f347c9c2745bce92c2706cb33a87211172a8f8e92087fdc501d07f7b8de4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43eac3eec77ccc736e40ad70b7026f77225ac7e5837afeb1a08f32fdd7d0b93`

```dockerfile
```

-	Layers:
	-	`sha256:d702fbcd1bfaedd00e8319117145a6389d6ea5e0c82a9d42f3162b728faeb4e5`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:6b0b00a37ddb7979ca235c35428c360669c9da2bcfa9233ae1ac9be85d0d4345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444254e21a5a8780d3528d8d19efbf156e2c5abdbb0cfe9788f1d1eedab18e2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:38 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1a6f37e82fee0dcce9cf7e8571403adb7ce8ca76666035b362c31649f4b2e`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:550334371afd2696f12dac3fd3739eea092ac27f6b0b773744e87d63aae577e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63dfea61fd8fa9fa90c1a671898c3ff2dc3edfc998eb6478ee5c9b3e5f33d7f`

```dockerfile
```

-	Layers:
	-	`sha256:958b223cfdb0c6fadea45187b0bf34bd7314cdb490d8581c32cd73f85ef90ae5`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:88aeaaa7e2045ccc03915e3f388f392216411e3fa768956ec3b12003643e8697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e37b72ad4a2af972471eebaedf8daa75a569452f35b1ab43ebe86fab23da376`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79c24a16cb2f9ad04dc2e860c74b6a0c8653d0340378eda7c4a9db7fac2f355`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b8ac0ce4a3228e54e91056d63c0aad4573821af86e16530e157710c2c2f48ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e7d98c930153daa0f647ce1a34edcfacc5ba63ac0cdbfab10485093d0fc0fa`

```dockerfile
```

-	Layers:
	-	`sha256:070f2bbece5473f2c0c55e418b792510a0febdefaba18480714cf7dc0da44524`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:00ace04168cdf245f42a3b4e51001be65d57b2688ba37ceb571c858367f82091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942ee14c16718cb6b226080a269139173f826f4c57756120cbabb10a04312a41`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831958881aa7c7363f4962a6a305dd34529b5a3b6f9fe34ea0c550a9a93123a`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:04f4203ae702f8e1b57048b7f4a4562fadedd65a9a8052c10c5da32881a66567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ade1f2cedf562271f325ad67e73e55747b1a3765d3cfc1376e87cfa671e8d4`

```dockerfile
```

-	Layers:
	-	`sha256:29172cfd963721f0ae26556bb1349dee2b0977a97ef6c34ef44f7ad4eeb9a594`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:fdf8115b60259ac2622bdde6924f704a6275feb0d6cd65e38f4aa7a571791656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd15e3d70e85b851f5786bcc5592cef3d495bd850f8f7cbcdc0ca7c700408b2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47da5cb15f63124b6ff2f092feb178a9029685c93134a876733691494c5cf9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c2a87cab23bdc37d169c93959e3ec821a456c1680a6551a7f5cf61acf16280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86a55fa4e6f66b879978374fa109f719ada684dd8a92f7ccda530fcbc8737`

```dockerfile
```

-	Layers:
	-	`sha256:7568c1ce7de6a041e52b780d3fd8b6872d5da377f7ac920fca57449c782c748c`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-scratch` - linux; s390x

```console
$ docker pull nats@sha256:7baa159ac707369edf5af5b2c2b7c240c82bd34149b3260dceee7ad5638d53cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d4acd870d3458242a8422ca0164de8903a47ffd0780a6b728485e25dac57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:08 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df52bd1462bfd4be75daf7de0a883ef6e005cb317917ea033fc18ee8368eb7`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5ff7a0dfeaa6f2d4722d44dd6c709280ee35981ac7914b9dbfe21f57553e8a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c64e47e3edc168434146e3dec0c50abffdc23b6ec839ab026d2b9f10ce86c8`

```dockerfile
```

-	Layers:
	-	`sha256:8c8467bb933eef06e5af049586ab2e9b851e9f07b23dc34a6533b00f8f1ddeff`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.7-windowsservercore`

```console
$ docker pull nats@sha256:184cb774079b425716c5507364372954c455f9142c93d1bc466677ac2cc75ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12.7-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:7790fa4d3db94cf7c89a7688f3f84537bb75287e452f1e554c1588a661d15cb1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077873124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a342bd15d69991f8343f2d756a7638e87fdfa2d5562cb647249e12b2bc09ae8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:06:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:06:25 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:06:26 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 21:06:26 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 21:06:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.7/nats-server-v2.12.7-windows-amd64.zip
# Tue, 14 Apr 2026 21:06:29 GMT
ENV NATS_SERVER_SHASUM=4e7880619018ccebe2aa9372a9a8bc362081a7414f93638143ea6d8049892146
# Tue, 14 Apr 2026 21:06:33 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Apr 2026 21:06:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Apr 2026 21:06:49 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:06:50 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:06:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:06:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234f0c5dc55953d98e0d13e9e881a65f871f8e0476a39dc8074be17e88c96ab`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e8f504a62653497a194c864fb383113d6df01412a46e631c3118b188201760`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d82249fabc12bddf45ee14ee15697a564705a6bae958426abd5f4e10bb35ed`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fce0a83450991329209dbbba5426b504eb424ca3c01086d950fe682844645f`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313c950879461faccbfdbe49b49b7ae9078f4f5f4440ac5d858ef0957df5ed6`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae88d9973cc6300fad7210fd6ceec8ad6f50c2a3521ea7a13d0dbd3039da44d6`  
		Last Modified: Tue, 14 Apr 2026 21:06:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5cbd1df81d61159af069584f9c11905a89d3b37b3bf4c04d8824003ec45c0`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 476.1 KB (476100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d18ee910801df31fa7a1ce17acaac50b7ec97bad952d423d008642554a5ebd9`  
		Last Modified: Tue, 14 Apr 2026 21:07:00 GMT  
		Size: 7.2 MB (7172018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd64f7fcdcc6dc03c3975a663297e49a35d229c0406f0ee49d954c76c7becb45`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.9 KB (1896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd424273b8b84b6ff389aa4eef9af352a6544807e63270647cc147eb2965112d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca72c491cc10f7581d8eb027dc3737bd51ab476833369bb5c2e9d80865d9521`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d050d88a8b0417554b75e53d2839e21fe0c82d7e9104c71eeb8648e9600fbe6d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.7-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:184cb774079b425716c5507364372954c455f9142c93d1bc466677ac2cc75ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:2.12.7-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:7790fa4d3db94cf7c89a7688f3f84537bb75287e452f1e554c1588a661d15cb1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077873124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a342bd15d69991f8343f2d756a7638e87fdfa2d5562cb647249e12b2bc09ae8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:06:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:06:25 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:06:26 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 21:06:26 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 21:06:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.7/nats-server-v2.12.7-windows-amd64.zip
# Tue, 14 Apr 2026 21:06:29 GMT
ENV NATS_SERVER_SHASUM=4e7880619018ccebe2aa9372a9a8bc362081a7414f93638143ea6d8049892146
# Tue, 14 Apr 2026 21:06:33 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Apr 2026 21:06:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Apr 2026 21:06:49 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:06:50 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:06:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:06:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234f0c5dc55953d98e0d13e9e881a65f871f8e0476a39dc8074be17e88c96ab`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e8f504a62653497a194c864fb383113d6df01412a46e631c3118b188201760`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d82249fabc12bddf45ee14ee15697a564705a6bae958426abd5f4e10bb35ed`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fce0a83450991329209dbbba5426b504eb424ca3c01086d950fe682844645f`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313c950879461faccbfdbe49b49b7ae9078f4f5f4440ac5d858ef0957df5ed6`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae88d9973cc6300fad7210fd6ceec8ad6f50c2a3521ea7a13d0dbd3039da44d6`  
		Last Modified: Tue, 14 Apr 2026 21:06:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5cbd1df81d61159af069584f9c11905a89d3b37b3bf4c04d8824003ec45c0`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 476.1 KB (476100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d18ee910801df31fa7a1ce17acaac50b7ec97bad952d423d008642554a5ebd9`  
		Last Modified: Tue, 14 Apr 2026 21:07:00 GMT  
		Size: 7.2 MB (7172018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd64f7fcdcc6dc03c3975a663297e49a35d229c0406f0ee49d954c76c7becb45`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.9 KB (1896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd424273b8b84b6ff389aa4eef9af352a6544807e63270647cc147eb2965112d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca72c491cc10f7581d8eb027dc3737bd51ab476833369bb5c2e9d80865d9521`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d050d88a8b0417554b75e53d2839e21fe0c82d7e9104c71eeb8648e9600fbe6d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:eafac85ab07d22f58da852c2be738ffebf9a426771ae0f6bc3d77cc58818f398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:2a575d676756410fc6468bfc0cc88a737ca244f800345756bbfe3f51df7a26f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7a8652ac9a57d88b7b40e3468f37e97a13c6f83fdb55e5b3f4d501ed10cbba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f79ffd9ff103bc84a4800bd77e3a21a2b8aa5283bb96c8971b80bc0f0b1325`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 7.1 MB (7104675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7565af587bddcdc18a03e6d18c244de584dbbee0a1345791c5f92af76834e52f`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fd907441994b474d09f8910bae025fe95188bfac1759e8191422eb0806c011`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d9b67e61825abfcca68a09f5f2217e3f9f0795bcfd5ae6b25f56d4a4d76244de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e9861b72a9f751c02868a963b26d866e3ed901dc51bc7adcf8c2d2988ef18f`

```dockerfile
```

-	Layers:
	-	`sha256:3638b25e681bd6c5f215250ca0fdd8b3af5c729dcecee3cf902cc5377613f375`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1493f7a8377a4c8f6aa2255676a9abf26baa6454afe853563c3226fb29ee24f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f53595b626382736d722114880915656af1c69519b90cb0f988cccbe55e502e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81a6c31c98e9d23f13c3e1f907bead88c63e1da172c607f1cf5e98bf39b2cfb`  
		Last Modified: Tue, 14 Apr 2026 19:18:19 GMT  
		Size: 6.8 MB (6824527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e93485e87180b419b674b3eaaefe0fb6cb8149f771a85b32884d318565c5b0d`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab1cdedb45964719fb488c1020b53f079ddd692ec19aa9224bcd4185b2f44cf`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a55de7e7cbe420676cde9540a343d1477bea77e79079b607e4ed24f48a7f3ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3362d5291b6a280bab2b1508a6cd3d6d0f5dc5beafa83a4cd908c971e0c2dbc9`

```dockerfile
```

-	Layers:
	-	`sha256:b608191e207ea42ead772d1c93799d794f7bcaf6248843f91721426b28e54576`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:43d26a2a5012f9e5cbb5f3a569bec60a0f31caff9241f2bea12c55576b20b43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b907f2c013544f942a4b8eb34f5dd75ec12f99e82cd0354ff8076468f5bd4a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a506cbdb04d5f850a7e6d7efad2de37c9281f87153355ae9f158463b8863c16`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 6.8 MB (6813977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f012309da8651a720251bebe8d821117e4af8a880054b044d6f9b77cb9bbd`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30097ae043c1bed74c22084b0906018b9e291c295790a03eb6e3c9be52d0585d`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b21ee8f249ab3c650417c4b20f0a8f05ef07196d420c9f2c03ff12d4f870dc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b6611241f2f57bb7846e1cc9646e70116cfb3b87ea4b5edffbaf1fcefe58a`

```dockerfile
```

-	Layers:
	-	`sha256:dd1462a37a47fe62aa5690e6fd6caccf9edd80f3b23d4f1537ff421f2c1db1b2`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ddfc383507987a61ec6ad0842ce9bedfa1c0dc8b0b61e20bf66f4ea1891c963f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10651943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e62a2c6d295007873d27b02e9bfb4b0d35219b9d38537a45aafe2a781a7ef8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75374d2efd25789f733679c46deb8015d53a34ffc525b1a5be14458cfaa7c572`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 6.5 MB (6511455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0469dd7527f8e826ccbde70f8429eb6445d7f986f67412ce5e6fe4f5efe762a`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fd106169b64170292228a08cc598dd7086fd77cb227d8b493a9442da8f2f03`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:c7745ae505e872b9e322bfc8b2f28d8d6f912d9cb77ef8fa4800676ff12f3e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040e174862b564526a86b8abfa14447199c7b3218c59218d695b784bff14213c`

```dockerfile
```

-	Layers:
	-	`sha256:c6ee43bf4bf2b5f9d032ec8ac9655bf3944c1926ec48a04662fddfe77bbba8d5`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:8177663ab814155404ddd225210e864a8db5f5bab6524fcd538e1c50e95b5ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c112147b37f5f3a82942b342ae66fbac493141594055744e01168da49832e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:23:16 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:23:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:23:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3016f09e58e2224328d6b41bb77318fceda5b54269054dde87e90e5c78a5850`  
		Last Modified: Tue, 14 Apr 2026 19:23:32 GMT  
		Size: 6.6 MB (6561426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac87bfa474f24897ae62b339e8d3e99d2477339cb9c7b9c9c27fe53e05575a`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5caa4d61a9b6f6e771c2817dc9c2d7f2b7737c8d5ba3352063ae308e6ba4bb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:1076c83f11053262280ca29e78934d54c350126d3bf945008131c45e30051279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2883b8d290089c7ecab48a7da59f92c662d33b5b0eb9d670e0b0f444447fe585`

```dockerfile
```

-	Layers:
	-	`sha256:56648b6f8b6b7d991ee9afea4af9d02a29fed6e3de695d2669ff6a10e1c66ad2`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:0382580cb171a9ef5220b58d8f8476e825dd541e23ddd9261c83fe81077c687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10593579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbff052312601b8843e5c7f71ffd689bab23a0bbc6c559f906df56d2ab3ad4cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe3d8c0011da8faf0966aa9995120fdc77207edbfce2a78a12b7ffa0e66cdee`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 6.9 MB (6942178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db786c0b404f3ce6941db702d0a29b1f7f7a2da1f5178eb375ae02a6864fb69`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaae1336b66f9d4544d0dada462003e4b60143899cc7d520d196916b4b2a931`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6bfbfebce9888aad4a527e1f5b945818e5241836164846ce875432b1e6bba4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d469341abe6fbb7b778259a810bc75cf066eabd0da34b49bac83dc9b756113`

```dockerfile
```

-	Layers:
	-	`sha256:25df845b450fa255e51db23f7115c4c5986bcc435fb73ff38329d7f8bcebbd2e`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:eafac85ab07d22f58da852c2be738ffebf9a426771ae0f6bc3d77cc58818f398
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:2a575d676756410fc6468bfc0cc88a737ca244f800345756bbfe3f51df7a26f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10910518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7a8652ac9a57d88b7b40e3468f37e97a13c6f83fdb55e5b3f4d501ed10cbba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:51 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:51 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f79ffd9ff103bc84a4800bd77e3a21a2b8aa5283bb96c8971b80bc0f0b1325`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 7.1 MB (7104675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7565af587bddcdc18a03e6d18c244de584dbbee0a1345791c5f92af76834e52f`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fd907441994b474d09f8910bae025fe95188bfac1759e8191422eb0806c011`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d9b67e61825abfcca68a09f5f2217e3f9f0795bcfd5ae6b25f56d4a4d76244de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e9861b72a9f751c02868a963b26d866e3ed901dc51bc7adcf8c2d2988ef18f`

```dockerfile
```

-	Layers:
	-	`sha256:3638b25e681bd6c5f215250ca0fdd8b3af5c729dcecee3cf902cc5377613f375`  
		Last Modified: Tue, 14 Apr 2026 19:17:56 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:1493f7a8377a4c8f6aa2255676a9abf26baa6454afe853563c3226fb29ee24f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f53595b626382736d722114880915656af1c69519b90cb0f988cccbe55e502e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81a6c31c98e9d23f13c3e1f907bead88c63e1da172c607f1cf5e98bf39b2cfb`  
		Last Modified: Tue, 14 Apr 2026 19:18:19 GMT  
		Size: 6.8 MB (6824527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e93485e87180b419b674b3eaaefe0fb6cb8149f771a85b32884d318565c5b0d`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab1cdedb45964719fb488c1020b53f079ddd692ec19aa9224bcd4185b2f44cf`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a55de7e7cbe420676cde9540a343d1477bea77e79079b607e4ed24f48a7f3ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3362d5291b6a280bab2b1508a6cd3d6d0f5dc5beafa83a4cd908c971e0c2dbc9`

```dockerfile
```

-	Layers:
	-	`sha256:b608191e207ea42ead772d1c93799d794f7bcaf6248843f91721426b28e54576`  
		Last Modified: Tue, 14 Apr 2026 19:18:18 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:43d26a2a5012f9e5cbb5f3a569bec60a0f31caff9241f2bea12c55576b20b43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b907f2c013544f942a4b8eb34f5dd75ec12f99e82cd0354ff8076468f5bd4a5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:12 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:12 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a506cbdb04d5f850a7e6d7efad2de37c9281f87153355ae9f158463b8863c16`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 6.8 MB (6813977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55f012309da8651a720251bebe8d821117e4af8a880054b044d6f9b77cb9bbd`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30097ae043c1bed74c22084b0906018b9e291c295790a03eb6e3c9be52d0585d`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:b21ee8f249ab3c650417c4b20f0a8f05ef07196d420c9f2c03ff12d4f870dc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62b6611241f2f57bb7846e1cc9646e70116cfb3b87ea4b5edffbaf1fcefe58a`

```dockerfile
```

-	Layers:
	-	`sha256:dd1462a37a47fe62aa5690e6fd6caccf9edd80f3b23d4f1537ff421f2c1db1b2`  
		Last Modified: Tue, 14 Apr 2026 19:18:17 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ddfc383507987a61ec6ad0842ce9bedfa1c0dc8b0b61e20bf66f4ea1891c963f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10651943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e62a2c6d295007873d27b02e9bfb4b0d35219b9d38537a45aafe2a781a7ef8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:18:31 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:18:31 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:18:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:18:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75374d2efd25789f733679c46deb8015d53a34ffc525b1a5be14458cfaa7c572`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 6.5 MB (6511455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0469dd7527f8e826ccbde70f8429eb6445d7f986f67412ce5e6fe4f5efe762a`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fd106169b64170292228a08cc598dd7086fd77cb227d8b493a9442da8f2f03`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:c7745ae505e872b9e322bfc8b2f28d8d6f912d9cb77ef8fa4800676ff12f3e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040e174862b564526a86b8abfa14447199c7b3218c59218d695b784bff14213c`

```dockerfile
```

-	Layers:
	-	`sha256:c6ee43bf4bf2b5f9d032ec8ac9655bf3944c1926ec48a04662fddfe77bbba8d5`  
		Last Modified: Tue, 14 Apr 2026 19:18:35 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:8177663ab814155404ddd225210e864a8db5f5bab6524fcd538e1c50e95b5ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10296695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c112147b37f5f3a82942b342ae66fbac493141594055744e01168da49832e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:23:16 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:23:16 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:23:17 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:23:18 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:23:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:23:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3016f09e58e2224328d6b41bb77318fceda5b54269054dde87e90e5c78a5850`  
		Last Modified: Tue, 14 Apr 2026 19:23:32 GMT  
		Size: 6.6 MB (6561426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ac87bfa474f24897ae62b339e8d3e99d2477339cb9c7b9c9c27fe53e05575a`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5caa4d61a9b6f6e771c2817dc9c2d7f2b7737c8d5ba3352063ae308e6ba4bb`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:1076c83f11053262280ca29e78934d54c350126d3bf945008131c45e30051279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2883b8d290089c7ecab48a7da59f92c662d33b5b0eb9d670e0b0f444447fe585`

```dockerfile
```

-	Layers:
	-	`sha256:56648b6f8b6b7d991ee9afea4af9d02a29fed6e3de695d2669ff6a10e1c66ad2`  
		Last Modified: Tue, 14 Apr 2026 19:23:31 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:0382580cb171a9ef5220b58d8f8476e825dd541e23ddd9261c83fe81077c687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10593579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbff052312601b8843e5c7f71ffd689bab23a0bbc6c559f906df56d2ab3ad4cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 19:17:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 14 Apr 2026 19:17:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 19:17:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Apr 2026 19:17:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe3d8c0011da8faf0966aa9995120fdc77207edbfce2a78a12b7ffa0e66cdee`  
		Last Modified: Tue, 14 Apr 2026 19:17:49 GMT  
		Size: 6.9 MB (6942178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db786c0b404f3ce6941db702d0a29b1f7f7a2da1f5178eb375ae02a6864fb69`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaae1336b66f9d4544d0dada462003e4b60143899cc7d520d196916b4b2a931`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6bfbfebce9888aad4a527e1f5b945818e5241836164846ce875432b1e6bba4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d469341abe6fbb7b778259a810bc75cf066eabd0da34b49bac83dc9b756113`

```dockerfile
```

-	Layers:
	-	`sha256:25df845b450fa255e51db23f7115c4c5986bcc435fb73ff38329d7f8bcebbd2e`  
		Last Modified: Tue, 14 Apr 2026 19:17:48 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:fd76fc5a1fd3e8e1b8c14ef1ddd04f9b379df11bb73e48ff417eb12b07e4c387
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.5020; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:ecb873658a349d84b05ab89ccdc9dc3d3153e45b1c32f344c56383cfe78090ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0247f7685ff68b4ae975febd9a287b05bfd142373a9ddeb8c2dac6bfbc859`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040b24667adc09216d21ad3439155962ccadd3d91a63d56b7da7fc06ee4af8d`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:248f347c9c2745bce92c2706cb33a87211172a8f8e92087fdc501d07f7b8de4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43eac3eec77ccc736e40ad70b7026f77225ac7e5837afeb1a08f32fdd7d0b93`

```dockerfile
```

-	Layers:
	-	`sha256:d702fbcd1bfaedd00e8319117145a6389d6ea5e0c82a9d42f3162b728faeb4e5`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:6b0b00a37ddb7979ca235c35428c360669c9da2bcfa9233ae1ac9be85d0d4345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444254e21a5a8780d3528d8d19efbf156e2c5abdbb0cfe9788f1d1eedab18e2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:38 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1a6f37e82fee0dcce9cf7e8571403adb7ce8ca76666035b362c31649f4b2e`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:550334371afd2696f12dac3fd3739eea092ac27f6b0b773744e87d63aae577e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63dfea61fd8fa9fa90c1a671898c3ff2dc3edfc998eb6478ee5c9b3e5f33d7f`

```dockerfile
```

-	Layers:
	-	`sha256:958b223cfdb0c6fadea45187b0bf34bd7314cdb490d8581c32cd73f85ef90ae5`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:88aeaaa7e2045ccc03915e3f388f392216411e3fa768956ec3b12003643e8697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e37b72ad4a2af972471eebaedf8daa75a569452f35b1ab43ebe86fab23da376`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79c24a16cb2f9ad04dc2e860c74b6a0c8653d0340378eda7c4a9db7fac2f355`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:b8ac0ce4a3228e54e91056d63c0aad4573821af86e16530e157710c2c2f48ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e7d98c930153daa0f647ce1a34edcfacc5ba63ac0cdbfab10485093d0fc0fa`

```dockerfile
```

-	Layers:
	-	`sha256:070f2bbece5473f2c0c55e418b792510a0febdefaba18480714cf7dc0da44524`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:00ace04168cdf245f42a3b4e51001be65d57b2688ba37ceb571c858367f82091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942ee14c16718cb6b226080a269139173f826f4c57756120cbabb10a04312a41`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831958881aa7c7363f4962a6a305dd34529b5a3b6f9fe34ea0c550a9a93123a`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:04f4203ae702f8e1b57048b7f4a4562fadedd65a9a8052c10c5da32881a66567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ade1f2cedf562271f325ad67e73e55747b1a3765d3cfc1376e87cfa671e8d4`

```dockerfile
```

-	Layers:
	-	`sha256:29172cfd963721f0ae26556bb1349dee2b0977a97ef6c34ef44f7ad4eeb9a594`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:fdf8115b60259ac2622bdde6924f704a6275feb0d6cd65e38f4aa7a571791656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd15e3d70e85b851f5786bcc5592cef3d495bd850f8f7cbcdc0ca7c700408b2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47da5cb15f63124b6ff2f092feb178a9029685c93134a876733691494c5cf9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:c2a87cab23bdc37d169c93959e3ec821a456c1680a6551a7f5cf61acf16280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86a55fa4e6f66b879978374fa109f719ada684dd8a92f7ccda530fcbc8737`

```dockerfile
```

-	Layers:
	-	`sha256:7568c1ce7de6a041e52b780d3fd8b6872d5da377f7ac920fca57449c782c748c`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:7baa159ac707369edf5af5b2c2b7c240c82bd34149b3260dceee7ad5638d53cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d4acd870d3458242a8422ca0164de8903a47ffd0780a6b728485e25dac57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:08 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df52bd1462bfd4be75daf7de0a883ef6e005cb317917ea033fc18ee8368eb7`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:5ff7a0dfeaa6f2d4722d44dd6c709280ee35981ac7914b9dbfe21f57553e8a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c64e47e3edc168434146e3dec0c50abffdc23b6ec839ab026d2b9f10ce86c8`

```dockerfile
```

-	Layers:
	-	`sha256:8c8467bb933eef06e5af049586ab2e9b851e9f07b23dc34a6533b00f8f1ddeff`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:d2b16b7517a2dd973e0999b071e016485a9a08c82b5369cc1ce858af54587e93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:ecb873658a349d84b05ab89ccdc9dc3d3153e45b1c32f344c56383cfe78090ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0247f7685ff68b4ae975febd9a287b05bfd142373a9ddeb8c2dac6bfbc859`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040b24667adc09216d21ad3439155962ccadd3d91a63d56b7da7fc06ee4af8d`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:248f347c9c2745bce92c2706cb33a87211172a8f8e92087fdc501d07f7b8de4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43eac3eec77ccc736e40ad70b7026f77225ac7e5837afeb1a08f32fdd7d0b93`

```dockerfile
```

-	Layers:
	-	`sha256:d702fbcd1bfaedd00e8319117145a6389d6ea5e0c82a9d42f3162b728faeb4e5`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6b0b00a37ddb7979ca235c35428c360669c9da2bcfa9233ae1ac9be85d0d4345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444254e21a5a8780d3528d8d19efbf156e2c5abdbb0cfe9788f1d1eedab18e2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:38 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1a6f37e82fee0dcce9cf7e8571403adb7ce8ca76666035b362c31649f4b2e`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:550334371afd2696f12dac3fd3739eea092ac27f6b0b773744e87d63aae577e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63dfea61fd8fa9fa90c1a671898c3ff2dc3edfc998eb6478ee5c9b3e5f33d7f`

```dockerfile
```

-	Layers:
	-	`sha256:958b223cfdb0c6fadea45187b0bf34bd7314cdb490d8581c32cd73f85ef90ae5`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:88aeaaa7e2045ccc03915e3f388f392216411e3fa768956ec3b12003643e8697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e37b72ad4a2af972471eebaedf8daa75a569452f35b1ab43ebe86fab23da376`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79c24a16cb2f9ad04dc2e860c74b6a0c8653d0340378eda7c4a9db7fac2f355`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:b8ac0ce4a3228e54e91056d63c0aad4573821af86e16530e157710c2c2f48ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e7d98c930153daa0f647ce1a34edcfacc5ba63ac0cdbfab10485093d0fc0fa`

```dockerfile
```

-	Layers:
	-	`sha256:070f2bbece5473f2c0c55e418b792510a0febdefaba18480714cf7dc0da44524`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:00ace04168cdf245f42a3b4e51001be65d57b2688ba37ceb571c858367f82091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942ee14c16718cb6b226080a269139173f826f4c57756120cbabb10a04312a41`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831958881aa7c7363f4962a6a305dd34529b5a3b6f9fe34ea0c550a9a93123a`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:04f4203ae702f8e1b57048b7f4a4562fadedd65a9a8052c10c5da32881a66567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ade1f2cedf562271f325ad67e73e55747b1a3765d3cfc1376e87cfa671e8d4`

```dockerfile
```

-	Layers:
	-	`sha256:29172cfd963721f0ae26556bb1349dee2b0977a97ef6c34ef44f7ad4eeb9a594`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:fdf8115b60259ac2622bdde6924f704a6275feb0d6cd65e38f4aa7a571791656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd15e3d70e85b851f5786bcc5592cef3d495bd850f8f7cbcdc0ca7c700408b2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47da5cb15f63124b6ff2f092feb178a9029685c93134a876733691494c5cf9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:c2a87cab23bdc37d169c93959e3ec821a456c1680a6551a7f5cf61acf16280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86a55fa4e6f66b879978374fa109f719ada684dd8a92f7ccda530fcbc8737`

```dockerfile
```

-	Layers:
	-	`sha256:7568c1ce7de6a041e52b780d3fd8b6872d5da377f7ac920fca57449c782c748c`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:7baa159ac707369edf5af5b2c2b7c240c82bd34149b3260dceee7ad5638d53cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d4acd870d3458242a8422ca0164de8903a47ffd0780a6b728485e25dac57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:08 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df52bd1462bfd4be75daf7de0a883ef6e005cb317917ea033fc18ee8368eb7`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:5ff7a0dfeaa6f2d4722d44dd6c709280ee35981ac7914b9dbfe21f57553e8a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c64e47e3edc168434146e3dec0c50abffdc23b6ec839ab026d2b9f10ce86c8`

```dockerfile
```

-	Layers:
	-	`sha256:8c8467bb933eef06e5af049586ab2e9b851e9f07b23dc34a6533b00f8f1ddeff`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:67c59681dcbe87f3ec27cdadc3ddaa6ffc47d3adae4c474940844954900fcd5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:19ea12d756b6d8a09df85dc48d18b0cef5746fdd6d364e43fd5f3592f9bcc755
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133802260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9fe3608c4de558af637aa1eee9f48aa553bd1f3611c754b570dec79662727`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 21:47:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:caa15c276184b91f93e79310fca4ace491bb7d9f588032444a45f465bf58c440 in C:\nats-server.exe 
# Tue, 14 Apr 2026 21:47:39 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:47:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:47:41 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc97fcff4179b8882e8966e9dac3b2d58ea75bd47d600dbf06efe952aef4845a`  
		Last Modified: Tue, 14 Apr 2026 21:47:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992360b9296c1212953b99ff677a5e5b6687dbfe47ddee18056f5cb51d61595a`  
		Last Modified: Tue, 14 Apr 2026 21:47:47 GMT  
		Size: 6.8 MB (6840331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63a8280b1f3dd4579789c18d28dbbffe6255a7a91589d382104f7f28833902`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86318ad18febea26a40c20342b3c6ddd103f919c5b15f90868ce0ffbaae5c2ec`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1edc8498e6dc5d0007293630c0ef9abebf3a9d2ba8f3c8ff2be0f57fff0d3b`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203fd402bc0d511f3ac3dc580a5edcd66f9efc301fc2561cef1a7c0833be018`  
		Last Modified: Tue, 14 Apr 2026 21:47:45 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:d2b16b7517a2dd973e0999b071e016485a9a08c82b5369cc1ce858af54587e93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:ecb873658a349d84b05ab89ccdc9dc3d3153e45b1c32f344c56383cfe78090ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0247f7685ff68b4ae975febd9a287b05bfd142373a9ddeb8c2dac6bfbc859`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040b24667adc09216d21ad3439155962ccadd3d91a63d56b7da7fc06ee4af8d`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:248f347c9c2745bce92c2706cb33a87211172a8f8e92087fdc501d07f7b8de4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43eac3eec77ccc736e40ad70b7026f77225ac7e5837afeb1a08f32fdd7d0b93`

```dockerfile
```

-	Layers:
	-	`sha256:d702fbcd1bfaedd00e8319117145a6389d6ea5e0c82a9d42f3162b728faeb4e5`  
		Last Modified: Tue, 14 Apr 2026 20:10:05 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:6b0b00a37ddb7979ca235c35428c360669c9da2bcfa9233ae1ac9be85d0d4345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444254e21a5a8780d3528d8d19efbf156e2c5abdbb0cfe9788f1d1eedab18e2e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:38 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:08:38 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:08:38 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:08:38 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd1a6f37e82fee0dcce9cf7e8571403adb7ce8ca76666035b362c31649f4b2e`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:550334371afd2696f12dac3fd3739eea092ac27f6b0b773744e87d63aae577e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63dfea61fd8fa9fa90c1a671898c3ff2dc3edfc998eb6478ee5c9b3e5f33d7f`

```dockerfile
```

-	Layers:
	-	`sha256:958b223cfdb0c6fadea45187b0bf34bd7314cdb490d8581c32cd73f85ef90ae5`  
		Last Modified: Tue, 14 Apr 2026 20:08:42 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:88aeaaa7e2045ccc03915e3f388f392216411e3fa768956ec3b12003643e8697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e37b72ad4a2af972471eebaedf8daa75a569452f35b1ab43ebe86fab23da376`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:14 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79c24a16cb2f9ad04dc2e860c74b6a0c8653d0340378eda7c4a9db7fac2f355`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b8ac0ce4a3228e54e91056d63c0aad4573821af86e16530e157710c2c2f48ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e7d98c930153daa0f647ce1a34edcfacc5ba63ac0cdbfab10485093d0fc0fa`

```dockerfile
```

-	Layers:
	-	`sha256:070f2bbece5473f2c0c55e418b792510a0febdefaba18480714cf7dc0da44524`  
		Last Modified: Tue, 14 Apr 2026 20:09:18 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:00ace04168cdf245f42a3b4e51001be65d57b2688ba37ceb571c858367f82091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942ee14c16718cb6b226080a269139173f826f4c57756120cbabb10a04312a41`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:10:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:10:03 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:10:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:10:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:10:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831958881aa7c7363f4962a6a305dd34529b5a3b6f9fe34ea0c550a9a93123a`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 511.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:04f4203ae702f8e1b57048b7f4a4562fadedd65a9a8052c10c5da32881a66567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ade1f2cedf562271f325ad67e73e55747b1a3765d3cfc1376e87cfa671e8d4`

```dockerfile
```

-	Layers:
	-	`sha256:29172cfd963721f0ae26556bb1349dee2b0977a97ef6c34ef44f7ad4eeb9a594`  
		Last Modified: Tue, 14 Apr 2026 20:10:08 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:fdf8115b60259ac2622bdde6924f704a6275feb0d6cd65e38f4aa7a571791656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd15e3d70e85b851f5786bcc5592cef3d495bd850f8f7cbcdc0ca7c700408b2f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:08:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:08:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:01 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47da5cb15f63124b6ff2f092feb178a9029685c93134a876733691494c5cf9b`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c2a87cab23bdc37d169c93959e3ec821a456c1680a6551a7f5cf61acf16280cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a86a55fa4e6f66b879978374fa109f719ada684dd8a92f7ccda530fcbc8737`

```dockerfile
```

-	Layers:
	-	`sha256:7568c1ce7de6a041e52b780d3fd8b6872d5da377f7ac920fca57449c782c748c`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:7baa159ac707369edf5af5b2c2b7c240c82bd34149b3260dceee7ad5638d53cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f164d4acd870d3458242a8422ca0164de8903a47ffd0780a6b728485e25dac57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 14 Apr 2026 20:09:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 14 Apr 2026 20:09:08 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 14 Apr 2026 20:09:08 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 14 Apr 2026 20:09:08 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 14 Apr 2026 20:09:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17df52bd1462bfd4be75daf7de0a883ef6e005cb317917ea033fc18ee8368eb7`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:5ff7a0dfeaa6f2d4722d44dd6c709280ee35981ac7914b9dbfe21f57553e8a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c64e47e3edc168434146e3dec0c50abffdc23b6ec839ab026d2b9f10ce86c8`

```dockerfile
```

-	Layers:
	-	`sha256:8c8467bb933eef06e5af049586ab2e9b851e9f07b23dc34a6533b00f8f1ddeff`  
		Last Modified: Tue, 14 Apr 2026 20:09:15 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:184cb774079b425716c5507364372954c455f9142c93d1bc466677ac2cc75ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:7790fa4d3db94cf7c89a7688f3f84537bb75287e452f1e554c1588a661d15cb1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077873124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a342bd15d69991f8343f2d756a7638e87fdfa2d5562cb647249e12b2bc09ae8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:06:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:06:25 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:06:26 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 21:06:26 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 21:06:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.7/nats-server-v2.12.7-windows-amd64.zip
# Tue, 14 Apr 2026 21:06:29 GMT
ENV NATS_SERVER_SHASUM=4e7880619018ccebe2aa9372a9a8bc362081a7414f93638143ea6d8049892146
# Tue, 14 Apr 2026 21:06:33 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Apr 2026 21:06:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Apr 2026 21:06:49 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:06:50 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:06:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:06:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234f0c5dc55953d98e0d13e9e881a65f871f8e0476a39dc8074be17e88c96ab`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e8f504a62653497a194c864fb383113d6df01412a46e631c3118b188201760`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d82249fabc12bddf45ee14ee15697a564705a6bae958426abd5f4e10bb35ed`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fce0a83450991329209dbbba5426b504eb424ca3c01086d950fe682844645f`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313c950879461faccbfdbe49b49b7ae9078f4f5f4440ac5d858ef0957df5ed6`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae88d9973cc6300fad7210fd6ceec8ad6f50c2a3521ea7a13d0dbd3039da44d6`  
		Last Modified: Tue, 14 Apr 2026 21:06:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5cbd1df81d61159af069584f9c11905a89d3b37b3bf4c04d8824003ec45c0`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 476.1 KB (476100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d18ee910801df31fa7a1ce17acaac50b7ec97bad952d423d008642554a5ebd9`  
		Last Modified: Tue, 14 Apr 2026 21:07:00 GMT  
		Size: 7.2 MB (7172018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd64f7fcdcc6dc03c3975a663297e49a35d229c0406f0ee49d954c76c7becb45`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.9 KB (1896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd424273b8b84b6ff389aa4eef9af352a6544807e63270647cc147eb2965112d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca72c491cc10f7581d8eb027dc3737bd51ab476833369bb5c2e9d80865d9521`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d050d88a8b0417554b75e53d2839e21fe0c82d7e9104c71eeb8648e9600fbe6d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:184cb774079b425716c5507364372954c455f9142c93d1bc466677ac2cc75ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull nats@sha256:7790fa4d3db94cf7c89a7688f3f84537bb75287e452f1e554c1588a661d15cb1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077873124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a342bd15d69991f8343f2d756a7638e87fdfa2d5562cb647249e12b2bc09ae8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:06:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:06:25 GMT
ENV NATS_DOCKERIZED=1
# Tue, 14 Apr 2026 21:06:26 GMT
ENV NATS_SERVER=2.12.7
# Tue, 14 Apr 2026 21:06:26 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Tue, 14 Apr 2026 21:06:28 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.7/nats-server-v2.12.7-windows-amd64.zip
# Tue, 14 Apr 2026 21:06:29 GMT
ENV NATS_SERVER_SHASUM=4e7880619018ccebe2aa9372a9a8bc362081a7414f93638143ea6d8049892146
# Tue, 14 Apr 2026 21:06:33 GMT
RUN Set-PSDebug -Trace 2
# Tue, 14 Apr 2026 21:06:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 14 Apr 2026 21:06:49 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Tue, 14 Apr 2026 21:06:50 GMT
EXPOSE 4222 6222 8222
# Tue, 14 Apr 2026 21:06:50 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 14 Apr 2026 21:06:51 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234f0c5dc55953d98e0d13e9e881a65f871f8e0476a39dc8074be17e88c96ab`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e8f504a62653497a194c864fb383113d6df01412a46e631c3118b188201760`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d82249fabc12bddf45ee14ee15697a564705a6bae958426abd5f4e10bb35ed`  
		Last Modified: Tue, 14 Apr 2026 21:06:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fce0a83450991329209dbbba5426b504eb424ca3c01086d950fe682844645f`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313c950879461faccbfdbe49b49b7ae9078f4f5f4440ac5d858ef0957df5ed6`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae88d9973cc6300fad7210fd6ceec8ad6f50c2a3521ea7a13d0dbd3039da44d6`  
		Last Modified: Tue, 14 Apr 2026 21:06:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5cbd1df81d61159af069584f9c11905a89d3b37b3bf4c04d8824003ec45c0`  
		Last Modified: Tue, 14 Apr 2026 21:06:57 GMT  
		Size: 476.1 KB (476100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d18ee910801df31fa7a1ce17acaac50b7ec97bad952d423d008642554a5ebd9`  
		Last Modified: Tue, 14 Apr 2026 21:07:00 GMT  
		Size: 7.2 MB (7172018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd64f7fcdcc6dc03c3975a663297e49a35d229c0406f0ee49d954c76c7becb45`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.9 KB (1896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd424273b8b84b6ff389aa4eef9af352a6544807e63270647cc147eb2965112d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dca72c491cc10f7581d8eb027dc3737bd51ab476833369bb5c2e9d80865d9521`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d050d88a8b0417554b75e53d2839e21fe0c82d7e9104c71eeb8648e9600fbe6d`  
		Last Modified: Tue, 14 Apr 2026 21:06:55 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
