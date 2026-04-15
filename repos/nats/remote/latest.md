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
