## `nats:latest`

```console
$ docker pull nats@sha256:edfbb6f15ab27d0e8c13505b6d80cbba9b4e67d3469696d84b56cb0a2a74e60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2300; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:dad4f69520337c2a80d2a9123963c971836f07f530cf4b7c56dde98a622e0a6b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4578170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba73da93bdda8525a9f473851ee3de9a2d23c21e1d0a51d7da118bc122df420`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 21:23:03 GMT
COPY file:4070919cac43aa01e3ef5dd95589f24a9d649dcc7b4d6364927c764b1f90392e in /nats-server 
# Fri, 03 Dec 2021 21:23:04 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 21:23:04 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 21:23:04 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 21:23:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:730cae3de796bb1fbb06f0f847317c2b738bf9af9d1233daafcf2f708eade5ec`  
		Last Modified: Fri, 03 Dec 2021 21:24:01 GMT  
		Size: 4.6 MB (4577696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39027e71725d02ee81938943fd0f3e980f01abbe21c5e8f8ea8219687aaae862`  
		Last Modified: Fri, 03 Dec 2021 21:24:00 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:78ee1d57413d89c46e808dbb121ad895537b74af783c6e6189366afa07638b66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3276dd6f6de73a2af8ca0c6bd2dc88c7f7ae0a0ce334bcae39c14047aab540`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:025e99b21a301a69c768cc2c72e67c371165b6314d59d0a5a95958216fd24eac in /nats-server 
# Sat, 04 Dec 2021 07:52:28 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Sat, 04 Dec 2021 07:52:29 GMT
EXPOSE 4222 6222 8222
# Sat, 04 Dec 2021 07:52:29 GMT
ENTRYPOINT ["/nats-server"]
# Sat, 04 Dec 2021 07:52:30 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:75a8e365d6e58c8d8f7fe944a206f76f3e800542aca1b53e849c4bffc78fd22d`  
		Last Modified: Sat, 04 Dec 2021 07:55:01 GMT  
		Size: 4.2 MB (4237211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2920e0912e6a42ee2fd0b7b8b31c6cca01c6c99f16c760f904492422ff7cae`  
		Last Modified: Sat, 04 Dec 2021 07:54:58 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2300; amd64

```console
$ docker pull nats@sha256:99c7322b540961f363b09f8639858695602351709ff4bd8b883dd5ccd0ff2670
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107426609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfeb0ce069f091d552a8ecdaf57a0e8f47fffc5d34d7aff5cc5d3d60886d002`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:03:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 02 Dec 2021 23:17:27 GMT
RUN cmd /S /C #(nop) COPY file:20c797e6dad00d7098dbf6d4d158c380fd073bc5fc24a80fd4f23205af77a338 in C:\nats-server.exe 
# Thu, 02 Dec 2021 23:17:28 GMT
RUN cmd /S /C #(nop) COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in C:\nats-server.conf 
# Thu, 02 Dec 2021 23:17:29 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 23:17:30 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 02 Dec 2021 23:17:31 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1d3f90d67d7551be12e9caf53f786235234151f513c0aadc754e5f033e183641`  
		Last Modified: Wed, 10 Nov 2021 17:06:32 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c80f67e6bdb94f78501d521f07fb2bf8634fec39442b25df7fe32a479d4a84`  
		Last Modified: Thu, 02 Dec 2021 23:21:20 GMT  
		Size: 4.6 MB (4637256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be64ef39306c1a5d7e6a283c3a0269013221313695bdacb6a5135799347e477`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.8 KB (1772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da9f12dc4664d0ec4aea4094087fba83f2fbfaf0e55c8329fd5f87cbe76f65d`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083e9d445c6220eda3b7812fdda284918ddf4ed878f984e4ccdfa2b98e5adba8`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de499b1ce88b906fea231dff65edaabb6610c8b553c2be0238dce603e9b5589`  
		Last Modified: Thu, 02 Dec 2021 23:21:19 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
