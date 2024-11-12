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
