## `nats:latest`

```console
$ docker pull nats@sha256:fa94605d0fbd684099b82914ab2604d662e125f1c27de977811c3677bc458a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
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
$ docker pull nats@sha256:8fc5b8a3af8cfd5209257567fb79ddc6adaa89aacb52f4b3b41c383bd28606e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5179709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb6f5ca89e0f8f4abd47d0dd20827db81f70160eae3c98d37e0fdbffeadedac`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:49:32 GMT
COPY file:c29c5d74c10915450ad41c3de7b25317b6802356e2d8da2a439b438b5b9b0036 in /nats-server 
# Tue, 19 Sep 2023 23:49:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:49:32 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:49:32 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:49:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:eda1601301f660b9f799945082ebd0ad9d1f9f10d9b7c7b54fb453ac5434764d`  
		Last Modified: Tue, 19 Sep 2023 23:50:27 GMT  
		Size: 5.2 MB (5179200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c1753d8953750d3d304538192c48170b3851ce4ee6f42b4083942a18117880`  
		Last Modified: Tue, 19 Sep 2023 23:50:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:4f09dbc6c43267500545fe441ec8057908d1b6bab5333c432c5e3d4c7ea0fd58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4980014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898dfa8e8c4c3e0c69c7c3aec16c90f1f6db172f3af0e7ff763b3bf8db42ed3c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:49:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:51aacaba9769a3f16e0467be1fc8eb86122f6f3496e89e41b61e0038083ae308 in /nats-server 
# Tue, 19 Sep 2023 23:49:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:49:29 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:49:29 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:49:29 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6a6e165fccf6da77ad3b09408162fc7daaafe266b71dd5da8679594aa110a3a5`  
		Last Modified: Wed, 06 Sep 2023 23:05:32 GMT  
		Size: 5.0 MB (4979506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07c6021b659fa78c25ff92ad1e74c46e34c95c5e691ca45f27ced97ea7ef9e2`  
		Last Modified: Tue, 19 Sep 2023 23:50:15 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:dd0bcaa689e244c1836c63f697b4229f1add60bfd786e0e02a9f37c6cb4408b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5030858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58505b09cd35074b35f5969778f252974001825fe789881ae56a278998bbe9c2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:43:03 GMT
COPY file:4a7474cb3b56fa1a7d66755a85c37a303f5e0e72d531740981aa82879c1edb9c in /nats-server 
# Tue, 19 Sep 2023 23:43:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:43:03 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:43:04 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:43:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:72049e33bf3141d0cf86c048b6b2ecd8566f5476c3934f9c198a548c99706c74`  
		Last Modified: Tue, 19 Sep 2023 23:44:04 GMT  
		Size: 5.0 MB (5030352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91b0ac736fed7878107d852356b9cecbacdf21e0bc1d8bdb8478629a443a2e2`  
		Last Modified: Tue, 19 Sep 2023 23:44:03 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:91e7a991da679db1020b25a760298f6944a9ea917e9ae90f10d1d7de9381fec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4778849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1745f4f81f20c728e9276ed07416c88490859cdbed438bdcb68aa051eb586c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 19 Sep 2023 23:42:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:d6eca5c67de65d1a8a30a51ea7318b044949c77108b2fdccc5aa0054c068c196 in /nats-server 
# Tue, 19 Sep 2023 23:42:56 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Tue, 19 Sep 2023 23:42:56 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:42:56 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 19 Sep 2023 23:42:56 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:88e5ff7f26ea25c6d2ab092989d9372cb32b3e60880124facfcefd7d3f0b7591`  
		Last Modified: Wed, 06 Sep 2023 22:40:49 GMT  
		Size: 4.8 MB (4778340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2424880e07e944598022ff8713b5897eb59c72af17978f7a3f1afa42dd022088`  
		Last Modified: Tue, 19 Sep 2023 23:43:51 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.4851; amd64

```console
$ docker pull nats@sha256:4a424d5ccb3ce81492d4a2aecc5bbe03a67a145345746a1d96c026d7956f33f2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110068714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c344b7589180b9b78bc248edaae3e05a72d7b3bd1240c9f0ecbc2bd8414643d3`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 05:08:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 20 Sep 2023 00:18:51 GMT
RUN cmd /S /C #(nop) COPY file:82881a6eaae1fdef881aedd297eada2f8ec0fc40e73c31dbc83c116c9f282e11 in C:\nats-server.exe 
# Wed, 20 Sep 2023 00:18:52 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 20 Sep 2023 00:18:52 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 20 Sep 2023 00:18:53 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 20 Sep 2023 00:18:54 GMT
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
	-	`sha256:8e311c6fa6640185d0147e86e5eee4ab6aac292985c5e1e0daeb8170482fd33d`  
		Last Modified: Wed, 20 Sep 2023 00:20:06 GMT  
		Size: 5.6 MB (5569723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b919469d50b165a5c87e445ee493dda4912cf2ad8db689c6d84a298c92e3b9`  
		Last Modified: Wed, 20 Sep 2023 00:20:05 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d34608f67091df8d80f28a392deb160738bbe00ec2a279d9edcfdd3b152eb8`  
		Last Modified: Wed, 20 Sep 2023 00:20:05 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c38e775b4dd4f949ccbee2cc13bc595e7ffad034c1ba158d7a8451c574cb98`  
		Last Modified: Wed, 20 Sep 2023 00:20:05 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc2e4e8b1ee6fac6ba0333ec74b715dc57449b31dc90cf5ad2315b8a962bc49`  
		Last Modified: Wed, 20 Sep 2023 00:20:05 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
