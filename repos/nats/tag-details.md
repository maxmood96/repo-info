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
-	[`nats:2.12`](#nats212)
-	[`nats:2.12-alpine`](#nats212-alpine)
-	[`nats:2.12-alpine3.22`](#nats212-alpine322)
-	[`nats:2.12-linux`](#nats212-linux)
-	[`nats:2.12-nanoserver`](#nats212-nanoserver)
-	[`nats:2.12-nanoserver-ltsc2022`](#nats212-nanoserver-ltsc2022)
-	[`nats:2.12-scratch`](#nats212-scratch)
-	[`nats:2.12-windowsservercore`](#nats212-windowsservercore)
-	[`nats:2.12-windowsservercore-ltsc2022`](#nats212-windowsservercore-ltsc2022)
-	[`nats:2.12.12`](#nats21212)
-	[`nats:2.12.12-alpine`](#nats21212-alpine)
-	[`nats:2.12.12-alpine3.22`](#nats21212-alpine322)
-	[`nats:2.12.12-linux`](#nats21212-linux)
-	[`nats:2.12.12-nanoserver`](#nats21212-nanoserver)
-	[`nats:2.12.12-nanoserver-ltsc2022`](#nats21212-nanoserver-ltsc2022)
-	[`nats:2.12.12-scratch`](#nats21212-scratch)
-	[`nats:2.12.12-windowsservercore`](#nats21212-windowsservercore)
-	[`nats:2.12.12-windowsservercore-ltsc2022`](#nats21212-windowsservercore-ltsc2022)
-	[`nats:2.14`](#nats214)
-	[`nats:2.14-alpine`](#nats214-alpine)
-	[`nats:2.14-alpine3.22`](#nats214-alpine322)
-	[`nats:2.14-linux`](#nats214-linux)
-	[`nats:2.14-nanoserver`](#nats214-nanoserver)
-	[`nats:2.14-nanoserver-ltsc2022`](#nats214-nanoserver-ltsc2022)
-	[`nats:2.14-scratch`](#nats214-scratch)
-	[`nats:2.14-windowsservercore`](#nats214-windowsservercore)
-	[`nats:2.14-windowsservercore-ltsc2022`](#nats214-windowsservercore-ltsc2022)
-	[`nats:2.14.3`](#nats2143)
-	[`nats:2.14.3-alpine`](#nats2143-alpine)
-	[`nats:2.14.3-alpine3.22`](#nats2143-alpine322)
-	[`nats:2.14.3-linux`](#nats2143-linux)
-	[`nats:2.14.3-nanoserver`](#nats2143-nanoserver)
-	[`nats:2.14.3-nanoserver-ltsc2022`](#nats2143-nanoserver-ltsc2022)
-	[`nats:2.14.3-scratch`](#nats2143-scratch)
-	[`nats:2.14.3-windowsservercore`](#nats2143-windowsservercore)
-	[`nats:2.14.3-windowsservercore-ltsc2022`](#nats2143-windowsservercore-ltsc2022)
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
$ docker pull nats@sha256:7ff2e641c33dbdb0dd13a943ba0b70d841b71275c607baa53ef9b8661f0b2d8c
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
	-	windows version 10.0.20348.5256; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:da52c7cd2dd8cfbfd7d2dfb251b761e42dbfd6fe0acb09fd26cbb42bdddb2866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6857592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ccfa5190b3b463a3fcf96e85c57584707cb0e37e977effc0b13df38ad27da`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:13:56 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:56 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:13:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:001b0b866410b42b38bcb2e428951af42433891ff425dfcce0b3a53cf93d9cf5`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.9 MB (6857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301e2bd5843dce0ae9f53e3b56e505349c98b58f06c463430d25b5c5ff3d2ac`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:4e6b9bd23e99f1e6893cbc2298ff6542ff362ac45479424f0cbbaa44e0bd7932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b91a2a2149df4bdf026d1ba840708ff2f744d4552979b6f5238e32d4b9fadd`

```dockerfile
```

-	Layers:
	-	`sha256:f2654502a1c07929b5dba813de85a6fecf099bd5b4e5dc0304f5bffb9a55374a`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:f954b0114100cc6b04d48371743c840445bbd9d9cd58fd347d548df20fb81377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc68893e7b073ba43eb1643ffef18c78a2bcde561b9df87690e4c25b31729d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:087a70319659349faa0bc66d2f258c634f201af06cf4cd72fd052fe0f1741923`  
		Last Modified: Mon, 29 Jun 2026 15:45:00 GMT  
		Size: 6.6 MB (6591390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48bfacc9913ae01cc25da4a4e0b5b45dd8572ebef94eb75ee659e643ca668f`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:2ddfb53928614b91b72d029bf8c1fe2c18c9323525cddd2435738502af8f535f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c648adf5a8076bdff845afbe972feb29cbce83a045fc1fa7a6407350edd450`

```dockerfile
```

-	Layers:
	-	`sha256:f18d91a70c6190eda91e68db672ccbc0be90eca9e3a3cbca1053dac4180c85bb`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:5acf1bcd52c9815e894b475e74896d5c20d20f75dc1d0a4609284c356a23e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eaac6cac973cc88e6d44cfa8e4fa97db877aa382eca9ca11a3aabdc71efaa4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95cb78be6f3eb15e97acc3a341503927e5ccafbd12a09b4a1b82fbb89f4787b5`  
		Last Modified: Mon, 29 Jun 2026 15:45:01 GMT  
		Size: 6.6 MB (6580972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce96a7f9a07f1a57504be91420ffc8fe2f13ee198161d2b34cfa5461201d23c9`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:7350f027d99946847895026cb1af3842bdad2563af2c7a4902c947e3e5859335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365d446dc11c95971d0b41e292ef423e0863365d7c070019c54d2c193b476ff`

```dockerfile
```

-	Layers:
	-	`sha256:0d8192ce2954c6a959615d982ceaa8825bd46cf89ead122b5706cc29fcf8bd71`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e15191f85a79618d9811e8747e99ac98b0a40bfaae0aaaa5001bb1230c1d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6207675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2b8f5a6e48a97cd470606ae3bf871c5e7a728291b699ed0fc6ade464b4cd4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ceb26b4c7119501bb3160d6cbbe50dce6ca269cc3bc37d3bfb9a8d65ab54e83e`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.2 MB (6207167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a970c139d6bb37d99b808c536d15fdfb2452430180d1906126f13f7c0e3e65c8`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:dbb4f985f00b8ed1cf158bbc14683f3982c6af4dbbd8a11fb368833ce8ab40d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762707c4a125db65916d8207dfc41bd88cb661dfd73431bef3936beaa1b6e79`

```dockerfile
```

-	Layers:
	-	`sha256:6d1ce7246188626d86f106948c8c45d6673d92d8b12bc55a2f76ad1a4a77c06b`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:0d2f692536149ac22566cf1b8c8c155bbf8704b0219606b603d37a2eb62f66a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6271147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5853d65dc9c9039e59f599fe9d6264c1b4b775d3ec6a9efaefa2487a1b2910c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:46 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:094159f217313d715a9c9416ce56b6efb6774fae53d0a118eb72c19dd5050f69`  
		Last Modified: Mon, 29 Jun 2026 15:45:02 GMT  
		Size: 6.3 MB (6270639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1d383fd4674e2d350a56d40d9d7a4a018dcdcac31733be7d84231bbad1d5b`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:7388f5e7e39dd5b070cb36fd9cf62973a1dbe1673ae86098ed3504c78e1ef328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a70cea4e571b8e5e9bb3f1775b350266ece5ba0911b4910d792e2f5c7a8522`

```dockerfile
```

-	Layers:
	-	`sha256:c683a72a6137cd681254bab9a60e1a450a3a8e636d80bcccb57e77942df0b512`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:fa31a78cc1dfc74ac5954db2d0fabe8025d55442dd778436f11eb45bbad212b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a751449230c715131c826c9e954f6c6faab06fed9d6ac6ef617518f68b0f57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c051b099bef1cbfeba54872473e4a7281c4a402d9f0b7c1bdf892e5e21ea8c51`  
		Last Modified: Mon, 29 Jun 2026 15:45:04 GMT  
		Size: 6.7 MB (6666239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd00d66579c55de314f0aa7536b46c9471486f908c26ae17a7d930bfdd9fb9`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:6e482d7d215597ddb64e6a49fb2d97ed5f170b063872e7b945de9574375342eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa169f897fcb8ad6d1b168458e6f22434b580cca5dd468838bbd781ec75f31a`

```dockerfile
```

-	Layers:
	-	`sha256:cfe01b7f8ddd174d7457c698713d2616d4d35273045161e7a898b8d8a593e3f4`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:9f0daa17d5998a047f470ea9d8842dc0eb687557782823b3fea2bc5538aeaf23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131054329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b328dd4c47b0486963aab87b1d33d09cc56b17a894d7d1f8cbff35d6514a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:13:42 GMT
RUN cmd /S /C #(nop) COPY file:d28b1675c385af4d7600302dadf40a3bf46cd73b4ca42fe37500427a26b9b480 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:13:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:13:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:13:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:13:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3906542123b76df88980ceb04181b631e9922c06a031cb9d6c343bc4fc335b59`  
		Last Modified: Mon, 29 Jun 2026 20:13:57 GMT  
		Size: 7.1 MB (7050935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0464c24aec36583186ddd00d659a44cbfbe8eb6967595e263922cee114f11541`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e247b1ab45847502319a775832f1e37efd8e27edab85850c1cd39355d7c59a`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bca692b6b90a8e7b2b7d9ea755343336ec76f096b7f3eef575a86f50e64dc5`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3557d9ac8171b21f42a1bee80b244527a6000a38cb1673347a20e01f26387`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:c11af972c99ae542de8925e6a7d9c533aa1eb039660420d2074beed6089b3bf0
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
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4e53bdfe4a9d810005abaf974dd9a12374c9cd187fa6be4622eff6a73b9e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8ea3792d3865371b24b0504e2a7a61140487a85c1289a56e6b0a414f3aa451`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fb591416c4f81c00164a6df7c9a0df260683e8939dad253a229dad6006eed7`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 7.0 MB (7001975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a94003f98dbb2cec821705d1615ee3fabdb6278a14a965fad556f00935df4e`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca954dfa8945adfa8283aac38370a786f5ed56c79b3a242cdc0a7717732e4c01`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d2617716222bd82abc599cbe8277f98292977c0dfdd769178f6be9d0fdbfafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf691e94e06290aeb75516eb80f45749858c6ac66c0462f375e5b23f89c0f28`

```dockerfile
```

-	Layers:
	-	`sha256:051ab4a8c59747a86c2b341f78f881dcb5ce383e1adb18760b2e37658493f9f3`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:13a3f0e29c614c6b948bac76e8511e103dae75a1f3aafb215d49defef515bda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10202964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b0bb66ac4162fc21cb64f4e23f7840a339f47c9c6e9fe68e07f879189b36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c57aa7f84636f8b81c22758ea4a628036299dea2750a000eb5de6220234b418`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 7.0 MB (6992381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b307022eba60d3fa1d5f402e6c270a824a7c22733d6b54b89a11d8e47f5df06`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979223c0d164e45ff3d261730284785ca49e194cd773a37086da9bdd856159e`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cc9db77acad1e638c9d195fe27bf9cb73a582f1d6c8a48de4aac85d42fe8b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e4eea65b1e82754ac2719f2026f89bf4d253eda69a68c1c7a0753cc424985`

```dockerfile
```

-	Layers:
	-	`sha256:be67ebf23efa9ed614c3e6ecbd8dbfe60c3c196c67672894c62befc4102a028d`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:064222a09af7b194af6760d6089aa9ebd93fe7b8136ec2193ddb72dd78d8bd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10740987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b422fa2e0339d3eb86f18cdd7040198afd726fadc2c6c0f499eff9c9038c9926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d45f995edc436f16aee98c90da4e281a787ba379a91c7b812155f24b01f240c`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 6.6 MB (6619532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721188e517e99c1592046fd1c1f9d23061e01b186bfce2cef6bc65a52a5f7fd`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d19df182cbee156b010b04853280b7c12519c2b2a73a5d9a80ae357c814c67`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e4aef08d7bba47a53a2cdfea2260f5792c1fdb440a5ad4ff982730170aa3deb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb8badc11acca1d928d62f328aa0f3707584a4655e9abfa03e3b1b697d59a65`

```dockerfile
```

-	Layers:
	-	`sha256:e3cd06dd05bb0a25b9621e25ea152cd6cffebb5eff99e2740970497eaafedfd3`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:c11af972c99ae542de8925e6a7d9c533aa1eb039660420d2074beed6089b3bf0
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
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4e53bdfe4a9d810005abaf974dd9a12374c9cd187fa6be4622eff6a73b9e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8ea3792d3865371b24b0504e2a7a61140487a85c1289a56e6b0a414f3aa451`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fb591416c4f81c00164a6df7c9a0df260683e8939dad253a229dad6006eed7`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 7.0 MB (7001975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a94003f98dbb2cec821705d1615ee3fabdb6278a14a965fad556f00935df4e`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca954dfa8945adfa8283aac38370a786f5ed56c79b3a242cdc0a7717732e4c01`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d2617716222bd82abc599cbe8277f98292977c0dfdd769178f6be9d0fdbfafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf691e94e06290aeb75516eb80f45749858c6ac66c0462f375e5b23f89c0f28`

```dockerfile
```

-	Layers:
	-	`sha256:051ab4a8c59747a86c2b341f78f881dcb5ce383e1adb18760b2e37658493f9f3`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:13a3f0e29c614c6b948bac76e8511e103dae75a1f3aafb215d49defef515bda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10202964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b0bb66ac4162fc21cb64f4e23f7840a339f47c9c6e9fe68e07f879189b36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c57aa7f84636f8b81c22758ea4a628036299dea2750a000eb5de6220234b418`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 7.0 MB (6992381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b307022eba60d3fa1d5f402e6c270a824a7c22733d6b54b89a11d8e47f5df06`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979223c0d164e45ff3d261730284785ca49e194cd773a37086da9bdd856159e`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:cc9db77acad1e638c9d195fe27bf9cb73a582f1d6c8a48de4aac85d42fe8b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e4eea65b1e82754ac2719f2026f89bf4d253eda69a68c1c7a0753cc424985`

```dockerfile
```

-	Layers:
	-	`sha256:be67ebf23efa9ed614c3e6ecbd8dbfe60c3c196c67672894c62befc4102a028d`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:064222a09af7b194af6760d6089aa9ebd93fe7b8136ec2193ddb72dd78d8bd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10740987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b422fa2e0339d3eb86f18cdd7040198afd726fadc2c6c0f499eff9c9038c9926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d45f995edc436f16aee98c90da4e281a787ba379a91c7b812155f24b01f240c`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 6.6 MB (6619532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721188e517e99c1592046fd1c1f9d23061e01b186bfce2cef6bc65a52a5f7fd`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d19df182cbee156b010b04853280b7c12519c2b2a73a5d9a80ae357c814c67`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e4aef08d7bba47a53a2cdfea2260f5792c1fdb440a5ad4ff982730170aa3deb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb8badc11acca1d928d62f328aa0f3707584a4655e9abfa03e3b1b697d59a65`

```dockerfile
```

-	Layers:
	-	`sha256:e3cd06dd05bb0a25b9621e25ea152cd6cffebb5eff99e2740970497eaafedfd3`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:1b5a0a665cbe50a4ea28e8a82cf809b26cee5027d1fcaf8682fadf8f385fdf29
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
$ docker pull nats@sha256:da52c7cd2dd8cfbfd7d2dfb251b761e42dbfd6fe0acb09fd26cbb42bdddb2866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6857592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ccfa5190b3b463a3fcf96e85c57584707cb0e37e977effc0b13df38ad27da`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:13:56 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:56 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:13:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:001b0b866410b42b38bcb2e428951af42433891ff425dfcce0b3a53cf93d9cf5`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.9 MB (6857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301e2bd5843dce0ae9f53e3b56e505349c98b58f06c463430d25b5c5ff3d2ac`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4e6b9bd23e99f1e6893cbc2298ff6542ff362ac45479424f0cbbaa44e0bd7932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b91a2a2149df4bdf026d1ba840708ff2f744d4552979b6f5238e32d4b9fadd`

```dockerfile
```

-	Layers:
	-	`sha256:f2654502a1c07929b5dba813de85a6fecf099bd5b4e5dc0304f5bffb9a55374a`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f954b0114100cc6b04d48371743c840445bbd9d9cd58fd347d548df20fb81377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc68893e7b073ba43eb1643ffef18c78a2bcde561b9df87690e4c25b31729d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:087a70319659349faa0bc66d2f258c634f201af06cf4cd72fd052fe0f1741923`  
		Last Modified: Mon, 29 Jun 2026 15:45:00 GMT  
		Size: 6.6 MB (6591390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48bfacc9913ae01cc25da4a4e0b5b45dd8572ebef94eb75ee659e643ca668f`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2ddfb53928614b91b72d029bf8c1fe2c18c9323525cddd2435738502af8f535f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c648adf5a8076bdff845afbe972feb29cbce83a045fc1fa7a6407350edd450`

```dockerfile
```

-	Layers:
	-	`sha256:f18d91a70c6190eda91e68db672ccbc0be90eca9e3a3cbca1053dac4180c85bb`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5acf1bcd52c9815e894b475e74896d5c20d20f75dc1d0a4609284c356a23e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eaac6cac973cc88e6d44cfa8e4fa97db877aa382eca9ca11a3aabdc71efaa4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95cb78be6f3eb15e97acc3a341503927e5ccafbd12a09b4a1b82fbb89f4787b5`  
		Last Modified: Mon, 29 Jun 2026 15:45:01 GMT  
		Size: 6.6 MB (6580972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce96a7f9a07f1a57504be91420ffc8fe2f13ee198161d2b34cfa5461201d23c9`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7350f027d99946847895026cb1af3842bdad2563af2c7a4902c947e3e5859335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365d446dc11c95971d0b41e292ef423e0863365d7c070019c54d2c193b476ff`

```dockerfile
```

-	Layers:
	-	`sha256:0d8192ce2954c6a959615d982ceaa8825bd46cf89ead122b5706cc29fcf8bd71`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e15191f85a79618d9811e8747e99ac98b0a40bfaae0aaaa5001bb1230c1d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6207675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2b8f5a6e48a97cd470606ae3bf871c5e7a728291b699ed0fc6ade464b4cd4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ceb26b4c7119501bb3160d6cbbe50dce6ca269cc3bc37d3bfb9a8d65ab54e83e`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.2 MB (6207167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a970c139d6bb37d99b808c536d15fdfb2452430180d1906126f13f7c0e3e65c8`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:dbb4f985f00b8ed1cf158bbc14683f3982c6af4dbbd8a11fb368833ce8ab40d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762707c4a125db65916d8207dfc41bd88cb661dfd73431bef3936beaa1b6e79`

```dockerfile
```

-	Layers:
	-	`sha256:6d1ce7246188626d86f106948c8c45d6673d92d8b12bc55a2f76ad1a4a77c06b`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:0d2f692536149ac22566cf1b8c8c155bbf8704b0219606b603d37a2eb62f66a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6271147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5853d65dc9c9039e59f599fe9d6264c1b4b775d3ec6a9efaefa2487a1b2910c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:46 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:094159f217313d715a9c9416ce56b6efb6774fae53d0a118eb72c19dd5050f69`  
		Last Modified: Mon, 29 Jun 2026 15:45:02 GMT  
		Size: 6.3 MB (6270639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1d383fd4674e2d350a56d40d9d7a4a018dcdcac31733be7d84231bbad1d5b`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7388f5e7e39dd5b070cb36fd9cf62973a1dbe1673ae86098ed3504c78e1ef328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a70cea4e571b8e5e9bb3f1775b350266ece5ba0911b4910d792e2f5c7a8522`

```dockerfile
```

-	Layers:
	-	`sha256:c683a72a6137cd681254bab9a60e1a450a3a8e636d80bcccb57e77942df0b512`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:fa31a78cc1dfc74ac5954db2d0fabe8025d55442dd778436f11eb45bbad212b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a751449230c715131c826c9e954f6c6faab06fed9d6ac6ef617518f68b0f57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c051b099bef1cbfeba54872473e4a7281c4a402d9f0b7c1bdf892e5e21ea8c51`  
		Last Modified: Mon, 29 Jun 2026 15:45:04 GMT  
		Size: 6.7 MB (6666239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd00d66579c55de314f0aa7536b46c9471486f908c26ae17a7d930bfdd9fb9`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6e482d7d215597ddb64e6a49fb2d97ed5f170b063872e7b945de9574375342eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa169f897fcb8ad6d1b168458e6f22434b580cca5dd468838bbd781ec75f31a`

```dockerfile
```

-	Layers:
	-	`sha256:cfe01b7f8ddd174d7457c698713d2616d4d35273045161e7a898b8d8a593e3f4`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:1d52723019944547c28befc6831cf54a194fe6cf5da2cbe5d83dada671148eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:9f0daa17d5998a047f470ea9d8842dc0eb687557782823b3fea2bc5538aeaf23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131054329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b328dd4c47b0486963aab87b1d33d09cc56b17a894d7d1f8cbff35d6514a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:13:42 GMT
RUN cmd /S /C #(nop) COPY file:d28b1675c385af4d7600302dadf40a3bf46cd73b4ca42fe37500427a26b9b480 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:13:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:13:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:13:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:13:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3906542123b76df88980ceb04181b631e9922c06a031cb9d6c343bc4fc335b59`  
		Last Modified: Mon, 29 Jun 2026 20:13:57 GMT  
		Size: 7.1 MB (7050935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0464c24aec36583186ddd00d659a44cbfbe8eb6967595e263922cee114f11541`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e247b1ab45847502319a775832f1e37efd8e27edab85850c1cd39355d7c59a`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bca692b6b90a8e7b2b7d9ea755343336ec76f096b7f3eef575a86f50e64dc5`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3557d9ac8171b21f42a1bee80b244527a6000a38cb1673347a20e01f26387`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:1d52723019944547c28befc6831cf54a194fe6cf5da2cbe5d83dada671148eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:9f0daa17d5998a047f470ea9d8842dc0eb687557782823b3fea2bc5538aeaf23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131054329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b328dd4c47b0486963aab87b1d33d09cc56b17a894d7d1f8cbff35d6514a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:13:42 GMT
RUN cmd /S /C #(nop) COPY file:d28b1675c385af4d7600302dadf40a3bf46cd73b4ca42fe37500427a26b9b480 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:13:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:13:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:13:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:13:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3906542123b76df88980ceb04181b631e9922c06a031cb9d6c343bc4fc335b59`  
		Last Modified: Mon, 29 Jun 2026 20:13:57 GMT  
		Size: 7.1 MB (7050935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0464c24aec36583186ddd00d659a44cbfbe8eb6967595e263922cee114f11541`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e247b1ab45847502319a775832f1e37efd8e27edab85850c1cd39355d7c59a`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bca692b6b90a8e7b2b7d9ea755343336ec76f096b7f3eef575a86f50e64dc5`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3557d9ac8171b21f42a1bee80b244527a6000a38cb1673347a20e01f26387`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:1b5a0a665cbe50a4ea28e8a82cf809b26cee5027d1fcaf8682fadf8f385fdf29
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
$ docker pull nats@sha256:da52c7cd2dd8cfbfd7d2dfb251b761e42dbfd6fe0acb09fd26cbb42bdddb2866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6857592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ccfa5190b3b463a3fcf96e85c57584707cb0e37e977effc0b13df38ad27da`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:13:56 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:56 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:13:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:001b0b866410b42b38bcb2e428951af42433891ff425dfcce0b3a53cf93d9cf5`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.9 MB (6857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301e2bd5843dce0ae9f53e3b56e505349c98b58f06c463430d25b5c5ff3d2ac`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4e6b9bd23e99f1e6893cbc2298ff6542ff362ac45479424f0cbbaa44e0bd7932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b91a2a2149df4bdf026d1ba840708ff2f744d4552979b6f5238e32d4b9fadd`

```dockerfile
```

-	Layers:
	-	`sha256:f2654502a1c07929b5dba813de85a6fecf099bd5b4e5dc0304f5bffb9a55374a`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f954b0114100cc6b04d48371743c840445bbd9d9cd58fd347d548df20fb81377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc68893e7b073ba43eb1643ffef18c78a2bcde561b9df87690e4c25b31729d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:087a70319659349faa0bc66d2f258c634f201af06cf4cd72fd052fe0f1741923`  
		Last Modified: Mon, 29 Jun 2026 15:45:00 GMT  
		Size: 6.6 MB (6591390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48bfacc9913ae01cc25da4a4e0b5b45dd8572ebef94eb75ee659e643ca668f`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2ddfb53928614b91b72d029bf8c1fe2c18c9323525cddd2435738502af8f535f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c648adf5a8076bdff845afbe972feb29cbce83a045fc1fa7a6407350edd450`

```dockerfile
```

-	Layers:
	-	`sha256:f18d91a70c6190eda91e68db672ccbc0be90eca9e3a3cbca1053dac4180c85bb`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5acf1bcd52c9815e894b475e74896d5c20d20f75dc1d0a4609284c356a23e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eaac6cac973cc88e6d44cfa8e4fa97db877aa382eca9ca11a3aabdc71efaa4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95cb78be6f3eb15e97acc3a341503927e5ccafbd12a09b4a1b82fbb89f4787b5`  
		Last Modified: Mon, 29 Jun 2026 15:45:01 GMT  
		Size: 6.6 MB (6580972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce96a7f9a07f1a57504be91420ffc8fe2f13ee198161d2b34cfa5461201d23c9`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7350f027d99946847895026cb1af3842bdad2563af2c7a4902c947e3e5859335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365d446dc11c95971d0b41e292ef423e0863365d7c070019c54d2c193b476ff`

```dockerfile
```

-	Layers:
	-	`sha256:0d8192ce2954c6a959615d982ceaa8825bd46cf89ead122b5706cc29fcf8bd71`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e15191f85a79618d9811e8747e99ac98b0a40bfaae0aaaa5001bb1230c1d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6207675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2b8f5a6e48a97cd470606ae3bf871c5e7a728291b699ed0fc6ade464b4cd4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ceb26b4c7119501bb3160d6cbbe50dce6ca269cc3bc37d3bfb9a8d65ab54e83e`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.2 MB (6207167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a970c139d6bb37d99b808c536d15fdfb2452430180d1906126f13f7c0e3e65c8`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:dbb4f985f00b8ed1cf158bbc14683f3982c6af4dbbd8a11fb368833ce8ab40d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762707c4a125db65916d8207dfc41bd88cb661dfd73431bef3936beaa1b6e79`

```dockerfile
```

-	Layers:
	-	`sha256:6d1ce7246188626d86f106948c8c45d6673d92d8b12bc55a2f76ad1a4a77c06b`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:0d2f692536149ac22566cf1b8c8c155bbf8704b0219606b603d37a2eb62f66a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6271147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5853d65dc9c9039e59f599fe9d6264c1b4b775d3ec6a9efaefa2487a1b2910c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:46 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:094159f217313d715a9c9416ce56b6efb6774fae53d0a118eb72c19dd5050f69`  
		Last Modified: Mon, 29 Jun 2026 15:45:02 GMT  
		Size: 6.3 MB (6270639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1d383fd4674e2d350a56d40d9d7a4a018dcdcac31733be7d84231bbad1d5b`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7388f5e7e39dd5b070cb36fd9cf62973a1dbe1673ae86098ed3504c78e1ef328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a70cea4e571b8e5e9bb3f1775b350266ece5ba0911b4910d792e2f5c7a8522`

```dockerfile
```

-	Layers:
	-	`sha256:c683a72a6137cd681254bab9a60e1a450a3a8e636d80bcccb57e77942df0b512`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:fa31a78cc1dfc74ac5954db2d0fabe8025d55442dd778436f11eb45bbad212b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a751449230c715131c826c9e954f6c6faab06fed9d6ac6ef617518f68b0f57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c051b099bef1cbfeba54872473e4a7281c4a402d9f0b7c1bdf892e5e21ea8c51`  
		Last Modified: Mon, 29 Jun 2026 15:45:04 GMT  
		Size: 6.7 MB (6666239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd00d66579c55de314f0aa7536b46c9471486f908c26ae17a7d930bfdd9fb9`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6e482d7d215597ddb64e6a49fb2d97ed5f170b063872e7b945de9574375342eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa169f897fcb8ad6d1b168458e6f22434b580cca5dd468838bbd781ec75f31a`

```dockerfile
```

-	Layers:
	-	`sha256:cfe01b7f8ddd174d7457c698713d2616d4d35273045161e7a898b8d8a593e3f4`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:f701716476a8d968bd766320239d98d7f973ebaaa7a6f960f65648bda132229e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:2c61006c6743420a33c3ade658d600d9b81f09a86df8c44fe02741a71d196d7f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140052973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782541001e22820de00703de294e85e7c622fc9ea85c9030e8fda96177afa0cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 29 Jun 2026 19:16:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Jun 2026 19:16:31 GMT
ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 19:16:32 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:16:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:16:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.3/nats-server-v2.14.3-windows-amd64.zip
# Mon, 29 Jun 2026 19:16:37 GMT
ENV NATS_SERVER_SHASUM=94e338d742761272e31eab1efb1f767eac3a2e56e4c05a7933c65a73fe95a27b
# Mon, 29 Jun 2026 19:17:35 GMT
RUN Set-PSDebug -Trace 2
# Mon, 29 Jun 2026 19:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 29 Jun 2026 19:18:06 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 19:18:08 GMT
EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 19:18:09 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 19:18:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac87f215828b12e2044c46470b221ea4307d0fc11cf8280e12474587a59317d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff6f7da74f9e652f79bc8278319981b268148b1548a3ef4220d3ccbe4b5473d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e85164857353b52ed850cc83049bc199678edaed484f95d1e38aa0a4f1b525b`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706cc542b32b6c088b1b95499c39a0c6f9dbe749f47087a0cd668545100147ba`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25bcf16bfd2387cc38d31f75eeac32290dada9d452e1f50b902530775f1c0ff`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aecb5ee131c5c835ec5c73c2ad224bf1e9c3ede99efeca9eec6a270f5c22b1`  
		Last Modified: Mon, 29 Jun 2026 19:18:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f1b98897859ea619b08dd0f0db49b009771052a13d263d4980a21c40901f2`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 496.7 KB (496723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784da3b63359a7bbb87eb47bb8a637b409b418e94af977bf3c24722cbc2ec89e`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 7.4 MB (7417113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae24643aacc8edba76b5661a3358a9461f9fda9a7d1f0fccaeca461dfb074a23`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe52ddb42630f70fd61331adf5e83118d27382c4d3922882adb2d981105bac94`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087e85133498df0eb7d45b8bc9353ec3fa1fc98964b2f88c33152ca73bf5abd6`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9462b672f1e05436ba0020f6b3b71b8db8b844d5c5183c1088c29d06d39df1be`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:f701716476a8d968bd766320239d98d7f973ebaaa7a6f960f65648bda132229e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:2c61006c6743420a33c3ade658d600d9b81f09a86df8c44fe02741a71d196d7f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140052973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782541001e22820de00703de294e85e7c622fc9ea85c9030e8fda96177afa0cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 29 Jun 2026 19:16:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Jun 2026 19:16:31 GMT
ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 19:16:32 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:16:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:16:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.3/nats-server-v2.14.3-windows-amd64.zip
# Mon, 29 Jun 2026 19:16:37 GMT
ENV NATS_SERVER_SHASUM=94e338d742761272e31eab1efb1f767eac3a2e56e4c05a7933c65a73fe95a27b
# Mon, 29 Jun 2026 19:17:35 GMT
RUN Set-PSDebug -Trace 2
# Mon, 29 Jun 2026 19:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 29 Jun 2026 19:18:06 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 19:18:08 GMT
EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 19:18:09 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 19:18:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac87f215828b12e2044c46470b221ea4307d0fc11cf8280e12474587a59317d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff6f7da74f9e652f79bc8278319981b268148b1548a3ef4220d3ccbe4b5473d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e85164857353b52ed850cc83049bc199678edaed484f95d1e38aa0a4f1b525b`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706cc542b32b6c088b1b95499c39a0c6f9dbe749f47087a0cd668545100147ba`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25bcf16bfd2387cc38d31f75eeac32290dada9d452e1f50b902530775f1c0ff`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aecb5ee131c5c835ec5c73c2ad224bf1e9c3ede99efeca9eec6a270f5c22b1`  
		Last Modified: Mon, 29 Jun 2026 19:18:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f1b98897859ea619b08dd0f0db49b009771052a13d263d4980a21c40901f2`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 496.7 KB (496723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784da3b63359a7bbb87eb47bb8a637b409b418e94af977bf3c24722cbc2ec89e`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 7.4 MB (7417113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae24643aacc8edba76b5661a3358a9461f9fda9a7d1f0fccaeca461dfb074a23`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe52ddb42630f70fd61331adf5e83118d27382c4d3922882adb2d981105bac94`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087e85133498df0eb7d45b8bc9353ec3fa1fc98964b2f88c33152ca73bf5abd6`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9462b672f1e05436ba0020f6b3b71b8db8b844d5c5183c1088c29d06d39df1be`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12`

```console
$ docker pull nats@sha256:df6c75f572c2b0f74dfa062505453192d899149701f198981f393ebb6588b9e1
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
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12` - linux; amd64

```console
$ docker pull nats@sha256:7150f4fdf587569abab9253aa349f72d871da06c77d36aac4436baab884f8c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6658478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6abe773e0ca7e8a35d9a950781562f2e0e465852116c0c49f2de69d6afba56`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:14:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:14:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:14:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:14:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:14:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:14:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:674ddc4edf02c32fd9e0c399e4ce2550d462d0349f360d1e401935b1cc4552a3`  
		Last Modified: Mon, 29 Jun 2026 15:45:26 GMT  
		Size: 6.7 MB (6657969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5702d3684f758185c73e87190842fd53cf65ff30cd7f72a65f65928e90fd72`  
		Last Modified: Mon, 29 Jun 2026 19:14:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:740aed9cbb77fa0feb9593a11b3ef7d80b0326393e62c8bdd29fb28f8deae33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b929051330e300f3043167fc391e5a658f9be6b99625f14821f9e9168a8e6a1`

```dockerfile
```

-	Layers:
	-	`sha256:15be1d8687e3ccb288b2395ac350e965c7b7866d8520bd18a41480f378b731c2`  
		Last Modified: Mon, 29 Jun 2026 19:14:05 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:65f623b6cde3c78df0b0d142ddc6e3e3bd1d9501422375bf621c8ab4a1955ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6398008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a728c107fe662f7111598a56d71ae7c36f4f5a4dd5d1f3b1b4a18bf937df0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:14 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9d8b42e91101f55d0b914352f42379d187b356167e68b6a4d7e248306781093`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.4 MB (6397501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d4cfe960fa26c031af0940ca78ea32b86745fc09a5196c72ee268c481ea651`  
		Last Modified: Mon, 29 Jun 2026 20:10:19 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:270e75e31932b739863421ce378d21bc9b4cbc65319749a56e84db12b75b06db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f84dc1cf6dac3435e77c51283d0504b385c0706684a17a6e1834692e0e300e9`

```dockerfile
```

-	Layers:
	-	`sha256:183c92f9da3d80b68ad84ea10e28ffa86aa9a426aa89e1ee50a75446473bdd53`  
		Last Modified: Mon, 29 Jun 2026 20:10:19 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:965e0f30952fe53c0edbbf51907861203a344a9f436d2f16e44ec62bbc6bc346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6389204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9954dc82025ebe69fb6051eba4e8b56422339f0c76b2978d73e05e4e95f4b686`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:13 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f51f3ae5a0e9a233d660597cb0991d0e4eda1b8d6081f2ebf7b11bf49726cbb`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.4 MB (6388696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064965fad9d634082e200408edb6c3cfd405a94c5e956a0589886e52ab1e280e`  
		Last Modified: Mon, 29 Jun 2026 20:10:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:371542e6b03232abc94eb181db393c6435a837da512cce3804798309c30bdd0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ea3056abc5f4e4d1b686c3750009080f9d259771aab353ae3dc28221d91b3`

```dockerfile
```

-	Layers:
	-	`sha256:207767c47f99e2d1e1fedd52ce5576598e2145c2fedbd08d52ebcb17283299be`  
		Last Modified: Mon, 29 Jun 2026 20:10:17 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cab7e89c5c123fa2c3080f70c5b47f612c9dc4ac52dc4323fbb3a595c57d7e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6136ec41f85090255a3129de60d735886601c26b2dff3bb5ae840dcfe8972d4b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:59 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:59 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c7f4ed7c5caaf7674fe731cc4314250f15b64d928d938c120113fda642ab9e35`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.1 MB (6055262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54c6d444001ace11b4843342fbb1034885520461c7f6927b617ae9ceec4f2be`  
		Last Modified: Mon, 29 Jun 2026 20:10:03 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:21a6ec729bb63eeb5fd248400b0794cea72020b49014664c9ea8f69873926b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b8f27c27fd4485ac0c2fb9fbd5f577f624409582d839d08b012e5a8980744`

```dockerfile
```

-	Layers:
	-	`sha256:359f4232c60d44b72e23371b39eef2f62ada8b687692b2f6f30998f4754f5cd3`  
		Last Modified: Mon, 29 Jun 2026 20:10:03 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; ppc64le

```console
$ docker pull nats@sha256:dffd7ab5566215b39ecc27f4cfbcbec3c87c5fc4d32314065b27fd2f8ab7be7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6114182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac585563eab840d4c0a5e821db019f88a9ffed79a5b5ac27087e72ae35f1674`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68d08cefc115ab2d0ba836794a2aafdbd770ca3b82386eaca56b76eface4067a`  
		Last Modified: Mon, 29 Jun 2026 15:45:25 GMT  
		Size: 6.1 MB (6113673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44bd89ff0f6f728c9f3bc4b6f7be421abaa6e18d57cfc1df853cbe8892117a2`  
		Last Modified: Mon, 29 Jun 2026 19:12:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:507a6e760ac10e306655b5e454edf3ada3f99dc7a91c5f550316e528a7eb2435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace002f95a4f8bad573dd00622c3969d09ed698044207e366057ba33a9a84a5f`

```dockerfile
```

-	Layers:
	-	`sha256:4caf767452a66fa4931c741b42734d256bf6283f3a6a1dd604cfba793beb3aa3`  
		Last Modified: Mon, 29 Jun 2026 19:12:53 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; s390x

```console
$ docker pull nats@sha256:b5f2090a2865bc73183bdbbd5c2db2d4a5e90ab9902682414eee67678f44290e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6507115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081b3d096315958b9213985797ab5c0d1d1f51a9c134de884bdaddeafc215ec5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:23 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:23 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee8c267e3cc1a37bddcdb99b2da7bdd61a07738138488ac8641bc09f0cb7dc28`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.5 MB (6506606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3296f5cd680ca40417700ab16719d01bec8116be5da79289dd9c07b418c26d`  
		Last Modified: Mon, 29 Jun 2026 19:18:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:29663b73d5d3b96d00fbcad47681317129a61e699cc8a6a1b4c60f6b3773993e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8327c934690bae04254b49b552f8448751bd0bcc4abada12f8c086c470592bfc`

```dockerfile
```

-	Layers:
	-	`sha256:2e4c1745430ed822c5b545dbfce9175f49597264d12d3dc7bcd1aa56762e9a7f`  
		Last Modified: Mon, 29 Jun 2026 19:18:32 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:5ecdfc23d4535a0aa4e23ea67d7f08e7100998b49c3dd1e63447b937700d7fbd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130850622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a629255666593ccb84568e18360988f19cf474b041607eab7de75faef30e045`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:14:23 GMT
RUN cmd /S /C #(nop) COPY file:d8af06503cfb328e70ba402a862262e409f0fc6efb978ecfbf29b4bf28c77da7 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:14:24 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:14:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:14:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:14:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f25f32e4beeeac81e5d4a8bac558446351e6d2f47c6c7236375f0595f8891a`  
		Last Modified: Mon, 29 Jun 2026 20:14:35 GMT  
		Size: 6.8 MB (6847146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a9bbbb700b4293074cd53c5f61f55df17ea3fe16126c4be3467ef619f37508`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee53ab55fd1943eb961de73595979a4ab2a3421568fbcea2f32471235ca5cc62`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b542ff1d76894ae7dadda2d201149301d63e9293d0c72eebb7b455325a22958`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517956deb7c51ec9602dd378c58b84756fcd2a8c7bbe9e2f50079414d869269d`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-alpine`

```console
$ docker pull nats@sha256:2ca98656a279b2d88cfdf2b8c3f0d5d7f3941ae9dc2ab12ebaa92d83e0f4ccdb
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
$ docker pull nats@sha256:425d3d24ac3b92b88cda1b153cc72f9535bfd1c0bcdd8f67740d9b22220e30f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4df4dc451af97c3499db640c4a6e0d6d6faa100799fe727d9e7e8be2f85756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f302f59e4314d1878834e19e5b71b17be0ae76d484bf8d2d1d2e13a49e87ffd`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 7.1 MB (7068014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d50079454fd127c8d11556ad65e8ae8d330d9b23fdebfbf84a7a2e1ef81830`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91585d73d765544cfc68e45bf7451cdcc41e98760273b1c14b994ea65a9421ca`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:627fc61f544347aee1241d88a072aaf2f482f3fe6d7dcae343a3386a0f71b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7dfec1367766e5087363e33ace912bc5cecf9d000ff7a9fcfc32e5edd3a827`

```dockerfile
```

-	Layers:
	-	`sha256:d5a9967d703c4696f237199b5172918a071980ff994625807ad12b66209342e7`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:da848228ada3065f9c2a15a503406d61499de6d7fba699cb3817e28f37f7402a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10304206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec13ec03de80b2e6a0934d8b43ae748adebabc51a7a5c46e46b20f578b49155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:13:09 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:13:09 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:13:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:13:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:13:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:13:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d0133a34d5e99791b0b3206d7eb6a9217a98a390b98e62774a8f53f4bda8c4`  
		Last Modified: Mon, 29 Jun 2026 19:13:14 GMT  
		Size: 6.8 MB (6808434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8527ed2a249d0102a50cb5daf85524e8a609d2dbc9cf393b619dd753e6cdda4`  
		Last Modified: Mon, 29 Jun 2026 19:13:13 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37a8bf70ff4688a4da1c7d8e4773643b11453e39faee3f9a3a2a5d114af4088`  
		Last Modified: Mon, 29 Jun 2026 19:13:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:402db16d9854509328c72bc3f951aa99d3247261cd154385a6603dc821063f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e2d38edf0c20d359c7a16600c7ca141f330898742c9eefc3bde4c3405faf2e`

```dockerfile
```

-	Layers:
	-	`sha256:b501f81ba3b78b726cf71f13fe9f1b0abe45339eb3815630fbbc8b320275bbf2`  
		Last Modified: Mon, 29 Jun 2026 19:13:13 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bdb7a59f6844170dc8334f1a35f8877fb79498789e8bece8335edd8570d70a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10011404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac147b9241325ef59b2f84a81dd728295ccc3de6ee18a853ba20326f55a6a7d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:34 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:12:34 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:12:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:34 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03da412883a51e21464226481f5dc565bc91499890464f6c8b947b8bb4f3224`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 6.8 MB (6800823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32017da75c3a70cb844f8cb7b3a37cd94f78537d3e2cd628483d23d537a2b9b8`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3bfb6f5d6546a6d9549ad1a5195221e2753c0f62fcc02026b3f4aca9944dde`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a80b31cb272cdafe50b728781f58bb9e8f82058635d34dab166a1bb7943ab003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd3bc4d2dd9978a3547b6749a373898c58d319e3c2e1322b10454bf3f6dd41b`

```dockerfile
```

-	Layers:
	-	`sha256:3a3d19fde6df2d85168077489af805b3edb561dff5c4de446506516319464998`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e7a28a0c0300aa1a737b1fd8c567f6da0fe96d970c3ee97dedaf475bc065e2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10589316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a473d4229d429ef3f28373acf98500d4f5fa8a054c1438e691c71f68c49977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:27 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:12:27 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:12:27 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:27 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:27 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159748456c3959ce6919c808af480b38f00972cf9fc9db5caaf0d3ccdf33e9c5`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 6.5 MB (6467860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a71adc900265c0969d3baefd35719826032c2917baf34e23acb556bd849192`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef83f1bdacd18e095d1825b1e6534d4c8290d91e67047fbd6b726c9c3a2a4cb0`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8af248235d9832c27c4088dfd29818c8474c47b99743d0ff62a2037c580bcc56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e2ff5e55bab6e49a25ff808dd57a35732350849f8f38e7fa435b6472dc2b00`

```dockerfile
```

-	Layers:
	-	`sha256:0e95cccbe78acbcfc3d29b69f3a4ca240123e634f7b76d89f717ceb6c6d791c6`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:79ab02351c08527aa75a4f0dcf0bcabf8313986a36b2974702bd8fb4980b9898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10248160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd4063f85a19f911d9ce871702a6b298f8a8f7bdb6cdd70bf271565cbd0383e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e590177a1f3832404927d73f703cd9b6de1bc6aa1c0a4071f73e62d61d6ff4d`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.5 MB (6527958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ea17abc7bdf67861515d4ae06c070fb7748d0cbec44453db6d05495a7af96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2a7741b38aa0865f53f2bc0c633a5727a70c07676d5f11582cbba4e5271703`

```dockerfile
```

-	Layers:
	-	`sha256:7c420f60382849b143e37e5624177f950ae9e5734cb82ee3cfc5487a594894d2`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:e416ac70e75c57154afc11270f4b79b26064bec8c6f45b33cc149de9369e4c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10555129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8f5c696629dedfa3f5d4827265a0ce1a254b61e328c4016a252e05fd6cd5d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2bc2f93033c9b7f596631cea725b6923dfa8204a1fbd0cad289cfb66ad686`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 6.9 MB (6917070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3319d5c969f4b3502a099f99e8b9d1c3bac616a3bddc3b10057dc687980fd7b1`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6498ad1fc5102f83402c9c078f53d9db7682b83a100cdf63606f711bce0f5d43`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9334e0829fc5846fd017385aec07371d829e8066ddd077be9208d80db65f9383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4430ea02178620fe9c9abc8a148ece6e6ef63f14d072c1c0f4852d54c98d2aa9`

```dockerfile
```

-	Layers:
	-	`sha256:f2d6fd7f8df0496ec5b02bad43bdccebdd9d1165cffbb23b9526bc4f3e6dbbdf`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-alpine3.22`

```console
$ docker pull nats@sha256:2ca98656a279b2d88cfdf2b8c3f0d5d7f3941ae9dc2ab12ebaa92d83e0f4ccdb
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
$ docker pull nats@sha256:425d3d24ac3b92b88cda1b153cc72f9535bfd1c0bcdd8f67740d9b22220e30f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4df4dc451af97c3499db640c4a6e0d6d6faa100799fe727d9e7e8be2f85756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f302f59e4314d1878834e19e5b71b17be0ae76d484bf8d2d1d2e13a49e87ffd`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 7.1 MB (7068014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d50079454fd127c8d11556ad65e8ae8d330d9b23fdebfbf84a7a2e1ef81830`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91585d73d765544cfc68e45bf7451cdcc41e98760273b1c14b994ea65a9421ca`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:627fc61f544347aee1241d88a072aaf2f482f3fe6d7dcae343a3386a0f71b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7dfec1367766e5087363e33ace912bc5cecf9d000ff7a9fcfc32e5edd3a827`

```dockerfile
```

-	Layers:
	-	`sha256:d5a9967d703c4696f237199b5172918a071980ff994625807ad12b66209342e7`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:da848228ada3065f9c2a15a503406d61499de6d7fba699cb3817e28f37f7402a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10304206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec13ec03de80b2e6a0934d8b43ae748adebabc51a7a5c46e46b20f578b49155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:13:09 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:13:09 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:13:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:13:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:13:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:13:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d0133a34d5e99791b0b3206d7eb6a9217a98a390b98e62774a8f53f4bda8c4`  
		Last Modified: Mon, 29 Jun 2026 19:13:14 GMT  
		Size: 6.8 MB (6808434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8527ed2a249d0102a50cb5daf85524e8a609d2dbc9cf393b619dd753e6cdda4`  
		Last Modified: Mon, 29 Jun 2026 19:13:13 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37a8bf70ff4688a4da1c7d8e4773643b11453e39faee3f9a3a2a5d114af4088`  
		Last Modified: Mon, 29 Jun 2026 19:13:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:402db16d9854509328c72bc3f951aa99d3247261cd154385a6603dc821063f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e2d38edf0c20d359c7a16600c7ca141f330898742c9eefc3bde4c3405faf2e`

```dockerfile
```

-	Layers:
	-	`sha256:b501f81ba3b78b726cf71f13fe9f1b0abe45339eb3815630fbbc8b320275bbf2`  
		Last Modified: Mon, 29 Jun 2026 19:13:13 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bdb7a59f6844170dc8334f1a35f8877fb79498789e8bece8335edd8570d70a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10011404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac147b9241325ef59b2f84a81dd728295ccc3de6ee18a853ba20326f55a6a7d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:34 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:12:34 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:12:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:34 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03da412883a51e21464226481f5dc565bc91499890464f6c8b947b8bb4f3224`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 6.8 MB (6800823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32017da75c3a70cb844f8cb7b3a37cd94f78537d3e2cd628483d23d537a2b9b8`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3bfb6f5d6546a6d9549ad1a5195221e2753c0f62fcc02026b3f4aca9944dde`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a80b31cb272cdafe50b728781f58bb9e8f82058635d34dab166a1bb7943ab003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd3bc4d2dd9978a3547b6749a373898c58d319e3c2e1322b10454bf3f6dd41b`

```dockerfile
```

-	Layers:
	-	`sha256:3a3d19fde6df2d85168077489af805b3edb561dff5c4de446506516319464998`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e7a28a0c0300aa1a737b1fd8c567f6da0fe96d970c3ee97dedaf475bc065e2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10589316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a473d4229d429ef3f28373acf98500d4f5fa8a054c1438e691c71f68c49977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:27 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:12:27 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:12:27 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:27 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:27 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159748456c3959ce6919c808af480b38f00972cf9fc9db5caaf0d3ccdf33e9c5`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 6.5 MB (6467860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a71adc900265c0969d3baefd35719826032c2917baf34e23acb556bd849192`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef83f1bdacd18e095d1825b1e6534d4c8290d91e67047fbd6b726c9c3a2a4cb0`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8af248235d9832c27c4088dfd29818c8474c47b99743d0ff62a2037c580bcc56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e2ff5e55bab6e49a25ff808dd57a35732350849f8f38e7fa435b6472dc2b00`

```dockerfile
```

-	Layers:
	-	`sha256:0e95cccbe78acbcfc3d29b69f3a4ca240123e634f7b76d89f717ceb6c6d791c6`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:79ab02351c08527aa75a4f0dcf0bcabf8313986a36b2974702bd8fb4980b9898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10248160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd4063f85a19f911d9ce871702a6b298f8a8f7bdb6cdd70bf271565cbd0383e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e590177a1f3832404927d73f703cd9b6de1bc6aa1c0a4071f73e62d61d6ff4d`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.5 MB (6527958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ea17abc7bdf67861515d4ae06c070fb7748d0cbec44453db6d05495a7af96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2a7741b38aa0865f53f2bc0c633a5727a70c07676d5f11582cbba4e5271703`

```dockerfile
```

-	Layers:
	-	`sha256:7c420f60382849b143e37e5624177f950ae9e5734cb82ee3cfc5487a594894d2`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:e416ac70e75c57154afc11270f4b79b26064bec8c6f45b33cc149de9369e4c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10555129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8f5c696629dedfa3f5d4827265a0ce1a254b61e328c4016a252e05fd6cd5d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2bc2f93033c9b7f596631cea725b6923dfa8204a1fbd0cad289cfb66ad686`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 6.9 MB (6917070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3319d5c969f4b3502a099f99e8b9d1c3bac616a3bddc3b10057dc687980fd7b1`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6498ad1fc5102f83402c9c078f53d9db7682b83a100cdf63606f711bce0f5d43`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9334e0829fc5846fd017385aec07371d829e8066ddd077be9208d80db65f9383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4430ea02178620fe9c9abc8a148ece6e6ef63f14d072c1c0f4852d54c98d2aa9`

```dockerfile
```

-	Layers:
	-	`sha256:f2d6fd7f8df0496ec5b02bad43bdccebdd9d1165cffbb23b9526bc4f3e6dbbdf`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-linux`

```console
$ docker pull nats@sha256:d36030092fd6372ff8bd774b87cd5eee71245f48eb8dca5d46b52a88870d9852
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
$ docker pull nats@sha256:7150f4fdf587569abab9253aa349f72d871da06c77d36aac4436baab884f8c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6658478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6abe773e0ca7e8a35d9a950781562f2e0e465852116c0c49f2de69d6afba56`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:14:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:14:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:14:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:14:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:14:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:14:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:674ddc4edf02c32fd9e0c399e4ce2550d462d0349f360d1e401935b1cc4552a3`  
		Last Modified: Mon, 29 Jun 2026 15:45:26 GMT  
		Size: 6.7 MB (6657969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5702d3684f758185c73e87190842fd53cf65ff30cd7f72a65f65928e90fd72`  
		Last Modified: Mon, 29 Jun 2026 19:14:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:740aed9cbb77fa0feb9593a11b3ef7d80b0326393e62c8bdd29fb28f8deae33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b929051330e300f3043167fc391e5a658f9be6b99625f14821f9e9168a8e6a1`

```dockerfile
```

-	Layers:
	-	`sha256:15be1d8687e3ccb288b2395ac350e965c7b7866d8520bd18a41480f378b731c2`  
		Last Modified: Mon, 29 Jun 2026 19:14:05 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:65f623b6cde3c78df0b0d142ddc6e3e3bd1d9501422375bf621c8ab4a1955ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6398008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a728c107fe662f7111598a56d71ae7c36f4f5a4dd5d1f3b1b4a18bf937df0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:14 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9d8b42e91101f55d0b914352f42379d187b356167e68b6a4d7e248306781093`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.4 MB (6397501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d4cfe960fa26c031af0940ca78ea32b86745fc09a5196c72ee268c481ea651`  
		Last Modified: Mon, 29 Jun 2026 20:10:19 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:270e75e31932b739863421ce378d21bc9b4cbc65319749a56e84db12b75b06db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f84dc1cf6dac3435e77c51283d0504b385c0706684a17a6e1834692e0e300e9`

```dockerfile
```

-	Layers:
	-	`sha256:183c92f9da3d80b68ad84ea10e28ffa86aa9a426aa89e1ee50a75446473bdd53`  
		Last Modified: Mon, 29 Jun 2026 20:10:19 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:965e0f30952fe53c0edbbf51907861203a344a9f436d2f16e44ec62bbc6bc346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6389204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9954dc82025ebe69fb6051eba4e8b56422339f0c76b2978d73e05e4e95f4b686`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:13 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f51f3ae5a0e9a233d660597cb0991d0e4eda1b8d6081f2ebf7b11bf49726cbb`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.4 MB (6388696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064965fad9d634082e200408edb6c3cfd405a94c5e956a0589886e52ab1e280e`  
		Last Modified: Mon, 29 Jun 2026 20:10:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:371542e6b03232abc94eb181db393c6435a837da512cce3804798309c30bdd0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ea3056abc5f4e4d1b686c3750009080f9d259771aab353ae3dc28221d91b3`

```dockerfile
```

-	Layers:
	-	`sha256:207767c47f99e2d1e1fedd52ce5576598e2145c2fedbd08d52ebcb17283299be`  
		Last Modified: Mon, 29 Jun 2026 20:10:17 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cab7e89c5c123fa2c3080f70c5b47f612c9dc4ac52dc4323fbb3a595c57d7e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6136ec41f85090255a3129de60d735886601c26b2dff3bb5ae840dcfe8972d4b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:59 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:59 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c7f4ed7c5caaf7674fe731cc4314250f15b64d928d938c120113fda642ab9e35`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.1 MB (6055262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54c6d444001ace11b4843342fbb1034885520461c7f6927b617ae9ceec4f2be`  
		Last Modified: Mon, 29 Jun 2026 20:10:03 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:21a6ec729bb63eeb5fd248400b0794cea72020b49014664c9ea8f69873926b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b8f27c27fd4485ac0c2fb9fbd5f577f624409582d839d08b012e5a8980744`

```dockerfile
```

-	Layers:
	-	`sha256:359f4232c60d44b72e23371b39eef2f62ada8b687692b2f6f30998f4754f5cd3`  
		Last Modified: Mon, 29 Jun 2026 20:10:03 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:dffd7ab5566215b39ecc27f4cfbcbec3c87c5fc4d32314065b27fd2f8ab7be7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6114182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac585563eab840d4c0a5e821db019f88a9ffed79a5b5ac27087e72ae35f1674`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68d08cefc115ab2d0ba836794a2aafdbd770ca3b82386eaca56b76eface4067a`  
		Last Modified: Mon, 29 Jun 2026 15:45:25 GMT  
		Size: 6.1 MB (6113673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44bd89ff0f6f728c9f3bc4b6f7be421abaa6e18d57cfc1df853cbe8892117a2`  
		Last Modified: Mon, 29 Jun 2026 19:12:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:507a6e760ac10e306655b5e454edf3ada3f99dc7a91c5f550316e528a7eb2435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace002f95a4f8bad573dd00622c3969d09ed698044207e366057ba33a9a84a5f`

```dockerfile
```

-	Layers:
	-	`sha256:4caf767452a66fa4931c741b42734d256bf6283f3a6a1dd604cfba793beb3aa3`  
		Last Modified: Mon, 29 Jun 2026 19:12:53 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; s390x

```console
$ docker pull nats@sha256:b5f2090a2865bc73183bdbbd5c2db2d4a5e90ab9902682414eee67678f44290e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6507115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081b3d096315958b9213985797ab5c0d1d1f51a9c134de884bdaddeafc215ec5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:23 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:23 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee8c267e3cc1a37bddcdb99b2da7bdd61a07738138488ac8641bc09f0cb7dc28`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.5 MB (6506606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3296f5cd680ca40417700ab16719d01bec8116be5da79289dd9c07b418c26d`  
		Last Modified: Mon, 29 Jun 2026 19:18:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:29663b73d5d3b96d00fbcad47681317129a61e699cc8a6a1b4c60f6b3773993e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8327c934690bae04254b49b552f8448751bd0bcc4abada12f8c086c470592bfc`

```dockerfile
```

-	Layers:
	-	`sha256:2e4c1745430ed822c5b545dbfce9175f49597264d12d3dc7bcd1aa56762e9a7f`  
		Last Modified: Mon, 29 Jun 2026 19:18:32 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-nanoserver`

```console
$ docker pull nats@sha256:71e43abcdbeb67a7181b118980fdab52782e3504de092855dc68d3095b7c6f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:5ecdfc23d4535a0aa4e23ea67d7f08e7100998b49c3dd1e63447b937700d7fbd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130850622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a629255666593ccb84568e18360988f19cf474b041607eab7de75faef30e045`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:14:23 GMT
RUN cmd /S /C #(nop) COPY file:d8af06503cfb328e70ba402a862262e409f0fc6efb978ecfbf29b4bf28c77da7 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:14:24 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:14:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:14:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:14:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f25f32e4beeeac81e5d4a8bac558446351e6d2f47c6c7236375f0595f8891a`  
		Last Modified: Mon, 29 Jun 2026 20:14:35 GMT  
		Size: 6.8 MB (6847146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a9bbbb700b4293074cd53c5f61f55df17ea3fe16126c4be3467ef619f37508`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee53ab55fd1943eb961de73595979a4ab2a3421568fbcea2f32471235ca5cc62`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b542ff1d76894ae7dadda2d201149301d63e9293d0c72eebb7b455325a22958`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517956deb7c51ec9602dd378c58b84756fcd2a8c7bbe9e2f50079414d869269d`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:71e43abcdbeb67a7181b118980fdab52782e3504de092855dc68d3095b7c6f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:5ecdfc23d4535a0aa4e23ea67d7f08e7100998b49c3dd1e63447b937700d7fbd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130850622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a629255666593ccb84568e18360988f19cf474b041607eab7de75faef30e045`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:14:23 GMT
RUN cmd /S /C #(nop) COPY file:d8af06503cfb328e70ba402a862262e409f0fc6efb978ecfbf29b4bf28c77da7 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:14:24 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:14:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:14:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:14:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f25f32e4beeeac81e5d4a8bac558446351e6d2f47c6c7236375f0595f8891a`  
		Last Modified: Mon, 29 Jun 2026 20:14:35 GMT  
		Size: 6.8 MB (6847146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a9bbbb700b4293074cd53c5f61f55df17ea3fe16126c4be3467ef619f37508`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee53ab55fd1943eb961de73595979a4ab2a3421568fbcea2f32471235ca5cc62`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b542ff1d76894ae7dadda2d201149301d63e9293d0c72eebb7b455325a22958`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517956deb7c51ec9602dd378c58b84756fcd2a8c7bbe9e2f50079414d869269d`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-scratch`

```console
$ docker pull nats@sha256:d36030092fd6372ff8bd774b87cd5eee71245f48eb8dca5d46b52a88870d9852
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
$ docker pull nats@sha256:7150f4fdf587569abab9253aa349f72d871da06c77d36aac4436baab884f8c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6658478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6abe773e0ca7e8a35d9a950781562f2e0e465852116c0c49f2de69d6afba56`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:14:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:14:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:14:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:14:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:14:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:14:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:674ddc4edf02c32fd9e0c399e4ce2550d462d0349f360d1e401935b1cc4552a3`  
		Last Modified: Mon, 29 Jun 2026 15:45:26 GMT  
		Size: 6.7 MB (6657969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5702d3684f758185c73e87190842fd53cf65ff30cd7f72a65f65928e90fd72`  
		Last Modified: Mon, 29 Jun 2026 19:14:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:740aed9cbb77fa0feb9593a11b3ef7d80b0326393e62c8bdd29fb28f8deae33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b929051330e300f3043167fc391e5a658f9be6b99625f14821f9e9168a8e6a1`

```dockerfile
```

-	Layers:
	-	`sha256:15be1d8687e3ccb288b2395ac350e965c7b7866d8520bd18a41480f378b731c2`  
		Last Modified: Mon, 29 Jun 2026 19:14:05 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:65f623b6cde3c78df0b0d142ddc6e3e3bd1d9501422375bf621c8ab4a1955ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6398008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a728c107fe662f7111598a56d71ae7c36f4f5a4dd5d1f3b1b4a18bf937df0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:14 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9d8b42e91101f55d0b914352f42379d187b356167e68b6a4d7e248306781093`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.4 MB (6397501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d4cfe960fa26c031af0940ca78ea32b86745fc09a5196c72ee268c481ea651`  
		Last Modified: Mon, 29 Jun 2026 20:10:19 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:270e75e31932b739863421ce378d21bc9b4cbc65319749a56e84db12b75b06db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f84dc1cf6dac3435e77c51283d0504b385c0706684a17a6e1834692e0e300e9`

```dockerfile
```

-	Layers:
	-	`sha256:183c92f9da3d80b68ad84ea10e28ffa86aa9a426aa89e1ee50a75446473bdd53`  
		Last Modified: Mon, 29 Jun 2026 20:10:19 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:965e0f30952fe53c0edbbf51907861203a344a9f436d2f16e44ec62bbc6bc346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6389204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9954dc82025ebe69fb6051eba4e8b56422339f0c76b2978d73e05e4e95f4b686`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:13 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f51f3ae5a0e9a233d660597cb0991d0e4eda1b8d6081f2ebf7b11bf49726cbb`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.4 MB (6388696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064965fad9d634082e200408edb6c3cfd405a94c5e956a0589886e52ab1e280e`  
		Last Modified: Mon, 29 Jun 2026 20:10:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:371542e6b03232abc94eb181db393c6435a837da512cce3804798309c30bdd0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ea3056abc5f4e4d1b686c3750009080f9d259771aab353ae3dc28221d91b3`

```dockerfile
```

-	Layers:
	-	`sha256:207767c47f99e2d1e1fedd52ce5576598e2145c2fedbd08d52ebcb17283299be`  
		Last Modified: Mon, 29 Jun 2026 20:10:17 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cab7e89c5c123fa2c3080f70c5b47f612c9dc4ac52dc4323fbb3a595c57d7e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6136ec41f85090255a3129de60d735886601c26b2dff3bb5ae840dcfe8972d4b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:59 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:59 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c7f4ed7c5caaf7674fe731cc4314250f15b64d928d938c120113fda642ab9e35`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.1 MB (6055262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54c6d444001ace11b4843342fbb1034885520461c7f6927b617ae9ceec4f2be`  
		Last Modified: Mon, 29 Jun 2026 20:10:03 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:21a6ec729bb63eeb5fd248400b0794cea72020b49014664c9ea8f69873926b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b8f27c27fd4485ac0c2fb9fbd5f577f624409582d839d08b012e5a8980744`

```dockerfile
```

-	Layers:
	-	`sha256:359f4232c60d44b72e23371b39eef2f62ada8b687692b2f6f30998f4754f5cd3`  
		Last Modified: Mon, 29 Jun 2026 20:10:03 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:dffd7ab5566215b39ecc27f4cfbcbec3c87c5fc4d32314065b27fd2f8ab7be7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6114182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac585563eab840d4c0a5e821db019f88a9ffed79a5b5ac27087e72ae35f1674`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68d08cefc115ab2d0ba836794a2aafdbd770ca3b82386eaca56b76eface4067a`  
		Last Modified: Mon, 29 Jun 2026 15:45:25 GMT  
		Size: 6.1 MB (6113673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44bd89ff0f6f728c9f3bc4b6f7be421abaa6e18d57cfc1df853cbe8892117a2`  
		Last Modified: Mon, 29 Jun 2026 19:12:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:507a6e760ac10e306655b5e454edf3ada3f99dc7a91c5f550316e528a7eb2435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace002f95a4f8bad573dd00622c3969d09ed698044207e366057ba33a9a84a5f`

```dockerfile
```

-	Layers:
	-	`sha256:4caf767452a66fa4931c741b42734d256bf6283f3a6a1dd604cfba793beb3aa3`  
		Last Modified: Mon, 29 Jun 2026 19:12:53 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; s390x

```console
$ docker pull nats@sha256:b5f2090a2865bc73183bdbbd5c2db2d4a5e90ab9902682414eee67678f44290e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6507115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081b3d096315958b9213985797ab5c0d1d1f51a9c134de884bdaddeafc215ec5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:23 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:23 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee8c267e3cc1a37bddcdb99b2da7bdd61a07738138488ac8641bc09f0cb7dc28`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.5 MB (6506606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3296f5cd680ca40417700ab16719d01bec8116be5da79289dd9c07b418c26d`  
		Last Modified: Mon, 29 Jun 2026 19:18:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:29663b73d5d3b96d00fbcad47681317129a61e699cc8a6a1b4c60f6b3773993e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8327c934690bae04254b49b552f8448751bd0bcc4abada12f8c086c470592bfc`

```dockerfile
```

-	Layers:
	-	`sha256:2e4c1745430ed822c5b545dbfce9175f49597264d12d3dc7bcd1aa56762e9a7f`  
		Last Modified: Mon, 29 Jun 2026 19:18:32 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-windowsservercore`

```console
$ docker pull nats@sha256:219eda2da2aaeaaf912b5fac6df5bc2fa546c80546af9cf24298b7d57914d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:604c31d88ae285f9ec90722d08fdad90c4330e77566c23cca02f2140f9606b3e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2139846230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cb2b5e0f13b10edb1ec4b88255e5081ca32adb4272405eaa62694d6fe72926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 29 Jun 2026 19:19:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Jun 2026 19:19:34 GMT
ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 19:19:36 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:19:38 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:19:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.12/nats-server-v2.12.12-windows-amd64.zip
# Mon, 29 Jun 2026 19:19:41 GMT
ENV NATS_SERVER_SHASUM=66e2ab6250083794321905e1f79db4f4ea53465d84ba0760e9b00d022133050e
# Mon, 29 Jun 2026 19:20:48 GMT
RUN Set-PSDebug -Trace 2
# Mon, 29 Jun 2026 19:21:19 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 29 Jun 2026 19:21:20 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 19:21:21 GMT
EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 19:21:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 19:21:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f16a108e9d2bc33f0fca3c6297f4dde89e1012565ec5e6c8f73be682780439`  
		Last Modified: Mon, 29 Jun 2026 19:21:31 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b1177876813fcaab7e5a78eafe360842b9e21ec4f386a30157a38ba5742a9c`  
		Last Modified: Mon, 29 Jun 2026 19:21:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deec645e54e5f448eaa23276e6a129ad75071ddae6caa11003fdb5f28b4e5273`  
		Last Modified: Mon, 29 Jun 2026 19:21:31 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7baba77b0b911dac427ec025b5ae24f0ff40dded40b44d2a4d01c637134f2d`  
		Last Modified: Mon, 29 Jun 2026 19:21:29 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54553d8793c8e91455ebc378ebd9c1d5004521e9a74d79a89ce5d758c507c4be`  
		Last Modified: Mon, 29 Jun 2026 19:21:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3009c0e4ff927dffa0ecd3202aaf1cecd51781deda11e7a92e8cc79e450f09`  
		Last Modified: Mon, 29 Jun 2026 19:21:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93cfa08438f07b9987856fb41a344e9ad7338b8bddcebad69d2e6af361f4351`  
		Last Modified: Mon, 29 Jun 2026 19:21:30 GMT  
		Size: 497.4 KB (497435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b29917a60e39eb7c14c9ada61401f9b5e9591c9b7dbd0cd10e494516126de9`  
		Last Modified: Mon, 29 Jun 2026 19:21:32 GMT  
		Size: 7.2 MB (7209661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de7971acafe042855b721098603831ecafe3a8a4d4db756df118142a6da5233`  
		Last Modified: Mon, 29 Jun 2026 19:21:27 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15cdc907f166db6e75f6e881466aa143f728bb6f4b29d78e2c1b180563c7a30`  
		Last Modified: Mon, 29 Jun 2026 19:21:28 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b328cd9297132c05a7f02b94c4eaf6789a52806787eaf8f6da6bb00c2eb92b2`  
		Last Modified: Mon, 29 Jun 2026 19:21:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e478cda9ffcf7171ed42b072890941e48880a8f922a7aad5fcb85f32335cb43e`  
		Last Modified: Mon, 29 Jun 2026 19:21:27 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:219eda2da2aaeaaf912b5fac6df5bc2fa546c80546af9cf24298b7d57914d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:604c31d88ae285f9ec90722d08fdad90c4330e77566c23cca02f2140f9606b3e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2139846230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cb2b5e0f13b10edb1ec4b88255e5081ca32adb4272405eaa62694d6fe72926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 29 Jun 2026 19:19:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Jun 2026 19:19:34 GMT
ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 19:19:36 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:19:38 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:19:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.12/nats-server-v2.12.12-windows-amd64.zip
# Mon, 29 Jun 2026 19:19:41 GMT
ENV NATS_SERVER_SHASUM=66e2ab6250083794321905e1f79db4f4ea53465d84ba0760e9b00d022133050e
# Mon, 29 Jun 2026 19:20:48 GMT
RUN Set-PSDebug -Trace 2
# Mon, 29 Jun 2026 19:21:19 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 29 Jun 2026 19:21:20 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 19:21:21 GMT
EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 19:21:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 19:21:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f16a108e9d2bc33f0fca3c6297f4dde89e1012565ec5e6c8f73be682780439`  
		Last Modified: Mon, 29 Jun 2026 19:21:31 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b1177876813fcaab7e5a78eafe360842b9e21ec4f386a30157a38ba5742a9c`  
		Last Modified: Mon, 29 Jun 2026 19:21:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deec645e54e5f448eaa23276e6a129ad75071ddae6caa11003fdb5f28b4e5273`  
		Last Modified: Mon, 29 Jun 2026 19:21:31 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7baba77b0b911dac427ec025b5ae24f0ff40dded40b44d2a4d01c637134f2d`  
		Last Modified: Mon, 29 Jun 2026 19:21:29 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54553d8793c8e91455ebc378ebd9c1d5004521e9a74d79a89ce5d758c507c4be`  
		Last Modified: Mon, 29 Jun 2026 19:21:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3009c0e4ff927dffa0ecd3202aaf1cecd51781deda11e7a92e8cc79e450f09`  
		Last Modified: Mon, 29 Jun 2026 19:21:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93cfa08438f07b9987856fb41a344e9ad7338b8bddcebad69d2e6af361f4351`  
		Last Modified: Mon, 29 Jun 2026 19:21:30 GMT  
		Size: 497.4 KB (497435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b29917a60e39eb7c14c9ada61401f9b5e9591c9b7dbd0cd10e494516126de9`  
		Last Modified: Mon, 29 Jun 2026 19:21:32 GMT  
		Size: 7.2 MB (7209661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de7971acafe042855b721098603831ecafe3a8a4d4db756df118142a6da5233`  
		Last Modified: Mon, 29 Jun 2026 19:21:27 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15cdc907f166db6e75f6e881466aa143f728bb6f4b29d78e2c1b180563c7a30`  
		Last Modified: Mon, 29 Jun 2026 19:21:28 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b328cd9297132c05a7f02b94c4eaf6789a52806787eaf8f6da6bb00c2eb92b2`  
		Last Modified: Mon, 29 Jun 2026 19:21:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e478cda9ffcf7171ed42b072890941e48880a8f922a7aad5fcb85f32335cb43e`  
		Last Modified: Mon, 29 Jun 2026 19:21:27 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.12`

```console
$ docker pull nats@sha256:df6c75f572c2b0f74dfa062505453192d899149701f198981f393ebb6588b9e1
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
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12.12` - linux; amd64

```console
$ docker pull nats@sha256:7150f4fdf587569abab9253aa349f72d871da06c77d36aac4436baab884f8c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6658478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6abe773e0ca7e8a35d9a950781562f2e0e465852116c0c49f2de69d6afba56`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:14:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:14:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:14:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:14:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:14:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:14:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:674ddc4edf02c32fd9e0c399e4ce2550d462d0349f360d1e401935b1cc4552a3`  
		Last Modified: Mon, 29 Jun 2026 15:45:26 GMT  
		Size: 6.7 MB (6657969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5702d3684f758185c73e87190842fd53cf65ff30cd7f72a65f65928e90fd72`  
		Last Modified: Mon, 29 Jun 2026 19:14:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12` - unknown; unknown

```console
$ docker pull nats@sha256:740aed9cbb77fa0feb9593a11b3ef7d80b0326393e62c8bdd29fb28f8deae33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b929051330e300f3043167fc391e5a658f9be6b99625f14821f9e9168a8e6a1`

```dockerfile
```

-	Layers:
	-	`sha256:15be1d8687e3ccb288b2395ac350e965c7b7866d8520bd18a41480f378b731c2`  
		Last Modified: Mon, 29 Jun 2026 19:14:05 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:65f623b6cde3c78df0b0d142ddc6e3e3bd1d9501422375bf621c8ab4a1955ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6398008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a728c107fe662f7111598a56d71ae7c36f4f5a4dd5d1f3b1b4a18bf937df0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:14 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9d8b42e91101f55d0b914352f42379d187b356167e68b6a4d7e248306781093`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.4 MB (6397501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d4cfe960fa26c031af0940ca78ea32b86745fc09a5196c72ee268c481ea651`  
		Last Modified: Mon, 29 Jun 2026 20:10:19 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12` - unknown; unknown

```console
$ docker pull nats@sha256:270e75e31932b739863421ce378d21bc9b4cbc65319749a56e84db12b75b06db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f84dc1cf6dac3435e77c51283d0504b385c0706684a17a6e1834692e0e300e9`

```dockerfile
```

-	Layers:
	-	`sha256:183c92f9da3d80b68ad84ea10e28ffa86aa9a426aa89e1ee50a75446473bdd53`  
		Last Modified: Mon, 29 Jun 2026 20:10:19 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:965e0f30952fe53c0edbbf51907861203a344a9f436d2f16e44ec62bbc6bc346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6389204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9954dc82025ebe69fb6051eba4e8b56422339f0c76b2978d73e05e4e95f4b686`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:13 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f51f3ae5a0e9a233d660597cb0991d0e4eda1b8d6081f2ebf7b11bf49726cbb`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.4 MB (6388696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064965fad9d634082e200408edb6c3cfd405a94c5e956a0589886e52ab1e280e`  
		Last Modified: Mon, 29 Jun 2026 20:10:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12` - unknown; unknown

```console
$ docker pull nats@sha256:371542e6b03232abc94eb181db393c6435a837da512cce3804798309c30bdd0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ea3056abc5f4e4d1b686c3750009080f9d259771aab353ae3dc28221d91b3`

```dockerfile
```

-	Layers:
	-	`sha256:207767c47f99e2d1e1fedd52ce5576598e2145c2fedbd08d52ebcb17283299be`  
		Last Modified: Mon, 29 Jun 2026 20:10:17 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cab7e89c5c123fa2c3080f70c5b47f612c9dc4ac52dc4323fbb3a595c57d7e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6136ec41f85090255a3129de60d735886601c26b2dff3bb5ae840dcfe8972d4b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:59 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:59 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c7f4ed7c5caaf7674fe731cc4314250f15b64d928d938c120113fda642ab9e35`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.1 MB (6055262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54c6d444001ace11b4843342fbb1034885520461c7f6927b617ae9ceec4f2be`  
		Last Modified: Mon, 29 Jun 2026 20:10:03 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12` - unknown; unknown

```console
$ docker pull nats@sha256:21a6ec729bb63eeb5fd248400b0794cea72020b49014664c9ea8f69873926b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b8f27c27fd4485ac0c2fb9fbd5f577f624409582d839d08b012e5a8980744`

```dockerfile
```

-	Layers:
	-	`sha256:359f4232c60d44b72e23371b39eef2f62ada8b687692b2f6f30998f4754f5cd3`  
		Last Modified: Mon, 29 Jun 2026 20:10:03 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12` - linux; ppc64le

```console
$ docker pull nats@sha256:dffd7ab5566215b39ecc27f4cfbcbec3c87c5fc4d32314065b27fd2f8ab7be7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6114182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac585563eab840d4c0a5e821db019f88a9ffed79a5b5ac27087e72ae35f1674`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68d08cefc115ab2d0ba836794a2aafdbd770ca3b82386eaca56b76eface4067a`  
		Last Modified: Mon, 29 Jun 2026 15:45:25 GMT  
		Size: 6.1 MB (6113673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44bd89ff0f6f728c9f3bc4b6f7be421abaa6e18d57cfc1df853cbe8892117a2`  
		Last Modified: Mon, 29 Jun 2026 19:12:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12` - unknown; unknown

```console
$ docker pull nats@sha256:507a6e760ac10e306655b5e454edf3ada3f99dc7a91c5f550316e528a7eb2435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace002f95a4f8bad573dd00622c3969d09ed698044207e366057ba33a9a84a5f`

```dockerfile
```

-	Layers:
	-	`sha256:4caf767452a66fa4931c741b42734d256bf6283f3a6a1dd604cfba793beb3aa3`  
		Last Modified: Mon, 29 Jun 2026 19:12:53 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12` - linux; s390x

```console
$ docker pull nats@sha256:b5f2090a2865bc73183bdbbd5c2db2d4a5e90ab9902682414eee67678f44290e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6507115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081b3d096315958b9213985797ab5c0d1d1f51a9c134de884bdaddeafc215ec5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:23 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:23 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee8c267e3cc1a37bddcdb99b2da7bdd61a07738138488ac8641bc09f0cb7dc28`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.5 MB (6506606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3296f5cd680ca40417700ab16719d01bec8116be5da79289dd9c07b418c26d`  
		Last Modified: Mon, 29 Jun 2026 19:18:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12` - unknown; unknown

```console
$ docker pull nats@sha256:29663b73d5d3b96d00fbcad47681317129a61e699cc8a6a1b4c60f6b3773993e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8327c934690bae04254b49b552f8448751bd0bcc4abada12f8c086c470592bfc`

```dockerfile
```

-	Layers:
	-	`sha256:2e4c1745430ed822c5b545dbfce9175f49597264d12d3dc7bcd1aa56762e9a7f`  
		Last Modified: Mon, 29 Jun 2026 19:18:32 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:5ecdfc23d4535a0aa4e23ea67d7f08e7100998b49c3dd1e63447b937700d7fbd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130850622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a629255666593ccb84568e18360988f19cf474b041607eab7de75faef30e045`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:14:23 GMT
RUN cmd /S /C #(nop) COPY file:d8af06503cfb328e70ba402a862262e409f0fc6efb978ecfbf29b4bf28c77da7 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:14:24 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:14:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:14:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:14:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f25f32e4beeeac81e5d4a8bac558446351e6d2f47c6c7236375f0595f8891a`  
		Last Modified: Mon, 29 Jun 2026 20:14:35 GMT  
		Size: 6.8 MB (6847146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a9bbbb700b4293074cd53c5f61f55df17ea3fe16126c4be3467ef619f37508`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee53ab55fd1943eb961de73595979a4ab2a3421568fbcea2f32471235ca5cc62`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b542ff1d76894ae7dadda2d201149301d63e9293d0c72eebb7b455325a22958`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517956deb7c51ec9602dd378c58b84756fcd2a8c7bbe9e2f50079414d869269d`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.12-alpine`

```console
$ docker pull nats@sha256:2ca98656a279b2d88cfdf2b8c3f0d5d7f3941ae9dc2ab12ebaa92d83e0f4ccdb
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

### `nats:2.12.12-alpine` - linux; amd64

```console
$ docker pull nats@sha256:425d3d24ac3b92b88cda1b153cc72f9535bfd1c0bcdd8f67740d9b22220e30f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4df4dc451af97c3499db640c4a6e0d6d6faa100799fe727d9e7e8be2f85756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f302f59e4314d1878834e19e5b71b17be0ae76d484bf8d2d1d2e13a49e87ffd`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 7.1 MB (7068014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d50079454fd127c8d11556ad65e8ae8d330d9b23fdebfbf84a7a2e1ef81830`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91585d73d765544cfc68e45bf7451cdcc41e98760273b1c14b994ea65a9421ca`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:627fc61f544347aee1241d88a072aaf2f482f3fe6d7dcae343a3386a0f71b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7dfec1367766e5087363e33ace912bc5cecf9d000ff7a9fcfc32e5edd3a827`

```dockerfile
```

-	Layers:
	-	`sha256:d5a9967d703c4696f237199b5172918a071980ff994625807ad12b66209342e7`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:da848228ada3065f9c2a15a503406d61499de6d7fba699cb3817e28f37f7402a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10304206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec13ec03de80b2e6a0934d8b43ae748adebabc51a7a5c46e46b20f578b49155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:13:09 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:13:09 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:13:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:13:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:13:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:13:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d0133a34d5e99791b0b3206d7eb6a9217a98a390b98e62774a8f53f4bda8c4`  
		Last Modified: Mon, 29 Jun 2026 19:13:14 GMT  
		Size: 6.8 MB (6808434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8527ed2a249d0102a50cb5daf85524e8a609d2dbc9cf393b619dd753e6cdda4`  
		Last Modified: Mon, 29 Jun 2026 19:13:13 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37a8bf70ff4688a4da1c7d8e4773643b11453e39faee3f9a3a2a5d114af4088`  
		Last Modified: Mon, 29 Jun 2026 19:13:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:402db16d9854509328c72bc3f951aa99d3247261cd154385a6603dc821063f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e2d38edf0c20d359c7a16600c7ca141f330898742c9eefc3bde4c3405faf2e`

```dockerfile
```

-	Layers:
	-	`sha256:b501f81ba3b78b726cf71f13fe9f1b0abe45339eb3815630fbbc8b320275bbf2`  
		Last Modified: Mon, 29 Jun 2026 19:13:13 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bdb7a59f6844170dc8334f1a35f8877fb79498789e8bece8335edd8570d70a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10011404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac147b9241325ef59b2f84a81dd728295ccc3de6ee18a853ba20326f55a6a7d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:34 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:12:34 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:12:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:34 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03da412883a51e21464226481f5dc565bc91499890464f6c8b947b8bb4f3224`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 6.8 MB (6800823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32017da75c3a70cb844f8cb7b3a37cd94f78537d3e2cd628483d23d537a2b9b8`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3bfb6f5d6546a6d9549ad1a5195221e2753c0f62fcc02026b3f4aca9944dde`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a80b31cb272cdafe50b728781f58bb9e8f82058635d34dab166a1bb7943ab003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd3bc4d2dd9978a3547b6749a373898c58d319e3c2e1322b10454bf3f6dd41b`

```dockerfile
```

-	Layers:
	-	`sha256:3a3d19fde6df2d85168077489af805b3edb561dff5c4de446506516319464998`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e7a28a0c0300aa1a737b1fd8c567f6da0fe96d970c3ee97dedaf475bc065e2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10589316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a473d4229d429ef3f28373acf98500d4f5fa8a054c1438e691c71f68c49977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:27 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:12:27 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:12:27 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:27 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:27 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159748456c3959ce6919c808af480b38f00972cf9fc9db5caaf0d3ccdf33e9c5`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 6.5 MB (6467860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a71adc900265c0969d3baefd35719826032c2917baf34e23acb556bd849192`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef83f1bdacd18e095d1825b1e6534d4c8290d91e67047fbd6b726c9c3a2a4cb0`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:8af248235d9832c27c4088dfd29818c8474c47b99743d0ff62a2037c580bcc56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e2ff5e55bab6e49a25ff808dd57a35732350849f8f38e7fa435b6472dc2b00`

```dockerfile
```

-	Layers:
	-	`sha256:0e95cccbe78acbcfc3d29b69f3a4ca240123e634f7b76d89f717ceb6c6d791c6`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:79ab02351c08527aa75a4f0dcf0bcabf8313986a36b2974702bd8fb4980b9898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10248160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd4063f85a19f911d9ce871702a6b298f8a8f7bdb6cdd70bf271565cbd0383e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e590177a1f3832404927d73f703cd9b6de1bc6aa1c0a4071f73e62d61d6ff4d`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.5 MB (6527958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ea17abc7bdf67861515d4ae06c070fb7748d0cbec44453db6d05495a7af96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2a7741b38aa0865f53f2bc0c633a5727a70c07676d5f11582cbba4e5271703`

```dockerfile
```

-	Layers:
	-	`sha256:7c420f60382849b143e37e5624177f950ae9e5734cb82ee3cfc5487a594894d2`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:e416ac70e75c57154afc11270f4b79b26064bec8c6f45b33cc149de9369e4c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10555129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8f5c696629dedfa3f5d4827265a0ce1a254b61e328c4016a252e05fd6cd5d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2bc2f93033c9b7f596631cea725b6923dfa8204a1fbd0cad289cfb66ad686`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 6.9 MB (6917070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3319d5c969f4b3502a099f99e8b9d1c3bac616a3bddc3b10057dc687980fd7b1`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6498ad1fc5102f83402c9c078f53d9db7682b83a100cdf63606f711bce0f5d43`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9334e0829fc5846fd017385aec07371d829e8066ddd077be9208d80db65f9383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4430ea02178620fe9c9abc8a148ece6e6ef63f14d072c1c0f4852d54c98d2aa9`

```dockerfile
```

-	Layers:
	-	`sha256:f2d6fd7f8df0496ec5b02bad43bdccebdd9d1165cffbb23b9526bc4f3e6dbbdf`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.12-alpine3.22`

```console
$ docker pull nats@sha256:2ca98656a279b2d88cfdf2b8c3f0d5d7f3941ae9dc2ab12ebaa92d83e0f4ccdb
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

### `nats:2.12.12-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:425d3d24ac3b92b88cda1b153cc72f9535bfd1c0bcdd8f67740d9b22220e30f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4df4dc451af97c3499db640c4a6e0d6d6faa100799fe727d9e7e8be2f85756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f302f59e4314d1878834e19e5b71b17be0ae76d484bf8d2d1d2e13a49e87ffd`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 7.1 MB (7068014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d50079454fd127c8d11556ad65e8ae8d330d9b23fdebfbf84a7a2e1ef81830`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91585d73d765544cfc68e45bf7451cdcc41e98760273b1c14b994ea65a9421ca`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:627fc61f544347aee1241d88a072aaf2f482f3fe6d7dcae343a3386a0f71b382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7dfec1367766e5087363e33ace912bc5cecf9d000ff7a9fcfc32e5edd3a827`

```dockerfile
```

-	Layers:
	-	`sha256:d5a9967d703c4696f237199b5172918a071980ff994625807ad12b66209342e7`  
		Last Modified: Mon, 29 Jun 2026 19:11:45 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:da848228ada3065f9c2a15a503406d61499de6d7fba699cb3817e28f37f7402a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10304206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec13ec03de80b2e6a0934d8b43ae748adebabc51a7a5c46e46b20f578b49155`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:13:09 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:13:09 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:13:09 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:13:09 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:13:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:13:09 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d0133a34d5e99791b0b3206d7eb6a9217a98a390b98e62774a8f53f4bda8c4`  
		Last Modified: Mon, 29 Jun 2026 19:13:14 GMT  
		Size: 6.8 MB (6808434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8527ed2a249d0102a50cb5daf85524e8a609d2dbc9cf393b619dd753e6cdda4`  
		Last Modified: Mon, 29 Jun 2026 19:13:13 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37a8bf70ff4688a4da1c7d8e4773643b11453e39faee3f9a3a2a5d114af4088`  
		Last Modified: Mon, 29 Jun 2026 19:13:13 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:402db16d9854509328c72bc3f951aa99d3247261cd154385a6603dc821063f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e2d38edf0c20d359c7a16600c7ca141f330898742c9eefc3bde4c3405faf2e`

```dockerfile
```

-	Layers:
	-	`sha256:b501f81ba3b78b726cf71f13fe9f1b0abe45339eb3815630fbbc8b320275bbf2`  
		Last Modified: Mon, 29 Jun 2026 19:13:13 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:1bdb7a59f6844170dc8334f1a35f8877fb79498789e8bece8335edd8570d70a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10011404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac147b9241325ef59b2f84a81dd728295ccc3de6ee18a853ba20326f55a6a7d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:34 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:12:34 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:12:34 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:34 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03da412883a51e21464226481f5dc565bc91499890464f6c8b947b8bb4f3224`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 6.8 MB (6800823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32017da75c3a70cb844f8cb7b3a37cd94f78537d3e2cd628483d23d537a2b9b8`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3bfb6f5d6546a6d9549ad1a5195221e2753c0f62fcc02026b3f4aca9944dde`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a80b31cb272cdafe50b728781f58bb9e8f82058635d34dab166a1bb7943ab003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd3bc4d2dd9978a3547b6749a373898c58d319e3c2e1322b10454bf3f6dd41b`

```dockerfile
```

-	Layers:
	-	`sha256:3a3d19fde6df2d85168077489af805b3edb561dff5c4de446506516319464998`  
		Last Modified: Mon, 29 Jun 2026 19:12:39 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e7a28a0c0300aa1a737b1fd8c567f6da0fe96d970c3ee97dedaf475bc065e2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10589316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a473d4229d429ef3f28373acf98500d4f5fa8a054c1438e691c71f68c49977`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:27 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:12:27 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:12:27 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:27 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:27 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:27 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159748456c3959ce6919c808af480b38f00972cf9fc9db5caaf0d3ccdf33e9c5`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 6.5 MB (6467860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a71adc900265c0969d3baefd35719826032c2917baf34e23acb556bd849192`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef83f1bdacd18e095d1825b1e6534d4c8290d91e67047fbd6b726c9c3a2a4cb0`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:8af248235d9832c27c4088dfd29818c8474c47b99743d0ff62a2037c580bcc56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e2ff5e55bab6e49a25ff808dd57a35732350849f8f38e7fa435b6472dc2b00`

```dockerfile
```

-	Layers:
	-	`sha256:0e95cccbe78acbcfc3d29b69f3a4ca240123e634f7b76d89f717ceb6c6d791c6`  
		Last Modified: Mon, 29 Jun 2026 19:12:32 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:79ab02351c08527aa75a4f0dcf0bcabf8313986a36b2974702bd8fb4980b9898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10248160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd4063f85a19f911d9ce871702a6b298f8a8f7bdb6cdd70bf271565cbd0383e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e590177a1f3832404927d73f703cd9b6de1bc6aa1c0a4071f73e62d61d6ff4d`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.5 MB (6527958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ea17abc7bdf67861515d4ae06c070fb7748d0cbec44453db6d05495a7af96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2a7741b38aa0865f53f2bc0c633a5727a70c07676d5f11582cbba4e5271703`

```dockerfile
```

-	Layers:
	-	`sha256:7c420f60382849b143e37e5624177f950ae9e5734cb82ee3cfc5487a594894d2`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:e416ac70e75c57154afc11270f4b79b26064bec8c6f45b33cc149de9369e4c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10555129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8f5c696629dedfa3f5d4827265a0ce1a254b61e328c4016a252e05fd6cd5d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:11:47 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='d28651f6690a47f6115562f43570896aa3754aff7421dba0a9c11e99263a382e' ;;     armhf) natsArch='arm6'; sha256='3af51b2f7cd5aa7fe86f805ebcda6a136cdfd0ee2d9e39a1951663e51b309f70' ;;     armv7) natsArch='arm7'; sha256='ade3527a9c81befae6b6e6d849ca23d9e8fa7e95b597a41f96ad0b74dc751ea1' ;;     x86_64) natsArch='amd64'; sha256='0ade8c59f966a37b9898e5f9ae408ad47f64e529423d3d07330848f4c3bb9300' ;;     x86) natsArch='386'; sha256='3e68f7fbd79a6febea21ff54baba19d4c51444ee89ffba779b6d86adf4ae6f79' ;;     s390x) natsArch='s390x'; sha256='63104abaff9fce8ec9a4ff689da14e1c850b8e039cf4254b5be35da588d01ad9' ;;     ppc64le) natsArch='ppc64le'; sha256='b290015331fa69d477acdd6dda18bacecc0a63ec90b51511f664902c4cc72f31' ;;     loong64) natsArch='loong64'; sha256='35fd6f8b0904ecdbce217f7e23a21c5f1eb1b8e4123ddeac803c570295213acd' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2bc2f93033c9b7f596631cea725b6923dfa8204a1fbd0cad289cfb66ad686`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 6.9 MB (6917070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3319d5c969f4b3502a099f99e8b9d1c3bac616a3bddc3b10057dc687980fd7b1`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6498ad1fc5102f83402c9c078f53d9db7682b83a100cdf63606f711bce0f5d43`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9334e0829fc5846fd017385aec07371d829e8066ddd077be9208d80db65f9383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4430ea02178620fe9c9abc8a148ece6e6ef63f14d072c1c0f4852d54c98d2aa9`

```dockerfile
```

-	Layers:
	-	`sha256:f2d6fd7f8df0496ec5b02bad43bdccebdd9d1165cffbb23b9526bc4f3e6dbbdf`  
		Last Modified: Mon, 29 Jun 2026 19:11:57 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.12-linux`

```console
$ docker pull nats@sha256:d36030092fd6372ff8bd774b87cd5eee71245f48eb8dca5d46b52a88870d9852
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

### `nats:2.12.12-linux` - linux; amd64

```console
$ docker pull nats@sha256:7150f4fdf587569abab9253aa349f72d871da06c77d36aac4436baab884f8c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6658478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6abe773e0ca7e8a35d9a950781562f2e0e465852116c0c49f2de69d6afba56`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:14:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:14:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:14:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:14:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:14:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:14:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:674ddc4edf02c32fd9e0c399e4ce2550d462d0349f360d1e401935b1cc4552a3`  
		Last Modified: Mon, 29 Jun 2026 15:45:26 GMT  
		Size: 6.7 MB (6657969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5702d3684f758185c73e87190842fd53cf65ff30cd7f72a65f65928e90fd72`  
		Last Modified: Mon, 29 Jun 2026 19:14:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:740aed9cbb77fa0feb9593a11b3ef7d80b0326393e62c8bdd29fb28f8deae33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b929051330e300f3043167fc391e5a658f9be6b99625f14821f9e9168a8e6a1`

```dockerfile
```

-	Layers:
	-	`sha256:15be1d8687e3ccb288b2395ac350e965c7b7866d8520bd18a41480f378b731c2`  
		Last Modified: Mon, 29 Jun 2026 19:14:05 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:65f623b6cde3c78df0b0d142ddc6e3e3bd1d9501422375bf621c8ab4a1955ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6398008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a728c107fe662f7111598a56d71ae7c36f4f5a4dd5d1f3b1b4a18bf937df0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:14 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9d8b42e91101f55d0b914352f42379d187b356167e68b6a4d7e248306781093`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.4 MB (6397501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d4cfe960fa26c031af0940ca78ea32b86745fc09a5196c72ee268c481ea651`  
		Last Modified: Mon, 29 Jun 2026 20:10:19 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:270e75e31932b739863421ce378d21bc9b4cbc65319749a56e84db12b75b06db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f84dc1cf6dac3435e77c51283d0504b385c0706684a17a6e1834692e0e300e9`

```dockerfile
```

-	Layers:
	-	`sha256:183c92f9da3d80b68ad84ea10e28ffa86aa9a426aa89e1ee50a75446473bdd53`  
		Last Modified: Mon, 29 Jun 2026 20:10:19 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:965e0f30952fe53c0edbbf51907861203a344a9f436d2f16e44ec62bbc6bc346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6389204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9954dc82025ebe69fb6051eba4e8b56422339f0c76b2978d73e05e4e95f4b686`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:13 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f51f3ae5a0e9a233d660597cb0991d0e4eda1b8d6081f2ebf7b11bf49726cbb`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.4 MB (6388696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064965fad9d634082e200408edb6c3cfd405a94c5e956a0589886e52ab1e280e`  
		Last Modified: Mon, 29 Jun 2026 20:10:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:371542e6b03232abc94eb181db393c6435a837da512cce3804798309c30bdd0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ea3056abc5f4e4d1b686c3750009080f9d259771aab353ae3dc28221d91b3`

```dockerfile
```

-	Layers:
	-	`sha256:207767c47f99e2d1e1fedd52ce5576598e2145c2fedbd08d52ebcb17283299be`  
		Last Modified: Mon, 29 Jun 2026 20:10:17 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cab7e89c5c123fa2c3080f70c5b47f612c9dc4ac52dc4323fbb3a595c57d7e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6136ec41f85090255a3129de60d735886601c26b2dff3bb5ae840dcfe8972d4b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:59 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:59 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c7f4ed7c5caaf7674fe731cc4314250f15b64d928d938c120113fda642ab9e35`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.1 MB (6055262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54c6d444001ace11b4843342fbb1034885520461c7f6927b617ae9ceec4f2be`  
		Last Modified: Mon, 29 Jun 2026 20:10:03 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:21a6ec729bb63eeb5fd248400b0794cea72020b49014664c9ea8f69873926b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b8f27c27fd4485ac0c2fb9fbd5f577f624409582d839d08b012e5a8980744`

```dockerfile
```

-	Layers:
	-	`sha256:359f4232c60d44b72e23371b39eef2f62ada8b687692b2f6f30998f4754f5cd3`  
		Last Modified: Mon, 29 Jun 2026 20:10:03 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:dffd7ab5566215b39ecc27f4cfbcbec3c87c5fc4d32314065b27fd2f8ab7be7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6114182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac585563eab840d4c0a5e821db019f88a9ffed79a5b5ac27087e72ae35f1674`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68d08cefc115ab2d0ba836794a2aafdbd770ca3b82386eaca56b76eface4067a`  
		Last Modified: Mon, 29 Jun 2026 15:45:25 GMT  
		Size: 6.1 MB (6113673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44bd89ff0f6f728c9f3bc4b6f7be421abaa6e18d57cfc1df853cbe8892117a2`  
		Last Modified: Mon, 29 Jun 2026 19:12:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:507a6e760ac10e306655b5e454edf3ada3f99dc7a91c5f550316e528a7eb2435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace002f95a4f8bad573dd00622c3969d09ed698044207e366057ba33a9a84a5f`

```dockerfile
```

-	Layers:
	-	`sha256:4caf767452a66fa4931c741b42734d256bf6283f3a6a1dd604cfba793beb3aa3`  
		Last Modified: Mon, 29 Jun 2026 19:12:53 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-linux` - linux; s390x

```console
$ docker pull nats@sha256:b5f2090a2865bc73183bdbbd5c2db2d4a5e90ab9902682414eee67678f44290e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6507115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081b3d096315958b9213985797ab5c0d1d1f51a9c134de884bdaddeafc215ec5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:23 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:23 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee8c267e3cc1a37bddcdb99b2da7bdd61a07738138488ac8641bc09f0cb7dc28`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.5 MB (6506606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3296f5cd680ca40417700ab16719d01bec8116be5da79289dd9c07b418c26d`  
		Last Modified: Mon, 29 Jun 2026 19:18:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:29663b73d5d3b96d00fbcad47681317129a61e699cc8a6a1b4c60f6b3773993e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8327c934690bae04254b49b552f8448751bd0bcc4abada12f8c086c470592bfc`

```dockerfile
```

-	Layers:
	-	`sha256:2e4c1745430ed822c5b545dbfce9175f49597264d12d3dc7bcd1aa56762e9a7f`  
		Last Modified: Mon, 29 Jun 2026 19:18:32 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.12-nanoserver`

```console
$ docker pull nats@sha256:71e43abcdbeb67a7181b118980fdab52782e3504de092855dc68d3095b7c6f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12.12-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:5ecdfc23d4535a0aa4e23ea67d7f08e7100998b49c3dd1e63447b937700d7fbd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130850622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a629255666593ccb84568e18360988f19cf474b041607eab7de75faef30e045`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:14:23 GMT
RUN cmd /S /C #(nop) COPY file:d8af06503cfb328e70ba402a862262e409f0fc6efb978ecfbf29b4bf28c77da7 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:14:24 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:14:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:14:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:14:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f25f32e4beeeac81e5d4a8bac558446351e6d2f47c6c7236375f0595f8891a`  
		Last Modified: Mon, 29 Jun 2026 20:14:35 GMT  
		Size: 6.8 MB (6847146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a9bbbb700b4293074cd53c5f61f55df17ea3fe16126c4be3467ef619f37508`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee53ab55fd1943eb961de73595979a4ab2a3421568fbcea2f32471235ca5cc62`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b542ff1d76894ae7dadda2d201149301d63e9293d0c72eebb7b455325a22958`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517956deb7c51ec9602dd378c58b84756fcd2a8c7bbe9e2f50079414d869269d`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.12-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:71e43abcdbeb67a7181b118980fdab52782e3504de092855dc68d3095b7c6f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12.12-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:5ecdfc23d4535a0aa4e23ea67d7f08e7100998b49c3dd1e63447b937700d7fbd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130850622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a629255666593ccb84568e18360988f19cf474b041607eab7de75faef30e045`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:14:23 GMT
RUN cmd /S /C #(nop) COPY file:d8af06503cfb328e70ba402a862262e409f0fc6efb978ecfbf29b4bf28c77da7 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:14:24 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:14:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:14:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:14:26 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f25f32e4beeeac81e5d4a8bac558446351e6d2f47c6c7236375f0595f8891a`  
		Last Modified: Mon, 29 Jun 2026 20:14:35 GMT  
		Size: 6.8 MB (6847146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a9bbbb700b4293074cd53c5f61f55df17ea3fe16126c4be3467ef619f37508`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee53ab55fd1943eb961de73595979a4ab2a3421568fbcea2f32471235ca5cc62`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b542ff1d76894ae7dadda2d201149301d63e9293d0c72eebb7b455325a22958`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517956deb7c51ec9602dd378c58b84756fcd2a8c7bbe9e2f50079414d869269d`  
		Last Modified: Mon, 29 Jun 2026 20:14:30 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.12-scratch`

```console
$ docker pull nats@sha256:d36030092fd6372ff8bd774b87cd5eee71245f48eb8dca5d46b52a88870d9852
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

### `nats:2.12.12-scratch` - linux; amd64

```console
$ docker pull nats@sha256:7150f4fdf587569abab9253aa349f72d871da06c77d36aac4436baab884f8c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6658478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6abe773e0ca7e8a35d9a950781562f2e0e465852116c0c49f2de69d6afba56`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:14:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:14:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:14:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:14:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:14:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:14:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:674ddc4edf02c32fd9e0c399e4ce2550d462d0349f360d1e401935b1cc4552a3`  
		Last Modified: Mon, 29 Jun 2026 15:45:26 GMT  
		Size: 6.7 MB (6657969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5702d3684f758185c73e87190842fd53cf65ff30cd7f72a65f65928e90fd72`  
		Last Modified: Mon, 29 Jun 2026 19:14:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:740aed9cbb77fa0feb9593a11b3ef7d80b0326393e62c8bdd29fb28f8deae33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b929051330e300f3043167fc391e5a658f9be6b99625f14821f9e9168a8e6a1`

```dockerfile
```

-	Layers:
	-	`sha256:15be1d8687e3ccb288b2395ac350e965c7b7866d8520bd18a41480f378b731c2`  
		Last Modified: Mon, 29 Jun 2026 19:14:05 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:65f623b6cde3c78df0b0d142ddc6e3e3bd1d9501422375bf621c8ab4a1955ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6398008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a728c107fe662f7111598a56d71ae7c36f4f5a4dd5d1f3b1b4a18bf937df0c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:14 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:14 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:14 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a9d8b42e91101f55d0b914352f42379d187b356167e68b6a4d7e248306781093`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.4 MB (6397501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d4cfe960fa26c031af0940ca78ea32b86745fc09a5196c72ee268c481ea651`  
		Last Modified: Mon, 29 Jun 2026 20:10:19 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:270e75e31932b739863421ce378d21bc9b4cbc65319749a56e84db12b75b06db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f84dc1cf6dac3435e77c51283d0504b385c0706684a17a6e1834692e0e300e9`

```dockerfile
```

-	Layers:
	-	`sha256:183c92f9da3d80b68ad84ea10e28ffa86aa9a426aa89e1ee50a75446473bdd53`  
		Last Modified: Mon, 29 Jun 2026 20:10:19 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:965e0f30952fe53c0edbbf51907861203a344a9f436d2f16e44ec62bbc6bc346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6389204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9954dc82025ebe69fb6051eba4e8b56422339f0c76b2978d73e05e4e95f4b686`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:13 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5f51f3ae5a0e9a233d660597cb0991d0e4eda1b8d6081f2ebf7b11bf49726cbb`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.4 MB (6388696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064965fad9d634082e200408edb6c3cfd405a94c5e956a0589886e52ab1e280e`  
		Last Modified: Mon, 29 Jun 2026 20:10:17 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:371542e6b03232abc94eb181db393c6435a837da512cce3804798309c30bdd0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512ea3056abc5f4e4d1b686c3750009080f9d259771aab353ae3dc28221d91b3`

```dockerfile
```

-	Layers:
	-	`sha256:207767c47f99e2d1e1fedd52ce5576598e2145c2fedbd08d52ebcb17283299be`  
		Last Modified: Mon, 29 Jun 2026 20:10:17 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cab7e89c5c123fa2c3080f70c5b47f612c9dc4ac52dc4323fbb3a595c57d7e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6136ec41f85090255a3129de60d735886601c26b2dff3bb5ae840dcfe8972d4b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:59 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:59 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:59 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:59 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:59 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c7f4ed7c5caaf7674fe731cc4314250f15b64d928d938c120113fda642ab9e35`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.1 MB (6055262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54c6d444001ace11b4843342fbb1034885520461c7f6927b617ae9ceec4f2be`  
		Last Modified: Mon, 29 Jun 2026 20:10:03 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:21a6ec729bb63eeb5fd248400b0794cea72020b49014664c9ea8f69873926b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b8f27c27fd4485ac0c2fb9fbd5f577f624409582d839d08b012e5a8980744`

```dockerfile
```

-	Layers:
	-	`sha256:359f4232c60d44b72e23371b39eef2f62ada8b687692b2f6f30998f4754f5cd3`  
		Last Modified: Mon, 29 Jun 2026 20:10:03 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:dffd7ab5566215b39ecc27f4cfbcbec3c87c5fc4d32314065b27fd2f8ab7be7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6114182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac585563eab840d4c0a5e821db019f88a9ffed79a5b5ac27087e72ae35f1674`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:47 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:68d08cefc115ab2d0ba836794a2aafdbd770ca3b82386eaca56b76eface4067a`  
		Last Modified: Mon, 29 Jun 2026 15:45:25 GMT  
		Size: 6.1 MB (6113673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44bd89ff0f6f728c9f3bc4b6f7be421abaa6e18d57cfc1df853cbe8892117a2`  
		Last Modified: Mon, 29 Jun 2026 19:12:53 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:507a6e760ac10e306655b5e454edf3ada3f99dc7a91c5f550316e528a7eb2435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace002f95a4f8bad573dd00622c3969d09ed698044207e366057ba33a9a84a5f`

```dockerfile
```

-	Layers:
	-	`sha256:4caf767452a66fa4931c741b42734d256bf6283f3a6a1dd604cfba793beb3aa3`  
		Last Modified: Mon, 29 Jun 2026 19:12:53 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.12-scratch` - linux; s390x

```console
$ docker pull nats@sha256:b5f2090a2865bc73183bdbbd5c2db2d4a5e90ab9902682414eee67678f44290e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6507115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081b3d096315958b9213985797ab5c0d1d1f51a9c134de884bdaddeafc215ec5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:23 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:23 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ee8c267e3cc1a37bddcdb99b2da7bdd61a07738138488ac8641bc09f0cb7dc28`  
		Last Modified: Mon, 29 Jun 2026 15:45:30 GMT  
		Size: 6.5 MB (6506606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3296f5cd680ca40417700ab16719d01bec8116be5da79289dd9c07b418c26d`  
		Last Modified: Mon, 29 Jun 2026 19:18:32 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:29663b73d5d3b96d00fbcad47681317129a61e699cc8a6a1b4c60f6b3773993e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8327c934690bae04254b49b552f8448751bd0bcc4abada12f8c086c470592bfc`

```dockerfile
```

-	Layers:
	-	`sha256:2e4c1745430ed822c5b545dbfce9175f49597264d12d3dc7bcd1aa56762e9a7f`  
		Last Modified: Mon, 29 Jun 2026 19:18:32 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.12-windowsservercore`

```console
$ docker pull nats@sha256:219eda2da2aaeaaf912b5fac6df5bc2fa546c80546af9cf24298b7d57914d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12.12-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:604c31d88ae285f9ec90722d08fdad90c4330e77566c23cca02f2140f9606b3e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2139846230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cb2b5e0f13b10edb1ec4b88255e5081ca32adb4272405eaa62694d6fe72926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 29 Jun 2026 19:19:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Jun 2026 19:19:34 GMT
ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 19:19:36 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:19:38 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:19:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.12/nats-server-v2.12.12-windows-amd64.zip
# Mon, 29 Jun 2026 19:19:41 GMT
ENV NATS_SERVER_SHASUM=66e2ab6250083794321905e1f79db4f4ea53465d84ba0760e9b00d022133050e
# Mon, 29 Jun 2026 19:20:48 GMT
RUN Set-PSDebug -Trace 2
# Mon, 29 Jun 2026 19:21:19 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 29 Jun 2026 19:21:20 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 19:21:21 GMT
EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 19:21:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 19:21:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f16a108e9d2bc33f0fca3c6297f4dde89e1012565ec5e6c8f73be682780439`  
		Last Modified: Mon, 29 Jun 2026 19:21:31 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b1177876813fcaab7e5a78eafe360842b9e21ec4f386a30157a38ba5742a9c`  
		Last Modified: Mon, 29 Jun 2026 19:21:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deec645e54e5f448eaa23276e6a129ad75071ddae6caa11003fdb5f28b4e5273`  
		Last Modified: Mon, 29 Jun 2026 19:21:31 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7baba77b0b911dac427ec025b5ae24f0ff40dded40b44d2a4d01c637134f2d`  
		Last Modified: Mon, 29 Jun 2026 19:21:29 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54553d8793c8e91455ebc378ebd9c1d5004521e9a74d79a89ce5d758c507c4be`  
		Last Modified: Mon, 29 Jun 2026 19:21:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3009c0e4ff927dffa0ecd3202aaf1cecd51781deda11e7a92e8cc79e450f09`  
		Last Modified: Mon, 29 Jun 2026 19:21:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93cfa08438f07b9987856fb41a344e9ad7338b8bddcebad69d2e6af361f4351`  
		Last Modified: Mon, 29 Jun 2026 19:21:30 GMT  
		Size: 497.4 KB (497435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b29917a60e39eb7c14c9ada61401f9b5e9591c9b7dbd0cd10e494516126de9`  
		Last Modified: Mon, 29 Jun 2026 19:21:32 GMT  
		Size: 7.2 MB (7209661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de7971acafe042855b721098603831ecafe3a8a4d4db756df118142a6da5233`  
		Last Modified: Mon, 29 Jun 2026 19:21:27 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15cdc907f166db6e75f6e881466aa143f728bb6f4b29d78e2c1b180563c7a30`  
		Last Modified: Mon, 29 Jun 2026 19:21:28 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b328cd9297132c05a7f02b94c4eaf6789a52806787eaf8f6da6bb00c2eb92b2`  
		Last Modified: Mon, 29 Jun 2026 19:21:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e478cda9ffcf7171ed42b072890941e48880a8f922a7aad5fcb85f32335cb43e`  
		Last Modified: Mon, 29 Jun 2026 19:21:27 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.12.12-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:219eda2da2aaeaaf912b5fac6df5bc2fa546c80546af9cf24298b7d57914d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.12.12-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:604c31d88ae285f9ec90722d08fdad90c4330e77566c23cca02f2140f9606b3e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2139846230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cb2b5e0f13b10edb1ec4b88255e5081ca32adb4272405eaa62694d6fe72926`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 29 Jun 2026 19:19:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Jun 2026 19:19:34 GMT
ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 19:19:36 GMT
ENV NATS_SERVER=2.12.12
# Mon, 29 Jun 2026 19:19:38 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.12
# Mon, 29 Jun 2026 19:19:40 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.12.12/nats-server-v2.12.12-windows-amd64.zip
# Mon, 29 Jun 2026 19:19:41 GMT
ENV NATS_SERVER_SHASUM=66e2ab6250083794321905e1f79db4f4ea53465d84ba0760e9b00d022133050e
# Mon, 29 Jun 2026 19:20:48 GMT
RUN Set-PSDebug -Trace 2
# Mon, 29 Jun 2026 19:21:19 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 29 Jun 2026 19:21:20 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 19:21:21 GMT
EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 19:21:22 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 19:21:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f16a108e9d2bc33f0fca3c6297f4dde89e1012565ec5e6c8f73be682780439`  
		Last Modified: Mon, 29 Jun 2026 19:21:31 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b1177876813fcaab7e5a78eafe360842b9e21ec4f386a30157a38ba5742a9c`  
		Last Modified: Mon, 29 Jun 2026 19:21:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deec645e54e5f448eaa23276e6a129ad75071ddae6caa11003fdb5f28b4e5273`  
		Last Modified: Mon, 29 Jun 2026 19:21:31 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7baba77b0b911dac427ec025b5ae24f0ff40dded40b44d2a4d01c637134f2d`  
		Last Modified: Mon, 29 Jun 2026 19:21:29 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54553d8793c8e91455ebc378ebd9c1d5004521e9a74d79a89ce5d758c507c4be`  
		Last Modified: Mon, 29 Jun 2026 19:21:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3009c0e4ff927dffa0ecd3202aaf1cecd51781deda11e7a92e8cc79e450f09`  
		Last Modified: Mon, 29 Jun 2026 19:21:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93cfa08438f07b9987856fb41a344e9ad7338b8bddcebad69d2e6af361f4351`  
		Last Modified: Mon, 29 Jun 2026 19:21:30 GMT  
		Size: 497.4 KB (497435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b29917a60e39eb7c14c9ada61401f9b5e9591c9b7dbd0cd10e494516126de9`  
		Last Modified: Mon, 29 Jun 2026 19:21:32 GMT  
		Size: 7.2 MB (7209661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de7971acafe042855b721098603831ecafe3a8a4d4db756df118142a6da5233`  
		Last Modified: Mon, 29 Jun 2026 19:21:27 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15cdc907f166db6e75f6e881466aa143f728bb6f4b29d78e2c1b180563c7a30`  
		Last Modified: Mon, 29 Jun 2026 19:21:28 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b328cd9297132c05a7f02b94c4eaf6789a52806787eaf8f6da6bb00c2eb92b2`  
		Last Modified: Mon, 29 Jun 2026 19:21:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e478cda9ffcf7171ed42b072890941e48880a8f922a7aad5fcb85f32335cb43e`  
		Last Modified: Mon, 29 Jun 2026 19:21:27 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14`

```console
$ docker pull nats@sha256:7ff2e641c33dbdb0dd13a943ba0b70d841b71275c607baa53ef9b8661f0b2d8c
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
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14` - linux; amd64

```console
$ docker pull nats@sha256:da52c7cd2dd8cfbfd7d2dfb251b761e42dbfd6fe0acb09fd26cbb42bdddb2866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6857592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ccfa5190b3b463a3fcf96e85c57584707cb0e37e977effc0b13df38ad27da`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:13:56 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:56 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:13:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:001b0b866410b42b38bcb2e428951af42433891ff425dfcce0b3a53cf93d9cf5`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.9 MB (6857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301e2bd5843dce0ae9f53e3b56e505349c98b58f06c463430d25b5c5ff3d2ac`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:4e6b9bd23e99f1e6893cbc2298ff6542ff362ac45479424f0cbbaa44e0bd7932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b91a2a2149df4bdf026d1ba840708ff2f744d4552979b6f5238e32d4b9fadd`

```dockerfile
```

-	Layers:
	-	`sha256:f2654502a1c07929b5dba813de85a6fecf099bd5b4e5dc0304f5bffb9a55374a`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm variant v6

```console
$ docker pull nats@sha256:f954b0114100cc6b04d48371743c840445bbd9d9cd58fd347d548df20fb81377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc68893e7b073ba43eb1643ffef18c78a2bcde561b9df87690e4c25b31729d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:087a70319659349faa0bc66d2f258c634f201af06cf4cd72fd052fe0f1741923`  
		Last Modified: Mon, 29 Jun 2026 15:45:00 GMT  
		Size: 6.6 MB (6591390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48bfacc9913ae01cc25da4a4e0b5b45dd8572ebef94eb75ee659e643ca668f`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:2ddfb53928614b91b72d029bf8c1fe2c18c9323525cddd2435738502af8f535f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c648adf5a8076bdff845afbe972feb29cbce83a045fc1fa7a6407350edd450`

```dockerfile
```

-	Layers:
	-	`sha256:f18d91a70c6190eda91e68db672ccbc0be90eca9e3a3cbca1053dac4180c85bb`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm variant v7

```console
$ docker pull nats@sha256:5acf1bcd52c9815e894b475e74896d5c20d20f75dc1d0a4609284c356a23e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eaac6cac973cc88e6d44cfa8e4fa97db877aa382eca9ca11a3aabdc71efaa4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95cb78be6f3eb15e97acc3a341503927e5ccafbd12a09b4a1b82fbb89f4787b5`  
		Last Modified: Mon, 29 Jun 2026 15:45:01 GMT  
		Size: 6.6 MB (6580972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce96a7f9a07f1a57504be91420ffc8fe2f13ee198161d2b34cfa5461201d23c9`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:7350f027d99946847895026cb1af3842bdad2563af2c7a4902c947e3e5859335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365d446dc11c95971d0b41e292ef423e0863365d7c070019c54d2c193b476ff`

```dockerfile
```

-	Layers:
	-	`sha256:0d8192ce2954c6a959615d982ceaa8825bd46cf89ead122b5706cc29fcf8bd71`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e15191f85a79618d9811e8747e99ac98b0a40bfaae0aaaa5001bb1230c1d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6207675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2b8f5a6e48a97cd470606ae3bf871c5e7a728291b699ed0fc6ade464b4cd4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ceb26b4c7119501bb3160d6cbbe50dce6ca269cc3bc37d3bfb9a8d65ab54e83e`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.2 MB (6207167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a970c139d6bb37d99b808c536d15fdfb2452430180d1906126f13f7c0e3e65c8`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:dbb4f985f00b8ed1cf158bbc14683f3982c6af4dbbd8a11fb368833ce8ab40d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762707c4a125db65916d8207dfc41bd88cb661dfd73431bef3936beaa1b6e79`

```dockerfile
```

-	Layers:
	-	`sha256:6d1ce7246188626d86f106948c8c45d6673d92d8b12bc55a2f76ad1a4a77c06b`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; ppc64le

```console
$ docker pull nats@sha256:0d2f692536149ac22566cf1b8c8c155bbf8704b0219606b603d37a2eb62f66a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6271147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5853d65dc9c9039e59f599fe9d6264c1b4b775d3ec6a9efaefa2487a1b2910c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:46 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:094159f217313d715a9c9416ce56b6efb6774fae53d0a118eb72c19dd5050f69`  
		Last Modified: Mon, 29 Jun 2026 15:45:02 GMT  
		Size: 6.3 MB (6270639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1d383fd4674e2d350a56d40d9d7a4a018dcdcac31733be7d84231bbad1d5b`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:7388f5e7e39dd5b070cb36fd9cf62973a1dbe1673ae86098ed3504c78e1ef328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a70cea4e571b8e5e9bb3f1775b350266ece5ba0911b4910d792e2f5c7a8522`

```dockerfile
```

-	Layers:
	-	`sha256:c683a72a6137cd681254bab9a60e1a450a3a8e636d80bcccb57e77942df0b512`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - linux; s390x

```console
$ docker pull nats@sha256:fa31a78cc1dfc74ac5954db2d0fabe8025d55442dd778436f11eb45bbad212b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a751449230c715131c826c9e954f6c6faab06fed9d6ac6ef617518f68b0f57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c051b099bef1cbfeba54872473e4a7281c4a402d9f0b7c1bdf892e5e21ea8c51`  
		Last Modified: Mon, 29 Jun 2026 15:45:04 GMT  
		Size: 6.7 MB (6666239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd00d66579c55de314f0aa7536b46c9471486f908c26ae17a7d930bfdd9fb9`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14` - unknown; unknown

```console
$ docker pull nats@sha256:6e482d7d215597ddb64e6a49fb2d97ed5f170b063872e7b945de9574375342eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa169f897fcb8ad6d1b168458e6f22434b580cca5dd468838bbd781ec75f31a`

```dockerfile
```

-	Layers:
	-	`sha256:cfe01b7f8ddd174d7457c698713d2616d4d35273045161e7a898b8d8a593e3f4`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:9f0daa17d5998a047f470ea9d8842dc0eb687557782823b3fea2bc5538aeaf23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131054329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b328dd4c47b0486963aab87b1d33d09cc56b17a894d7d1f8cbff35d6514a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:13:42 GMT
RUN cmd /S /C #(nop) COPY file:d28b1675c385af4d7600302dadf40a3bf46cd73b4ca42fe37500427a26b9b480 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:13:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:13:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:13:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:13:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3906542123b76df88980ceb04181b631e9922c06a031cb9d6c343bc4fc335b59`  
		Last Modified: Mon, 29 Jun 2026 20:13:57 GMT  
		Size: 7.1 MB (7050935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0464c24aec36583186ddd00d659a44cbfbe8eb6967595e263922cee114f11541`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e247b1ab45847502319a775832f1e37efd8e27edab85850c1cd39355d7c59a`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bca692b6b90a8e7b2b7d9ea755343336ec76f096b7f3eef575a86f50e64dc5`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3557d9ac8171b21f42a1bee80b244527a6000a38cb1673347a20e01f26387`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-alpine`

```console
$ docker pull nats@sha256:c11af972c99ae542de8925e6a7d9c533aa1eb039660420d2074beed6089b3bf0
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

### `nats:2.14-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4e53bdfe4a9d810005abaf974dd9a12374c9cd187fa6be4622eff6a73b9e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8ea3792d3865371b24b0504e2a7a61140487a85c1289a56e6b0a414f3aa451`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fb591416c4f81c00164a6df7c9a0df260683e8939dad253a229dad6006eed7`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 7.0 MB (7001975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a94003f98dbb2cec821705d1615ee3fabdb6278a14a965fad556f00935df4e`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca954dfa8945adfa8283aac38370a786f5ed56c79b3a242cdc0a7717732e4c01`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d2617716222bd82abc599cbe8277f98292977c0dfdd769178f6be9d0fdbfafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf691e94e06290aeb75516eb80f45749858c6ac66c0462f375e5b23f89c0f28`

```dockerfile
```

-	Layers:
	-	`sha256:051ab4a8c59747a86c2b341f78f881dcb5ce383e1adb18760b2e37658493f9f3`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:13a3f0e29c614c6b948bac76e8511e103dae75a1f3aafb215d49defef515bda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10202964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b0bb66ac4162fc21cb64f4e23f7840a339f47c9c6e9fe68e07f879189b36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c57aa7f84636f8b81c22758ea4a628036299dea2750a000eb5de6220234b418`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 7.0 MB (6992381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b307022eba60d3fa1d5f402e6c270a824a7c22733d6b54b89a11d8e47f5df06`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979223c0d164e45ff3d261730284785ca49e194cd773a37086da9bdd856159e`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cc9db77acad1e638c9d195fe27bf9cb73a582f1d6c8a48de4aac85d42fe8b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e4eea65b1e82754ac2719f2026f89bf4d253eda69a68c1c7a0753cc424985`

```dockerfile
```

-	Layers:
	-	`sha256:be67ebf23efa9ed614c3e6ecbd8dbfe60c3c196c67672894c62befc4102a028d`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:064222a09af7b194af6760d6089aa9ebd93fe7b8136ec2193ddb72dd78d8bd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10740987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b422fa2e0339d3eb86f18cdd7040198afd726fadc2c6c0f499eff9c9038c9926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d45f995edc436f16aee98c90da4e281a787ba379a91c7b812155f24b01f240c`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 6.6 MB (6619532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721188e517e99c1592046fd1c1f9d23061e01b186bfce2cef6bc65a52a5f7fd`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d19df182cbee156b010b04853280b7c12519c2b2a73a5d9a80ae357c814c67`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e4aef08d7bba47a53a2cdfea2260f5792c1fdb440a5ad4ff982730170aa3deb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb8badc11acca1d928d62f328aa0f3707584a4655e9abfa03e3b1b697d59a65`

```dockerfile
```

-	Layers:
	-	`sha256:e3cd06dd05bb0a25b9621e25ea152cd6cffebb5eff99e2740970497eaafedfd3`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-alpine3.22`

```console
$ docker pull nats@sha256:c11af972c99ae542de8925e6a7d9c533aa1eb039660420d2074beed6089b3bf0
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

### `nats:2.14-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4e53bdfe4a9d810005abaf974dd9a12374c9cd187fa6be4622eff6a73b9e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8ea3792d3865371b24b0504e2a7a61140487a85c1289a56e6b0a414f3aa451`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fb591416c4f81c00164a6df7c9a0df260683e8939dad253a229dad6006eed7`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 7.0 MB (7001975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a94003f98dbb2cec821705d1615ee3fabdb6278a14a965fad556f00935df4e`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca954dfa8945adfa8283aac38370a786f5ed56c79b3a242cdc0a7717732e4c01`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d2617716222bd82abc599cbe8277f98292977c0dfdd769178f6be9d0fdbfafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf691e94e06290aeb75516eb80f45749858c6ac66c0462f375e5b23f89c0f28`

```dockerfile
```

-	Layers:
	-	`sha256:051ab4a8c59747a86c2b341f78f881dcb5ce383e1adb18760b2e37658493f9f3`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:13a3f0e29c614c6b948bac76e8511e103dae75a1f3aafb215d49defef515bda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10202964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b0bb66ac4162fc21cb64f4e23f7840a339f47c9c6e9fe68e07f879189b36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c57aa7f84636f8b81c22758ea4a628036299dea2750a000eb5de6220234b418`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 7.0 MB (6992381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b307022eba60d3fa1d5f402e6c270a824a7c22733d6b54b89a11d8e47f5df06`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979223c0d164e45ff3d261730284785ca49e194cd773a37086da9bdd856159e`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:cc9db77acad1e638c9d195fe27bf9cb73a582f1d6c8a48de4aac85d42fe8b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e4eea65b1e82754ac2719f2026f89bf4d253eda69a68c1c7a0753cc424985`

```dockerfile
```

-	Layers:
	-	`sha256:be67ebf23efa9ed614c3e6ecbd8dbfe60c3c196c67672894c62befc4102a028d`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:064222a09af7b194af6760d6089aa9ebd93fe7b8136ec2193ddb72dd78d8bd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10740987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b422fa2e0339d3eb86f18cdd7040198afd726fadc2c6c0f499eff9c9038c9926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d45f995edc436f16aee98c90da4e281a787ba379a91c7b812155f24b01f240c`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 6.6 MB (6619532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721188e517e99c1592046fd1c1f9d23061e01b186bfce2cef6bc65a52a5f7fd`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d19df182cbee156b010b04853280b7c12519c2b2a73a5d9a80ae357c814c67`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e4aef08d7bba47a53a2cdfea2260f5792c1fdb440a5ad4ff982730170aa3deb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb8badc11acca1d928d62f328aa0f3707584a4655e9abfa03e3b1b697d59a65`

```dockerfile
```

-	Layers:
	-	`sha256:e3cd06dd05bb0a25b9621e25ea152cd6cffebb5eff99e2740970497eaafedfd3`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-linux`

```console
$ docker pull nats@sha256:1b5a0a665cbe50a4ea28e8a82cf809b26cee5027d1fcaf8682fadf8f385fdf29
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

### `nats:2.14-linux` - linux; amd64

```console
$ docker pull nats@sha256:da52c7cd2dd8cfbfd7d2dfb251b761e42dbfd6fe0acb09fd26cbb42bdddb2866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6857592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ccfa5190b3b463a3fcf96e85c57584707cb0e37e977effc0b13df38ad27da`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:13:56 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:56 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:13:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:001b0b866410b42b38bcb2e428951af42433891ff425dfcce0b3a53cf93d9cf5`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.9 MB (6857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301e2bd5843dce0ae9f53e3b56e505349c98b58f06c463430d25b5c5ff3d2ac`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4e6b9bd23e99f1e6893cbc2298ff6542ff362ac45479424f0cbbaa44e0bd7932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b91a2a2149df4bdf026d1ba840708ff2f744d4552979b6f5238e32d4b9fadd`

```dockerfile
```

-	Layers:
	-	`sha256:f2654502a1c07929b5dba813de85a6fecf099bd5b4e5dc0304f5bffb9a55374a`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f954b0114100cc6b04d48371743c840445bbd9d9cd58fd347d548df20fb81377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc68893e7b073ba43eb1643ffef18c78a2bcde561b9df87690e4c25b31729d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:087a70319659349faa0bc66d2f258c634f201af06cf4cd72fd052fe0f1741923`  
		Last Modified: Mon, 29 Jun 2026 15:45:00 GMT  
		Size: 6.6 MB (6591390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48bfacc9913ae01cc25da4a4e0b5b45dd8572ebef94eb75ee659e643ca668f`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2ddfb53928614b91b72d029bf8c1fe2c18c9323525cddd2435738502af8f535f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c648adf5a8076bdff845afbe972feb29cbce83a045fc1fa7a6407350edd450`

```dockerfile
```

-	Layers:
	-	`sha256:f18d91a70c6190eda91e68db672ccbc0be90eca9e3a3cbca1053dac4180c85bb`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5acf1bcd52c9815e894b475e74896d5c20d20f75dc1d0a4609284c356a23e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eaac6cac973cc88e6d44cfa8e4fa97db877aa382eca9ca11a3aabdc71efaa4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95cb78be6f3eb15e97acc3a341503927e5ccafbd12a09b4a1b82fbb89f4787b5`  
		Last Modified: Mon, 29 Jun 2026 15:45:01 GMT  
		Size: 6.6 MB (6580972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce96a7f9a07f1a57504be91420ffc8fe2f13ee198161d2b34cfa5461201d23c9`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7350f027d99946847895026cb1af3842bdad2563af2c7a4902c947e3e5859335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365d446dc11c95971d0b41e292ef423e0863365d7c070019c54d2c193b476ff`

```dockerfile
```

-	Layers:
	-	`sha256:0d8192ce2954c6a959615d982ceaa8825bd46cf89ead122b5706cc29fcf8bd71`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e15191f85a79618d9811e8747e99ac98b0a40bfaae0aaaa5001bb1230c1d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6207675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2b8f5a6e48a97cd470606ae3bf871c5e7a728291b699ed0fc6ade464b4cd4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ceb26b4c7119501bb3160d6cbbe50dce6ca269cc3bc37d3bfb9a8d65ab54e83e`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.2 MB (6207167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a970c139d6bb37d99b808c536d15fdfb2452430180d1906126f13f7c0e3e65c8`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:dbb4f985f00b8ed1cf158bbc14683f3982c6af4dbbd8a11fb368833ce8ab40d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762707c4a125db65916d8207dfc41bd88cb661dfd73431bef3936beaa1b6e79`

```dockerfile
```

-	Layers:
	-	`sha256:6d1ce7246188626d86f106948c8c45d6673d92d8b12bc55a2f76ad1a4a77c06b`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:0d2f692536149ac22566cf1b8c8c155bbf8704b0219606b603d37a2eb62f66a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6271147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5853d65dc9c9039e59f599fe9d6264c1b4b775d3ec6a9efaefa2487a1b2910c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:46 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:094159f217313d715a9c9416ce56b6efb6774fae53d0a118eb72c19dd5050f69`  
		Last Modified: Mon, 29 Jun 2026 15:45:02 GMT  
		Size: 6.3 MB (6270639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1d383fd4674e2d350a56d40d9d7a4a018dcdcac31733be7d84231bbad1d5b`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7388f5e7e39dd5b070cb36fd9cf62973a1dbe1673ae86098ed3504c78e1ef328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a70cea4e571b8e5e9bb3f1775b350266ece5ba0911b4910d792e2f5c7a8522`

```dockerfile
```

-	Layers:
	-	`sha256:c683a72a6137cd681254bab9a60e1a450a3a8e636d80bcccb57e77942df0b512`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-linux` - linux; s390x

```console
$ docker pull nats@sha256:fa31a78cc1dfc74ac5954db2d0fabe8025d55442dd778436f11eb45bbad212b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a751449230c715131c826c9e954f6c6faab06fed9d6ac6ef617518f68b0f57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c051b099bef1cbfeba54872473e4a7281c4a402d9f0b7c1bdf892e5e21ea8c51`  
		Last Modified: Mon, 29 Jun 2026 15:45:04 GMT  
		Size: 6.7 MB (6666239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd00d66579c55de314f0aa7536b46c9471486f908c26ae17a7d930bfdd9fb9`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6e482d7d215597ddb64e6a49fb2d97ed5f170b063872e7b945de9574375342eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa169f897fcb8ad6d1b168458e6f22434b580cca5dd468838bbd781ec75f31a`

```dockerfile
```

-	Layers:
	-	`sha256:cfe01b7f8ddd174d7457c698713d2616d4d35273045161e7a898b8d8a593e3f4`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-nanoserver`

```console
$ docker pull nats@sha256:1d52723019944547c28befc6831cf54a194fe6cf5da2cbe5d83dada671148eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:9f0daa17d5998a047f470ea9d8842dc0eb687557782823b3fea2bc5538aeaf23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131054329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b328dd4c47b0486963aab87b1d33d09cc56b17a894d7d1f8cbff35d6514a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:13:42 GMT
RUN cmd /S /C #(nop) COPY file:d28b1675c385af4d7600302dadf40a3bf46cd73b4ca42fe37500427a26b9b480 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:13:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:13:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:13:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:13:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3906542123b76df88980ceb04181b631e9922c06a031cb9d6c343bc4fc335b59`  
		Last Modified: Mon, 29 Jun 2026 20:13:57 GMT  
		Size: 7.1 MB (7050935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0464c24aec36583186ddd00d659a44cbfbe8eb6967595e263922cee114f11541`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e247b1ab45847502319a775832f1e37efd8e27edab85850c1cd39355d7c59a`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bca692b6b90a8e7b2b7d9ea755343336ec76f096b7f3eef575a86f50e64dc5`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3557d9ac8171b21f42a1bee80b244527a6000a38cb1673347a20e01f26387`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:1d52723019944547c28befc6831cf54a194fe6cf5da2cbe5d83dada671148eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:9f0daa17d5998a047f470ea9d8842dc0eb687557782823b3fea2bc5538aeaf23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131054329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b328dd4c47b0486963aab87b1d33d09cc56b17a894d7d1f8cbff35d6514a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:13:42 GMT
RUN cmd /S /C #(nop) COPY file:d28b1675c385af4d7600302dadf40a3bf46cd73b4ca42fe37500427a26b9b480 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:13:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:13:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:13:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:13:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3906542123b76df88980ceb04181b631e9922c06a031cb9d6c343bc4fc335b59`  
		Last Modified: Mon, 29 Jun 2026 20:13:57 GMT  
		Size: 7.1 MB (7050935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0464c24aec36583186ddd00d659a44cbfbe8eb6967595e263922cee114f11541`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e247b1ab45847502319a775832f1e37efd8e27edab85850c1cd39355d7c59a`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bca692b6b90a8e7b2b7d9ea755343336ec76f096b7f3eef575a86f50e64dc5`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3557d9ac8171b21f42a1bee80b244527a6000a38cb1673347a20e01f26387`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-scratch`

```console
$ docker pull nats@sha256:1b5a0a665cbe50a4ea28e8a82cf809b26cee5027d1fcaf8682fadf8f385fdf29
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

### `nats:2.14-scratch` - linux; amd64

```console
$ docker pull nats@sha256:da52c7cd2dd8cfbfd7d2dfb251b761e42dbfd6fe0acb09fd26cbb42bdddb2866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6857592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ccfa5190b3b463a3fcf96e85c57584707cb0e37e977effc0b13df38ad27da`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:13:56 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:56 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:13:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:001b0b866410b42b38bcb2e428951af42433891ff425dfcce0b3a53cf93d9cf5`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.9 MB (6857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301e2bd5843dce0ae9f53e3b56e505349c98b58f06c463430d25b5c5ff3d2ac`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4e6b9bd23e99f1e6893cbc2298ff6542ff362ac45479424f0cbbaa44e0bd7932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b91a2a2149df4bdf026d1ba840708ff2f744d4552979b6f5238e32d4b9fadd`

```dockerfile
```

-	Layers:
	-	`sha256:f2654502a1c07929b5dba813de85a6fecf099bd5b4e5dc0304f5bffb9a55374a`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f954b0114100cc6b04d48371743c840445bbd9d9cd58fd347d548df20fb81377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc68893e7b073ba43eb1643ffef18c78a2bcde561b9df87690e4c25b31729d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:087a70319659349faa0bc66d2f258c634f201af06cf4cd72fd052fe0f1741923`  
		Last Modified: Mon, 29 Jun 2026 15:45:00 GMT  
		Size: 6.6 MB (6591390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48bfacc9913ae01cc25da4a4e0b5b45dd8572ebef94eb75ee659e643ca668f`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2ddfb53928614b91b72d029bf8c1fe2c18c9323525cddd2435738502af8f535f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c648adf5a8076bdff845afbe972feb29cbce83a045fc1fa7a6407350edd450`

```dockerfile
```

-	Layers:
	-	`sha256:f18d91a70c6190eda91e68db672ccbc0be90eca9e3a3cbca1053dac4180c85bb`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5acf1bcd52c9815e894b475e74896d5c20d20f75dc1d0a4609284c356a23e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eaac6cac973cc88e6d44cfa8e4fa97db877aa382eca9ca11a3aabdc71efaa4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95cb78be6f3eb15e97acc3a341503927e5ccafbd12a09b4a1b82fbb89f4787b5`  
		Last Modified: Mon, 29 Jun 2026 15:45:01 GMT  
		Size: 6.6 MB (6580972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce96a7f9a07f1a57504be91420ffc8fe2f13ee198161d2b34cfa5461201d23c9`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7350f027d99946847895026cb1af3842bdad2563af2c7a4902c947e3e5859335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365d446dc11c95971d0b41e292ef423e0863365d7c070019c54d2c193b476ff`

```dockerfile
```

-	Layers:
	-	`sha256:0d8192ce2954c6a959615d982ceaa8825bd46cf89ead122b5706cc29fcf8bd71`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e15191f85a79618d9811e8747e99ac98b0a40bfaae0aaaa5001bb1230c1d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6207675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2b8f5a6e48a97cd470606ae3bf871c5e7a728291b699ed0fc6ade464b4cd4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ceb26b4c7119501bb3160d6cbbe50dce6ca269cc3bc37d3bfb9a8d65ab54e83e`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.2 MB (6207167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a970c139d6bb37d99b808c536d15fdfb2452430180d1906126f13f7c0e3e65c8`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:dbb4f985f00b8ed1cf158bbc14683f3982c6af4dbbd8a11fb368833ce8ab40d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762707c4a125db65916d8207dfc41bd88cb661dfd73431bef3936beaa1b6e79`

```dockerfile
```

-	Layers:
	-	`sha256:6d1ce7246188626d86f106948c8c45d6673d92d8b12bc55a2f76ad1a4a77c06b`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:0d2f692536149ac22566cf1b8c8c155bbf8704b0219606b603d37a2eb62f66a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6271147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5853d65dc9c9039e59f599fe9d6264c1b4b775d3ec6a9efaefa2487a1b2910c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:46 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:094159f217313d715a9c9416ce56b6efb6774fae53d0a118eb72c19dd5050f69`  
		Last Modified: Mon, 29 Jun 2026 15:45:02 GMT  
		Size: 6.3 MB (6270639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1d383fd4674e2d350a56d40d9d7a4a018dcdcac31733be7d84231bbad1d5b`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7388f5e7e39dd5b070cb36fd9cf62973a1dbe1673ae86098ed3504c78e1ef328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a70cea4e571b8e5e9bb3f1775b350266ece5ba0911b4910d792e2f5c7a8522`

```dockerfile
```

-	Layers:
	-	`sha256:c683a72a6137cd681254bab9a60e1a450a3a8e636d80bcccb57e77942df0b512`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14-scratch` - linux; s390x

```console
$ docker pull nats@sha256:fa31a78cc1dfc74ac5954db2d0fabe8025d55442dd778436f11eb45bbad212b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a751449230c715131c826c9e954f6c6faab06fed9d6ac6ef617518f68b0f57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c051b099bef1cbfeba54872473e4a7281c4a402d9f0b7c1bdf892e5e21ea8c51`  
		Last Modified: Mon, 29 Jun 2026 15:45:04 GMT  
		Size: 6.7 MB (6666239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd00d66579c55de314f0aa7536b46c9471486f908c26ae17a7d930bfdd9fb9`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6e482d7d215597ddb64e6a49fb2d97ed5f170b063872e7b945de9574375342eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa169f897fcb8ad6d1b168458e6f22434b580cca5dd468838bbd781ec75f31a`

```dockerfile
```

-	Layers:
	-	`sha256:cfe01b7f8ddd174d7457c698713d2616d4d35273045161e7a898b8d8a593e3f4`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14-windowsservercore`

```console
$ docker pull nats@sha256:f701716476a8d968bd766320239d98d7f973ebaaa7a6f960f65648bda132229e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:2c61006c6743420a33c3ade658d600d9b81f09a86df8c44fe02741a71d196d7f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140052973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782541001e22820de00703de294e85e7c622fc9ea85c9030e8fda96177afa0cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 29 Jun 2026 19:16:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Jun 2026 19:16:31 GMT
ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 19:16:32 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:16:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:16:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.3/nats-server-v2.14.3-windows-amd64.zip
# Mon, 29 Jun 2026 19:16:37 GMT
ENV NATS_SERVER_SHASUM=94e338d742761272e31eab1efb1f767eac3a2e56e4c05a7933c65a73fe95a27b
# Mon, 29 Jun 2026 19:17:35 GMT
RUN Set-PSDebug -Trace 2
# Mon, 29 Jun 2026 19:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 29 Jun 2026 19:18:06 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 19:18:08 GMT
EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 19:18:09 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 19:18:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac87f215828b12e2044c46470b221ea4307d0fc11cf8280e12474587a59317d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff6f7da74f9e652f79bc8278319981b268148b1548a3ef4220d3ccbe4b5473d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e85164857353b52ed850cc83049bc199678edaed484f95d1e38aa0a4f1b525b`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706cc542b32b6c088b1b95499c39a0c6f9dbe749f47087a0cd668545100147ba`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25bcf16bfd2387cc38d31f75eeac32290dada9d452e1f50b902530775f1c0ff`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aecb5ee131c5c835ec5c73c2ad224bf1e9c3ede99efeca9eec6a270f5c22b1`  
		Last Modified: Mon, 29 Jun 2026 19:18:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f1b98897859ea619b08dd0f0db49b009771052a13d263d4980a21c40901f2`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 496.7 KB (496723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784da3b63359a7bbb87eb47bb8a637b409b418e94af977bf3c24722cbc2ec89e`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 7.4 MB (7417113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae24643aacc8edba76b5661a3358a9461f9fda9a7d1f0fccaeca461dfb074a23`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe52ddb42630f70fd61331adf5e83118d27382c4d3922882adb2d981105bac94`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087e85133498df0eb7d45b8bc9353ec3fa1fc98964b2f88c33152ca73bf5abd6`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9462b672f1e05436ba0020f6b3b71b8db8b844d5c5183c1088c29d06d39df1be`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:f701716476a8d968bd766320239d98d7f973ebaaa7a6f960f65648bda132229e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:2c61006c6743420a33c3ade658d600d9b81f09a86df8c44fe02741a71d196d7f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140052973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782541001e22820de00703de294e85e7c622fc9ea85c9030e8fda96177afa0cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 29 Jun 2026 19:16:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Jun 2026 19:16:31 GMT
ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 19:16:32 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:16:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:16:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.3/nats-server-v2.14.3-windows-amd64.zip
# Mon, 29 Jun 2026 19:16:37 GMT
ENV NATS_SERVER_SHASUM=94e338d742761272e31eab1efb1f767eac3a2e56e4c05a7933c65a73fe95a27b
# Mon, 29 Jun 2026 19:17:35 GMT
RUN Set-PSDebug -Trace 2
# Mon, 29 Jun 2026 19:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 29 Jun 2026 19:18:06 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 19:18:08 GMT
EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 19:18:09 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 19:18:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac87f215828b12e2044c46470b221ea4307d0fc11cf8280e12474587a59317d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff6f7da74f9e652f79bc8278319981b268148b1548a3ef4220d3ccbe4b5473d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e85164857353b52ed850cc83049bc199678edaed484f95d1e38aa0a4f1b525b`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706cc542b32b6c088b1b95499c39a0c6f9dbe749f47087a0cd668545100147ba`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25bcf16bfd2387cc38d31f75eeac32290dada9d452e1f50b902530775f1c0ff`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aecb5ee131c5c835ec5c73c2ad224bf1e9c3ede99efeca9eec6a270f5c22b1`  
		Last Modified: Mon, 29 Jun 2026 19:18:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f1b98897859ea619b08dd0f0db49b009771052a13d263d4980a21c40901f2`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 496.7 KB (496723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784da3b63359a7bbb87eb47bb8a637b409b418e94af977bf3c24722cbc2ec89e`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 7.4 MB (7417113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae24643aacc8edba76b5661a3358a9461f9fda9a7d1f0fccaeca461dfb074a23`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe52ddb42630f70fd61331adf5e83118d27382c4d3922882adb2d981105bac94`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087e85133498df0eb7d45b8bc9353ec3fa1fc98964b2f88c33152ca73bf5abd6`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9462b672f1e05436ba0020f6b3b71b8db8b844d5c5183c1088c29d06d39df1be`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.3`

```console
$ docker pull nats@sha256:7ff2e641c33dbdb0dd13a943ba0b70d841b71275c607baa53ef9b8661f0b2d8c
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
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14.3` - linux; amd64

```console
$ docker pull nats@sha256:da52c7cd2dd8cfbfd7d2dfb251b761e42dbfd6fe0acb09fd26cbb42bdddb2866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6857592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ccfa5190b3b463a3fcf96e85c57584707cb0e37e977effc0b13df38ad27da`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:13:56 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:56 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:13:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:001b0b866410b42b38bcb2e428951af42433891ff425dfcce0b3a53cf93d9cf5`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.9 MB (6857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301e2bd5843dce0ae9f53e3b56e505349c98b58f06c463430d25b5c5ff3d2ac`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3` - unknown; unknown

```console
$ docker pull nats@sha256:4e6b9bd23e99f1e6893cbc2298ff6542ff362ac45479424f0cbbaa44e0bd7932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b91a2a2149df4bdf026d1ba840708ff2f744d4552979b6f5238e32d4b9fadd`

```dockerfile
```

-	Layers:
	-	`sha256:f2654502a1c07929b5dba813de85a6fecf099bd5b4e5dc0304f5bffb9a55374a`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3` - linux; arm variant v6

```console
$ docker pull nats@sha256:f954b0114100cc6b04d48371743c840445bbd9d9cd58fd347d548df20fb81377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc68893e7b073ba43eb1643ffef18c78a2bcde561b9df87690e4c25b31729d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:087a70319659349faa0bc66d2f258c634f201af06cf4cd72fd052fe0f1741923`  
		Last Modified: Mon, 29 Jun 2026 15:45:00 GMT  
		Size: 6.6 MB (6591390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48bfacc9913ae01cc25da4a4e0b5b45dd8572ebef94eb75ee659e643ca668f`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3` - unknown; unknown

```console
$ docker pull nats@sha256:2ddfb53928614b91b72d029bf8c1fe2c18c9323525cddd2435738502af8f535f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c648adf5a8076bdff845afbe972feb29cbce83a045fc1fa7a6407350edd450`

```dockerfile
```

-	Layers:
	-	`sha256:f18d91a70c6190eda91e68db672ccbc0be90eca9e3a3cbca1053dac4180c85bb`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3` - linux; arm variant v7

```console
$ docker pull nats@sha256:5acf1bcd52c9815e894b475e74896d5c20d20f75dc1d0a4609284c356a23e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eaac6cac973cc88e6d44cfa8e4fa97db877aa382eca9ca11a3aabdc71efaa4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95cb78be6f3eb15e97acc3a341503927e5ccafbd12a09b4a1b82fbb89f4787b5`  
		Last Modified: Mon, 29 Jun 2026 15:45:01 GMT  
		Size: 6.6 MB (6580972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce96a7f9a07f1a57504be91420ffc8fe2f13ee198161d2b34cfa5461201d23c9`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3` - unknown; unknown

```console
$ docker pull nats@sha256:7350f027d99946847895026cb1af3842bdad2563af2c7a4902c947e3e5859335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365d446dc11c95971d0b41e292ef423e0863365d7c070019c54d2c193b476ff`

```dockerfile
```

-	Layers:
	-	`sha256:0d8192ce2954c6a959615d982ceaa8825bd46cf89ead122b5706cc29fcf8bd71`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e15191f85a79618d9811e8747e99ac98b0a40bfaae0aaaa5001bb1230c1d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6207675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2b8f5a6e48a97cd470606ae3bf871c5e7a728291b699ed0fc6ade464b4cd4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ceb26b4c7119501bb3160d6cbbe50dce6ca269cc3bc37d3bfb9a8d65ab54e83e`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.2 MB (6207167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a970c139d6bb37d99b808c536d15fdfb2452430180d1906126f13f7c0e3e65c8`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3` - unknown; unknown

```console
$ docker pull nats@sha256:dbb4f985f00b8ed1cf158bbc14683f3982c6af4dbbd8a11fb368833ce8ab40d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762707c4a125db65916d8207dfc41bd88cb661dfd73431bef3936beaa1b6e79`

```dockerfile
```

-	Layers:
	-	`sha256:6d1ce7246188626d86f106948c8c45d6673d92d8b12bc55a2f76ad1a4a77c06b`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3` - linux; ppc64le

```console
$ docker pull nats@sha256:0d2f692536149ac22566cf1b8c8c155bbf8704b0219606b603d37a2eb62f66a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6271147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5853d65dc9c9039e59f599fe9d6264c1b4b775d3ec6a9efaefa2487a1b2910c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:46 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:094159f217313d715a9c9416ce56b6efb6774fae53d0a118eb72c19dd5050f69`  
		Last Modified: Mon, 29 Jun 2026 15:45:02 GMT  
		Size: 6.3 MB (6270639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1d383fd4674e2d350a56d40d9d7a4a018dcdcac31733be7d84231bbad1d5b`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3` - unknown; unknown

```console
$ docker pull nats@sha256:7388f5e7e39dd5b070cb36fd9cf62973a1dbe1673ae86098ed3504c78e1ef328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a70cea4e571b8e5e9bb3f1775b350266ece5ba0911b4910d792e2f5c7a8522`

```dockerfile
```

-	Layers:
	-	`sha256:c683a72a6137cd681254bab9a60e1a450a3a8e636d80bcccb57e77942df0b512`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3` - linux; s390x

```console
$ docker pull nats@sha256:fa31a78cc1dfc74ac5954db2d0fabe8025d55442dd778436f11eb45bbad212b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a751449230c715131c826c9e954f6c6faab06fed9d6ac6ef617518f68b0f57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c051b099bef1cbfeba54872473e4a7281c4a402d9f0b7c1bdf892e5e21ea8c51`  
		Last Modified: Mon, 29 Jun 2026 15:45:04 GMT  
		Size: 6.7 MB (6666239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd00d66579c55de314f0aa7536b46c9471486f908c26ae17a7d930bfdd9fb9`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3` - unknown; unknown

```console
$ docker pull nats@sha256:6e482d7d215597ddb64e6a49fb2d97ed5f170b063872e7b945de9574375342eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa169f897fcb8ad6d1b168458e6f22434b580cca5dd468838bbd781ec75f31a`

```dockerfile
```

-	Layers:
	-	`sha256:cfe01b7f8ddd174d7457c698713d2616d4d35273045161e7a898b8d8a593e3f4`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:9f0daa17d5998a047f470ea9d8842dc0eb687557782823b3fea2bc5538aeaf23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131054329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b328dd4c47b0486963aab87b1d33d09cc56b17a894d7d1f8cbff35d6514a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:13:42 GMT
RUN cmd /S /C #(nop) COPY file:d28b1675c385af4d7600302dadf40a3bf46cd73b4ca42fe37500427a26b9b480 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:13:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:13:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:13:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:13:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3906542123b76df88980ceb04181b631e9922c06a031cb9d6c343bc4fc335b59`  
		Last Modified: Mon, 29 Jun 2026 20:13:57 GMT  
		Size: 7.1 MB (7050935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0464c24aec36583186ddd00d659a44cbfbe8eb6967595e263922cee114f11541`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e247b1ab45847502319a775832f1e37efd8e27edab85850c1cd39355d7c59a`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bca692b6b90a8e7b2b7d9ea755343336ec76f096b7f3eef575a86f50e64dc5`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3557d9ac8171b21f42a1bee80b244527a6000a38cb1673347a20e01f26387`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.3-alpine`

```console
$ docker pull nats@sha256:c11af972c99ae542de8925e6a7d9c533aa1eb039660420d2074beed6089b3bf0
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

### `nats:2.14.3-alpine` - linux; amd64

```console
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4e53bdfe4a9d810005abaf974dd9a12374c9cd187fa6be4622eff6a73b9e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8ea3792d3865371b24b0504e2a7a61140487a85c1289a56e6b0a414f3aa451`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fb591416c4f81c00164a6df7c9a0df260683e8939dad253a229dad6006eed7`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 7.0 MB (7001975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a94003f98dbb2cec821705d1615ee3fabdb6278a14a965fad556f00935df4e`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca954dfa8945adfa8283aac38370a786f5ed56c79b3a242cdc0a7717732e4c01`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d2617716222bd82abc599cbe8277f98292977c0dfdd769178f6be9d0fdbfafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf691e94e06290aeb75516eb80f45749858c6ac66c0462f375e5b23f89c0f28`

```dockerfile
```

-	Layers:
	-	`sha256:051ab4a8c59747a86c2b341f78f881dcb5ce383e1adb18760b2e37658493f9f3`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:13a3f0e29c614c6b948bac76e8511e103dae75a1f3aafb215d49defef515bda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10202964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b0bb66ac4162fc21cb64f4e23f7840a339f47c9c6e9fe68e07f879189b36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c57aa7f84636f8b81c22758ea4a628036299dea2750a000eb5de6220234b418`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 7.0 MB (6992381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b307022eba60d3fa1d5f402e6c270a824a7c22733d6b54b89a11d8e47f5df06`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979223c0d164e45ff3d261730284785ca49e194cd773a37086da9bdd856159e`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cc9db77acad1e638c9d195fe27bf9cb73a582f1d6c8a48de4aac85d42fe8b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e4eea65b1e82754ac2719f2026f89bf4d253eda69a68c1c7a0753cc424985`

```dockerfile
```

-	Layers:
	-	`sha256:be67ebf23efa9ed614c3e6ecbd8dbfe60c3c196c67672894c62befc4102a028d`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:064222a09af7b194af6760d6089aa9ebd93fe7b8136ec2193ddb72dd78d8bd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10740987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b422fa2e0339d3eb86f18cdd7040198afd726fadc2c6c0f499eff9c9038c9926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d45f995edc436f16aee98c90da4e281a787ba379a91c7b812155f24b01f240c`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 6.6 MB (6619532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721188e517e99c1592046fd1c1f9d23061e01b186bfce2cef6bc65a52a5f7fd`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d19df182cbee156b010b04853280b7c12519c2b2a73a5d9a80ae357c814c67`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e4aef08d7bba47a53a2cdfea2260f5792c1fdb440a5ad4ff982730170aa3deb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb8badc11acca1d928d62f328aa0f3707584a4655e9abfa03e3b1b697d59a65`

```dockerfile
```

-	Layers:
	-	`sha256:e3cd06dd05bb0a25b9621e25ea152cd6cffebb5eff99e2740970497eaafedfd3`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.3-alpine3.22`

```console
$ docker pull nats@sha256:c11af972c99ae542de8925e6a7d9c533aa1eb039660420d2074beed6089b3bf0
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

### `nats:2.14.3-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4e53bdfe4a9d810005abaf974dd9a12374c9cd187fa6be4622eff6a73b9e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8ea3792d3865371b24b0504e2a7a61140487a85c1289a56e6b0a414f3aa451`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fb591416c4f81c00164a6df7c9a0df260683e8939dad253a229dad6006eed7`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 7.0 MB (7001975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a94003f98dbb2cec821705d1615ee3fabdb6278a14a965fad556f00935df4e`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca954dfa8945adfa8283aac38370a786f5ed56c79b3a242cdc0a7717732e4c01`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d2617716222bd82abc599cbe8277f98292977c0dfdd769178f6be9d0fdbfafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf691e94e06290aeb75516eb80f45749858c6ac66c0462f375e5b23f89c0f28`

```dockerfile
```

-	Layers:
	-	`sha256:051ab4a8c59747a86c2b341f78f881dcb5ce383e1adb18760b2e37658493f9f3`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:13a3f0e29c614c6b948bac76e8511e103dae75a1f3aafb215d49defef515bda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10202964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b0bb66ac4162fc21cb64f4e23f7840a339f47c9c6e9fe68e07f879189b36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c57aa7f84636f8b81c22758ea4a628036299dea2750a000eb5de6220234b418`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 7.0 MB (6992381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b307022eba60d3fa1d5f402e6c270a824a7c22733d6b54b89a11d8e47f5df06`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979223c0d164e45ff3d261730284785ca49e194cd773a37086da9bdd856159e`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:cc9db77acad1e638c9d195fe27bf9cb73a582f1d6c8a48de4aac85d42fe8b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e4eea65b1e82754ac2719f2026f89bf4d253eda69a68c1c7a0753cc424985`

```dockerfile
```

-	Layers:
	-	`sha256:be67ebf23efa9ed614c3e6ecbd8dbfe60c3c196c67672894c62befc4102a028d`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:064222a09af7b194af6760d6089aa9ebd93fe7b8136ec2193ddb72dd78d8bd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10740987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b422fa2e0339d3eb86f18cdd7040198afd726fadc2c6c0f499eff9c9038c9926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d45f995edc436f16aee98c90da4e281a787ba379a91c7b812155f24b01f240c`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 6.6 MB (6619532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721188e517e99c1592046fd1c1f9d23061e01b186bfce2cef6bc65a52a5f7fd`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d19df182cbee156b010b04853280b7c12519c2b2a73a5d9a80ae357c814c67`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e4aef08d7bba47a53a2cdfea2260f5792c1fdb440a5ad4ff982730170aa3deb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb8badc11acca1d928d62f328aa0f3707584a4655e9abfa03e3b1b697d59a65`

```dockerfile
```

-	Layers:
	-	`sha256:e3cd06dd05bb0a25b9621e25ea152cd6cffebb5eff99e2740970497eaafedfd3`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.3-linux`

```console
$ docker pull nats@sha256:1b5a0a665cbe50a4ea28e8a82cf809b26cee5027d1fcaf8682fadf8f385fdf29
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

### `nats:2.14.3-linux` - linux; amd64

```console
$ docker pull nats@sha256:da52c7cd2dd8cfbfd7d2dfb251b761e42dbfd6fe0acb09fd26cbb42bdddb2866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6857592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ccfa5190b3b463a3fcf96e85c57584707cb0e37e977effc0b13df38ad27da`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:13:56 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:56 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:13:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:001b0b866410b42b38bcb2e428951af42433891ff425dfcce0b3a53cf93d9cf5`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.9 MB (6857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301e2bd5843dce0ae9f53e3b56e505349c98b58f06c463430d25b5c5ff3d2ac`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4e6b9bd23e99f1e6893cbc2298ff6542ff362ac45479424f0cbbaa44e0bd7932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b91a2a2149df4bdf026d1ba840708ff2f744d4552979b6f5238e32d4b9fadd`

```dockerfile
```

-	Layers:
	-	`sha256:f2654502a1c07929b5dba813de85a6fecf099bd5b4e5dc0304f5bffb9a55374a`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f954b0114100cc6b04d48371743c840445bbd9d9cd58fd347d548df20fb81377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc68893e7b073ba43eb1643ffef18c78a2bcde561b9df87690e4c25b31729d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:087a70319659349faa0bc66d2f258c634f201af06cf4cd72fd052fe0f1741923`  
		Last Modified: Mon, 29 Jun 2026 15:45:00 GMT  
		Size: 6.6 MB (6591390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48bfacc9913ae01cc25da4a4e0b5b45dd8572ebef94eb75ee659e643ca668f`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2ddfb53928614b91b72d029bf8c1fe2c18c9323525cddd2435738502af8f535f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c648adf5a8076bdff845afbe972feb29cbce83a045fc1fa7a6407350edd450`

```dockerfile
```

-	Layers:
	-	`sha256:f18d91a70c6190eda91e68db672ccbc0be90eca9e3a3cbca1053dac4180c85bb`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5acf1bcd52c9815e894b475e74896d5c20d20f75dc1d0a4609284c356a23e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eaac6cac973cc88e6d44cfa8e4fa97db877aa382eca9ca11a3aabdc71efaa4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95cb78be6f3eb15e97acc3a341503927e5ccafbd12a09b4a1b82fbb89f4787b5`  
		Last Modified: Mon, 29 Jun 2026 15:45:01 GMT  
		Size: 6.6 MB (6580972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce96a7f9a07f1a57504be91420ffc8fe2f13ee198161d2b34cfa5461201d23c9`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7350f027d99946847895026cb1af3842bdad2563af2c7a4902c947e3e5859335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365d446dc11c95971d0b41e292ef423e0863365d7c070019c54d2c193b476ff`

```dockerfile
```

-	Layers:
	-	`sha256:0d8192ce2954c6a959615d982ceaa8825bd46cf89ead122b5706cc29fcf8bd71`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e15191f85a79618d9811e8747e99ac98b0a40bfaae0aaaa5001bb1230c1d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6207675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2b8f5a6e48a97cd470606ae3bf871c5e7a728291b699ed0fc6ade464b4cd4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ceb26b4c7119501bb3160d6cbbe50dce6ca269cc3bc37d3bfb9a8d65ab54e83e`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.2 MB (6207167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a970c139d6bb37d99b808c536d15fdfb2452430180d1906126f13f7c0e3e65c8`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-linux` - unknown; unknown

```console
$ docker pull nats@sha256:dbb4f985f00b8ed1cf158bbc14683f3982c6af4dbbd8a11fb368833ce8ab40d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762707c4a125db65916d8207dfc41bd88cb661dfd73431bef3936beaa1b6e79`

```dockerfile
```

-	Layers:
	-	`sha256:6d1ce7246188626d86f106948c8c45d6673d92d8b12bc55a2f76ad1a4a77c06b`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:0d2f692536149ac22566cf1b8c8c155bbf8704b0219606b603d37a2eb62f66a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6271147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5853d65dc9c9039e59f599fe9d6264c1b4b775d3ec6a9efaefa2487a1b2910c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:46 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:094159f217313d715a9c9416ce56b6efb6774fae53d0a118eb72c19dd5050f69`  
		Last Modified: Mon, 29 Jun 2026 15:45:02 GMT  
		Size: 6.3 MB (6270639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1d383fd4674e2d350a56d40d9d7a4a018dcdcac31733be7d84231bbad1d5b`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7388f5e7e39dd5b070cb36fd9cf62973a1dbe1673ae86098ed3504c78e1ef328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a70cea4e571b8e5e9bb3f1775b350266ece5ba0911b4910d792e2f5c7a8522`

```dockerfile
```

-	Layers:
	-	`sha256:c683a72a6137cd681254bab9a60e1a450a3a8e636d80bcccb57e77942df0b512`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-linux` - linux; s390x

```console
$ docker pull nats@sha256:fa31a78cc1dfc74ac5954db2d0fabe8025d55442dd778436f11eb45bbad212b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a751449230c715131c826c9e954f6c6faab06fed9d6ac6ef617518f68b0f57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c051b099bef1cbfeba54872473e4a7281c4a402d9f0b7c1bdf892e5e21ea8c51`  
		Last Modified: Mon, 29 Jun 2026 15:45:04 GMT  
		Size: 6.7 MB (6666239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd00d66579c55de314f0aa7536b46c9471486f908c26ae17a7d930bfdd9fb9`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-linux` - unknown; unknown

```console
$ docker pull nats@sha256:6e482d7d215597ddb64e6a49fb2d97ed5f170b063872e7b945de9574375342eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa169f897fcb8ad6d1b168458e6f22434b580cca5dd468838bbd781ec75f31a`

```dockerfile
```

-	Layers:
	-	`sha256:cfe01b7f8ddd174d7457c698713d2616d4d35273045161e7a898b8d8a593e3f4`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.3-nanoserver`

```console
$ docker pull nats@sha256:1d52723019944547c28befc6831cf54a194fe6cf5da2cbe5d83dada671148eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14.3-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:9f0daa17d5998a047f470ea9d8842dc0eb687557782823b3fea2bc5538aeaf23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131054329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b328dd4c47b0486963aab87b1d33d09cc56b17a894d7d1f8cbff35d6514a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:13:42 GMT
RUN cmd /S /C #(nop) COPY file:d28b1675c385af4d7600302dadf40a3bf46cd73b4ca42fe37500427a26b9b480 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:13:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:13:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:13:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:13:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3906542123b76df88980ceb04181b631e9922c06a031cb9d6c343bc4fc335b59`  
		Last Modified: Mon, 29 Jun 2026 20:13:57 GMT  
		Size: 7.1 MB (7050935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0464c24aec36583186ddd00d659a44cbfbe8eb6967595e263922cee114f11541`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e247b1ab45847502319a775832f1e37efd8e27edab85850c1cd39355d7c59a`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bca692b6b90a8e7b2b7d9ea755343336ec76f096b7f3eef575a86f50e64dc5`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3557d9ac8171b21f42a1bee80b244527a6000a38cb1673347a20e01f26387`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.3-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:1d52723019944547c28befc6831cf54a194fe6cf5da2cbe5d83dada671148eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14.3-nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:9f0daa17d5998a047f470ea9d8842dc0eb687557782823b3fea2bc5538aeaf23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131054329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b328dd4c47b0486963aab87b1d33d09cc56b17a894d7d1f8cbff35d6514a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:13:42 GMT
RUN cmd /S /C #(nop) COPY file:d28b1675c385af4d7600302dadf40a3bf46cd73b4ca42fe37500427a26b9b480 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:13:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:13:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:13:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:13:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3906542123b76df88980ceb04181b631e9922c06a031cb9d6c343bc4fc335b59`  
		Last Modified: Mon, 29 Jun 2026 20:13:57 GMT  
		Size: 7.1 MB (7050935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0464c24aec36583186ddd00d659a44cbfbe8eb6967595e263922cee114f11541`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e247b1ab45847502319a775832f1e37efd8e27edab85850c1cd39355d7c59a`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bca692b6b90a8e7b2b7d9ea755343336ec76f096b7f3eef575a86f50e64dc5`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3557d9ac8171b21f42a1bee80b244527a6000a38cb1673347a20e01f26387`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.3-scratch`

```console
$ docker pull nats@sha256:1b5a0a665cbe50a4ea28e8a82cf809b26cee5027d1fcaf8682fadf8f385fdf29
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

### `nats:2.14.3-scratch` - linux; amd64

```console
$ docker pull nats@sha256:da52c7cd2dd8cfbfd7d2dfb251b761e42dbfd6fe0acb09fd26cbb42bdddb2866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6857592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ccfa5190b3b463a3fcf96e85c57584707cb0e37e977effc0b13df38ad27da`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:13:56 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:56 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:13:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:001b0b866410b42b38bcb2e428951af42433891ff425dfcce0b3a53cf93d9cf5`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.9 MB (6857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301e2bd5843dce0ae9f53e3b56e505349c98b58f06c463430d25b5c5ff3d2ac`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4e6b9bd23e99f1e6893cbc2298ff6542ff362ac45479424f0cbbaa44e0bd7932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b91a2a2149df4bdf026d1ba840708ff2f744d4552979b6f5238e32d4b9fadd`

```dockerfile
```

-	Layers:
	-	`sha256:f2654502a1c07929b5dba813de85a6fecf099bd5b4e5dc0304f5bffb9a55374a`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f954b0114100cc6b04d48371743c840445bbd9d9cd58fd347d548df20fb81377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc68893e7b073ba43eb1643ffef18c78a2bcde561b9df87690e4c25b31729d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:087a70319659349faa0bc66d2f258c634f201af06cf4cd72fd052fe0f1741923`  
		Last Modified: Mon, 29 Jun 2026 15:45:00 GMT  
		Size: 6.6 MB (6591390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48bfacc9913ae01cc25da4a4e0b5b45dd8572ebef94eb75ee659e643ca668f`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2ddfb53928614b91b72d029bf8c1fe2c18c9323525cddd2435738502af8f535f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c648adf5a8076bdff845afbe972feb29cbce83a045fc1fa7a6407350edd450`

```dockerfile
```

-	Layers:
	-	`sha256:f18d91a70c6190eda91e68db672ccbc0be90eca9e3a3cbca1053dac4180c85bb`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5acf1bcd52c9815e894b475e74896d5c20d20f75dc1d0a4609284c356a23e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eaac6cac973cc88e6d44cfa8e4fa97db877aa382eca9ca11a3aabdc71efaa4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95cb78be6f3eb15e97acc3a341503927e5ccafbd12a09b4a1b82fbb89f4787b5`  
		Last Modified: Mon, 29 Jun 2026 15:45:01 GMT  
		Size: 6.6 MB (6580972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce96a7f9a07f1a57504be91420ffc8fe2f13ee198161d2b34cfa5461201d23c9`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7350f027d99946847895026cb1af3842bdad2563af2c7a4902c947e3e5859335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365d446dc11c95971d0b41e292ef423e0863365d7c070019c54d2c193b476ff`

```dockerfile
```

-	Layers:
	-	`sha256:0d8192ce2954c6a959615d982ceaa8825bd46cf89ead122b5706cc29fcf8bd71`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e15191f85a79618d9811e8747e99ac98b0a40bfaae0aaaa5001bb1230c1d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6207675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2b8f5a6e48a97cd470606ae3bf871c5e7a728291b699ed0fc6ade464b4cd4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ceb26b4c7119501bb3160d6cbbe50dce6ca269cc3bc37d3bfb9a8d65ab54e83e`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.2 MB (6207167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a970c139d6bb37d99b808c536d15fdfb2452430180d1906126f13f7c0e3e65c8`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:dbb4f985f00b8ed1cf158bbc14683f3982c6af4dbbd8a11fb368833ce8ab40d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762707c4a125db65916d8207dfc41bd88cb661dfd73431bef3936beaa1b6e79`

```dockerfile
```

-	Layers:
	-	`sha256:6d1ce7246188626d86f106948c8c45d6673d92d8b12bc55a2f76ad1a4a77c06b`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:0d2f692536149ac22566cf1b8c8c155bbf8704b0219606b603d37a2eb62f66a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6271147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5853d65dc9c9039e59f599fe9d6264c1b4b775d3ec6a9efaefa2487a1b2910c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:46 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:094159f217313d715a9c9416ce56b6efb6774fae53d0a118eb72c19dd5050f69`  
		Last Modified: Mon, 29 Jun 2026 15:45:02 GMT  
		Size: 6.3 MB (6270639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1d383fd4674e2d350a56d40d9d7a4a018dcdcac31733be7d84231bbad1d5b`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7388f5e7e39dd5b070cb36fd9cf62973a1dbe1673ae86098ed3504c78e1ef328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a70cea4e571b8e5e9bb3f1775b350266ece5ba0911b4910d792e2f5c7a8522`

```dockerfile
```

-	Layers:
	-	`sha256:c683a72a6137cd681254bab9a60e1a450a3a8e636d80bcccb57e77942df0b512`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.14.3-scratch` - linux; s390x

```console
$ docker pull nats@sha256:fa31a78cc1dfc74ac5954db2d0fabe8025d55442dd778436f11eb45bbad212b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a751449230c715131c826c9e954f6c6faab06fed9d6ac6ef617518f68b0f57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c051b099bef1cbfeba54872473e4a7281c4a402d9f0b7c1bdf892e5e21ea8c51`  
		Last Modified: Mon, 29 Jun 2026 15:45:04 GMT  
		Size: 6.7 MB (6666239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd00d66579c55de314f0aa7536b46c9471486f908c26ae17a7d930bfdd9fb9`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.14.3-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6e482d7d215597ddb64e6a49fb2d97ed5f170b063872e7b945de9574375342eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa169f897fcb8ad6d1b168458e6f22434b580cca5dd468838bbd781ec75f31a`

```dockerfile
```

-	Layers:
	-	`sha256:cfe01b7f8ddd174d7457c698713d2616d4d35273045161e7a898b8d8a593e3f4`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.14.3-windowsservercore`

```console
$ docker pull nats@sha256:f701716476a8d968bd766320239d98d7f973ebaaa7a6f960f65648bda132229e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14.3-windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:2c61006c6743420a33c3ade658d600d9b81f09a86df8c44fe02741a71d196d7f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140052973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782541001e22820de00703de294e85e7c622fc9ea85c9030e8fda96177afa0cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 29 Jun 2026 19:16:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Jun 2026 19:16:31 GMT
ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 19:16:32 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:16:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:16:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.3/nats-server-v2.14.3-windows-amd64.zip
# Mon, 29 Jun 2026 19:16:37 GMT
ENV NATS_SERVER_SHASUM=94e338d742761272e31eab1efb1f767eac3a2e56e4c05a7933c65a73fe95a27b
# Mon, 29 Jun 2026 19:17:35 GMT
RUN Set-PSDebug -Trace 2
# Mon, 29 Jun 2026 19:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 29 Jun 2026 19:18:06 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 19:18:08 GMT
EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 19:18:09 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 19:18:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac87f215828b12e2044c46470b221ea4307d0fc11cf8280e12474587a59317d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff6f7da74f9e652f79bc8278319981b268148b1548a3ef4220d3ccbe4b5473d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e85164857353b52ed850cc83049bc199678edaed484f95d1e38aa0a4f1b525b`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706cc542b32b6c088b1b95499c39a0c6f9dbe749f47087a0cd668545100147ba`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25bcf16bfd2387cc38d31f75eeac32290dada9d452e1f50b902530775f1c0ff`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aecb5ee131c5c835ec5c73c2ad224bf1e9c3ede99efeca9eec6a270f5c22b1`  
		Last Modified: Mon, 29 Jun 2026 19:18:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f1b98897859ea619b08dd0f0db49b009771052a13d263d4980a21c40901f2`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 496.7 KB (496723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784da3b63359a7bbb87eb47bb8a637b409b418e94af977bf3c24722cbc2ec89e`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 7.4 MB (7417113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae24643aacc8edba76b5661a3358a9461f9fda9a7d1f0fccaeca461dfb074a23`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe52ddb42630f70fd61331adf5e83118d27382c4d3922882adb2d981105bac94`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087e85133498df0eb7d45b8bc9353ec3fa1fc98964b2f88c33152ca73bf5abd6`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9462b672f1e05436ba0020f6b3b71b8db8b844d5c5183c1088c29d06d39df1be`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.14.3-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:f701716476a8d968bd766320239d98d7f973ebaaa7a6f960f65648bda132229e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:2.14.3-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:2c61006c6743420a33c3ade658d600d9b81f09a86df8c44fe02741a71d196d7f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140052973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782541001e22820de00703de294e85e7c622fc9ea85c9030e8fda96177afa0cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 29 Jun 2026 19:16:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Jun 2026 19:16:31 GMT
ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 19:16:32 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:16:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:16:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.3/nats-server-v2.14.3-windows-amd64.zip
# Mon, 29 Jun 2026 19:16:37 GMT
ENV NATS_SERVER_SHASUM=94e338d742761272e31eab1efb1f767eac3a2e56e4c05a7933c65a73fe95a27b
# Mon, 29 Jun 2026 19:17:35 GMT
RUN Set-PSDebug -Trace 2
# Mon, 29 Jun 2026 19:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 29 Jun 2026 19:18:06 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 19:18:08 GMT
EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 19:18:09 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 19:18:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac87f215828b12e2044c46470b221ea4307d0fc11cf8280e12474587a59317d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff6f7da74f9e652f79bc8278319981b268148b1548a3ef4220d3ccbe4b5473d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e85164857353b52ed850cc83049bc199678edaed484f95d1e38aa0a4f1b525b`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706cc542b32b6c088b1b95499c39a0c6f9dbe749f47087a0cd668545100147ba`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25bcf16bfd2387cc38d31f75eeac32290dada9d452e1f50b902530775f1c0ff`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aecb5ee131c5c835ec5c73c2ad224bf1e9c3ede99efeca9eec6a270f5c22b1`  
		Last Modified: Mon, 29 Jun 2026 19:18:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f1b98897859ea619b08dd0f0db49b009771052a13d263d4980a21c40901f2`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 496.7 KB (496723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784da3b63359a7bbb87eb47bb8a637b409b418e94af977bf3c24722cbc2ec89e`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 7.4 MB (7417113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae24643aacc8edba76b5661a3358a9461f9fda9a7d1f0fccaeca461dfb074a23`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe52ddb42630f70fd61331adf5e83118d27382c4d3922882adb2d981105bac94`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087e85133498df0eb7d45b8bc9353ec3fa1fc98964b2f88c33152ca73bf5abd6`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9462b672f1e05436ba0020f6b3b71b8db8b844d5c5183c1088c29d06d39df1be`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:c11af972c99ae542de8925e6a7d9c533aa1eb039660420d2074beed6089b3bf0
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
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4e53bdfe4a9d810005abaf974dd9a12374c9cd187fa6be4622eff6a73b9e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8ea3792d3865371b24b0504e2a7a61140487a85c1289a56e6b0a414f3aa451`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fb591416c4f81c00164a6df7c9a0df260683e8939dad253a229dad6006eed7`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 7.0 MB (7001975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a94003f98dbb2cec821705d1615ee3fabdb6278a14a965fad556f00935df4e`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca954dfa8945adfa8283aac38370a786f5ed56c79b3a242cdc0a7717732e4c01`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d2617716222bd82abc599cbe8277f98292977c0dfdd769178f6be9d0fdbfafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf691e94e06290aeb75516eb80f45749858c6ac66c0462f375e5b23f89c0f28`

```dockerfile
```

-	Layers:
	-	`sha256:051ab4a8c59747a86c2b341f78f881dcb5ce383e1adb18760b2e37658493f9f3`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:13a3f0e29c614c6b948bac76e8511e103dae75a1f3aafb215d49defef515bda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10202964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b0bb66ac4162fc21cb64f4e23f7840a339f47c9c6e9fe68e07f879189b36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c57aa7f84636f8b81c22758ea4a628036299dea2750a000eb5de6220234b418`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 7.0 MB (6992381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b307022eba60d3fa1d5f402e6c270a824a7c22733d6b54b89a11d8e47f5df06`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979223c0d164e45ff3d261730284785ca49e194cd773a37086da9bdd856159e`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:cc9db77acad1e638c9d195fe27bf9cb73a582f1d6c8a48de4aac85d42fe8b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e4eea65b1e82754ac2719f2026f89bf4d253eda69a68c1c7a0753cc424985`

```dockerfile
```

-	Layers:
	-	`sha256:be67ebf23efa9ed614c3e6ecbd8dbfe60c3c196c67672894c62befc4102a028d`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:064222a09af7b194af6760d6089aa9ebd93fe7b8136ec2193ddb72dd78d8bd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10740987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b422fa2e0339d3eb86f18cdd7040198afd726fadc2c6c0f499eff9c9038c9926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d45f995edc436f16aee98c90da4e281a787ba379a91c7b812155f24b01f240c`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 6.6 MB (6619532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721188e517e99c1592046fd1c1f9d23061e01b186bfce2cef6bc65a52a5f7fd`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d19df182cbee156b010b04853280b7c12519c2b2a73a5d9a80ae357c814c67`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:e4aef08d7bba47a53a2cdfea2260f5792c1fdb440a5ad4ff982730170aa3deb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb8badc11acca1d928d62f328aa0f3707584a4655e9abfa03e3b1b697d59a65`

```dockerfile
```

-	Layers:
	-	`sha256:e3cd06dd05bb0a25b9621e25ea152cd6cffebb5eff99e2740970497eaafedfd3`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:c11af972c99ae542de8925e6a7d9c533aa1eb039660420d2074beed6089b3bf0
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
$ docker pull nats@sha256:a42e284980d105c1b668d553175b4c7abc9b7187c5e9859baf4f1d564772b85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11056026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bc12a71290912ecf2ffb2e5df45be9ae532fef1b8240aef6102891d375ce25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:20 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328794545e9bf2e5cced545a15e65e783306486272234d91c5d2719d0ec9b70`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 7.3 MB (7267461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266119c4af18be04cdea3885753ddc31a6343f4a3cdd22439d75ab32a2587dbb`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ff0c17447e0330a97ae8ec95d6fdcadcd8cb8991d6c548858ec3d69a3c23a2`  
		Last Modified: Mon, 29 Jun 2026 19:11:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2f3d3942c5b8e78340ff935ef0179cde1967969ba70ca4664fc6dfaaea0a4ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac360c9f1c2562befb519baafc614b6161d4ceee74f7701c04b24cb07d223f`

```dockerfile
```

-	Layers:
	-	`sha256:564b644082e6223b0d2da321c2a6a1e4337ba6eee056219eeed745c943604b09`  
		Last Modified: Mon, 29 Jun 2026 19:11:25 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:d4e53bdfe4a9d810005abaf974dd9a12374c9cd187fa6be4622eff6a73b9e2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8ea3792d3865371b24b0504e2a7a61140487a85c1289a56e6b0a414f3aa451`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:53 GMT
ADD alpine-minirootfs-3.22.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:53 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:42 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:8efcda622ba07f4da6b9309a34f4650a7a052a1d29a2fc346284c2c1b0899202`  
		Last Modified: Mon, 22 Jun 2026 19:19:58 GMT  
		Size: 3.5 MB (3494800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fb591416c4f81c00164a6df7c9a0df260683e8939dad253a229dad6006eed7`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 7.0 MB (7001975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a94003f98dbb2cec821705d1615ee3fabdb6278a14a965fad556f00935df4e`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca954dfa8945adfa8283aac38370a786f5ed56c79b3a242cdc0a7717732e4c01`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d2617716222bd82abc599cbe8277f98292977c0dfdd769178f6be9d0fdbfafc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf691e94e06290aeb75516eb80f45749858c6ac66c0462f375e5b23f89c0f28`

```dockerfile
```

-	Layers:
	-	`sha256:051ab4a8c59747a86c2b341f78f881dcb5ce383e1adb18760b2e37658493f9f3`  
		Last Modified: Mon, 29 Jun 2026 19:12:47 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:13a3f0e29c614c6b948bac76e8511e103dae75a1f3aafb215d49defef515bda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10202964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b0bb66ac4162fc21cb64f4e23f7840a339f47c9c6e9fe68e07f879189b36aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:47 GMT
ADD alpine-minirootfs-3.22.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:19 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:19 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:276ca41f8e7974c0de50f2551aabece03d11f231f68ab5c6c5051410e0d8c2e7`  
		Last Modified: Mon, 22 Jun 2026 12:03:28 GMT  
		Size: 3.2 MB (3209612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c57aa7f84636f8b81c22758ea4a628036299dea2750a000eb5de6220234b418`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 7.0 MB (6992381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b307022eba60d3fa1d5f402e6c270a824a7c22733d6b54b89a11d8e47f5df06`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979223c0d164e45ff3d261730284785ca49e194cd773a37086da9bdd856159e`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:cc9db77acad1e638c9d195fe27bf9cb73a582f1d6c8a48de4aac85d42fe8b288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e4eea65b1e82754ac2719f2026f89bf4d253eda69a68c1c7a0753cc424985`

```dockerfile
```

-	Layers:
	-	`sha256:be67ebf23efa9ed614c3e6ecbd8dbfe60c3c196c67672894c62befc4102a028d`  
		Last Modified: Mon, 29 Jun 2026 19:12:24 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:064222a09af7b194af6760d6089aa9ebd93fe7b8136ec2193ddb72dd78d8bd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10740987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b422fa2e0339d3eb86f18cdd7040198afd726fadc2c6c0f499eff9c9038c9926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:12:29 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:12:29 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d45f995edc436f16aee98c90da4e281a787ba379a91c7b812155f24b01f240c`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 6.6 MB (6619532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6721188e517e99c1592046fd1c1f9d23061e01b186bfce2cef6bc65a52a5f7fd`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d19df182cbee156b010b04853280b7c12519c2b2a73a5d9a80ae357c814c67`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:e4aef08d7bba47a53a2cdfea2260f5792c1fdb440a5ad4ff982730170aa3deb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb8badc11acca1d928d62f328aa0f3707584a4655e9abfa03e3b1b697d59a65`

```dockerfile
```

-	Layers:
	-	`sha256:e3cd06dd05bb0a25b9621e25ea152cd6cffebb5eff99e2740970497eaafedfd3`  
		Last Modified: Mon, 29 Jun 2026 19:12:33 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:4cf2613394dd476c98defc5949b0112c58104e69fdedcea45623d8a0500232ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10404101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e46a96841a5e8a1a059d0b1f2e9f7ef331d2f66c708831b9b3b20e44dd08b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.22.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:24 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9cefbc3ea4c22353ee0ff5d3bed351562709ff27de0432db57d479a5f81bb73a`  
		Last Modified: Mon, 22 Jun 2026 12:03:29 GMT  
		Size: 3.7 MB (3719232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25f5c4125e4e65d2291719a7301077f73955ea8a486793cdff158dd5b38f2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:31 GMT  
		Size: 6.7 MB (6683899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b5b2751240aedcffc66cd15114fdf1dc1edbd92583859340ff12750f05eee9`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed46b6e66255726a7da20746e5335e6cfd61adcb302045bacb12653a3fb48796`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:911ea621f7b7bdc2849cb0bf7c5d77fc52979adadcf778fe1895cca4f30c7d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1733bfcfab9d319252505097d1b8090505f3d0cfd8707c419d6e05613fec1bc7`

```dockerfile
```

-	Layers:
	-	`sha256:95525b415b6f44f224df4f52f3673394dacc4e6da64f4cdd96d7f69ed6227977`  
		Last Modified: Mon, 29 Jun 2026 19:11:30 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:1b40e5777ca5e42f1a686c44c10756b93b42ecf9828e34535c3362c661ffe383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10715340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e765891c29d76f069d9a16b30c6de0b6d5dd98fec8bc48ac2a30e38412754a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:15 GMT
ADD alpine-minirootfs-3.22.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:15 GMT
CMD ["/bin/sh"]
# Mon, 29 Jun 2026 19:11:39 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:11:39 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='1759b6a0ddebade9471b7c02891dfaa8c73b526c6f3ce391d4e21ec3eceffab8' ;;     armhf) natsArch='arm6'; sha256='95d285b170a1417121fbb62ec5c9b618552855d072f48be86cd4d11544227704' ;;     armv7) natsArch='arm7'; sha256='d70d6de7ad0d587ad3047f4516a054f64b693edb79894d7ec0a2d176be31f6cf' ;;     x86_64) natsArch='amd64'; sha256='f3d0c820c749f81d717310fb00d4903919e70e3e66b268bd352a088b9788eb93' ;;     x86) natsArch='386'; sha256='071d031273136987af2da68103bd1080fbdd463b244c703388d0164726b17357' ;;     s390x) natsArch='s390x'; sha256='be525fec7cf3dac23e9617ca2b4b3767e79b1f684a456f3a2e85e1b3d40a6da9' ;;     ppc64le) natsArch='ppc64le'; sha256='12b4ecc73e7023b501a374913c7e70f7487107743dbab7cc7da627348b87f9d3' ;;     loong64) natsArch='loong64'; sha256='9a69c1fd01d290695cef2e33412e0e3ad4fe8e4af03faf0be137cd7e287bd55b' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 29 Jun 2026 19:11:39 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 29 Jun 2026 19:11:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Jun 2026 19:11:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5cc76dd142694657b89f934ffd4984b6a34734e31f9cfb8fd5e05181e6a23101`  
		Last Modified: Mon, 22 Jun 2026 12:03:27 GMT  
		Size: 3.6 MB (3637085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771170401b4070c1dd173335f21881887683088a98679a5ad80585b2067bc1e2`  
		Last Modified: Mon, 29 Jun 2026 19:11:52 GMT  
		Size: 7.1 MB (7077286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b09c93cbe4710a2235d033d228f7973210a7b7a93081d020e649a8ee2b2c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcceda063df49f85902f8d00b7d2a5de091e8f90c478cb5943dfef623befe7c`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5256630d95ea8d78de9df1f862aa8468e2618c70446f2b2b34a479e31cc09d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd0c6ed24bd266521a1aeef3a2d01fac948384e4dc7e53cf92e059d06220860`

```dockerfile
```

-	Layers:
	-	`sha256:e4110a5e17fc15bf29266ec20af296d24defb647f46623a029d38782d3188aa6`  
		Last Modified: Mon, 29 Jun 2026 19:11:51 GMT  
		Size: 15.4 KB (15404 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:7ff2e641c33dbdb0dd13a943ba0b70d841b71275c607baa53ef9b8661f0b2d8c
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
	-	windows version 10.0.20348.5256; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:da52c7cd2dd8cfbfd7d2dfb251b761e42dbfd6fe0acb09fd26cbb42bdddb2866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6857592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ccfa5190b3b463a3fcf96e85c57584707cb0e37e977effc0b13df38ad27da`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:13:56 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:56 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:13:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:001b0b866410b42b38bcb2e428951af42433891ff425dfcce0b3a53cf93d9cf5`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.9 MB (6857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301e2bd5843dce0ae9f53e3b56e505349c98b58f06c463430d25b5c5ff3d2ac`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:4e6b9bd23e99f1e6893cbc2298ff6542ff362ac45479424f0cbbaa44e0bd7932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b91a2a2149df4bdf026d1ba840708ff2f744d4552979b6f5238e32d4b9fadd`

```dockerfile
```

-	Layers:
	-	`sha256:f2654502a1c07929b5dba813de85a6fecf099bd5b4e5dc0304f5bffb9a55374a`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:f954b0114100cc6b04d48371743c840445bbd9d9cd58fd347d548df20fb81377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc68893e7b073ba43eb1643ffef18c78a2bcde561b9df87690e4c25b31729d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:087a70319659349faa0bc66d2f258c634f201af06cf4cd72fd052fe0f1741923`  
		Last Modified: Mon, 29 Jun 2026 15:45:00 GMT  
		Size: 6.6 MB (6591390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48bfacc9913ae01cc25da4a4e0b5b45dd8572ebef94eb75ee659e643ca668f`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:2ddfb53928614b91b72d029bf8c1fe2c18c9323525cddd2435738502af8f535f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c648adf5a8076bdff845afbe972feb29cbce83a045fc1fa7a6407350edd450`

```dockerfile
```

-	Layers:
	-	`sha256:f18d91a70c6190eda91e68db672ccbc0be90eca9e3a3cbca1053dac4180c85bb`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:5acf1bcd52c9815e894b475e74896d5c20d20f75dc1d0a4609284c356a23e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eaac6cac973cc88e6d44cfa8e4fa97db877aa382eca9ca11a3aabdc71efaa4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95cb78be6f3eb15e97acc3a341503927e5ccafbd12a09b4a1b82fbb89f4787b5`  
		Last Modified: Mon, 29 Jun 2026 15:45:01 GMT  
		Size: 6.6 MB (6580972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce96a7f9a07f1a57504be91420ffc8fe2f13ee198161d2b34cfa5461201d23c9`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:7350f027d99946847895026cb1af3842bdad2563af2c7a4902c947e3e5859335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365d446dc11c95971d0b41e292ef423e0863365d7c070019c54d2c193b476ff`

```dockerfile
```

-	Layers:
	-	`sha256:0d8192ce2954c6a959615d982ceaa8825bd46cf89ead122b5706cc29fcf8bd71`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e15191f85a79618d9811e8747e99ac98b0a40bfaae0aaaa5001bb1230c1d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6207675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2b8f5a6e48a97cd470606ae3bf871c5e7a728291b699ed0fc6ade464b4cd4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ceb26b4c7119501bb3160d6cbbe50dce6ca269cc3bc37d3bfb9a8d65ab54e83e`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.2 MB (6207167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a970c139d6bb37d99b808c536d15fdfb2452430180d1906126f13f7c0e3e65c8`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:dbb4f985f00b8ed1cf158bbc14683f3982c6af4dbbd8a11fb368833ce8ab40d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762707c4a125db65916d8207dfc41bd88cb661dfd73431bef3936beaa1b6e79`

```dockerfile
```

-	Layers:
	-	`sha256:6d1ce7246188626d86f106948c8c45d6673d92d8b12bc55a2f76ad1a4a77c06b`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:0d2f692536149ac22566cf1b8c8c155bbf8704b0219606b603d37a2eb62f66a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6271147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5853d65dc9c9039e59f599fe9d6264c1b4b775d3ec6a9efaefa2487a1b2910c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:46 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:094159f217313d715a9c9416ce56b6efb6774fae53d0a118eb72c19dd5050f69`  
		Last Modified: Mon, 29 Jun 2026 15:45:02 GMT  
		Size: 6.3 MB (6270639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1d383fd4674e2d350a56d40d9d7a4a018dcdcac31733be7d84231bbad1d5b`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:7388f5e7e39dd5b070cb36fd9cf62973a1dbe1673ae86098ed3504c78e1ef328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a70cea4e571b8e5e9bb3f1775b350266ece5ba0911b4910d792e2f5c7a8522`

```dockerfile
```

-	Layers:
	-	`sha256:c683a72a6137cd681254bab9a60e1a450a3a8e636d80bcccb57e77942df0b512`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:fa31a78cc1dfc74ac5954db2d0fabe8025d55442dd778436f11eb45bbad212b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a751449230c715131c826c9e954f6c6faab06fed9d6ac6ef617518f68b0f57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c051b099bef1cbfeba54872473e4a7281c4a402d9f0b7c1bdf892e5e21ea8c51`  
		Last Modified: Mon, 29 Jun 2026 15:45:04 GMT  
		Size: 6.7 MB (6666239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd00d66579c55de314f0aa7536b46c9471486f908c26ae17a7d930bfdd9fb9`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:6e482d7d215597ddb64e6a49fb2d97ed5f170b063872e7b945de9574375342eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa169f897fcb8ad6d1b168458e6f22434b580cca5dd468838bbd781ec75f31a`

```dockerfile
```

-	Layers:
	-	`sha256:cfe01b7f8ddd174d7457c698713d2616d4d35273045161e7a898b8d8a593e3f4`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:9f0daa17d5998a047f470ea9d8842dc0eb687557782823b3fea2bc5538aeaf23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131054329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b328dd4c47b0486963aab87b1d33d09cc56b17a894d7d1f8cbff35d6514a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:13:42 GMT
RUN cmd /S /C #(nop) COPY file:d28b1675c385af4d7600302dadf40a3bf46cd73b4ca42fe37500427a26b9b480 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:13:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:13:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:13:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:13:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3906542123b76df88980ceb04181b631e9922c06a031cb9d6c343bc4fc335b59`  
		Last Modified: Mon, 29 Jun 2026 20:13:57 GMT  
		Size: 7.1 MB (7050935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0464c24aec36583186ddd00d659a44cbfbe8eb6967595e263922cee114f11541`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e247b1ab45847502319a775832f1e37efd8e27edab85850c1cd39355d7c59a`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bca692b6b90a8e7b2b7d9ea755343336ec76f096b7f3eef575a86f50e64dc5`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3557d9ac8171b21f42a1bee80b244527a6000a38cb1673347a20e01f26387`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:1b5a0a665cbe50a4ea28e8a82cf809b26cee5027d1fcaf8682fadf8f385fdf29
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
$ docker pull nats@sha256:da52c7cd2dd8cfbfd7d2dfb251b761e42dbfd6fe0acb09fd26cbb42bdddb2866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6857592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ccfa5190b3b463a3fcf96e85c57584707cb0e37e977effc0b13df38ad27da`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:13:56 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:56 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:13:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:001b0b866410b42b38bcb2e428951af42433891ff425dfcce0b3a53cf93d9cf5`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.9 MB (6857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301e2bd5843dce0ae9f53e3b56e505349c98b58f06c463430d25b5c5ff3d2ac`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:4e6b9bd23e99f1e6893cbc2298ff6542ff362ac45479424f0cbbaa44e0bd7932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b91a2a2149df4bdf026d1ba840708ff2f744d4552979b6f5238e32d4b9fadd`

```dockerfile
```

-	Layers:
	-	`sha256:f2654502a1c07929b5dba813de85a6fecf099bd5b4e5dc0304f5bffb9a55374a`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:f954b0114100cc6b04d48371743c840445bbd9d9cd58fd347d548df20fb81377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc68893e7b073ba43eb1643ffef18c78a2bcde561b9df87690e4c25b31729d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:087a70319659349faa0bc66d2f258c634f201af06cf4cd72fd052fe0f1741923`  
		Last Modified: Mon, 29 Jun 2026 15:45:00 GMT  
		Size: 6.6 MB (6591390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48bfacc9913ae01cc25da4a4e0b5b45dd8572ebef94eb75ee659e643ca668f`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:2ddfb53928614b91b72d029bf8c1fe2c18c9323525cddd2435738502af8f535f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c648adf5a8076bdff845afbe972feb29cbce83a045fc1fa7a6407350edd450`

```dockerfile
```

-	Layers:
	-	`sha256:f18d91a70c6190eda91e68db672ccbc0be90eca9e3a3cbca1053dac4180c85bb`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5acf1bcd52c9815e894b475e74896d5c20d20f75dc1d0a4609284c356a23e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eaac6cac973cc88e6d44cfa8e4fa97db877aa382eca9ca11a3aabdc71efaa4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95cb78be6f3eb15e97acc3a341503927e5ccafbd12a09b4a1b82fbb89f4787b5`  
		Last Modified: Mon, 29 Jun 2026 15:45:01 GMT  
		Size: 6.6 MB (6580972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce96a7f9a07f1a57504be91420ffc8fe2f13ee198161d2b34cfa5461201d23c9`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:7350f027d99946847895026cb1af3842bdad2563af2c7a4902c947e3e5859335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365d446dc11c95971d0b41e292ef423e0863365d7c070019c54d2c193b476ff`

```dockerfile
```

-	Layers:
	-	`sha256:0d8192ce2954c6a959615d982ceaa8825bd46cf89ead122b5706cc29fcf8bd71`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e15191f85a79618d9811e8747e99ac98b0a40bfaae0aaaa5001bb1230c1d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6207675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2b8f5a6e48a97cd470606ae3bf871c5e7a728291b699ed0fc6ade464b4cd4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ceb26b4c7119501bb3160d6cbbe50dce6ca269cc3bc37d3bfb9a8d65ab54e83e`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.2 MB (6207167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a970c139d6bb37d99b808c536d15fdfb2452430180d1906126f13f7c0e3e65c8`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:dbb4f985f00b8ed1cf158bbc14683f3982c6af4dbbd8a11fb368833ce8ab40d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762707c4a125db65916d8207dfc41bd88cb661dfd73431bef3936beaa1b6e79`

```dockerfile
```

-	Layers:
	-	`sha256:6d1ce7246188626d86f106948c8c45d6673d92d8b12bc55a2f76ad1a4a77c06b`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:0d2f692536149ac22566cf1b8c8c155bbf8704b0219606b603d37a2eb62f66a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6271147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5853d65dc9c9039e59f599fe9d6264c1b4b775d3ec6a9efaefa2487a1b2910c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:46 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:094159f217313d715a9c9416ce56b6efb6774fae53d0a118eb72c19dd5050f69`  
		Last Modified: Mon, 29 Jun 2026 15:45:02 GMT  
		Size: 6.3 MB (6270639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1d383fd4674e2d350a56d40d9d7a4a018dcdcac31733be7d84231bbad1d5b`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:7388f5e7e39dd5b070cb36fd9cf62973a1dbe1673ae86098ed3504c78e1ef328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a70cea4e571b8e5e9bb3f1775b350266ece5ba0911b4910d792e2f5c7a8522`

```dockerfile
```

-	Layers:
	-	`sha256:c683a72a6137cd681254bab9a60e1a450a3a8e636d80bcccb57e77942df0b512`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:fa31a78cc1dfc74ac5954db2d0fabe8025d55442dd778436f11eb45bbad212b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a751449230c715131c826c9e954f6c6faab06fed9d6ac6ef617518f68b0f57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c051b099bef1cbfeba54872473e4a7281c4a402d9f0b7c1bdf892e5e21ea8c51`  
		Last Modified: Mon, 29 Jun 2026 15:45:04 GMT  
		Size: 6.7 MB (6666239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd00d66579c55de314f0aa7536b46c9471486f908c26ae17a7d930bfdd9fb9`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:6e482d7d215597ddb64e6a49fb2d97ed5f170b063872e7b945de9574375342eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa169f897fcb8ad6d1b168458e6f22434b580cca5dd468838bbd781ec75f31a`

```dockerfile
```

-	Layers:
	-	`sha256:cfe01b7f8ddd174d7457c698713d2616d4d35273045161e7a898b8d8a593e3f4`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:1d52723019944547c28befc6831cf54a194fe6cf5da2cbe5d83dada671148eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:9f0daa17d5998a047f470ea9d8842dc0eb687557782823b3fea2bc5538aeaf23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131054329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b328dd4c47b0486963aab87b1d33d09cc56b17a894d7d1f8cbff35d6514a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:13:42 GMT
RUN cmd /S /C #(nop) COPY file:d28b1675c385af4d7600302dadf40a3bf46cd73b4ca42fe37500427a26b9b480 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:13:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:13:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:13:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:13:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3906542123b76df88980ceb04181b631e9922c06a031cb9d6c343bc4fc335b59`  
		Last Modified: Mon, 29 Jun 2026 20:13:57 GMT  
		Size: 7.1 MB (7050935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0464c24aec36583186ddd00d659a44cbfbe8eb6967595e263922cee114f11541`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e247b1ab45847502319a775832f1e37efd8e27edab85850c1cd39355d7c59a`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bca692b6b90a8e7b2b7d9ea755343336ec76f096b7f3eef575a86f50e64dc5`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3557d9ac8171b21f42a1bee80b244527a6000a38cb1673347a20e01f26387`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:1d52723019944547c28befc6831cf54a194fe6cf5da2cbe5d83dada671148eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:9f0daa17d5998a047f470ea9d8842dc0eb687557782823b3fea2bc5538aeaf23
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 MB (131054329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0b328dd4c47b0486963aab87b1d33d09cc56b17a894d7d1f8cbff35d6514a7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Mon, 29 Jun 2026 20:13:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 20:13:42 GMT
RUN cmd /S /C #(nop) COPY file:d28b1675c385af4d7600302dadf40a3bf46cd73b4ca42fe37500427a26b9b480 in C:\nats-server.exe 
# Mon, 29 Jun 2026 20:13:44 GMT
RUN cmd /S /C #(nop) COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 20:13:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 20:13:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 20:13:48 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009c7fdf180fbd2e449732d8667e2bd25318b296d7f9385339be98aa234c835e`  
		Last Modified: Mon, 29 Jun 2026 20:13:55 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3906542123b76df88980ceb04181b631e9922c06a031cb9d6c343bc4fc335b59`  
		Last Modified: Mon, 29 Jun 2026 20:13:57 GMT  
		Size: 7.1 MB (7050935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0464c24aec36583186ddd00d659a44cbfbe8eb6967595e263922cee114f11541`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e247b1ab45847502319a775832f1e37efd8e27edab85850c1cd39355d7c59a`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bca692b6b90a8e7b2b7d9ea755343336ec76f096b7f3eef575a86f50e64dc5`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd3557d9ac8171b21f42a1bee80b244527a6000a38cb1673347a20e01f26387`  
		Last Modified: Mon, 29 Jun 2026 20:13:53 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:1b5a0a665cbe50a4ea28e8a82cf809b26cee5027d1fcaf8682fadf8f385fdf29
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
$ docker pull nats@sha256:da52c7cd2dd8cfbfd7d2dfb251b761e42dbfd6fe0acb09fd26cbb42bdddb2866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6857592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ccfa5190b3b463a3fcf96e85c57584707cb0e37e977effc0b13df38ad27da`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:13:56 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:13:56 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:13:56 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:13:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:001b0b866410b42b38bcb2e428951af42433891ff425dfcce0b3a53cf93d9cf5`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.9 MB (6857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a301e2bd5843dce0ae9f53e3b56e505349c98b58f06c463430d25b5c5ff3d2ac`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4e6b9bd23e99f1e6893cbc2298ff6542ff362ac45479424f0cbbaa44e0bd7932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b91a2a2149df4bdf026d1ba840708ff2f744d4552979b6f5238e32d4b9fadd`

```dockerfile
```

-	Layers:
	-	`sha256:f2654502a1c07929b5dba813de85a6fecf099bd5b4e5dc0304f5bffb9a55374a`  
		Last Modified: Mon, 29 Jun 2026 19:14:00 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f954b0114100cc6b04d48371743c840445bbd9d9cd58fd347d548df20fb81377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6591898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fecc68893e7b073ba43eb1643ffef18c78a2bcde561b9df87690e4c25b31729d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:02 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:087a70319659349faa0bc66d2f258c634f201af06cf4cd72fd052fe0f1741923`  
		Last Modified: Mon, 29 Jun 2026 15:45:00 GMT  
		Size: 6.6 MB (6591390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48bfacc9913ae01cc25da4a4e0b5b45dd8572ebef94eb75ee659e643ca668f`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2ddfb53928614b91b72d029bf8c1fe2c18c9323525cddd2435738502af8f535f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c648adf5a8076bdff845afbe972feb29cbce83a045fc1fa7a6407350edd450`

```dockerfile
```

-	Layers:
	-	`sha256:f18d91a70c6190eda91e68db672ccbc0be90eca9e3a3cbca1053dac4180c85bb`  
		Last Modified: Mon, 29 Jun 2026 20:10:07 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5acf1bcd52c9815e894b475e74896d5c20d20f75dc1d0a4609284c356a23e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02eaac6cac973cc88e6d44cfa8e4fa97db877aa382eca9ca11a3aabdc71efaa4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:10:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:10:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:10:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:10:01 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:10:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:95cb78be6f3eb15e97acc3a341503927e5ccafbd12a09b4a1b82fbb89f4787b5`  
		Last Modified: Mon, 29 Jun 2026 15:45:01 GMT  
		Size: 6.6 MB (6580972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce96a7f9a07f1a57504be91420ffc8fe2f13ee198161d2b34cfa5461201d23c9`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7350f027d99946847895026cb1af3842bdad2563af2c7a4902c947e3e5859335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6365d446dc11c95971d0b41e292ef423e0863365d7c070019c54d2c193b476ff`

```dockerfile
```

-	Layers:
	-	`sha256:0d8192ce2954c6a959615d982ceaa8825bd46cf89ead122b5706cc29fcf8bd71`  
		Last Modified: Mon, 29 Jun 2026 20:10:05 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:25e15191f85a79618d9811e8747e99ac98b0a40bfaae0aaaa5001bb1230c1d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6207675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2b8f5a6e48a97cd470606ae3bf871c5e7a728291b699ed0fc6ade464b4cd4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 20:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 20:09:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 20:09:47 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 20:09:47 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 20:09:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ceb26b4c7119501bb3160d6cbbe50dce6ca269cc3bc37d3bfb9a8d65ab54e83e`  
		Last Modified: Mon, 29 Jun 2026 15:45:05 GMT  
		Size: 6.2 MB (6207167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a970c139d6bb37d99b808c536d15fdfb2452430180d1906126f13f7c0e3e65c8`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:dbb4f985f00b8ed1cf158bbc14683f3982c6af4dbbd8a11fb368833ce8ab40d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8762707c4a125db65916d8207dfc41bd88cb661dfd73431bef3936beaa1b6e79`

```dockerfile
```

-	Layers:
	-	`sha256:6d1ce7246188626d86f106948c8c45d6673d92d8b12bc55a2f76ad1a4a77c06b`  
		Last Modified: Mon, 29 Jun 2026 20:09:51 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:0d2f692536149ac22566cf1b8c8c155bbf8704b0219606b603d37a2eb62f66a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6271147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5853d65dc9c9039e59f599fe9d6264c1b4b775d3ec6a9efaefa2487a1b2910c1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:12:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:12:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:12:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:12:46 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:12:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:094159f217313d715a9c9416ce56b6efb6774fae53d0a118eb72c19dd5050f69`  
		Last Modified: Mon, 29 Jun 2026 15:45:02 GMT  
		Size: 6.3 MB (6270639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa1d383fd4674e2d350a56d40d9d7a4a018dcdcac31733be7d84231bbad1d5b`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7388f5e7e39dd5b070cb36fd9cf62973a1dbe1673ae86098ed3504c78e1ef328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a70cea4e571b8e5e9bb3f1775b350266ece5ba0911b4910d792e2f5c7a8522`

```dockerfile
```

-	Layers:
	-	`sha256:c683a72a6137cd681254bab9a60e1a450a3a8e636d80bcccb57e77942df0b512`  
		Last Modified: Mon, 29 Jun 2026 19:12:52 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:fa31a78cc1dfc74ac5954db2d0fabe8025d55442dd778436f11eb45bbad212b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6666748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a751449230c715131c826c9e954f6c6faab06fed9d6ac6ef617518f68b0f57`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 29 Jun 2026 19:18:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 29 Jun 2026 19:18:18 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Mon, 29 Jun 2026 19:18:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 29 Jun 2026 19:18:19 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 29 Jun 2026 19:18:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c051b099bef1cbfeba54872473e4a7281c4a402d9f0b7c1bdf892e5e21ea8c51`  
		Last Modified: Mon, 29 Jun 2026 15:45:04 GMT  
		Size: 6.7 MB (6666239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd00d66579c55de314f0aa7536b46c9471486f908c26ae17a7d930bfdd9fb9`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:6e482d7d215597ddb64e6a49fb2d97ed5f170b063872e7b945de9574375342eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa169f897fcb8ad6d1b168458e6f22434b580cca5dd468838bbd781ec75f31a`

```dockerfile
```

-	Layers:
	-	`sha256:cfe01b7f8ddd174d7457c698713d2616d4d35273045161e7a898b8d8a593e3f4`  
		Last Modified: Mon, 29 Jun 2026 19:18:27 GMT  
		Size: 10.4 KB (10422 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:f701716476a8d968bd766320239d98d7f973ebaaa7a6f960f65648bda132229e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:windowsservercore` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:2c61006c6743420a33c3ade658d600d9b81f09a86df8c44fe02741a71d196d7f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140052973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782541001e22820de00703de294e85e7c622fc9ea85c9030e8fda96177afa0cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 29 Jun 2026 19:16:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Jun 2026 19:16:31 GMT
ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 19:16:32 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:16:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:16:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.3/nats-server-v2.14.3-windows-amd64.zip
# Mon, 29 Jun 2026 19:16:37 GMT
ENV NATS_SERVER_SHASUM=94e338d742761272e31eab1efb1f767eac3a2e56e4c05a7933c65a73fe95a27b
# Mon, 29 Jun 2026 19:17:35 GMT
RUN Set-PSDebug -Trace 2
# Mon, 29 Jun 2026 19:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 29 Jun 2026 19:18:06 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 19:18:08 GMT
EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 19:18:09 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 19:18:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac87f215828b12e2044c46470b221ea4307d0fc11cf8280e12474587a59317d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff6f7da74f9e652f79bc8278319981b268148b1548a3ef4220d3ccbe4b5473d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e85164857353b52ed850cc83049bc199678edaed484f95d1e38aa0a4f1b525b`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706cc542b32b6c088b1b95499c39a0c6f9dbe749f47087a0cd668545100147ba`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25bcf16bfd2387cc38d31f75eeac32290dada9d452e1f50b902530775f1c0ff`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aecb5ee131c5c835ec5c73c2ad224bf1e9c3ede99efeca9eec6a270f5c22b1`  
		Last Modified: Mon, 29 Jun 2026 19:18:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f1b98897859ea619b08dd0f0db49b009771052a13d263d4980a21c40901f2`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 496.7 KB (496723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784da3b63359a7bbb87eb47bb8a637b409b418e94af977bf3c24722cbc2ec89e`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 7.4 MB (7417113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae24643aacc8edba76b5661a3358a9461f9fda9a7d1f0fccaeca461dfb074a23`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe52ddb42630f70fd61331adf5e83118d27382c4d3922882adb2d981105bac94`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087e85133498df0eb7d45b8bc9353ec3fa1fc98964b2f88c33152ca73bf5abd6`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9462b672f1e05436ba0020f6b3b71b8db8b844d5c5183c1088c29d06d39df1be`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:f701716476a8d968bd766320239d98d7f973ebaaa7a6f960f65648bda132229e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull nats@sha256:2c61006c6743420a33c3ade658d600d9b81f09a86df8c44fe02741a71d196d7f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2140052973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782541001e22820de00703de294e85e7c622fc9ea85c9030e8fda96177afa0cb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 29 Jun 2026 19:16:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 29 Jun 2026 19:16:31 GMT
ENV NATS_DOCKERIZED=1
# Mon, 29 Jun 2026 19:16:32 GMT
ENV NATS_SERVER=2.14.3
# Mon, 29 Jun 2026 19:16:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.14.3
# Mon, 29 Jun 2026 19:16:35 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.14.3/nats-server-v2.14.3-windows-amd64.zip
# Mon, 29 Jun 2026 19:16:37 GMT
ENV NATS_SERVER_SHASUM=94e338d742761272e31eab1efb1f767eac3a2e56e4c05a7933c65a73fe95a27b
# Mon, 29 Jun 2026 19:17:35 GMT
RUN Set-PSDebug -Trace 2
# Mon, 29 Jun 2026 19:18:05 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 29 Jun 2026 19:18:06 GMT
COPY file:955816fff9b6400a43d9954c1d8f3dc8ab654bfbdf5936157955e3e678752b7b in C:\nats-server.conf 
# Mon, 29 Jun 2026 19:18:08 GMT
EXPOSE 4222 6222 8222
# Mon, 29 Jun 2026 19:18:09 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 29 Jun 2026 19:18:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac87f215828b12e2044c46470b221ea4307d0fc11cf8280e12474587a59317d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff6f7da74f9e652f79bc8278319981b268148b1548a3ef4220d3ccbe4b5473d`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e85164857353b52ed850cc83049bc199678edaed484f95d1e38aa0a4f1b525b`  
		Last Modified: Mon, 29 Jun 2026 19:18:18 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706cc542b32b6c088b1b95499c39a0c6f9dbe749f47087a0cd668545100147ba`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25bcf16bfd2387cc38d31f75eeac32290dada9d452e1f50b902530775f1c0ff`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aecb5ee131c5c835ec5c73c2ad224bf1e9c3ede99efeca9eec6a270f5c22b1`  
		Last Modified: Mon, 29 Jun 2026 19:18:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2f1b98897859ea619b08dd0f0db49b009771052a13d263d4980a21c40901f2`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 496.7 KB (496723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784da3b63359a7bbb87eb47bb8a637b409b418e94af977bf3c24722cbc2ec89e`  
		Last Modified: Mon, 29 Jun 2026 19:18:17 GMT  
		Size: 7.4 MB (7417113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae24643aacc8edba76b5661a3358a9461f9fda9a7d1f0fccaeca461dfb074a23`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.9 KB (1859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe52ddb42630f70fd61331adf5e83118d27382c4d3922882adb2d981105bac94`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087e85133498df0eb7d45b8bc9353ec3fa1fc98964b2f88c33152ca73bf5abd6`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9462b672f1e05436ba0020f6b3b71b8db8b844d5c5183c1088c29d06d39df1be`  
		Last Modified: Mon, 29 Jun 2026 19:18:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
