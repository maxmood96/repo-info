<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.20`](#nats2-alpine320)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.20`](#nats210-alpine320)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-1809`](#nats210-nanoserver-1809)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-1809`](#nats210-windowsservercore-1809)
-	[`nats:2.10.22`](#nats21022)
-	[`nats:2.10.22-alpine`](#nats21022-alpine)
-	[`nats:2.10.22-alpine3.20`](#nats21022-alpine320)
-	[`nats:2.10.22-linux`](#nats21022-linux)
-	[`nats:2.10.22-nanoserver`](#nats21022-nanoserver)
-	[`nats:2.10.22-nanoserver-1809`](#nats21022-nanoserver-1809)
-	[`nats:2.10.22-scratch`](#nats21022-scratch)
-	[`nats:2.10.22-windowsservercore`](#nats21022-windowsservercore)
-	[`nats:2.10.22-windowsservercore-1809`](#nats21022-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.20`](#natsalpine320)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:22291a43a802939fcfb2f6bacc0895fe3e7a0a911d90089fcb80aa542a7916a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6414; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:cf17ea3e72ac5786933f6830c6f8a1f314ee3227c6d5a43a8208cd2209795d1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa91a8e01e866d6ac77564c2f6479ba33abf92c46beb144f3b21eccbc3da73d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:4e74b2e1e01358cf9fa59c99b10fbb480dcd04043aa01e911cbb369929a58b6d in /nats-server 
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:20:25 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:20:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6f7dfeec586f016d13de8ccc72ee9a4d0266081d746284dd24553679e8f270a`  
		Last Modified: Thu, 17 Oct 2024 21:21:01 GMT  
		Size: 5.7 MB (5748818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b070d5d9d06e85ff9fbf39e87e9d234e69f485f88e1e1e1e9e292793325531`  
		Last Modified: Thu, 17 Oct 2024 21:21:00 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:a69426fe3cb56df6a0ee6b3ffa731fed7807b3b7136124726a1e4b87f9a470c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f66e9ff2284e532d8dcdcc0ec25768e152719b68aaa6d29ee1118037fa85f25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 22:17:13 GMT
COPY file:b65e8a9bb5f2b4c735a6f8c122ee2d12894e9117b3eb8415ee37a09eb3dfc8fc in /nats-server 
# Thu, 17 Oct 2024 22:17:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 22:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:14 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 22:17:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:643a17103c442b34df1e96cddbbbe769ef86067423b6949edc6a18c2e37276ba`  
		Last Modified: Thu, 17 Oct 2024 22:17:55 GMT  
		Size: 5.4 MB (5401876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea3faf87f8ffaa4bbacb9d0a81ffd3271e548798e67909dd40052b0bfc7d17`  
		Last Modified: Thu, 17 Oct 2024 22:17:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6069286023d0aa7e507339d8ffb1fd96511f097f722defdde0b4aa8ab4bfbb18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978c140eae43e730d89beb80a0cecdc21d5f0bbc918740ef666ae6ca452fffab`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:41:31 GMT
COPY file:39d7a23794edfcc30c80279af72b7bb8c06fb246cf7ca6c9a42367fcedfd8ad8 in /nats-server 
# Thu, 17 Oct 2024 21:41:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:41:32 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:41:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:837a74f8e729034ff6fc0c30d887028e32b5b1fe59cfb5a4921c7ca9d7625d1e`  
		Last Modified: Thu, 17 Oct 2024 21:42:07 GMT  
		Size: 5.3 MB (5310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66b03fb1668e0ebc0e509084c23d0210d71d0aaa08b9adc6809b50a4f82617`  
		Last Modified: Thu, 17 Oct 2024 21:42:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:9dc6c878ae8689a81e1cb11e7f446214f0eac6afe87d0debc0e0ee5ce81f1133
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695f18f0d73cd9368d192965881be9889ddb8cd16229ffcd059d0445cef412`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:24:33 GMT
COPY file:3d2381b9bf875590f88faa41270a50686e219045e55f00d47f0a3eee4b321bb2 in /nats-server 
# Thu, 17 Oct 2024 21:24:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:24:34 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:24:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:649ac2cb3ceb83f140568686079586cee4e9d5b3f9c34d5c850170a7c4255721`  
		Last Modified: Thu, 17 Oct 2024 21:25:11 GMT  
		Size: 5.3 MB (5279100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65356850f21a24152c66a4e8c3dd9008e2bb460105560be62856e6cc871a3d`  
		Last Modified: Thu, 17 Oct 2024 21:25:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:ecf979b855b9d1f3f6e9958abadfa89125bbba78a418fa725e3746fb2c566118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5602359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253fbe5efbd93d154ad650a47694d0e8b5f4b175dca7a4d3f81ac01f550b9021`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 02:50:14 GMT
COPY file:271e6c0ff401adcd125f2dfef8362ecfc809360856739670b17b3d60e010d872 in /nats-server 
# Fri, 27 Sep 2024 02:50:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 02:50:15 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:15 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 02:50:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c3217868c91b7a4ec1706f93f1d04f3e870c4b7d72d4ed60e3a0f7b9231dcc48`  
		Last Modified: Fri, 27 Sep 2024 02:50:48 GMT  
		Size: 5.6 MB (5601851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a38ff285b474e22578457a2ba0e56f65860a5323d354991b9e438250a392640`  
		Last Modified: Fri, 27 Sep 2024 02:50:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:aa92b18c4aaa8b4a86b817c76c7879136117bb5f6e506cd57b2b407612ce8ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da025743137b99ca37782c7c65b87197d643ecdd42e7210da78e20f218769df7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:17:52 GMT
RUN cmd /S /C #(nop) COPY file:8e415274f0a16ec3fa03a87478f007a6a8ede142612bbcd4aa265fef9c8611e4 in C:\nats-server.exe 
# Thu, 17 Oct 2024 22:17:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6a46f1af9b261dfa3ca4c23edabd47ada1a0c2242f883f8fc4e82d0e08abf`  
		Last Modified: Thu, 10 Oct 2024 00:41:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ede2810b9c7050684298f17d5ea9f7733eac55d920c1a344403c3a47adec223`  
		Last Modified: Thu, 17 Oct 2024 22:18:39 GMT  
		Size: 5.9 MB (5870144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6fdf5dc8052b24e56cd315505d0c008ec1aedadf4826d83b7c970cea8c887a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038bfb23519c0926ece84c8e7e5d34e03f7a0722a552518de0ddb674adb4806`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514425d814a52dd1a55dd2a61bceb51b7700a3e740c02b0abffd877c7dfef55d`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f9d7551799d2a32fab62c45954fd3d568fa4f52ad0dabe4670e12c857e87a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:11f9e3db3a0be9938832a5d1368d596ebd4b29fb4d0081faf79c5eca5bc5de1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:2bc41d9c0116d148cb34ec27494ad2d4dbc00af9dd75ff4287285d7bf0e4a4b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490e1f605d26f9271d52d5572fcf7daa76c6a2663e53363cb117ffe82b9289a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:20:16 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:20:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:20:19 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:20:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1182bbe83cb5dffc4c5111d0eae24291762eed6c5ad0fcc16f7adb4d5dbf8ce`  
		Last Modified: Thu, 17 Oct 2024 21:20:42 GMT  
		Size: 6.2 MB (6205597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81ba83521b841dc3eebb71f57e30308ccd5cba4e54f2d64cee7c9c95f287ed`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba842ab45501ef1d6a9cfe4cd7da9189a52de3620d0e5927a780e1a984e7858`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:18678ce6c4ee85e8fd7540cefeafdbb6e971a9182cbd281514250088151502d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8957927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bc8e02edcf576a6c0ca36420b4ad0a27ebd7112e82895c407c6fcdb3cf5cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:16:53 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:16:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 22:16:59 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 22:17:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc14a98b7dcabdd1f9abaadd9ba19693909ff74b16a1144dfbd488205aa652fc`  
		Last Modified: Thu, 17 Oct 2024 22:17:35 GMT  
		Size: 5.9 MB (5861447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b2b3b6eb6b1166c6d7b6dd00dd207188510d44a79bbc7aaa6deaca863d788`  
		Last Modified: Thu, 17 Oct 2024 22:17:34 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d271454f5e2e3966cd3722e57f02f67954b117bd4cfbab0e897286ce790b80`  
		Last Modified: Thu, 17 Oct 2024 22:17:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:efbf1e31d1287668e721964813207552a1e1a6cfd9295e6d557c4afad70c0ea8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e226bae4d0988e4f376ccaf3e72c8866a6ac9ee9cb5e992b10ec958897102d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:41:11 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:41:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:41:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:41:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889842c7efddd822dfd25eed95de81301ebf4915452badbd0c8bff2d8a3caa05`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 5.8 MB (5766406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4249e6a2cd5a39fe0c071fba606a912e3f144ad8403d4903b5aa14c389e05bb`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e822ac3e87d68f68a53efeed1ada7eb53d52422cd07e6a5081d0a0f76ac11531`  
		Last Modified: Thu, 17 Oct 2024 21:41:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:dcf714589eecb104d7fa02f8b96d9237e0ed304d4e197f173c1b1a7fa6b84c69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f18d784537de3ada637cd2d7141beff8d6d9f5cf28f891cd4479a973ec21344`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:24:02 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:24:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:24:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:24:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:24:09 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:24:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab23cb4c9e20f29a29e551b5c69af60c62de567048303107fc3e9915f73dda`  
		Last Modified: Thu, 17 Oct 2024 21:24:52 GMT  
		Size: 5.7 MB (5738848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01760873bd1fd3df13327f58577b680a1cc258467c2f5be99814d29a95d5a1`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c59ecf181a23129656d036419f90f28e0f05f75383157f1a587f0baba23dd3`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:2bad042975a1ddf4b27ae5705c3089b0fb170357a4ea8c1f12aa6a2b755c444d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9524279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69126879c257e7194d41aaa8571bb3e99c20849806570c6d9d3b1c2bc98d9e76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 02:50:03 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 02:50:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 02:50:05 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 02:50:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd523085a6b2d713f6ede8ddb823b69c092def1e9427f762de69b1edf71a92e`  
		Last Modified: Fri, 27 Sep 2024 02:50:35 GMT  
		Size: 6.1 MB (6061706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2a26252ad86d5d3dc0e4608b6ac9ed7efa6021f5484705ee40b27383fa3dc3`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ce1b00925dd2d2eed18086124ddb6332dee23d816b3eebc5282e33b669890c`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.20`

```console
$ docker pull nats@sha256:11f9e3db3a0be9938832a5d1368d596ebd4b29fb4d0081faf79c5eca5bc5de1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:2bc41d9c0116d148cb34ec27494ad2d4dbc00af9dd75ff4287285d7bf0e4a4b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490e1f605d26f9271d52d5572fcf7daa76c6a2663e53363cb117ffe82b9289a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:20:16 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:20:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:20:19 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:20:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1182bbe83cb5dffc4c5111d0eae24291762eed6c5ad0fcc16f7adb4d5dbf8ce`  
		Last Modified: Thu, 17 Oct 2024 21:20:42 GMT  
		Size: 6.2 MB (6205597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81ba83521b841dc3eebb71f57e30308ccd5cba4e54f2d64cee7c9c95f287ed`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba842ab45501ef1d6a9cfe4cd7da9189a52de3620d0e5927a780e1a984e7858`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:18678ce6c4ee85e8fd7540cefeafdbb6e971a9182cbd281514250088151502d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8957927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bc8e02edcf576a6c0ca36420b4ad0a27ebd7112e82895c407c6fcdb3cf5cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:16:53 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:16:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 22:16:59 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 22:17:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc14a98b7dcabdd1f9abaadd9ba19693909ff74b16a1144dfbd488205aa652fc`  
		Last Modified: Thu, 17 Oct 2024 22:17:35 GMT  
		Size: 5.9 MB (5861447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b2b3b6eb6b1166c6d7b6dd00dd207188510d44a79bbc7aaa6deaca863d788`  
		Last Modified: Thu, 17 Oct 2024 22:17:34 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d271454f5e2e3966cd3722e57f02f67954b117bd4cfbab0e897286ce790b80`  
		Last Modified: Thu, 17 Oct 2024 22:17:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:efbf1e31d1287668e721964813207552a1e1a6cfd9295e6d557c4afad70c0ea8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e226bae4d0988e4f376ccaf3e72c8866a6ac9ee9cb5e992b10ec958897102d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:41:11 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:41:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:41:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:41:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889842c7efddd822dfd25eed95de81301ebf4915452badbd0c8bff2d8a3caa05`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 5.8 MB (5766406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4249e6a2cd5a39fe0c071fba606a912e3f144ad8403d4903b5aa14c389e05bb`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e822ac3e87d68f68a53efeed1ada7eb53d52422cd07e6a5081d0a0f76ac11531`  
		Last Modified: Thu, 17 Oct 2024 21:41:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:dcf714589eecb104d7fa02f8b96d9237e0ed304d4e197f173c1b1a7fa6b84c69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f18d784537de3ada637cd2d7141beff8d6d9f5cf28f891cd4479a973ec21344`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:24:02 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:24:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:24:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:24:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:24:09 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:24:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab23cb4c9e20f29a29e551b5c69af60c62de567048303107fc3e9915f73dda`  
		Last Modified: Thu, 17 Oct 2024 21:24:52 GMT  
		Size: 5.7 MB (5738848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01760873bd1fd3df13327f58577b680a1cc258467c2f5be99814d29a95d5a1`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c59ecf181a23129656d036419f90f28e0f05f75383157f1a587f0baba23dd3`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:2bad042975a1ddf4b27ae5705c3089b0fb170357a4ea8c1f12aa6a2b755c444d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9524279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69126879c257e7194d41aaa8571bb3e99c20849806570c6d9d3b1c2bc98d9e76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 02:50:03 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 02:50:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 02:50:05 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 02:50:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd523085a6b2d713f6ede8ddb823b69c092def1e9427f762de69b1edf71a92e`  
		Last Modified: Fri, 27 Sep 2024 02:50:35 GMT  
		Size: 6.1 MB (6061706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2a26252ad86d5d3dc0e4608b6ac9ed7efa6021f5484705ee40b27383fa3dc3`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ce1b00925dd2d2eed18086124ddb6332dee23d816b3eebc5282e33b669890c`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:99d82c006a940560cd7270494d4b072ef2187f60d9b2f96053d3c4a720890e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:cf17ea3e72ac5786933f6830c6f8a1f314ee3227c6d5a43a8208cd2209795d1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa91a8e01e866d6ac77564c2f6479ba33abf92c46beb144f3b21eccbc3da73d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:4e74b2e1e01358cf9fa59c99b10fbb480dcd04043aa01e911cbb369929a58b6d in /nats-server 
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:20:25 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:20:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6f7dfeec586f016d13de8ccc72ee9a4d0266081d746284dd24553679e8f270a`  
		Last Modified: Thu, 17 Oct 2024 21:21:01 GMT  
		Size: 5.7 MB (5748818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b070d5d9d06e85ff9fbf39e87e9d234e69f485f88e1e1e1e9e292793325531`  
		Last Modified: Thu, 17 Oct 2024 21:21:00 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a69426fe3cb56df6a0ee6b3ffa731fed7807b3b7136124726a1e4b87f9a470c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f66e9ff2284e532d8dcdcc0ec25768e152719b68aaa6d29ee1118037fa85f25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 22:17:13 GMT
COPY file:b65e8a9bb5f2b4c735a6f8c122ee2d12894e9117b3eb8415ee37a09eb3dfc8fc in /nats-server 
# Thu, 17 Oct 2024 22:17:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 22:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:14 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 22:17:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:643a17103c442b34df1e96cddbbbe769ef86067423b6949edc6a18c2e37276ba`  
		Last Modified: Thu, 17 Oct 2024 22:17:55 GMT  
		Size: 5.4 MB (5401876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea3faf87f8ffaa4bbacb9d0a81ffd3271e548798e67909dd40052b0bfc7d17`  
		Last Modified: Thu, 17 Oct 2024 22:17:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6069286023d0aa7e507339d8ffb1fd96511f097f722defdde0b4aa8ab4bfbb18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978c140eae43e730d89beb80a0cecdc21d5f0bbc918740ef666ae6ca452fffab`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:41:31 GMT
COPY file:39d7a23794edfcc30c80279af72b7bb8c06fb246cf7ca6c9a42367fcedfd8ad8 in /nats-server 
# Thu, 17 Oct 2024 21:41:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:41:32 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:41:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:837a74f8e729034ff6fc0c30d887028e32b5b1fe59cfb5a4921c7ca9d7625d1e`  
		Last Modified: Thu, 17 Oct 2024 21:42:07 GMT  
		Size: 5.3 MB (5310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66b03fb1668e0ebc0e509084c23d0210d71d0aaa08b9adc6809b50a4f82617`  
		Last Modified: Thu, 17 Oct 2024 21:42:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:9dc6c878ae8689a81e1cb11e7f446214f0eac6afe87d0debc0e0ee5ce81f1133
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695f18f0d73cd9368d192965881be9889ddb8cd16229ffcd059d0445cef412`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:24:33 GMT
COPY file:3d2381b9bf875590f88faa41270a50686e219045e55f00d47f0a3eee4b321bb2 in /nats-server 
# Thu, 17 Oct 2024 21:24:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:24:34 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:24:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:649ac2cb3ceb83f140568686079586cee4e9d5b3f9c34d5c850170a7c4255721`  
		Last Modified: Thu, 17 Oct 2024 21:25:11 GMT  
		Size: 5.3 MB (5279100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65356850f21a24152c66a4e8c3dd9008e2bb460105560be62856e6cc871a3d`  
		Last Modified: Thu, 17 Oct 2024 21:25:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:ecf979b855b9d1f3f6e9958abadfa89125bbba78a418fa725e3746fb2c566118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5602359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253fbe5efbd93d154ad650a47694d0e8b5f4b175dca7a4d3f81ac01f550b9021`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 02:50:14 GMT
COPY file:271e6c0ff401adcd125f2dfef8362ecfc809360856739670b17b3d60e010d872 in /nats-server 
# Fri, 27 Sep 2024 02:50:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 02:50:15 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:15 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 02:50:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c3217868c91b7a4ec1706f93f1d04f3e870c4b7d72d4ed60e3a0f7b9231dcc48`  
		Last Modified: Fri, 27 Sep 2024 02:50:48 GMT  
		Size: 5.6 MB (5601851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a38ff285b474e22578457a2ba0e56f65860a5323d354991b9e438250a392640`  
		Last Modified: Fri, 27 Sep 2024 02:50:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:5762142a7f15bd3e97dda219ec3985997c351ce00b39dbfc9a771e735ecdce49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:aa92b18c4aaa8b4a86b817c76c7879136117bb5f6e506cd57b2b407612ce8ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da025743137b99ca37782c7c65b87197d643ecdd42e7210da78e20f218769df7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:17:52 GMT
RUN cmd /S /C #(nop) COPY file:8e415274f0a16ec3fa03a87478f007a6a8ede142612bbcd4aa265fef9c8611e4 in C:\nats-server.exe 
# Thu, 17 Oct 2024 22:17:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6a46f1af9b261dfa3ca4c23edabd47ada1a0c2242f883f8fc4e82d0e08abf`  
		Last Modified: Thu, 10 Oct 2024 00:41:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ede2810b9c7050684298f17d5ea9f7733eac55d920c1a344403c3a47adec223`  
		Last Modified: Thu, 17 Oct 2024 22:18:39 GMT  
		Size: 5.9 MB (5870144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6fdf5dc8052b24e56cd315505d0c008ec1aedadf4826d83b7c970cea8c887a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038bfb23519c0926ece84c8e7e5d34e03f7a0722a552518de0ddb674adb4806`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514425d814a52dd1a55dd2a61bceb51b7700a3e740c02b0abffd877c7dfef55d`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f9d7551799d2a32fab62c45954fd3d568fa4f52ad0dabe4670e12c857e87a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:5762142a7f15bd3e97dda219ec3985997c351ce00b39dbfc9a771e735ecdce49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:aa92b18c4aaa8b4a86b817c76c7879136117bb5f6e506cd57b2b407612ce8ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da025743137b99ca37782c7c65b87197d643ecdd42e7210da78e20f218769df7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:17:52 GMT
RUN cmd /S /C #(nop) COPY file:8e415274f0a16ec3fa03a87478f007a6a8ede142612bbcd4aa265fef9c8611e4 in C:\nats-server.exe 
# Thu, 17 Oct 2024 22:17:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6a46f1af9b261dfa3ca4c23edabd47ada1a0c2242f883f8fc4e82d0e08abf`  
		Last Modified: Thu, 10 Oct 2024 00:41:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ede2810b9c7050684298f17d5ea9f7733eac55d920c1a344403c3a47adec223`  
		Last Modified: Thu, 17 Oct 2024 22:18:39 GMT  
		Size: 5.9 MB (5870144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6fdf5dc8052b24e56cd315505d0c008ec1aedadf4826d83b7c970cea8c887a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038bfb23519c0926ece84c8e7e5d34e03f7a0722a552518de0ddb674adb4806`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514425d814a52dd1a55dd2a61bceb51b7700a3e740c02b0abffd877c7dfef55d`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f9d7551799d2a32fab62c45954fd3d568fa4f52ad0dabe4670e12c857e87a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:99d82c006a940560cd7270494d4b072ef2187f60d9b2f96053d3c4a720890e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:cf17ea3e72ac5786933f6830c6f8a1f314ee3227c6d5a43a8208cd2209795d1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa91a8e01e866d6ac77564c2f6479ba33abf92c46beb144f3b21eccbc3da73d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:4e74b2e1e01358cf9fa59c99b10fbb480dcd04043aa01e911cbb369929a58b6d in /nats-server 
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:20:25 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:20:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6f7dfeec586f016d13de8ccc72ee9a4d0266081d746284dd24553679e8f270a`  
		Last Modified: Thu, 17 Oct 2024 21:21:01 GMT  
		Size: 5.7 MB (5748818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b070d5d9d06e85ff9fbf39e87e9d234e69f485f88e1e1e1e9e292793325531`  
		Last Modified: Thu, 17 Oct 2024 21:21:00 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a69426fe3cb56df6a0ee6b3ffa731fed7807b3b7136124726a1e4b87f9a470c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f66e9ff2284e532d8dcdcc0ec25768e152719b68aaa6d29ee1118037fa85f25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 22:17:13 GMT
COPY file:b65e8a9bb5f2b4c735a6f8c122ee2d12894e9117b3eb8415ee37a09eb3dfc8fc in /nats-server 
# Thu, 17 Oct 2024 22:17:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 22:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:14 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 22:17:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:643a17103c442b34df1e96cddbbbe769ef86067423b6949edc6a18c2e37276ba`  
		Last Modified: Thu, 17 Oct 2024 22:17:55 GMT  
		Size: 5.4 MB (5401876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea3faf87f8ffaa4bbacb9d0a81ffd3271e548798e67909dd40052b0bfc7d17`  
		Last Modified: Thu, 17 Oct 2024 22:17:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6069286023d0aa7e507339d8ffb1fd96511f097f722defdde0b4aa8ab4bfbb18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978c140eae43e730d89beb80a0cecdc21d5f0bbc918740ef666ae6ca452fffab`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:41:31 GMT
COPY file:39d7a23794edfcc30c80279af72b7bb8c06fb246cf7ca6c9a42367fcedfd8ad8 in /nats-server 
# Thu, 17 Oct 2024 21:41:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:41:32 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:41:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:837a74f8e729034ff6fc0c30d887028e32b5b1fe59cfb5a4921c7ca9d7625d1e`  
		Last Modified: Thu, 17 Oct 2024 21:42:07 GMT  
		Size: 5.3 MB (5310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66b03fb1668e0ebc0e509084c23d0210d71d0aaa08b9adc6809b50a4f82617`  
		Last Modified: Thu, 17 Oct 2024 21:42:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:9dc6c878ae8689a81e1cb11e7f446214f0eac6afe87d0debc0e0ee5ce81f1133
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695f18f0d73cd9368d192965881be9889ddb8cd16229ffcd059d0445cef412`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:24:33 GMT
COPY file:3d2381b9bf875590f88faa41270a50686e219045e55f00d47f0a3eee4b321bb2 in /nats-server 
# Thu, 17 Oct 2024 21:24:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:24:34 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:24:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:649ac2cb3ceb83f140568686079586cee4e9d5b3f9c34d5c850170a7c4255721`  
		Last Modified: Thu, 17 Oct 2024 21:25:11 GMT  
		Size: 5.3 MB (5279100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65356850f21a24152c66a4e8c3dd9008e2bb460105560be62856e6cc871a3d`  
		Last Modified: Thu, 17 Oct 2024 21:25:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:ecf979b855b9d1f3f6e9958abadfa89125bbba78a418fa725e3746fb2c566118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5602359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253fbe5efbd93d154ad650a47694d0e8b5f4b175dca7a4d3f81ac01f550b9021`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 02:50:14 GMT
COPY file:271e6c0ff401adcd125f2dfef8362ecfc809360856739670b17b3d60e010d872 in /nats-server 
# Fri, 27 Sep 2024 02:50:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 02:50:15 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:15 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 02:50:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c3217868c91b7a4ec1706f93f1d04f3e870c4b7d72d4ed60e3a0f7b9231dcc48`  
		Last Modified: Fri, 27 Sep 2024 02:50:48 GMT  
		Size: 5.6 MB (5601851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a38ff285b474e22578457a2ba0e56f65860a5323d354991b9e438250a392640`  
		Last Modified: Fri, 27 Sep 2024 02:50:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:697ec56703339f66b45f1f84d1d28c50fea6d1913340dc3417f07cb03466d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:143e9e296c13d7a71bfa00b08230709e757e96150a25e8bce3ad72f9538c4d93
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908432251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b77a82bb41c8594376ef53c13cf0fb93896749662022faf0b92f3ff75dc3b18`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 10 Oct 2024 00:38:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Oct 2024 00:38:10 GMT
ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:15:24 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:15:26 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 17 Oct 2024 22:15:28 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 17 Oct 2024 22:16:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 17 Oct 2024 22:17:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 17 Oct 2024 22:17:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196a5b13ab4e3918e43ddd7bbb877dbf52e832257c9ec3eb8019cd414af2e3a`  
		Last Modified: Thu, 10 Oct 2024 00:40:53 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484871eca2e8c738eb04d659975dd4a80e9dae8daf6e59d2297e6c3e81f03bd6`  
		Last Modified: Thu, 10 Oct 2024 00:40:52 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368fa5ecea627e9b785fb5887c6fc61ba24222a0164cff921e705fe2608d154`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475e61a46a9199c2067156908c860a41c2e9745af42c903fb4ef6422082a246`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948095eebb084fb778711564072ea58aea5733478d3b2f451850a8f19705193f`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37e14f1bd78d70c68d454292424b48c3ee9cd02835c28d253c0acaef2e1947`  
		Last Modified: Thu, 17 Oct 2024 22:18:25 GMT  
		Size: 444.4 KB (444352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f75af290818f7d902ec97658a83cd371aed1a0648369ba143d70e628c2c480`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 6.1 MB (6149451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e19f4bee2c3ad99b0a342f55ddab3fad4c6537df793f3d0f2e0c0afbba481b`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1d61f19a1bcb3733a1bdefa6317397344bd1380cbc31ed46f8449ac9ca0710`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cbc0f6dd89bcef1b602c11babb7e58e8383097a287ac1c8e8d079b0c735af9`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22bd1ed76deddbcee8c0032b3760f182c88d86e44473ce346a6796644395b35`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:697ec56703339f66b45f1f84d1d28c50fea6d1913340dc3417f07cb03466d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:143e9e296c13d7a71bfa00b08230709e757e96150a25e8bce3ad72f9538c4d93
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908432251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b77a82bb41c8594376ef53c13cf0fb93896749662022faf0b92f3ff75dc3b18`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 10 Oct 2024 00:38:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Oct 2024 00:38:10 GMT
ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:15:24 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:15:26 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 17 Oct 2024 22:15:28 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 17 Oct 2024 22:16:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 17 Oct 2024 22:17:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 17 Oct 2024 22:17:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196a5b13ab4e3918e43ddd7bbb877dbf52e832257c9ec3eb8019cd414af2e3a`  
		Last Modified: Thu, 10 Oct 2024 00:40:53 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484871eca2e8c738eb04d659975dd4a80e9dae8daf6e59d2297e6c3e81f03bd6`  
		Last Modified: Thu, 10 Oct 2024 00:40:52 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368fa5ecea627e9b785fb5887c6fc61ba24222a0164cff921e705fe2608d154`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475e61a46a9199c2067156908c860a41c2e9745af42c903fb4ef6422082a246`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948095eebb084fb778711564072ea58aea5733478d3b2f451850a8f19705193f`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37e14f1bd78d70c68d454292424b48c3ee9cd02835c28d253c0acaef2e1947`  
		Last Modified: Thu, 17 Oct 2024 22:18:25 GMT  
		Size: 444.4 KB (444352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f75af290818f7d902ec97658a83cd371aed1a0648369ba143d70e628c2c480`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 6.1 MB (6149451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e19f4bee2c3ad99b0a342f55ddab3fad4c6537df793f3d0f2e0c0afbba481b`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1d61f19a1bcb3733a1bdefa6317397344bd1380cbc31ed46f8449ac9ca0710`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cbc0f6dd89bcef1b602c11babb7e58e8383097a287ac1c8e8d079b0c735af9`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22bd1ed76deddbcee8c0032b3760f182c88d86e44473ce346a6796644395b35`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:22291a43a802939fcfb2f6bacc0895fe3e7a0a911d90089fcb80aa542a7916a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:cf17ea3e72ac5786933f6830c6f8a1f314ee3227c6d5a43a8208cd2209795d1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa91a8e01e866d6ac77564c2f6479ba33abf92c46beb144f3b21eccbc3da73d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:4e74b2e1e01358cf9fa59c99b10fbb480dcd04043aa01e911cbb369929a58b6d in /nats-server 
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:20:25 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:20:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6f7dfeec586f016d13de8ccc72ee9a4d0266081d746284dd24553679e8f270a`  
		Last Modified: Thu, 17 Oct 2024 21:21:01 GMT  
		Size: 5.7 MB (5748818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b070d5d9d06e85ff9fbf39e87e9d234e69f485f88e1e1e1e9e292793325531`  
		Last Modified: Thu, 17 Oct 2024 21:21:00 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:a69426fe3cb56df6a0ee6b3ffa731fed7807b3b7136124726a1e4b87f9a470c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f66e9ff2284e532d8dcdcc0ec25768e152719b68aaa6d29ee1118037fa85f25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 22:17:13 GMT
COPY file:b65e8a9bb5f2b4c735a6f8c122ee2d12894e9117b3eb8415ee37a09eb3dfc8fc in /nats-server 
# Thu, 17 Oct 2024 22:17:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 22:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:14 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 22:17:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:643a17103c442b34df1e96cddbbbe769ef86067423b6949edc6a18c2e37276ba`  
		Last Modified: Thu, 17 Oct 2024 22:17:55 GMT  
		Size: 5.4 MB (5401876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea3faf87f8ffaa4bbacb9d0a81ffd3271e548798e67909dd40052b0bfc7d17`  
		Last Modified: Thu, 17 Oct 2024 22:17:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6069286023d0aa7e507339d8ffb1fd96511f097f722defdde0b4aa8ab4bfbb18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978c140eae43e730d89beb80a0cecdc21d5f0bbc918740ef666ae6ca452fffab`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:41:31 GMT
COPY file:39d7a23794edfcc30c80279af72b7bb8c06fb246cf7ca6c9a42367fcedfd8ad8 in /nats-server 
# Thu, 17 Oct 2024 21:41:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:41:32 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:41:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:837a74f8e729034ff6fc0c30d887028e32b5b1fe59cfb5a4921c7ca9d7625d1e`  
		Last Modified: Thu, 17 Oct 2024 21:42:07 GMT  
		Size: 5.3 MB (5310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66b03fb1668e0ebc0e509084c23d0210d71d0aaa08b9adc6809b50a4f82617`  
		Last Modified: Thu, 17 Oct 2024 21:42:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:9dc6c878ae8689a81e1cb11e7f446214f0eac6afe87d0debc0e0ee5ce81f1133
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695f18f0d73cd9368d192965881be9889ddb8cd16229ffcd059d0445cef412`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:24:33 GMT
COPY file:3d2381b9bf875590f88faa41270a50686e219045e55f00d47f0a3eee4b321bb2 in /nats-server 
# Thu, 17 Oct 2024 21:24:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:24:34 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:24:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:649ac2cb3ceb83f140568686079586cee4e9d5b3f9c34d5c850170a7c4255721`  
		Last Modified: Thu, 17 Oct 2024 21:25:11 GMT  
		Size: 5.3 MB (5279100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65356850f21a24152c66a4e8c3dd9008e2bb460105560be62856e6cc871a3d`  
		Last Modified: Thu, 17 Oct 2024 21:25:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:ecf979b855b9d1f3f6e9958abadfa89125bbba78a418fa725e3746fb2c566118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5602359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253fbe5efbd93d154ad650a47694d0e8b5f4b175dca7a4d3f81ac01f550b9021`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 02:50:14 GMT
COPY file:271e6c0ff401adcd125f2dfef8362ecfc809360856739670b17b3d60e010d872 in /nats-server 
# Fri, 27 Sep 2024 02:50:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 02:50:15 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:15 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 02:50:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c3217868c91b7a4ec1706f93f1d04f3e870c4b7d72d4ed60e3a0f7b9231dcc48`  
		Last Modified: Fri, 27 Sep 2024 02:50:48 GMT  
		Size: 5.6 MB (5601851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a38ff285b474e22578457a2ba0e56f65860a5323d354991b9e438250a392640`  
		Last Modified: Fri, 27 Sep 2024 02:50:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:aa92b18c4aaa8b4a86b817c76c7879136117bb5f6e506cd57b2b407612ce8ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da025743137b99ca37782c7c65b87197d643ecdd42e7210da78e20f218769df7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:17:52 GMT
RUN cmd /S /C #(nop) COPY file:8e415274f0a16ec3fa03a87478f007a6a8ede142612bbcd4aa265fef9c8611e4 in C:\nats-server.exe 
# Thu, 17 Oct 2024 22:17:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6a46f1af9b261dfa3ca4c23edabd47ada1a0c2242f883f8fc4e82d0e08abf`  
		Last Modified: Thu, 10 Oct 2024 00:41:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ede2810b9c7050684298f17d5ea9f7733eac55d920c1a344403c3a47adec223`  
		Last Modified: Thu, 17 Oct 2024 22:18:39 GMT  
		Size: 5.9 MB (5870144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6fdf5dc8052b24e56cd315505d0c008ec1aedadf4826d83b7c970cea8c887a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038bfb23519c0926ece84c8e7e5d34e03f7a0722a552518de0ddb674adb4806`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514425d814a52dd1a55dd2a61bceb51b7700a3e740c02b0abffd877c7dfef55d`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f9d7551799d2a32fab62c45954fd3d568fa4f52ad0dabe4670e12c857e87a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:11f9e3db3a0be9938832a5d1368d596ebd4b29fb4d0081faf79c5eca5bc5de1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:2bc41d9c0116d148cb34ec27494ad2d4dbc00af9dd75ff4287285d7bf0e4a4b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490e1f605d26f9271d52d5572fcf7daa76c6a2663e53363cb117ffe82b9289a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:20:16 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:20:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:20:19 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:20:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1182bbe83cb5dffc4c5111d0eae24291762eed6c5ad0fcc16f7adb4d5dbf8ce`  
		Last Modified: Thu, 17 Oct 2024 21:20:42 GMT  
		Size: 6.2 MB (6205597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81ba83521b841dc3eebb71f57e30308ccd5cba4e54f2d64cee7c9c95f287ed`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba842ab45501ef1d6a9cfe4cd7da9189a52de3620d0e5927a780e1a984e7858`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:18678ce6c4ee85e8fd7540cefeafdbb6e971a9182cbd281514250088151502d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8957927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bc8e02edcf576a6c0ca36420b4ad0a27ebd7112e82895c407c6fcdb3cf5cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:16:53 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:16:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 22:16:59 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 22:17:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc14a98b7dcabdd1f9abaadd9ba19693909ff74b16a1144dfbd488205aa652fc`  
		Last Modified: Thu, 17 Oct 2024 22:17:35 GMT  
		Size: 5.9 MB (5861447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b2b3b6eb6b1166c6d7b6dd00dd207188510d44a79bbc7aaa6deaca863d788`  
		Last Modified: Thu, 17 Oct 2024 22:17:34 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d271454f5e2e3966cd3722e57f02f67954b117bd4cfbab0e897286ce790b80`  
		Last Modified: Thu, 17 Oct 2024 22:17:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:efbf1e31d1287668e721964813207552a1e1a6cfd9295e6d557c4afad70c0ea8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e226bae4d0988e4f376ccaf3e72c8866a6ac9ee9cb5e992b10ec958897102d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:41:11 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:41:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:41:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:41:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889842c7efddd822dfd25eed95de81301ebf4915452badbd0c8bff2d8a3caa05`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 5.8 MB (5766406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4249e6a2cd5a39fe0c071fba606a912e3f144ad8403d4903b5aa14c389e05bb`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e822ac3e87d68f68a53efeed1ada7eb53d52422cd07e6a5081d0a0f76ac11531`  
		Last Modified: Thu, 17 Oct 2024 21:41:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:dcf714589eecb104d7fa02f8b96d9237e0ed304d4e197f173c1b1a7fa6b84c69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f18d784537de3ada637cd2d7141beff8d6d9f5cf28f891cd4479a973ec21344`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:24:02 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:24:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:24:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:24:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:24:09 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:24:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab23cb4c9e20f29a29e551b5c69af60c62de567048303107fc3e9915f73dda`  
		Last Modified: Thu, 17 Oct 2024 21:24:52 GMT  
		Size: 5.7 MB (5738848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01760873bd1fd3df13327f58577b680a1cc258467c2f5be99814d29a95d5a1`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c59ecf181a23129656d036419f90f28e0f05f75383157f1a587f0baba23dd3`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:2bad042975a1ddf4b27ae5705c3089b0fb170357a4ea8c1f12aa6a2b755c444d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9524279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69126879c257e7194d41aaa8571bb3e99c20849806570c6d9d3b1c2bc98d9e76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 02:50:03 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 02:50:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 02:50:05 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 02:50:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd523085a6b2d713f6ede8ddb823b69c092def1e9427f762de69b1edf71a92e`  
		Last Modified: Fri, 27 Sep 2024 02:50:35 GMT  
		Size: 6.1 MB (6061706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2a26252ad86d5d3dc0e4608b6ac9ed7efa6021f5484705ee40b27383fa3dc3`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ce1b00925dd2d2eed18086124ddb6332dee23d816b3eebc5282e33b669890c`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine3.20`

```console
$ docker pull nats@sha256:11f9e3db3a0be9938832a5d1368d596ebd4b29fb4d0081faf79c5eca5bc5de1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:2bc41d9c0116d148cb34ec27494ad2d4dbc00af9dd75ff4287285d7bf0e4a4b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490e1f605d26f9271d52d5572fcf7daa76c6a2663e53363cb117ffe82b9289a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:20:16 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:20:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:20:19 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:20:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1182bbe83cb5dffc4c5111d0eae24291762eed6c5ad0fcc16f7adb4d5dbf8ce`  
		Last Modified: Thu, 17 Oct 2024 21:20:42 GMT  
		Size: 6.2 MB (6205597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81ba83521b841dc3eebb71f57e30308ccd5cba4e54f2d64cee7c9c95f287ed`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba842ab45501ef1d6a9cfe4cd7da9189a52de3620d0e5927a780e1a984e7858`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:18678ce6c4ee85e8fd7540cefeafdbb6e971a9182cbd281514250088151502d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8957927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bc8e02edcf576a6c0ca36420b4ad0a27ebd7112e82895c407c6fcdb3cf5cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:16:53 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:16:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 22:16:59 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 22:17:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc14a98b7dcabdd1f9abaadd9ba19693909ff74b16a1144dfbd488205aa652fc`  
		Last Modified: Thu, 17 Oct 2024 22:17:35 GMT  
		Size: 5.9 MB (5861447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b2b3b6eb6b1166c6d7b6dd00dd207188510d44a79bbc7aaa6deaca863d788`  
		Last Modified: Thu, 17 Oct 2024 22:17:34 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d271454f5e2e3966cd3722e57f02f67954b117bd4cfbab0e897286ce790b80`  
		Last Modified: Thu, 17 Oct 2024 22:17:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:efbf1e31d1287668e721964813207552a1e1a6cfd9295e6d557c4afad70c0ea8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e226bae4d0988e4f376ccaf3e72c8866a6ac9ee9cb5e992b10ec958897102d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:41:11 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:41:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:41:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:41:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889842c7efddd822dfd25eed95de81301ebf4915452badbd0c8bff2d8a3caa05`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 5.8 MB (5766406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4249e6a2cd5a39fe0c071fba606a912e3f144ad8403d4903b5aa14c389e05bb`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e822ac3e87d68f68a53efeed1ada7eb53d52422cd07e6a5081d0a0f76ac11531`  
		Last Modified: Thu, 17 Oct 2024 21:41:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:dcf714589eecb104d7fa02f8b96d9237e0ed304d4e197f173c1b1a7fa6b84c69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f18d784537de3ada637cd2d7141beff8d6d9f5cf28f891cd4479a973ec21344`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:24:02 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:24:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:24:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:24:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:24:09 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:24:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab23cb4c9e20f29a29e551b5c69af60c62de567048303107fc3e9915f73dda`  
		Last Modified: Thu, 17 Oct 2024 21:24:52 GMT  
		Size: 5.7 MB (5738848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01760873bd1fd3df13327f58577b680a1cc258467c2f5be99814d29a95d5a1`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c59ecf181a23129656d036419f90f28e0f05f75383157f1a587f0baba23dd3`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:2bad042975a1ddf4b27ae5705c3089b0fb170357a4ea8c1f12aa6a2b755c444d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9524279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69126879c257e7194d41aaa8571bb3e99c20849806570c6d9d3b1c2bc98d9e76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 02:50:03 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 02:50:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 02:50:05 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 02:50:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd523085a6b2d713f6ede8ddb823b69c092def1e9427f762de69b1edf71a92e`  
		Last Modified: Fri, 27 Sep 2024 02:50:35 GMT  
		Size: 6.1 MB (6061706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2a26252ad86d5d3dc0e4608b6ac9ed7efa6021f5484705ee40b27383fa3dc3`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ce1b00925dd2d2eed18086124ddb6332dee23d816b3eebc5282e33b669890c`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:99d82c006a940560cd7270494d4b072ef2187f60d9b2f96053d3c4a720890e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:cf17ea3e72ac5786933f6830c6f8a1f314ee3227c6d5a43a8208cd2209795d1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa91a8e01e866d6ac77564c2f6479ba33abf92c46beb144f3b21eccbc3da73d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:4e74b2e1e01358cf9fa59c99b10fbb480dcd04043aa01e911cbb369929a58b6d in /nats-server 
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:20:25 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:20:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6f7dfeec586f016d13de8ccc72ee9a4d0266081d746284dd24553679e8f270a`  
		Last Modified: Thu, 17 Oct 2024 21:21:01 GMT  
		Size: 5.7 MB (5748818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b070d5d9d06e85ff9fbf39e87e9d234e69f485f88e1e1e1e9e292793325531`  
		Last Modified: Thu, 17 Oct 2024 21:21:00 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a69426fe3cb56df6a0ee6b3ffa731fed7807b3b7136124726a1e4b87f9a470c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f66e9ff2284e532d8dcdcc0ec25768e152719b68aaa6d29ee1118037fa85f25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 22:17:13 GMT
COPY file:b65e8a9bb5f2b4c735a6f8c122ee2d12894e9117b3eb8415ee37a09eb3dfc8fc in /nats-server 
# Thu, 17 Oct 2024 22:17:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 22:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:14 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 22:17:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:643a17103c442b34df1e96cddbbbe769ef86067423b6949edc6a18c2e37276ba`  
		Last Modified: Thu, 17 Oct 2024 22:17:55 GMT  
		Size: 5.4 MB (5401876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea3faf87f8ffaa4bbacb9d0a81ffd3271e548798e67909dd40052b0bfc7d17`  
		Last Modified: Thu, 17 Oct 2024 22:17:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6069286023d0aa7e507339d8ffb1fd96511f097f722defdde0b4aa8ab4bfbb18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978c140eae43e730d89beb80a0cecdc21d5f0bbc918740ef666ae6ca452fffab`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:41:31 GMT
COPY file:39d7a23794edfcc30c80279af72b7bb8c06fb246cf7ca6c9a42367fcedfd8ad8 in /nats-server 
# Thu, 17 Oct 2024 21:41:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:41:32 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:41:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:837a74f8e729034ff6fc0c30d887028e32b5b1fe59cfb5a4921c7ca9d7625d1e`  
		Last Modified: Thu, 17 Oct 2024 21:42:07 GMT  
		Size: 5.3 MB (5310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66b03fb1668e0ebc0e509084c23d0210d71d0aaa08b9adc6809b50a4f82617`  
		Last Modified: Thu, 17 Oct 2024 21:42:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:9dc6c878ae8689a81e1cb11e7f446214f0eac6afe87d0debc0e0ee5ce81f1133
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695f18f0d73cd9368d192965881be9889ddb8cd16229ffcd059d0445cef412`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:24:33 GMT
COPY file:3d2381b9bf875590f88faa41270a50686e219045e55f00d47f0a3eee4b321bb2 in /nats-server 
# Thu, 17 Oct 2024 21:24:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:24:34 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:24:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:649ac2cb3ceb83f140568686079586cee4e9d5b3f9c34d5c850170a7c4255721`  
		Last Modified: Thu, 17 Oct 2024 21:25:11 GMT  
		Size: 5.3 MB (5279100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65356850f21a24152c66a4e8c3dd9008e2bb460105560be62856e6cc871a3d`  
		Last Modified: Thu, 17 Oct 2024 21:25:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:ecf979b855b9d1f3f6e9958abadfa89125bbba78a418fa725e3746fb2c566118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5602359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253fbe5efbd93d154ad650a47694d0e8b5f4b175dca7a4d3f81ac01f550b9021`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 02:50:14 GMT
COPY file:271e6c0ff401adcd125f2dfef8362ecfc809360856739670b17b3d60e010d872 in /nats-server 
# Fri, 27 Sep 2024 02:50:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 02:50:15 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:15 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 02:50:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c3217868c91b7a4ec1706f93f1d04f3e870c4b7d72d4ed60e3a0f7b9231dcc48`  
		Last Modified: Fri, 27 Sep 2024 02:50:48 GMT  
		Size: 5.6 MB (5601851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a38ff285b474e22578457a2ba0e56f65860a5323d354991b9e438250a392640`  
		Last Modified: Fri, 27 Sep 2024 02:50:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:5762142a7f15bd3e97dda219ec3985997c351ce00b39dbfc9a771e735ecdce49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:aa92b18c4aaa8b4a86b817c76c7879136117bb5f6e506cd57b2b407612ce8ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da025743137b99ca37782c7c65b87197d643ecdd42e7210da78e20f218769df7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:17:52 GMT
RUN cmd /S /C #(nop) COPY file:8e415274f0a16ec3fa03a87478f007a6a8ede142612bbcd4aa265fef9c8611e4 in C:\nats-server.exe 
# Thu, 17 Oct 2024 22:17:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6a46f1af9b261dfa3ca4c23edabd47ada1a0c2242f883f8fc4e82d0e08abf`  
		Last Modified: Thu, 10 Oct 2024 00:41:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ede2810b9c7050684298f17d5ea9f7733eac55d920c1a344403c3a47adec223`  
		Last Modified: Thu, 17 Oct 2024 22:18:39 GMT  
		Size: 5.9 MB (5870144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6fdf5dc8052b24e56cd315505d0c008ec1aedadf4826d83b7c970cea8c887a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038bfb23519c0926ece84c8e7e5d34e03f7a0722a552518de0ddb674adb4806`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514425d814a52dd1a55dd2a61bceb51b7700a3e740c02b0abffd877c7dfef55d`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f9d7551799d2a32fab62c45954fd3d568fa4f52ad0dabe4670e12c857e87a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:5762142a7f15bd3e97dda219ec3985997c351ce00b39dbfc9a771e735ecdce49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:aa92b18c4aaa8b4a86b817c76c7879136117bb5f6e506cd57b2b407612ce8ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da025743137b99ca37782c7c65b87197d643ecdd42e7210da78e20f218769df7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:17:52 GMT
RUN cmd /S /C #(nop) COPY file:8e415274f0a16ec3fa03a87478f007a6a8ede142612bbcd4aa265fef9c8611e4 in C:\nats-server.exe 
# Thu, 17 Oct 2024 22:17:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6a46f1af9b261dfa3ca4c23edabd47ada1a0c2242f883f8fc4e82d0e08abf`  
		Last Modified: Thu, 10 Oct 2024 00:41:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ede2810b9c7050684298f17d5ea9f7733eac55d920c1a344403c3a47adec223`  
		Last Modified: Thu, 17 Oct 2024 22:18:39 GMT  
		Size: 5.9 MB (5870144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6fdf5dc8052b24e56cd315505d0c008ec1aedadf4826d83b7c970cea8c887a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038bfb23519c0926ece84c8e7e5d34e03f7a0722a552518de0ddb674adb4806`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514425d814a52dd1a55dd2a61bceb51b7700a3e740c02b0abffd877c7dfef55d`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f9d7551799d2a32fab62c45954fd3d568fa4f52ad0dabe4670e12c857e87a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:99d82c006a940560cd7270494d4b072ef2187f60d9b2f96053d3c4a720890e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:cf17ea3e72ac5786933f6830c6f8a1f314ee3227c6d5a43a8208cd2209795d1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa91a8e01e866d6ac77564c2f6479ba33abf92c46beb144f3b21eccbc3da73d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:4e74b2e1e01358cf9fa59c99b10fbb480dcd04043aa01e911cbb369929a58b6d in /nats-server 
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:20:25 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:20:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6f7dfeec586f016d13de8ccc72ee9a4d0266081d746284dd24553679e8f270a`  
		Last Modified: Thu, 17 Oct 2024 21:21:01 GMT  
		Size: 5.7 MB (5748818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b070d5d9d06e85ff9fbf39e87e9d234e69f485f88e1e1e1e9e292793325531`  
		Last Modified: Thu, 17 Oct 2024 21:21:00 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a69426fe3cb56df6a0ee6b3ffa731fed7807b3b7136124726a1e4b87f9a470c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f66e9ff2284e532d8dcdcc0ec25768e152719b68aaa6d29ee1118037fa85f25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 22:17:13 GMT
COPY file:b65e8a9bb5f2b4c735a6f8c122ee2d12894e9117b3eb8415ee37a09eb3dfc8fc in /nats-server 
# Thu, 17 Oct 2024 22:17:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 22:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:14 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 22:17:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:643a17103c442b34df1e96cddbbbe769ef86067423b6949edc6a18c2e37276ba`  
		Last Modified: Thu, 17 Oct 2024 22:17:55 GMT  
		Size: 5.4 MB (5401876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea3faf87f8ffaa4bbacb9d0a81ffd3271e548798e67909dd40052b0bfc7d17`  
		Last Modified: Thu, 17 Oct 2024 22:17:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6069286023d0aa7e507339d8ffb1fd96511f097f722defdde0b4aa8ab4bfbb18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978c140eae43e730d89beb80a0cecdc21d5f0bbc918740ef666ae6ca452fffab`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:41:31 GMT
COPY file:39d7a23794edfcc30c80279af72b7bb8c06fb246cf7ca6c9a42367fcedfd8ad8 in /nats-server 
# Thu, 17 Oct 2024 21:41:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:41:32 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:41:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:837a74f8e729034ff6fc0c30d887028e32b5b1fe59cfb5a4921c7ca9d7625d1e`  
		Last Modified: Thu, 17 Oct 2024 21:42:07 GMT  
		Size: 5.3 MB (5310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66b03fb1668e0ebc0e509084c23d0210d71d0aaa08b9adc6809b50a4f82617`  
		Last Modified: Thu, 17 Oct 2024 21:42:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:9dc6c878ae8689a81e1cb11e7f446214f0eac6afe87d0debc0e0ee5ce81f1133
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695f18f0d73cd9368d192965881be9889ddb8cd16229ffcd059d0445cef412`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:24:33 GMT
COPY file:3d2381b9bf875590f88faa41270a50686e219045e55f00d47f0a3eee4b321bb2 in /nats-server 
# Thu, 17 Oct 2024 21:24:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:24:34 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:24:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:649ac2cb3ceb83f140568686079586cee4e9d5b3f9c34d5c850170a7c4255721`  
		Last Modified: Thu, 17 Oct 2024 21:25:11 GMT  
		Size: 5.3 MB (5279100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65356850f21a24152c66a4e8c3dd9008e2bb460105560be62856e6cc871a3d`  
		Last Modified: Thu, 17 Oct 2024 21:25:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:ecf979b855b9d1f3f6e9958abadfa89125bbba78a418fa725e3746fb2c566118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5602359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253fbe5efbd93d154ad650a47694d0e8b5f4b175dca7a4d3f81ac01f550b9021`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 02:50:14 GMT
COPY file:271e6c0ff401adcd125f2dfef8362ecfc809360856739670b17b3d60e010d872 in /nats-server 
# Fri, 27 Sep 2024 02:50:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 02:50:15 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:15 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 02:50:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c3217868c91b7a4ec1706f93f1d04f3e870c4b7d72d4ed60e3a0f7b9231dcc48`  
		Last Modified: Fri, 27 Sep 2024 02:50:48 GMT  
		Size: 5.6 MB (5601851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a38ff285b474e22578457a2ba0e56f65860a5323d354991b9e438250a392640`  
		Last Modified: Fri, 27 Sep 2024 02:50:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:697ec56703339f66b45f1f84d1d28c50fea6d1913340dc3417f07cb03466d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:143e9e296c13d7a71bfa00b08230709e757e96150a25e8bce3ad72f9538c4d93
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908432251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b77a82bb41c8594376ef53c13cf0fb93896749662022faf0b92f3ff75dc3b18`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 10 Oct 2024 00:38:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Oct 2024 00:38:10 GMT
ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:15:24 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:15:26 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 17 Oct 2024 22:15:28 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 17 Oct 2024 22:16:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 17 Oct 2024 22:17:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 17 Oct 2024 22:17:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196a5b13ab4e3918e43ddd7bbb877dbf52e832257c9ec3eb8019cd414af2e3a`  
		Last Modified: Thu, 10 Oct 2024 00:40:53 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484871eca2e8c738eb04d659975dd4a80e9dae8daf6e59d2297e6c3e81f03bd6`  
		Last Modified: Thu, 10 Oct 2024 00:40:52 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368fa5ecea627e9b785fb5887c6fc61ba24222a0164cff921e705fe2608d154`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475e61a46a9199c2067156908c860a41c2e9745af42c903fb4ef6422082a246`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948095eebb084fb778711564072ea58aea5733478d3b2f451850a8f19705193f`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37e14f1bd78d70c68d454292424b48c3ee9cd02835c28d253c0acaef2e1947`  
		Last Modified: Thu, 17 Oct 2024 22:18:25 GMT  
		Size: 444.4 KB (444352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f75af290818f7d902ec97658a83cd371aed1a0648369ba143d70e628c2c480`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 6.1 MB (6149451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e19f4bee2c3ad99b0a342f55ddab3fad4c6537df793f3d0f2e0c0afbba481b`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1d61f19a1bcb3733a1bdefa6317397344bd1380cbc31ed46f8449ac9ca0710`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cbc0f6dd89bcef1b602c11babb7e58e8383097a287ac1c8e8d079b0c735af9`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22bd1ed76deddbcee8c0032b3760f182c88d86e44473ce346a6796644395b35`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:697ec56703339f66b45f1f84d1d28c50fea6d1913340dc3417f07cb03466d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:143e9e296c13d7a71bfa00b08230709e757e96150a25e8bce3ad72f9538c4d93
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908432251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b77a82bb41c8594376ef53c13cf0fb93896749662022faf0b92f3ff75dc3b18`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 10 Oct 2024 00:38:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Oct 2024 00:38:10 GMT
ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:15:24 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:15:26 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 17 Oct 2024 22:15:28 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 17 Oct 2024 22:16:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 17 Oct 2024 22:17:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 17 Oct 2024 22:17:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196a5b13ab4e3918e43ddd7bbb877dbf52e832257c9ec3eb8019cd414af2e3a`  
		Last Modified: Thu, 10 Oct 2024 00:40:53 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484871eca2e8c738eb04d659975dd4a80e9dae8daf6e59d2297e6c3e81f03bd6`  
		Last Modified: Thu, 10 Oct 2024 00:40:52 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368fa5ecea627e9b785fb5887c6fc61ba24222a0164cff921e705fe2608d154`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475e61a46a9199c2067156908c860a41c2e9745af42c903fb4ef6422082a246`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948095eebb084fb778711564072ea58aea5733478d3b2f451850a8f19705193f`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37e14f1bd78d70c68d454292424b48c3ee9cd02835c28d253c0acaef2e1947`  
		Last Modified: Thu, 17 Oct 2024 22:18:25 GMT  
		Size: 444.4 KB (444352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f75af290818f7d902ec97658a83cd371aed1a0648369ba143d70e628c2c480`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 6.1 MB (6149451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e19f4bee2c3ad99b0a342f55ddab3fad4c6537df793f3d0f2e0c0afbba481b`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1d61f19a1bcb3733a1bdefa6317397344bd1380cbc31ed46f8449ac9ca0710`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cbc0f6dd89bcef1b602c11babb7e58e8383097a287ac1c8e8d079b0c735af9`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22bd1ed76deddbcee8c0032b3760f182c88d86e44473ce346a6796644395b35`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22`

```console
$ docker pull nats@sha256:d44aa37933b0b476d82c5f7fd02dfc21aa4a624878174f6e2edcc989fb545a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10.22` - linux; amd64

```console
$ docker pull nats@sha256:cf17ea3e72ac5786933f6830c6f8a1f314ee3227c6d5a43a8208cd2209795d1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa91a8e01e866d6ac77564c2f6479ba33abf92c46beb144f3b21eccbc3da73d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:4e74b2e1e01358cf9fa59c99b10fbb480dcd04043aa01e911cbb369929a58b6d in /nats-server 
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:20:25 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:20:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6f7dfeec586f016d13de8ccc72ee9a4d0266081d746284dd24553679e8f270a`  
		Last Modified: Thu, 17 Oct 2024 21:21:01 GMT  
		Size: 5.7 MB (5748818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b070d5d9d06e85ff9fbf39e87e9d234e69f485f88e1e1e1e9e292793325531`  
		Last Modified: Thu, 17 Oct 2024 21:21:00 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:a69426fe3cb56df6a0ee6b3ffa731fed7807b3b7136124726a1e4b87f9a470c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f66e9ff2284e532d8dcdcc0ec25768e152719b68aaa6d29ee1118037fa85f25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 22:17:13 GMT
COPY file:b65e8a9bb5f2b4c735a6f8c122ee2d12894e9117b3eb8415ee37a09eb3dfc8fc in /nats-server 
# Thu, 17 Oct 2024 22:17:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 22:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:14 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 22:17:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:643a17103c442b34df1e96cddbbbe769ef86067423b6949edc6a18c2e37276ba`  
		Last Modified: Thu, 17 Oct 2024 22:17:55 GMT  
		Size: 5.4 MB (5401876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea3faf87f8ffaa4bbacb9d0a81ffd3271e548798e67909dd40052b0bfc7d17`  
		Last Modified: Thu, 17 Oct 2024 22:17:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6069286023d0aa7e507339d8ffb1fd96511f097f722defdde0b4aa8ab4bfbb18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978c140eae43e730d89beb80a0cecdc21d5f0bbc918740ef666ae6ca452fffab`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:41:31 GMT
COPY file:39d7a23794edfcc30c80279af72b7bb8c06fb246cf7ca6c9a42367fcedfd8ad8 in /nats-server 
# Thu, 17 Oct 2024 21:41:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:41:32 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:41:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:837a74f8e729034ff6fc0c30d887028e32b5b1fe59cfb5a4921c7ca9d7625d1e`  
		Last Modified: Thu, 17 Oct 2024 21:42:07 GMT  
		Size: 5.3 MB (5310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66b03fb1668e0ebc0e509084c23d0210d71d0aaa08b9adc6809b50a4f82617`  
		Last Modified: Thu, 17 Oct 2024 21:42:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9dc6c878ae8689a81e1cb11e7f446214f0eac6afe87d0debc0e0ee5ce81f1133
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695f18f0d73cd9368d192965881be9889ddb8cd16229ffcd059d0445cef412`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:24:33 GMT
COPY file:3d2381b9bf875590f88faa41270a50686e219045e55f00d47f0a3eee4b321bb2 in /nats-server 
# Thu, 17 Oct 2024 21:24:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:24:34 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:24:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:649ac2cb3ceb83f140568686079586cee4e9d5b3f9c34d5c850170a7c4255721`  
		Last Modified: Thu, 17 Oct 2024 21:25:11 GMT  
		Size: 5.3 MB (5279100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65356850f21a24152c66a4e8c3dd9008e2bb460105560be62856e6cc871a3d`  
		Last Modified: Thu, 17 Oct 2024 21:25:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:aa92b18c4aaa8b4a86b817c76c7879136117bb5f6e506cd57b2b407612ce8ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da025743137b99ca37782c7c65b87197d643ecdd42e7210da78e20f218769df7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:17:52 GMT
RUN cmd /S /C #(nop) COPY file:8e415274f0a16ec3fa03a87478f007a6a8ede142612bbcd4aa265fef9c8611e4 in C:\nats-server.exe 
# Thu, 17 Oct 2024 22:17:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6a46f1af9b261dfa3ca4c23edabd47ada1a0c2242f883f8fc4e82d0e08abf`  
		Last Modified: Thu, 10 Oct 2024 00:41:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ede2810b9c7050684298f17d5ea9f7733eac55d920c1a344403c3a47adec223`  
		Last Modified: Thu, 17 Oct 2024 22:18:39 GMT  
		Size: 5.9 MB (5870144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6fdf5dc8052b24e56cd315505d0c008ec1aedadf4826d83b7c970cea8c887a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038bfb23519c0926ece84c8e7e5d34e03f7a0722a552518de0ddb674adb4806`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514425d814a52dd1a55dd2a61bceb51b7700a3e740c02b0abffd877c7dfef55d`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f9d7551799d2a32fab62c45954fd3d568fa4f52ad0dabe4670e12c857e87a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-alpine`

```console
$ docker pull nats@sha256:84445fae64e542f846bd1ee8b0b70e9c3fe9728a386d15a670f52b2f62355673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `nats:2.10.22-alpine` - linux; amd64

```console
$ docker pull nats@sha256:2bc41d9c0116d148cb34ec27494ad2d4dbc00af9dd75ff4287285d7bf0e4a4b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490e1f605d26f9271d52d5572fcf7daa76c6a2663e53363cb117ffe82b9289a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:20:16 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:20:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:20:19 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:20:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1182bbe83cb5dffc4c5111d0eae24291762eed6c5ad0fcc16f7adb4d5dbf8ce`  
		Last Modified: Thu, 17 Oct 2024 21:20:42 GMT  
		Size: 6.2 MB (6205597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81ba83521b841dc3eebb71f57e30308ccd5cba4e54f2d64cee7c9c95f287ed`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba842ab45501ef1d6a9cfe4cd7da9189a52de3620d0e5927a780e1a984e7858`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:18678ce6c4ee85e8fd7540cefeafdbb6e971a9182cbd281514250088151502d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8957927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bc8e02edcf576a6c0ca36420b4ad0a27ebd7112e82895c407c6fcdb3cf5cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:16:53 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:16:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 22:16:59 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 22:17:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc14a98b7dcabdd1f9abaadd9ba19693909ff74b16a1144dfbd488205aa652fc`  
		Last Modified: Thu, 17 Oct 2024 22:17:35 GMT  
		Size: 5.9 MB (5861447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b2b3b6eb6b1166c6d7b6dd00dd207188510d44a79bbc7aaa6deaca863d788`  
		Last Modified: Thu, 17 Oct 2024 22:17:34 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d271454f5e2e3966cd3722e57f02f67954b117bd4cfbab0e897286ce790b80`  
		Last Modified: Thu, 17 Oct 2024 22:17:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:efbf1e31d1287668e721964813207552a1e1a6cfd9295e6d557c4afad70c0ea8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e226bae4d0988e4f376ccaf3e72c8866a6ac9ee9cb5e992b10ec958897102d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:41:11 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:41:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:41:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:41:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889842c7efddd822dfd25eed95de81301ebf4915452badbd0c8bff2d8a3caa05`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 5.8 MB (5766406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4249e6a2cd5a39fe0c071fba606a912e3f144ad8403d4903b5aa14c389e05bb`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e822ac3e87d68f68a53efeed1ada7eb53d52422cd07e6a5081d0a0f76ac11531`  
		Last Modified: Thu, 17 Oct 2024 21:41:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:dcf714589eecb104d7fa02f8b96d9237e0ed304d4e197f173c1b1a7fa6b84c69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f18d784537de3ada637cd2d7141beff8d6d9f5cf28f891cd4479a973ec21344`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:24:02 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:24:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:24:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:24:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:24:09 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:24:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab23cb4c9e20f29a29e551b5c69af60c62de567048303107fc3e9915f73dda`  
		Last Modified: Thu, 17 Oct 2024 21:24:52 GMT  
		Size: 5.7 MB (5738848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01760873bd1fd3df13327f58577b680a1cc258467c2f5be99814d29a95d5a1`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c59ecf181a23129656d036419f90f28e0f05f75383157f1a587f0baba23dd3`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-alpine3.20`

```console
$ docker pull nats@sha256:84445fae64e542f846bd1ee8b0b70e9c3fe9728a386d15a670f52b2f62355673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `nats:2.10.22-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:2bc41d9c0116d148cb34ec27494ad2d4dbc00af9dd75ff4287285d7bf0e4a4b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490e1f605d26f9271d52d5572fcf7daa76c6a2663e53363cb117ffe82b9289a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:20:16 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:20:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:20:19 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:20:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1182bbe83cb5dffc4c5111d0eae24291762eed6c5ad0fcc16f7adb4d5dbf8ce`  
		Last Modified: Thu, 17 Oct 2024 21:20:42 GMT  
		Size: 6.2 MB (6205597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81ba83521b841dc3eebb71f57e30308ccd5cba4e54f2d64cee7c9c95f287ed`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba842ab45501ef1d6a9cfe4cd7da9189a52de3620d0e5927a780e1a984e7858`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:18678ce6c4ee85e8fd7540cefeafdbb6e971a9182cbd281514250088151502d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8957927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bc8e02edcf576a6c0ca36420b4ad0a27ebd7112e82895c407c6fcdb3cf5cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:16:53 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:16:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 22:16:59 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 22:17:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc14a98b7dcabdd1f9abaadd9ba19693909ff74b16a1144dfbd488205aa652fc`  
		Last Modified: Thu, 17 Oct 2024 22:17:35 GMT  
		Size: 5.9 MB (5861447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b2b3b6eb6b1166c6d7b6dd00dd207188510d44a79bbc7aaa6deaca863d788`  
		Last Modified: Thu, 17 Oct 2024 22:17:34 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d271454f5e2e3966cd3722e57f02f67954b117bd4cfbab0e897286ce790b80`  
		Last Modified: Thu, 17 Oct 2024 22:17:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:efbf1e31d1287668e721964813207552a1e1a6cfd9295e6d557c4afad70c0ea8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e226bae4d0988e4f376ccaf3e72c8866a6ac9ee9cb5e992b10ec958897102d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:41:11 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:41:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:41:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:41:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889842c7efddd822dfd25eed95de81301ebf4915452badbd0c8bff2d8a3caa05`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 5.8 MB (5766406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4249e6a2cd5a39fe0c071fba606a912e3f144ad8403d4903b5aa14c389e05bb`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e822ac3e87d68f68a53efeed1ada7eb53d52422cd07e6a5081d0a0f76ac11531`  
		Last Modified: Thu, 17 Oct 2024 21:41:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:dcf714589eecb104d7fa02f8b96d9237e0ed304d4e197f173c1b1a7fa6b84c69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f18d784537de3ada637cd2d7141beff8d6d9f5cf28f891cd4479a973ec21344`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:24:02 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:24:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:24:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:24:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:24:09 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:24:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab23cb4c9e20f29a29e551b5c69af60c62de567048303107fc3e9915f73dda`  
		Last Modified: Thu, 17 Oct 2024 21:24:52 GMT  
		Size: 5.7 MB (5738848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01760873bd1fd3df13327f58577b680a1cc258467c2f5be99814d29a95d5a1`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c59ecf181a23129656d036419f90f28e0f05f75383157f1a587f0baba23dd3`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-linux`

```console
$ docker pull nats@sha256:0b70d96330f84917daa018a7bc98e11d1f8f3b273195136fa8b9c39f18120b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `nats:2.10.22-linux` - linux; amd64

```console
$ docker pull nats@sha256:cf17ea3e72ac5786933f6830c6f8a1f314ee3227c6d5a43a8208cd2209795d1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa91a8e01e866d6ac77564c2f6479ba33abf92c46beb144f3b21eccbc3da73d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:4e74b2e1e01358cf9fa59c99b10fbb480dcd04043aa01e911cbb369929a58b6d in /nats-server 
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:20:25 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:20:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6f7dfeec586f016d13de8ccc72ee9a4d0266081d746284dd24553679e8f270a`  
		Last Modified: Thu, 17 Oct 2024 21:21:01 GMT  
		Size: 5.7 MB (5748818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b070d5d9d06e85ff9fbf39e87e9d234e69f485f88e1e1e1e9e292793325531`  
		Last Modified: Thu, 17 Oct 2024 21:21:00 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a69426fe3cb56df6a0ee6b3ffa731fed7807b3b7136124726a1e4b87f9a470c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f66e9ff2284e532d8dcdcc0ec25768e152719b68aaa6d29ee1118037fa85f25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 22:17:13 GMT
COPY file:b65e8a9bb5f2b4c735a6f8c122ee2d12894e9117b3eb8415ee37a09eb3dfc8fc in /nats-server 
# Thu, 17 Oct 2024 22:17:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 22:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:14 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 22:17:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:643a17103c442b34df1e96cddbbbe769ef86067423b6949edc6a18c2e37276ba`  
		Last Modified: Thu, 17 Oct 2024 22:17:55 GMT  
		Size: 5.4 MB (5401876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea3faf87f8ffaa4bbacb9d0a81ffd3271e548798e67909dd40052b0bfc7d17`  
		Last Modified: Thu, 17 Oct 2024 22:17:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6069286023d0aa7e507339d8ffb1fd96511f097f722defdde0b4aa8ab4bfbb18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978c140eae43e730d89beb80a0cecdc21d5f0bbc918740ef666ae6ca452fffab`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:41:31 GMT
COPY file:39d7a23794edfcc30c80279af72b7bb8c06fb246cf7ca6c9a42367fcedfd8ad8 in /nats-server 
# Thu, 17 Oct 2024 21:41:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:41:32 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:41:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:837a74f8e729034ff6fc0c30d887028e32b5b1fe59cfb5a4921c7ca9d7625d1e`  
		Last Modified: Thu, 17 Oct 2024 21:42:07 GMT  
		Size: 5.3 MB (5310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66b03fb1668e0ebc0e509084c23d0210d71d0aaa08b9adc6809b50a4f82617`  
		Last Modified: Thu, 17 Oct 2024 21:42:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:9dc6c878ae8689a81e1cb11e7f446214f0eac6afe87d0debc0e0ee5ce81f1133
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695f18f0d73cd9368d192965881be9889ddb8cd16229ffcd059d0445cef412`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:24:33 GMT
COPY file:3d2381b9bf875590f88faa41270a50686e219045e55f00d47f0a3eee4b321bb2 in /nats-server 
# Thu, 17 Oct 2024 21:24:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:24:34 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:24:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:649ac2cb3ceb83f140568686079586cee4e9d5b3f9c34d5c850170a7c4255721`  
		Last Modified: Thu, 17 Oct 2024 21:25:11 GMT  
		Size: 5.3 MB (5279100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65356850f21a24152c66a4e8c3dd9008e2bb460105560be62856e6cc871a3d`  
		Last Modified: Thu, 17 Oct 2024 21:25:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-nanoserver`

```console
$ docker pull nats@sha256:5762142a7f15bd3e97dda219ec3985997c351ce00b39dbfc9a771e735ecdce49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10.22-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:aa92b18c4aaa8b4a86b817c76c7879136117bb5f6e506cd57b2b407612ce8ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da025743137b99ca37782c7c65b87197d643ecdd42e7210da78e20f218769df7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:17:52 GMT
RUN cmd /S /C #(nop) COPY file:8e415274f0a16ec3fa03a87478f007a6a8ede142612bbcd4aa265fef9c8611e4 in C:\nats-server.exe 
# Thu, 17 Oct 2024 22:17:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6a46f1af9b261dfa3ca4c23edabd47ada1a0c2242f883f8fc4e82d0e08abf`  
		Last Modified: Thu, 10 Oct 2024 00:41:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ede2810b9c7050684298f17d5ea9f7733eac55d920c1a344403c3a47adec223`  
		Last Modified: Thu, 17 Oct 2024 22:18:39 GMT  
		Size: 5.9 MB (5870144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6fdf5dc8052b24e56cd315505d0c008ec1aedadf4826d83b7c970cea8c887a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038bfb23519c0926ece84c8e7e5d34e03f7a0722a552518de0ddb674adb4806`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514425d814a52dd1a55dd2a61bceb51b7700a3e740c02b0abffd877c7dfef55d`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f9d7551799d2a32fab62c45954fd3d568fa4f52ad0dabe4670e12c857e87a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-nanoserver-1809`

```console
$ docker pull nats@sha256:5762142a7f15bd3e97dda219ec3985997c351ce00b39dbfc9a771e735ecdce49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10.22-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:aa92b18c4aaa8b4a86b817c76c7879136117bb5f6e506cd57b2b407612ce8ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da025743137b99ca37782c7c65b87197d643ecdd42e7210da78e20f218769df7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:17:52 GMT
RUN cmd /S /C #(nop) COPY file:8e415274f0a16ec3fa03a87478f007a6a8ede142612bbcd4aa265fef9c8611e4 in C:\nats-server.exe 
# Thu, 17 Oct 2024 22:17:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6a46f1af9b261dfa3ca4c23edabd47ada1a0c2242f883f8fc4e82d0e08abf`  
		Last Modified: Thu, 10 Oct 2024 00:41:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ede2810b9c7050684298f17d5ea9f7733eac55d920c1a344403c3a47adec223`  
		Last Modified: Thu, 17 Oct 2024 22:18:39 GMT  
		Size: 5.9 MB (5870144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6fdf5dc8052b24e56cd315505d0c008ec1aedadf4826d83b7c970cea8c887a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038bfb23519c0926ece84c8e7e5d34e03f7a0722a552518de0ddb674adb4806`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514425d814a52dd1a55dd2a61bceb51b7700a3e740c02b0abffd877c7dfef55d`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f9d7551799d2a32fab62c45954fd3d568fa4f52ad0dabe4670e12c857e87a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-scratch`

```console
$ docker pull nats@sha256:0b70d96330f84917daa018a7bc98e11d1f8f3b273195136fa8b9c39f18120b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `nats:2.10.22-scratch` - linux; amd64

```console
$ docker pull nats@sha256:cf17ea3e72ac5786933f6830c6f8a1f314ee3227c6d5a43a8208cd2209795d1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa91a8e01e866d6ac77564c2f6479ba33abf92c46beb144f3b21eccbc3da73d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:4e74b2e1e01358cf9fa59c99b10fbb480dcd04043aa01e911cbb369929a58b6d in /nats-server 
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:20:25 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:20:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6f7dfeec586f016d13de8ccc72ee9a4d0266081d746284dd24553679e8f270a`  
		Last Modified: Thu, 17 Oct 2024 21:21:01 GMT  
		Size: 5.7 MB (5748818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b070d5d9d06e85ff9fbf39e87e9d234e69f485f88e1e1e1e9e292793325531`  
		Last Modified: Thu, 17 Oct 2024 21:21:00 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a69426fe3cb56df6a0ee6b3ffa731fed7807b3b7136124726a1e4b87f9a470c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f66e9ff2284e532d8dcdcc0ec25768e152719b68aaa6d29ee1118037fa85f25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 22:17:13 GMT
COPY file:b65e8a9bb5f2b4c735a6f8c122ee2d12894e9117b3eb8415ee37a09eb3dfc8fc in /nats-server 
# Thu, 17 Oct 2024 22:17:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 22:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:14 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 22:17:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:643a17103c442b34df1e96cddbbbe769ef86067423b6949edc6a18c2e37276ba`  
		Last Modified: Thu, 17 Oct 2024 22:17:55 GMT  
		Size: 5.4 MB (5401876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea3faf87f8ffaa4bbacb9d0a81ffd3271e548798e67909dd40052b0bfc7d17`  
		Last Modified: Thu, 17 Oct 2024 22:17:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6069286023d0aa7e507339d8ffb1fd96511f097f722defdde0b4aa8ab4bfbb18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978c140eae43e730d89beb80a0cecdc21d5f0bbc918740ef666ae6ca452fffab`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:41:31 GMT
COPY file:39d7a23794edfcc30c80279af72b7bb8c06fb246cf7ca6c9a42367fcedfd8ad8 in /nats-server 
# Thu, 17 Oct 2024 21:41:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:41:32 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:41:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:837a74f8e729034ff6fc0c30d887028e32b5b1fe59cfb5a4921c7ca9d7625d1e`  
		Last Modified: Thu, 17 Oct 2024 21:42:07 GMT  
		Size: 5.3 MB (5310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66b03fb1668e0ebc0e509084c23d0210d71d0aaa08b9adc6809b50a4f82617`  
		Last Modified: Thu, 17 Oct 2024 21:42:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:9dc6c878ae8689a81e1cb11e7f446214f0eac6afe87d0debc0e0ee5ce81f1133
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695f18f0d73cd9368d192965881be9889ddb8cd16229ffcd059d0445cef412`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:24:33 GMT
COPY file:3d2381b9bf875590f88faa41270a50686e219045e55f00d47f0a3eee4b321bb2 in /nats-server 
# Thu, 17 Oct 2024 21:24:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:24:34 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:24:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:649ac2cb3ceb83f140568686079586cee4e9d5b3f9c34d5c850170a7c4255721`  
		Last Modified: Thu, 17 Oct 2024 21:25:11 GMT  
		Size: 5.3 MB (5279100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65356850f21a24152c66a4e8c3dd9008e2bb460105560be62856e6cc871a3d`  
		Last Modified: Thu, 17 Oct 2024 21:25:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-windowsservercore`

```console
$ docker pull nats@sha256:697ec56703339f66b45f1f84d1d28c50fea6d1913340dc3417f07cb03466d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10.22-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:143e9e296c13d7a71bfa00b08230709e757e96150a25e8bce3ad72f9538c4d93
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908432251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b77a82bb41c8594376ef53c13cf0fb93896749662022faf0b92f3ff75dc3b18`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 10 Oct 2024 00:38:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Oct 2024 00:38:10 GMT
ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:15:24 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:15:26 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 17 Oct 2024 22:15:28 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 17 Oct 2024 22:16:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 17 Oct 2024 22:17:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 17 Oct 2024 22:17:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196a5b13ab4e3918e43ddd7bbb877dbf52e832257c9ec3eb8019cd414af2e3a`  
		Last Modified: Thu, 10 Oct 2024 00:40:53 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484871eca2e8c738eb04d659975dd4a80e9dae8daf6e59d2297e6c3e81f03bd6`  
		Last Modified: Thu, 10 Oct 2024 00:40:52 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368fa5ecea627e9b785fb5887c6fc61ba24222a0164cff921e705fe2608d154`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475e61a46a9199c2067156908c860a41c2e9745af42c903fb4ef6422082a246`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948095eebb084fb778711564072ea58aea5733478d3b2f451850a8f19705193f`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37e14f1bd78d70c68d454292424b48c3ee9cd02835c28d253c0acaef2e1947`  
		Last Modified: Thu, 17 Oct 2024 22:18:25 GMT  
		Size: 444.4 KB (444352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f75af290818f7d902ec97658a83cd371aed1a0648369ba143d70e628c2c480`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 6.1 MB (6149451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e19f4bee2c3ad99b0a342f55ddab3fad4c6537df793f3d0f2e0c0afbba481b`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1d61f19a1bcb3733a1bdefa6317397344bd1380cbc31ed46f8449ac9ca0710`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cbc0f6dd89bcef1b602c11babb7e58e8383097a287ac1c8e8d079b0c735af9`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22bd1ed76deddbcee8c0032b3760f182c88d86e44473ce346a6796644395b35`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-windowsservercore-1809`

```console
$ docker pull nats@sha256:697ec56703339f66b45f1f84d1d28c50fea6d1913340dc3417f07cb03466d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10.22-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:143e9e296c13d7a71bfa00b08230709e757e96150a25e8bce3ad72f9538c4d93
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908432251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b77a82bb41c8594376ef53c13cf0fb93896749662022faf0b92f3ff75dc3b18`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 10 Oct 2024 00:38:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Oct 2024 00:38:10 GMT
ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:15:24 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:15:26 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 17 Oct 2024 22:15:28 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 17 Oct 2024 22:16:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 17 Oct 2024 22:17:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 17 Oct 2024 22:17:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196a5b13ab4e3918e43ddd7bbb877dbf52e832257c9ec3eb8019cd414af2e3a`  
		Last Modified: Thu, 10 Oct 2024 00:40:53 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484871eca2e8c738eb04d659975dd4a80e9dae8daf6e59d2297e6c3e81f03bd6`  
		Last Modified: Thu, 10 Oct 2024 00:40:52 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368fa5ecea627e9b785fb5887c6fc61ba24222a0164cff921e705fe2608d154`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475e61a46a9199c2067156908c860a41c2e9745af42c903fb4ef6422082a246`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948095eebb084fb778711564072ea58aea5733478d3b2f451850a8f19705193f`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37e14f1bd78d70c68d454292424b48c3ee9cd02835c28d253c0acaef2e1947`  
		Last Modified: Thu, 17 Oct 2024 22:18:25 GMT  
		Size: 444.4 KB (444352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f75af290818f7d902ec97658a83cd371aed1a0648369ba143d70e628c2c480`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 6.1 MB (6149451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e19f4bee2c3ad99b0a342f55ddab3fad4c6537df793f3d0f2e0c0afbba481b`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1d61f19a1bcb3733a1bdefa6317397344bd1380cbc31ed46f8449ac9ca0710`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cbc0f6dd89bcef1b602c11babb7e58e8383097a287ac1c8e8d079b0c735af9`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22bd1ed76deddbcee8c0032b3760f182c88d86e44473ce346a6796644395b35`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:11f9e3db3a0be9938832a5d1368d596ebd4b29fb4d0081faf79c5eca5bc5de1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:2bc41d9c0116d148cb34ec27494ad2d4dbc00af9dd75ff4287285d7bf0e4a4b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490e1f605d26f9271d52d5572fcf7daa76c6a2663e53363cb117ffe82b9289a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:20:16 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:20:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:20:19 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:20:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1182bbe83cb5dffc4c5111d0eae24291762eed6c5ad0fcc16f7adb4d5dbf8ce`  
		Last Modified: Thu, 17 Oct 2024 21:20:42 GMT  
		Size: 6.2 MB (6205597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81ba83521b841dc3eebb71f57e30308ccd5cba4e54f2d64cee7c9c95f287ed`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba842ab45501ef1d6a9cfe4cd7da9189a52de3620d0e5927a780e1a984e7858`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:18678ce6c4ee85e8fd7540cefeafdbb6e971a9182cbd281514250088151502d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8957927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bc8e02edcf576a6c0ca36420b4ad0a27ebd7112e82895c407c6fcdb3cf5cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:16:53 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:16:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 22:16:59 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 22:17:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc14a98b7dcabdd1f9abaadd9ba19693909ff74b16a1144dfbd488205aa652fc`  
		Last Modified: Thu, 17 Oct 2024 22:17:35 GMT  
		Size: 5.9 MB (5861447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b2b3b6eb6b1166c6d7b6dd00dd207188510d44a79bbc7aaa6deaca863d788`  
		Last Modified: Thu, 17 Oct 2024 22:17:34 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d271454f5e2e3966cd3722e57f02f67954b117bd4cfbab0e897286ce790b80`  
		Last Modified: Thu, 17 Oct 2024 22:17:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:efbf1e31d1287668e721964813207552a1e1a6cfd9295e6d557c4afad70c0ea8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e226bae4d0988e4f376ccaf3e72c8866a6ac9ee9cb5e992b10ec958897102d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:41:11 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:41:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:41:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:41:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889842c7efddd822dfd25eed95de81301ebf4915452badbd0c8bff2d8a3caa05`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 5.8 MB (5766406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4249e6a2cd5a39fe0c071fba606a912e3f144ad8403d4903b5aa14c389e05bb`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e822ac3e87d68f68a53efeed1ada7eb53d52422cd07e6a5081d0a0f76ac11531`  
		Last Modified: Thu, 17 Oct 2024 21:41:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:dcf714589eecb104d7fa02f8b96d9237e0ed304d4e197f173c1b1a7fa6b84c69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f18d784537de3ada637cd2d7141beff8d6d9f5cf28f891cd4479a973ec21344`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:24:02 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:24:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:24:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:24:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:24:09 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:24:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab23cb4c9e20f29a29e551b5c69af60c62de567048303107fc3e9915f73dda`  
		Last Modified: Thu, 17 Oct 2024 21:24:52 GMT  
		Size: 5.7 MB (5738848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01760873bd1fd3df13327f58577b680a1cc258467c2f5be99814d29a95d5a1`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c59ecf181a23129656d036419f90f28e0f05f75383157f1a587f0baba23dd3`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:2bad042975a1ddf4b27ae5705c3089b0fb170357a4ea8c1f12aa6a2b755c444d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9524279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69126879c257e7194d41aaa8571bb3e99c20849806570c6d9d3b1c2bc98d9e76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 02:50:03 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 02:50:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 02:50:05 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 02:50:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd523085a6b2d713f6ede8ddb823b69c092def1e9427f762de69b1edf71a92e`  
		Last Modified: Fri, 27 Sep 2024 02:50:35 GMT  
		Size: 6.1 MB (6061706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2a26252ad86d5d3dc0e4608b6ac9ed7efa6021f5484705ee40b27383fa3dc3`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ce1b00925dd2d2eed18086124ddb6332dee23d816b3eebc5282e33b669890c`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.20`

```console
$ docker pull nats@sha256:11f9e3db3a0be9938832a5d1368d596ebd4b29fb4d0081faf79c5eca5bc5de1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:2bc41d9c0116d148cb34ec27494ad2d4dbc00af9dd75ff4287285d7bf0e4a4b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490e1f605d26f9271d52d5572fcf7daa76c6a2663e53363cb117ffe82b9289a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:20:16 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:20:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:20:19 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:20:19 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:20:20 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1182bbe83cb5dffc4c5111d0eae24291762eed6c5ad0fcc16f7adb4d5dbf8ce`  
		Last Modified: Thu, 17 Oct 2024 21:20:42 GMT  
		Size: 6.2 MB (6205597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e81ba83521b841dc3eebb71f57e30308ccd5cba4e54f2d64cee7c9c95f287ed`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba842ab45501ef1d6a9cfe4cd7da9189a52de3620d0e5927a780e1a984e7858`  
		Last Modified: Thu, 17 Oct 2024 21:20:41 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:d530a8ae8e098ff2f2ada79d670a5e380ee7c58d9c28859988dfe3a9aef0e1d3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9234196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38748aa3e85aa2ac3d94c8167763e59374c2d8febf40554a5729971bf8397e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 00:36:48 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 00:36:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 00:36:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 00:36:51 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 00:36:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2041ef437d35857dd600e422222257a10c3a7ef47eff7cdd6c38b277d76e1c98`  
		Last Modified: Fri, 27 Sep 2024 00:37:14 GMT  
		Size: 5.9 MB (5866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a9c82f9973ebc517df96f30dc248ce045ebbea238b73ed0b82a932a88d1a1`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f01161c31497b867842707ef9fea9b5d075204cb1395558757694ea2b2f9569`  
		Last Modified: Fri, 27 Sep 2024 00:37:13 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:18678ce6c4ee85e8fd7540cefeafdbb6e971a9182cbd281514250088151502d9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8957927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089bc8e02edcf576a6c0ca36420b4ad0a27ebd7112e82895c407c6fcdb3cf5cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 22:16:53 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:16:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 22:16:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 22:16:59 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 22:17:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc14a98b7dcabdd1f9abaadd9ba19693909ff74b16a1144dfbd488205aa652fc`  
		Last Modified: Thu, 17 Oct 2024 22:17:35 GMT  
		Size: 5.9 MB (5861447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72b2b3b6eb6b1166c6d7b6dd00dd207188510d44a79bbc7aaa6deaca863d788`  
		Last Modified: Thu, 17 Oct 2024 22:17:34 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d271454f5e2e3966cd3722e57f02f67954b117bd4cfbab0e897286ce790b80`  
		Last Modified: Thu, 17 Oct 2024 22:17:33 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:efbf1e31d1287668e721964813207552a1e1a6cfd9295e6d557c4afad70c0ea8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e226bae4d0988e4f376ccaf3e72c8866a6ac9ee9cb5e992b10ec958897102d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:41:11 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:41:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:41:14 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:41:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:41:14 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889842c7efddd822dfd25eed95de81301ebf4915452badbd0c8bff2d8a3caa05`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 5.8 MB (5766406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4249e6a2cd5a39fe0c071fba606a912e3f144ad8403d4903b5aa14c389e05bb`  
		Last Modified: Thu, 17 Oct 2024 21:41:49 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e822ac3e87d68f68a53efeed1ada7eb53d52422cd07e6a5081d0a0f76ac11531`  
		Last Modified: Thu, 17 Oct 2024 21:41:48 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:dcf714589eecb104d7fa02f8b96d9237e0ed304d4e197f173c1b1a7fa6b84c69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f18d784537de3ada637cd2d7141beff8d6d9f5cf28f891cd4479a973ec21344`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 21:24:02 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 21:24:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 17 Oct 2024 21:24:08 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 17 Oct 2024 21:24:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 17 Oct 2024 21:24:09 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 21:24:11 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab23cb4c9e20f29a29e551b5c69af60c62de567048303107fc3e9915f73dda`  
		Last Modified: Thu, 17 Oct 2024 21:24:52 GMT  
		Size: 5.7 MB (5738848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01760873bd1fd3df13327f58577b680a1cc258467c2f5be99814d29a95d5a1`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c59ecf181a23129656d036419f90f28e0f05f75383157f1a587f0baba23dd3`  
		Last Modified: Thu, 17 Oct 2024 21:24:51 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:2bad042975a1ddf4b27ae5705c3089b0fb170357a4ea8c1f12aa6a2b755c444d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9524279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69126879c257e7194d41aaa8571bb3e99c20849806570c6d9d3b1c2bc98d9e76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 27 Sep 2024 02:50:03 GMT
ENV NATS_SERVER=2.10.21
# Fri, 27 Sep 2024 02:50:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='fe4124d7d8228a005d12a1b4a0f5fe12dfa33a6f99d56ae30a4ef3fe88e11b7e' ;; 		armhf) natsArch='arm6'; sha256='96e8302636733a686e4864d0f59b9feed92f66d88ab12d69146d1db803e3bd31' ;; 		armv7) natsArch='arm7'; sha256='a90b592ccab21ec063b03536298473d8d0399b30a467a8fa16602f30d6616f00' ;; 		x86_64) natsArch='amd64'; sha256='004ddf97c3396511e3e6d356e9bc8760ad9c19e73443fd790a44fbf3ca63bb23' ;; 		x86) natsArch='386'; sha256='053325da8f26554a0991882b9b4827a149bc6d0af2d806b7f618bb8f7581feac' ;; 		s390x) natsArch='s390x'; sha256='b6a39675e8fa0e15431bf0a407adf13225f572027dd608e0e8f88ab3e09c8ebc' ;; 		ppc64le) natsArch='ppc64le'; sha256='08177db78c3b70bd38471605e7acce19ad4f71324160b825e96f8dcd3f84fe2b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 27 Sep 2024 02:50:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Sep 2024 02:50:05 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Sep 2024 02:50:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd523085a6b2d713f6ede8ddb823b69c092def1e9427f762de69b1edf71a92e`  
		Last Modified: Fri, 27 Sep 2024 02:50:35 GMT  
		Size: 6.1 MB (6061706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2a26252ad86d5d3dc0e4608b6ac9ed7efa6021f5484705ee40b27383fa3dc3`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ce1b00925dd2d2eed18086124ddb6332dee23d816b3eebc5282e33b669890c`  
		Last Modified: Fri, 27 Sep 2024 02:50:34 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:22291a43a802939fcfb2f6bacc0895fe3e7a0a911d90089fcb80aa542a7916a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6414; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:cf17ea3e72ac5786933f6830c6f8a1f314ee3227c6d5a43a8208cd2209795d1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa91a8e01e866d6ac77564c2f6479ba33abf92c46beb144f3b21eccbc3da73d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:4e74b2e1e01358cf9fa59c99b10fbb480dcd04043aa01e911cbb369929a58b6d in /nats-server 
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:20:25 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:20:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6f7dfeec586f016d13de8ccc72ee9a4d0266081d746284dd24553679e8f270a`  
		Last Modified: Thu, 17 Oct 2024 21:21:01 GMT  
		Size: 5.7 MB (5748818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b070d5d9d06e85ff9fbf39e87e9d234e69f485f88e1e1e1e9e292793325531`  
		Last Modified: Thu, 17 Oct 2024 21:21:00 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:a69426fe3cb56df6a0ee6b3ffa731fed7807b3b7136124726a1e4b87f9a470c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f66e9ff2284e532d8dcdcc0ec25768e152719b68aaa6d29ee1118037fa85f25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 22:17:13 GMT
COPY file:b65e8a9bb5f2b4c735a6f8c122ee2d12894e9117b3eb8415ee37a09eb3dfc8fc in /nats-server 
# Thu, 17 Oct 2024 22:17:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 22:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:14 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 22:17:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:643a17103c442b34df1e96cddbbbe769ef86067423b6949edc6a18c2e37276ba`  
		Last Modified: Thu, 17 Oct 2024 22:17:55 GMT  
		Size: 5.4 MB (5401876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea3faf87f8ffaa4bbacb9d0a81ffd3271e548798e67909dd40052b0bfc7d17`  
		Last Modified: Thu, 17 Oct 2024 22:17:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6069286023d0aa7e507339d8ffb1fd96511f097f722defdde0b4aa8ab4bfbb18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978c140eae43e730d89beb80a0cecdc21d5f0bbc918740ef666ae6ca452fffab`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:41:31 GMT
COPY file:39d7a23794edfcc30c80279af72b7bb8c06fb246cf7ca6c9a42367fcedfd8ad8 in /nats-server 
# Thu, 17 Oct 2024 21:41:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:41:32 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:41:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:837a74f8e729034ff6fc0c30d887028e32b5b1fe59cfb5a4921c7ca9d7625d1e`  
		Last Modified: Thu, 17 Oct 2024 21:42:07 GMT  
		Size: 5.3 MB (5310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66b03fb1668e0ebc0e509084c23d0210d71d0aaa08b9adc6809b50a4f82617`  
		Last Modified: Thu, 17 Oct 2024 21:42:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:9dc6c878ae8689a81e1cb11e7f446214f0eac6afe87d0debc0e0ee5ce81f1133
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695f18f0d73cd9368d192965881be9889ddb8cd16229ffcd059d0445cef412`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:24:33 GMT
COPY file:3d2381b9bf875590f88faa41270a50686e219045e55f00d47f0a3eee4b321bb2 in /nats-server 
# Thu, 17 Oct 2024 21:24:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:24:34 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:24:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:649ac2cb3ceb83f140568686079586cee4e9d5b3f9c34d5c850170a7c4255721`  
		Last Modified: Thu, 17 Oct 2024 21:25:11 GMT  
		Size: 5.3 MB (5279100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65356850f21a24152c66a4e8c3dd9008e2bb460105560be62856e6cc871a3d`  
		Last Modified: Thu, 17 Oct 2024 21:25:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:ecf979b855b9d1f3f6e9958abadfa89125bbba78a418fa725e3746fb2c566118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5602359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253fbe5efbd93d154ad650a47694d0e8b5f4b175dca7a4d3f81ac01f550b9021`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 02:50:14 GMT
COPY file:271e6c0ff401adcd125f2dfef8362ecfc809360856739670b17b3d60e010d872 in /nats-server 
# Fri, 27 Sep 2024 02:50:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 02:50:15 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:15 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 02:50:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c3217868c91b7a4ec1706f93f1d04f3e870c4b7d72d4ed60e3a0f7b9231dcc48`  
		Last Modified: Fri, 27 Sep 2024 02:50:48 GMT  
		Size: 5.6 MB (5601851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a38ff285b474e22578457a2ba0e56f65860a5323d354991b9e438250a392640`  
		Last Modified: Fri, 27 Sep 2024 02:50:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:aa92b18c4aaa8b4a86b817c76c7879136117bb5f6e506cd57b2b407612ce8ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da025743137b99ca37782c7c65b87197d643ecdd42e7210da78e20f218769df7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:17:52 GMT
RUN cmd /S /C #(nop) COPY file:8e415274f0a16ec3fa03a87478f007a6a8ede142612bbcd4aa265fef9c8611e4 in C:\nats-server.exe 
# Thu, 17 Oct 2024 22:17:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6a46f1af9b261dfa3ca4c23edabd47ada1a0c2242f883f8fc4e82d0e08abf`  
		Last Modified: Thu, 10 Oct 2024 00:41:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ede2810b9c7050684298f17d5ea9f7733eac55d920c1a344403c3a47adec223`  
		Last Modified: Thu, 17 Oct 2024 22:18:39 GMT  
		Size: 5.9 MB (5870144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6fdf5dc8052b24e56cd315505d0c008ec1aedadf4826d83b7c970cea8c887a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038bfb23519c0926ece84c8e7e5d34e03f7a0722a552518de0ddb674adb4806`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514425d814a52dd1a55dd2a61bceb51b7700a3e740c02b0abffd877c7dfef55d`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f9d7551799d2a32fab62c45954fd3d568fa4f52ad0dabe4670e12c857e87a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:99d82c006a940560cd7270494d4b072ef2187f60d9b2f96053d3c4a720890e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:cf17ea3e72ac5786933f6830c6f8a1f314ee3227c6d5a43a8208cd2209795d1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa91a8e01e866d6ac77564c2f6479ba33abf92c46beb144f3b21eccbc3da73d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:4e74b2e1e01358cf9fa59c99b10fbb480dcd04043aa01e911cbb369929a58b6d in /nats-server 
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:20:25 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:20:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6f7dfeec586f016d13de8ccc72ee9a4d0266081d746284dd24553679e8f270a`  
		Last Modified: Thu, 17 Oct 2024 21:21:01 GMT  
		Size: 5.7 MB (5748818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b070d5d9d06e85ff9fbf39e87e9d234e69f485f88e1e1e1e9e292793325531`  
		Last Modified: Thu, 17 Oct 2024 21:21:00 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a69426fe3cb56df6a0ee6b3ffa731fed7807b3b7136124726a1e4b87f9a470c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f66e9ff2284e532d8dcdcc0ec25768e152719b68aaa6d29ee1118037fa85f25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 22:17:13 GMT
COPY file:b65e8a9bb5f2b4c735a6f8c122ee2d12894e9117b3eb8415ee37a09eb3dfc8fc in /nats-server 
# Thu, 17 Oct 2024 22:17:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 22:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:14 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 22:17:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:643a17103c442b34df1e96cddbbbe769ef86067423b6949edc6a18c2e37276ba`  
		Last Modified: Thu, 17 Oct 2024 22:17:55 GMT  
		Size: 5.4 MB (5401876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea3faf87f8ffaa4bbacb9d0a81ffd3271e548798e67909dd40052b0bfc7d17`  
		Last Modified: Thu, 17 Oct 2024 22:17:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6069286023d0aa7e507339d8ffb1fd96511f097f722defdde0b4aa8ab4bfbb18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978c140eae43e730d89beb80a0cecdc21d5f0bbc918740ef666ae6ca452fffab`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:41:31 GMT
COPY file:39d7a23794edfcc30c80279af72b7bb8c06fb246cf7ca6c9a42367fcedfd8ad8 in /nats-server 
# Thu, 17 Oct 2024 21:41:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:41:32 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:41:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:837a74f8e729034ff6fc0c30d887028e32b5b1fe59cfb5a4921c7ca9d7625d1e`  
		Last Modified: Thu, 17 Oct 2024 21:42:07 GMT  
		Size: 5.3 MB (5310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66b03fb1668e0ebc0e509084c23d0210d71d0aaa08b9adc6809b50a4f82617`  
		Last Modified: Thu, 17 Oct 2024 21:42:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:9dc6c878ae8689a81e1cb11e7f446214f0eac6afe87d0debc0e0ee5ce81f1133
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695f18f0d73cd9368d192965881be9889ddb8cd16229ffcd059d0445cef412`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:24:33 GMT
COPY file:3d2381b9bf875590f88faa41270a50686e219045e55f00d47f0a3eee4b321bb2 in /nats-server 
# Thu, 17 Oct 2024 21:24:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:24:34 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:24:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:649ac2cb3ceb83f140568686079586cee4e9d5b3f9c34d5c850170a7c4255721`  
		Last Modified: Thu, 17 Oct 2024 21:25:11 GMT  
		Size: 5.3 MB (5279100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65356850f21a24152c66a4e8c3dd9008e2bb460105560be62856e6cc871a3d`  
		Last Modified: Thu, 17 Oct 2024 21:25:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:ecf979b855b9d1f3f6e9958abadfa89125bbba78a418fa725e3746fb2c566118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5602359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253fbe5efbd93d154ad650a47694d0e8b5f4b175dca7a4d3f81ac01f550b9021`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 02:50:14 GMT
COPY file:271e6c0ff401adcd125f2dfef8362ecfc809360856739670b17b3d60e010d872 in /nats-server 
# Fri, 27 Sep 2024 02:50:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 02:50:15 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:15 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 02:50:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c3217868c91b7a4ec1706f93f1d04f3e870c4b7d72d4ed60e3a0f7b9231dcc48`  
		Last Modified: Fri, 27 Sep 2024 02:50:48 GMT  
		Size: 5.6 MB (5601851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a38ff285b474e22578457a2ba0e56f65860a5323d354991b9e438250a392640`  
		Last Modified: Fri, 27 Sep 2024 02:50:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:5762142a7f15bd3e97dda219ec3985997c351ce00b39dbfc9a771e735ecdce49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:aa92b18c4aaa8b4a86b817c76c7879136117bb5f6e506cd57b2b407612ce8ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da025743137b99ca37782c7c65b87197d643ecdd42e7210da78e20f218769df7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:17:52 GMT
RUN cmd /S /C #(nop) COPY file:8e415274f0a16ec3fa03a87478f007a6a8ede142612bbcd4aa265fef9c8611e4 in C:\nats-server.exe 
# Thu, 17 Oct 2024 22:17:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6a46f1af9b261dfa3ca4c23edabd47ada1a0c2242f883f8fc4e82d0e08abf`  
		Last Modified: Thu, 10 Oct 2024 00:41:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ede2810b9c7050684298f17d5ea9f7733eac55d920c1a344403c3a47adec223`  
		Last Modified: Thu, 17 Oct 2024 22:18:39 GMT  
		Size: 5.9 MB (5870144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6fdf5dc8052b24e56cd315505d0c008ec1aedadf4826d83b7c970cea8c887a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038bfb23519c0926ece84c8e7e5d34e03f7a0722a552518de0ddb674adb4806`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514425d814a52dd1a55dd2a61bceb51b7700a3e740c02b0abffd877c7dfef55d`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f9d7551799d2a32fab62c45954fd3d568fa4f52ad0dabe4670e12c857e87a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:5762142a7f15bd3e97dda219ec3985997c351ce00b39dbfc9a771e735ecdce49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:aa92b18c4aaa8b4a86b817c76c7879136117bb5f6e506cd57b2b407612ce8ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da025743137b99ca37782c7c65b87197d643ecdd42e7210da78e20f218769df7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:17:52 GMT
RUN cmd /S /C #(nop) COPY file:8e415274f0a16ec3fa03a87478f007a6a8ede142612bbcd4aa265fef9c8611e4 in C:\nats-server.exe 
# Thu, 17 Oct 2024 22:17:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:55 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:56 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f6a46f1af9b261dfa3ca4c23edabd47ada1a0c2242f883f8fc4e82d0e08abf`  
		Last Modified: Thu, 10 Oct 2024 00:41:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ede2810b9c7050684298f17d5ea9f7733eac55d920c1a344403c3a47adec223`  
		Last Modified: Thu, 17 Oct 2024 22:18:39 GMT  
		Size: 5.9 MB (5870144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6fdf5dc8052b24e56cd315505d0c008ec1aedadf4826d83b7c970cea8c887a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7038bfb23519c0926ece84c8e7e5d34e03f7a0722a552518de0ddb674adb4806`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514425d814a52dd1a55dd2a61bceb51b7700a3e740c02b0abffd877c7dfef55d`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0f9d7551799d2a32fab62c45954fd3d568fa4f52ad0dabe4670e12c857e87a`  
		Last Modified: Thu, 17 Oct 2024 22:18:38 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:99d82c006a940560cd7270494d4b072ef2187f60d9b2f96053d3c4a720890e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:cf17ea3e72ac5786933f6830c6f8a1f314ee3227c6d5a43a8208cd2209795d1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa91a8e01e866d6ac77564c2f6479ba33abf92c46beb144f3b21eccbc3da73d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 22:17:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:4e74b2e1e01358cf9fa59c99b10fbb480dcd04043aa01e911cbb369929a58b6d in /nats-server 
# Thu, 17 Oct 2024 21:20:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:20:25 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:20:25 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:20:26 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f6f7dfeec586f016d13de8ccc72ee9a4d0266081d746284dd24553679e8f270a`  
		Last Modified: Thu, 17 Oct 2024 21:21:01 GMT  
		Size: 5.7 MB (5748818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b070d5d9d06e85ff9fbf39e87e9d234e69f485f88e1e1e1e9e292793325531`  
		Last Modified: Thu, 17 Oct 2024 21:21:00 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:0d7e46ad16dc880231db76d822c49ce4692d1399715caae2bc5be115a47f70a2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5410818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaa2093955a6ffbad02945c42e85b7fb5aaf3d10c782be6ef7c6b67f2df97f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 27 Sep 2024 00:36:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:c03dbfab86c1af2dc6416490f5e4dbe14e743fcf09a9aa3825f56f4beceaf96d in /nats-server 
# Fri, 27 Sep 2024 00:36:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 00:36:57 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 00:36:58 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 00:36:58 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e5c9215e5cf313e63f1d003288c0faccb73658db733c891f60bbd2341fc6b5cb`  
		Last Modified: Fri, 27 Sep 2024 00:37:33 GMT  
		Size: 5.4 MB (5410310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a345129087ad63af192c153feb511627915df0755828ff3c219107f67c5af12`  
		Last Modified: Fri, 27 Sep 2024 00:37:32 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:a69426fe3cb56df6a0ee6b3ffa731fed7807b3b7136124726a1e4b87f9a470c5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5402384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f66e9ff2284e532d8dcdcc0ec25768e152719b68aaa6d29ee1118037fa85f25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 22:17:13 GMT
COPY file:b65e8a9bb5f2b4c735a6f8c122ee2d12894e9117b3eb8415ee37a09eb3dfc8fc in /nats-server 
# Thu, 17 Oct 2024 22:17:14 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 22:17:14 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:14 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 22:17:14 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:643a17103c442b34df1e96cddbbbe769ef86067423b6949edc6a18c2e37276ba`  
		Last Modified: Thu, 17 Oct 2024 22:17:55 GMT  
		Size: 5.4 MB (5401876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eea3faf87f8ffaa4bbacb9d0a81ffd3271e548798e67909dd40052b0bfc7d17`  
		Last Modified: Thu, 17 Oct 2024 22:17:53 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6069286023d0aa7e507339d8ffb1fd96511f097f722defdde0b4aa8ab4bfbb18
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978c140eae43e730d89beb80a0cecdc21d5f0bbc918740ef666ae6ca452fffab`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:41:31 GMT
COPY file:39d7a23794edfcc30c80279af72b7bb8c06fb246cf7ca6c9a42367fcedfd8ad8 in /nats-server 
# Thu, 17 Oct 2024 21:41:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:41:32 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:41:32 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:41:32 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:837a74f8e729034ff6fc0c30d887028e32b5b1fe59cfb5a4921c7ca9d7625d1e`  
		Last Modified: Thu, 17 Oct 2024 21:42:07 GMT  
		Size: 5.3 MB (5310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c66b03fb1668e0ebc0e509084c23d0210d71d0aaa08b9adc6809b50a4f82617`  
		Last Modified: Thu, 17 Oct 2024 21:42:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:9dc6c878ae8689a81e1cb11e7f446214f0eac6afe87d0debc0e0ee5ce81f1133
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695f18f0d73cd9368d192965881be9889ddb8cd16229ffcd059d0445cef412`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:53:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 21:24:33 GMT
COPY file:3d2381b9bf875590f88faa41270a50686e219045e55f00d47f0a3eee4b321bb2 in /nats-server 
# Thu, 17 Oct 2024 21:24:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 21:24:34 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 21:24:34 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 21:24:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:649ac2cb3ceb83f140568686079586cee4e9d5b3f9c34d5c850170a7c4255721`  
		Last Modified: Thu, 17 Oct 2024 21:25:11 GMT  
		Size: 5.3 MB (5279100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d65356850f21a24152c66a4e8c3dd9008e2bb460105560be62856e6cc871a3d`  
		Last Modified: Thu, 17 Oct 2024 21:25:10 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:ecf979b855b9d1f3f6e9958abadfa89125bbba78a418fa725e3746fb2c566118
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5602359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253fbe5efbd93d154ad650a47694d0e8b5f4b175dca7a4d3f81ac01f550b9021`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 02:50:14 GMT
COPY file:271e6c0ff401adcd125f2dfef8362ecfc809360856739670b17b3d60e010d872 in /nats-server 
# Fri, 27 Sep 2024 02:50:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 02:50:15 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 02:50:15 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 02:50:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c3217868c91b7a4ec1706f93f1d04f3e870c4b7d72d4ed60e3a0f7b9231dcc48`  
		Last Modified: Fri, 27 Sep 2024 02:50:48 GMT  
		Size: 5.6 MB (5601851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a38ff285b474e22578457a2ba0e56f65860a5323d354991b9e438250a392640`  
		Last Modified: Fri, 27 Sep 2024 02:50:47 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:697ec56703339f66b45f1f84d1d28c50fea6d1913340dc3417f07cb03466d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:143e9e296c13d7a71bfa00b08230709e757e96150a25e8bce3ad72f9538c4d93
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908432251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b77a82bb41c8594376ef53c13cf0fb93896749662022faf0b92f3ff75dc3b18`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 10 Oct 2024 00:38:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Oct 2024 00:38:10 GMT
ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:15:24 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:15:26 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 17 Oct 2024 22:15:28 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 17 Oct 2024 22:16:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 17 Oct 2024 22:17:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 17 Oct 2024 22:17:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196a5b13ab4e3918e43ddd7bbb877dbf52e832257c9ec3eb8019cd414af2e3a`  
		Last Modified: Thu, 10 Oct 2024 00:40:53 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484871eca2e8c738eb04d659975dd4a80e9dae8daf6e59d2297e6c3e81f03bd6`  
		Last Modified: Thu, 10 Oct 2024 00:40:52 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368fa5ecea627e9b785fb5887c6fc61ba24222a0164cff921e705fe2608d154`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475e61a46a9199c2067156908c860a41c2e9745af42c903fb4ef6422082a246`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948095eebb084fb778711564072ea58aea5733478d3b2f451850a8f19705193f`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37e14f1bd78d70c68d454292424b48c3ee9cd02835c28d253c0acaef2e1947`  
		Last Modified: Thu, 17 Oct 2024 22:18:25 GMT  
		Size: 444.4 KB (444352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f75af290818f7d902ec97658a83cd371aed1a0648369ba143d70e628c2c480`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 6.1 MB (6149451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e19f4bee2c3ad99b0a342f55ddab3fad4c6537df793f3d0f2e0c0afbba481b`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1d61f19a1bcb3733a1bdefa6317397344bd1380cbc31ed46f8449ac9ca0710`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cbc0f6dd89bcef1b602c11babb7e58e8383097a287ac1c8e8d079b0c735af9`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22bd1ed76deddbcee8c0032b3760f182c88d86e44473ce346a6796644395b35`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:697ec56703339f66b45f1f84d1d28c50fea6d1913340dc3417f07cb03466d039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:143e9e296c13d7a71bfa00b08230709e757e96150a25e8bce3ad72f9538c4d93
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908432251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b77a82bb41c8594376ef53c13cf0fb93896749662022faf0b92f3ff75dc3b18`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 10 Oct 2024 00:38:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 10 Oct 2024 00:38:10 GMT
ENV NATS_DOCKERIZED=1
# Thu, 17 Oct 2024 22:15:24 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 22:15:26 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Thu, 17 Oct 2024 22:15:28 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Thu, 17 Oct 2024 22:16:23 GMT
RUN Set-PSDebug -Trace 2
# Thu, 17 Oct 2024 22:17:36 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 17 Oct 2024 22:17:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 17 Oct 2024 22:17:38 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 22:17:39 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 17 Oct 2024 22:17:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1196a5b13ab4e3918e43ddd7bbb877dbf52e832257c9ec3eb8019cd414af2e3a`  
		Last Modified: Thu, 10 Oct 2024 00:40:53 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484871eca2e8c738eb04d659975dd4a80e9dae8daf6e59d2297e6c3e81f03bd6`  
		Last Modified: Thu, 10 Oct 2024 00:40:52 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0368fa5ecea627e9b785fb5887c6fc61ba24222a0164cff921e705fe2608d154`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9475e61a46a9199c2067156908c860a41c2e9745af42c903fb4ef6422082a246`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948095eebb084fb778711564072ea58aea5733478d3b2f451850a8f19705193f`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd37e14f1bd78d70c68d454292424b48c3ee9cd02835c28d253c0acaef2e1947`  
		Last Modified: Thu, 17 Oct 2024 22:18:25 GMT  
		Size: 444.4 KB (444352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f75af290818f7d902ec97658a83cd371aed1a0648369ba143d70e628c2c480`  
		Last Modified: Thu, 17 Oct 2024 22:18:24 GMT  
		Size: 6.1 MB (6149451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e19f4bee2c3ad99b0a342f55ddab3fad4c6537df793f3d0f2e0c0afbba481b`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1d61f19a1bcb3733a1bdefa6317397344bd1380cbc31ed46f8449ac9ca0710`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cbc0f6dd89bcef1b602c11babb7e58e8383097a287ac1c8e8d079b0c735af9`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22bd1ed76deddbcee8c0032b3760f182c88d86e44473ce346a6796644395b35`  
		Last Modified: Thu, 17 Oct 2024 22:18:22 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
