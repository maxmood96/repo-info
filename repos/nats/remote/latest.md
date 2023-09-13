## `nats:latest`

```console
$ docker pull nats@sha256:2f39dcadc2da982ae96eca5e92df9fe10487811c8e5f1e9c34813916b22f09b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4851; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:841691cd373d85dfef90326ad2625e6498d8472d68d7d64b9a7d11b566729e77
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5245280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfd417bdbd2f1eb2b6798d0a0fbba5ce7e3bd1d7ce50d29b8965cb174e801ed`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 Sep 2023 23:20:12 GMT
COPY file:acdb0e47969d6e334bcadb9c85dfef3166c764ff4ac55254185a04b1a6e8bbee in /nats-server 
# Wed, 06 Sep 2023 23:20:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 06 Sep 2023 23:20:12 GMT
EXPOSE 4222 6222 8222
# Wed, 06 Sep 2023 23:20:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 06 Sep 2023 23:20:12 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 06 Sep 2023 23:20:12 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:aac801db9a2a97942dde4494f98ce2d08c529a3af03ecb92f0b93426bbfd6419`  
		Last Modified: Wed, 06 Sep 2023 23:20:56 GMT  
		Size: 5.2 MB (5244773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f86dbe6523f83ad4a9d3f35c66bb097fad7505a3bd4de2123ea173ea21f1e38`  
		Last Modified: Wed, 06 Sep 2023 23:20:55 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:ec9d67b684f4605aa5fd2b86b64953bb8062a49d2916cf8e5fab437de945df15
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4980015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d632b911d90b9fc8ad6e2d0fd53012e9c8cc6ca17c685d2c8c2a6c4de2cb2c45`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 Sep 2023 23:04:49 GMT
COPY file:51aacaba9769a3f16e0467be1fc8eb86122f6f3496e89e41b61e0038083ae308 in /nats-server 
# Wed, 06 Sep 2023 23:04:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 06 Sep 2023 23:04:49 GMT
EXPOSE 4222 6222 8222
# Wed, 06 Sep 2023 23:04:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 06 Sep 2023 23:04:49 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 06 Sep 2023 23:04:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e165fccf6da77ad3b09408162fc7daaafe266b71dd5da8679594aa110a3a5`  
		Last Modified: Wed, 06 Sep 2023 23:05:32 GMT  
		Size: 5.0 MB (4979506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1baf063892d372757ae2be4c42843e0a096826874b64519c230fd85bd65e69e8`  
		Last Modified: Wed, 06 Sep 2023 23:05:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:58dfaa80e9889d01819641e707279821d96d6f5eb7ce87e29eaa38cd4e0b5cac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d43ddba67d73d9d9c8f19b9fbec53ca1bcb7f04349363538f7d08fd069dbd2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 Sep 2023 22:57:45 GMT
COPY file:aae670bb79c659968f632ae3be388af62614010873ced2a439475906dbb769c6 in /nats-server 
# Wed, 06 Sep 2023 22:57:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 06 Sep 2023 22:57:45 GMT
EXPOSE 4222 6222 8222
# Wed, 06 Sep 2023 22:57:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 06 Sep 2023 22:57:46 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 06 Sep 2023 22:57:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:55b6dbad6639da13368cebb9688e8a5caaee29041e6b5e2e798201dfcf2b67ad`  
		Last Modified: Wed, 06 Sep 2023 22:58:23 GMT  
		Size: 5.0 MB (4970341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17c52d1a9dd756c463e0590216b217bfee91f63c66217c407f1c98b1ebbc3b9`  
		Last Modified: Wed, 06 Sep 2023 22:58:22 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:dd48788f80e3925791e0dddfa44348b7df9022fbc914b20cf00e051a0b3adbf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4778848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e35fd1c4293b595f11452fdc3e7dd6d5d9e033ecc9b1e6a35ff40577f2cba9f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 06 Sep 2023 22:40:07 GMT
COPY file:d6eca5c67de65d1a8a30a51ea7318b044949c77108b2fdccc5aa0054c068c196 in /nats-server 
# Wed, 06 Sep 2023 22:40:07 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 06 Sep 2023 22:40:07 GMT
EXPOSE 4222 6222 8222
# Wed, 06 Sep 2023 22:40:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 06 Sep 2023 22:40:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 06 Sep 2023 22:40:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88e5ff7f26ea25c6d2ab092989d9372cb32b3e60880124facfcefd7d3f0b7591`  
		Last Modified: Wed, 06 Sep 2023 22:40:49 GMT  
		Size: 4.8 MB (4778340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7795fd345dfb406d659c2502b733417a10ee85274263050ee36ab4aa021a38d9`  
		Last Modified: Wed, 06 Sep 2023 22:40:48 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:ef369c5330e436aca92b7521434dcad6019b82114a6095132bc5e4e582a93861
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109819053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053513aeb5883341d4904ae9f696d46f6f79373919c304dc1199f0cde262ef4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Sep 2023 05:08:05 GMT
RUN cmd /S /C #(nop) COPY file:393d7e944d1b6697a14f19f6cb9673d95da4e1a0fc9508b238325e94beebc857 in C:\nats-server.exe 
# Wed, 13 Sep 2023 05:08:05 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 13 Sep 2023 05:08:06 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 13 Sep 2023 05:08:07 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 13 Sep 2023 05:08:07 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baa9930674eb6676a1690e63a275d0da517ab8b8aeab7ccd20591f76f7c69a5`  
		Last Modified: Wed, 13 Sep 2023 05:08:48 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf628408f2a1164bcd400567aa3cd56db3926c391837397914b8cd6c337369f`  
		Last Modified: Wed, 13 Sep 2023 05:08:47 GMT  
		Size: 5.3 MB (5320086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e6195a95c838cacd22627e342b84f22112007d2f4e70079c6de80beb6e7c45`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c249fb3d5e5f1f8e0ef37e85a0cfaed40a4bb8df20e92e8937d686c2ec18fed`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01b907719f9c8b285c36f7971a978e09c143bfa695bfcc5f46a9d56fd55458d`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af083ba70a28322391995a59e841ea4478fe0d88eabbb83b4cfcbf20fab0cc4`  
		Last Modified: Wed, 13 Sep 2023 05:08:45 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
