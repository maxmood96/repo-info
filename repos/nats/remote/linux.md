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
