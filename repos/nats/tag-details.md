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
$ docker pull nats@sha256:1e8a58578fc2bac0291e050ce1125ddddd20993a7ff69338477cf7340cfa5b36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6414; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:7d17934b9fb7919dddde5d9734bd930edbbfaa888620d6034ff2a2a075a70b8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c544065896dd05328d933226b8772214f20ed88a2b0a4204583808512da26b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 23:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:11:49 GMT
COPY file:599deb839bb95a86f12b4d60230bc1be60e32c5dc5c0154d74c0f731cde2308c in /nats-server 
# Thu, 17 Oct 2024 23:11:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:11:50 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:11:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:11:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0f71dd90432a06c2aa03225ae4879e772eac63efb325c3f442d3a919815f5a26`  
		Last Modified: Thu, 17 Oct 2024 23:12:25 GMT  
		Size: 5.4 MB (5413988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e837e0c9c42392b060a853eb45ab66a14a4abc81b16f2259170ce50b972d98`  
		Last Modified: Thu, 17 Oct 2024 23:12:24 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:e805751ca6ac0b7b844c1b19147bad2dd6cb0b55a7a6dd0c243abc0aeebbcc4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4de73388ec3d9260d0465732011f4f035ce8d6340e271aa5465ab5743414f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:ab282700f0edfa4479ed811aff6c658546f5e54ba267d9711f026e2912c31944 in /nats-server 
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:19:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:19:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:19:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:368952e49973696488b28bf26bc5d9f9606e8c12c9fec5e098f0f756d0b24a0b`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 5.6 MB (5603672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64732d91efb14caeeef19ab3e61ec01753b0095d2f291ea6f9b9816e42525e66`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d23003b22072b07cea7c57403d30519c9974445420181d8e174fbfa45fa533ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0b23cf06fe3a7a78cbf9050f6de38b3cbd86fd9eadd9aa0b576d10af31480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaa26dccaea10b5b83d01ed56f7a196c902179c89f7b031693a66884d17aef`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 5.7 MB (5738932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd34510b2845266284f593caae986bea90464fb438d79811c16c21afc268db9`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb0025099f5180f9671beb5f58c8b9fb8950f5971472ca2aded6d8c086dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:03:02 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6ff0dd9b59f440e98ec6d6043cae3c81909695d9cf72e4f75ee2729e8104db86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e08b6ff60c9977edbbe63a98b79f532617da8c1b3435d620244dd54347bea`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a5a969359fee4a9f6bfec8cf77271b3a9243079c36ba7fbda1fadd5e0130c`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.20`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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

### `nats:2-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:d23003b22072b07cea7c57403d30519c9974445420181d8e174fbfa45fa533ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0b23cf06fe3a7a78cbf9050f6de38b3cbd86fd9eadd9aa0b576d10af31480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaa26dccaea10b5b83d01ed56f7a196c902179c89f7b031693a66884d17aef`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 5.7 MB (5738932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd34510b2845266284f593caae986bea90464fb438d79811c16c21afc268db9`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb0025099f5180f9671beb5f58c8b9fb8950f5971472ca2aded6d8c086dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:03:02 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:6ff0dd9b59f440e98ec6d6043cae3c81909695d9cf72e4f75ee2729e8104db86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e08b6ff60c9977edbbe63a98b79f532617da8c1b3435d620244dd54347bea`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a5a969359fee4a9f6bfec8cf77271b3a9243079c36ba7fbda1fadd5e0130c`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:51c31ef2cf7a5448096d592bce29506e9282f565a40d83e22b359a723d30866f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7d17934b9fb7919dddde5d9734bd930edbbfaa888620d6034ff2a2a075a70b8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c544065896dd05328d933226b8772214f20ed88a2b0a4204583808512da26b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 23:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:11:49 GMT
COPY file:599deb839bb95a86f12b4d60230bc1be60e32c5dc5c0154d74c0f731cde2308c in /nats-server 
# Thu, 17 Oct 2024 23:11:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:11:50 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:11:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:11:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0f71dd90432a06c2aa03225ae4879e772eac63efb325c3f442d3a919815f5a26`  
		Last Modified: Thu, 17 Oct 2024 23:12:25 GMT  
		Size: 5.4 MB (5413988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e837e0c9c42392b060a853eb45ab66a14a4abc81b16f2259170ce50b972d98`  
		Last Modified: Thu, 17 Oct 2024 23:12:24 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:e805751ca6ac0b7b844c1b19147bad2dd6cb0b55a7a6dd0c243abc0aeebbcc4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4de73388ec3d9260d0465732011f4f035ce8d6340e271aa5465ab5743414f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:ab282700f0edfa4479ed811aff6c658546f5e54ba267d9711f026e2912c31944 in /nats-server 
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:19:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:19:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:19:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:368952e49973696488b28bf26bc5d9f9606e8c12c9fec5e098f0f756d0b24a0b`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 5.6 MB (5603672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64732d91efb14caeeef19ab3e61ec01753b0095d2f291ea6f9b9816e42525e66`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:51c31ef2cf7a5448096d592bce29506e9282f565a40d83e22b359a723d30866f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7d17934b9fb7919dddde5d9734bd930edbbfaa888620d6034ff2a2a075a70b8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c544065896dd05328d933226b8772214f20ed88a2b0a4204583808512da26b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 23:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:11:49 GMT
COPY file:599deb839bb95a86f12b4d60230bc1be60e32c5dc5c0154d74c0f731cde2308c in /nats-server 
# Thu, 17 Oct 2024 23:11:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:11:50 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:11:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:11:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0f71dd90432a06c2aa03225ae4879e772eac63efb325c3f442d3a919815f5a26`  
		Last Modified: Thu, 17 Oct 2024 23:12:25 GMT  
		Size: 5.4 MB (5413988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e837e0c9c42392b060a853eb45ab66a14a4abc81b16f2259170ce50b972d98`  
		Last Modified: Thu, 17 Oct 2024 23:12:24 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:e805751ca6ac0b7b844c1b19147bad2dd6cb0b55a7a6dd0c243abc0aeebbcc4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4de73388ec3d9260d0465732011f4f035ce8d6340e271aa5465ab5743414f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:ab282700f0edfa4479ed811aff6c658546f5e54ba267d9711f026e2912c31944 in /nats-server 
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:19:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:19:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:19:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:368952e49973696488b28bf26bc5d9f9606e8c12c9fec5e098f0f756d0b24a0b`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 5.6 MB (5603672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64732d91efb14caeeef19ab3e61ec01753b0095d2f291ea6f9b9816e42525e66`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:ab78e2172e61085ae9afc4925e54a987a6d679c9da46d25c484bccf5269d16cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:9448640f937b2f4ee4da3d9937c09b47019f037d5c9e61162580a7d561ce019b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908560921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07a345182b93fdfa8288b594f93c71bc993ca4566321461fecbccf9b0fbbaa2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 12 Nov 2024 00:55:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Nov 2024 00:55:07 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER=2.10.22
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Tue, 12 Nov 2024 00:55:09 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Tue, 12 Nov 2024 00:56:31 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Nov 2024 00:56:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Nov 2024 00:56:57 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 00:56:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 00:56:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 00:56:59 GMT
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
	-	`sha256:58ed0f15243f28f3922f00ed16ecfd22d610f79e0e0daf969dcdf0305ee22ec2`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525058aca77fecf4a52d3e5639a8cd7a8b045d1d0bea041de779ac8d8de030de`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d097959e3c6dc4700daf17b4454b636a4c282eceb830d2d505abf9f1251f1b`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1199e5b06310464b9e94c92b4e883c9f6a5e9e1d24e67bf6415a19de08cdc4f`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c315d41fb2fb62d04f1dea32b9c14e351ba070df978fb722d8307a7fc728a3`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d262f864554f378348b8cbf71b9bc91e6871d9397b4238cde655fb93a78e9c`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 493.1 KB (493088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335838a75c168178d65d906d3c3f5b69f20896629cd5b8aa314087add21137a`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 6.2 MB (6230344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b52fdabfa3405a6f81753210b18cb9389020984bfaf4eb657f2d31d772e5af`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494d7679741aeba6e3aca4377b6c2aaa8ad88fc86ef6a81f4cbe969a23d450c9`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4650fb4eadfc488ae6b5d6bcb5272870243a44e7f3bb7e6884d5cc8cff303cf7`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784c12c0d16c854801762a89df692d823cfc1dcc0579f4458a11171e6f8b17a4`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:ab78e2172e61085ae9afc4925e54a987a6d679c9da46d25c484bccf5269d16cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:9448640f937b2f4ee4da3d9937c09b47019f037d5c9e61162580a7d561ce019b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908560921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07a345182b93fdfa8288b594f93c71bc993ca4566321461fecbccf9b0fbbaa2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 12 Nov 2024 00:55:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Nov 2024 00:55:07 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER=2.10.22
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Tue, 12 Nov 2024 00:55:09 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Tue, 12 Nov 2024 00:56:31 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Nov 2024 00:56:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Nov 2024 00:56:57 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 00:56:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 00:56:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 00:56:59 GMT
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
	-	`sha256:58ed0f15243f28f3922f00ed16ecfd22d610f79e0e0daf969dcdf0305ee22ec2`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525058aca77fecf4a52d3e5639a8cd7a8b045d1d0bea041de779ac8d8de030de`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d097959e3c6dc4700daf17b4454b636a4c282eceb830d2d505abf9f1251f1b`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1199e5b06310464b9e94c92b4e883c9f6a5e9e1d24e67bf6415a19de08cdc4f`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c315d41fb2fb62d04f1dea32b9c14e351ba070df978fb722d8307a7fc728a3`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d262f864554f378348b8cbf71b9bc91e6871d9397b4238cde655fb93a78e9c`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 493.1 KB (493088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335838a75c168178d65d906d3c3f5b69f20896629cd5b8aa314087add21137a`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 6.2 MB (6230344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b52fdabfa3405a6f81753210b18cb9389020984bfaf4eb657f2d31d772e5af`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494d7679741aeba6e3aca4377b6c2aaa8ad88fc86ef6a81f4cbe969a23d450c9`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4650fb4eadfc488ae6b5d6bcb5272870243a44e7f3bb7e6884d5cc8cff303cf7`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784c12c0d16c854801762a89df692d823cfc1dcc0579f4458a11171e6f8b17a4`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:1e8a58578fc2bac0291e050ce1125ddddd20993a7ff69338477cf7340cfa5b36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:7d17934b9fb7919dddde5d9734bd930edbbfaa888620d6034ff2a2a075a70b8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c544065896dd05328d933226b8772214f20ed88a2b0a4204583808512da26b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 23:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:11:49 GMT
COPY file:599deb839bb95a86f12b4d60230bc1be60e32c5dc5c0154d74c0f731cde2308c in /nats-server 
# Thu, 17 Oct 2024 23:11:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:11:50 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:11:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:11:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0f71dd90432a06c2aa03225ae4879e772eac63efb325c3f442d3a919815f5a26`  
		Last Modified: Thu, 17 Oct 2024 23:12:25 GMT  
		Size: 5.4 MB (5413988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e837e0c9c42392b060a853eb45ab66a14a4abc81b16f2259170ce50b972d98`  
		Last Modified: Thu, 17 Oct 2024 23:12:24 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:e805751ca6ac0b7b844c1b19147bad2dd6cb0b55a7a6dd0c243abc0aeebbcc4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4de73388ec3d9260d0465732011f4f035ce8d6340e271aa5465ab5743414f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:ab282700f0edfa4479ed811aff6c658546f5e54ba267d9711f026e2912c31944 in /nats-server 
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:19:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:19:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:19:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:368952e49973696488b28bf26bc5d9f9606e8c12c9fec5e098f0f756d0b24a0b`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 5.6 MB (5603672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64732d91efb14caeeef19ab3e61ec01753b0095d2f291ea6f9b9816e42525e66`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d23003b22072b07cea7c57403d30519c9974445420181d8e174fbfa45fa533ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0b23cf06fe3a7a78cbf9050f6de38b3cbd86fd9eadd9aa0b576d10af31480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaa26dccaea10b5b83d01ed56f7a196c902179c89f7b031693a66884d17aef`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 5.7 MB (5738932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd34510b2845266284f593caae986bea90464fb438d79811c16c21afc268db9`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb0025099f5180f9671beb5f58c8b9fb8950f5971472ca2aded6d8c086dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:03:02 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6ff0dd9b59f440e98ec6d6043cae3c81909695d9cf72e4f75ee2729e8104db86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e08b6ff60c9977edbbe63a98b79f532617da8c1b3435d620244dd54347bea`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a5a969359fee4a9f6bfec8cf77271b3a9243079c36ba7fbda1fadd5e0130c`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.20`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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

### `nats:2.10-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:d23003b22072b07cea7c57403d30519c9974445420181d8e174fbfa45fa533ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0b23cf06fe3a7a78cbf9050f6de38b3cbd86fd9eadd9aa0b576d10af31480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaa26dccaea10b5b83d01ed56f7a196c902179c89f7b031693a66884d17aef`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 5.7 MB (5738932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd34510b2845266284f593caae986bea90464fb438d79811c16c21afc268db9`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb0025099f5180f9671beb5f58c8b9fb8950f5971472ca2aded6d8c086dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:03:02 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:6ff0dd9b59f440e98ec6d6043cae3c81909695d9cf72e4f75ee2729e8104db86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e08b6ff60c9977edbbe63a98b79f532617da8c1b3435d620244dd54347bea`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a5a969359fee4a9f6bfec8cf77271b3a9243079c36ba7fbda1fadd5e0130c`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:51c31ef2cf7a5448096d592bce29506e9282f565a40d83e22b359a723d30866f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7d17934b9fb7919dddde5d9734bd930edbbfaa888620d6034ff2a2a075a70b8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c544065896dd05328d933226b8772214f20ed88a2b0a4204583808512da26b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 23:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:11:49 GMT
COPY file:599deb839bb95a86f12b4d60230bc1be60e32c5dc5c0154d74c0f731cde2308c in /nats-server 
# Thu, 17 Oct 2024 23:11:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:11:50 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:11:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:11:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0f71dd90432a06c2aa03225ae4879e772eac63efb325c3f442d3a919815f5a26`  
		Last Modified: Thu, 17 Oct 2024 23:12:25 GMT  
		Size: 5.4 MB (5413988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e837e0c9c42392b060a853eb45ab66a14a4abc81b16f2259170ce50b972d98`  
		Last Modified: Thu, 17 Oct 2024 23:12:24 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:e805751ca6ac0b7b844c1b19147bad2dd6cb0b55a7a6dd0c243abc0aeebbcc4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4de73388ec3d9260d0465732011f4f035ce8d6340e271aa5465ab5743414f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:ab282700f0edfa4479ed811aff6c658546f5e54ba267d9711f026e2912c31944 in /nats-server 
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:19:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:19:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:19:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:368952e49973696488b28bf26bc5d9f9606e8c12c9fec5e098f0f756d0b24a0b`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 5.6 MB (5603672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64732d91efb14caeeef19ab3e61ec01753b0095d2f291ea6f9b9816e42525e66`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-1809`

```console
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:51c31ef2cf7a5448096d592bce29506e9282f565a40d83e22b359a723d30866f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7d17934b9fb7919dddde5d9734bd930edbbfaa888620d6034ff2a2a075a70b8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c544065896dd05328d933226b8772214f20ed88a2b0a4204583808512da26b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 23:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:11:49 GMT
COPY file:599deb839bb95a86f12b4d60230bc1be60e32c5dc5c0154d74c0f731cde2308c in /nats-server 
# Thu, 17 Oct 2024 23:11:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:11:50 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:11:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:11:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0f71dd90432a06c2aa03225ae4879e772eac63efb325c3f442d3a919815f5a26`  
		Last Modified: Thu, 17 Oct 2024 23:12:25 GMT  
		Size: 5.4 MB (5413988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e837e0c9c42392b060a853eb45ab66a14a4abc81b16f2259170ce50b972d98`  
		Last Modified: Thu, 17 Oct 2024 23:12:24 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:e805751ca6ac0b7b844c1b19147bad2dd6cb0b55a7a6dd0c243abc0aeebbcc4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4de73388ec3d9260d0465732011f4f035ce8d6340e271aa5465ab5743414f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:ab282700f0edfa4479ed811aff6c658546f5e54ba267d9711f026e2912c31944 in /nats-server 
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:19:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:19:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:19:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:368952e49973696488b28bf26bc5d9f9606e8c12c9fec5e098f0f756d0b24a0b`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 5.6 MB (5603672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64732d91efb14caeeef19ab3e61ec01753b0095d2f291ea6f9b9816e42525e66`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:ab78e2172e61085ae9afc4925e54a987a6d679c9da46d25c484bccf5269d16cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:9448640f937b2f4ee4da3d9937c09b47019f037d5c9e61162580a7d561ce019b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908560921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07a345182b93fdfa8288b594f93c71bc993ca4566321461fecbccf9b0fbbaa2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 12 Nov 2024 00:55:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Nov 2024 00:55:07 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER=2.10.22
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Tue, 12 Nov 2024 00:55:09 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Tue, 12 Nov 2024 00:56:31 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Nov 2024 00:56:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Nov 2024 00:56:57 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 00:56:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 00:56:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 00:56:59 GMT
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
	-	`sha256:58ed0f15243f28f3922f00ed16ecfd22d610f79e0e0daf969dcdf0305ee22ec2`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525058aca77fecf4a52d3e5639a8cd7a8b045d1d0bea041de779ac8d8de030de`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d097959e3c6dc4700daf17b4454b636a4c282eceb830d2d505abf9f1251f1b`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1199e5b06310464b9e94c92b4e883c9f6a5e9e1d24e67bf6415a19de08cdc4f`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c315d41fb2fb62d04f1dea32b9c14e351ba070df978fb722d8307a7fc728a3`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d262f864554f378348b8cbf71b9bc91e6871d9397b4238cde655fb93a78e9c`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 493.1 KB (493088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335838a75c168178d65d906d3c3f5b69f20896629cd5b8aa314087add21137a`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 6.2 MB (6230344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b52fdabfa3405a6f81753210b18cb9389020984bfaf4eb657f2d31d772e5af`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494d7679741aeba6e3aca4377b6c2aaa8ad88fc86ef6a81f4cbe969a23d450c9`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4650fb4eadfc488ae6b5d6bcb5272870243a44e7f3bb7e6884d5cc8cff303cf7`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784c12c0d16c854801762a89df692d823cfc1dcc0579f4458a11171e6f8b17a4`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-1809`

```console
$ docker pull nats@sha256:ab78e2172e61085ae9afc4925e54a987a6d679c9da46d25c484bccf5269d16cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:9448640f937b2f4ee4da3d9937c09b47019f037d5c9e61162580a7d561ce019b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908560921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07a345182b93fdfa8288b594f93c71bc993ca4566321461fecbccf9b0fbbaa2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 12 Nov 2024 00:55:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Nov 2024 00:55:07 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER=2.10.22
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Tue, 12 Nov 2024 00:55:09 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Tue, 12 Nov 2024 00:56:31 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Nov 2024 00:56:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Nov 2024 00:56:57 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 00:56:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 00:56:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 00:56:59 GMT
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
	-	`sha256:58ed0f15243f28f3922f00ed16ecfd22d610f79e0e0daf969dcdf0305ee22ec2`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525058aca77fecf4a52d3e5639a8cd7a8b045d1d0bea041de779ac8d8de030de`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d097959e3c6dc4700daf17b4454b636a4c282eceb830d2d505abf9f1251f1b`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1199e5b06310464b9e94c92b4e883c9f6a5e9e1d24e67bf6415a19de08cdc4f`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c315d41fb2fb62d04f1dea32b9c14e351ba070df978fb722d8307a7fc728a3`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d262f864554f378348b8cbf71b9bc91e6871d9397b4238cde655fb93a78e9c`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 493.1 KB (493088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335838a75c168178d65d906d3c3f5b69f20896629cd5b8aa314087add21137a`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 6.2 MB (6230344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b52fdabfa3405a6f81753210b18cb9389020984bfaf4eb657f2d31d772e5af`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494d7679741aeba6e3aca4377b6c2aaa8ad88fc86ef6a81f4cbe969a23d450c9`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4650fb4eadfc488ae6b5d6bcb5272870243a44e7f3bb7e6884d5cc8cff303cf7`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784c12c0d16c854801762a89df692d823cfc1dcc0579f4458a11171e6f8b17a4`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22`

```console
$ docker pull nats@sha256:1e8a58578fc2bac0291e050ce1125ddddd20993a7ff69338477cf7340cfa5b36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10.22` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:7d17934b9fb7919dddde5d9734bd930edbbfaa888620d6034ff2a2a075a70b8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c544065896dd05328d933226b8772214f20ed88a2b0a4204583808512da26b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 23:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:11:49 GMT
COPY file:599deb839bb95a86f12b4d60230bc1be60e32c5dc5c0154d74c0f731cde2308c in /nats-server 
# Thu, 17 Oct 2024 23:11:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:11:50 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:11:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:11:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0f71dd90432a06c2aa03225ae4879e772eac63efb325c3f442d3a919815f5a26`  
		Last Modified: Thu, 17 Oct 2024 23:12:25 GMT  
		Size: 5.4 MB (5413988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e837e0c9c42392b060a853eb45ab66a14a4abc81b16f2259170ce50b972d98`  
		Last Modified: Thu, 17 Oct 2024 23:12:24 GMT  
		Size: 507.0 B  
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

### `nats:2.10.22` - linux; s390x

```console
$ docker pull nats@sha256:e805751ca6ac0b7b844c1b19147bad2dd6cb0b55a7a6dd0c243abc0aeebbcc4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4de73388ec3d9260d0465732011f4f035ce8d6340e271aa5465ab5743414f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:ab282700f0edfa4479ed811aff6c658546f5e54ba267d9711f026e2912c31944 in /nats-server 
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:19:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:19:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:19:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:368952e49973696488b28bf26bc5d9f9606e8c12c9fec5e098f0f756d0b24a0b`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 5.6 MB (5603672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64732d91efb14caeeef19ab3e61ec01753b0095d2f291ea6f9b9816e42525e66`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.10.22` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-alpine`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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

### `nats:2.10.22-alpine` - linux; amd64

```console
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d23003b22072b07cea7c57403d30519c9974445420181d8e174fbfa45fa533ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0b23cf06fe3a7a78cbf9050f6de38b3cbd86fd9eadd9aa0b576d10af31480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaa26dccaea10b5b83d01ed56f7a196c902179c89f7b031693a66884d17aef`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 5.7 MB (5738932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd34510b2845266284f593caae986bea90464fb438d79811c16c21afc268db9`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb0025099f5180f9671beb5f58c8b9fb8950f5971472ca2aded6d8c086dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:03:02 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6ff0dd9b59f440e98ec6d6043cae3c81909695d9cf72e4f75ee2729e8104db86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e08b6ff60c9977edbbe63a98b79f532617da8c1b3435d620244dd54347bea`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a5a969359fee4a9f6bfec8cf77271b3a9243079c36ba7fbda1fadd5e0130c`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.22-alpine3.20`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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

### `nats:2.10.22-alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:d23003b22072b07cea7c57403d30519c9974445420181d8e174fbfa45fa533ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0b23cf06fe3a7a78cbf9050f6de38b3cbd86fd9eadd9aa0b576d10af31480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaa26dccaea10b5b83d01ed56f7a196c902179c89f7b031693a66884d17aef`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 5.7 MB (5738932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd34510b2845266284f593caae986bea90464fb438d79811c16c21afc268db9`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb0025099f5180f9671beb5f58c8b9fb8950f5971472ca2aded6d8c086dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:03:02 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:6ff0dd9b59f440e98ec6d6043cae3c81909695d9cf72e4f75ee2729e8104db86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e08b6ff60c9977edbbe63a98b79f532617da8c1b3435d620244dd54347bea`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a5a969359fee4a9f6bfec8cf77271b3a9243079c36ba7fbda1fadd5e0130c`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.22-linux`

```console
$ docker pull nats@sha256:51c31ef2cf7a5448096d592bce29506e9282f565a40d83e22b359a723d30866f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.22-linux` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-linux` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7d17934b9fb7919dddde5d9734bd930edbbfaa888620d6034ff2a2a075a70b8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c544065896dd05328d933226b8772214f20ed88a2b0a4204583808512da26b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 23:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:11:49 GMT
COPY file:599deb839bb95a86f12b4d60230bc1be60e32c5dc5c0154d74c0f731cde2308c in /nats-server 
# Thu, 17 Oct 2024 23:11:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:11:50 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:11:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:11:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0f71dd90432a06c2aa03225ae4879e772eac63efb325c3f442d3a919815f5a26`  
		Last Modified: Thu, 17 Oct 2024 23:12:25 GMT  
		Size: 5.4 MB (5413988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e837e0c9c42392b060a853eb45ab66a14a4abc81b16f2259170ce50b972d98`  
		Last Modified: Thu, 17 Oct 2024 23:12:24 GMT  
		Size: 507.0 B  
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

### `nats:2.10.22-linux` - linux; s390x

```console
$ docker pull nats@sha256:e805751ca6ac0b7b844c1b19147bad2dd6cb0b55a7a6dd0c243abc0aeebbcc4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4de73388ec3d9260d0465732011f4f035ce8d6340e271aa5465ab5743414f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:ab282700f0edfa4479ed811aff6c658546f5e54ba267d9711f026e2912c31944 in /nats-server 
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:19:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:19:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:19:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:368952e49973696488b28bf26bc5d9f9606e8c12c9fec5e098f0f756d0b24a0b`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 5.6 MB (5603672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64732d91efb14caeeef19ab3e61ec01753b0095d2f291ea6f9b9816e42525e66`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-nanoserver`

```console
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10.22-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-nanoserver-1809`

```console
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10.22-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-scratch`

```console
$ docker pull nats@sha256:51c31ef2cf7a5448096d592bce29506e9282f565a40d83e22b359a723d30866f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:2.10.22-scratch` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.22-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.22-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7d17934b9fb7919dddde5d9734bd930edbbfaa888620d6034ff2a2a075a70b8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c544065896dd05328d933226b8772214f20ed88a2b0a4204583808512da26b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 23:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:11:49 GMT
COPY file:599deb839bb95a86f12b4d60230bc1be60e32c5dc5c0154d74c0f731cde2308c in /nats-server 
# Thu, 17 Oct 2024 23:11:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:11:50 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:11:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:11:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0f71dd90432a06c2aa03225ae4879e772eac63efb325c3f442d3a919815f5a26`  
		Last Modified: Thu, 17 Oct 2024 23:12:25 GMT  
		Size: 5.4 MB (5413988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e837e0c9c42392b060a853eb45ab66a14a4abc81b16f2259170ce50b972d98`  
		Last Modified: Thu, 17 Oct 2024 23:12:24 GMT  
		Size: 507.0 B  
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

### `nats:2.10.22-scratch` - linux; s390x

```console
$ docker pull nats@sha256:e805751ca6ac0b7b844c1b19147bad2dd6cb0b55a7a6dd0c243abc0aeebbcc4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4de73388ec3d9260d0465732011f4f035ce8d6340e271aa5465ab5743414f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:ab282700f0edfa4479ed811aff6c658546f5e54ba267d9711f026e2912c31944 in /nats-server 
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:19:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:19:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:19:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:368952e49973696488b28bf26bc5d9f9606e8c12c9fec5e098f0f756d0b24a0b`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 5.6 MB (5603672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64732d91efb14caeeef19ab3e61ec01753b0095d2f291ea6f9b9816e42525e66`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-windowsservercore`

```console
$ docker pull nats@sha256:ab78e2172e61085ae9afc4925e54a987a6d679c9da46d25c484bccf5269d16cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10.22-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:9448640f937b2f4ee4da3d9937c09b47019f037d5c9e61162580a7d561ce019b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908560921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07a345182b93fdfa8288b594f93c71bc993ca4566321461fecbccf9b0fbbaa2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 12 Nov 2024 00:55:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Nov 2024 00:55:07 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER=2.10.22
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Tue, 12 Nov 2024 00:55:09 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Tue, 12 Nov 2024 00:56:31 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Nov 2024 00:56:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Nov 2024 00:56:57 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 00:56:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 00:56:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 00:56:59 GMT
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
	-	`sha256:58ed0f15243f28f3922f00ed16ecfd22d610f79e0e0daf969dcdf0305ee22ec2`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525058aca77fecf4a52d3e5639a8cd7a8b045d1d0bea041de779ac8d8de030de`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d097959e3c6dc4700daf17b4454b636a4c282eceb830d2d505abf9f1251f1b`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1199e5b06310464b9e94c92b4e883c9f6a5e9e1d24e67bf6415a19de08cdc4f`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c315d41fb2fb62d04f1dea32b9c14e351ba070df978fb722d8307a7fc728a3`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d262f864554f378348b8cbf71b9bc91e6871d9397b4238cde655fb93a78e9c`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 493.1 KB (493088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335838a75c168178d65d906d3c3f5b69f20896629cd5b8aa314087add21137a`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 6.2 MB (6230344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b52fdabfa3405a6f81753210b18cb9389020984bfaf4eb657f2d31d772e5af`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494d7679741aeba6e3aca4377b6c2aaa8ad88fc86ef6a81f4cbe969a23d450c9`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4650fb4eadfc488ae6b5d6bcb5272870243a44e7f3bb7e6884d5cc8cff303cf7`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784c12c0d16c854801762a89df692d823cfc1dcc0579f4458a11171e6f8b17a4`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.22-windowsservercore-1809`

```console
$ docker pull nats@sha256:ab78e2172e61085ae9afc4925e54a987a6d679c9da46d25c484bccf5269d16cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:2.10.22-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:9448640f937b2f4ee4da3d9937c09b47019f037d5c9e61162580a7d561ce019b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908560921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07a345182b93fdfa8288b594f93c71bc993ca4566321461fecbccf9b0fbbaa2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 12 Nov 2024 00:55:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Nov 2024 00:55:07 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER=2.10.22
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Tue, 12 Nov 2024 00:55:09 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Tue, 12 Nov 2024 00:56:31 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Nov 2024 00:56:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Nov 2024 00:56:57 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 00:56:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 00:56:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 00:56:59 GMT
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
	-	`sha256:58ed0f15243f28f3922f00ed16ecfd22d610f79e0e0daf969dcdf0305ee22ec2`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525058aca77fecf4a52d3e5639a8cd7a8b045d1d0bea041de779ac8d8de030de`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d097959e3c6dc4700daf17b4454b636a4c282eceb830d2d505abf9f1251f1b`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1199e5b06310464b9e94c92b4e883c9f6a5e9e1d24e67bf6415a19de08cdc4f`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c315d41fb2fb62d04f1dea32b9c14e351ba070df978fb722d8307a7fc728a3`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d262f864554f378348b8cbf71b9bc91e6871d9397b4238cde655fb93a78e9c`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 493.1 KB (493088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335838a75c168178d65d906d3c3f5b69f20896629cd5b8aa314087add21137a`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 6.2 MB (6230344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b52fdabfa3405a6f81753210b18cb9389020984bfaf4eb657f2d31d772e5af`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494d7679741aeba6e3aca4377b6c2aaa8ad88fc86ef6a81f4cbe969a23d450c9`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4650fb4eadfc488ae6b5d6bcb5272870243a44e7f3bb7e6884d5cc8cff303cf7`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784c12c0d16c854801762a89df692d823cfc1dcc0579f4458a11171e6f8b17a4`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d23003b22072b07cea7c57403d30519c9974445420181d8e174fbfa45fa533ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0b23cf06fe3a7a78cbf9050f6de38b3cbd86fd9eadd9aa0b576d10af31480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaa26dccaea10b5b83d01ed56f7a196c902179c89f7b031693a66884d17aef`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 5.7 MB (5738932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd34510b2845266284f593caae986bea90464fb438d79811c16c21afc268db9`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb0025099f5180f9671beb5f58c8b9fb8950f5971472ca2aded6d8c086dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:03:02 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6ff0dd9b59f440e98ec6d6043cae3c81909695d9cf72e4f75ee2729e8104db86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e08b6ff60c9977edbbe63a98b79f532617da8c1b3435d620244dd54347bea`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a5a969359fee4a9f6bfec8cf77271b3a9243079c36ba7fbda1fadd5e0130c`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.20`

```console
$ docker pull nats@sha256:73b0ba5fec5518c5f698597c58d2a3350a2b5ccae43e84c308f8d2da1242deca
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

### `nats:alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:aa536352f09b109b909e8bfbf9859a40601481bb3742ebc7a09cfaf638622407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9830542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede291869d412212887b120efa5c8b7f3b08aefea8f280cd067254c01c2821e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d773e5a5acd4a5185e1795ce442fae0815b4cde8653279c82cb254f75c731910`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 6.2 MB (6205667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae6cea471c207a94e7b03500b522e43c2a3eadd03542e610de9d99ab66afb0`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae68805e7e9a1127a5a8d98e4da64d38cf8b0d9bd426df532b489f42860fd6ea`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:02807cf2f8c136dbf08462f9e4830c0ebe9789135bd35f9dc1b3bed84498f403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7502fcca317f6d32816fbedbe1b62bc47f8c999075143f1668fe57bce064a8`

```dockerfile
```

-	Layers:
	-	`sha256:2d235c7a9ec1b8f79a5b506d4f47baa00cda2f90ab4c8e3e4b95135a10c82667`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:08995147ec70b3d9cf6231fcaf9c5693f13f0f8fd2350e601c621f38b84d6e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9237219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d69a74357f1c0cc0b96cfa8306847367e64f3404a70a674e10549211ca3787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65afc62adacdff0bf527d9f1b6aaf695b5d37e83fe01a9318f61f316f7f181b6`  
		Last Modified: Tue, 12 Nov 2024 02:43:39 GMT  
		Size: 5.9 MB (5869651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e0190e0f471373e9e66c70a2752250ed9e69da363c0bfba42143fede6fdf1`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dbad2f5874fb9d2a78809f1cb2d73967711a343f8a69c0d2feaae390b4b80`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:f9d6d9aa5070fd9051dc1f6b9b181fb2d58de8807e51d6258c1f350ab3b25b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815d234991f683d0c7e6bf47ad52a53158e360aad37d3918ef50be115c7513f7`

```dockerfile
```

-	Layers:
	-	`sha256:4c385d33a858d7f1cd17b4c8542b01b2bbe4b5c9fa4370e858c3e425169b3651`  
		Last Modified: Tue, 12 Nov 2024 02:43:38 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:36d03e7613d05ab6ce1c1817bc4d9720beb6999b2ad53544eb5e3a2516cd1ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad61f6950b1867cb131ac306bfe2a393ccd3dab4507a6325e59c48f2af639b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0594eef92af6aa29d7428599f3b9e122522e0df39967aea2702a1a7354bc793b`  
		Last Modified: Tue, 12 Nov 2024 02:48:30 GMT  
		Size: 5.9 MB (5861556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed14b98308733affe9fe749214fb8643392c322570578c6ddfbe5251a8ca2db`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b57653849bc6f738b0c3a45512d4f5f55ed7cf0466cd66da9978681b3d05bb`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:424c646570a8c538d99567b966badb8922973ba030077c7d9d5adcbba052386c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d834b5f412a01df4f8c691931cc747d1cbfa65438f1dc948e63e145688149d`

```dockerfile
```

-	Layers:
	-	`sha256:ff72db6a7c559ec37ebb7d4eb71dffcb585101245d8ba8d3bdfbccba6d296c9e`  
		Last Modified: Tue, 12 Nov 2024 02:48:29 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a7f055eca1521c7f5a89ba5f3dcbff015d57b7a929f8653829c4e6f84164ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9855266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75531e0cd58e417f674a8e110cb1b6e032052abc49a34eedf099ba501b1d32b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bd95ee62c7b05e1bf51249d821ab5d9c7323b886d6011744c379d852026d7e`  
		Last Modified: Tue, 12 Nov 2024 03:26:08 GMT  
		Size: 5.8 MB (5766572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20828f336b418c422317d432dc54494c2f6f4697807ed67b33b3bf87374d264`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd330508109963791b4e971f393f42a96ffa843f5e1ece34de92c80dd95e5a9`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:22ac145883a598f4b7c32a900872632569da0619343044db5863844cc5058fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c5b2ebe0e5f3de2734ead969830dbff55bda027a2f6102738f18c7b977ce07`

```dockerfile
```

-	Layers:
	-	`sha256:7cbe0336f7559a824c148c9cb1e5ce3cdf8928a832551a22b11df2774e094d57`  
		Last Modified: Tue, 12 Nov 2024 03:26:07 GMT  
		Size: 14.5 KB (14473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:d23003b22072b07cea7c57403d30519c9974445420181d8e174fbfa45fa533ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0b23cf06fe3a7a78cbf9050f6de38b3cbd86fd9eadd9aa0b576d10af31480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaa26dccaea10b5b83d01ed56f7a196c902179c89f7b031693a66884d17aef`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 5.7 MB (5738932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd34510b2845266284f593caae986bea90464fb438d79811c16c21afc268db9`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb0025099f5180f9671beb5f58c8b9fb8950f5971472ca2aded6d8c086dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:03:02 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:6ff0dd9b59f440e98ec6d6043cae3c81909695d9cf72e4f75ee2729e8104db86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e08b6ff60c9977edbbe63a98b79f532617da8c1b3435d620244dd54347bea`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a5a969359fee4a9f6bfec8cf77271b3a9243079c36ba7fbda1fadd5e0130c`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:cda604f86c6f675320fbd53dce9269d1393938cde088c37491afd1b1a4ddb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9526654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8bbb69f923453ac9b983b9d3a9d7e88d1f8c9de5b29ecb82922d0fc8bc99da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24a04eddab32efb185e6d873c262922dce57394b371a3901e3bb19e5f4cdbc`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 6.1 MB (6064072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa499bc6c83adb2be115e61e0c7a9e080e79501dbc174968339ba9e3bfe4a0`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d05fb7412b90c2f9ba0f5842dbb79f53b2bc89fa193ba41fee4a85f0534d04`  
		Last Modified: Tue, 12 Nov 2024 02:57:34 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.20` - unknown; unknown

```console
$ docker pull nats@sha256:b5f26e32d54b599383af173aa3afe007e7b2342bad2e9ae78ffac68e49a82d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3c81387bfd79dbecbffc981bf9b9658f21b3e9606b7880fcedf1261b9d521`

```dockerfile
```

-	Layers:
	-	`sha256:e2b54010f5848cb09c8db6514ef7b759e9ddfd276bc92657148c8b7422c3d2df`  
		Last Modified: Tue, 12 Nov 2024 02:57:33 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:1e8a58578fc2bac0291e050ce1125ddddd20993a7ff69338477cf7340cfa5b36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.6414; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:7d17934b9fb7919dddde5d9734bd930edbbfaa888620d6034ff2a2a075a70b8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c544065896dd05328d933226b8772214f20ed88a2b0a4204583808512da26b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 23:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:11:49 GMT
COPY file:599deb839bb95a86f12b4d60230bc1be60e32c5dc5c0154d74c0f731cde2308c in /nats-server 
# Thu, 17 Oct 2024 23:11:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:11:50 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:11:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:11:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0f71dd90432a06c2aa03225ae4879e772eac63efb325c3f442d3a919815f5a26`  
		Last Modified: Thu, 17 Oct 2024 23:12:25 GMT  
		Size: 5.4 MB (5413988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e837e0c9c42392b060a853eb45ab66a14a4abc81b16f2259170ce50b972d98`  
		Last Modified: Thu, 17 Oct 2024 23:12:24 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:e805751ca6ac0b7b844c1b19147bad2dd6cb0b55a7a6dd0c243abc0aeebbcc4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4de73388ec3d9260d0465732011f4f035ce8d6340e271aa5465ab5743414f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:ab282700f0edfa4479ed811aff6c658546f5e54ba267d9711f026e2912c31944 in /nats-server 
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:19:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:19:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:19:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:368952e49973696488b28bf26bc5d9f9606e8c12c9fec5e098f0f756d0b24a0b`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 5.6 MB (5603672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64732d91efb14caeeef19ab3e61ec01753b0095d2f291ea6f9b9816e42525e66`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:51c31ef2cf7a5448096d592bce29506e9282f565a40d83e22b359a723d30866f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:7d17934b9fb7919dddde5d9734bd930edbbfaa888620d6034ff2a2a075a70b8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c544065896dd05328d933226b8772214f20ed88a2b0a4204583808512da26b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 23:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:11:49 GMT
COPY file:599deb839bb95a86f12b4d60230bc1be60e32c5dc5c0154d74c0f731cde2308c in /nats-server 
# Thu, 17 Oct 2024 23:11:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:11:50 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:11:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:11:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0f71dd90432a06c2aa03225ae4879e772eac63efb325c3f442d3a919815f5a26`  
		Last Modified: Thu, 17 Oct 2024 23:12:25 GMT  
		Size: 5.4 MB (5413988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e837e0c9c42392b060a853eb45ab66a14a4abc81b16f2259170ce50b972d98`  
		Last Modified: Thu, 17 Oct 2024 23:12:24 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:e805751ca6ac0b7b844c1b19147bad2dd6cb0b55a7a6dd0c243abc0aeebbcc4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4de73388ec3d9260d0465732011f4f035ce8d6340e271aa5465ab5743414f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:ab282700f0edfa4479ed811aff6c658546f5e54ba267d9711f026e2912c31944 in /nats-server 
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:19:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:19:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:19:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:368952e49973696488b28bf26bc5d9f9606e8c12c9fec5e098f0f756d0b24a0b`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 5.6 MB (5603672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64732d91efb14caeeef19ab3e61ec01753b0095d2f291ea6f9b9816e42525e66`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:f8924d81bd9732f82846c91bb856438bd2a35819af18351b3adc9e9d037e2198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:053fd6a67430966b5ef4253d8b1cfc23a311da729a9389d83b3dfd01800e63ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160969543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842d20e36f047cfb078828de10ee4d9abbbd7eebde56d0c84f6d90843adee82a`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Tue, 12 Nov 2024 02:02:48 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 02:02:49 GMT
RUN cmd /S /C #(nop) COPY file:6efa011ff84014d148ada9315a3292149a71c3daa1b536499f2b43a2daee2d50 in C:\nats-server.exe 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 02:02:50 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 02:02:51 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3c2d0f66b6ae0af6bb08b99b128223baab674d525e452e0991867c2a1173b0`  
		Last Modified: Tue, 12 Nov 2024 02:02:57 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ba4c6aafec94bd41860c1d9e8327b73b0ac64c85b1c317350f3df49318178d`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 5.9 MB (5870082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01af1e1e6a4962ecc81604ad1b09ea03a4519d9de02bfd8f36edb94d3f8bef32`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1db4ff41e188b9274e333b99fd768fd30e9023a68547ce0a4f7f910f0e3e88`  
		Last Modified: Tue, 12 Nov 2024 02:02:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c3ee6788b430468c453082a98238ebe894e2beb7699b2dc742b1e842ed0616`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619838cdeb9173ba7f68fc27c3eaf3bbd6cb680b441c766e7f4274f6b25573f6`  
		Last Modified: Tue, 12 Nov 2024 02:02:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:51c31ef2cf7a5448096d592bce29506e9282f565a40d83e22b359a723d30866f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:26b0ee1a95285aedae137aefb953701d9da1dfffcf7818eb3aeb536c4373892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9321c727224d6919153399a2554913ee3ea75615c40faf0b0b61719fd4cba18f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 18:08:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 18:08:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fc7b6eeb42db27589fb02b7af7648621b4230b391664f1cabca731c0cb74c6c0`  
		Last Modified: Thu, 17 Oct 2024 18:09:47 GMT  
		Size: 5.7 MB (5748809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648a1fe081b19052a39d36fde23ff89c48a0b60bddc52cdf58474ed9b7e16ab4`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:92b63acf1eb46cb3ce90a6406fcf9cf3214ba330e4dacef512280529a04870ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd7260fa709b7a3bb731d03f1fc89313f81c37eaacc9a95aef394dde1aa26ae`

```dockerfile
```

-	Layers:
	-	`sha256:eb1f99c4d9cf8c2d861e264c9ba0cdb9161bb70c2764c955ab1f90310af1f472`  
		Last Modified: Tue, 12 Nov 2024 03:05:27 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:7d17934b9fb7919dddde5d9734bd930edbbfaa888620d6034ff2a2a075a70b8d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c544065896dd05328d933226b8772214f20ed88a2b0a4204583808512da26b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 17 Oct 2024 23:11:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:11:49 GMT
COPY file:599deb839bb95a86f12b4d60230bc1be60e32c5dc5c0154d74c0f731cde2308c in /nats-server 
# Thu, 17 Oct 2024 23:11:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:11:50 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:11:50 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:11:50 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0f71dd90432a06c2aa03225ae4879e772eac63efb325c3f442d3a919815f5a26`  
		Last Modified: Thu, 17 Oct 2024 23:12:25 GMT  
		Size: 5.4 MB (5413988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e837e0c9c42392b060a853eb45ab66a14a4abc81b16f2259170ce50b972d98`  
		Last Modified: Thu, 17 Oct 2024 23:12:24 GMT  
		Size: 507.0 B  
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
$ docker pull nats@sha256:e805751ca6ac0b7b844c1b19147bad2dd6cb0b55a7a6dd0c243abc0aeebbcc4b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4de73388ec3d9260d0465732011f4f035ce8d6340e271aa5465ab5743414f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 18:02:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:ab282700f0edfa4479ed811aff6c658546f5e54ba267d9711f026e2912c31944 in /nats-server 
# Thu, 17 Oct 2024 23:19:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 17 Oct 2024 23:19:35 GMT
EXPOSE 4222 6222 8222
# Thu, 17 Oct 2024 23:19:35 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 17 Oct 2024 23:19:35 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:368952e49973696488b28bf26bc5d9f9606e8c12c9fec5e098f0f756d0b24a0b`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 5.6 MB (5603672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64732d91efb14caeeef19ab3e61ec01753b0095d2f291ea6f9b9816e42525e66`  
		Last Modified: Thu, 17 Oct 2024 23:20:18 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:ab78e2172e61085ae9afc4925e54a987a6d679c9da46d25c484bccf5269d16cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:9448640f937b2f4ee4da3d9937c09b47019f037d5c9e61162580a7d561ce019b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908560921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07a345182b93fdfa8288b594f93c71bc993ca4566321461fecbccf9b0fbbaa2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 12 Nov 2024 00:55:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Nov 2024 00:55:07 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER=2.10.22
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Tue, 12 Nov 2024 00:55:09 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Tue, 12 Nov 2024 00:56:31 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Nov 2024 00:56:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Nov 2024 00:56:57 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 00:56:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 00:56:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 00:56:59 GMT
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
	-	`sha256:58ed0f15243f28f3922f00ed16ecfd22d610f79e0e0daf969dcdf0305ee22ec2`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525058aca77fecf4a52d3e5639a8cd7a8b045d1d0bea041de779ac8d8de030de`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d097959e3c6dc4700daf17b4454b636a4c282eceb830d2d505abf9f1251f1b`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1199e5b06310464b9e94c92b4e883c9f6a5e9e1d24e67bf6415a19de08cdc4f`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c315d41fb2fb62d04f1dea32b9c14e351ba070df978fb722d8307a7fc728a3`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d262f864554f378348b8cbf71b9bc91e6871d9397b4238cde655fb93a78e9c`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 493.1 KB (493088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335838a75c168178d65d906d3c3f5b69f20896629cd5b8aa314087add21137a`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 6.2 MB (6230344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b52fdabfa3405a6f81753210b18cb9389020984bfaf4eb657f2d31d772e5af`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494d7679741aeba6e3aca4377b6c2aaa8ad88fc86ef6a81f4cbe969a23d450c9`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4650fb4eadfc488ae6b5d6bcb5272870243a44e7f3bb7e6884d5cc8cff303cf7`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784c12c0d16c854801762a89df692d823cfc1dcc0579f4458a11171e6f8b17a4`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:ab78e2172e61085ae9afc4925e54a987a6d679c9da46d25c484bccf5269d16cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull nats@sha256:9448640f937b2f4ee4da3d9937c09b47019f037d5c9e61162580a7d561ce019b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908560921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07a345182b93fdfa8288b594f93c71bc993ca4566321461fecbccf9b0fbbaa2`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 12 Nov 2024 00:55:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Nov 2024 00:55:07 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER=2.10.22
# Tue, 12 Nov 2024 00:55:08 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.22/nats-server-v2.10.22-windows-amd64.zip
# Tue, 12 Nov 2024 00:55:09 GMT
ENV NATS_SERVER_SHASUM=33c8a0c6feb441ec4c7007e0af9ef2a45356d6809cd08ec4871a3d659fc74e91
# Tue, 12 Nov 2024 00:56:31 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Nov 2024 00:56:57 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Nov 2024 00:56:57 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Nov 2024 00:56:58 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Nov 2024 00:56:58 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Nov 2024 00:56:59 GMT
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
	-	`sha256:58ed0f15243f28f3922f00ed16ecfd22d610f79e0e0daf969dcdf0305ee22ec2`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525058aca77fecf4a52d3e5639a8cd7a8b045d1d0bea041de779ac8d8de030de`  
		Last Modified: Tue, 12 Nov 2024 00:57:03 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d097959e3c6dc4700daf17b4454b636a4c282eceb830d2d505abf9f1251f1b`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1199e5b06310464b9e94c92b4e883c9f6a5e9e1d24e67bf6415a19de08cdc4f`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c315d41fb2fb62d04f1dea32b9c14e351ba070df978fb722d8307a7fc728a3`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d262f864554f378348b8cbf71b9bc91e6871d9397b4238cde655fb93a78e9c`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 493.1 KB (493088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a335838a75c168178d65d906d3c3f5b69f20896629cd5b8aa314087add21137a`  
		Last Modified: Tue, 12 Nov 2024 00:57:02 GMT  
		Size: 6.2 MB (6230344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b52fdabfa3405a6f81753210b18cb9389020984bfaf4eb657f2d31d772e5af`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494d7679741aeba6e3aca4377b6c2aaa8ad88fc86ef6a81f4cbe969a23d450c9`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4650fb4eadfc488ae6b5d6bcb5272870243a44e7f3bb7e6884d5cc8cff303cf7`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:784c12c0d16c854801762a89df692d823cfc1dcc0579f4458a11171e6f8b17a4`  
		Last Modified: Tue, 12 Nov 2024 00:57:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
