## `nats:2-scratch`

```console
$ docker pull nats@sha256:63fcef243491a588a0be05f032de4588ff0b94b2472a6324ffa29ccdf4ad6bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

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

### `nats:2-scratch` - linux; arm variant v6

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

### `nats:2-scratch` - linux; arm variant v7

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

### `nats:2-scratch` - linux; arm64 variant v8

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
