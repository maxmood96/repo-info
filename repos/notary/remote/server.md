## `notary:server`

```console
$ docker pull notary@sha256:712e9515a65e5affef46a54c4fd12a034332ddd468cf63124a80515dab0ac738
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
$ docker pull notary@sha256:a2887b56060c19b51b99b40b9409b74d74f7021619cc23a2804bffc9c6ee8b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7956928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a1e95c6a8d87575db0c7d03fb498d609e65646927c981ca2d4fbede25ac7051`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 10:15:51 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 10:15:51 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 11 Feb 2023 10:15:51 GMT
ENV INSTALLDIR=/notary/server
# Sat, 11 Feb 2023 10:15:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 11 Feb 2023 10:15:51 GMT
WORKDIR /notary/server
# Tue, 14 Feb 2023 19:48:17 GMT
COPY /notary-server ./ # buildkit
# Tue, 14 Feb 2023 19:48:18 GMT
RUN ./notary-server --version # buildkit
# Tue, 14 Feb 2023 19:48:18 GMT
COPY ./server-config.json . # buildkit
# Tue, 14 Feb 2023 19:48:18 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 14 Feb 2023 19:48:18 GMT
USER notary
# Tue, 14 Feb 2023 19:48:18 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 14 Feb 2023 19:48:18 GMT
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
	-	`sha256:487d6846b1a9e0256a3524df73e7c2901a37bed73f9394be3bb4103bbdc4ea8d`  
		Last Modified: Tue, 14 Feb 2023 19:48:35 GMT  
		Size: 5.1 MB (5146934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5402ee7643d3e7e0aea93e7e4806f42ce953744208d5ff7ca7dcdd297949185`  
		Last Modified: Tue, 14 Feb 2023 19:48:35 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534886c3af403f2b17e507238b0d0d2b839c5a2ed15898b60d7f018055f80138`  
		Last Modified: Tue, 14 Feb 2023 19:48:35 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2261f4437115ac983c58411c70ded7acaf077d978d759be2587685853105eed`  
		Last Modified: Tue, 14 Feb 2023 19:48:35 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:993c0fe0ae4eab93f7c5c36b4cbd538a0f92f5fe89a80b9017419df41ca1a1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2814165b9c1e537a7ec425568b01f1b251034848f80aa07c77591dd196d0d020`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 02:32:16 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 02:32:16 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 11 Feb 2023 02:32:16 GMT
ENV INSTALLDIR=/notary/server
# Sat, 11 Feb 2023 02:32:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 11 Feb 2023 02:32:16 GMT
WORKDIR /notary/server
# Tue, 14 Feb 2023 21:24:54 GMT
COPY /notary-server ./ # buildkit
# Tue, 14 Feb 2023 21:24:55 GMT
RUN ./notary-server --version # buildkit
# Tue, 14 Feb 2023 21:24:55 GMT
COPY ./server-config.json . # buildkit
# Tue, 14 Feb 2023 21:24:55 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 14 Feb 2023 21:24:55 GMT
USER notary
# Tue, 14 Feb 2023 21:24:55 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 14 Feb 2023 21:24:55 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e652d0821d7b3cb171424201f4c94165c61ecc2b9f1b6d059c6b18994ffd08`  
		Last Modified: Sat, 11 Feb 2023 02:33:16 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6518db8c658881034639d4f169c4aafa493f3b97ef918f0b182b25e0f48465c6`  
		Last Modified: Sat, 11 Feb 2023 02:33:14 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f666a396e49acc8df91223f123d7e5cb11b2337727e91ccd41b483c169c40f00`  
		Last Modified: Tue, 14 Feb 2023 21:25:30 GMT  
		Size: 4.9 MB (4891954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c477e5fd98889323591af0dbfd81da23b8bf0c5d16bfe3a0b465d7551c92b015`  
		Last Modified: Tue, 14 Feb 2023 21:25:29 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f640809eb6c5ddbb51001a13019a6db7b02958ee814574fdd837620764f343`  
		Last Modified: Tue, 14 Feb 2023 21:25:29 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2fd90df433457d6d2b4263c26b6b1b85df08e6c5b61f4d8e6939dabe6654a75`  
		Last Modified: Tue, 14 Feb 2023 21:25:29 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:477611895e2ae43a1c4ae1232a80f8795a7c55a6f33d938e85406898cc07cc3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f16667c9d87cb3396ff1b9eca79af762bf1911b406e1f83e69913be9d834e66`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 02:01:39 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 02:01:39 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 11 Feb 2023 02:01:39 GMT
ENV INSTALLDIR=/notary/server
# Sat, 11 Feb 2023 02:01:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 11 Feb 2023 02:01:39 GMT
WORKDIR /notary/server
# Tue, 14 Feb 2023 20:05:03 GMT
COPY /notary-server ./ # buildkit
# Tue, 14 Feb 2023 20:05:04 GMT
RUN ./notary-server --version # buildkit
# Tue, 14 Feb 2023 20:05:04 GMT
COPY ./server-config.json . # buildkit
# Tue, 14 Feb 2023 20:05:04 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 14 Feb 2023 20:05:04 GMT
USER notary
# Tue, 14 Feb 2023 20:05:04 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 14 Feb 2023 20:05:04 GMT
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
	-	`sha256:0ce210b702cb843704e45125cfce874a777fd6a55c770a32a2f5a896c0e773a7`  
		Last Modified: Tue, 14 Feb 2023 20:05:22 GMT  
		Size: 4.7 MB (4732933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03a0f708d756e8640b16678c930dba7db7f9c200c116db8f237ba2bee0c2987`  
		Last Modified: Tue, 14 Feb 2023 20:05:21 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6ac46a6c1d29d8b606b8e72e959ea5bbe53410c5454c1128904bcd76234731`  
		Last Modified: Tue, 14 Feb 2023 20:05:21 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ad87b79bdddada59ddb13ed86a64be7dc8e1e776a6305ff05acc86ac1a15d9`  
		Last Modified: Tue, 14 Feb 2023 20:05:22 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; 386

```console
$ docker pull notary@sha256:0051a396f9f855c79af832411477a4c7d2378269fc49944bff0715d4fd0eccba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7754948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230c21477b98b5a11af0491ebeeb38d1b540df1682e89ee33b1fa8d429f64a0a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:57:54 GMT
RUN adduser -D -H -g "" notary
# Sat, 12 Nov 2022 04:57:55 GMT
EXPOSE 4443
# Sat, 12 Nov 2022 04:57:56 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 04:57:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 04:57:58 GMT
WORKDIR /notary/server
# Wed, 16 Nov 2022 20:11:14 GMT
COPY file:a4c6c805f5f0a0a5415c68f8471cb31bca1747a0f8e35cf5005cea98e0fba5b5 in ./ 
# Wed, 16 Nov 2022 20:11:14 GMT
RUN ./notary-server --version
# Wed, 16 Nov 2022 20:11:16 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Wed, 16 Nov 2022 20:11:17 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Wed, 16 Nov 2022 20:11:17 GMT
USER notary
# Wed, 16 Nov 2022 20:11:18 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 16 Nov 2022 20:11:19 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e2a37344f15c9c47f28fb76d0bbfae6f9adb65b4d686216a9a5881505ed0ec`  
		Last Modified: Sat, 12 Nov 2022 04:58:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9866a73f72dbc8d55f6da18666277753336525decc6cf3f5862f64f9aede0bb4`  
		Last Modified: Sat, 12 Nov 2022 04:58:40 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:babe522935d5c7619a31b2dbe314aa999f9638f58cfd681d4ead6cf30174456e`  
		Last Modified: Wed, 16 Nov 2022 20:11:48 GMT  
		Size: 4.9 MB (4944492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cba96d642e8b023076db8e169e56c622fd46d71523562be43e6488fde467c1f`  
		Last Modified: Wed, 16 Nov 2022 20:11:47 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2526f0d6947677f3d4316cad2f10abb51443194ed1ba4f3d3b757a812041fd13`  
		Last Modified: Wed, 16 Nov 2022 20:11:47 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; ppc64le

```console
$ docker pull notary@sha256:4455476a2044a6173a3ff87b432456677728e1dd071a0e61a58b429ff39de8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21fe4be34cc930680dd74d93cd2635777341a6b83fe5944d4c30c8008fa4e0fd`
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
# Tue, 14 Feb 2023 20:14:46 GMT
COPY /notary-server ./ # buildkit
# Tue, 14 Feb 2023 20:14:46 GMT
RUN ./notary-server --version # buildkit
# Tue, 14 Feb 2023 20:14:47 GMT
COPY ./server-config.json . # buildkit
# Tue, 14 Feb 2023 20:14:47 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 14 Feb 2023 20:14:47 GMT
USER notary
# Tue, 14 Feb 2023 20:14:47 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 14 Feb 2023 20:14:47 GMT
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
	-	`sha256:b771047091b6ffcb37bedd4c32c7079ea306bae1684ec9b9eabf4f6e3c4b9ca5`  
		Last Modified: Tue, 14 Feb 2023 20:15:21 GMT  
		Size: 4.6 MB (4637173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d2a10fccab08de9e5923b4ec3bc3b6fe49ac8c5b1d011a007cb253bc01fe5b`  
		Last Modified: Tue, 14 Feb 2023 20:15:20 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045c425c4d1d0b795444b81b62c22f0bb06f3035d3bd813a6dc994b7fa35d616`  
		Last Modified: Tue, 14 Feb 2023 20:15:20 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c4c8bb85af16915aa06f0e909653198a3be722d59583e7d2ad508e25639ad4`  
		Last Modified: Tue, 14 Feb 2023 20:15:20 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; s390x

```console
$ docker pull notary@sha256:a81bca1263711ee0c98ce648efccb89c08e43c3b6140e016e52fd67e5fe2eb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7569510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8790a1c5e350ae4289f6a10df068774c1f161b0b10d6ff081cb3eea149ecdd8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:38:26 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 03:38:26 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 11 Feb 2023 03:38:26 GMT
ENV INSTALLDIR=/notary/server
# Sat, 11 Feb 2023 03:38:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 11 Feb 2023 03:38:26 GMT
WORKDIR /notary/server
# Tue, 14 Feb 2023 20:11:10 GMT
COPY /notary-server ./ # buildkit
# Tue, 14 Feb 2023 20:11:10 GMT
RUN ./notary-server --version # buildkit
# Tue, 14 Feb 2023 20:11:10 GMT
COPY ./server-config.json . # buildkit
# Tue, 14 Feb 2023 20:11:10 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 14 Feb 2023 20:11:10 GMT
USER notary
# Tue, 14 Feb 2023 20:11:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 14 Feb 2023 20:11:10 GMT
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
	-	`sha256:7c75add70220598690f6ddee6110d6c3abc7a3d87465e472c8e2a4383161d42c`  
		Last Modified: Tue, 14 Feb 2023 20:11:43 GMT  
		Size: 5.0 MB (4973695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8b57bd5d47d546118346b050879199fd20564efa56e188ed5c24849dcb6ab1`  
		Last Modified: Tue, 14 Feb 2023 20:11:42 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233f6279916a848ff51598d6ad3d352e0e39faedddd2d5b7a05892b48b67d78d`  
		Last Modified: Tue, 14 Feb 2023 20:11:42 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8856e3c3ed294e627ee452379107302c39d29f6ed98172164ea22350dc1f4e75`  
		Last Modified: Tue, 14 Feb 2023 20:11:42 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
