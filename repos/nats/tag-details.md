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
$ docker pull nats@sha256:c9e19fc4f9d0b36f9d2da3175ce3c95220806d098c24d328feb869886ab4afef
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
$ docker pull nats@sha256:391f0072ce67ee55b761370c314dbc8a7281473e0bfda3ac659049f1b08075a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95d5bca384b7959bb5cf1a743a13f85be65a9488c0552f4df4cec87389b3200`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:57 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e87fa5d12be7bc0f44b53fa6cd141e76f56faef2467d8d9769be47ac8a3674`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:7c0366118c1dc0312ba0da7857982f13047f2ec8f1fe47820ae2510cc388c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f6f9d105ca7c46470f68af2b4271f0ed40ff0ad556161424e05e3a8ecaa28`

```dockerfile
```

-	Layers:
	-	`sha256:334dab01a895b2d00e9ac0e339855e2a15daf4569eef8b6a44197b75ed20f62f`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea3c1af26c064464b8f6bca423596b7220fa93816adaf83f706c9ae34b91985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37732cf595594fea3845c95390a620ae7b6486b55c225260d9a94cf8aa1c3191`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34d7930b8b8e75da31eb1b797ef0912c6853bdc85ad347e1b797a5634d3577`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:8e85b848d4b99afd92319210009a21f0052594311083d77fcf1ee8d6cab7cd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd733e47fb31591cc226c0a9aeceff2ca10b4207b7a4381cdd83879112bed1e8`

```dockerfile
```

-	Layers:
	-	`sha256:9705c11af89c00eef360d7c22c0fee24c5db2d4c6b9c7611bfc6452b12f7eb79`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3a84a8d961bad8bad4fe7fb65dee444f2a66a059b8558ae8fb65574034a28e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9ca91358bfb3db35540bfd10f98b46899bfd81947a3e7c8034dbdccd3698e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1cc2ded7c5a3d7e8d9680c305f87bde0af7613fd1da0bd9f7b3f4b28528afd`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:d2dc28bfb63659ddc44a14336f01f50ae3f3163b738ec04ce8fe354eb7cb0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdc86cc80dfedb4387659a7fa450f4216ffa6e6ac70823bfe739ccd9ed6902`

```dockerfile
```

-	Layers:
	-	`sha256:a28c5e1d2bd63600380e93535a5184c2c136a6aceb6cb7955e7d0e27563e1515`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:67c19494d70d06a12fdb38cf1be9df8ac8c003f1a8b236cd006d98ecc44c1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb010d3d2ef36bf55d9822e7505d72bc8749b4c81f49fa8347f6bc0170c6fe0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:16 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986e74a3c2ed133ac9088b767d56152dbe9ab65a416b04c81b00818be1ea963b`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:360bbf5808469578c04388e925785d45de711f2e0721b45aaf6f69dd5d197235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc87059696946491f60585793b3ae1fb94f85c1837a552ee798c7fd04d8c20f5`

```dockerfile
```

-	Layers:
	-	`sha256:3df5561b2a5a1ba9b17f6deec10fced17cc1921bad7497afc9fa646a3ee3e06a`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:b7d4c7253edb794c82e7dfed2c9cfa02dfd904e51f74f28ba31e047f62fc7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6ccedb2bd06fad337c3208934e55614b5dce7689fdc624d7c1ea46585b0910`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:150a2bdf7ca081074b6337f2c6a2ce949012f032b621816bf7d9518a4c9c8b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0e2cf0c979f91dcf610709e731f9d2524dd2a0d1270d5f0b2d331e8e5cce5`

```dockerfile
```

-	Layers:
	-	`sha256:71e0f2fc0ec84444d3f17187d21565a2004ebcf91fc6379221afe6b5f292aff3`  
		Last Modified: Fri, 17 Apr 2026 02:08:48 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
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
$ docker pull nats@sha256:e602ceca19bddc3dd7197b4b1afde53a16cd9d31a5500a8ae5620f36cb01963c
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
$ docker pull nats@sha256:16179be8b1ec51f6e587273a8f77f42773ea1f12228ad777764d971e7b43c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10911201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9559d6064637f63c271167a9d7c010ff5364b1eec2b0208599b50488ba703d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7a1e64c52df3467627e6d1c644bcb8211343cd68dddf6166bdffbccaf244fd`  
		Last Modified: Fri, 17 Apr 2026 00:15:33 GMT  
		Size: 7.1 MB (7102043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029b2f91063f4996b4cd7e46a633ab1a441fa1b56b1f99ed0b8451abeca076cb`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d704923a1249776a808f8aeafbe1adf7092d06b738b33f076cad79dcad5cf25`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ca41342c8a71a1155058491c46bc3acc5e7cdb6651860972e62fb3c748ab050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d7c6232cacba47988be2ed2b963902987d654145e91fa75e175f098bdbdb14`

```dockerfile
```

-	Layers:
	-	`sha256:dc14f6b45ffd0cf094851f620d7c09a23513353217e1640bd80f9752ae64eb67`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:46f43a77c9d9be15ca3b2787d01a7fc76c0ad5c1f84b62acdfe9c75bdf2364cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1b5fcf3af1aec5f8186371ced026734b0dc358f81fd79977d24923f55da091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52664fd029115b59e10665beb1de4db22437397f1e12d9ef21a10227a4bcb0b3`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 6.8 MB (6821275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a63f62b766f87fc00d415fb393198a177ca29d74ef894de1081a534644c51f`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42627bd4fc0b9abb95a7fe4472894e86dac74bcfafc35397fe46a8b51863a24b`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:02712ae3dfd268f7c0f286d515e88ffd04661bd2afa30df5ef55d8c1251c2d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc157db9d7cfbdfb06f25ffab6be682d8f329dbd5cb945f440a0b934ff633ae`

```dockerfile
```

-	Layers:
	-	`sha256:3921d54fa2bad5abd1ccb3ba03fdde77fb3342fb0c2f5f4ae861e1142b27e559`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:dc95c9071c61ae217f8b7ccc6c6cc4ed7135efd907ab216185d7a046f848263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edceff3cd31a9ba3c0916ec5a29e6f96072c9da161efff71263cdbd8bb621fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3ef39893803a1aa71385b7b4a0e2f2489c1714926ebc5a17f0f283f992c574`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 6.8 MB (6812139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05c0dd84c92bf393d4eeb2e08cb836caae1367d08914ed39ee6012bc7979eb`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5b69ca76cd026d2a3a3104034ad0bcde0f0a1ff1a54e334a1d5f2b7aa2ce0`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a096ab49bf85fe59d54ca81110922ea5bdd2e0d348e69d0f6025e938b39f26b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af01ae40e078b504a99160d21be1719bf0893debfd46c721e0f3f1b5fb2b8d88`

```dockerfile
```

