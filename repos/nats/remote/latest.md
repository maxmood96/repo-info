## `nats:latest`

```console
$ docker pull nats@sha256:04fcc71e7d416348e8761b4081931d735d3774f5b14d33b724cc6caad6037893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4010; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:1a82b1b261d169994fc6162f2f25894a49e20971560f8b2dff4f90eefb32b421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74665a2673c052e85d3417cec864d1aabab3263f3328051037a133d9b85765ce`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:32a9f093b76345e99bd81ff00eabc5ab1ae6c2bdc7d6c843c923049ea3c620ce in /nats-server 
# Thu, 02 Mar 2023 19:20:01 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 19:20:01 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:20:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 19:20:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 19:20:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:436f213323b997ad7aca1675cce2c9a9366e3cd51995b9829835ab9762901f98`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (4972530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb98c93488e5f33bab9a8b331c5fbe988a9dd644e39cc15e6626550ec05e541`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:8e1ba487c56a25895759177de201768f40c51ceeedca983afa03875039445bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4739851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60b5d45617b9109e120de34ac32b0647324dba3d69d2c56366545e50c2484c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:614e1182091dacdaa5043752e8239600bae8aa334cfd383cc326d1753d3eba64 in /nats-server 
# Thu, 02 Mar 2023 18:49:36 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:49:36 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:49:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:49:36 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:49:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d859c106d4072b51eee7be282394c7f0c288186311ae904751cd95c3cf9468ae`  
		Last Modified: Thu, 02 Mar 2023 18:50:54 GMT  
		Size: 4.7 MB (4739343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7000b41bf11d721897d126c1e72201203bcc8e9716daad77d7d42ae97853a`  
		Last Modified: Thu, 02 Mar 2023 18:50:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:644eac35d964521bc85286defaf1bae093b36618fe862eedff9a996e330fc60c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4731109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e814afeda8d92b2fb3dcdacf4648234504c6e4cd7fc24cce256cc588a439d7e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:a63786ae76c5e718a4952dd30b2265019e1ca48099ad19279d2e77e5ad704bfc in /nats-server 
# Thu, 02 Mar 2023 18:57:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:57:50 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:57:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:57:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:57:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e714c80855fb90cb44f135a04bf323493a749536bb9106eb3ef4e69a70682897`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 4.7 MB (4730600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e020ba411c44ee7d23b6bdbd966700955c2d087afd3d79a9ad51e0390e8e7b6`  
		Last Modified: Thu, 02 Mar 2023 18:59:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:35ef84ac5e9bb0d0229fb1a773677d6ee7b23bb58937427d20aaa36987562373
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4559479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f367536d7ef4331c52bf405914c6f7affdccdb8eed05fb4c981efe519fd06f00`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:23081283f9b4d8145ad2b3a276cc08fcb49c4850e322db9560525e495d1bf362 in /nats-server 
# Thu, 02 Mar 2023 18:40:16 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 02 Mar 2023 18:40:16 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 18:40:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 02 Mar 2023 18:40:16 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Mar 2023 18:40:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a910efaa632bb8401dbca7cfe541f6dc4da71ea38708992ef153250254493114`  
		Last Modified: Thu, 02 Mar 2023 18:41:09 GMT  
		Size: 4.6 MB (4558972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be7fc9abf13897cf1a5e7026f6a49b3308d5a864640e1f4b6e526ee95f093fc`  
		Last Modified: Thu, 02 Mar 2023 18:41:08 GMT  
		Size: 507.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.4010; amd64

```console
$ docker pull nats@sha256:43348610453f5ecf2cb1eb6b88a459f7ad59353df14950ea55d72a27737f66af
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111708291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94392dbb17d455d1e80a3bc24798e3e1d761cbcd472f1616a352d0995335dbf0`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 07 Feb 2023 10:14:28 GMT
RUN Apply image 10.0.17763.4010
# Thu, 16 Feb 2023 02:07:44 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Mar 2023 19:19:54 GMT
RUN cmd /S /C #(nop) COPY file:c0761502e8e3e74fa63209f49b4d4f61a9c596c726f61d96e045d0b22538ada5 in C:\nats-server.exe 
# Thu, 02 Mar 2023 19:19:55 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Mar 2023 19:19:56 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Mar 2023 19:19:57 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:00eaf3341cd3cc6b72f91399cb3bd1aba30eb7eead7596532fe54c4bf1b010d7`  
		Last Modified: Thu, 16 Feb 2023 00:31:21 GMT  
		Size: 106.7 MB (106674970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efce19f72ba3efadcebf91b9628f9e85de500fcaa86b6ec8076169cc4bb312c0`  
		Last Modified: Thu, 16 Feb 2023 02:08:32 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4653b8562b98f6d770621adbd89d3392ed2c490da6c30dec79027c7e24ca6b`  
		Last Modified: Thu, 02 Mar 2023 19:20:48 GMT  
		Size: 5.0 MB (5026943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283f9c4ca607d846e0fc14dd248b106caf329d7c20316e59898b4a202459a77`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c525626770477530f07d56e4934dd0c036e55624d0182762d6df8afbc46aa99`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cda701c245116defdc445fe6ef3e38f73716d9f527f2876d1843abaef3ca11`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7890747cf0e8bf22b460262ebe10c19f91d00c0710a010fbe2d48d81ca8f0`  
		Last Modified: Thu, 02 Mar 2023 19:20:46 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
