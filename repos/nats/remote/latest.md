## `nats:latest`

```console
$ docker pull nats@sha256:e5add9ab86abeecd959edb7b2ea8573a32db4fc732475b9bad75612fa9aa98c3
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
$ docker pull nats@sha256:b6ea546f1a9d455cf68379a3ac424135c71e84005ac1f90e251eebb43e8d61b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779d728e0809548ae5180c791509a008e5ff27aa960bc1bdc2e97c7d7616236c`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 21 Jun 2024 00:29:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 05:21:33 GMT
COPY file:e5d61edee7cd6c6309dd147dc3287a0f078a06c0731cf46d0c5be4cfec85a189 in /nats-server 
# Fri, 27 Sep 2024 05:21:34 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 05:21:34 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 05:21:34 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 05:21:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:35d3f5c4c780268fff0d8ff0bfe19c94a3493d19a92b4d1d4919e711e76ae9ca`  
		Last Modified: Fri, 27 Sep 2024 05:22:06 GMT  
		Size: 5.4 MB (5400230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6316a346e6538d8ed1e2f8e9aa1ac04f80fdc9c007eb518fd070a565b3d02c49`  
		Last Modified: Fri, 27 Sep 2024 05:22:05 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:6841807bd9388d3f63f1f2c74a58b1a8e706f6d97337593be072dc1c95f5aa9d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5307654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748d2b3035fc8f031ce587db0df49531711e6929cc6fd1fe852bc34919d62fb8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 20 Jun 2024 19:07:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 27 Sep 2024 04:44:47 GMT
COPY file:90ec92f2c97083e8e996654858f1f8e663a2ecd498d5bf4fc1f0989e027cb32a in /nats-server 
# Fri, 27 Sep 2024 04:44:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Fri, 27 Sep 2024 04:44:47 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Sep 2024 04:44:47 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 27 Sep 2024 04:44:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:87792cfc1596a0174fbdf1f99d7e36c6c5ae4ef763543d3057bf72cf31a541c6`  
		Last Modified: Fri, 27 Sep 2024 04:45:21 GMT  
		Size: 5.3 MB (5307146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44efe933c30e0f95f288f90ec2c46fd382b065340a7312f1e15e981681d07176`  
		Last Modified: Fri, 27 Sep 2024 04:45:20 GMT  
		Size: 508.0 B  
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
$ docker pull nats@sha256:3b70aad90245a122f42d068a50ed9c0343ee837ec133777db8bbdab11e4fe34b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160965782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a9089b5b6e51ff693a82c396a4bc899ae7f8ed4e56008ad5fadca9237070c4`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:40:22 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 10 Oct 2024 00:40:24 GMT
RUN cmd /S /C #(nop) COPY file:a1c9a1f2c47ba86596c509adc31752919b1187c6d0031227193f6c0373671753 in C:\nats-server.exe 
# Thu, 10 Oct 2024 00:40:25 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Thu, 10 Oct 2024 00:40:26 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 10 Oct 2024 00:40:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 10 Oct 2024 00:40:27 GMT
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
	-	`sha256:d431fd0db55cfb4c1f6ec594babd961195abb4e75c732e641a278b94216a0638`  
		Last Modified: Thu, 10 Oct 2024 00:41:07 GMT  
		Size: 5.9 MB (5866386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820256ded1f2e0b9e8fe7954e92c2eb76c367dc59a828374683c26ab2c2c5f6f`  
		Last Modified: Thu, 10 Oct 2024 00:41:05 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70291f4c7c17278a69f696f5d2eab88a2b73f01455fda152912ac9d52991c3af`  
		Last Modified: Thu, 10 Oct 2024 00:41:06 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5e745e4b24179d8d461944bbe781e6374c0fa0a4d02a5210d61263b999a71b`  
		Last Modified: Thu, 10 Oct 2024 00:41:05 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b2423a915517c27337bb1589c5a32499e0f355c5612b2792c5654ff11468a3`  
		Last Modified: Thu, 10 Oct 2024 00:41:05 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