-	Layers:
	-	`sha256:23e4cd5325bfcff95bbb97f89ba5f6e6dc0407032e7c0fb1cde3ad1ac6830a7b`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb1c336dc892313409a8a9be0bd058eeb502231aa3383b448d862253abe72660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10653076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7263323b7691f6bfc1ce77845e1493322e0a7fb05848ba9496d17994e3c358`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414ff6f42514787c192e710db9db418be359224a6173e1237a72689ab899901a`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 6.5 MB (6510214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bb42c58d7e11c558e5072fdac886e2e8d5119360c8339777bf525f6b3de3be`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f5a1bbeb5c096e363e206a3d729f50c23ae559b4b3d9fea208d0b170b4864d`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a80cf61114fd852a49cc7cc405df6566531f25fb08f1698e38110bd13b16bcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1eea64ca314ff49953a4d62c6f57c8921b550e4a65eef8447cab8789dafa98`

```dockerfile
```

-	Layers:
	-	`sha256:f96940dabf37dc5e896241d7598fd3bf014ea2f2dec81a8253215bce6dd38616`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:53b58d1e5ac5757d0090c9c82d6b43c4fa3983e2af4ada84b96a6431d7a6cad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2412c201b02e670a6c66daff1a839dbf8949e02fd7bab2be04cea5c1e0c738e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:02 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:19:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ed90b89f0799173e6fccc22fecf8ff6c8973c8ed4ff1831c68a7c7569b4cd`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 6.6 MB (6560526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac41c2bd3722584f61f21b39d46ec42523bd6ea86f211b9027e5acf3135de9`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49b420d0d646e4990b9696c25668a04fb23ae54be76f6897fbd49eae67b24c`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:35462817b467f61ebceb4eca3c0ac8d23fbdee1ba0b903f77d995d769a172ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f729ef5c8fed43aecc14c5a725ab776840e1a16f702f8496ef3b696338d2f4d3`

```dockerfile
```

-	Layers:
	-	`sha256:822b657516851096b98cd62907a761f8ccbbb44813254a0078eb31d4f272c619`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:8dd0bb86b226ee0c00b11bee7e5402a505865da642006ff14293d14912b11e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10596317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2033c7f5d89abe8c752cd0bceac3d04d00854284c008645ba31f91ef04652287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7537aff86e4637878e5664a942467243a0f2cd0f3724bad313542c288b66619f`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 6.9 MB (6941474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c98718326853d62529f33a4745f08a21999d45bddc49bf4d4175feb2bd9c49`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5b57122821a0589eb6f05dc704b4f828e3060b27f5c6eeec2cad9b5b52bf3c`  
		Last Modified: Fri, 17 Apr 2026 00:13:46 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6a1b0dd4f10ca2f0dcfcd22ebcb04999217fcbf87ad066c7993d2a45e3970490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c0a8646f0475362f0b87ffe0fba73b5631df8220475194d2849b657ea3b049`

```dockerfile
```

-	Layers:
	-	`sha256:a85160fd978747e6ebfeae736628c48024e7b74f2f00bc194d8b8fb7b1c81552`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:e602ceca19bddc3dd7197b4b1afde53a16cd9d31a5500a8ae5620f36cb01963c
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
$ docker pull nats@sha256:16179be8b1ec51f6e587273a8f77f42773ea1f12228ad777764d971e7b43c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10911201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9559d6064637f63c271167a9d7c010ff5364b1eec2b0208599b50488ba703d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7a1e64c52df3467627e6d1c644bcb8211343cd68dddf6166bdffbccaf244fd`  
		Last Modified: Fri, 17 Apr 2026 00:15:33 GMT  
		Size: 7.1 MB (7102043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029b2f91063f4996b4cd7e46a633ab1a441fa1b56b1f99ed0b8451abeca076cb`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d704923a1249776a808f8aeafbe1adf7092d06b738b33f076cad79dcad5cf25`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ca41342c8a71a1155058491c46bc3acc5e7cdb6651860972e62fb3c748ab050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d7c6232cacba47988be2ed2b963902987d654145e91fa75e175f098bdbdb14`

```dockerfile
```

-	Layers:
	-	`sha256:dc14f6b45ffd0cf094851f620d7c09a23513353217e1640bd80f9752ae64eb67`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:46f43a77c9d9be15ca3b2787d01a7fc76c0ad5c1f84b62acdfe9c75bdf2364cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1b5fcf3af1aec5f8186371ced026734b0dc358f81fd79977d24923f55da091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52664fd029115b59e10665beb1de4db22437397f1e12d9ef21a10227a4bcb0b3`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 6.8 MB (6821275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a63f62b766f87fc00d415fb393198a177ca29d74ef894de1081a534644c51f`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42627bd4fc0b9abb95a7fe4472894e86dac74bcfafc35397fe46a8b51863a24b`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:02712ae3dfd268f7c0f286d515e88ffd04661bd2afa30df5ef55d8c1251c2d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc157db9d7cfbdfb06f25ffab6be682d8f329dbd5cb945f440a0b934ff633ae`

```dockerfile
```

-	Layers:
	-	`sha256:3921d54fa2bad5abd1ccb3ba03fdde77fb3342fb0c2f5f4ae861e1142b27e559`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:dc95c9071c61ae217f8b7ccc6c6cc4ed7135efd907ab216185d7a046f848263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edceff3cd31a9ba3c0916ec5a29e6f96072c9da161efff71263cdbd8bb621fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3ef39893803a1aa71385b7b4a0e2f2489c1714926ebc5a17f0f283f992c574`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 6.8 MB (6812139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05c0dd84c92bf393d4eeb2e08cb836caae1367d08914ed39ee6012bc7979eb`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5b69ca76cd026d2a3a3104034ad0bcde0f0a1ff1a54e334a1d5f2b7aa2ce0`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a096ab49bf85fe59d54ca81110922ea5bdd2e0d348e69d0f6025e938b39f26b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af01ae40e078b504a99160d21be1719bf0893debfd46c721e0f3f1b5fb2b8d88`

```dockerfile
```

-	Layers:
	-	`sha256:23e4cd5325bfcff95bbb97f89ba5f6e6dc0407032e7c0fb1cde3ad1ac6830a7b`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb1c336dc892313409a8a9be0bd058eeb502231aa3383b448d862253abe72660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10653076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7263323b7691f6bfc1ce77845e1493322e0a7fb05848ba9496d17994e3c358`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414ff6f42514787c192e710db9db418be359224a6173e1237a72689ab899901a`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 6.5 MB (6510214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bb42c58d7e11c558e5072fdac886e2e8d5119360c8339777bf525f6b3de3be`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f5a1bbeb5c096e363e206a3d729f50c23ae559b4b3d9fea208d0b170b4864d`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a80cf61114fd852a49cc7cc405df6566531f25fb08f1698e38110bd13b16bcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1eea64ca314ff49953a4d62c6f57c8921b550e4a65eef8447cab8789dafa98`

```dockerfile
```

-	Layers:
	-	`sha256:f96940dabf37dc5e896241d7598fd3bf014ea2f2dec81a8253215bce6dd38616`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:53b58d1e5ac5757d0090c9c82d6b43c4fa3983e2af4ada84b96a6431d7a6cad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2412c201b02e670a6c66daff1a839dbf8949e02fd7bab2be04cea5c1e0c738e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:02 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:19:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ed90b89f0799173e6fccc22fecf8ff6c8973c8ed4ff1831c68a7c7569b4cd`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 6.6 MB (6560526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac41c2bd3722584f61f21b39d46ec42523bd6ea86f211b9027e5acf3135de9`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49b420d0d646e4990b9696c25668a04fb23ae54be76f6897fbd49eae67b24c`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:35462817b467f61ebceb4eca3c0ac8d23fbdee1ba0b903f77d995d769a172ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f729ef5c8fed43aecc14c5a725ab776840e1a16f702f8496ef3b696338d2f4d3`

```dockerfile
```

-	Layers:
	-	`sha256:822b657516851096b98cd62907a761f8ccbbb44813254a0078eb31d4f272c619`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:8dd0bb86b226ee0c00b11bee7e5402a505865da642006ff14293d14912b11e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10596317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2033c7f5d89abe8c752cd0bceac3d04d00854284c008645ba31f91ef04652287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7537aff86e4637878e5664a942467243a0f2cd0f3724bad313542c288b66619f`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 6.9 MB (6941474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c98718326853d62529f33a4745f08a21999d45bddc49bf4d4175feb2bd9c49`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5b57122821a0589eb6f05dc704b4f828e3060b27f5c6eeec2cad9b5b52bf3c`  
		Last Modified: Fri, 17 Apr 2026 00:13:46 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6a1b0dd4f10ca2f0dcfcd22ebcb04999217fcbf87ad066c7993d2a45e3970490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c0a8646f0475362f0b87ffe0fba73b5631df8220475194d2849b657ea3b049`

```dockerfile
```

-	Layers:
	-	`sha256:a85160fd978747e6ebfeae736628c48024e7b74f2f00bc194d8b8fb7b1c81552`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:dbda35114cbb4890d9ee9ff85c1328bbdce97e1ae72ea36d681ef6dcf972d202
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
$ docker pull nats@sha256:391f0072ce67ee55b761370c314dbc8a7281473e0bfda3ac659049f1b08075a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95d5bca384b7959bb5cf1a743a13f85be65a9488c0552f4df4cec87389b3200`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:57 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e87fa5d12be7bc0f44b53fa6cd141e76f56faef2467d8d9769be47ac8a3674`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7c0366118c1dc0312ba0da7857982f13047f2ec8f1fe47820ae2510cc388c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f6f9d105ca7c46470f68af2b4271f0ed40ff0ad556161424e05e3a8ecaa28`

```dockerfile
```

-	Layers:
	-	`sha256:334dab01a895b2d00e9ac0e339855e2a15daf4569eef8b6a44197b75ed20f62f`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea3c1af26c064464b8f6bca423596b7220fa93816adaf83f706c9ae34b91985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37732cf595594fea3845c95390a620ae7b6486b55c225260d9a94cf8aa1c3191`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34d7930b8b8e75da31eb1b797ef0912c6853bdc85ad347e1b797a5634d3577`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8e85b848d4b99afd92319210009a21f0052594311083d77fcf1ee8d6cab7cd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd733e47fb31591cc226c0a9aeceff2ca10b4207b7a4381cdd83879112bed1e8`

```dockerfile
```

-	Layers:
	-	`sha256:9705c11af89c00eef360d7c22c0fee24c5db2d4c6b9c7611bfc6452b12f7eb79`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3a84a8d961bad8bad4fe7fb65dee444f2a66a059b8558ae8fb65574034a28e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9ca91358bfb3db35540bfd10f98b46899bfd81947a3e7c8034dbdccd3698e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1cc2ded7c5a3d7e8d9680c305f87bde0af7613fd1da0bd9f7b3f4b28528afd`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d2dc28bfb63659ddc44a14336f01f50ae3f3163b738ec04ce8fe354eb7cb0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdc86cc80dfedb4387659a7fa450f4216ffa6e6ac70823bfe739ccd9ed6902`

```dockerfile
```

-	Layers:
	-	`sha256:a28c5e1d2bd63600380e93535a5184c2c136a6aceb6cb7955e7d0e27563e1515`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:67c19494d70d06a12fdb38cf1be9df8ac8c003f1a8b236cd006d98ecc44c1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb010d3d2ef36bf55d9822e7505d72bc8749b4c81f49fa8347f6bc0170c6fe0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:16 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986e74a3c2ed133ac9088b767d56152dbe9ab65a416b04c81b00818be1ea963b`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:360bbf5808469578c04388e925785d45de711f2e0721b45aaf6f69dd5d197235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc87059696946491f60585793b3ae1fb94f85c1837a552ee798c7fd04d8c20f5`

```dockerfile
```

-	Layers:
	-	`sha256:3df5561b2a5a1ba9b17f6deec10fced17cc1921bad7497afc9fa646a3ee3e06a`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:b7d4c7253edb794c82e7dfed2c9cfa02dfd904e51f74f28ba31e047f62fc7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6ccedb2bd06fad337c3208934e55614b5dce7689fdc624d7c1ea46585b0910`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:150a2bdf7ca081074b6337f2c6a2ce949012f032b621816bf7d9518a4c9c8b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0e2cf0c979f91dcf610709e731f9d2524dd2a0d1270d5f0b2d331e8e5cce5`

```dockerfile
```

-	Layers:
	-	`sha256:71e0f2fc0ec84444d3f17187d21565a2004ebcf91fc6379221afe6b5f292aff3`  
		Last Modified: Fri, 17 Apr 2026 02:08:48 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
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
$ docker pull nats@sha256:dbda35114cbb4890d9ee9ff85c1328bbdce97e1ae72ea36d681ef6dcf972d202
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
$ docker pull nats@sha256:391f0072ce67ee55b761370c314dbc8a7281473e0bfda3ac659049f1b08075a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95d5bca384b7959bb5cf1a743a13f85be65a9488c0552f4df4cec87389b3200`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:57 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e87fa5d12be7bc0f44b53fa6cd141e76f56faef2467d8d9769be47ac8a3674`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7c0366118c1dc0312ba0da7857982f13047f2ec8f1fe47820ae2510cc388c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f6f9d105ca7c46470f68af2b4271f0ed40ff0ad556161424e05e3a8ecaa28`

```dockerfile
```

-	Layers:
	-	`sha256:334dab01a895b2d00e9ac0e339855e2a15daf4569eef8b6a44197b75ed20f62f`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea3c1af26c064464b8f6bca423596b7220fa93816adaf83f706c9ae34b91985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37732cf595594fea3845c95390a620ae7b6486b55c225260d9a94cf8aa1c3191`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34d7930b8b8e75da31eb1b797ef0912c6853bdc85ad347e1b797a5634d3577`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8e85b848d4b99afd92319210009a21f0052594311083d77fcf1ee8d6cab7cd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd733e47fb31591cc226c0a9aeceff2ca10b4207b7a4381cdd83879112bed1e8`

```dockerfile
```

-	Layers:
	-	`sha256:9705c11af89c00eef360d7c22c0fee24c5db2d4c6b9c7611bfc6452b12f7eb79`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3a84a8d961bad8bad4fe7fb65dee444f2a66a059b8558ae8fb65574034a28e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9ca91358bfb3db35540bfd10f98b46899bfd81947a3e7c8034dbdccd3698e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1cc2ded7c5a3d7e8d9680c305f87bde0af7613fd1da0bd9f7b3f4b28528afd`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d2dc28bfb63659ddc44a14336f01f50ae3f3163b738ec04ce8fe354eb7cb0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdc86cc80dfedb4387659a7fa450f4216ffa6e6ac70823bfe739ccd9ed6902`

```dockerfile
```

-	Layers:
	-	`sha256:a28c5e1d2bd63600380e93535a5184c2c136a6aceb6cb7955e7d0e27563e1515`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:67c19494d70d06a12fdb38cf1be9df8ac8c003f1a8b236cd006d98ecc44c1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb010d3d2ef36bf55d9822e7505d72bc8749b4c81f49fa8347f6bc0170c6fe0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:16 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986e74a3c2ed133ac9088b767d56152dbe9ab65a416b04c81b00818be1ea963b`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:360bbf5808469578c04388e925785d45de711f2e0721b45aaf6f69dd5d197235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc87059696946491f60585793b3ae1fb94f85c1837a552ee798c7fd04d8c20f5`

```dockerfile
```

-	Layers:
	-	`sha256:3df5561b2a5a1ba9b17f6deec10fced17cc1921bad7497afc9fa646a3ee3e06a`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:b7d4c7253edb794c82e7dfed2c9cfa02dfd904e51f74f28ba31e047f62fc7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6ccedb2bd06fad337c3208934e55614b5dce7689fdc624d7c1ea46585b0910`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:150a2bdf7ca081074b6337f2c6a2ce949012f032b621816bf7d9518a4c9c8b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0e2cf0c979f91dcf610709e731f9d2524dd2a0d1270d5f0b2d331e8e5cce5`

```dockerfile
```

-	Layers:
	-	`sha256:71e0f2fc0ec84444d3f17187d21565a2004ebcf91fc6379221afe6b5f292aff3`  
		Last Modified: Fri, 17 Apr 2026 02:08:48 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
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
$ docker pull nats@sha256:8f093cb30e8bfed2eff4bbea70dfcbffd847be40ec674b9f7a7b9d26f41234b2
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
$ docker pull nats@sha256:6026fcefbc8c47c2be01c22b3a8adbc42025c17cc928c009579e868ad7508b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6497607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcfa3f1357bff7c1c7510611163f749aebfe279ae866ab5a044e5e57c95c99b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:13:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:13:44 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:13:44 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:13:44 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:13:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:13:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9f0ebe5f9a1ae3ad639c8afca45fb722413353ade56a44dcf62bcfef80217dbb`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.5 MB (6497097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e1a3d878997721992626d968612830e36b2bf02e02b3328b3ac15759c0ea8b`  
		Last Modified: Fri, 17 Apr 2026 01:13:49 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:8f27fed47cda974f867f1386700a6014a9ef5d590e1af2cf0ada26b3ae3e0bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58ce43223a92800c17c75cd47418a48eefaebdabbc17a285314e76f115fdb9a`

```dockerfile
```

-	Layers:
	-	`sha256:33bf04ede4f3a943ff024e5f12bce32c5a0bb9166748872e0ef22cf5880371bb`  
		Last Modified: Fri, 17 Apr 2026 01:13:48 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:2608cfbd354d33b2932a94dc2b47d3dbf341008a40d371a532df9ccfe27e6d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0a7010738d4da19f91e4851984e905ffb94ca75f74f7ad75cc38eee92db67b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ac4c14b3f8076df43f73c9299994bae9134a062823f58d1140353085aa0b300`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.2 MB (6218951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ac5d76972bd80e5cf01b62c77075191e2cbb49fae723136503f99e8bbd5f40`  
		Last Modified: Fri, 17 Apr 2026 01:12:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:ba5ca70d7ca25a54873350a2eec247fdfbf818d63999e42204ff63fc7baba133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce46eb21add643afa47e6df6f20c6c2cbf05136e0948d3845137fff0575666e`

```dockerfile
```

-	Layers:
	-	`sha256:514ec24cb478e0f1b0db84a74f997f1697890c620f506018cafe047d8877ddc9`  
		Last Modified: Fri, 17 Apr 2026 01:12:33 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:50ed86b0111c027e65a30fb481e8905ac9a72718c5bfc9ae0bd7e9ba415f57d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad77b34c838e5f91c829d1a936243ad9ef7dece98be3ff3e381708b8fb828fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:43 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:43 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2a83fab97c651eacbf830fb7bd159907e5e14fda32f73c5628adf6899c32f67f`  
		Last Modified: Tue, 14 Apr 2026 16:12:11 GMT  
		Size: 6.2 MB (6208591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b4c7d8a44ca53c6ad494b2527e7b06e45cd0c74f651ee0c129f18d3ad5ad7b`  
		Last Modified: Fri, 17 Apr 2026 01:14:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:4fe65a1f80a741422bd860b28fd48efab7f9cc6334306494e5a5be9f3f51ad61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0e3bb622be324aa20e50643edfe951dd8bf5117d3cb183797d4e4c524dedb9`

```dockerfile
```

-	Layers:
	-	`sha256:9bea04e9589cbb82cb5be1827548ae5b11d2b919d91c72d80684ce5c3c358417`  
		Last Modified: Fri, 17 Apr 2026 01:14:47 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc6d37d617039b414987344c5b51fa5e2013343f0a1b017a42a9b1f3a341fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827af36b416951d2b3da590c3dd45bc88d1d022bd97438a1c8a9a3592444158f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:20 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:20 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53e14ebbec1f96d7732d422be8ee7b587c333a423ac37b45d8cbe989c7ffe1ed`  
		Last Modified: Tue, 14 Apr 2026 16:12:13 GMT  
		Size: 5.9 MB (5915332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26776296d50b8eb0772a64317fbbfe8298dd48e5acfbf80b00f34a606f4ab307`  
		Last Modified: Fri, 17 Apr 2026 01:34:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:ca8abe494d9e5c45013a55f63e3c336b7a648ad0645e1bebae8e9940e4ec4f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45ebf0e78412d9c83ec1c4b61db202bab3b503098bad7fe005e74cc0cf9d835`

```dockerfile
```

-	Layers:
	-	`sha256:f81079af62e66239b51e888dd23be34b9d7e9981a85be373ac54a2a655c7da92`  
		Last Modified: Fri, 17 Apr 2026 01:34:24 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; ppc64le

```console
$ docker pull nats@sha256:d473b23d3f76c223d24ebcb4d727b485952b8740d23d2f9adae98cec46090b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28940f6db27811588c31afbfe9d7f62cfa2bf5997035734a32059c51f1e15e51`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b63ce4825759431170974b945ec1ddea7f5665ed75cc067dc0285b5ece42ed12`  
		Last Modified: Tue, 14 Apr 2026 16:12:12 GMT  
		Size: 6.0 MB (5964595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:b71158efc942b40e496205c76cbb8ad0980bc9d7d44ec3bbabd6be9068c9acad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39b14348c59fd4c68e56a6b3993caf73d1de83a4bf32b3c4f42f1e45913dbd3`

```dockerfile
```

-	Layers:
	-	`sha256:58a49e99d73072d878df8c1f584d36ab8228edbea9c6e74afc2c9cc78323ae73`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; s390x

```console
$ docker pull nats@sha256:e35294278ff76bcb1fe56374110f4b06c269576ed7790035cb884905514779bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f361bf360d8325e6fcd51b413da8e62bc9d3349d5ffa47ce66c77b64b681ec30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9078b3e5e7cd72051df8071c386cbf0335d800dad99509157ffcfd8f4fc361`  
		Last Modified: Fri, 17 Apr 2026 03:00:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:f7b77c54d8013e193fe1637d61d70596d15af7f467886c746e4990c02b80a60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcd2c9c3f0905b48a181ecb2c54e99817e889d09b559ccb3625163e3ddb9966`

```dockerfile
```

-	Layers:
	-	`sha256:553590c07c651e9bd4871f634514aac2810de7afce20d412adc0440624524452`  
		Last Modified: Fri, 17 Apr 2026 03:00:37 GMT  
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
$ docker pull nats@sha256:47169454fd238c3bd104f9947a6f84c1fb4713cd89ebf29da541ce53358fc298
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
$ docker pull nats@sha256:62cb3a8de632e3dfc2a90d75436361b4d9655f0e05b4ac6cdf288625f4f1e4e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10764196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f43e01dbd062a0d7445ccf07425daf97f3c9b131dfad1d83d461fd25d02efd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:33 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:33 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:33 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:33 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1549fe52811b163dad6363b19ed5b1dbef22580dc8ae8bdd81255aff0606a`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 7.0 MB (6955039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a5a095806d982618ddf3458b47c0baa71e872550911885ed97c871ef77c8e7`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f6f70f1098d315ac2b26d3cee22d86094f5b422b2da94051a8103c43aee3a1`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:37ec2d35b904a87b031d377ad0ae1e9ca58941a8bc07810544ff31a7b23fbf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb3b132e4c95883151904f270f848d226d65efb3e8b60f25e24fd40f2683dd1`

```dockerfile
```

-	Layers:
	-	`sha256:d66433550b59c3ff75c3899eec8b1ce426114a3d83be4442fb12653ec74633cc`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ade01f393bf6a62dbbf014521365a975fe801491c9d992f3f94a4abc44c106f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10183416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7bbe121c0a8795dff73d14514e795827a41ec26cb05a5e5892c478274e7706`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:14 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc48e8c2cd02fa0b377d3d44d3bcb287dbb8e23ae6c5a3312a9bc14a911d38`  
		Last Modified: Fri, 17 Apr 2026 00:15:18 GMT  
		Size: 6.7 MB (6675063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abaa56ee89bdb343291cbf0836ce0dc7e79d6e22d62ec1c716cc914ce78392a`  
		Last Modified: Fri, 17 Apr 2026 00:15:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76353b3690a868dfe403515baad9237d61a90c25d662c002b89a52b3f365651`  
		Last Modified: Fri, 17 Apr 2026 00:15:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6bcec4f288d3676b4f8445a15d0a5c6846f7500324ce4ab89720295c199e0a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d764686032a4d0e7b2fd5fd9c5fbcd156171954280332b878087488eed9f125`

```dockerfile
```

-	Layers:
	-	`sha256:b1902c9888c320fc05d5cf411a5ead25736ee29e8a75a4abf0d2a564f9e5e2af`  
		Last Modified: Fri, 17 Apr 2026 00:15:18 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:88a5786e1e232199af0d994f6238cd75f33a3ee619529c8a8d92a0f7e510e858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9892783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b72c9e361f2152192713775a37eb16526bc2a7eaf0d5794b8e626c49854ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:23 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:23 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8398c47bd6ae433e2f3bde40e5b7df392542d47b2ac820c799ec796860eece`  
		Last Modified: Fri, 17 Apr 2026 00:15:28 GMT  
		Size: 6.7 MB (6665982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e72553ddff68e46b6a6af6efc169ab89bda6adbe6e8ba8569efa24f73a9668e`  
		Last Modified: Fri, 17 Apr 2026 00:15:27 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8838dd2cec0e257fdb4d239e2cb2f9a8bf78861d335156509372ec8083f221d`  
		Last Modified: Fri, 17 Apr 2026 00:15:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d063fda2ce7d9f50f9682d64c4d08e3b6fb5ca3b3a9a7fdb28eb84198478a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fea9b0e1ac50a218f647545512fa8b99188d3691f302045aa4261dc115d0f28`

```dockerfile
```

-	Layers:
	-	`sha256:3e9156041859edf9dc260aa9723eaf36a8da562e34800f44246c2269f6a71001`  
		Last Modified: Fri, 17 Apr 2026 00:15:27 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b66ae5ec567a90f00ae8df30b7dbb3f4b21758b4a1bb851ad6e9e49f5459daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20967c1b8e8d3f14a25f79e551d609e7793330fa502e5352f98891698bc12747`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:48 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:48 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:48 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:48 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:48 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab00d275d537a0cf1bfff28ff033bfaaf1353fcb42866a4f07501d59d90bc7a`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 6.4 MB (6373171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47320975f8b7e1919afbb55c23e84d1c8ea6c173ea1cb0196d9e7b31a94c44bc`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d629ae6d1b6079aeef1b3945679b6dc9cc6abf4e879628c41fd27c3108e1229f`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:29d83cbe455749a4217796d3f569beb308a3ae52e0658fa438e0e06e31c9b61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd85bb55d9be014e8a3ae6ee5fe03a93c8c3804d371904c09b3f3c2bab691e22`

```dockerfile
```

-	Layers:
	-	`sha256:f93982492431d5153d601735002a6ab47c467a168b7014901e0a7a4d6269bb06`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:8117df0b7f4ad130b27d34b371e6c206b3d8b6a86bcdc42c3662c4bff6ed1913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10161336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5afbda650d00b3b63b8591f36292178fb8270a017753f74fa9bcea9bac0575f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:10 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:19:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:19:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:19:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:19:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:19:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93502a03a8dc6cb0bf0383513a9b456a73eb7c3b00be855656913a7cc49eedd7`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 6.4 MB (6423711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb736d1c701df89f81b8ed7ae7299183b39fe61f218ddd30c0827dd8b27de4`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634ed6629dc149c04e1521c52443e7a95aabdc4a0584471afb00b01ba37f9519`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a7a1b0415e793868f1d0860af59b5be0e593808ff727210f48fa836c9f8e5d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131ff907d57e77f9145cf7fa68644970173220c5e54f35168211ab4649dd7a8f`

```dockerfile
```

-	Layers:
	-	`sha256:d5007684d306b92f1cc83a2c33ce052b11c02462641285aa473582e754738278`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:4665ef744eae958df06fa7f90eccf092c87b9303443dbe64df734d268c0d062d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10451115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c53ccc0e5f29509d8e8e600842f57455cf61213d9cbcbe173ebe2eb6eeb7268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:10 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:14:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:14:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:14:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:14:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:14:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:14:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f5ee94b985986baff103bfd91cf80667d3e192e194589c77442193ea9dd536`  
		Last Modified: Fri, 17 Apr 2026 00:14:19 GMT  
		Size: 6.8 MB (6796273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842a65e3e80f55672514dcef5e81832f7cebec6fe722429319b244893692ab1`  
		Last Modified: Fri, 17 Apr 2026 00:14:18 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d79d22c5b0229cae6cce00ca941a3ff246c9243200d12d1224eb8520af2d58`  
		Last Modified: Fri, 17 Apr 2026 00:14:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:58c5ef69555aa04c57d8b23c2ddc0e6b05dcb1eafb0e0e899ed80bdd8abc096d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec68f5a904cb0c482f67800cf10ae7beaa437942e0c7bc948843cf4f96f91a0b`

```dockerfile
```

-	Layers:
	-	`sha256:9f20b34e5ebc33ed80836487c456d86edc1d2473c21d8d5276688d09ca045a66`  
		Last Modified: Fri, 17 Apr 2026 00:14:18 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.22`

```console
$ docker pull nats@sha256:47169454fd238c3bd104f9947a6f84c1fb4713cd89ebf29da541ce53358fc298
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
$ docker pull nats@sha256:62cb3a8de632e3dfc2a90d75436361b4d9655f0e05b4ac6cdf288625f4f1e4e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10764196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f43e01dbd062a0d7445ccf07425daf97f3c9b131dfad1d83d461fd25d02efd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:33 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:33 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:33 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:33 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1549fe52811b163dad6363b19ed5b1dbef22580dc8ae8bdd81255aff0606a`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 7.0 MB (6955039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a5a095806d982618ddf3458b47c0baa71e872550911885ed97c871ef77c8e7`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f6f70f1098d315ac2b26d3cee22d86094f5b422b2da94051a8103c43aee3a1`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:37ec2d35b904a87b031d377ad0ae1e9ca58941a8bc07810544ff31a7b23fbf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb3b132e4c95883151904f270f848d226d65efb3e8b60f25e24fd40f2683dd1`

```dockerfile
```

-	Layers:
	-	`sha256:d66433550b59c3ff75c3899eec8b1ce426114a3d83be4442fb12653ec74633cc`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:ade01f393bf6a62dbbf014521365a975fe801491c9d992f3f94a4abc44c106f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10183416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7bbe121c0a8795dff73d14514e795827a41ec26cb05a5e5892c478274e7706`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:14 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc48e8c2cd02fa0b377d3d44d3bcb287dbb8e23ae6c5a3312a9bc14a911d38`  
		Last Modified: Fri, 17 Apr 2026 00:15:18 GMT  
		Size: 6.7 MB (6675063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abaa56ee89bdb343291cbf0836ce0dc7e79d6e22d62ec1c716cc914ce78392a`  
		Last Modified: Fri, 17 Apr 2026 00:15:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76353b3690a868dfe403515baad9237d61a90c25d662c002b89a52b3f365651`  
		Last Modified: Fri, 17 Apr 2026 00:15:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6bcec4f288d3676b4f8445a15d0a5c6846f7500324ce4ab89720295c199e0a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d764686032a4d0e7b2fd5fd9c5fbcd156171954280332b878087488eed9f125`

```dockerfile
```

-	Layers:
	-	`sha256:b1902c9888c320fc05d5cf411a5ead25736ee29e8a75a4abf0d2a564f9e5e2af`  
		Last Modified: Fri, 17 Apr 2026 00:15:18 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:88a5786e1e232199af0d994f6238cd75f33a3ee619529c8a8d92a0f7e510e858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9892783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b72c9e361f2152192713775a37eb16526bc2a7eaf0d5794b8e626c49854ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:23 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:23 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8398c47bd6ae433e2f3bde40e5b7df392542d47b2ac820c799ec796860eece`  
		Last Modified: Fri, 17 Apr 2026 00:15:28 GMT  
		Size: 6.7 MB (6665982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e72553ddff68e46b6a6af6efc169ab89bda6adbe6e8ba8569efa24f73a9668e`  
		Last Modified: Fri, 17 Apr 2026 00:15:27 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8838dd2cec0e257fdb4d239e2cb2f9a8bf78861d335156509372ec8083f221d`  
		Last Modified: Fri, 17 Apr 2026 00:15:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d063fda2ce7d9f50f9682d64c4d08e3b6fb5ca3b3a9a7fdb28eb84198478a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fea9b0e1ac50a218f647545512fa8b99188d3691f302045aa4261dc115d0f28`

```dockerfile
```

-	Layers:
	-	`sha256:3e9156041859edf9dc260aa9723eaf36a8da562e34800f44246c2269f6a71001`  
		Last Modified: Fri, 17 Apr 2026 00:15:27 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b66ae5ec567a90f00ae8df30b7dbb3f4b21758b4a1bb851ad6e9e49f5459daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20967c1b8e8d3f14a25f79e551d609e7793330fa502e5352f98891698bc12747`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:48 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:48 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:48 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:48 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:48 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab00d275d537a0cf1bfff28ff033bfaaf1353fcb42866a4f07501d59d90bc7a`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 6.4 MB (6373171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47320975f8b7e1919afbb55c23e84d1c8ea6c173ea1cb0196d9e7b31a94c44bc`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d629ae6d1b6079aeef1b3945679b6dc9cc6abf4e879628c41fd27c3108e1229f`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:29d83cbe455749a4217796d3f569beb308a3ae52e0658fa438e0e06e31c9b61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd85bb55d9be014e8a3ae6ee5fe03a93c8c3804d371904c09b3f3c2bab691e22`

```dockerfile
```

-	Layers:
	-	`sha256:f93982492431d5153d601735002a6ab47c467a168b7014901e0a7a4d6269bb06`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:8117df0b7f4ad130b27d34b371e6c206b3d8b6a86bcdc42c3662c4bff6ed1913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10161336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5afbda650d00b3b63b8591f36292178fb8270a017753f74fa9bcea9bac0575f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:10 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:19:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:19:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:19:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:19:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:19:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93502a03a8dc6cb0bf0383513a9b456a73eb7c3b00be855656913a7cc49eedd7`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 6.4 MB (6423711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb736d1c701df89f81b8ed7ae7299183b39fe61f218ddd30c0827dd8b27de4`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634ed6629dc149c04e1521c52443e7a95aabdc4a0584471afb00b01ba37f9519`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a7a1b0415e793868f1d0860af59b5be0e593808ff727210f48fa836c9f8e5d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131ff907d57e77f9145cf7fa68644970173220c5e54f35168211ab4649dd7a8f`

```dockerfile
```

-	Layers:
	-	`sha256:d5007684d306b92f1cc83a2c33ce052b11c02462641285aa473582e754738278`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:4665ef744eae958df06fa7f90eccf092c87b9303443dbe64df734d268c0d062d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10451115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c53ccc0e5f29509d8e8e600842f57455cf61213d9cbcbe173ebe2eb6eeb7268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:10 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:14:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:14:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:14:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:14:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:14:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:14:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f5ee94b985986baff103bfd91cf80667d3e192e194589c77442193ea9dd536`  
		Last Modified: Fri, 17 Apr 2026 00:14:19 GMT  
		Size: 6.8 MB (6796273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842a65e3e80f55672514dcef5e81832f7cebec6fe722429319b244893692ab1`  
		Last Modified: Fri, 17 Apr 2026 00:14:18 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d79d22c5b0229cae6cce00ca941a3ff246c9243200d12d1224eb8520af2d58`  
		Last Modified: Fri, 17 Apr 2026 00:14:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:58c5ef69555aa04c57d8b23c2ddc0e6b05dcb1eafb0e0e899ed80bdd8abc096d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec68f5a904cb0c482f67800cf10ae7beaa437942e0c7bc948843cf4f96f91a0b`

```dockerfile
```

-	Layers:
	-	`sha256:9f20b34e5ebc33ed80836487c456d86edc1d2473c21d8d5276688d09ca045a66`  
		Last Modified: Fri, 17 Apr 2026 00:14:18 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

```console
$ docker pull nats@sha256:53e4bacf2ece7434816db894b8e378076666105b2c46a8bd42ff344e3b4bb4e3
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
$ docker pull nats@sha256:6026fcefbc8c47c2be01c22b3a8adbc42025c17cc928c009579e868ad7508b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6497607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcfa3f1357bff7c1c7510611163f749aebfe279ae866ab5a044e5e57c95c99b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:13:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:13:44 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:13:44 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:13:44 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:13:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:13:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9f0ebe5f9a1ae3ad639c8afca45fb722413353ade56a44dcf62bcfef80217dbb`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.5 MB (6497097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e1a3d878997721992626d968612830e36b2bf02e02b3328b3ac15759c0ea8b`  
		Last Modified: Fri, 17 Apr 2026 01:13:49 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8f27fed47cda974f867f1386700a6014a9ef5d590e1af2cf0ada26b3ae3e0bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58ce43223a92800c17c75cd47418a48eefaebdabbc17a285314e76f115fdb9a`

```dockerfile
```

-	Layers:
	-	`sha256:33bf04ede4f3a943ff024e5f12bce32c5a0bb9166748872e0ef22cf5880371bb`  
		Last Modified: Fri, 17 Apr 2026 01:13:48 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:2608cfbd354d33b2932a94dc2b47d3dbf341008a40d371a532df9ccfe27e6d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0a7010738d4da19f91e4851984e905ffb94ca75f74f7ad75cc38eee92db67b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ac4c14b3f8076df43f73c9299994bae9134a062823f58d1140353085aa0b300`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.2 MB (6218951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ac5d76972bd80e5cf01b62c77075191e2cbb49fae723136503f99e8bbd5f40`  
		Last Modified: Fri, 17 Apr 2026 01:12:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ba5ca70d7ca25a54873350a2eec247fdfbf818d63999e42204ff63fc7baba133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce46eb21add643afa47e6df6f20c6c2cbf05136e0948d3845137fff0575666e`

```dockerfile
```

-	Layers:
	-	`sha256:514ec24cb478e0f1b0db84a74f997f1697890c620f506018cafe047d8877ddc9`  
		Last Modified: Fri, 17 Apr 2026 01:12:33 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:50ed86b0111c027e65a30fb481e8905ac9a72718c5bfc9ae0bd7e9ba415f57d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad77b34c838e5f91c829d1a936243ad9ef7dece98be3ff3e381708b8fb828fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:43 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:43 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2a83fab97c651eacbf830fb7bd159907e5e14fda32f73c5628adf6899c32f67f`  
		Last Modified: Tue, 14 Apr 2026 16:12:11 GMT  
		Size: 6.2 MB (6208591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b4c7d8a44ca53c6ad494b2527e7b06e45cd0c74f651ee0c129f18d3ad5ad7b`  
		Last Modified: Fri, 17 Apr 2026 01:14:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4fe65a1f80a741422bd860b28fd48efab7f9cc6334306494e5a5be9f3f51ad61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0e3bb622be324aa20e50643edfe951dd8bf5117d3cb183797d4e4c524dedb9`

```dockerfile
```

-	Layers:
	-	`sha256:9bea04e9589cbb82cb5be1827548ae5b11d2b919d91c72d80684ce5c3c358417`  
		Last Modified: Fri, 17 Apr 2026 01:14:47 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc6d37d617039b414987344c5b51fa5e2013343f0a1b017a42a9b1f3a341fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827af36b416951d2b3da590c3dd45bc88d1d022bd97438a1c8a9a3592444158f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:20 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:20 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53e14ebbec1f96d7732d422be8ee7b587c333a423ac37b45d8cbe989c7ffe1ed`  
		Last Modified: Tue, 14 Apr 2026 16:12:13 GMT  
		Size: 5.9 MB (5915332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26776296d50b8eb0772a64317fbbfe8298dd48e5acfbf80b00f34a606f4ab307`  
		Last Modified: Fri, 17 Apr 2026 01:34:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ca8abe494d9e5c45013a55f63e3c336b7a648ad0645e1bebae8e9940e4ec4f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45ebf0e78412d9c83ec1c4b61db202bab3b503098bad7fe005e74cc0cf9d835`

```dockerfile
```

-	Layers:
	-	`sha256:f81079af62e66239b51e888dd23be34b9d7e9981a85be373ac54a2a655c7da92`  
		Last Modified: Fri, 17 Apr 2026 01:34:24 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:d473b23d3f76c223d24ebcb4d727b485952b8740d23d2f9adae98cec46090b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28940f6db27811588c31afbfe9d7f62cfa2bf5997035734a32059c51f1e15e51`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b63ce4825759431170974b945ec1ddea7f5665ed75cc067dc0285b5ece42ed12`  
		Last Modified: Tue, 14 Apr 2026 16:12:12 GMT  
		Size: 6.0 MB (5964595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b71158efc942b40e496205c76cbb8ad0980bc9d7d44ec3bbabd6be9068c9acad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39b14348c59fd4c68e56a6b3993caf73d1de83a4bf32b3c4f42f1e45913dbd3`

```dockerfile
```

-	Layers:
	-	`sha256:58a49e99d73072d878df8c1f584d36ab8228edbea9c6e74afc2c9cc78323ae73`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:e35294278ff76bcb1fe56374110f4b06c269576ed7790035cb884905514779bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f361bf360d8325e6fcd51b413da8e62bc9d3349d5ffa47ce66c77b64b681ec30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9078b3e5e7cd72051df8071c386cbf0335d800dad99509157ffcfd8f4fc361`  
		Last Modified: Fri, 17 Apr 2026 03:00:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f7b77c54d8013e193fe1637d61d70596d15af7f467886c746e4990c02b80a60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcd2c9c3f0905b48a181ecb2c54e99817e889d09b559ccb3625163e3ddb9966`

```dockerfile
```

-	Layers:
	-	`sha256:553590c07c651e9bd4871f634514aac2810de7afce20d412adc0440624524452`  
		Last Modified: Fri, 17 Apr 2026 03:00:37 GMT  
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
$ docker pull nats@sha256:53e4bacf2ece7434816db894b8e378076666105b2c46a8bd42ff344e3b4bb4e3
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
$ docker pull nats@sha256:6026fcefbc8c47c2be01c22b3a8adbc42025c17cc928c009579e868ad7508b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6497607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcfa3f1357bff7c1c7510611163f749aebfe279ae866ab5a044e5e57c95c99b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:13:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:13:44 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:13:44 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:13:44 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:13:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:13:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9f0ebe5f9a1ae3ad639c8afca45fb722413353ade56a44dcf62bcfef80217dbb`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.5 MB (6497097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e1a3d878997721992626d968612830e36b2bf02e02b3328b3ac15759c0ea8b`  
		Last Modified: Fri, 17 Apr 2026 01:13:49 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8f27fed47cda974f867f1386700a6014a9ef5d590e1af2cf0ada26b3ae3e0bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58ce43223a92800c17c75cd47418a48eefaebdabbc17a285314e76f115fdb9a`

```dockerfile
```

-	Layers:
	-	`sha256:33bf04ede4f3a943ff024e5f12bce32c5a0bb9166748872e0ef22cf5880371bb`  
		Last Modified: Fri, 17 Apr 2026 01:13:48 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:2608cfbd354d33b2932a94dc2b47d3dbf341008a40d371a532df9ccfe27e6d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0a7010738d4da19f91e4851984e905ffb94ca75f74f7ad75cc38eee92db67b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ac4c14b3f8076df43f73c9299994bae9134a062823f58d1140353085aa0b300`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.2 MB (6218951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ac5d76972bd80e5cf01b62c77075191e2cbb49fae723136503f99e8bbd5f40`  
		Last Modified: Fri, 17 Apr 2026 01:12:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ba5ca70d7ca25a54873350a2eec247fdfbf818d63999e42204ff63fc7baba133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce46eb21add643afa47e6df6f20c6c2cbf05136e0948d3845137fff0575666e`

```dockerfile
```

-	Layers:
	-	`sha256:514ec24cb478e0f1b0db84a74f997f1697890c620f506018cafe047d8877ddc9`  
		Last Modified: Fri, 17 Apr 2026 01:12:33 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:50ed86b0111c027e65a30fb481e8905ac9a72718c5bfc9ae0bd7e9ba415f57d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad77b34c838e5f91c829d1a936243ad9ef7dece98be3ff3e381708b8fb828fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:43 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:43 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2a83fab97c651eacbf830fb7bd159907e5e14fda32f73c5628adf6899c32f67f`  
		Last Modified: Tue, 14 Apr 2026 16:12:11 GMT  
		Size: 6.2 MB (6208591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b4c7d8a44ca53c6ad494b2527e7b06e45cd0c74f651ee0c129f18d3ad5ad7b`  
		Last Modified: Fri, 17 Apr 2026 01:14:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4fe65a1f80a741422bd860b28fd48efab7f9cc6334306494e5a5be9f3f51ad61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0e3bb622be324aa20e50643edfe951dd8bf5117d3cb183797d4e4c524dedb9`

```dockerfile
```

-	Layers:
	-	`sha256:9bea04e9589cbb82cb5be1827548ae5b11d2b919d91c72d80684ce5c3c358417`  
		Last Modified: Fri, 17 Apr 2026 01:14:47 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc6d37d617039b414987344c5b51fa5e2013343f0a1b017a42a9b1f3a341fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827af36b416951d2b3da590c3dd45bc88d1d022bd97438a1c8a9a3592444158f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:20 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:20 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53e14ebbec1f96d7732d422be8ee7b587c333a423ac37b45d8cbe989c7ffe1ed`  
		Last Modified: Tue, 14 Apr 2026 16:12:13 GMT  
		Size: 5.9 MB (5915332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26776296d50b8eb0772a64317fbbfe8298dd48e5acfbf80b00f34a606f4ab307`  
		Last Modified: Fri, 17 Apr 2026 01:34:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ca8abe494d9e5c45013a55f63e3c336b7a648ad0645e1bebae8e9940e4ec4f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45ebf0e78412d9c83ec1c4b61db202bab3b503098bad7fe005e74cc0cf9d835`

```dockerfile
```

-	Layers:
	-	`sha256:f81079af62e66239b51e888dd23be34b9d7e9981a85be373ac54a2a655c7da92`  
		Last Modified: Fri, 17 Apr 2026 01:34:24 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:d473b23d3f76c223d24ebcb4d727b485952b8740d23d2f9adae98cec46090b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28940f6db27811588c31afbfe9d7f62cfa2bf5997035734a32059c51f1e15e51`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b63ce4825759431170974b945ec1ddea7f5665ed75cc067dc0285b5ece42ed12`  
		Last Modified: Tue, 14 Apr 2026 16:12:12 GMT  
		Size: 6.0 MB (5964595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b71158efc942b40e496205c76cbb8ad0980bc9d7d44ec3bbabd6be9068c9acad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39b14348c59fd4c68e56a6b3993caf73d1de83a4bf32b3c4f42f1e45913dbd3`

```dockerfile
```

-	Layers:
	-	`sha256:58a49e99d73072d878df8c1f584d36ab8228edbea9c6e74afc2c9cc78323ae73`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:e35294278ff76bcb1fe56374110f4b06c269576ed7790035cb884905514779bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f361bf360d8325e6fcd51b413da8e62bc9d3349d5ffa47ce66c77b64b681ec30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9078b3e5e7cd72051df8071c386cbf0335d800dad99509157ffcfd8f4fc361`  
		Last Modified: Fri, 17 Apr 2026 03:00:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f7b77c54d8013e193fe1637d61d70596d15af7f467886c746e4990c02b80a60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcd2c9c3f0905b48a181ecb2c54e99817e889d09b559ccb3625163e3ddb9966`

```dockerfile
```

-	Layers:
	-	`sha256:553590c07c651e9bd4871f634514aac2810de7afce20d412adc0440624524452`  
		Last Modified: Fri, 17 Apr 2026 03:00:37 GMT  
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
$ docker pull nats@sha256:8f093cb30e8bfed2eff4bbea70dfcbffd847be40ec674b9f7a7b9d26f41234b2
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
$ docker pull nats@sha256:6026fcefbc8c47c2be01c22b3a8adbc42025c17cc928c009579e868ad7508b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6497607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcfa3f1357bff7c1c7510611163f749aebfe279ae866ab5a044e5e57c95c99b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:13:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:13:44 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:13:44 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:13:44 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:13:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:13:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9f0ebe5f9a1ae3ad639c8afca45fb722413353ade56a44dcf62bcfef80217dbb`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.5 MB (6497097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e1a3d878997721992626d968612830e36b2bf02e02b3328b3ac15759c0ea8b`  
		Last Modified: Fri, 17 Apr 2026 01:13:49 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16` - unknown; unknown

```console
$ docker pull nats@sha256:8f27fed47cda974f867f1386700a6014a9ef5d590e1af2cf0ada26b3ae3e0bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58ce43223a92800c17c75cd47418a48eefaebdabbc17a285314e76f115fdb9a`

```dockerfile
```

-	Layers:
	-	`sha256:33bf04ede4f3a943ff024e5f12bce32c5a0bb9166748872e0ef22cf5880371bb`  
		Last Modified: Fri, 17 Apr 2026 01:13:48 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16` - linux; arm variant v6

```console
$ docker pull nats@sha256:2608cfbd354d33b2932a94dc2b47d3dbf341008a40d371a532df9ccfe27e6d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0a7010738d4da19f91e4851984e905ffb94ca75f74f7ad75cc38eee92db67b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ac4c14b3f8076df43f73c9299994bae9134a062823f58d1140353085aa0b300`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.2 MB (6218951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ac5d76972bd80e5cf01b62c77075191e2cbb49fae723136503f99e8bbd5f40`  
		Last Modified: Fri, 17 Apr 2026 01:12:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16` - unknown; unknown

```console
$ docker pull nats@sha256:ba5ca70d7ca25a54873350a2eec247fdfbf818d63999e42204ff63fc7baba133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce46eb21add643afa47e6df6f20c6c2cbf05136e0948d3845137fff0575666e`

```dockerfile
```

-	Layers:
	-	`sha256:514ec24cb478e0f1b0db84a74f997f1697890c620f506018cafe047d8877ddc9`  
		Last Modified: Fri, 17 Apr 2026 01:12:33 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16` - linux; arm variant v7

```console
$ docker pull nats@sha256:50ed86b0111c027e65a30fb481e8905ac9a72718c5bfc9ae0bd7e9ba415f57d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad77b34c838e5f91c829d1a936243ad9ef7dece98be3ff3e381708b8fb828fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:43 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:43 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2a83fab97c651eacbf830fb7bd159907e5e14fda32f73c5628adf6899c32f67f`  
		Last Modified: Tue, 14 Apr 2026 16:12:11 GMT  
		Size: 6.2 MB (6208591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b4c7d8a44ca53c6ad494b2527e7b06e45cd0c74f651ee0c129f18d3ad5ad7b`  
		Last Modified: Fri, 17 Apr 2026 01:14:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16` - unknown; unknown

```console
$ docker pull nats@sha256:4fe65a1f80a741422bd860b28fd48efab7f9cc6334306494e5a5be9f3f51ad61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0e3bb622be324aa20e50643edfe951dd8bf5117d3cb183797d4e4c524dedb9`

```dockerfile
```

-	Layers:
	-	`sha256:9bea04e9589cbb82cb5be1827548ae5b11d2b919d91c72d80684ce5c3c358417`  
		Last Modified: Fri, 17 Apr 2026 01:14:47 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc6d37d617039b414987344c5b51fa5e2013343f0a1b017a42a9b1f3a341fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827af36b416951d2b3da590c3dd45bc88d1d022bd97438a1c8a9a3592444158f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:20 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:20 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53e14ebbec1f96d7732d422be8ee7b587c333a423ac37b45d8cbe989c7ffe1ed`  
		Last Modified: Tue, 14 Apr 2026 16:12:13 GMT  
		Size: 5.9 MB (5915332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26776296d50b8eb0772a64317fbbfe8298dd48e5acfbf80b00f34a606f4ab307`  
		Last Modified: Fri, 17 Apr 2026 01:34:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16` - unknown; unknown

```console
$ docker pull nats@sha256:ca8abe494d9e5c45013a55f63e3c336b7a648ad0645e1bebae8e9940e4ec4f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45ebf0e78412d9c83ec1c4b61db202bab3b503098bad7fe005e74cc0cf9d835`

```dockerfile
```

-	Layers:
	-	`sha256:f81079af62e66239b51e888dd23be34b9d7e9981a85be373ac54a2a655c7da92`  
		Last Modified: Fri, 17 Apr 2026 01:34:24 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16` - linux; ppc64le

```console
$ docker pull nats@sha256:d473b23d3f76c223d24ebcb4d727b485952b8740d23d2f9adae98cec46090b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28940f6db27811588c31afbfe9d7f62cfa2bf5997035734a32059c51f1e15e51`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b63ce4825759431170974b945ec1ddea7f5665ed75cc067dc0285b5ece42ed12`  
		Last Modified: Tue, 14 Apr 2026 16:12:12 GMT  
		Size: 6.0 MB (5964595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16` - unknown; unknown

```console
$ docker pull nats@sha256:b71158efc942b40e496205c76cbb8ad0980bc9d7d44ec3bbabd6be9068c9acad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39b14348c59fd4c68e56a6b3993caf73d1de83a4bf32b3c4f42f1e45913dbd3`

```dockerfile
```

-	Layers:
	-	`sha256:58a49e99d73072d878df8c1f584d36ab8228edbea9c6e74afc2c9cc78323ae73`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16` - linux; s390x

```console
$ docker pull nats@sha256:e35294278ff76bcb1fe56374110f4b06c269576ed7790035cb884905514779bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f361bf360d8325e6fcd51b413da8e62bc9d3349d5ffa47ce66c77b64b681ec30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9078b3e5e7cd72051df8071c386cbf0335d800dad99509157ffcfd8f4fc361`  
		Last Modified: Fri, 17 Apr 2026 03:00:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16` - unknown; unknown

```console
$ docker pull nats@sha256:f7b77c54d8013e193fe1637d61d70596d15af7f467886c746e4990c02b80a60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcd2c9c3f0905b48a181ecb2c54e99817e889d09b559ccb3625163e3ddb9966`

```dockerfile
```

-	Layers:
	-	`sha256:553590c07c651e9bd4871f634514aac2810de7afce20d412adc0440624524452`  
		Last Modified: Fri, 17 Apr 2026 03:00:37 GMT  
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
$ docker pull nats@sha256:47169454fd238c3bd104f9947a6f84c1fb4713cd89ebf29da541ce53358fc298
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
$ docker pull nats@sha256:62cb3a8de632e3dfc2a90d75436361b4d9655f0e05b4ac6cdf288625f4f1e4e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10764196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f43e01dbd062a0d7445ccf07425daf97f3c9b131dfad1d83d461fd25d02efd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:33 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:33 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:33 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:33 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1549fe52811b163dad6363b19ed5b1dbef22580dc8ae8bdd81255aff0606a`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 7.0 MB (6955039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a5a095806d982618ddf3458b47c0baa71e872550911885ed97c871ef77c8e7`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f6f70f1098d315ac2b26d3cee22d86094f5b422b2da94051a8103c43aee3a1`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:37ec2d35b904a87b031d377ad0ae1e9ca58941a8bc07810544ff31a7b23fbf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb3b132e4c95883151904f270f848d226d65efb3e8b60f25e24fd40f2683dd1`

```dockerfile
```

-	Layers:
	-	`sha256:d66433550b59c3ff75c3899eec8b1ce426114a3d83be4442fb12653ec74633cc`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ade01f393bf6a62dbbf014521365a975fe801491c9d992f3f94a4abc44c106f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10183416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7bbe121c0a8795dff73d14514e795827a41ec26cb05a5e5892c478274e7706`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:14 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc48e8c2cd02fa0b377d3d44d3bcb287dbb8e23ae6c5a3312a9bc14a911d38`  
		Last Modified: Fri, 17 Apr 2026 00:15:18 GMT  
		Size: 6.7 MB (6675063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abaa56ee89bdb343291cbf0836ce0dc7e79d6e22d62ec1c716cc914ce78392a`  
		Last Modified: Fri, 17 Apr 2026 00:15:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76353b3690a868dfe403515baad9237d61a90c25d662c002b89a52b3f365651`  
		Last Modified: Fri, 17 Apr 2026 00:15:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6bcec4f288d3676b4f8445a15d0a5c6846f7500324ce4ab89720295c199e0a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d764686032a4d0e7b2fd5fd9c5fbcd156171954280332b878087488eed9f125`

```dockerfile
```

-	Layers:
	-	`sha256:b1902c9888c320fc05d5cf411a5ead25736ee29e8a75a4abf0d2a564f9e5e2af`  
		Last Modified: Fri, 17 Apr 2026 00:15:18 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:88a5786e1e232199af0d994f6238cd75f33a3ee619529c8a8d92a0f7e510e858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9892783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b72c9e361f2152192713775a37eb16526bc2a7eaf0d5794b8e626c49854ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:23 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:23 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8398c47bd6ae433e2f3bde40e5b7df392542d47b2ac820c799ec796860eece`  
		Last Modified: Fri, 17 Apr 2026 00:15:28 GMT  
		Size: 6.7 MB (6665982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e72553ddff68e46b6a6af6efc169ab89bda6adbe6e8ba8569efa24f73a9668e`  
		Last Modified: Fri, 17 Apr 2026 00:15:27 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8838dd2cec0e257fdb4d239e2cb2f9a8bf78861d335156509372ec8083f221d`  
		Last Modified: Fri, 17 Apr 2026 00:15:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d063fda2ce7d9f50f9682d64c4d08e3b6fb5ca3b3a9a7fdb28eb84198478a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fea9b0e1ac50a218f647545512fa8b99188d3691f302045aa4261dc115d0f28`

```dockerfile
```

-	Layers:
	-	`sha256:3e9156041859edf9dc260aa9723eaf36a8da562e34800f44246c2269f6a71001`  
		Last Modified: Fri, 17 Apr 2026 00:15:27 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b66ae5ec567a90f00ae8df30b7dbb3f4b21758b4a1bb851ad6e9e49f5459daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20967c1b8e8d3f14a25f79e551d609e7793330fa502e5352f98891698bc12747`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:48 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:48 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:48 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:48 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:48 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab00d275d537a0cf1bfff28ff033bfaaf1353fcb42866a4f07501d59d90bc7a`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 6.4 MB (6373171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47320975f8b7e1919afbb55c23e84d1c8ea6c173ea1cb0196d9e7b31a94c44bc`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d629ae6d1b6079aeef1b3945679b6dc9cc6abf4e879628c41fd27c3108e1229f`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:29d83cbe455749a4217796d3f569beb308a3ae52e0658fa438e0e06e31c9b61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd85bb55d9be014e8a3ae6ee5fe03a93c8c3804d371904c09b3f3c2bab691e22`

```dockerfile
```

-	Layers:
	-	`sha256:f93982492431d5153d601735002a6ab47c467a168b7014901e0a7a4d6269bb06`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:8117df0b7f4ad130b27d34b371e6c206b3d8b6a86bcdc42c3662c4bff6ed1913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10161336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5afbda650d00b3b63b8591f36292178fb8270a017753f74fa9bcea9bac0575f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:10 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:19:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:19:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:19:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:19:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:19:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93502a03a8dc6cb0bf0383513a9b456a73eb7c3b00be855656913a7cc49eedd7`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 6.4 MB (6423711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb736d1c701df89f81b8ed7ae7299183b39fe61f218ddd30c0827dd8b27de4`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634ed6629dc149c04e1521c52443e7a95aabdc4a0584471afb00b01ba37f9519`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a7a1b0415e793868f1d0860af59b5be0e593808ff727210f48fa836c9f8e5d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131ff907d57e77f9145cf7fa68644970173220c5e54f35168211ab4649dd7a8f`

```dockerfile
```

-	Layers:
	-	`sha256:d5007684d306b92f1cc83a2c33ce052b11c02462641285aa473582e754738278`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine` - linux; s390x

```console
$ docker pull nats@sha256:4665ef744eae958df06fa7f90eccf092c87b9303443dbe64df734d268c0d062d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10451115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c53ccc0e5f29509d8e8e600842f57455cf61213d9cbcbe173ebe2eb6eeb7268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:10 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:14:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:14:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:14:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:14:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:14:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:14:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f5ee94b985986baff103bfd91cf80667d3e192e194589c77442193ea9dd536`  
		Last Modified: Fri, 17 Apr 2026 00:14:19 GMT  
		Size: 6.8 MB (6796273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842a65e3e80f55672514dcef5e81832f7cebec6fe722429319b244893692ab1`  
		Last Modified: Fri, 17 Apr 2026 00:14:18 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d79d22c5b0229cae6cce00ca941a3ff246c9243200d12d1224eb8520af2d58`  
		Last Modified: Fri, 17 Apr 2026 00:14:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:58c5ef69555aa04c57d8b23c2ddc0e6b05dcb1eafb0e0e899ed80bdd8abc096d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec68f5a904cb0c482f67800cf10ae7beaa437942e0c7bc948843cf4f96f91a0b`

```dockerfile
```

-	Layers:
	-	`sha256:9f20b34e5ebc33ed80836487c456d86edc1d2473c21d8d5276688d09ca045a66`  
		Last Modified: Fri, 17 Apr 2026 00:14:18 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.16-alpine3.22`

```console
$ docker pull nats@sha256:47169454fd238c3bd104f9947a6f84c1fb4713cd89ebf29da541ce53358fc298
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
$ docker pull nats@sha256:62cb3a8de632e3dfc2a90d75436361b4d9655f0e05b4ac6cdf288625f4f1e4e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10764196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f43e01dbd062a0d7445ccf07425daf97f3c9b131dfad1d83d461fd25d02efd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:33 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:33 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:33 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:33 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:33 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:33 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea1549fe52811b163dad6363b19ed5b1dbef22580dc8ae8bdd81255aff0606a`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 7.0 MB (6955039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a5a095806d982618ddf3458b47c0baa71e872550911885ed97c871ef77c8e7`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f6f70f1098d315ac2b26d3cee22d86094f5b422b2da94051a8103c43aee3a1`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:37ec2d35b904a87b031d377ad0ae1e9ca58941a8bc07810544ff31a7b23fbf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb3b132e4c95883151904f270f848d226d65efb3e8b60f25e24fd40f2683dd1`

```dockerfile
```

-	Layers:
	-	`sha256:d66433550b59c3ff75c3899eec8b1ce426114a3d83be4442fb12653ec74633cc`  
		Last Modified: Fri, 17 Apr 2026 00:15:37 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:ade01f393bf6a62dbbf014521365a975fe801491c9d992f3f94a4abc44c106f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10183416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7bbe121c0a8795dff73d14514e795827a41ec26cb05a5e5892c478274e7706`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:14 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:14 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:14 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:14 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:14 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc48e8c2cd02fa0b377d3d44d3bcb287dbb8e23ae6c5a3312a9bc14a911d38`  
		Last Modified: Fri, 17 Apr 2026 00:15:18 GMT  
		Size: 6.7 MB (6675063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abaa56ee89bdb343291cbf0836ce0dc7e79d6e22d62ec1c716cc914ce78392a`  
		Last Modified: Fri, 17 Apr 2026 00:15:17 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76353b3690a868dfe403515baad9237d61a90c25d662c002b89a52b3f365651`  
		Last Modified: Fri, 17 Apr 2026 00:15:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6bcec4f288d3676b4f8445a15d0a5c6846f7500324ce4ab89720295c199e0a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d764686032a4d0e7b2fd5fd9c5fbcd156171954280332b878087488eed9f125`

```dockerfile
```

-	Layers:
	-	`sha256:b1902c9888c320fc05d5cf411a5ead25736ee29e8a75a4abf0d2a564f9e5e2af`  
		Last Modified: Fri, 17 Apr 2026 00:15:18 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:88a5786e1e232199af0d994f6238cd75f33a3ee619529c8a8d92a0f7e510e858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9892783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1b72c9e361f2152192713775a37eb16526bc2a7eaf0d5794b8e626c49854ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:23 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:23 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8398c47bd6ae433e2f3bde40e5b7df392542d47b2ac820c799ec796860eece`  
		Last Modified: Fri, 17 Apr 2026 00:15:28 GMT  
		Size: 6.7 MB (6665982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e72553ddff68e46b6a6af6efc169ab89bda6adbe6e8ba8569efa24f73a9668e`  
		Last Modified: Fri, 17 Apr 2026 00:15:27 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8838dd2cec0e257fdb4d239e2cb2f9a8bf78861d335156509372ec8083f221d`  
		Last Modified: Fri, 17 Apr 2026 00:15:27 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d063fda2ce7d9f50f9682d64c4d08e3b6fb5ca3b3a9a7fdb28eb84198478a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fea9b0e1ac50a218f647545512fa8b99188d3691f302045aa4261dc115d0f28`

```dockerfile
```

-	Layers:
	-	`sha256:3e9156041859edf9dc260aa9723eaf36a8da562e34800f44246c2269f6a71001`  
		Last Modified: Fri, 17 Apr 2026 00:15:27 GMT  
		Size: 14.3 KB (14289 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:b66ae5ec567a90f00ae8df30b7dbb3f4b21758b4a1bb851ad6e9e49f5459daef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20967c1b8e8d3f14a25f79e551d609e7793330fa502e5352f98891698bc12747`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:48 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:15:48 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:15:48 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:48 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:48 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:48 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:48 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab00d275d537a0cf1bfff28ff033bfaaf1353fcb42866a4f07501d59d90bc7a`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 6.4 MB (6373171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47320975f8b7e1919afbb55c23e84d1c8ea6c173ea1cb0196d9e7b31a94c44bc`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d629ae6d1b6079aeef1b3945679b6dc9cc6abf4e879628c41fd27c3108e1229f`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:29d83cbe455749a4217796d3f569beb308a3ae52e0658fa438e0e06e31c9b61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd85bb55d9be014e8a3ae6ee5fe03a93c8c3804d371904c09b3f3c2bab691e22`

```dockerfile
```

-	Layers:
	-	`sha256:f93982492431d5153d601735002a6ab47c467a168b7014901e0a7a4d6269bb06`  
		Last Modified: Fri, 17 Apr 2026 00:15:52 GMT  
		Size: 14.3 KB (14313 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:8117df0b7f4ad130b27d34b371e6c206b3d8b6a86bcdc42c3662c4bff6ed1913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10161336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5afbda650d00b3b63b8591f36292178fb8270a017753f74fa9bcea9bac0575f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:10 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:19:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:19:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:19:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:19:11 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:19:11 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:19:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93502a03a8dc6cb0bf0383513a9b456a73eb7c3b00be855656913a7cc49eedd7`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 6.4 MB (6423711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bb736d1c701df89f81b8ed7ae7299183b39fe61f218ddd30c0827dd8b27de4`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634ed6629dc149c04e1521c52443e7a95aabdc4a0584471afb00b01ba37f9519`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a7a1b0415e793868f1d0860af59b5be0e593808ff727210f48fa836c9f8e5d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131ff907d57e77f9145cf7fa68644970173220c5e54f35168211ab4649dd7a8f`

```dockerfile
```

-	Layers:
	-	`sha256:d5007684d306b92f1cc83a2c33ce052b11c02462641285aa473582e754738278`  
		Last Modified: Fri, 17 Apr 2026 00:19:19 GMT  
		Size: 14.3 KB (14253 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:4665ef744eae958df06fa7f90eccf092c87b9303443dbe64df734d268c0d062d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10451115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c53ccc0e5f29509d8e8e600842f57455cf61213d9cbcbe173ebe2eb6eeb7268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:10 GMT
ENV NATS_SERVER=2.11.16
# Fri, 17 Apr 2026 00:14:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.11.16
# Fri, 17 Apr 2026 00:14:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='db7822e823829414a66b81f0553d9acffc27d6576d66313d92366c9ea2e85afb' ;;     armhf) natsArch='arm6'; sha256='77715f8c48eb3223e03bf814e98c7783f41d9476b61761ebb875d0070ab1f89c' ;;     armv7) natsArch='arm7'; sha256='98356346374d7a6b43910aa977e9b322b9c19638d666a5ff512efb5d3a46e7b8' ;;     x86_64) natsArch='amd64'; sha256='90b1a5d5c379e68862018b8eb731ef20bda9da86a33b7432f5d58e3dd14a9230' ;;     x86) natsArch='386'; sha256='e6ff1d7b6eaa5ab05197ffe5f125b528b2be9a317214c0206f49c9874939f8b5' ;;     s390x) natsArch='s390x'; sha256='b003d96583150ac7ce3091bb06e5e31a6e40e83929381bfa4909d27b45b85e31' ;;     ppc64le) natsArch='ppc64le'; sha256='8e7f8335b7c4e82930507e4c0326ef2711e073782f034b892a204613e41f974c' ;;     loong64) natsArch='loong64'; sha256='16ecea37b754306b07477d5f747f67a5bad18ccf0e47f7f11e51b4872f4935ca' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:14:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:14:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:14:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:14:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f5ee94b985986baff103bfd91cf80667d3e192e194589c77442193ea9dd536`  
		Last Modified: Fri, 17 Apr 2026 00:14:19 GMT  
		Size: 6.8 MB (6796273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842a65e3e80f55672514dcef5e81832f7cebec6fe722429319b244893692ab1`  
		Last Modified: Fri, 17 Apr 2026 00:14:18 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d79d22c5b0229cae6cce00ca941a3ff246c9243200d12d1224eb8520af2d58`  
		Last Modified: Fri, 17 Apr 2026 00:14:18 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:58c5ef69555aa04c57d8b23c2ddc0e6b05dcb1eafb0e0e899ed80bdd8abc096d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec68f5a904cb0c482f67800cf10ae7beaa437942e0c7bc948843cf4f96f91a0b`

```dockerfile
```

-	Layers:
	-	`sha256:9f20b34e5ebc33ed80836487c456d86edc1d2473c21d8d5276688d09ca045a66`  
		Last Modified: Fri, 17 Apr 2026 00:14:18 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.16-linux`

```console
$ docker pull nats@sha256:53e4bacf2ece7434816db894b8e378076666105b2c46a8bd42ff344e3b4bb4e3
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
$ docker pull nats@sha256:6026fcefbc8c47c2be01c22b3a8adbc42025c17cc928c009579e868ad7508b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6497607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcfa3f1357bff7c1c7510611163f749aebfe279ae866ab5a044e5e57c95c99b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:13:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:13:44 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:13:44 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:13:44 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:13:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:13:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9f0ebe5f9a1ae3ad639c8afca45fb722413353ade56a44dcf62bcfef80217dbb`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.5 MB (6497097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e1a3d878997721992626d968612830e36b2bf02e02b3328b3ac15759c0ea8b`  
		Last Modified: Fri, 17 Apr 2026 01:13:49 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8f27fed47cda974f867f1386700a6014a9ef5d590e1af2cf0ada26b3ae3e0bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58ce43223a92800c17c75cd47418a48eefaebdabbc17a285314e76f115fdb9a`

```dockerfile
```

-	Layers:
	-	`sha256:33bf04ede4f3a943ff024e5f12bce32c5a0bb9166748872e0ef22cf5880371bb`  
		Last Modified: Fri, 17 Apr 2026 01:13:48 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:2608cfbd354d33b2932a94dc2b47d3dbf341008a40d371a532df9ccfe27e6d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0a7010738d4da19f91e4851984e905ffb94ca75f74f7ad75cc38eee92db67b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ac4c14b3f8076df43f73c9299994bae9134a062823f58d1140353085aa0b300`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.2 MB (6218951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ac5d76972bd80e5cf01b62c77075191e2cbb49fae723136503f99e8bbd5f40`  
		Last Modified: Fri, 17 Apr 2026 01:12:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ba5ca70d7ca25a54873350a2eec247fdfbf818d63999e42204ff63fc7baba133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce46eb21add643afa47e6df6f20c6c2cbf05136e0948d3845137fff0575666e`

```dockerfile
```

-	Layers:
	-	`sha256:514ec24cb478e0f1b0db84a74f997f1697890c620f506018cafe047d8877ddc9`  
		Last Modified: Fri, 17 Apr 2026 01:12:33 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:50ed86b0111c027e65a30fb481e8905ac9a72718c5bfc9ae0bd7e9ba415f57d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad77b34c838e5f91c829d1a936243ad9ef7dece98be3ff3e381708b8fb828fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:43 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:43 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2a83fab97c651eacbf830fb7bd159907e5e14fda32f73c5628adf6899c32f67f`  
		Last Modified: Tue, 14 Apr 2026 16:12:11 GMT  
		Size: 6.2 MB (6208591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b4c7d8a44ca53c6ad494b2527e7b06e45cd0c74f651ee0c129f18d3ad5ad7b`  
		Last Modified: Fri, 17 Apr 2026 01:14:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4fe65a1f80a741422bd860b28fd48efab7f9cc6334306494e5a5be9f3f51ad61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0e3bb622be324aa20e50643edfe951dd8bf5117d3cb183797d4e4c524dedb9`

```dockerfile
```

-	Layers:
	-	`sha256:9bea04e9589cbb82cb5be1827548ae5b11d2b919d91c72d80684ce5c3c358417`  
		Last Modified: Fri, 17 Apr 2026 01:14:47 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc6d37d617039b414987344c5b51fa5e2013343f0a1b017a42a9b1f3a341fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827af36b416951d2b3da590c3dd45bc88d1d022bd97438a1c8a9a3592444158f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:20 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:20 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53e14ebbec1f96d7732d422be8ee7b587c333a423ac37b45d8cbe989c7ffe1ed`  
		Last Modified: Tue, 14 Apr 2026 16:12:13 GMT  
		Size: 5.9 MB (5915332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26776296d50b8eb0772a64317fbbfe8298dd48e5acfbf80b00f34a606f4ab307`  
		Last Modified: Fri, 17 Apr 2026 01:34:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-linux` - unknown; unknown

```console
$ docker pull nats@sha256:ca8abe494d9e5c45013a55f63e3c336b7a648ad0645e1bebae8e9940e4ec4f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45ebf0e78412d9c83ec1c4b61db202bab3b503098bad7fe005e74cc0cf9d835`

```dockerfile
```

-	Layers:
	-	`sha256:f81079af62e66239b51e888dd23be34b9d7e9981a85be373ac54a2a655c7da92`  
		Last Modified: Fri, 17 Apr 2026 01:34:24 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:d473b23d3f76c223d24ebcb4d727b485952b8740d23d2f9adae98cec46090b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28940f6db27811588c31afbfe9d7f62cfa2bf5997035734a32059c51f1e15e51`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b63ce4825759431170974b945ec1ddea7f5665ed75cc067dc0285b5ece42ed12`  
		Last Modified: Tue, 14 Apr 2026 16:12:12 GMT  
		Size: 6.0 MB (5964595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b71158efc942b40e496205c76cbb8ad0980bc9d7d44ec3bbabd6be9068c9acad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39b14348c59fd4c68e56a6b3993caf73d1de83a4bf32b3c4f42f1e45913dbd3`

```dockerfile
```

-	Layers:
	-	`sha256:58a49e99d73072d878df8c1f584d36ab8228edbea9c6e74afc2c9cc78323ae73`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-linux` - linux; s390x

```console
$ docker pull nats@sha256:e35294278ff76bcb1fe56374110f4b06c269576ed7790035cb884905514779bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f361bf360d8325e6fcd51b413da8e62bc9d3349d5ffa47ce66c77b64b681ec30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9078b3e5e7cd72051df8071c386cbf0335d800dad99509157ffcfd8f4fc361`  
		Last Modified: Fri, 17 Apr 2026 03:00:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f7b77c54d8013e193fe1637d61d70596d15af7f467886c746e4990c02b80a60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcd2c9c3f0905b48a181ecb2c54e99817e889d09b559ccb3625163e3ddb9966`

```dockerfile
```

-	Layers:
	-	`sha256:553590c07c651e9bd4871f634514aac2810de7afce20d412adc0440624524452`  
		Last Modified: Fri, 17 Apr 2026 03:00:37 GMT  
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
$ docker pull nats@sha256:53e4bacf2ece7434816db894b8e378076666105b2c46a8bd42ff344e3b4bb4e3
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
$ docker pull nats@sha256:6026fcefbc8c47c2be01c22b3a8adbc42025c17cc928c009579e868ad7508b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6497607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcfa3f1357bff7c1c7510611163f749aebfe279ae866ab5a044e5e57c95c99b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:13:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:13:44 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:13:44 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:13:44 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:13:44 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:13:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9f0ebe5f9a1ae3ad639c8afca45fb722413353ade56a44dcf62bcfef80217dbb`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.5 MB (6497097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e1a3d878997721992626d968612830e36b2bf02e02b3328b3ac15759c0ea8b`  
		Last Modified: Fri, 17 Apr 2026 01:13:49 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8f27fed47cda974f867f1386700a6014a9ef5d590e1af2cf0ada26b3ae3e0bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58ce43223a92800c17c75cd47418a48eefaebdabbc17a285314e76f115fdb9a`

```dockerfile
```

-	Layers:
	-	`sha256:33bf04ede4f3a943ff024e5f12bce32c5a0bb9166748872e0ef22cf5880371bb`  
		Last Modified: Fri, 17 Apr 2026 01:13:48 GMT  
		Size: 8.7 KB (8668 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:2608cfbd354d33b2932a94dc2b47d3dbf341008a40d371a532df9ccfe27e6d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0a7010738d4da19f91e4851984e905ffb94ca75f74f7ad75cc38eee92db67b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:29 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:29 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:29 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4ac4c14b3f8076df43f73c9299994bae9134a062823f58d1140353085aa0b300`  
		Last Modified: Tue, 14 Apr 2026 16:12:16 GMT  
		Size: 6.2 MB (6218951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ac5d76972bd80e5cf01b62c77075191e2cbb49fae723136503f99e8bbd5f40`  
		Last Modified: Fri, 17 Apr 2026 01:12:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ba5ca70d7ca25a54873350a2eec247fdfbf818d63999e42204ff63fc7baba133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce46eb21add643afa47e6df6f20c6c2cbf05136e0948d3845137fff0575666e`

```dockerfile
```

-	Layers:
	-	`sha256:514ec24cb478e0f1b0db84a74f997f1697890c620f506018cafe047d8877ddc9`  
		Last Modified: Fri, 17 Apr 2026 01:12:33 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:50ed86b0111c027e65a30fb481e8905ac9a72718c5bfc9ae0bd7e9ba415f57d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad77b34c838e5f91c829d1a936243ad9ef7dece98be3ff3e381708b8fb828fa`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:43 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:43 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:43 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:43 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:43 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2a83fab97c651eacbf830fb7bd159907e5e14fda32f73c5628adf6899c32f67f`  
		Last Modified: Tue, 14 Apr 2026 16:12:11 GMT  
		Size: 6.2 MB (6208591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b4c7d8a44ca53c6ad494b2527e7b06e45cd0c74f651ee0c129f18d3ad5ad7b`  
		Last Modified: Fri, 17 Apr 2026 01:14:47 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4fe65a1f80a741422bd860b28fd48efab7f9cc6334306494e5a5be9f3f51ad61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0e3bb622be324aa20e50643edfe951dd8bf5117d3cb183797d4e4c524dedb9`

```dockerfile
```

-	Layers:
	-	`sha256:9bea04e9589cbb82cb5be1827548ae5b11d2b919d91c72d80684ce5c3c358417`  
		Last Modified: Fri, 17 Apr 2026 01:14:47 GMT  
		Size: 8.8 KB (8750 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cc6d37d617039b414987344c5b51fa5e2013343f0a1b017a42a9b1f3a341fe6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:827af36b416951d2b3da590c3dd45bc88d1d022bd97438a1c8a9a3592444158f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:20 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:20 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:20 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:20 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:20 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:53e14ebbec1f96d7732d422be8ee7b587c333a423ac37b45d8cbe989c7ffe1ed`  
		Last Modified: Tue, 14 Apr 2026 16:12:13 GMT  
		Size: 5.9 MB (5915332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26776296d50b8eb0772a64317fbbfe8298dd48e5acfbf80b00f34a606f4ab307`  
		Last Modified: Fri, 17 Apr 2026 01:34:24 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:ca8abe494d9e5c45013a55f63e3c336b7a648ad0645e1bebae8e9940e4ec4f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45ebf0e78412d9c83ec1c4b61db202bab3b503098bad7fe005e74cc0cf9d835`

```dockerfile
```

-	Layers:
	-	`sha256:f81079af62e66239b51e888dd23be34b9d7e9981a85be373ac54a2a655c7da92`  
		Last Modified: Fri, 17 Apr 2026 01:34:24 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:d473b23d3f76c223d24ebcb4d727b485952b8740d23d2f9adae98cec46090b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5965103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28940f6db27811588c31afbfe9d7f62cfa2bf5997035734a32059c51f1e15e51`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b63ce4825759431170974b945ec1ddea7f5665ed75cc067dc0285b5ece42ed12`  
		Last Modified: Tue, 14 Apr 2026 16:12:12 GMT  
		Size: 6.0 MB (5964595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:b71158efc942b40e496205c76cbb8ad0980bc9d7d44ec3bbabd6be9068c9acad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39b14348c59fd4c68e56a6b3993caf73d1de83a4bf32b3c4f42f1e45913dbd3`

```dockerfile
```

-	Layers:
	-	`sha256:58a49e99d73072d878df8c1f584d36ab8228edbea9c6e74afc2c9cc78323ae73`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.16-scratch` - linux; s390x

```console
$ docker pull nats@sha256:e35294278ff76bcb1fe56374110f4b06c269576ed7790035cb884905514779bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f361bf360d8325e6fcd51b413da8e62bc9d3349d5ffa47ce66c77b64b681ec30`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:29 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:30 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:30 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:630a731dec28ccf09693a05b2ed94a0f0cae3d0344b892c6e9cbc6089699e7fc`  
		Last Modified: Tue, 14 Apr 2026 16:12:17 GMT  
		Size: 6.3 MB (6337424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9078b3e5e7cd72051df8071c386cbf0335d800dad99509157ffcfd8f4fc361`  
		Last Modified: Fri, 17 Apr 2026 03:00:44 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.16-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f7b77c54d8013e193fe1637d61d70596d15af7f467886c746e4990c02b80a60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcd2c9c3f0905b48a181ecb2c54e99817e889d09b559ccb3625163e3ddb9966`

```dockerfile
```

-	Layers:
	-	`sha256:553590c07c651e9bd4871f634514aac2810de7afce20d412adc0440624524452`  
		Last Modified: Fri, 17 Apr 2026 03:00:37 GMT  
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
$ docker pull nats@sha256:c9e19fc4f9d0b36f9d2da3175ce3c95220806d098c24d328feb869886ab4afef
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
$ docker pull nats@sha256:391f0072ce67ee55b761370c314dbc8a7281473e0bfda3ac659049f1b08075a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95d5bca384b7959bb5cf1a743a13f85be65a9488c0552f4df4cec87389b3200`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:57 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e87fa5d12be7bc0f44b53fa6cd141e76f56faef2467d8d9769be47ac8a3674`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:7c0366118c1dc0312ba0da7857982f13047f2ec8f1fe47820ae2510cc388c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f6f9d105ca7c46470f68af2b4271f0ed40ff0ad556161424e05e3a8ecaa28`

```dockerfile
```

-	Layers:
	-	`sha256:334dab01a895b2d00e9ac0e339855e2a15daf4569eef8b6a44197b75ed20f62f`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea3c1af26c064464b8f6bca423596b7220fa93816adaf83f706c9ae34b91985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37732cf595594fea3845c95390a620ae7b6486b55c225260d9a94cf8aa1c3191`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34d7930b8b8e75da31eb1b797ef0912c6853bdc85ad347e1b797a5634d3577`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:8e85b848d4b99afd92319210009a21f0052594311083d77fcf1ee8d6cab7cd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd733e47fb31591cc226c0a9aeceff2ca10b4207b7a4381cdd83879112bed1e8`

```dockerfile
```

-	Layers:
	-	`sha256:9705c11af89c00eef360d7c22c0fee24c5db2d4c6b9c7611bfc6452b12f7eb79`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3a84a8d961bad8bad4fe7fb65dee444f2a66a059b8558ae8fb65574034a28e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9ca91358bfb3db35540bfd10f98b46899bfd81947a3e7c8034dbdccd3698e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1cc2ded7c5a3d7e8d9680c305f87bde0af7613fd1da0bd9f7b3f4b28528afd`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:d2dc28bfb63659ddc44a14336f01f50ae3f3163b738ec04ce8fe354eb7cb0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdc86cc80dfedb4387659a7fa450f4216ffa6e6ac70823bfe739ccd9ed6902`

```dockerfile
```

-	Layers:
	-	`sha256:a28c5e1d2bd63600380e93535a5184c2c136a6aceb6cb7955e7d0e27563e1515`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:67c19494d70d06a12fdb38cf1be9df8ac8c003f1a8b236cd006d98ecc44c1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb010d3d2ef36bf55d9822e7505d72bc8749b4c81f49fa8347f6bc0170c6fe0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:16 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986e74a3c2ed133ac9088b767d56152dbe9ab65a416b04c81b00818be1ea963b`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:360bbf5808469578c04388e925785d45de711f2e0721b45aaf6f69dd5d197235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc87059696946491f60585793b3ae1fb94f85c1837a552ee798c7fd04d8c20f5`

```dockerfile
```

-	Layers:
	-	`sha256:3df5561b2a5a1ba9b17f6deec10fced17cc1921bad7497afc9fa646a3ee3e06a`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; ppc64le

```console
$ docker pull nats@sha256:b7d4c7253edb794c82e7dfed2c9cfa02dfd904e51f74f28ba31e047f62fc7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6ccedb2bd06fad337c3208934e55614b5dce7689fdc624d7c1ea46585b0910`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:150a2bdf7ca081074b6337f2c6a2ce949012f032b621816bf7d9518a4c9c8b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0e2cf0c979f91dcf610709e731f9d2524dd2a0d1270d5f0b2d331e8e5cce5`

```dockerfile
```

-	Layers:
	-	`sha256:71e0f2fc0ec84444d3f17187d21565a2004ebcf91fc6379221afe6b5f292aff3`  
		Last Modified: Fri, 17 Apr 2026 02:08:48 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
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
$ docker pull nats@sha256:e602ceca19bddc3dd7197b4b1afde53a16cd9d31a5500a8ae5620f36cb01963c
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
$ docker pull nats@sha256:16179be8b1ec51f6e587273a8f77f42773ea1f12228ad777764d971e7b43c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10911201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9559d6064637f63c271167a9d7c010ff5364b1eec2b0208599b50488ba703d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7a1e64c52df3467627e6d1c644bcb8211343cd68dddf6166bdffbccaf244fd`  
		Last Modified: Fri, 17 Apr 2026 00:15:33 GMT  
		Size: 7.1 MB (7102043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029b2f91063f4996b4cd7e46a633ab1a441fa1b56b1f99ed0b8451abeca076cb`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d704923a1249776a808f8aeafbe1adf7092d06b738b33f076cad79dcad5cf25`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ca41342c8a71a1155058491c46bc3acc5e7cdb6651860972e62fb3c748ab050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d7c6232cacba47988be2ed2b963902987d654145e91fa75e175f098bdbdb14`

```dockerfile
```

-	Layers:
	-	`sha256:dc14f6b45ffd0cf094851f620d7c09a23513353217e1640bd80f9752ae64eb67`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:46f43a77c9d9be15ca3b2787d01a7fc76c0ad5c1f84b62acdfe9c75bdf2364cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1b5fcf3af1aec5f8186371ced026734b0dc358f81fd79977d24923f55da091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52664fd029115b59e10665beb1de4db22437397f1e12d9ef21a10227a4bcb0b3`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 6.8 MB (6821275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a63f62b766f87fc00d415fb393198a177ca29d74ef894de1081a534644c51f`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42627bd4fc0b9abb95a7fe4472894e86dac74bcfafc35397fe46a8b51863a24b`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:02712ae3dfd268f7c0f286d515e88ffd04661bd2afa30df5ef55d8c1251c2d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc157db9d7cfbdfb06f25ffab6be682d8f329dbd5cb945f440a0b934ff633ae`

```dockerfile
```

-	Layers:
	-	`sha256:3921d54fa2bad5abd1ccb3ba03fdde77fb3342fb0c2f5f4ae861e1142b27e559`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:dc95c9071c61ae217f8b7ccc6c6cc4ed7135efd907ab216185d7a046f848263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edceff3cd31a9ba3c0916ec5a29e6f96072c9da161efff71263cdbd8bb621fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3ef39893803a1aa71385b7b4a0e2f2489c1714926ebc5a17f0f283f992c574`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 6.8 MB (6812139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05c0dd84c92bf393d4eeb2e08cb836caae1367d08914ed39ee6012bc7979eb`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5b69ca76cd026d2a3a3104034ad0bcde0f0a1ff1a54e334a1d5f2b7aa2ce0`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a096ab49bf85fe59d54ca81110922ea5bdd2e0d348e69d0f6025e938b39f26b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af01ae40e078b504a99160d21be1719bf0893debfd46c721e0f3f1b5fb2b8d88`

```dockerfile
```

-	Layers:
	-	`sha256:23e4cd5325bfcff95bbb97f89ba5f6e6dc0407032e7c0fb1cde3ad1ac6830a7b`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb1c336dc892313409a8a9be0bd058eeb502231aa3383b448d862253abe72660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10653076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7263323b7691f6bfc1ce77845e1493322e0a7fb05848ba9496d17994e3c358`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414ff6f42514787c192e710db9db418be359224a6173e1237a72689ab899901a`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 6.5 MB (6510214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bb42c58d7e11c558e5072fdac886e2e8d5119360c8339777bf525f6b3de3be`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f5a1bbeb5c096e363e206a3d729f50c23ae559b4b3d9fea208d0b170b4864d`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a80cf61114fd852a49cc7cc405df6566531f25fb08f1698e38110bd13b16bcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1eea64ca314ff49953a4d62c6f57c8921b550e4a65eef8447cab8789dafa98`

```dockerfile
```

-	Layers:
	-	`sha256:f96940dabf37dc5e896241d7598fd3bf014ea2f2dec81a8253215bce6dd38616`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:53b58d1e5ac5757d0090c9c82d6b43c4fa3983e2af4ada84b96a6431d7a6cad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2412c201b02e670a6c66daff1a839dbf8949e02fd7bab2be04cea5c1e0c738e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:02 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:19:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ed90b89f0799173e6fccc22fecf8ff6c8973c8ed4ff1831c68a7c7569b4cd`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 6.6 MB (6560526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac41c2bd3722584f61f21b39d46ec42523bd6ea86f211b9027e5acf3135de9`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49b420d0d646e4990b9696c25668a04fb23ae54be76f6897fbd49eae67b24c`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:35462817b467f61ebceb4eca3c0ac8d23fbdee1ba0b903f77d995d769a172ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f729ef5c8fed43aecc14c5a725ab776840e1a16f702f8496ef3b696338d2f4d3`

```dockerfile
```

-	Layers:
	-	`sha256:822b657516851096b98cd62907a761f8ccbbb44813254a0078eb31d4f272c619`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine` - linux; s390x

```console
$ docker pull nats@sha256:8dd0bb86b226ee0c00b11bee7e5402a505865da642006ff14293d14912b11e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10596317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2033c7f5d89abe8c752cd0bceac3d04d00854284c008645ba31f91ef04652287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7537aff86e4637878e5664a942467243a0f2cd0f3724bad313542c288b66619f`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 6.9 MB (6941474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c98718326853d62529f33a4745f08a21999d45bddc49bf4d4175feb2bd9c49`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5b57122821a0589eb6f05dc704b4f828e3060b27f5c6eeec2cad9b5b52bf3c`  
		Last Modified: Fri, 17 Apr 2026 00:13:46 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6a1b0dd4f10ca2f0dcfcd22ebcb04999217fcbf87ad066c7993d2a45e3970490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c0a8646f0475362f0b87ffe0fba73b5631df8220475194d2849b657ea3b049`

```dockerfile
```

-	Layers:
	-	`sha256:a85160fd978747e6ebfeae736628c48024e7b74f2f00bc194d8b8fb7b1c81552`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-alpine3.22`

```console
$ docker pull nats@sha256:e602ceca19bddc3dd7197b4b1afde53a16cd9d31a5500a8ae5620f36cb01963c
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
$ docker pull nats@sha256:16179be8b1ec51f6e587273a8f77f42773ea1f12228ad777764d971e7b43c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10911201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9559d6064637f63c271167a9d7c010ff5364b1eec2b0208599b50488ba703d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7a1e64c52df3467627e6d1c644bcb8211343cd68dddf6166bdffbccaf244fd`  
		Last Modified: Fri, 17 Apr 2026 00:15:33 GMT  
		Size: 7.1 MB (7102043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029b2f91063f4996b4cd7e46a633ab1a441fa1b56b1f99ed0b8451abeca076cb`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d704923a1249776a808f8aeafbe1adf7092d06b738b33f076cad79dcad5cf25`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ca41342c8a71a1155058491c46bc3acc5e7cdb6651860972e62fb3c748ab050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d7c6232cacba47988be2ed2b963902987d654145e91fa75e175f098bdbdb14`

```dockerfile
```

-	Layers:
	-	`sha256:dc14f6b45ffd0cf094851f620d7c09a23513353217e1640bd80f9752ae64eb67`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:46f43a77c9d9be15ca3b2787d01a7fc76c0ad5c1f84b62acdfe9c75bdf2364cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1b5fcf3af1aec5f8186371ced026734b0dc358f81fd79977d24923f55da091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52664fd029115b59e10665beb1de4db22437397f1e12d9ef21a10227a4bcb0b3`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 6.8 MB (6821275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a63f62b766f87fc00d415fb393198a177ca29d74ef894de1081a534644c51f`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42627bd4fc0b9abb95a7fe4472894e86dac74bcfafc35397fe46a8b51863a24b`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:02712ae3dfd268f7c0f286d515e88ffd04661bd2afa30df5ef55d8c1251c2d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc157db9d7cfbdfb06f25ffab6be682d8f329dbd5cb945f440a0b934ff633ae`

```dockerfile
```

-	Layers:
	-	`sha256:3921d54fa2bad5abd1ccb3ba03fdde77fb3342fb0c2f5f4ae861e1142b27e559`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:dc95c9071c61ae217f8b7ccc6c6cc4ed7135efd907ab216185d7a046f848263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edceff3cd31a9ba3c0916ec5a29e6f96072c9da161efff71263cdbd8bb621fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3ef39893803a1aa71385b7b4a0e2f2489c1714926ebc5a17f0f283f992c574`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 6.8 MB (6812139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05c0dd84c92bf393d4eeb2e08cb836caae1367d08914ed39ee6012bc7979eb`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5b69ca76cd026d2a3a3104034ad0bcde0f0a1ff1a54e334a1d5f2b7aa2ce0`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a096ab49bf85fe59d54ca81110922ea5bdd2e0d348e69d0f6025e938b39f26b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af01ae40e078b504a99160d21be1719bf0893debfd46c721e0f3f1b5fb2b8d88`

```dockerfile
```

-	Layers:
	-	`sha256:23e4cd5325bfcff95bbb97f89ba5f6e6dc0407032e7c0fb1cde3ad1ac6830a7b`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb1c336dc892313409a8a9be0bd058eeb502231aa3383b448d862253abe72660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10653076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7263323b7691f6bfc1ce77845e1493322e0a7fb05848ba9496d17994e3c358`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414ff6f42514787c192e710db9db418be359224a6173e1237a72689ab899901a`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 6.5 MB (6510214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bb42c58d7e11c558e5072fdac886e2e8d5119360c8339777bf525f6b3de3be`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f5a1bbeb5c096e363e206a3d729f50c23ae559b4b3d9fea208d0b170b4864d`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a80cf61114fd852a49cc7cc405df6566531f25fb08f1698e38110bd13b16bcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1eea64ca314ff49953a4d62c6f57c8921b550e4a65eef8447cab8789dafa98`

```dockerfile
```

-	Layers:
	-	`sha256:f96940dabf37dc5e896241d7598fd3bf014ea2f2dec81a8253215bce6dd38616`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:53b58d1e5ac5757d0090c9c82d6b43c4fa3983e2af4ada84b96a6431d7a6cad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2412c201b02e670a6c66daff1a839dbf8949e02fd7bab2be04cea5c1e0c738e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:02 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:19:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ed90b89f0799173e6fccc22fecf8ff6c8973c8ed4ff1831c68a7c7569b4cd`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 6.6 MB (6560526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac41c2bd3722584f61f21b39d46ec42523bd6ea86f211b9027e5acf3135de9`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49b420d0d646e4990b9696c25668a04fb23ae54be76f6897fbd49eae67b24c`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:35462817b467f61ebceb4eca3c0ac8d23fbdee1ba0b903f77d995d769a172ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f729ef5c8fed43aecc14c5a725ab776840e1a16f702f8496ef3b696338d2f4d3`

```dockerfile
```

-	Layers:
	-	`sha256:822b657516851096b98cd62907a761f8ccbbb44813254a0078eb31d4f272c619`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:8dd0bb86b226ee0c00b11bee7e5402a505865da642006ff14293d14912b11e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10596317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2033c7f5d89abe8c752cd0bceac3d04d00854284c008645ba31f91ef04652287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7537aff86e4637878e5664a942467243a0f2cd0f3724bad313542c288b66619f`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 6.9 MB (6941474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c98718326853d62529f33a4745f08a21999d45bddc49bf4d4175feb2bd9c49`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5b57122821a0589eb6f05dc704b4f828e3060b27f5c6eeec2cad9b5b52bf3c`  
		Last Modified: Fri, 17 Apr 2026 00:13:46 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6a1b0dd4f10ca2f0dcfcd22ebcb04999217fcbf87ad066c7993d2a45e3970490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c0a8646f0475362f0b87ffe0fba73b5631df8220475194d2849b657ea3b049`

```dockerfile
```

-	Layers:
	-	`sha256:a85160fd978747e6ebfeae736628c48024e7b74f2f00bc194d8b8fb7b1c81552`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12-linux`

```console
$ docker pull nats@sha256:dbda35114cbb4890d9ee9ff85c1328bbdce97e1ae72ea36d681ef6dcf972d202
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
$ docker pull nats@sha256:391f0072ce67ee55b761370c314dbc8a7281473e0bfda3ac659049f1b08075a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95d5bca384b7959bb5cf1a743a13f85be65a9488c0552f4df4cec87389b3200`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:57 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e87fa5d12be7bc0f44b53fa6cd141e76f56faef2467d8d9769be47ac8a3674`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7c0366118c1dc0312ba0da7857982f13047f2ec8f1fe47820ae2510cc388c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f6f9d105ca7c46470f68af2b4271f0ed40ff0ad556161424e05e3a8ecaa28`

```dockerfile
```

-	Layers:
	-	`sha256:334dab01a895b2d00e9ac0e339855e2a15daf4569eef8b6a44197b75ed20f62f`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea3c1af26c064464b8f6bca423596b7220fa93816adaf83f706c9ae34b91985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37732cf595594fea3845c95390a620ae7b6486b55c225260d9a94cf8aa1c3191`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34d7930b8b8e75da31eb1b797ef0912c6853bdc85ad347e1b797a5634d3577`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8e85b848d4b99afd92319210009a21f0052594311083d77fcf1ee8d6cab7cd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd733e47fb31591cc226c0a9aeceff2ca10b4207b7a4381cdd83879112bed1e8`

```dockerfile
```

-	Layers:
	-	`sha256:9705c11af89c00eef360d7c22c0fee24c5db2d4c6b9c7611bfc6452b12f7eb79`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3a84a8d961bad8bad4fe7fb65dee444f2a66a059b8558ae8fb65574034a28e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9ca91358bfb3db35540bfd10f98b46899bfd81947a3e7c8034dbdccd3698e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1cc2ded7c5a3d7e8d9680c305f87bde0af7613fd1da0bd9f7b3f4b28528afd`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d2dc28bfb63659ddc44a14336f01f50ae3f3163b738ec04ce8fe354eb7cb0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdc86cc80dfedb4387659a7fa450f4216ffa6e6ac70823bfe739ccd9ed6902`

```dockerfile
```

-	Layers:
	-	`sha256:a28c5e1d2bd63600380e93535a5184c2c136a6aceb6cb7955e7d0e27563e1515`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:67c19494d70d06a12fdb38cf1be9df8ac8c003f1a8b236cd006d98ecc44c1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb010d3d2ef36bf55d9822e7505d72bc8749b4c81f49fa8347f6bc0170c6fe0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:16 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986e74a3c2ed133ac9088b767d56152dbe9ab65a416b04c81b00818be1ea963b`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:360bbf5808469578c04388e925785d45de711f2e0721b45aaf6f69dd5d197235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc87059696946491f60585793b3ae1fb94f85c1837a552ee798c7fd04d8c20f5`

```dockerfile
```

-	Layers:
	-	`sha256:3df5561b2a5a1ba9b17f6deec10fced17cc1921bad7497afc9fa646a3ee3e06a`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:b7d4c7253edb794c82e7dfed2c9cfa02dfd904e51f74f28ba31e047f62fc7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6ccedb2bd06fad337c3208934e55614b5dce7689fdc624d7c1ea46585b0910`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:150a2bdf7ca081074b6337f2c6a2ce949012f032b621816bf7d9518a4c9c8b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0e2cf0c979f91dcf610709e731f9d2524dd2a0d1270d5f0b2d331e8e5cce5`

```dockerfile
```

-	Layers:
	-	`sha256:71e0f2fc0ec84444d3f17187d21565a2004ebcf91fc6379221afe6b5f292aff3`  
		Last Modified: Fri, 17 Apr 2026 02:08:48 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-linux` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
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
$ docker pull nats@sha256:dbda35114cbb4890d9ee9ff85c1328bbdce97e1ae72ea36d681ef6dcf972d202
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
$ docker pull nats@sha256:391f0072ce67ee55b761370c314dbc8a7281473e0bfda3ac659049f1b08075a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95d5bca384b7959bb5cf1a743a13f85be65a9488c0552f4df4cec87389b3200`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:57 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e87fa5d12be7bc0f44b53fa6cd141e76f56faef2467d8d9769be47ac8a3674`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7c0366118c1dc0312ba0da7857982f13047f2ec8f1fe47820ae2510cc388c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f6f9d105ca7c46470f68af2b4271f0ed40ff0ad556161424e05e3a8ecaa28`

```dockerfile
```

-	Layers:
	-	`sha256:334dab01a895b2d00e9ac0e339855e2a15daf4569eef8b6a44197b75ed20f62f`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea3c1af26c064464b8f6bca423596b7220fa93816adaf83f706c9ae34b91985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37732cf595594fea3845c95390a620ae7b6486b55c225260d9a94cf8aa1c3191`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34d7930b8b8e75da31eb1b797ef0912c6853bdc85ad347e1b797a5634d3577`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8e85b848d4b99afd92319210009a21f0052594311083d77fcf1ee8d6cab7cd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd733e47fb31591cc226c0a9aeceff2ca10b4207b7a4381cdd83879112bed1e8`

```dockerfile
```

-	Layers:
	-	`sha256:9705c11af89c00eef360d7c22c0fee24c5db2d4c6b9c7611bfc6452b12f7eb79`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3a84a8d961bad8bad4fe7fb65dee444f2a66a059b8558ae8fb65574034a28e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9ca91358bfb3db35540bfd10f98b46899bfd81947a3e7c8034dbdccd3698e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1cc2ded7c5a3d7e8d9680c305f87bde0af7613fd1da0bd9f7b3f4b28528afd`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d2dc28bfb63659ddc44a14336f01f50ae3f3163b738ec04ce8fe354eb7cb0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdc86cc80dfedb4387659a7fa450f4216ffa6e6ac70823bfe739ccd9ed6902`

```dockerfile
```

-	Layers:
	-	`sha256:a28c5e1d2bd63600380e93535a5184c2c136a6aceb6cb7955e7d0e27563e1515`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:67c19494d70d06a12fdb38cf1be9df8ac8c003f1a8b236cd006d98ecc44c1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb010d3d2ef36bf55d9822e7505d72bc8749b4c81f49fa8347f6bc0170c6fe0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:16 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986e74a3c2ed133ac9088b767d56152dbe9ab65a416b04c81b00818be1ea963b`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:360bbf5808469578c04388e925785d45de711f2e0721b45aaf6f69dd5d197235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc87059696946491f60585793b3ae1fb94f85c1837a552ee798c7fd04d8c20f5`

```dockerfile
```

-	Layers:
	-	`sha256:3df5561b2a5a1ba9b17f6deec10fced17cc1921bad7497afc9fa646a3ee3e06a`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:b7d4c7253edb794c82e7dfed2c9cfa02dfd904e51f74f28ba31e047f62fc7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6ccedb2bd06fad337c3208934e55614b5dce7689fdc624d7c1ea46585b0910`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:150a2bdf7ca081074b6337f2c6a2ce949012f032b621816bf7d9518a4c9c8b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0e2cf0c979f91dcf610709e731f9d2524dd2a0d1270d5f0b2d331e8e5cce5`

```dockerfile
```

-	Layers:
	-	`sha256:71e0f2fc0ec84444d3f17187d21565a2004ebcf91fc6379221afe6b5f292aff3`  
		Last Modified: Fri, 17 Apr 2026 02:08:48 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12-scratch` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
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
$ docker pull nats@sha256:c9e19fc4f9d0b36f9d2da3175ce3c95220806d098c24d328feb869886ab4afef
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
$ docker pull nats@sha256:391f0072ce67ee55b761370c314dbc8a7281473e0bfda3ac659049f1b08075a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95d5bca384b7959bb5cf1a743a13f85be65a9488c0552f4df4cec87389b3200`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:57 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e87fa5d12be7bc0f44b53fa6cd141e76f56faef2467d8d9769be47ac8a3674`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7` - unknown; unknown

```console
$ docker pull nats@sha256:7c0366118c1dc0312ba0da7857982f13047f2ec8f1fe47820ae2510cc388c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f6f9d105ca7c46470f68af2b4271f0ed40ff0ad556161424e05e3a8ecaa28`

```dockerfile
```

-	Layers:
	-	`sha256:334dab01a895b2d00e9ac0e339855e2a15daf4569eef8b6a44197b75ed20f62f`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea3c1af26c064464b8f6bca423596b7220fa93816adaf83f706c9ae34b91985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37732cf595594fea3845c95390a620ae7b6486b55c225260d9a94cf8aa1c3191`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34d7930b8b8e75da31eb1b797ef0912c6853bdc85ad347e1b797a5634d3577`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7` - unknown; unknown

```console
$ docker pull nats@sha256:8e85b848d4b99afd92319210009a21f0052594311083d77fcf1ee8d6cab7cd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd733e47fb31591cc226c0a9aeceff2ca10b4207b7a4381cdd83879112bed1e8`

```dockerfile
```

-	Layers:
	-	`sha256:9705c11af89c00eef360d7c22c0fee24c5db2d4c6b9c7611bfc6452b12f7eb79`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3a84a8d961bad8bad4fe7fb65dee444f2a66a059b8558ae8fb65574034a28e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9ca91358bfb3db35540bfd10f98b46899bfd81947a3e7c8034dbdccd3698e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1cc2ded7c5a3d7e8d9680c305f87bde0af7613fd1da0bd9f7b3f4b28528afd`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7` - unknown; unknown

```console
$ docker pull nats@sha256:d2dc28bfb63659ddc44a14336f01f50ae3f3163b738ec04ce8fe354eb7cb0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdc86cc80dfedb4387659a7fa450f4216ffa6e6ac70823bfe739ccd9ed6902`

```dockerfile
```

-	Layers:
	-	`sha256:a28c5e1d2bd63600380e93535a5184c2c136a6aceb6cb7955e7d0e27563e1515`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:67c19494d70d06a12fdb38cf1be9df8ac8c003f1a8b236cd006d98ecc44c1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb010d3d2ef36bf55d9822e7505d72bc8749b4c81f49fa8347f6bc0170c6fe0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:16 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986e74a3c2ed133ac9088b767d56152dbe9ab65a416b04c81b00818be1ea963b`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7` - unknown; unknown

```console
$ docker pull nats@sha256:360bbf5808469578c04388e925785d45de711f2e0721b45aaf6f69dd5d197235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc87059696946491f60585793b3ae1fb94f85c1837a552ee798c7fd04d8c20f5`

```dockerfile
```

-	Layers:
	-	`sha256:3df5561b2a5a1ba9b17f6deec10fced17cc1921bad7497afc9fa646a3ee3e06a`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7` - linux; ppc64le

```console
$ docker pull nats@sha256:b7d4c7253edb794c82e7dfed2c9cfa02dfd904e51f74f28ba31e047f62fc7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6ccedb2bd06fad337c3208934e55614b5dce7689fdc624d7c1ea46585b0910`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7` - unknown; unknown

```console
$ docker pull nats@sha256:150a2bdf7ca081074b6337f2c6a2ce949012f032b621816bf7d9518a4c9c8b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0e2cf0c979f91dcf610709e731f9d2524dd2a0d1270d5f0b2d331e8e5cce5`

```dockerfile
```

-	Layers:
	-	`sha256:71e0f2fc0ec84444d3f17187d21565a2004ebcf91fc6379221afe6b5f292aff3`  
		Last Modified: Fri, 17 Apr 2026 02:08:48 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
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
$ docker pull nats@sha256:e602ceca19bddc3dd7197b4b1afde53a16cd9d31a5500a8ae5620f36cb01963c
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
$ docker pull nats@sha256:16179be8b1ec51f6e587273a8f77f42773ea1f12228ad777764d971e7b43c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10911201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9559d6064637f63c271167a9d7c010ff5364b1eec2b0208599b50488ba703d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7a1e64c52df3467627e6d1c644bcb8211343cd68dddf6166bdffbccaf244fd`  
		Last Modified: Fri, 17 Apr 2026 00:15:33 GMT  
		Size: 7.1 MB (7102043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029b2f91063f4996b4cd7e46a633ab1a441fa1b56b1f99ed0b8451abeca076cb`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d704923a1249776a808f8aeafbe1adf7092d06b738b33f076cad79dcad5cf25`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ca41342c8a71a1155058491c46bc3acc5e7cdb6651860972e62fb3c748ab050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d7c6232cacba47988be2ed2b963902987d654145e91fa75e175f098bdbdb14`

```dockerfile
```

-	Layers:
	-	`sha256:dc14f6b45ffd0cf094851f620d7c09a23513353217e1640bd80f9752ae64eb67`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:46f43a77c9d9be15ca3b2787d01a7fc76c0ad5c1f84b62acdfe9c75bdf2364cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1b5fcf3af1aec5f8186371ced026734b0dc358f81fd79977d24923f55da091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52664fd029115b59e10665beb1de4db22437397f1e12d9ef21a10227a4bcb0b3`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 6.8 MB (6821275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a63f62b766f87fc00d415fb393198a177ca29d74ef894de1081a534644c51f`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42627bd4fc0b9abb95a7fe4472894e86dac74bcfafc35397fe46a8b51863a24b`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:02712ae3dfd268f7c0f286d515e88ffd04661bd2afa30df5ef55d8c1251c2d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc157db9d7cfbdfb06f25ffab6be682d8f329dbd5cb945f440a0b934ff633ae`

```dockerfile
```

-	Layers:
	-	`sha256:3921d54fa2bad5abd1ccb3ba03fdde77fb3342fb0c2f5f4ae861e1142b27e559`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:dc95c9071c61ae217f8b7ccc6c6cc4ed7135efd907ab216185d7a046f848263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edceff3cd31a9ba3c0916ec5a29e6f96072c9da161efff71263cdbd8bb621fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3ef39893803a1aa71385b7b4a0e2f2489c1714926ebc5a17f0f283f992c574`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 6.8 MB (6812139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05c0dd84c92bf393d4eeb2e08cb836caae1367d08914ed39ee6012bc7979eb`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5b69ca76cd026d2a3a3104034ad0bcde0f0a1ff1a54e334a1d5f2b7aa2ce0`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a096ab49bf85fe59d54ca81110922ea5bdd2e0d348e69d0f6025e938b39f26b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af01ae40e078b504a99160d21be1719bf0893debfd46c721e0f3f1b5fb2b8d88`

```dockerfile
```

-	Layers:
	-	`sha256:23e4cd5325bfcff95bbb97f89ba5f6e6dc0407032e7c0fb1cde3ad1ac6830a7b`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb1c336dc892313409a8a9be0bd058eeb502231aa3383b448d862253abe72660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10653076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7263323b7691f6bfc1ce77845e1493322e0a7fb05848ba9496d17994e3c358`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414ff6f42514787c192e710db9db418be359224a6173e1237a72689ab899901a`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 6.5 MB (6510214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bb42c58d7e11c558e5072fdac886e2e8d5119360c8339777bf525f6b3de3be`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f5a1bbeb5c096e363e206a3d729f50c23ae559b4b3d9fea208d0b170b4864d`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a80cf61114fd852a49cc7cc405df6566531f25fb08f1698e38110bd13b16bcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1eea64ca314ff49953a4d62c6f57c8921b550e4a65eef8447cab8789dafa98`

```dockerfile
```

-	Layers:
	-	`sha256:f96940dabf37dc5e896241d7598fd3bf014ea2f2dec81a8253215bce6dd38616`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:53b58d1e5ac5757d0090c9c82d6b43c4fa3983e2af4ada84b96a6431d7a6cad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2412c201b02e670a6c66daff1a839dbf8949e02fd7bab2be04cea5c1e0c738e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:02 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:19:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ed90b89f0799173e6fccc22fecf8ff6c8973c8ed4ff1831c68a7c7569b4cd`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 6.6 MB (6560526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac41c2bd3722584f61f21b39d46ec42523bd6ea86f211b9027e5acf3135de9`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49b420d0d646e4990b9696c25668a04fb23ae54be76f6897fbd49eae67b24c`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:35462817b467f61ebceb4eca3c0ac8d23fbdee1ba0b903f77d995d769a172ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f729ef5c8fed43aecc14c5a725ab776840e1a16f702f8496ef3b696338d2f4d3`

```dockerfile
```

-	Layers:
	-	`sha256:822b657516851096b98cd62907a761f8ccbbb44813254a0078eb31d4f272c619`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine` - linux; s390x

```console
$ docker pull nats@sha256:8dd0bb86b226ee0c00b11bee7e5402a505865da642006ff14293d14912b11e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10596317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2033c7f5d89abe8c752cd0bceac3d04d00854284c008645ba31f91ef04652287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7537aff86e4637878e5664a942467243a0f2cd0f3724bad313542c288b66619f`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 6.9 MB (6941474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c98718326853d62529f33a4745f08a21999d45bddc49bf4d4175feb2bd9c49`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5b57122821a0589eb6f05dc704b4f828e3060b27f5c6eeec2cad9b5b52bf3c`  
		Last Modified: Fri, 17 Apr 2026 00:13:46 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6a1b0dd4f10ca2f0dcfcd22ebcb04999217fcbf87ad066c7993d2a45e3970490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c0a8646f0475362f0b87ffe0fba73b5631df8220475194d2849b657ea3b049`

```dockerfile
```

-	Layers:
	-	`sha256:a85160fd978747e6ebfeae736628c48024e7b74f2f00bc194d8b8fb7b1c81552`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.7-alpine3.22`

```console
$ docker pull nats@sha256:e602ceca19bddc3dd7197b4b1afde53a16cd9d31a5500a8ae5620f36cb01963c
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
$ docker pull nats@sha256:16179be8b1ec51f6e587273a8f77f42773ea1f12228ad777764d971e7b43c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10911201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9559d6064637f63c271167a9d7c010ff5364b1eec2b0208599b50488ba703d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7a1e64c52df3467627e6d1c644bcb8211343cd68dddf6166bdffbccaf244fd`  
		Last Modified: Fri, 17 Apr 2026 00:15:33 GMT  
		Size: 7.1 MB (7102043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029b2f91063f4996b4cd7e46a633ab1a441fa1b56b1f99ed0b8451abeca076cb`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d704923a1249776a808f8aeafbe1adf7092d06b738b33f076cad79dcad5cf25`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ca41342c8a71a1155058491c46bc3acc5e7cdb6651860972e62fb3c748ab050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d7c6232cacba47988be2ed2b963902987d654145e91fa75e175f098bdbdb14`

```dockerfile
```

-	Layers:
	-	`sha256:dc14f6b45ffd0cf094851f620d7c09a23513353217e1640bd80f9752ae64eb67`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:46f43a77c9d9be15ca3b2787d01a7fc76c0ad5c1f84b62acdfe9c75bdf2364cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1b5fcf3af1aec5f8186371ced026734b0dc358f81fd79977d24923f55da091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52664fd029115b59e10665beb1de4db22437397f1e12d9ef21a10227a4bcb0b3`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 6.8 MB (6821275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a63f62b766f87fc00d415fb393198a177ca29d74ef894de1081a534644c51f`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42627bd4fc0b9abb95a7fe4472894e86dac74bcfafc35397fe46a8b51863a24b`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:02712ae3dfd268f7c0f286d515e88ffd04661bd2afa30df5ef55d8c1251c2d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc157db9d7cfbdfb06f25ffab6be682d8f329dbd5cb945f440a0b934ff633ae`

```dockerfile
```

-	Layers:
	-	`sha256:3921d54fa2bad5abd1ccb3ba03fdde77fb3342fb0c2f5f4ae861e1142b27e559`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:dc95c9071c61ae217f8b7ccc6c6cc4ed7135efd907ab216185d7a046f848263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edceff3cd31a9ba3c0916ec5a29e6f96072c9da161efff71263cdbd8bb621fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3ef39893803a1aa71385b7b4a0e2f2489c1714926ebc5a17f0f283f992c574`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 6.8 MB (6812139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05c0dd84c92bf393d4eeb2e08cb836caae1367d08914ed39ee6012bc7979eb`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5b69ca76cd026d2a3a3104034ad0bcde0f0a1ff1a54e334a1d5f2b7aa2ce0`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a096ab49bf85fe59d54ca81110922ea5bdd2e0d348e69d0f6025e938b39f26b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af01ae40e078b504a99160d21be1719bf0893debfd46c721e0f3f1b5fb2b8d88`

```dockerfile
```

-	Layers:
	-	`sha256:23e4cd5325bfcff95bbb97f89ba5f6e6dc0407032e7c0fb1cde3ad1ac6830a7b`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb1c336dc892313409a8a9be0bd058eeb502231aa3383b448d862253abe72660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10653076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7263323b7691f6bfc1ce77845e1493322e0a7fb05848ba9496d17994e3c358`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414ff6f42514787c192e710db9db418be359224a6173e1237a72689ab899901a`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 6.5 MB (6510214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bb42c58d7e11c558e5072fdac886e2e8d5119360c8339777bf525f6b3de3be`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f5a1bbeb5c096e363e206a3d729f50c23ae559b4b3d9fea208d0b170b4864d`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a80cf61114fd852a49cc7cc405df6566531f25fb08f1698e38110bd13b16bcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1eea64ca314ff49953a4d62c6f57c8921b550e4a65eef8447cab8789dafa98`

```dockerfile
```

-	Layers:
	-	`sha256:f96940dabf37dc5e896241d7598fd3bf014ea2f2dec81a8253215bce6dd38616`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:53b58d1e5ac5757d0090c9c82d6b43c4fa3983e2af4ada84b96a6431d7a6cad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2412c201b02e670a6c66daff1a839dbf8949e02fd7bab2be04cea5c1e0c738e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:02 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:19:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ed90b89f0799173e6fccc22fecf8ff6c8973c8ed4ff1831c68a7c7569b4cd`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 6.6 MB (6560526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac41c2bd3722584f61f21b39d46ec42523bd6ea86f211b9027e5acf3135de9`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49b420d0d646e4990b9696c25668a04fb23ae54be76f6897fbd49eae67b24c`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:35462817b467f61ebceb4eca3c0ac8d23fbdee1ba0b903f77d995d769a172ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f729ef5c8fed43aecc14c5a725ab776840e1a16f702f8496ef3b696338d2f4d3`

```dockerfile
```

-	Layers:
	-	`sha256:822b657516851096b98cd62907a761f8ccbbb44813254a0078eb31d4f272c619`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:8dd0bb86b226ee0c00b11bee7e5402a505865da642006ff14293d14912b11e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10596317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2033c7f5d89abe8c752cd0bceac3d04d00854284c008645ba31f91ef04652287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7537aff86e4637878e5664a942467243a0f2cd0f3724bad313542c288b66619f`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 6.9 MB (6941474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c98718326853d62529f33a4745f08a21999d45bddc49bf4d4175feb2bd9c49`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5b57122821a0589eb6f05dc704b4f828e3060b27f5c6eeec2cad9b5b52bf3c`  
		Last Modified: Fri, 17 Apr 2026 00:13:46 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6a1b0dd4f10ca2f0dcfcd22ebcb04999217fcbf87ad066c7993d2a45e3970490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c0a8646f0475362f0b87ffe0fba73b5631df8220475194d2849b657ea3b049`

```dockerfile
```

-	Layers:
	-	`sha256:a85160fd978747e6ebfeae736628c48024e7b74f2f00bc194d8b8fb7b1c81552`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.12.7-linux`

```console
$ docker pull nats@sha256:dbda35114cbb4890d9ee9ff85c1328bbdce97e1ae72ea36d681ef6dcf972d202
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
$ docker pull nats@sha256:391f0072ce67ee55b761370c314dbc8a7281473e0bfda3ac659049f1b08075a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95d5bca384b7959bb5cf1a743a13f85be65a9488c0552f4df4cec87389b3200`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:57 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e87fa5d12be7bc0f44b53fa6cd141e76f56faef2467d8d9769be47ac8a3674`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-linux` - unknown; unknown

```console
$ docker pull nats@sha256:7c0366118c1dc0312ba0da7857982f13047f2ec8f1fe47820ae2510cc388c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f6f9d105ca7c46470f68af2b4271f0ed40ff0ad556161424e05e3a8ecaa28`

```dockerfile
```

-	Layers:
	-	`sha256:334dab01a895b2d00e9ac0e339855e2a15daf4569eef8b6a44197b75ed20f62f`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea3c1af26c064464b8f6bca423596b7220fa93816adaf83f706c9ae34b91985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37732cf595594fea3845c95390a620ae7b6486b55c225260d9a94cf8aa1c3191`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34d7930b8b8e75da31eb1b797ef0912c6853bdc85ad347e1b797a5634d3577`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8e85b848d4b99afd92319210009a21f0052594311083d77fcf1ee8d6cab7cd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd733e47fb31591cc226c0a9aeceff2ca10b4207b7a4381cdd83879112bed1e8`

```dockerfile
```

-	Layers:
	-	`sha256:9705c11af89c00eef360d7c22c0fee24c5db2d4c6b9c7611bfc6452b12f7eb79`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3a84a8d961bad8bad4fe7fb65dee444f2a66a059b8558ae8fb65574034a28e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9ca91358bfb3db35540bfd10f98b46899bfd81947a3e7c8034dbdccd3698e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1cc2ded7c5a3d7e8d9680c305f87bde0af7613fd1da0bd9f7b3f4b28528afd`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d2dc28bfb63659ddc44a14336f01f50ae3f3163b738ec04ce8fe354eb7cb0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdc86cc80dfedb4387659a7fa450f4216ffa6e6ac70823bfe739ccd9ed6902`

```dockerfile
```

-	Layers:
	-	`sha256:a28c5e1d2bd63600380e93535a5184c2c136a6aceb6cb7955e7d0e27563e1515`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:67c19494d70d06a12fdb38cf1be9df8ac8c003f1a8b236cd006d98ecc44c1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb010d3d2ef36bf55d9822e7505d72bc8749b4c81f49fa8347f6bc0170c6fe0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:16 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986e74a3c2ed133ac9088b767d56152dbe9ab65a416b04c81b00818be1ea963b`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-linux` - unknown; unknown

```console
$ docker pull nats@sha256:360bbf5808469578c04388e925785d45de711f2e0721b45aaf6f69dd5d197235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc87059696946491f60585793b3ae1fb94f85c1837a552ee798c7fd04d8c20f5`

```dockerfile
```

-	Layers:
	-	`sha256:3df5561b2a5a1ba9b17f6deec10fced17cc1921bad7497afc9fa646a3ee3e06a`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:b7d4c7253edb794c82e7dfed2c9cfa02dfd904e51f74f28ba31e047f62fc7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6ccedb2bd06fad337c3208934e55614b5dce7689fdc624d7c1ea46585b0910`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-linux` - unknown; unknown

```console
$ docker pull nats@sha256:150a2bdf7ca081074b6337f2c6a2ce949012f032b621816bf7d9518a4c9c8b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0e2cf0c979f91dcf610709e731f9d2524dd2a0d1270d5f0b2d331e8e5cce5`

```dockerfile
```

-	Layers:
	-	`sha256:71e0f2fc0ec84444d3f17187d21565a2004ebcf91fc6379221afe6b5f292aff3`  
		Last Modified: Fri, 17 Apr 2026 02:08:48 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-linux` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-linux` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
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
$ docker pull nats@sha256:dbda35114cbb4890d9ee9ff85c1328bbdce97e1ae72ea36d681ef6dcf972d202
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
$ docker pull nats@sha256:391f0072ce67ee55b761370c314dbc8a7281473e0bfda3ac659049f1b08075a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95d5bca384b7959bb5cf1a743a13f85be65a9488c0552f4df4cec87389b3200`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:57 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e87fa5d12be7bc0f44b53fa6cd141e76f56faef2467d8d9769be47ac8a3674`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7c0366118c1dc0312ba0da7857982f13047f2ec8f1fe47820ae2510cc388c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f6f9d105ca7c46470f68af2b4271f0ed40ff0ad556161424e05e3a8ecaa28`

```dockerfile
```

-	Layers:
	-	`sha256:334dab01a895b2d00e9ac0e339855e2a15daf4569eef8b6a44197b75ed20f62f`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea3c1af26c064464b8f6bca423596b7220fa93816adaf83f706c9ae34b91985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37732cf595594fea3845c95390a620ae7b6486b55c225260d9a94cf8aa1c3191`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34d7930b8b8e75da31eb1b797ef0912c6853bdc85ad347e1b797a5634d3577`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8e85b848d4b99afd92319210009a21f0052594311083d77fcf1ee8d6cab7cd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd733e47fb31591cc226c0a9aeceff2ca10b4207b7a4381cdd83879112bed1e8`

```dockerfile
```

-	Layers:
	-	`sha256:9705c11af89c00eef360d7c22c0fee24c5db2d4c6b9c7611bfc6452b12f7eb79`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3a84a8d961bad8bad4fe7fb65dee444f2a66a059b8558ae8fb65574034a28e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9ca91358bfb3db35540bfd10f98b46899bfd81947a3e7c8034dbdccd3698e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1cc2ded7c5a3d7e8d9680c305f87bde0af7613fd1da0bd9f7b3f4b28528afd`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d2dc28bfb63659ddc44a14336f01f50ae3f3163b738ec04ce8fe354eb7cb0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdc86cc80dfedb4387659a7fa450f4216ffa6e6ac70823bfe739ccd9ed6902`

```dockerfile
```

-	Layers:
	-	`sha256:a28c5e1d2bd63600380e93535a5184c2c136a6aceb6cb7955e7d0e27563e1515`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:67c19494d70d06a12fdb38cf1be9df8ac8c003f1a8b236cd006d98ecc44c1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb010d3d2ef36bf55d9822e7505d72bc8749b4c81f49fa8347f6bc0170c6fe0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:16 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986e74a3c2ed133ac9088b767d56152dbe9ab65a416b04c81b00818be1ea963b`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:360bbf5808469578c04388e925785d45de711f2e0721b45aaf6f69dd5d197235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc87059696946491f60585793b3ae1fb94f85c1837a552ee798c7fd04d8c20f5`

```dockerfile
```

-	Layers:
	-	`sha256:3df5561b2a5a1ba9b17f6deec10fced17cc1921bad7497afc9fa646a3ee3e06a`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:b7d4c7253edb794c82e7dfed2c9cfa02dfd904e51f74f28ba31e047f62fc7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6ccedb2bd06fad337c3208934e55614b5dce7689fdc624d7c1ea46585b0910`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:150a2bdf7ca081074b6337f2c6a2ce949012f032b621816bf7d9518a4c9c8b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0e2cf0c979f91dcf610709e731f9d2524dd2a0d1270d5f0b2d331e8e5cce5`

```dockerfile
```

-	Layers:
	-	`sha256:71e0f2fc0ec84444d3f17187d21565a2004ebcf91fc6379221afe6b5f292aff3`  
		Last Modified: Fri, 17 Apr 2026 02:08:48 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.12.7-scratch` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.12.7-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
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
$ docker pull nats@sha256:e602ceca19bddc3dd7197b4b1afde53a16cd9d31a5500a8ae5620f36cb01963c
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
$ docker pull nats@sha256:16179be8b1ec51f6e587273a8f77f42773ea1f12228ad777764d971e7b43c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10911201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9559d6064637f63c271167a9d7c010ff5364b1eec2b0208599b50488ba703d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7a1e64c52df3467627e6d1c644bcb8211343cd68dddf6166bdffbccaf244fd`  
		Last Modified: Fri, 17 Apr 2026 00:15:33 GMT  
		Size: 7.1 MB (7102043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029b2f91063f4996b4cd7e46a633ab1a441fa1b56b1f99ed0b8451abeca076cb`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d704923a1249776a808f8aeafbe1adf7092d06b738b33f076cad79dcad5cf25`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ca41342c8a71a1155058491c46bc3acc5e7cdb6651860972e62fb3c748ab050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d7c6232cacba47988be2ed2b963902987d654145e91fa75e175f098bdbdb14`

```dockerfile
```

-	Layers:
	-	`sha256:dc14f6b45ffd0cf094851f620d7c09a23513353217e1640bd80f9752ae64eb67`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:46f43a77c9d9be15ca3b2787d01a7fc76c0ad5c1f84b62acdfe9c75bdf2364cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1b5fcf3af1aec5f8186371ced026734b0dc358f81fd79977d24923f55da091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52664fd029115b59e10665beb1de4db22437397f1e12d9ef21a10227a4bcb0b3`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 6.8 MB (6821275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a63f62b766f87fc00d415fb393198a177ca29d74ef894de1081a534644c51f`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42627bd4fc0b9abb95a7fe4472894e86dac74bcfafc35397fe46a8b51863a24b`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:02712ae3dfd268f7c0f286d515e88ffd04661bd2afa30df5ef55d8c1251c2d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc157db9d7cfbdfb06f25ffab6be682d8f329dbd5cb945f440a0b934ff633ae`

```dockerfile
```

-	Layers:
	-	`sha256:3921d54fa2bad5abd1ccb3ba03fdde77fb3342fb0c2f5f4ae861e1142b27e559`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:dc95c9071c61ae217f8b7ccc6c6cc4ed7135efd907ab216185d7a046f848263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edceff3cd31a9ba3c0916ec5a29e6f96072c9da161efff71263cdbd8bb621fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3ef39893803a1aa71385b7b4a0e2f2489c1714926ebc5a17f0f283f992c574`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 6.8 MB (6812139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05c0dd84c92bf393d4eeb2e08cb836caae1367d08914ed39ee6012bc7979eb`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5b69ca76cd026d2a3a3104034ad0bcde0f0a1ff1a54e334a1d5f2b7aa2ce0`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a096ab49bf85fe59d54ca81110922ea5bdd2e0d348e69d0f6025e938b39f26b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af01ae40e078b504a99160d21be1719bf0893debfd46c721e0f3f1b5fb2b8d88`

```dockerfile
```

-	Layers:
	-	`sha256:23e4cd5325bfcff95bbb97f89ba5f6e6dc0407032e7c0fb1cde3ad1ac6830a7b`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb1c336dc892313409a8a9be0bd058eeb502231aa3383b448d862253abe72660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10653076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7263323b7691f6bfc1ce77845e1493322e0a7fb05848ba9496d17994e3c358`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414ff6f42514787c192e710db9db418be359224a6173e1237a72689ab899901a`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 6.5 MB (6510214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bb42c58d7e11c558e5072fdac886e2e8d5119360c8339777bf525f6b3de3be`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f5a1bbeb5c096e363e206a3d729f50c23ae559b4b3d9fea208d0b170b4864d`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a80cf61114fd852a49cc7cc405df6566531f25fb08f1698e38110bd13b16bcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1eea64ca314ff49953a4d62c6f57c8921b550e4a65eef8447cab8789dafa98`

```dockerfile
```

-	Layers:
	-	`sha256:f96940dabf37dc5e896241d7598fd3bf014ea2f2dec81a8253215bce6dd38616`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:53b58d1e5ac5757d0090c9c82d6b43c4fa3983e2af4ada84b96a6431d7a6cad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2412c201b02e670a6c66daff1a839dbf8949e02fd7bab2be04cea5c1e0c738e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:02 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:19:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ed90b89f0799173e6fccc22fecf8ff6c8973c8ed4ff1831c68a7c7569b4cd`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 6.6 MB (6560526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac41c2bd3722584f61f21b39d46ec42523bd6ea86f211b9027e5acf3135de9`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49b420d0d646e4990b9696c25668a04fb23ae54be76f6897fbd49eae67b24c`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:35462817b467f61ebceb4eca3c0ac8d23fbdee1ba0b903f77d995d769a172ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f729ef5c8fed43aecc14c5a725ab776840e1a16f702f8496ef3b696338d2f4d3`

```dockerfile
```

-	Layers:
	-	`sha256:822b657516851096b98cd62907a761f8ccbbb44813254a0078eb31d4f272c619`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:8dd0bb86b226ee0c00b11bee7e5402a505865da642006ff14293d14912b11e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10596317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2033c7f5d89abe8c752cd0bceac3d04d00854284c008645ba31f91ef04652287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7537aff86e4637878e5664a942467243a0f2cd0f3724bad313542c288b66619f`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 6.9 MB (6941474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c98718326853d62529f33a4745f08a21999d45bddc49bf4d4175feb2bd9c49`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5b57122821a0589eb6f05dc704b4f828e3060b27f5c6eeec2cad9b5b52bf3c`  
		Last Modified: Fri, 17 Apr 2026 00:13:46 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6a1b0dd4f10ca2f0dcfcd22ebcb04999217fcbf87ad066c7993d2a45e3970490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c0a8646f0475362f0b87ffe0fba73b5631df8220475194d2849b657ea3b049`

```dockerfile
```

-	Layers:
	-	`sha256:a85160fd978747e6ebfeae736628c48024e7b74f2f00bc194d8b8fb7b1c81552`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:e602ceca19bddc3dd7197b4b1afde53a16cd9d31a5500a8ae5620f36cb01963c
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
$ docker pull nats@sha256:16179be8b1ec51f6e587273a8f77f42773ea1f12228ad777764d971e7b43c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10911201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9559d6064637f63c271167a9d7c010ff5364b1eec2b0208599b50488ba703d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:28 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:28 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7a1e64c52df3467627e6d1c644bcb8211343cd68dddf6166bdffbccaf244fd`  
		Last Modified: Fri, 17 Apr 2026 00:15:33 GMT  
		Size: 7.1 MB (7102043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029b2f91063f4996b4cd7e46a633ab1a441fa1b56b1f99ed0b8451abeca076cb`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d704923a1249776a808f8aeafbe1adf7092d06b738b33f076cad79dcad5cf25`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ca41342c8a71a1155058491c46bc3acc5e7cdb6651860972e62fb3c748ab050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d7c6232cacba47988be2ed2b963902987d654145e91fa75e175f098bdbdb14`

```dockerfile
```

-	Layers:
	-	`sha256:dc14f6b45ffd0cf094851f620d7c09a23513353217e1640bd80f9752ae64eb67`  
		Last Modified: Fri, 17 Apr 2026 00:15:32 GMT  
		Size: 15.4 KB (15403 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:46f43a77c9d9be15ca3b2787d01a7fc76c0ad5c1f84b62acdfe9c75bdf2364cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1b5fcf3af1aec5f8186371ced026734b0dc358f81fd79977d24923f55da091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:14:54 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:14:54 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:14:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52664fd029115b59e10665beb1de4db22437397f1e12d9ef21a10227a4bcb0b3`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 6.8 MB (6821275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a63f62b766f87fc00d415fb393198a177ca29d74ef894de1081a534644c51f`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42627bd4fc0b9abb95a7fe4472894e86dac74bcfafc35397fe46a8b51863a24b`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:02712ae3dfd268f7c0f286d515e88ffd04661bd2afa30df5ef55d8c1251c2d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc157db9d7cfbdfb06f25ffab6be682d8f329dbd5cb945f440a0b934ff633ae`

```dockerfile
```

-	Layers:
	-	`sha256:3921d54fa2bad5abd1ccb3ba03fdde77fb3342fb0c2f5f4ae861e1142b27e559`  
		Last Modified: Fri, 17 Apr 2026 00:14:58 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:dc95c9071c61ae217f8b7ccc6c6cc4ed7135efd907ab216185d7a046f848263a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10038938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edceff3cd31a9ba3c0916ec5a29e6f96072c9da161efff71263cdbd8bb621fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:10 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:10 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3ef39893803a1aa71385b7b4a0e2f2489c1714926ebc5a17f0f283f992c574`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 6.8 MB (6812139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb05c0dd84c92bf393d4eeb2e08cb836caae1367d08914ed39ee6012bc7979eb`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5b69ca76cd026d2a3a3104034ad0bcde0f0a1ff1a54e334a1d5f2b7aa2ce0`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a096ab49bf85fe59d54ca81110922ea5bdd2e0d348e69d0f6025e938b39f26b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af01ae40e078b504a99160d21be1719bf0893debfd46c721e0f3f1b5fb2b8d88`

```dockerfile
```

-	Layers:
	-	`sha256:23e4cd5325bfcff95bbb97f89ba5f6e6dc0407032e7c0fb1cde3ad1ac6830a7b`  
		Last Modified: Fri, 17 Apr 2026 00:15:14 GMT  
		Size: 15.5 KB (15516 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:cb1c336dc892313409a8a9be0bd058eeb502231aa3383b448d862253abe72660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10653076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7263323b7691f6bfc1ce77845e1493322e0a7fb05848ba9496d17994e3c358`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:15:40 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:15:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:15:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:15:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414ff6f42514787c192e710db9db418be359224a6173e1237a72689ab899901a`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 6.5 MB (6510214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bb42c58d7e11c558e5072fdac886e2e8d5119360c8339777bf525f6b3de3be`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f5a1bbeb5c096e363e206a3d729f50c23ae559b4b3d9fea208d0b170b4864d`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:a80cf61114fd852a49cc7cc405df6566531f25fb08f1698e38110bd13b16bcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 KB (15556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1eea64ca314ff49953a4d62c6f57c8921b550e4a65eef8447cab8789dafa98`

```dockerfile
```

-	Layers:
	-	`sha256:f96940dabf37dc5e896241d7598fd3bf014ea2f2dec81a8253215bce6dd38616`  
		Last Modified: Fri, 17 Apr 2026 00:15:45 GMT  
		Size: 15.6 KB (15556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:53b58d1e5ac5757d0090c9c82d6b43c4fa3983e2af4ada84b96a6431d7a6cad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10298151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2412c201b02e670a6c66daff1a839dbf8949e02fd7bab2be04cea5c1e0c738e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:02 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:19:02 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:19:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:19:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b2ed90b89f0799173e6fccc22fecf8ff6c8973c8ed4ff1831c68a7c7569b4cd`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 6.6 MB (6560526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac41c2bd3722584f61f21b39d46ec42523bd6ea86f211b9027e5acf3135de9`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b49b420d0d646e4990b9696c25668a04fb23ae54be76f6897fbd49eae67b24c`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:35462817b467f61ebceb4eca3c0ac8d23fbdee1ba0b903f77d995d769a172ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 KB (15472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f729ef5c8fed43aecc14c5a725ab776840e1a16f702f8496ef3b696338d2f4d3`

```dockerfile
```

-	Layers:
	-	`sha256:822b657516851096b98cd62907a761f8ccbbb44813254a0078eb31d4f272c619`  
		Last Modified: Fri, 17 Apr 2026 00:19:12 GMT  
		Size: 15.5 KB (15472 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:8dd0bb86b226ee0c00b11bee7e5402a505865da642006ff14293d14912b11e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10596317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2033c7f5d89abe8c752cd0bceac3d04d00854284c008645ba31f91ef04652287`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
ENV NATS_SERVER=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
LABEL org.opencontainers.image.title=NATS Server org.opencontainers.image.description=NATS is an open-source, high-performance, cloud native messaging system. org.opencontainers.image.url=https://nats.io org.opencontainers.image.documentation=https://docs.nats.io org.opencontainers.image.source=https://github.com/nats-io/nats-docker org.opencontainers.image.vendor=NATS.io org.opencontainers.image.licenses=Apache-2.0 org.opencontainers.image.version=2.12.7
# Fri, 17 Apr 2026 00:13:37 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='3b9a79986778285c0e5acaba0b1218b72f6159db68fe5b8916a7d846240f9f22' ;;     armhf) natsArch='arm6'; sha256='83e4886378c1b779a8036b614d99a5d3841fbb12838d076031b153bec8aff247' ;;     armv7) natsArch='arm7'; sha256='c6a2563489aa54ecb2f5ff73d24fc5f9052ef70c4bf179b10ea322811cd42a0b' ;;     x86_64) natsArch='amd64'; sha256='570d2d627db111e679cc1e6bc57ba78f373ed1769acd8dc9c21c8f62d15b3c52' ;;     x86) natsArch='386'; sha256='6f866cdd4e5c4414f50e62394ee1fd132ad3b972086d10df12d88c30264a66ac' ;;     s390x) natsArch='s390x'; sha256='34ae4158237e879c7bf79875101f14a79184c23757f11d521c40c59518203950' ;;     ppc64le) natsArch='ppc64le'; sha256='6508ea8a70d7d5cc68978150a55bd51e2a41a37f120c361d7b48c06c699728c8' ;;     loong64) natsArch='loong64'; sha256='614bd0bffe5c7835bbef5e330e25dcf0041c73d84a7976ba598c5c1d5bd49980' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 17 Apr 2026 00:13:37 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 00:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7537aff86e4637878e5664a942467243a0f2cd0f3724bad313542c288b66619f`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 6.9 MB (6941474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c98718326853d62529f33a4745f08a21999d45bddc49bf4d4175feb2bd9c49`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5b57122821a0589eb6f05dc704b4f828e3060b27f5c6eeec2cad9b5b52bf3c`  
		Last Modified: Fri, 17 Apr 2026 00:13:46 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:6a1b0dd4f10ca2f0dcfcd22ebcb04999217fcbf87ad066c7993d2a45e3970490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 KB (15402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c0a8646f0475362f0b87ffe0fba73b5631df8220475194d2849b657ea3b049`

```dockerfile
```

-	Layers:
	-	`sha256:a85160fd978747e6ebfeae736628c48024e7b74f2f00bc194d8b8fb7b1c81552`  
		Last Modified: Fri, 17 Apr 2026 00:13:45 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:c9e19fc4f9d0b36f9d2da3175ce3c95220806d098c24d328feb869886ab4afef
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
$ docker pull nats@sha256:391f0072ce67ee55b761370c314dbc8a7281473e0bfda3ac659049f1b08075a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95d5bca384b7959bb5cf1a743a13f85be65a9488c0552f4df4cec87389b3200`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:57 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e87fa5d12be7bc0f44b53fa6cd141e76f56faef2467d8d9769be47ac8a3674`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:7c0366118c1dc0312ba0da7857982f13047f2ec8f1fe47820ae2510cc388c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f6f9d105ca7c46470f68af2b4271f0ed40ff0ad556161424e05e3a8ecaa28`

```dockerfile
```

-	Layers:
	-	`sha256:334dab01a895b2d00e9ac0e339855e2a15daf4569eef8b6a44197b75ed20f62f`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea3c1af26c064464b8f6bca423596b7220fa93816adaf83f706c9ae34b91985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37732cf595594fea3845c95390a620ae7b6486b55c225260d9a94cf8aa1c3191`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34d7930b8b8e75da31eb1b797ef0912c6853bdc85ad347e1b797a5634d3577`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:8e85b848d4b99afd92319210009a21f0052594311083d77fcf1ee8d6cab7cd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd733e47fb31591cc226c0a9aeceff2ca10b4207b7a4381cdd83879112bed1e8`

```dockerfile
```

-	Layers:
	-	`sha256:9705c11af89c00eef360d7c22c0fee24c5db2d4c6b9c7611bfc6452b12f7eb79`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3a84a8d961bad8bad4fe7fb65dee444f2a66a059b8558ae8fb65574034a28e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9ca91358bfb3db35540bfd10f98b46899bfd81947a3e7c8034dbdccd3698e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1cc2ded7c5a3d7e8d9680c305f87bde0af7613fd1da0bd9f7b3f4b28528afd`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:d2dc28bfb63659ddc44a14336f01f50ae3f3163b738ec04ce8fe354eb7cb0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdc86cc80dfedb4387659a7fa450f4216ffa6e6ac70823bfe739ccd9ed6902`

```dockerfile
```

-	Layers:
	-	`sha256:a28c5e1d2bd63600380e93535a5184c2c136a6aceb6cb7955e7d0e27563e1515`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:67c19494d70d06a12fdb38cf1be9df8ac8c003f1a8b236cd006d98ecc44c1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb010d3d2ef36bf55d9822e7505d72bc8749b4c81f49fa8347f6bc0170c6fe0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:16 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986e74a3c2ed133ac9088b767d56152dbe9ab65a416b04c81b00818be1ea963b`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:360bbf5808469578c04388e925785d45de711f2e0721b45aaf6f69dd5d197235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc87059696946491f60585793b3ae1fb94f85c1837a552ee798c7fd04d8c20f5`

```dockerfile
```

-	Layers:
	-	`sha256:3df5561b2a5a1ba9b17f6deec10fced17cc1921bad7497afc9fa646a3ee3e06a`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:b7d4c7253edb794c82e7dfed2c9cfa02dfd904e51f74f28ba31e047f62fc7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6ccedb2bd06fad337c3208934e55614b5dce7689fdc624d7c1ea46585b0910`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:150a2bdf7ca081074b6337f2c6a2ce949012f032b621816bf7d9518a4c9c8b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0e2cf0c979f91dcf610709e731f9d2524dd2a0d1270d5f0b2d331e8e5cce5`

```dockerfile
```

-	Layers:
	-	`sha256:71e0f2fc0ec84444d3f17187d21565a2004ebcf91fc6379221afe6b5f292aff3`  
		Last Modified: Fri, 17 Apr 2026 02:08:48 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
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
$ docker pull nats@sha256:dbda35114cbb4890d9ee9ff85c1328bbdce97e1ae72ea36d681ef6dcf972d202
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
$ docker pull nats@sha256:391f0072ce67ee55b761370c314dbc8a7281473e0bfda3ac659049f1b08075a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95d5bca384b7959bb5cf1a743a13f85be65a9488c0552f4df4cec87389b3200`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:57 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e87fa5d12be7bc0f44b53fa6cd141e76f56faef2467d8d9769be47ac8a3674`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:7c0366118c1dc0312ba0da7857982f13047f2ec8f1fe47820ae2510cc388c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f6f9d105ca7c46470f68af2b4271f0ed40ff0ad556161424e05e3a8ecaa28`

```dockerfile
```

-	Layers:
	-	`sha256:334dab01a895b2d00e9ac0e339855e2a15daf4569eef8b6a44197b75ed20f62f`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea3c1af26c064464b8f6bca423596b7220fa93816adaf83f706c9ae34b91985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37732cf595594fea3845c95390a620ae7b6486b55c225260d9a94cf8aa1c3191`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34d7930b8b8e75da31eb1b797ef0912c6853bdc85ad347e1b797a5634d3577`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:8e85b848d4b99afd92319210009a21f0052594311083d77fcf1ee8d6cab7cd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd733e47fb31591cc226c0a9aeceff2ca10b4207b7a4381cdd83879112bed1e8`

```dockerfile
```

-	Layers:
	-	`sha256:9705c11af89c00eef360d7c22c0fee24c5db2d4c6b9c7611bfc6452b12f7eb79`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3a84a8d961bad8bad4fe7fb65dee444f2a66a059b8558ae8fb65574034a28e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9ca91358bfb3db35540bfd10f98b46899bfd81947a3e7c8034dbdccd3698e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1cc2ded7c5a3d7e8d9680c305f87bde0af7613fd1da0bd9f7b3f4b28528afd`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:d2dc28bfb63659ddc44a14336f01f50ae3f3163b738ec04ce8fe354eb7cb0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdc86cc80dfedb4387659a7fa450f4216ffa6e6ac70823bfe739ccd9ed6902`

```dockerfile
```

-	Layers:
	-	`sha256:a28c5e1d2bd63600380e93535a5184c2c136a6aceb6cb7955e7d0e27563e1515`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:67c19494d70d06a12fdb38cf1be9df8ac8c003f1a8b236cd006d98ecc44c1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb010d3d2ef36bf55d9822e7505d72bc8749b4c81f49fa8347f6bc0170c6fe0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:16 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986e74a3c2ed133ac9088b767d56152dbe9ab65a416b04c81b00818be1ea963b`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:360bbf5808469578c04388e925785d45de711f2e0721b45aaf6f69dd5d197235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc87059696946491f60585793b3ae1fb94f85c1837a552ee798c7fd04d8c20f5`

```dockerfile
```

-	Layers:
	-	`sha256:3df5561b2a5a1ba9b17f6deec10fced17cc1921bad7497afc9fa646a3ee3e06a`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:b7d4c7253edb794c82e7dfed2c9cfa02dfd904e51f74f28ba31e047f62fc7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6ccedb2bd06fad337c3208934e55614b5dce7689fdc624d7c1ea46585b0910`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:150a2bdf7ca081074b6337f2c6a2ce949012f032b621816bf7d9518a4c9c8b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0e2cf0c979f91dcf610709e731f9d2524dd2a0d1270d5f0b2d331e8e5cce5`

```dockerfile
```

-	Layers:
	-	`sha256:71e0f2fc0ec84444d3f17187d21565a2004ebcf91fc6379221afe6b5f292aff3`  
		Last Modified: Fri, 17 Apr 2026 02:08:48 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
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
$ docker pull nats@sha256:dbda35114cbb4890d9ee9ff85c1328bbdce97e1ae72ea36d681ef6dcf972d202
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
$ docker pull nats@sha256:391f0072ce67ee55b761370c314dbc8a7281473e0bfda3ac659049f1b08075a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6648882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95d5bca384b7959bb5cf1a743a13f85be65a9488c0552f4df4cec87389b3200`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:57 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:57 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:57 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:57 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a8451ce6e4196fd024b52ca657119928b600d43ac7117982d67211f05efc43fd`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.6 MB (6648374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e87fa5d12be7bc0f44b53fa6cd141e76f56faef2467d8d9769be47ac8a3674`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7c0366118c1dc0312ba0da7857982f13047f2ec8f1fe47820ae2510cc388c121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9f6f9d105ca7c46470f68af2b4271f0ed40ff0ad556161424e05e3a8ecaa28`

```dockerfile
```

-	Layers:
	-	`sha256:334dab01a895b2d00e9ac0e339855e2a15daf4569eef8b6a44197b75ed20f62f`  
		Last Modified: Fri, 17 Apr 2026 01:13:01 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:ea3c1af26c064464b8f6bca423596b7220fa93816adaf83f706c9ae34b91985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6364679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37732cf595594fea3845c95390a620ae7b6486b55c225260d9a94cf8aa1c3191`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:12:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:12:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:12:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:12:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:12:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:746afff54b001c7c268a77143632427f5ffba713a94f3d52bb22af6cd8a7d3a8`  
		Last Modified: Tue, 14 Apr 2026 16:11:09 GMT  
		Size: 6.4 MB (6364169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf34d7930b8b8e75da31eb1b797ef0912c6853bdc85ad347e1b797a5634d3577`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8e85b848d4b99afd92319210009a21f0052594311083d77fcf1ee8d6cab7cd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd733e47fb31591cc226c0a9aeceff2ca10b4207b7a4381cdd83879112bed1e8`

```dockerfile
```

-	Layers:
	-	`sha256:9705c11af89c00eef360d7c22c0fee24c5db2d4c6b9c7611bfc6452b12f7eb79`  
		Last Modified: Fri, 17 Apr 2026 01:12:23 GMT  
		Size: 10.6 KB (10553 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:b3a84a8d961bad8bad4fe7fb65dee444f2a66a059b8558ae8fb65574034a28e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9ca91358bfb3db35540bfd10f98b46899bfd81947a3e7c8034dbdccd3698e8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:14:06 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:14:06 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:14:06 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:14:06 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ca1e6577fdd68cfe620659d82b112ec23bf158b6a173febdd3d70bfc74d946b4`  
		Last Modified: Tue, 14 Apr 2026 16:11:10 GMT  
		Size: 6.4 MB (6354846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1cc2ded7c5a3d7e8d9680c305f87bde0af7613fd1da0bd9f7b3f4b28528afd`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d2dc28bfb63659ddc44a14336f01f50ae3f3163b738ec04ce8fe354eb7cb0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6bdc86cc80dfedb4387659a7fa450f4216ffa6e6ac70823bfe739ccd9ed6902`

```dockerfile
```

-	Layers:
	-	`sha256:a28c5e1d2bd63600380e93535a5184c2c136a6aceb6cb7955e7d0e27563e1515`  
		Last Modified: Fri, 17 Apr 2026 01:14:10 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:67c19494d70d06a12fdb38cf1be9df8ac8c003f1a8b236cd006d98ecc44c1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb010d3d2ef36bf55d9822e7505d72bc8749b4c81f49fa8347f6bc0170c6fe0b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 01:34:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 01:34:16 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 01:34:16 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 01:34:16 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 01:34:16 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:032bcde41f07bb8de227264cddec9f6eb56b4fbde8d57360ccddc5d70f9182d6`  
		Last Modified: Tue, 14 Apr 2026 16:11:08 GMT  
		Size: 6.1 MB (6051536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986e74a3c2ed133ac9088b767d56152dbe9ab65a416b04c81b00818be1ea963b`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:360bbf5808469578c04388e925785d45de711f2e0721b45aaf6f69dd5d197235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc87059696946491f60585793b3ae1fb94f85c1837a552ee798c7fd04d8c20f5`

```dockerfile
```

-	Layers:
	-	`sha256:3df5561b2a5a1ba9b17f6deec10fced17cc1921bad7497afc9fa646a3ee3e06a`  
		Last Modified: Fri, 17 Apr 2026 01:34:20 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:b7d4c7253edb794c82e7dfed2c9cfa02dfd904e51f74f28ba31e047f62fc7af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6ccedb2bd06fad337c3208934e55614b5dce7689fdc624d7c1ea46585b0910`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 02:08:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 02:08:41 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 02:08:41 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 02:08:41 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 02:08:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a430f4947d3090824a57e56312630c3e12f05b451b4da815c0a588f85edce757`  
		Last Modified: Tue, 14 Apr 2026 16:11:12 GMT  
		Size: 6.1 MB (6101770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a925c08690d93273f6f267a53aa73e8b95fe7c212ff68ede0f2923f99c3a7557`  
		Last Modified: Fri, 17 Apr 2026 02:08:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:150a2bdf7ca081074b6337f2c6a2ce949012f032b621816bf7d9518a4c9c8b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0a0e2cf0c979f91dcf610709e731f9d2524dd2a0d1270d5f0b2d331e8e5cce5`

```dockerfile
```

-	Layers:
	-	`sha256:71e0f2fc0ec84444d3f17187d21565a2004ebcf91fc6379221afe6b5f292aff3`  
		Last Modified: Fri, 17 Apr 2026 02:08:48 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:a324ebc8b5d5b6ff086d68e64e098e17b66fc156f389274951e42f52a8b23f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6484832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2e38fe080c76d6ae166c282817ade10d4b525a2898f2d3e1b9fe04121adc65`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 17 Apr 2026 03:00:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 17 Apr 2026 03:00:24 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 17 Apr 2026 03:00:24 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 17 Apr 2026 03:00:24 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 17 Apr 2026 03:00:24 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d69db880d0d8e9c17bddedd14c44838155e3731884ca58d832714f41ae0994a4`  
		Last Modified: Tue, 14 Apr 2026 16:11:11 GMT  
		Size: 6.5 MB (6484325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ccaf9a504ceac367bb1bc015bc93297b1ef3d33665d652d900abe49b377dbe`  
		Last Modified: Fri, 17 Apr 2026 03:00:32 GMT  
		Size: 507.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:f2d18eadcea78f33d5f94d1f4377e745b760a034301e4572eb57583fbd9619a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d598ec99a37a3b2f7edc4cb93bae9e92010c88541711b5fcf5860a5d4b854`

```dockerfile
```

-	Layers:
	-	`sha256:09e6ae93ba30d5c350f4cd3637afca9beb1f8a79cc8764a543ff277031438145`  
		Last Modified: Fri, 17 Apr 2026 03:00:34 GMT  
		Size: 10.4 KB (10422 bytes)  
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
