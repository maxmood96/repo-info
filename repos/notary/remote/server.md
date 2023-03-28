## `notary:server`

```console
$ docker pull notary@sha256:e20fcc2a76a41a553c3de9297a0458b8d013d5485869d45fb6d0d0cd2d5f6eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:server` - linux; amd64

```console
$ docker pull notary@sha256:7eaaeb3126723c072de81b2af359de25ec17617ec5bbbc88acc9f6dc2a47e3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7957067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9358e3fc227aa684cfa31b63fdf32a8a3a627b7191ea5b2e74dfed5d79f9179`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Wed, 08 Mar 2023 00:28:10 GMT
RUN adduser -D -H -g "" notary # buildkit
# Wed, 08 Mar 2023 00:28:10 GMT
EXPOSE map[4443/tcp:{}]
# Wed, 08 Mar 2023 00:28:10 GMT
ENV INSTALLDIR=/notary/server
# Wed, 08 Mar 2023 00:28:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Wed, 08 Mar 2023 00:28:10 GMT
WORKDIR /notary/server
# Wed, 08 Mar 2023 00:28:10 GMT
COPY /notary-server ./ # buildkit
# Wed, 08 Mar 2023 00:28:10 GMT
RUN ./notary-server --version # buildkit
# Wed, 08 Mar 2023 00:28:10 GMT
COPY ./server-config.json . # buildkit
# Wed, 08 Mar 2023 00:28:10 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 08 Mar 2023 00:28:10 GMT
USER notary
# Wed, 08 Mar 2023 00:28:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 08 Mar 2023 00:28:10 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a8bf9348133d1e770b90e9991d3f65c555075470962fb5e1321cf7201947a6`  
		Last Modified: Sat, 11 Feb 2023 10:16:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760faad2c97be8ade88979e95e3256e1d5d0866d3a50a935d789b03b24e6415`  
		Last Modified: Sat, 11 Feb 2023 10:16:23 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2df55172ca943aea44947a07407532c65ec992355ac8f63e2b62af1fc9407da`  
		Last Modified: Wed, 08 Mar 2023 00:49:32 GMT  
		Size: 5.1 MB (5147069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc53564397309052ac64f81f4aaf11752f427caefc737d7144be9a35a37d1bd1`  
		Last Modified: Wed, 08 Mar 2023 00:49:32 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab4a116adb5f5b80fda19935d7ce203ac6d2a495b9b108b064a0922484843cc`  
		Last Modified: Wed, 08 Mar 2023 00:49:32 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41160ed84ebf6a530e72036c3bfed555cd739ed0b93a1a70196f9a1d4d623f53`  
		Last Modified: Wed, 08 Mar 2023 00:49:31 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:23d915b8fc86ba84a47569759c085a1fce986718b48ed6c3798edc7f92865eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c51aedff3c3e5ac57a0ff65372e9ae7a6ea98548e62e4c9354c6ffe2bf1c8f6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:54:37 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 27 Mar 2023 22:54:37 GMT
ENV INSTALLDIR=/notary/server
# Mon, 27 Mar 2023 22:54:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 27 Mar 2023 22:54:37 GMT
WORKDIR /notary/server
# Mon, 27 Mar 2023 22:54:37 GMT
COPY /notary-server ./ # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
RUN ./notary-server --version # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
COPY ./server-config.json . # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:54:37 GMT
USER notary
# Mon, 27 Mar 2023 22:54:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:54:37 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b05793ac14c68387ad3a34fa8d5d4136f040e8b820b1eee3595d30529d87e46`  
		Last Modified: Wed, 08 Mar 2023 00:17:02 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214377c027ebc3bfa8cf5d9c6adfe42cde43421c65fc600f490de087016f240c`  
		Last Modified: Wed, 08 Mar 2023 00:17:00 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3bb2a4e62a65feb82fba8588770b570f54113f46f523b08f7818828fa53331`  
		Last Modified: Tue, 28 Mar 2023 00:20:59 GMT  
		Size: 4.9 MB (4891950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cff8843aea5a062ff464e1104d4cb83972aaa0839fc7d62c2a9775ed52d1fbf`  
		Last Modified: Tue, 28 Mar 2023 00:20:58 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d263be01dcc7d5866ad1c9c9ed1ef5740967e63099e03f6b85a3e1f72749d9e6`  
		Last Modified: Tue, 28 Mar 2023 00:20:58 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd4b4ae5f17d4495c678e86f290ed0dad3c41e9926c582bb4526c43c39e67fd`  
		Last Modified: Tue, 28 Mar 2023 00:20:58 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:f0775d4bbcea47a84310991b768d649959d948dad9cc1a85f131d03bd0964552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d997f7c0e87c3c8696679215af202389165ea2f6e3762e6809275f790748400`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Tue, 07 Mar 2023 23:45:55 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 07 Mar 2023 23:45:55 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 07 Mar 2023 23:45:55 GMT
ENV INSTALLDIR=/notary/server
# Tue, 07 Mar 2023 23:45:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 07 Mar 2023 23:45:55 GMT
WORKDIR /notary/server
# Tue, 07 Mar 2023 23:45:55 GMT
COPY /notary-server ./ # buildkit
# Tue, 07 Mar 2023 23:45:55 GMT
RUN ./notary-server --version # buildkit
# Tue, 07 Mar 2023 23:45:55 GMT
COPY ./server-config.json . # buildkit
# Tue, 07 Mar 2023 23:45:55 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 07 Mar 2023 23:45:55 GMT
USER notary
# Tue, 07 Mar 2023 23:45:55 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 07 Mar 2023 23:45:55 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b9e3dceb52b5f1909f74e5761d8b0968630630d4c5d37134133ff1529d57ca`  
		Last Modified: Sat, 11 Feb 2023 02:02:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9362a2b1100a2d3d12c1fa9941ef61cde36540c7d918725c75f1730eaaed51e`  
		Last Modified: Sat, 11 Feb 2023 02:02:09 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af65511d2d3fd0c0a35b03af44b1d1549f49896f89e6a0c119e7bae191923d5c`  
		Last Modified: Wed, 08 Mar 2023 00:05:41 GMT  
		Size: 4.7 MB (4732808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3fbc8df4b893167b6524a94b784f83d8c9f2ddf16bdab1b646f4b1dcec8b8e`  
		Last Modified: Wed, 08 Mar 2023 00:05:41 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ad95bb804cb93a324515db8c684035512869aa854e7de02a01f1f39828bd52`  
		Last Modified: Wed, 08 Mar 2023 00:05:41 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac29e62b8f7c59b3957f88ba49961df75e4ce160f28a9b39dfef2a05b846322`  
		Last Modified: Wed, 08 Mar 2023 00:05:41 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; 386

```console
$ docker pull notary@sha256:53aa4de3bdba5a5aa16805f5b7b00f59793c8a21030afb10a643a45fc5c360ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfcc7ab0c08a28de8b1f735be0b5ce640ff5a7c8f0bb039d34e38af53f636f9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:29 GMT
ADD file:59ac1f8f33f9b9727892b7e45b33f54ef3c20d9d876c49d6a4c057641821d68f in / 
# Fri, 10 Feb 2023 21:24:29 GMT
CMD ["/bin/sh"]
# Tue, 07 Mar 2023 23:54:04 GMT
RUN adduser -D -H -g "" notary # buildkit
# Tue, 07 Mar 2023 23:54:04 GMT
EXPOSE map[4443/tcp:{}]
# Tue, 07 Mar 2023 23:54:04 GMT
ENV INSTALLDIR=/notary/server
# Tue, 07 Mar 2023 23:54:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 07 Mar 2023 23:54:04 GMT
WORKDIR /notary/server
# Tue, 07 Mar 2023 23:54:04 GMT
COPY /notary-server ./ # buildkit
# Tue, 07 Mar 2023 23:54:04 GMT
RUN ./notary-server --version # buildkit
# Tue, 07 Mar 2023 23:54:04 GMT
COPY ./server-config.json . # buildkit
# Tue, 07 Mar 2023 23:54:04 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 07 Mar 2023 23:54:04 GMT
USER notary
# Tue, 07 Mar 2023 23:54:04 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 07 Mar 2023 23:54:04 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:0987f51cd58a7d03bc7d6ff0a3a0a843c1a3fefcd41e3c8adc3999ddde7441e8`  
		Last Modified: Fri, 10 Feb 2023 21:25:30 GMT  
		Size: 2.8 MB (2810653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a5d52ee7c24d6c22b90002a097b005546a90c2cbe5b10f3899de1861e70fc9`  
		Last Modified: Fri, 24 Mar 2023 05:08:41 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b20e182789380c56462b76096f5ecc4baa970e7bb0835aa8c20ff8b9f7b759`  
		Last Modified: Fri, 24 Mar 2023 05:08:40 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7789392adf8966ad6da923a3f62f8a783c24621406b10b19e793359726e25ac`  
		Last Modified: Fri, 24 Mar 2023 05:08:41 GMT  
		Size: 4.9 MB (4948875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c34f1eab42969100f9cd2f66d024ef078406de2a64c3f284af6e007d6a83ea`  
		Last Modified: Fri, 24 Mar 2023 05:08:40 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4b725f8991bcf28272bfece5e5ddfff71fc952bbeb652e4a5a8e9a9a405d21`  
		Last Modified: Fri, 24 Mar 2023 05:08:40 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694660037e058d5270d86be609852419a1f9c06b9b9223de8c11fd352ff6e628`  
		Last Modified: Fri, 24 Mar 2023 05:08:40 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; ppc64le

```console
$ docker pull notary@sha256:2db26874d36ba99b64f33312719e187dd9980b7328b0aa7543780185eef1675f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74b96c5feff45ae934526e57edab7769bfad0411a9cfe5b74b723371fa48e2b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 09:31:58 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 09:31:58 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 11 Feb 2023 09:31:58 GMT
ENV INSTALLDIR=/notary/server
# Sat, 11 Feb 2023 09:31:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 11 Feb 2023 09:31:58 GMT
WORKDIR /notary/server
# Wed, 08 Mar 2023 00:51:02 GMT
COPY /notary-server ./ # buildkit
# Wed, 08 Mar 2023 00:51:03 GMT
RUN ./notary-server --version # buildkit
# Wed, 08 Mar 2023 00:51:03 GMT
COPY ./server-config.json . # buildkit
# Wed, 08 Mar 2023 00:51:04 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 08 Mar 2023 00:51:04 GMT
USER notary
# Wed, 08 Mar 2023 00:51:04 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 08 Mar 2023 00:51:04 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674d271c42b70a8c82b552b2772787a6cac62d60cdc88c599bd983e06b4b1199`  
		Last Modified: Sat, 11 Feb 2023 09:33:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17b8bc3dd04442591c8af362c063ac63f5cf8890143e98399dcc289f1979b12`  
		Last Modified: Sat, 11 Feb 2023 09:33:08 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db80eee1c1a3a4255721bcde302a3be6a3d5ee5a02ebea316b4345ec5ab5b436`  
		Last Modified: Wed, 08 Mar 2023 00:51:35 GMT  
		Size: 4.6 MB (4637497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cda42b97cb66a057cfa129de14d6c87b4c772de9821c98f5a2dd8f87ec5466`  
		Last Modified: Wed, 08 Mar 2023 00:51:34 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3329ec8c5aec01bef13887ae95dfc28fbe8d3e35c11b095bacc1c37d8ab8231b`  
		Last Modified: Wed, 08 Mar 2023 00:51:34 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0da99db09af96b4eab45370e4f3b5092445f0efd78d2fa60d38dfa23216d4e9`  
		Last Modified: Wed, 08 Mar 2023 00:51:34 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; s390x

```console
$ docker pull notary@sha256:66ce80b97742cc86430993a51cc05ec461c7d6e5f37323f357de15292d1020e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7569941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98fdcb053f0657d56fccb8333c34d9d8fd96bc5b8edf34b16fef0b1ac71ebc5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Mon, 27 Mar 2023 22:43:44 GMT
RUN adduser -D -H -g "" notary # buildkit
# Mon, 27 Mar 2023 22:43:44 GMT
EXPOSE map[4443/tcp:{}]
# Mon, 27 Mar 2023 22:43:44 GMT
ENV INSTALLDIR=/notary/server
# Mon, 27 Mar 2023 22:43:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Mon, 27 Mar 2023 22:43:44 GMT
WORKDIR /notary/server
# Mon, 27 Mar 2023 22:43:44 GMT
COPY /notary-server ./ # buildkit
# Mon, 27 Mar 2023 22:43:44 GMT
RUN ./notary-server --version # buildkit
# Mon, 27 Mar 2023 22:43:44 GMT
COPY ./server-config.json . # buildkit
# Mon, 27 Mar 2023 22:43:44 GMT
COPY ./entrypoint.sh . # buildkit
# Mon, 27 Mar 2023 22:43:44 GMT
USER notary
# Mon, 27 Mar 2023 22:43:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 27 Mar 2023 22:43:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf825008c0747d1db1e6a08e31a5fa2a33c8e0f8a5fe8b2f86af75110c97e790`  
		Last Modified: Sat, 11 Feb 2023 03:39:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdd04f22f8d5c18f264048c202d6471e42bdd87d0431faf250d202652262e4e`  
		Last Modified: Sat, 11 Feb 2023 03:39:14 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69598ff35241064a6aeb26df9e24e2276bbe56c4b25dc3809100063af2c53551`  
		Last Modified: Tue, 28 Mar 2023 00:53:30 GMT  
		Size: 5.0 MB (4974127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd56a70e7bc9848ae4d5d05043f8c35de591b86faa9799498e13b7f0f2a03b2`  
		Last Modified: Tue, 28 Mar 2023 00:53:30 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b7258eb951923ba69743fc3edb22c8b826a14f85b3250bb60ab553234396ae`  
		Last Modified: Tue, 28 Mar 2023 00:53:30 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241b4e70fe6410eb025ecd372906eb62c5cf43f0c8a77504e717dce8decda4e2`  
		Last Modified: Tue, 28 Mar 2023 00:53:30 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
