<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `notary`

-	[`notary:server`](#notaryserver)
-	[`notary:server-0.7.0`](#notaryserver-070)
-	[`notary:signer`](#notarysigner)
-	[`notary:signer-0.7.0`](#notarysigner-070)

## `notary:server`

```console
$ docker pull notary@sha256:e0a470730a2192268fbe3cf74b7b4bd13e84a2d59f274042031344badaf91a79
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
$ docker pull notary@sha256:f31cfcc32cd35b3b000a6d4f90ac18406f8311255976f9fd31a80ffc0b6594f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ee151479f99297a9965ef0a6a8f16ade1cb73c9932b1c19e5b4e5b2acde6cc`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:38:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 06:38:02 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 06:38:02 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 06:38:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 06:38:02 GMT
WORKDIR /notary/server
# Wed, 11 Jan 2023 00:28:20 GMT
COPY /notary-server ./ # buildkit
# Wed, 11 Jan 2023 00:28:20 GMT
RUN ./notary-server --version # buildkit
# Wed, 11 Jan 2023 00:28:21 GMT
COPY ./server-config.json . # buildkit
# Wed, 11 Jan 2023 00:28:21 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 11 Jan 2023 00:28:21 GMT
USER notary
# Wed, 11 Jan 2023 00:28:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 00:28:21 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab556644ad7457163fa974396862be0db6a3e9b2a288041b04e6009ae65f4ed`  
		Last Modified: Sat, 12 Nov 2022 06:38:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed42602a65127618c555766dddb85795b2a28b21875015cc78f009e503b964d`  
		Last Modified: Sat, 12 Nov 2022 06:38:18 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef06100438a2bf4e36e29814583a87c44dd3054d22576c60074012a581a4cba5`  
		Last Modified: Wed, 11 Jan 2023 00:28:37 GMT  
		Size: 5.1 MB (5143252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8936f6951e0b4c37477a0110a1c707c9086edf0a7a3bd95d8d8b60165974391c`  
		Last Modified: Wed, 11 Jan 2023 00:28:36 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659367c4e2ff2c5d63a9d5761542ca00485d105e36a1eb56320369e891004470`  
		Last Modified: Wed, 11 Jan 2023 00:28:36 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6e4c9abd9870c4741062598dcf0d14a0a931595b65ba60461e4cf257e4bf5e`  
		Last Modified: Wed, 11 Jan 2023 00:28:36 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:94a7f44c0823c725318d9850534922b45fd87d37ed3fa1b6ff10340fb3a6318f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c583cd685b2dc71e537ea2e8266313b612bfad39937b6d294e91743c52bb2d`
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
# Sat, 11 Feb 2023 02:32:38 GMT
COPY /notary-server ./ # buildkit
# Sat, 11 Feb 2023 02:32:38 GMT
RUN ./notary-server --version # buildkit
# Sat, 11 Feb 2023 02:32:38 GMT
COPY ./server-config.json . # buildkit
# Sat, 11 Feb 2023 02:32:38 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 02:32:38 GMT
USER notary
# Sat, 11 Feb 2023 02:32:38 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 02:32:38 GMT
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
	-	`sha256:fa5d9dc845a51532ff633754a056db8ad31821a93dac8da4f57c3d5e133f52ae`  
		Last Modified: Sat, 11 Feb 2023 02:33:15 GMT  
		Size: 4.9 MB (4889026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbdc9724c289c4e78ec03366272a38951b9be496f9ce7c2c27b945d7ed605da`  
		Last Modified: Sat, 11 Feb 2023 02:33:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15226eafff3e6efdf1bd17280db9e7ccb97f6a85f2a59175cb0995d86ef80468`  
		Last Modified: Sat, 11 Feb 2023 02:33:14 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf80926f59059e4492f2548fcf98a7d665c872f37e0d3b59fd17f30366a77655`  
		Last Modified: Sat, 11 Feb 2023 02:33:14 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:fab1d152ba85f7d557c64bfe0571ed3f9001aac11124af5d460c4cf5521d813d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa946002f86aa32e4ec4fb72c68c061772e44abc41b8a4e361727a0530ad2d2`
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
# Sat, 11 Feb 2023 02:01:53 GMT
COPY /notary-server ./ # buildkit
# Sat, 11 Feb 2023 02:01:53 GMT
RUN ./notary-server --version # buildkit
# Sat, 11 Feb 2023 02:01:53 GMT
COPY ./server-config.json . # buildkit
# Sat, 11 Feb 2023 02:01:53 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 02:01:53 GMT
USER notary
# Sat, 11 Feb 2023 02:01:53 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 02:01:53 GMT
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
	-	`sha256:c300a137cf68b056bb2ea317ea498939e29f5b35416092479c58ca7c0594c9c0`  
		Last Modified: Sat, 11 Feb 2023 02:02:09 GMT  
		Size: 4.7 MB (4731061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1864a8e05666cfd16029d00d651645befbc32204a6fd9fe049335a5578443f`  
		Last Modified: Sat, 11 Feb 2023 02:02:08 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e378f4175175b52400ef7d37f5246676e8739de0f7b99c818f9a9e466851ad2a`  
		Last Modified: Sat, 11 Feb 2023 02:02:08 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35695e5d302ab305c852568c3806cbe4d3e34ef4ae4c0284de4e74852b830b7`  
		Last Modified: Sat, 11 Feb 2023 02:02:08 GMT  
		Size: 380.0 B  
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
$ docker pull notary@sha256:11c151b9b4da4033b1ef329402096cade396dd81953d622ef40717cac03c69cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec4a7732690b8055140b56caa47e849077c85a65112cf1f06d3453717fa8e25`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:12:27 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 07:12:27 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 07:12:27 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 07:12:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 07:12:27 GMT
WORKDIR /notary/server
# Wed, 11 Jan 2023 00:34:27 GMT
COPY /notary-server ./ # buildkit
# Wed, 11 Jan 2023 00:34:27 GMT
RUN ./notary-server --version # buildkit
# Wed, 11 Jan 2023 00:34:28 GMT
COPY ./server-config.json . # buildkit
# Wed, 11 Jan 2023 00:34:28 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 11 Jan 2023 00:34:28 GMT
USER notary
# Wed, 11 Jan 2023 00:34:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 00:34:28 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15023fe5082ace3d77a3ca4c98a9b31b5bef60a4835bddce618606ee9f17cf6`  
		Last Modified: Sat, 12 Nov 2022 07:13:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f15b402da893576104d72bedce0b38fd79217c0335b5c4ce1a6076cebbb1b8a`  
		Last Modified: Sat, 12 Nov 2022 07:12:59 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83598c98641df89168c689b5a5544eb47c20fe268fac165b3a3991374f5869b`  
		Last Modified: Wed, 11 Jan 2023 00:35:04 GMT  
		Size: 4.6 MB (4634388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f398a819638b368af0c080a30450a975c3179f5a77e134686d560928ca93c`  
		Last Modified: Wed, 11 Jan 2023 00:35:03 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eab9cb545d457c31b42c3940dc6ef7ae068ebf9fc8715b0f7a4cef6d11c4b2d`  
		Last Modified: Wed, 11 Jan 2023 00:35:03 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f249b0c64141d81e53c3545ae2001788a0671d1511f217edc11164592f0192`  
		Last Modified: Wed, 11 Jan 2023 00:35:03 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; s390x

```console
$ docker pull notary@sha256:eba39b625421d699f2dfbbeef57a55d6719cc33ee0bf53f7fd81848691a47a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7565514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07dbed1a3b95a002a7ae9bcf37bc5fd356fd4c15b0a10a3b3e6439bc8db799b2`
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
# Sat, 11 Feb 2023 03:38:47 GMT
COPY /notary-server ./ # buildkit
# Sat, 11 Feb 2023 03:38:47 GMT
RUN ./notary-server --version # buildkit
# Sat, 11 Feb 2023 03:38:47 GMT
COPY ./server-config.json . # buildkit
# Sat, 11 Feb 2023 03:38:47 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 03:38:47 GMT
USER notary
# Sat, 11 Feb 2023 03:38:47 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 03:38:47 GMT
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
	-	`sha256:5acbe100bf786f87d635e681b91483e54b27402fc321f94fade09a0211c16b77`  
		Last Modified: Sat, 11 Feb 2023 03:39:15 GMT  
		Size: 5.0 MB (4969707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d049f45e496638d6bd7afff4acf37625c71956bf7616e3f911944998126d5`  
		Last Modified: Sat, 11 Feb 2023 03:39:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdac13dd23a3cedb4523f8a01c7c1ca746055820bc99832e76863438b0f14f5`  
		Last Modified: Sat, 11 Feb 2023 03:39:14 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e15ebb842f7608aab222e3a83fe1fa08805fdd433f59134ac695272a831ccb`  
		Last Modified: Sat, 11 Feb 2023 03:39:14 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:server-0.7.0`

```console
$ docker pull notary@sha256:e0a470730a2192268fbe3cf74b7b4bd13e84a2d59f274042031344badaf91a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:server-0.7.0` - linux; amd64

```console
$ docker pull notary@sha256:f31cfcc32cd35b3b000a6d4f90ac18406f8311255976f9fd31a80ffc0b6594f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ee151479f99297a9965ef0a6a8f16ade1cb73c9932b1c19e5b4e5b2acde6cc`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:38:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 06:38:02 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 06:38:02 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 06:38:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 06:38:02 GMT
WORKDIR /notary/server
# Wed, 11 Jan 2023 00:28:20 GMT
COPY /notary-server ./ # buildkit
# Wed, 11 Jan 2023 00:28:20 GMT
RUN ./notary-server --version # buildkit
# Wed, 11 Jan 2023 00:28:21 GMT
COPY ./server-config.json . # buildkit
# Wed, 11 Jan 2023 00:28:21 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 11 Jan 2023 00:28:21 GMT
USER notary
# Wed, 11 Jan 2023 00:28:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 00:28:21 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab556644ad7457163fa974396862be0db6a3e9b2a288041b04e6009ae65f4ed`  
		Last Modified: Sat, 12 Nov 2022 06:38:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed42602a65127618c555766dddb85795b2a28b21875015cc78f009e503b964d`  
		Last Modified: Sat, 12 Nov 2022 06:38:18 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef06100438a2bf4e36e29814583a87c44dd3054d22576c60074012a581a4cba5`  
		Last Modified: Wed, 11 Jan 2023 00:28:37 GMT  
		Size: 5.1 MB (5143252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8936f6951e0b4c37477a0110a1c707c9086edf0a7a3bd95d8d8b60165974391c`  
		Last Modified: Wed, 11 Jan 2023 00:28:36 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659367c4e2ff2c5d63a9d5761542ca00485d105e36a1eb56320369e891004470`  
		Last Modified: Wed, 11 Jan 2023 00:28:36 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6e4c9abd9870c4741062598dcf0d14a0a931595b65ba60461e4cf257e4bf5e`  
		Last Modified: Wed, 11 Jan 2023 00:28:36 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:94a7f44c0823c725318d9850534922b45fd87d37ed3fa1b6ff10340fb3a6318f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c583cd685b2dc71e537ea2e8266313b612bfad39937b6d294e91743c52bb2d`
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
# Sat, 11 Feb 2023 02:32:38 GMT
COPY /notary-server ./ # buildkit
# Sat, 11 Feb 2023 02:32:38 GMT
RUN ./notary-server --version # buildkit
# Sat, 11 Feb 2023 02:32:38 GMT
COPY ./server-config.json . # buildkit
# Sat, 11 Feb 2023 02:32:38 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 02:32:38 GMT
USER notary
# Sat, 11 Feb 2023 02:32:38 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 02:32:38 GMT
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
	-	`sha256:fa5d9dc845a51532ff633754a056db8ad31821a93dac8da4f57c3d5e133f52ae`  
		Last Modified: Sat, 11 Feb 2023 02:33:15 GMT  
		Size: 4.9 MB (4889026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbdc9724c289c4e78ec03366272a38951b9be496f9ce7c2c27b945d7ed605da`  
		Last Modified: Sat, 11 Feb 2023 02:33:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15226eafff3e6efdf1bd17280db9e7ccb97f6a85f2a59175cb0995d86ef80468`  
		Last Modified: Sat, 11 Feb 2023 02:33:14 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf80926f59059e4492f2548fcf98a7d665c872f37e0d3b59fd17f30366a77655`  
		Last Modified: Sat, 11 Feb 2023 02:33:14 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:fab1d152ba85f7d557c64bfe0571ed3f9001aac11124af5d460c4cf5521d813d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa946002f86aa32e4ec4fb72c68c061772e44abc41b8a4e361727a0530ad2d2`
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
# Sat, 11 Feb 2023 02:01:53 GMT
COPY /notary-server ./ # buildkit
# Sat, 11 Feb 2023 02:01:53 GMT
RUN ./notary-server --version # buildkit
# Sat, 11 Feb 2023 02:01:53 GMT
COPY ./server-config.json . # buildkit
# Sat, 11 Feb 2023 02:01:53 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 02:01:53 GMT
USER notary
# Sat, 11 Feb 2023 02:01:53 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 02:01:53 GMT
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
	-	`sha256:c300a137cf68b056bb2ea317ea498939e29f5b35416092479c58ca7c0594c9c0`  
		Last Modified: Sat, 11 Feb 2023 02:02:09 GMT  
		Size: 4.7 MB (4731061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1864a8e05666cfd16029d00d651645befbc32204a6fd9fe049335a5578443f`  
		Last Modified: Sat, 11 Feb 2023 02:02:08 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e378f4175175b52400ef7d37f5246676e8739de0f7b99c818f9a9e466851ad2a`  
		Last Modified: Sat, 11 Feb 2023 02:02:08 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35695e5d302ab305c852568c3806cbe4d3e34ef4ae4c0284de4e74852b830b7`  
		Last Modified: Sat, 11 Feb 2023 02:02:08 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; 386

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

### `notary:server-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:11c151b9b4da4033b1ef329402096cade396dd81953d622ef40717cac03c69cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec4a7732690b8055140b56caa47e849077c85a65112cf1f06d3453717fa8e25`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:12:27 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 07:12:27 GMT
EXPOSE map[4443/tcp:{}]
# Sat, 12 Nov 2022 07:12:27 GMT
ENV INSTALLDIR=/notary/server
# Sat, 12 Nov 2022 07:12:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Sat, 12 Nov 2022 07:12:27 GMT
WORKDIR /notary/server
# Wed, 11 Jan 2023 00:34:27 GMT
COPY /notary-server ./ # buildkit
# Wed, 11 Jan 2023 00:34:27 GMT
RUN ./notary-server --version # buildkit
# Wed, 11 Jan 2023 00:34:28 GMT
COPY ./server-config.json . # buildkit
# Wed, 11 Jan 2023 00:34:28 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 11 Jan 2023 00:34:28 GMT
USER notary
# Wed, 11 Jan 2023 00:34:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 00:34:28 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15023fe5082ace3d77a3ca4c98a9b31b5bef60a4835bddce618606ee9f17cf6`  
		Last Modified: Sat, 12 Nov 2022 07:13:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f15b402da893576104d72bedce0b38fd79217c0335b5c4ce1a6076cebbb1b8a`  
		Last Modified: Sat, 12 Nov 2022 07:12:59 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83598c98641df89168c689b5a5544eb47c20fe268fac165b3a3991374f5869b`  
		Last Modified: Wed, 11 Jan 2023 00:35:04 GMT  
		Size: 4.6 MB (4634388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f398a819638b368af0c080a30450a975c3179f5a77e134686d560928ca93c`  
		Last Modified: Wed, 11 Jan 2023 00:35:03 GMT  
		Size: 90.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eab9cb545d457c31b42c3940dc6ef7ae068ebf9fc8715b0f7a4cef6d11c4b2d`  
		Last Modified: Wed, 11 Jan 2023 00:35:03 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f249b0c64141d81e53c3545ae2001788a0671d1511f217edc11164592f0192`  
		Last Modified: Wed, 11 Jan 2023 00:35:03 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:eba39b625421d699f2dfbbeef57a55d6719cc33ee0bf53f7fd81848691a47a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7565514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07dbed1a3b95a002a7ae9bcf37bc5fd356fd4c15b0a10a3b3e6439bc8db799b2`
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
# Sat, 11 Feb 2023 03:38:47 GMT
COPY /notary-server ./ # buildkit
# Sat, 11 Feb 2023 03:38:47 GMT
RUN ./notary-server --version # buildkit
# Sat, 11 Feb 2023 03:38:47 GMT
COPY ./server-config.json . # buildkit
# Sat, 11 Feb 2023 03:38:47 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 03:38:47 GMT
USER notary
# Sat, 11 Feb 2023 03:38:47 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 03:38:47 GMT
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
	-	`sha256:5acbe100bf786f87d635e681b91483e54b27402fc321f94fade09a0211c16b77`  
		Last Modified: Sat, 11 Feb 2023 03:39:15 GMT  
		Size: 5.0 MB (4969707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d049f45e496638d6bd7afff4acf37625c71956bf7616e3f911944998126d5`  
		Last Modified: Sat, 11 Feb 2023 03:39:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdac13dd23a3cedb4523f8a01c7c1ca746055820bc99832e76863438b0f14f5`  
		Last Modified: Sat, 11 Feb 2023 03:39:14 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e15ebb842f7608aab222e3a83fe1fa08805fdd433f59134ac695272a831ccb`  
		Last Modified: Sat, 11 Feb 2023 03:39:14 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:signer`

```console
$ docker pull notary@sha256:b3ba0e2985f1f882616ef90f5b54ab6cf05b3befd674f056c83ceac4070c9e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:signer` - linux; amd64

```console
$ docker pull notary@sha256:f00c696380534b61fbf5e0c9137f0d2c475222c77b2a2b3090807c21dbf19480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7565648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120b11cd1c150c6e4e3c823fc330779f4984867eac70bd007f2f2599f6d01152`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:38:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 06:38:08 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 06:38:08 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 06:38:08 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 06:38:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 06:38:08 GMT
WORKDIR /notary/signer
# Wed, 11 Jan 2023 00:28:27 GMT
COPY /notary-signer ./ # buildkit
# Wed, 11 Jan 2023 00:28:27 GMT
RUN ./notary-signer --version # buildkit
# Wed, 11 Jan 2023 00:28:28 GMT
COPY ./signer-config.json . # buildkit
# Wed, 11 Jan 2023 00:28:28 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 11 Jan 2023 00:28:28 GMT
USER notary
# Wed, 11 Jan 2023 00:28:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 00:28:28 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab556644ad7457163fa974396862be0db6a3e9b2a288041b04e6009ae65f4ed`  
		Last Modified: Sat, 12 Nov 2022 06:38:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da59cda2c120691b5be31fdc1571f10856ae5c4527c577ae2f76cd70fcd4a05`  
		Last Modified: Sat, 12 Nov 2022 06:38:29 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18df28869ba84e36cb24d2a6ffa9c8c495aadfd4a580bbc2fd32241b8d3e53bf`  
		Last Modified: Wed, 11 Jan 2023 00:28:47 GMT  
		Size: 4.8 MB (4757208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d38f8b72abfe9ed90b46e58eec6c1c29e3956676d9859f7df8ba7c9ccd8fb6`  
		Last Modified: Wed, 11 Jan 2023 00:28:46 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf34f3a2e8b14a03d0f25158b458b3ca10e626f01f0abee722308141866bbc95`  
		Last Modified: Wed, 11 Jan 2023 00:28:46 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8fa916538b7fae7415495c17ce06d7c5066d3fd40a5c5b7da79a6233f391b9`  
		Last Modified: Wed, 11 Jan 2023 00:28:46 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm variant v6

```console
$ docker pull notary@sha256:bb634ca5536aa9b0f344d70a69b5bba91834f122d8b4b80b5d77f78a9cd9e115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7139247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b297fbb89517418584491cdfd9419367d1c4f28cb4691026d3f683e650942858`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 02:32:16 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 02:32:55 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 11 Feb 2023 02:32:55 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 11 Feb 2023 02:32:55 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 11 Feb 2023 02:32:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 11 Feb 2023 02:32:55 GMT
WORKDIR /notary/signer
# Sat, 11 Feb 2023 02:32:55 GMT
COPY /notary-signer ./ # buildkit
# Sat, 11 Feb 2023 02:32:56 GMT
RUN ./notary-signer --version # buildkit
# Sat, 11 Feb 2023 02:32:56 GMT
COPY ./signer-config.json . # buildkit
# Sat, 11 Feb 2023 02:32:56 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 02:32:56 GMT
USER notary
# Sat, 11 Feb 2023 02:32:56 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 02:32:56 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:c3c6ce0c76930b11592424a93e59b53baba39c156698eec54ee9e678cdede4a7`  
		Last Modified: Sat, 11 Feb 2023 02:33:27 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa00b98a5acf034479f22ee64b7429d4a0aeaa856b44629b9756452041aa9e4`  
		Last Modified: Sat, 11 Feb 2023 02:33:27 GMT  
		Size: 4.5 MB (4520337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ffb805c9e2812b9294142e339972078f0d79a633a4ea690056cc04b6424e87`  
		Last Modified: Sat, 11 Feb 2023 02:33:26 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76d0cb4d34a8add21d4d92b2a4853079a584c6e0b04fe49ece561625ba35e4f`  
		Last Modified: Sat, 11 Feb 2023 02:33:27 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0ac6a2120d1e1319ad9168d959adcff931ac1e2a7c1c6d21a95efe4c5a712e`  
		Last Modified: Sat, 11 Feb 2023 02:33:27 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:7cc9193896a1b251d5c57fd458cab668557003ab8e654e19235f798dbfc39463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7096247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b45990584b7c7b8d55319e5d6f006444953afe3ff1a8e91ba320205454af5af`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 02:01:39 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 11 Feb 2023 02:01:58 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 11 Feb 2023 02:01:58 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 11 Feb 2023 02:01:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 11 Feb 2023 02:01:58 GMT
WORKDIR /notary/signer
# Sat, 11 Feb 2023 02:01:58 GMT
COPY /notary-signer ./ # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
RUN ./notary-signer --version # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
COPY ./signer-config.json . # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
USER notary
# Sat, 11 Feb 2023 02:01:58 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 02:01:58 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:9044747e4fd585aae1a06ddae8513379f85e397343798bc36f0e5504eaa9863f`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b44e162f00aeb4f435e25060abfebcd6a3177de0014d4e29bbf5a153ceb48f5`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 4.4 MB (4384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8714777b7cf5843776b9082e6dd73159753d55218ae6f1732bdaff862c5ef93`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ed9f175dc798302fa2481354771d76f6e4f027aacb021b415e8dfb173dc4fb`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b02ad41bc78686eaa6c286b9846236aeb22f1725692e5b5d7192923273d196c`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; 386

```console
$ docker pull notary@sha256:79b4c323f58cb5f6ea257c2af5204098abeea66bb6d3c60b46f4693e04741701
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddf368d5d9c9179b534f7d9a67b82e27281f60554a17dc0820eabc3abfca32c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:57:54 GMT
RUN adduser -D -H -g "" notary
# Sat, 12 Nov 2022 04:58:12 GMT
EXPOSE 4444
# Sat, 12 Nov 2022 04:58:12 GMT
EXPOSE 7899
# Sat, 12 Nov 2022 04:58:13 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 04:58:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 04:58:15 GMT
WORKDIR /notary/signer
# Wed, 16 Nov 2022 20:11:26 GMT
COPY file:044b2b6099382d2e11ff09d47c7a63f7cf3796f05317a8a2bbfed5d98c843503 in ./ 
# Wed, 16 Nov 2022 20:11:26 GMT
RUN ./notary-signer --version
# Wed, 16 Nov 2022 20:11:28 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Wed, 16 Nov 2022 20:11:29 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Wed, 16 Nov 2022 20:11:29 GMT
USER notary
# Wed, 16 Nov 2022 20:11:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 16 Nov 2022 20:11:31 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:e26472dc994c1e659b114a40b8becb18e4595de57079b3495843fe3ee077329d`  
		Last Modified: Sat, 12 Nov 2022 04:58:51 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77cc9f8b030709827b83734498c26e9c13fdcad73c1751041bf38760164b7c8`  
		Last Modified: Wed, 16 Nov 2022 20:11:58 GMT  
		Size: 4.6 MB (4571177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d739be5aa3edcc7ba9f282a037921fc7c54d03aa47497444165ee21ada1487a6`  
		Last Modified: Wed, 16 Nov 2022 20:11:57 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f6cc98121c6d6e23c455cc4891ee75f1d872207a89e3ff24c67d8eedf86dac`  
		Last Modified: Wed, 16 Nov 2022 20:11:58 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; ppc64le

```console
$ docker pull notary@sha256:2b2cac51751dbe89a896622064b2b6daa113c9af5a44c68b092ffe41f1b2334f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7096889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f7d83174a997548fe80efaf19090e2ca8db1780da72697fd0e25fec0544cb5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:12:27 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 07:12:40 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 07:12:40 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 07:12:40 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 07:12:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 07:12:40 GMT
WORKDIR /notary/signer
# Wed, 11 Jan 2023 00:34:42 GMT
COPY /notary-signer ./ # buildkit
# Wed, 11 Jan 2023 00:34:43 GMT
RUN ./notary-signer --version # buildkit
# Wed, 11 Jan 2023 00:34:44 GMT
COPY ./signer-config.json . # buildkit
# Wed, 11 Jan 2023 00:34:44 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 11 Jan 2023 00:34:44 GMT
USER notary
# Wed, 11 Jan 2023 00:34:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 00:34:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15023fe5082ace3d77a3ca4c98a9b31b5bef60a4835bddce618606ee9f17cf6`  
		Last Modified: Sat, 12 Nov 2022 07:13:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca3c7abc8ed18b90618dae3d8ed39fa05a0357ae27fab896191fb471938ae78`  
		Last Modified: Sat, 12 Nov 2022 07:13:14 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deee061c403b3386800e6c7e6923b535156333ff7487eba4829685703f26b077`  
		Last Modified: Wed, 11 Jan 2023 00:35:16 GMT  
		Size: 4.3 MB (4293169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105871502b0be8567633ecfebc62cb7b991169a9deab7511536215264306a237`  
		Last Modified: Wed, 11 Jan 2023 00:35:15 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c93a3c85bd91aacf3c678ee7161a59f4e917b935af370e2610d5a427db3f94`  
		Last Modified: Wed, 11 Jan 2023 00:35:15 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152baf0ef7c80edfa82907d1e9ab9aa1a72dea74d9a533f9b7ed79414953cb57`  
		Last Modified: Wed, 11 Jan 2023 00:35:15 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; s390x

```console
$ docker pull notary@sha256:8820af22a3b00b473863d68fb40268dec9836bb55f3303db4333e876d085859c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7197247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f539e399ab2f3957c8fbad1bde72670b37493863b4da684a17e1812913a7f2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:38:26 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 03:38:57 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 11 Feb 2023 03:38:57 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 11 Feb 2023 03:38:57 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 11 Feb 2023 03:38:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 11 Feb 2023 03:38:57 GMT
WORKDIR /notary/signer
# Sat, 11 Feb 2023 03:38:57 GMT
COPY /notary-signer ./ # buildkit
# Sat, 11 Feb 2023 03:38:58 GMT
RUN ./notary-signer --version # buildkit
# Sat, 11 Feb 2023 03:38:58 GMT
COPY ./signer-config.json . # buildkit
# Sat, 11 Feb 2023 03:38:58 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 03:38:58 GMT
USER notary
# Sat, 11 Feb 2023 03:38:58 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 03:38:58 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:e47b3001bbc3d992bc8bd18f0274d2c096ab38122bfe91ebb713a068610faf80`  
		Last Modified: Sat, 11 Feb 2023 03:39:21 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7369c97070f6a3fbdc8ff9020486e48e76f68bea04cd630597a2b427124f61`  
		Last Modified: Sat, 11 Feb 2023 03:39:22 GMT  
		Size: 4.6 MB (4601507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e525f79d1d26921173c24db57698269bbb8a4052185fdf39494626b1315748a3`  
		Last Modified: Sat, 11 Feb 2023 03:39:21 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a82556109a5343cbc38e64d4587eca77872ead719d83b49d0f1973a2d51d2dc`  
		Last Modified: Sat, 11 Feb 2023 03:39:21 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4563f9e909600e7aaa50b03cd21fa864ab8cd2f3d51ecce02e3d966076d944eb`  
		Last Modified: Sat, 11 Feb 2023 03:39:21 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:b3ba0e2985f1f882616ef90f5b54ab6cf05b3befd674f056c83ceac4070c9e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:signer-0.7.0` - linux; amd64

```console
$ docker pull notary@sha256:f00c696380534b61fbf5e0c9137f0d2c475222c77b2a2b3090807c21dbf19480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7565648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120b11cd1c150c6e4e3c823fc330779f4984867eac70bd007f2f2599f6d01152`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:38:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 06:38:08 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 06:38:08 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 06:38:08 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 06:38:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 06:38:08 GMT
WORKDIR /notary/signer
# Wed, 11 Jan 2023 00:28:27 GMT
COPY /notary-signer ./ # buildkit
# Wed, 11 Jan 2023 00:28:27 GMT
RUN ./notary-signer --version # buildkit
# Wed, 11 Jan 2023 00:28:28 GMT
COPY ./signer-config.json . # buildkit
# Wed, 11 Jan 2023 00:28:28 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 11 Jan 2023 00:28:28 GMT
USER notary
# Wed, 11 Jan 2023 00:28:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 00:28:28 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab556644ad7457163fa974396862be0db6a3e9b2a288041b04e6009ae65f4ed`  
		Last Modified: Sat, 12 Nov 2022 06:38:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da59cda2c120691b5be31fdc1571f10856ae5c4527c577ae2f76cd70fcd4a05`  
		Last Modified: Sat, 12 Nov 2022 06:38:29 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18df28869ba84e36cb24d2a6ffa9c8c495aadfd4a580bbc2fd32241b8d3e53bf`  
		Last Modified: Wed, 11 Jan 2023 00:28:47 GMT  
		Size: 4.8 MB (4757208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d38f8b72abfe9ed90b46e58eec6c1c29e3956676d9859f7df8ba7c9ccd8fb6`  
		Last Modified: Wed, 11 Jan 2023 00:28:46 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf34f3a2e8b14a03d0f25158b458b3ca10e626f01f0abee722308141866bbc95`  
		Last Modified: Wed, 11 Jan 2023 00:28:46 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8fa916538b7fae7415495c17ce06d7c5066d3fd40a5c5b7da79a6233f391b9`  
		Last Modified: Wed, 11 Jan 2023 00:28:46 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:bb634ca5536aa9b0f344d70a69b5bba91834f122d8b4b80b5d77f78a9cd9e115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7139247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b297fbb89517418584491cdfd9419367d1c4f28cb4691026d3f683e650942858`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 02:32:16 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 02:32:55 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 11 Feb 2023 02:32:55 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 11 Feb 2023 02:32:55 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 11 Feb 2023 02:32:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 11 Feb 2023 02:32:55 GMT
WORKDIR /notary/signer
# Sat, 11 Feb 2023 02:32:55 GMT
COPY /notary-signer ./ # buildkit
# Sat, 11 Feb 2023 02:32:56 GMT
RUN ./notary-signer --version # buildkit
# Sat, 11 Feb 2023 02:32:56 GMT
COPY ./signer-config.json . # buildkit
# Sat, 11 Feb 2023 02:32:56 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 02:32:56 GMT
USER notary
# Sat, 11 Feb 2023 02:32:56 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 02:32:56 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:c3c6ce0c76930b11592424a93e59b53baba39c156698eec54ee9e678cdede4a7`  
		Last Modified: Sat, 11 Feb 2023 02:33:27 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa00b98a5acf034479f22ee64b7429d4a0aeaa856b44629b9756452041aa9e4`  
		Last Modified: Sat, 11 Feb 2023 02:33:27 GMT  
		Size: 4.5 MB (4520337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ffb805c9e2812b9294142e339972078f0d79a633a4ea690056cc04b6424e87`  
		Last Modified: Sat, 11 Feb 2023 02:33:26 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76d0cb4d34a8add21d4d92b2a4853079a584c6e0b04fe49ece561625ba35e4f`  
		Last Modified: Sat, 11 Feb 2023 02:33:27 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0ac6a2120d1e1319ad9168d959adcff931ac1e2a7c1c6d21a95efe4c5a712e`  
		Last Modified: Sat, 11 Feb 2023 02:33:27 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:7cc9193896a1b251d5c57fd458cab668557003ab8e654e19235f798dbfc39463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7096247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b45990584b7c7b8d55319e5d6f006444953afe3ff1a8e91ba320205454af5af`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 02:01:39 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 11 Feb 2023 02:01:58 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 11 Feb 2023 02:01:58 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 11 Feb 2023 02:01:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 11 Feb 2023 02:01:58 GMT
WORKDIR /notary/signer
# Sat, 11 Feb 2023 02:01:58 GMT
COPY /notary-signer ./ # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
RUN ./notary-signer --version # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
COPY ./signer-config.json . # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
USER notary
# Sat, 11 Feb 2023 02:01:58 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 02:01:58 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:9044747e4fd585aae1a06ddae8513379f85e397343798bc36f0e5504eaa9863f`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b44e162f00aeb4f435e25060abfebcd6a3177de0014d4e29bbf5a153ceb48f5`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 4.4 MB (4384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8714777b7cf5843776b9082e6dd73159753d55218ae6f1732bdaff862c5ef93`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ed9f175dc798302fa2481354771d76f6e4f027aacb021b415e8dfb173dc4fb`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b02ad41bc78686eaa6c286b9846236aeb22f1725692e5b5d7192923273d196c`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:79b4c323f58cb5f6ea257c2af5204098abeea66bb6d3c60b46f4693e04741701
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddf368d5d9c9179b534f7d9a67b82e27281f60554a17dc0820eabc3abfca32c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:57:54 GMT
RUN adduser -D -H -g "" notary
# Sat, 12 Nov 2022 04:58:12 GMT
EXPOSE 4444
# Sat, 12 Nov 2022 04:58:12 GMT
EXPOSE 7899
# Sat, 12 Nov 2022 04:58:13 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 04:58:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 04:58:15 GMT
WORKDIR /notary/signer
# Wed, 16 Nov 2022 20:11:26 GMT
COPY file:044b2b6099382d2e11ff09d47c7a63f7cf3796f05317a8a2bbfed5d98c843503 in ./ 
# Wed, 16 Nov 2022 20:11:26 GMT
RUN ./notary-signer --version
# Wed, 16 Nov 2022 20:11:28 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Wed, 16 Nov 2022 20:11:29 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Wed, 16 Nov 2022 20:11:29 GMT
USER notary
# Wed, 16 Nov 2022 20:11:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 16 Nov 2022 20:11:31 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:e26472dc994c1e659b114a40b8becb18e4595de57079b3495843fe3ee077329d`  
		Last Modified: Sat, 12 Nov 2022 04:58:51 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77cc9f8b030709827b83734498c26e9c13fdcad73c1751041bf38760164b7c8`  
		Last Modified: Wed, 16 Nov 2022 20:11:58 GMT  
		Size: 4.6 MB (4571177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d739be5aa3edcc7ba9f282a037921fc7c54d03aa47497444165ee21ada1487a6`  
		Last Modified: Wed, 16 Nov 2022 20:11:57 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f6cc98121c6d6e23c455cc4891ee75f1d872207a89e3ff24c67d8eedf86dac`  
		Last Modified: Wed, 16 Nov 2022 20:11:58 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:2b2cac51751dbe89a896622064b2b6daa113c9af5a44c68b092ffe41f1b2334f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7096889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f7d83174a997548fe80efaf19090e2ca8db1780da72697fd0e25fec0544cb5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:12:27 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 07:12:40 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 07:12:40 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 07:12:40 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 07:12:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 07:12:40 GMT
WORKDIR /notary/signer
# Wed, 11 Jan 2023 00:34:42 GMT
COPY /notary-signer ./ # buildkit
# Wed, 11 Jan 2023 00:34:43 GMT
RUN ./notary-signer --version # buildkit
# Wed, 11 Jan 2023 00:34:44 GMT
COPY ./signer-config.json . # buildkit
# Wed, 11 Jan 2023 00:34:44 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 11 Jan 2023 00:34:44 GMT
USER notary
# Wed, 11 Jan 2023 00:34:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 00:34:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15023fe5082ace3d77a3ca4c98a9b31b5bef60a4835bddce618606ee9f17cf6`  
		Last Modified: Sat, 12 Nov 2022 07:13:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca3c7abc8ed18b90618dae3d8ed39fa05a0357ae27fab896191fb471938ae78`  
		Last Modified: Sat, 12 Nov 2022 07:13:14 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deee061c403b3386800e6c7e6923b535156333ff7487eba4829685703f26b077`  
		Last Modified: Wed, 11 Jan 2023 00:35:16 GMT  
		Size: 4.3 MB (4293169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105871502b0be8567633ecfebc62cb7b991169a9deab7511536215264306a237`  
		Last Modified: Wed, 11 Jan 2023 00:35:15 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c93a3c85bd91aacf3c678ee7161a59f4e917b935af370e2610d5a427db3f94`  
		Last Modified: Wed, 11 Jan 2023 00:35:15 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152baf0ef7c80edfa82907d1e9ab9aa1a72dea74d9a533f9b7ed79414953cb57`  
		Last Modified: Wed, 11 Jan 2023 00:35:15 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:8820af22a3b00b473863d68fb40268dec9836bb55f3303db4333e876d085859c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7197247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f539e399ab2f3957c8fbad1bde72670b37493863b4da684a17e1812913a7f2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:38:26 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 03:38:57 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 11 Feb 2023 03:38:57 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 11 Feb 2023 03:38:57 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 11 Feb 2023 03:38:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 11 Feb 2023 03:38:57 GMT
WORKDIR /notary/signer
# Sat, 11 Feb 2023 03:38:57 GMT
COPY /notary-signer ./ # buildkit
# Sat, 11 Feb 2023 03:38:58 GMT
RUN ./notary-signer --version # buildkit
# Sat, 11 Feb 2023 03:38:58 GMT
COPY ./signer-config.json . # buildkit
# Sat, 11 Feb 2023 03:38:58 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 03:38:58 GMT
USER notary
# Sat, 11 Feb 2023 03:38:58 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 03:38:58 GMT
CMD ["notary-signer" "--version"]
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
	-	`sha256:e47b3001bbc3d992bc8bd18f0274d2c096ab38122bfe91ebb713a068610faf80`  
		Last Modified: Sat, 11 Feb 2023 03:39:21 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7369c97070f6a3fbdc8ff9020486e48e76f68bea04cd630597a2b427124f61`  
		Last Modified: Sat, 11 Feb 2023 03:39:22 GMT  
		Size: 4.6 MB (4601507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e525f79d1d26921173c24db57698269bbb8a4052185fdf39494626b1315748a3`  
		Last Modified: Sat, 11 Feb 2023 03:39:21 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a82556109a5343cbc38e64d4587eca77872ead719d83b49d0f1973a2d51d2dc`  
		Last Modified: Sat, 11 Feb 2023 03:39:21 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4563f9e909600e7aaa50b03cd21fa864ab8cd2f3d51ecce02e3d966076d944eb`  
		Last Modified: Sat, 11 Feb 2023 03:39:21 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
