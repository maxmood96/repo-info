<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `notary`

-	[`notary:server`](#notaryserver)
-	[`notary:server-0.7.0`](#notaryserver-070)
-	[`notary:signer`](#notarysigner)
-	[`notary:signer-0.7.0`](#notarysigner-070)

## `notary:server`

```console
$ docker pull notary@sha256:da9db50d9602861ee0c91b907ceff79c5435a872d48832692406a04af278c58c
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
$ docker pull notary@sha256:5fb572b42f869100019223e88bea7fdb970c99a7bed15d693ebcfb07c30c90d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b2c7e4c0706a63ad53086ecdc0e2f950b225b49bf1f3807b8ed6080fc1b160`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:52:21 GMT
RUN RUN /bin/sh -c adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:52:21 GMT
RUN EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 01:52:21 GMT
RUN ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 01:52:21 GMT
RUN ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 01:52:21 GMT
RUN WORKDIR /notary/server
# Tue, 25 Oct 2022 01:52:41 GMT
RUN COPY /notary-server ./ # buildkit
# Tue, 25 Oct 2022 01:52:41 GMT
RUN RUN /bin/sh -c ./notary-server --version # buildkit
# Tue, 25 Oct 2022 01:52:41 GMT
RUN COPY ./server-config.json . # buildkit
# Tue, 25 Oct 2022 01:52:41 GMT
RUN COPY ./entrypoint.sh . # buildkit
# Tue, 25 Oct 2022 01:52:41 GMT
RUN USER notary
# Tue, 25 Oct 2022 01:52:41 GMT
RUN ENTRYPOINT ["entrypoint.sh"]
# Tue, 25 Oct 2022 01:52:41 GMT
RUN CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ae0db85ee62912972b015b43b47b5849f5b66900a08ad146a42f7c16d02def`  
		Last Modified: Tue, 25 Oct 2022 01:53:00 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae714b9c46c68b869025bf262b5afec2bb7f99f3739cdae14e11604248f87fd`  
		Last Modified: Tue, 25 Oct 2022 01:52:58 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb5988268b5ce114ad501a67026ee4c7beaaa4ceb5e0caeecb1323f69081ee4`  
		Last Modified: Tue, 25 Oct 2022 01:52:59 GMT  
		Size: 5.1 MB (5143114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633a0f4a6583d329246e2cb77d177b072ad76c5d91fc75833979d5903902e3e2`  
		Last Modified: Tue, 25 Oct 2022 01:52:58 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85eadab3113f2431afe68461f05df57b0d365862172a791d600e30f47b8b849b`  
		Last Modified: Tue, 25 Oct 2022 01:52:58 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6232df1b1bcee75f7d4edb89236c13e7ef4d4359076262d966d77c33d5edd8`  
		Last Modified: Tue, 25 Oct 2022 01:52:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm variant v6

```console
$ docker pull notary@sha256:69715961d90afb23dcd00843121a87d8751c727b57bd1de273b00e0153a276d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8344745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7525cdb059004173bfdcb900a2593fc6a0bea45cbcf37fdd945fc9c6f9045ce`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:18 GMT
ADD file:a62ad8c2b01195a2d42109e23b6d8ce69e2a816702518b2d823139f28c0ff799 in / 
# Mon, 04 Apr 2022 23:50:19 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 02:05:11 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 02:05:11 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 02:05:12 GMT
ENV INSTALLDIR=/notary/server
# Fri, 06 May 2022 02:05:12 GMT
EXPOSE 4443
# Fri, 06 May 2022 02:05:13 GMT
WORKDIR /notary/server
# Fri, 06 May 2022 02:05:40 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --version
# Fri, 06 May 2022 02:05:40 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Fri, 06 May 2022 02:05:41 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Fri, 06 May 2022 02:05:42 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 02:05:43 GMT
USER notary
# Fri, 06 May 2022 02:05:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Fri, 06 May 2022 02:05:43 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 02:05:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:6c4809594a4b80d650b9951499cc7be9a90fc7b306e1dd8052f821b60733ae0c`  
		Last Modified: Mon, 04 Apr 2022 23:52:09 GMT  
		Size: 2.6 MB (2605389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b941e03c3da865a69f9d30c13dde97171fe28cef6d72a16781d9faf4445e1`  
		Last Modified: Fri, 06 May 2022 02:06:56 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec356af48d05d45cb3e0fbd603e3da6a0793554bbd480b1bfa8b42be1073be37`  
		Last Modified: Fri, 06 May 2022 02:06:59 GMT  
		Size: 5.7 MB (5737230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc2ffa839e593a064a7020b3f6bf522d356710cbed25b71abeeaa4cc6947ecc`  
		Last Modified: Fri, 06 May 2022 02:06:56 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420fc87c3fb11d297c4b09c6be560cd84143a3a7d584278ac45d763bdc64a3f8`  
		Last Modified: Fri, 06 May 2022 02:06:56 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d2fa141338a1dac3da46f56b7c2d9e738c559a593138f6b007433322036f5f`  
		Last Modified: Fri, 06 May 2022 02:06:56 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:9bcc59824e4db2194b96f114a58dcd02e8a5ee01bfcc57e088d634f2c7766b02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8346196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad96cd15f3785f09c8a0dc678758238c222d5610476282c70b306ba865c1ee6b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:53 GMT
ADD file:a2a992b7f6af1e6f8f5648f329f4a4058d8c4377417ac23ae211290c0cdc8f4b in / 
# Mon, 04 Apr 2022 23:39:53 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 01:04:59 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 01:05:00 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 01:05:01 GMT
ENV INSTALLDIR=/notary/server
# Fri, 06 May 2022 01:05:02 GMT
EXPOSE 4443
# Fri, 06 May 2022 01:05:03 GMT
WORKDIR /notary/server
# Fri, 06 May 2022 01:05:17 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --version
# Fri, 06 May 2022 01:05:18 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Fri, 06 May 2022 01:05:19 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Fri, 06 May 2022 01:05:19 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 01:05:20 GMT
USER notary
# Fri, 06 May 2022 01:05:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Fri, 06 May 2022 01:05:22 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 01:05:23 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:0eeab5c200691bd777e227c6eea27f7ca3c8232b67118a76edac2dcde3186aa1`  
		Last Modified: Mon, 04 Apr 2022 23:41:02 GMT  
		Size: 2.7 MB (2716243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ed6330a9615a6e518283d07985b18d479a8f03c5c3f20015c6582538def18a`  
		Last Modified: Fri, 06 May 2022 01:06:14 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f91204882744da81d33ffcfc2d335958d94620b343be39e566107e354d4f2b9`  
		Last Modified: Fri, 06 May 2022 01:06:15 GMT  
		Size: 5.6 MB (5627862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b3c5e562a2e32c0984910ea2a31cbc0ebf70cfd1f0df3daca43466587ac161`  
		Last Modified: Fri, 06 May 2022 01:06:14 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2496335307234f487bccec5dd92b220fd206a951193aaaa8a893358ed5b3658`  
		Last Modified: Fri, 06 May 2022 01:06:14 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db8c9d2946bfc3596ae37b6aae0f362c1743c06274f0580f1d28bd048a53f44`  
		Last Modified: Fri, 06 May 2022 01:06:14 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; 386

```console
$ docker pull notary@sha256:37f2f429ef0f26e10ce0ffd80eb1db04075cc655e4ade968934feb015c81a5e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8660466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9890bfefc0e3351b820e016a71a528d1956569ab2df6944908ad9a909472f22`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:44 GMT
ADD file:c1616ef1514518ef1f90874b6fab7c42951a5736600b54942fd4ad4338a24b11 in / 
# Mon, 04 Apr 2022 23:38:44 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 01:53:33 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 01:53:34 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 01:53:35 GMT
ENV INSTALLDIR=/notary/server
# Fri, 06 May 2022 01:53:36 GMT
EXPOSE 4443
# Fri, 06 May 2022 01:53:37 GMT
WORKDIR /notary/server
# Fri, 06 May 2022 01:53:52 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --version
# Fri, 06 May 2022 01:53:54 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Fri, 06 May 2022 01:53:55 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Fri, 06 May 2022 01:53:55 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 01:53:56 GMT
USER notary
# Fri, 06 May 2022 01:53:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Fri, 06 May 2022 01:53:58 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 01:53:59 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:6f153ea7cf9623ea20df5792c26f8dfd80af131fecab00e40983e554e495421e`  
		Last Modified: Mon, 04 Apr 2022 23:39:57 GMT  
		Size: 2.8 MB (2798126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480520f3392b90043910d7268b537ecd1659ddbb5cb29c5adf77c88fef47d65a`  
		Last Modified: Fri, 06 May 2022 01:54:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00018550dcea7efab5be15d233fd261496846d3a597e4f07175aefc34a746117`  
		Last Modified: Fri, 06 May 2022 01:54:48 GMT  
		Size: 5.9 MB (5860251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddfb2fc3b62b892c8667daec55783ef3d63453ab4563b516c177934fcb49572`  
		Last Modified: Fri, 06 May 2022 01:54:47 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69e20ab1fa4892eca94c25948de9a1fdc3330ab23f1efffc98693352ee04fa5`  
		Last Modified: Fri, 06 May 2022 01:54:47 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c545d4343d941bfd383dd6acff9bdf6431eef4e14113eb33d31225edfe550c`  
		Last Modified: Fri, 06 May 2022 01:54:47 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; ppc64le

```console
$ docker pull notary@sha256:bae576e49f3c5ac60baf81b0cd47f6c7e292e3c1a2cc8b081d846e0cda62a5b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8348451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0495e05e0d7e4df038032361130b3a554797bc2a511c2c618a8890b845f212d3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 05 Apr 2022 00:24:09 GMT
ADD file:53d4ef78df099d878ecfe359308c0a3ee650850966fefbe1fd7c05f3b2d89e1b in / 
# Tue, 05 Apr 2022 00:24:11 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 01:48:47 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 01:48:49 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 01:48:53 GMT
ENV INSTALLDIR=/notary/server
# Fri, 06 May 2022 01:48:55 GMT
EXPOSE 4443
# Fri, 06 May 2022 01:49:00 GMT
WORKDIR /notary/server
# Fri, 06 May 2022 01:49:48 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --version
# Fri, 06 May 2022 01:49:50 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Fri, 06 May 2022 01:49:52 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Fri, 06 May 2022 01:49:57 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 01:50:01 GMT
USER notary
# Fri, 06 May 2022 01:50:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Fri, 06 May 2022 01:50:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 01:50:17 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:57c1475d5a6dc8e68a1b09bd09db22cc33e8f163a3841ce5100e0569acefcabe`  
		Last Modified: Tue, 05 Apr 2022 00:25:31 GMT  
		Size: 2.8 MB (2806745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d113a2296216ff0801eaaa23faf16370c503b4070e9895dd7788112939579b`  
		Last Modified: Fri, 06 May 2022 01:53:18 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9969d0f4c7adddcdbd67e584df60bb9ef69365671ae03723b39dc9807ffb8f71`  
		Last Modified: Fri, 06 May 2022 01:53:19 GMT  
		Size: 5.5 MB (5539583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4601a5f5eccd51d842fb5c837594b84c44958c2d40ad210aa02f774d8ce2d99c`  
		Last Modified: Fri, 06 May 2022 01:53:18 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfede6060e49c4ea18bb60fce541803e16bc21a163f2c7bd1e0d65273ea9ca2`  
		Last Modified: Fri, 06 May 2022 01:53:18 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fe6431b53b4dcf01fbf89da7c8ab80fbd68973c9ed96993ba18843a532afe9`  
		Last Modified: Fri, 06 May 2022 01:53:18 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server` - linux; s390x

```console
$ docker pull notary@sha256:5f0d8363d713d58005c200e30235ebbad1efd30d126fa6e8b921bef23dc549f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7560845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa0f87211b3a607ac91983abd06c400f17981935a09b074bcf4e6fa517d0a55`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:21:39 GMT
RUN RUN /bin/sh -c adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:21:39 GMT
RUN EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 01:21:39 GMT
RUN ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 01:21:39 GMT
RUN ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 01:21:39 GMT
RUN WORKDIR /notary/server
# Tue, 25 Oct 2022 01:22:02 GMT
RUN COPY /notary-server ./ # buildkit
# Tue, 25 Oct 2022 01:22:02 GMT
RUN RUN /bin/sh -c ./notary-server --version # buildkit
# Tue, 25 Oct 2022 01:22:02 GMT
RUN COPY ./server-config.json . # buildkit
# Tue, 25 Oct 2022 01:22:02 GMT
RUN COPY ./entrypoint.sh . # buildkit
# Tue, 25 Oct 2022 01:22:02 GMT
RUN USER notary
# Tue, 25 Oct 2022 01:22:02 GMT
RUN ENTRYPOINT ["entrypoint.sh"]
# Tue, 25 Oct 2022 01:22:02 GMT
RUN CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e57b7c2a2dbd108e38c96fd7b110170d3b57a921f34c3b015736a93b17e5ad`  
		Last Modified: Tue, 25 Oct 2022 01:22:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb73212e82f7d46920138e024d3233301bdffa778ba147338014ae69d65ba43c`  
		Last Modified: Tue, 25 Oct 2022 01:22:33 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6932c1633389acd33f1d9f659c505be3568406222966cef27e8ba12b8e99f2`  
		Last Modified: Tue, 25 Oct 2022 01:22:34 GMT  
		Size: 5.0 MB (4968022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8343a44b4f6777d4568e22ad69163d4b47cfd5210a1bd7d7b8299f0375980b1c`  
		Last Modified: Tue, 25 Oct 2022 01:22:33 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35439890b4d9dfb792c63c9afbed662ba45d800f8fd549997b8d5bd1952a4c86`  
		Last Modified: Tue, 25 Oct 2022 01:22:33 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9b2fbcdeb33d0cf5ed9e7962b4e280767c894054d34bc8e0de779a5f39e634`  
		Last Modified: Tue, 25 Oct 2022 01:22:33 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:server-0.7.0`

```console
$ docker pull notary@sha256:da9db50d9602861ee0c91b907ceff79c5435a872d48832692406a04af278c58c
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
$ docker pull notary@sha256:5fb572b42f869100019223e88bea7fdb970c99a7bed15d693ebcfb07c30c90d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7951396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b2c7e4c0706a63ad53086ecdc0e2f950b225b49bf1f3807b8ed6080fc1b160`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:52:21 GMT
RUN RUN /bin/sh -c adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:52:21 GMT
RUN EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 01:52:21 GMT
RUN ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 01:52:21 GMT
RUN ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 01:52:21 GMT
RUN WORKDIR /notary/server
# Tue, 25 Oct 2022 01:52:41 GMT
RUN COPY /notary-server ./ # buildkit
# Tue, 25 Oct 2022 01:52:41 GMT
RUN RUN /bin/sh -c ./notary-server --version # buildkit
# Tue, 25 Oct 2022 01:52:41 GMT
RUN COPY ./server-config.json . # buildkit
# Tue, 25 Oct 2022 01:52:41 GMT
RUN COPY ./entrypoint.sh . # buildkit
# Tue, 25 Oct 2022 01:52:41 GMT
RUN USER notary
# Tue, 25 Oct 2022 01:52:41 GMT
RUN ENTRYPOINT ["entrypoint.sh"]
# Tue, 25 Oct 2022 01:52:41 GMT
RUN CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ae0db85ee62912972b015b43b47b5849f5b66900a08ad146a42f7c16d02def`  
		Last Modified: Tue, 25 Oct 2022 01:53:00 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae714b9c46c68b869025bf262b5afec2bb7f99f3739cdae14e11604248f87fd`  
		Last Modified: Tue, 25 Oct 2022 01:52:58 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb5988268b5ce114ad501a67026ee4c7beaaa4ceb5e0caeecb1323f69081ee4`  
		Last Modified: Tue, 25 Oct 2022 01:52:59 GMT  
		Size: 5.1 MB (5143114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633a0f4a6583d329246e2cb77d177b072ad76c5d91fc75833979d5903902e3e2`  
		Last Modified: Tue, 25 Oct 2022 01:52:58 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85eadab3113f2431afe68461f05df57b0d365862172a791d600e30f47b8b849b`  
		Last Modified: Tue, 25 Oct 2022 01:52:58 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6232df1b1bcee75f7d4edb89236c13e7ef4d4359076262d966d77c33d5edd8`  
		Last Modified: Tue, 25 Oct 2022 01:52:58 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:69715961d90afb23dcd00843121a87d8751c727b57bd1de273b00e0153a276d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8344745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7525cdb059004173bfdcb900a2593fc6a0bea45cbcf37fdd945fc9c6f9045ce`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:18 GMT
ADD file:a62ad8c2b01195a2d42109e23b6d8ce69e2a816702518b2d823139f28c0ff799 in / 
# Mon, 04 Apr 2022 23:50:19 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 02:05:11 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 02:05:11 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 02:05:12 GMT
ENV INSTALLDIR=/notary/server
# Fri, 06 May 2022 02:05:12 GMT
EXPOSE 4443
# Fri, 06 May 2022 02:05:13 GMT
WORKDIR /notary/server
# Fri, 06 May 2022 02:05:40 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --version
# Fri, 06 May 2022 02:05:40 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Fri, 06 May 2022 02:05:41 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Fri, 06 May 2022 02:05:42 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 02:05:43 GMT
USER notary
# Fri, 06 May 2022 02:05:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Fri, 06 May 2022 02:05:43 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 02:05:44 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:6c4809594a4b80d650b9951499cc7be9a90fc7b306e1dd8052f821b60733ae0c`  
		Last Modified: Mon, 04 Apr 2022 23:52:09 GMT  
		Size: 2.6 MB (2605389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790b941e03c3da865a69f9d30c13dde97171fe28cef6d72a16781d9faf4445e1`  
		Last Modified: Fri, 06 May 2022 02:06:56 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec356af48d05d45cb3e0fbd603e3da6a0793554bbd480b1bfa8b42be1073be37`  
		Last Modified: Fri, 06 May 2022 02:06:59 GMT  
		Size: 5.7 MB (5737230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc2ffa839e593a064a7020b3f6bf522d356710cbed25b71abeeaa4cc6947ecc`  
		Last Modified: Fri, 06 May 2022 02:06:56 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420fc87c3fb11d297c4b09c6be560cd84143a3a7d584278ac45d763bdc64a3f8`  
		Last Modified: Fri, 06 May 2022 02:06:56 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d2fa141338a1dac3da46f56b7c2d9e738c559a593138f6b007433322036f5f`  
		Last Modified: Fri, 06 May 2022 02:06:56 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:9bcc59824e4db2194b96f114a58dcd02e8a5ee01bfcc57e088d634f2c7766b02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8346196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad96cd15f3785f09c8a0dc678758238c222d5610476282c70b306ba865c1ee6b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:53 GMT
ADD file:a2a992b7f6af1e6f8f5648f329f4a4058d8c4377417ac23ae211290c0cdc8f4b in / 
# Mon, 04 Apr 2022 23:39:53 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 01:04:59 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 01:05:00 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 01:05:01 GMT
ENV INSTALLDIR=/notary/server
# Fri, 06 May 2022 01:05:02 GMT
EXPOSE 4443
# Fri, 06 May 2022 01:05:03 GMT
WORKDIR /notary/server
# Fri, 06 May 2022 01:05:17 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --version
# Fri, 06 May 2022 01:05:18 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Fri, 06 May 2022 01:05:19 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Fri, 06 May 2022 01:05:19 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 01:05:20 GMT
USER notary
# Fri, 06 May 2022 01:05:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Fri, 06 May 2022 01:05:22 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 01:05:23 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:0eeab5c200691bd777e227c6eea27f7ca3c8232b67118a76edac2dcde3186aa1`  
		Last Modified: Mon, 04 Apr 2022 23:41:02 GMT  
		Size: 2.7 MB (2716243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ed6330a9615a6e518283d07985b18d479a8f03c5c3f20015c6582538def18a`  
		Last Modified: Fri, 06 May 2022 01:06:14 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f91204882744da81d33ffcfc2d335958d94620b343be39e566107e354d4f2b9`  
		Last Modified: Fri, 06 May 2022 01:06:15 GMT  
		Size: 5.6 MB (5627862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b3c5e562a2e32c0984910ea2a31cbc0ebf70cfd1f0df3daca43466587ac161`  
		Last Modified: Fri, 06 May 2022 01:06:14 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2496335307234f487bccec5dd92b220fd206a951193aaaa8a893358ed5b3658`  
		Last Modified: Fri, 06 May 2022 01:06:14 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db8c9d2946bfc3596ae37b6aae0f362c1743c06274f0580f1d28bd048a53f44`  
		Last Modified: Fri, 06 May 2022 01:06:14 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:37f2f429ef0f26e10ce0ffd80eb1db04075cc655e4ade968934feb015c81a5e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8660466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9890bfefc0e3351b820e016a71a528d1956569ab2df6944908ad9a909472f22`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:44 GMT
ADD file:c1616ef1514518ef1f90874b6fab7c42951a5736600b54942fd4ad4338a24b11 in / 
# Mon, 04 Apr 2022 23:38:44 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 01:53:33 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 01:53:34 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 01:53:35 GMT
ENV INSTALLDIR=/notary/server
# Fri, 06 May 2022 01:53:36 GMT
EXPOSE 4443
# Fri, 06 May 2022 01:53:37 GMT
WORKDIR /notary/server
# Fri, 06 May 2022 01:53:52 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --version
# Fri, 06 May 2022 01:53:54 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Fri, 06 May 2022 01:53:55 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Fri, 06 May 2022 01:53:55 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 01:53:56 GMT
USER notary
# Fri, 06 May 2022 01:53:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Fri, 06 May 2022 01:53:58 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 01:53:59 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:6f153ea7cf9623ea20df5792c26f8dfd80af131fecab00e40983e554e495421e`  
		Last Modified: Mon, 04 Apr 2022 23:39:57 GMT  
		Size: 2.8 MB (2798126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480520f3392b90043910d7268b537ecd1659ddbb5cb29c5adf77c88fef47d65a`  
		Last Modified: Fri, 06 May 2022 01:54:47 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00018550dcea7efab5be15d233fd261496846d3a597e4f07175aefc34a746117`  
		Last Modified: Fri, 06 May 2022 01:54:48 GMT  
		Size: 5.9 MB (5860251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddfb2fc3b62b892c8667daec55783ef3d63453ab4563b516c177934fcb49572`  
		Last Modified: Fri, 06 May 2022 01:54:47 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69e20ab1fa4892eca94c25948de9a1fdc3330ab23f1efffc98693352ee04fa5`  
		Last Modified: Fri, 06 May 2022 01:54:47 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c545d4343d941bfd383dd6acff9bdf6431eef4e14113eb33d31225edfe550c`  
		Last Modified: Fri, 06 May 2022 01:54:47 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:bae576e49f3c5ac60baf81b0cd47f6c7e292e3c1a2cc8b081d846e0cda62a5b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8348451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0495e05e0d7e4df038032361130b3a554797bc2a511c2c618a8890b845f212d3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 05 Apr 2022 00:24:09 GMT
ADD file:53d4ef78df099d878ecfe359308c0a3ee650850966fefbe1fd7c05f3b2d89e1b in / 
# Tue, 05 Apr 2022 00:24:11 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 01:48:47 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 01:48:49 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 01:48:53 GMT
ENV INSTALLDIR=/notary/server
# Fri, 06 May 2022 01:48:55 GMT
EXPOSE 4443
# Fri, 06 May 2022 01:49:00 GMT
WORKDIR /notary/server
# Fri, 06 May 2022 01:49:48 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-server;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-server ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-server --version
# Fri, 06 May 2022 01:49:50 GMT
COPY file:33643ab6368f7007610a81abd5ef291ec43cbd47a0d1581b29490690dc44f709 in . 
# Fri, 06 May 2022 01:49:52 GMT
COPY file:ad1ab25ac8ceb29f1cdc7363c26c083887d76bdbd37db998baad09873ef0811e in . 
# Fri, 06 May 2022 01:49:57 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 01:50:01 GMT
USER notary
# Fri, 06 May 2022 01:50:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Fri, 06 May 2022 01:50:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 01:50:17 GMT
CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:57c1475d5a6dc8e68a1b09bd09db22cc33e8f163a3841ce5100e0569acefcabe`  
		Last Modified: Tue, 05 Apr 2022 00:25:31 GMT  
		Size: 2.8 MB (2806745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d113a2296216ff0801eaaa23faf16370c503b4070e9895dd7788112939579b`  
		Last Modified: Fri, 06 May 2022 01:53:18 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9969d0f4c7adddcdbd67e584df60bb9ef69365671ae03723b39dc9807ffb8f71`  
		Last Modified: Fri, 06 May 2022 01:53:19 GMT  
		Size: 5.5 MB (5539583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4601a5f5eccd51d842fb5c837594b84c44958c2d40ad210aa02f774d8ce2d99c`  
		Last Modified: Fri, 06 May 2022 01:53:18 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfede6060e49c4ea18bb60fce541803e16bc21a163f2c7bd1e0d65273ea9ca2`  
		Last Modified: Fri, 06 May 2022 01:53:18 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fe6431b53b4dcf01fbf89da7c8ab80fbd68973c9ed96993ba18843a532afe9`  
		Last Modified: Fri, 06 May 2022 01:53:18 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:server-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:5f0d8363d713d58005c200e30235ebbad1efd30d126fa6e8b921bef23dc549f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7560845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa0f87211b3a607ac91983abd06c400f17981935a09b074bcf4e6fa517d0a55`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-server","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:21:39 GMT
RUN RUN /bin/sh -c adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:21:39 GMT
RUN EXPOSE map[4443/tcp:{}]
# Tue, 25 Oct 2022 01:21:39 GMT
RUN ENV INSTALLDIR=/notary/server
# Tue, 25 Oct 2022 01:21:39 GMT
RUN ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/server
# Tue, 25 Oct 2022 01:21:39 GMT
RUN WORKDIR /notary/server
# Tue, 25 Oct 2022 01:22:02 GMT
RUN COPY /notary-server ./ # buildkit
# Tue, 25 Oct 2022 01:22:02 GMT
RUN RUN /bin/sh -c ./notary-server --version # buildkit
# Tue, 25 Oct 2022 01:22:02 GMT
RUN COPY ./server-config.json . # buildkit
# Tue, 25 Oct 2022 01:22:02 GMT
RUN COPY ./entrypoint.sh . # buildkit
# Tue, 25 Oct 2022 01:22:02 GMT
RUN USER notary
# Tue, 25 Oct 2022 01:22:02 GMT
RUN ENTRYPOINT ["entrypoint.sh"]
# Tue, 25 Oct 2022 01:22:02 GMT
RUN CMD ["notary-server" "--version"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e57b7c2a2dbd108e38c96fd7b110170d3b57a921f34c3b015736a93b17e5ad`  
		Last Modified: Tue, 25 Oct 2022 01:22:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb73212e82f7d46920138e024d3233301bdffa778ba147338014ae69d65ba43c`  
		Last Modified: Tue, 25 Oct 2022 01:22:33 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6932c1633389acd33f1d9f659c505be3568406222966cef27e8ba12b8e99f2`  
		Last Modified: Tue, 25 Oct 2022 01:22:34 GMT  
		Size: 5.0 MB (4968022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8343a44b4f6777d4568e22ad69163d4b47cfd5210a1bd7d7b8299f0375980b1c`  
		Last Modified: Tue, 25 Oct 2022 01:22:33 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35439890b4d9dfb792c63c9afbed662ba45d800f8fd549997b8d5bd1952a4c86`  
		Last Modified: Tue, 25 Oct 2022 01:22:33 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9b2fbcdeb33d0cf5ed9e7962b4e280767c894054d34bc8e0de779a5f39e634`  
		Last Modified: Tue, 25 Oct 2022 01:22:33 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:signer`

```console
$ docker pull notary@sha256:ffc8077159f18d31646f1dc1160efe26033ed620b1123428cbdaf8589ec03409
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
$ docker pull notary@sha256:435522136a07d4f5dca5036914d6c54642cb17fd1d0b86badc786a4a49db3a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7564780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b034bbaca404162659e59fa203570e78de7572f824a237b851946962f34282`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:52:21 GMT
RUN RUN /bin/sh -c adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:52:46 GMT
RUN EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 01:52:46 GMT
RUN EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 01:52:46 GMT
RUN ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 01:52:46 GMT
RUN ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 01:52:46 GMT
RUN WORKDIR /notary/signer
# Tue, 25 Oct 2022 01:52:46 GMT
RUN COPY /notary-signer ./ # buildkit
# Tue, 25 Oct 2022 01:52:47 GMT
RUN RUN /bin/sh -c ./notary-signer --version # buildkit
# Tue, 25 Oct 2022 01:52:47 GMT
RUN COPY ./signer-config.json . # buildkit
# Tue, 25 Oct 2022 01:52:47 GMT
RUN COPY ./entrypoint.sh . # buildkit
# Tue, 25 Oct 2022 01:52:47 GMT
RUN USER notary
# Tue, 25 Oct 2022 01:52:47 GMT
RUN ENTRYPOINT ["entrypoint.sh"]
# Tue, 25 Oct 2022 01:52:47 GMT
RUN CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ae0db85ee62912972b015b43b47b5849f5b66900a08ad146a42f7c16d02def`  
		Last Modified: Tue, 25 Oct 2022 01:53:00 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc4162474250e31d2a4a4d6cd0a4f0e9813709d78b77293938ace79068cf662`  
		Last Modified: Tue, 25 Oct 2022 01:53:10 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ee735c69980c01445ef5036153b011dcdd76875748196eaa8d8775508450ae`  
		Last Modified: Tue, 25 Oct 2022 01:53:11 GMT  
		Size: 4.8 MB (4756567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d68484c344b8650efe9be82c4354b43b79c802c8d9bf93722123e5c3881b9f`  
		Last Modified: Tue, 25 Oct 2022 01:53:10 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f7ed463735c7515ccf5e53f9f11ecb965c358c3c62eb0be96ff7994687582b`  
		Last Modified: Tue, 25 Oct 2022 01:53:10 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6bf69440a2a92b3633d1651c79e0a62ee6db216c30dc6cafdb0f995dba1871`  
		Last Modified: Tue, 25 Oct 2022 01:53:10 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm variant v6

```console
$ docker pull notary@sha256:ecc9599c6083d660954554c662039feba162e63849b27526878b778b1a20d76e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7832442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3946c21e7d54f760243b7fe6da3fa1f3e09a59649bf464ad052c616407f7efc`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:18 GMT
ADD file:a62ad8c2b01195a2d42109e23b6d8ce69e2a816702518b2d823139f28c0ff799 in / 
# Mon, 04 Apr 2022 23:50:19 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 02:05:11 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 02:05:11 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 02:05:55 GMT
ENV INSTALLDIR=/notary/signer
# Fri, 06 May 2022 02:05:55 GMT
EXPOSE 4444
# Fri, 06 May 2022 02:05:55 GMT
EXPOSE 7899
# Fri, 06 May 2022 02:05:56 GMT
WORKDIR /notary/signer
# Fri, 06 May 2022 02:06:20 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --version
# Fri, 06 May 2022 02:06:21 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Fri, 06 May 2022 02:06:21 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Fri, 06 May 2022 02:06:23 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 02:06:23 GMT
USER notary
# Fri, 06 May 2022 02:06:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Fri, 06 May 2022 02:06:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 02:06:25 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:6c4809594a4b80d650b9951499cc7be9a90fc7b306e1dd8052f821b60733ae0c`  
		Last Modified: Mon, 04 Apr 2022 23:52:09 GMT  
		Size: 2.6 MB (2605389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97413f849b39c68cf917253d769bfb48a252f9a5bfbae0bea43eef9dbbba6faf`  
		Last Modified: Fri, 06 May 2022 02:07:10 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391b456a9486091521ee65ecf7b8e9a5137eb9e6f3812873383016b612e4e0af`  
		Last Modified: Fri, 06 May 2022 02:07:14 GMT  
		Size: 5.2 MB (5224994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a57ee2bed83f59845981c57d3e90a8738c1b5639c2007a1b9092a81a5eac0`  
		Last Modified: Fri, 06 May 2022 02:07:10 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82410eb437488395040d7b0b4553beb7b1ca392267473dfbc4dd3464e6213846`  
		Last Modified: Fri, 06 May 2022 02:07:11 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d33fb84c26d75e7d4b61c2bc1209a34c90463e06b2abef8f24d9e80f26ca3e0`  
		Last Modified: Fri, 06 May 2022 02:07:10 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:7a9a154671aae54e66ae934eda9d351a9f0e94e6f6051e25152fd89557207154
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7841091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cef4bf442a1e88d5a920d55d9dd600f99ba2784e4c81a33821ceb0ec4220c6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:53 GMT
ADD file:a2a992b7f6af1e6f8f5648f329f4a4058d8c4377417ac23ae211290c0cdc8f4b in / 
# Mon, 04 Apr 2022 23:39:53 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 01:04:59 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 01:05:00 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 01:05:31 GMT
ENV INSTALLDIR=/notary/signer
# Fri, 06 May 2022 01:05:31 GMT
EXPOSE 4444
# Fri, 06 May 2022 01:05:32 GMT
EXPOSE 7899
# Fri, 06 May 2022 01:05:33 GMT
WORKDIR /notary/signer
# Fri, 06 May 2022 01:05:46 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --version
# Fri, 06 May 2022 01:05:48 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Fri, 06 May 2022 01:05:49 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Fri, 06 May 2022 01:05:49 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 01:05:50 GMT
USER notary
# Fri, 06 May 2022 01:05:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Fri, 06 May 2022 01:05:52 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 01:05:53 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:0eeab5c200691bd777e227c6eea27f7ca3c8232b67118a76edac2dcde3186aa1`  
		Last Modified: Mon, 04 Apr 2022 23:41:02 GMT  
		Size: 2.7 MB (2716243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cf437e97bb18b23e8738bd6a0b24c57c968229af758dedf8b88b43bfa29d71`  
		Last Modified: Fri, 06 May 2022 01:06:26 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8de63c68835afb5132d090b373b5f01a96af21d75898f7d83c864542cfda612`  
		Last Modified: Fri, 06 May 2022 01:06:27 GMT  
		Size: 5.1 MB (5122824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addcd789570140c19b150e5762cf103cae080a8afe76d68fef8343278994ba36`  
		Last Modified: Fri, 06 May 2022 01:06:26 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5183beb303d6ceff1b263a554d7672189d3c9289feb6ab244e1927a892d16ae`  
		Last Modified: Fri, 06 May 2022 01:06:26 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a0736d73a7eab449dff23e209e70596bfb2cbaecb420c43af812eb10d5cec`  
		Last Modified: Fri, 06 May 2022 01:06:26 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; 386

```console
$ docker pull notary@sha256:3bf2e3e5f997f20c914c26a7cf8e8df4722b7360fd4ec45837a1d26efeb50da8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8140731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31a389c769d279bad2efe63a14376da2e2c1e974aac94ce7d03ace8db49a4d7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:44 GMT
ADD file:c1616ef1514518ef1f90874b6fab7c42951a5736600b54942fd4ad4338a24b11 in / 
# Mon, 04 Apr 2022 23:38:44 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 01:53:33 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 01:53:34 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 01:54:04 GMT
ENV INSTALLDIR=/notary/signer
# Fri, 06 May 2022 01:54:05 GMT
EXPOSE 4444
# Fri, 06 May 2022 01:54:06 GMT
EXPOSE 7899
# Fri, 06 May 2022 01:54:07 GMT
WORKDIR /notary/signer
# Fri, 06 May 2022 01:54:20 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --version
# Fri, 06 May 2022 01:54:22 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Fri, 06 May 2022 01:54:23 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Fri, 06 May 2022 01:54:23 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 01:54:24 GMT
USER notary
# Fri, 06 May 2022 01:54:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Fri, 06 May 2022 01:54:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 01:54:27 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:6f153ea7cf9623ea20df5792c26f8dfd80af131fecab00e40983e554e495421e`  
		Last Modified: Mon, 04 Apr 2022 23:39:57 GMT  
		Size: 2.8 MB (2798126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9771b285e704a9bcfed3caf1883e833870862183e8e96a407ea0e7f22ebacc39`  
		Last Modified: Fri, 06 May 2022 01:54:58 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e40381195b49324230c92a904af28546b44616df3c2b304a3063338f61e946`  
		Last Modified: Fri, 06 May 2022 01:54:59 GMT  
		Size: 5.3 MB (5340578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2278e8233aaa0be43027a19ccdec3ad0a653158c3c66ba7f4fb4d35bd199b380`  
		Last Modified: Fri, 06 May 2022 01:54:58 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6fc02ebfb9b86df12f26ab0aeb99c4d823e9c0db6452495eaade43b9ba9b15`  
		Last Modified: Fri, 06 May 2022 01:54:58 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b53293a74204d6f4cb670ed5ca76b6b009700011c785dffb863d982a793021`  
		Last Modified: Fri, 06 May 2022 01:54:58 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; ppc64le

```console
$ docker pull notary@sha256:f9e05866c3f37b70a1ca602fa70173f3bcf428b70b9f5423d342bec7ee19dd53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7850404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974555b30dc83be4d8f3540998769870dd78f8a8fc7cacf1f1c7cce357210d74`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 05 Apr 2022 00:24:09 GMT
ADD file:53d4ef78df099d878ecfe359308c0a3ee650850966fefbe1fd7c05f3b2d89e1b in / 
# Tue, 05 Apr 2022 00:24:11 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 01:48:47 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 01:48:49 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 01:50:42 GMT
ENV INSTALLDIR=/notary/signer
# Fri, 06 May 2022 01:50:48 GMT
EXPOSE 4444
# Fri, 06 May 2022 01:50:54 GMT
EXPOSE 7899
# Fri, 06 May 2022 01:51:03 GMT
WORKDIR /notary/signer
# Fri, 06 May 2022 01:52:07 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --version
# Fri, 06 May 2022 01:52:11 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Fri, 06 May 2022 01:52:12 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Fri, 06 May 2022 01:52:21 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 01:52:27 GMT
USER notary
# Fri, 06 May 2022 01:52:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Fri, 06 May 2022 01:52:35 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 01:52:45 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:57c1475d5a6dc8e68a1b09bd09db22cc33e8f163a3841ce5100e0569acefcabe`  
		Last Modified: Tue, 05 Apr 2022 00:25:31 GMT  
		Size: 2.8 MB (2806745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eb2f6a2acaca474fa57ed221c8af545cb3427bac48728f5c70f290aa41bd6b`  
		Last Modified: Fri, 06 May 2022 01:53:32 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7742f817347981ecc0a3f52f67d4ceab6bf4efa2500da0ba0374f3f05b13090e`  
		Last Modified: Fri, 06 May 2022 01:53:33 GMT  
		Size: 5.0 MB (5041595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920db4815a208e2208166e0eba0142dd5b1482e797804a0ee3f73073b1dd9831`  
		Last Modified: Fri, 06 May 2022 01:53:32 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5ae35dd84126fb8dd98d4f50f77ae759328e7ce783394b59439efe31a25057`  
		Last Modified: Fri, 06 May 2022 01:53:33 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153896dbbb4d18a59a23b52989f2d3b868c82a9a0915a5c3b3fda53ccc195c73`  
		Last Modified: Fri, 06 May 2022 01:53:32 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer` - linux; s390x

```console
$ docker pull notary@sha256:db12a82c9b66296e5ed9c95a15ed0b7ffd4e7df3ff1f755674065c0828e78762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079db5b5438125037c313d032802e63377417286edfc666e1572380b504ac40e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:21:39 GMT
RUN RUN /bin/sh -c adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:22:14 GMT
RUN EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 01:22:14 GMT
RUN EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 01:22:14 GMT
RUN ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 01:22:14 GMT
RUN ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 01:22:14 GMT
RUN WORKDIR /notary/signer
# Tue, 25 Oct 2022 01:22:14 GMT
RUN COPY /notary-signer ./ # buildkit
# Tue, 25 Oct 2022 01:22:14 GMT
RUN RUN /bin/sh -c ./notary-signer --version # buildkit
# Tue, 25 Oct 2022 01:22:14 GMT
RUN COPY ./signer-config.json . # buildkit
# Tue, 25 Oct 2022 01:22:14 GMT
RUN COPY ./entrypoint.sh . # buildkit
# Tue, 25 Oct 2022 01:22:14 GMT
RUN USER notary
# Tue, 25 Oct 2022 01:22:14 GMT
RUN ENTRYPOINT ["entrypoint.sh"]
# Tue, 25 Oct 2022 01:22:14 GMT
RUN CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e57b7c2a2dbd108e38c96fd7b110170d3b57a921f34c3b015736a93b17e5ad`  
		Last Modified: Tue, 25 Oct 2022 01:22:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc551ab4c025f7c0eea7a8a1e22a13f7c353f3db3a08e4cae43a782e73d9b89a`  
		Last Modified: Tue, 25 Oct 2022 01:22:40 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914ee92749a07541df36795929204e1db4dde0af26dbffebcd68c5280d62380c`  
		Last Modified: Tue, 25 Oct 2022 01:22:41 GMT  
		Size: 4.6 MB (4601261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337c5b8b7050aa5b72729655bbe4b7cebfe80b809f416bc9975de2c4024c81ce`  
		Last Modified: Tue, 25 Oct 2022 01:22:40 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0bfe5e7ce871451593a461f32f992f2ed637f9bcedf2a46624e62da2d1b4aa`  
		Last Modified: Tue, 25 Oct 2022 01:22:40 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced1e547d1f2398fd325b348d5c6bf9f71864266123f6eb5cd293c199a3f5e35`  
		Last Modified: Tue, 25 Oct 2022 01:22:40 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:ffc8077159f18d31646f1dc1160efe26033ed620b1123428cbdaf8589ec03409
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
$ docker pull notary@sha256:435522136a07d4f5dca5036914d6c54642cb17fd1d0b86badc786a4a49db3a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7564780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b034bbaca404162659e59fa203570e78de7572f824a237b851946962f34282`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:52:21 GMT
RUN RUN /bin/sh -c adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:52:46 GMT
RUN EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 01:52:46 GMT
RUN EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 01:52:46 GMT
RUN ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 01:52:46 GMT
RUN ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 01:52:46 GMT
RUN WORKDIR /notary/signer
# Tue, 25 Oct 2022 01:52:46 GMT
RUN COPY /notary-signer ./ # buildkit
# Tue, 25 Oct 2022 01:52:47 GMT
RUN RUN /bin/sh -c ./notary-signer --version # buildkit
# Tue, 25 Oct 2022 01:52:47 GMT
RUN COPY ./signer-config.json . # buildkit
# Tue, 25 Oct 2022 01:52:47 GMT
RUN COPY ./entrypoint.sh . # buildkit
# Tue, 25 Oct 2022 01:52:47 GMT
RUN USER notary
# Tue, 25 Oct 2022 01:52:47 GMT
RUN ENTRYPOINT ["entrypoint.sh"]
# Tue, 25 Oct 2022 01:52:47 GMT
RUN CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ae0db85ee62912972b015b43b47b5849f5b66900a08ad146a42f7c16d02def`  
		Last Modified: Tue, 25 Oct 2022 01:53:00 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc4162474250e31d2a4a4d6cd0a4f0e9813709d78b77293938ace79068cf662`  
		Last Modified: Tue, 25 Oct 2022 01:53:10 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ee735c69980c01445ef5036153b011dcdd76875748196eaa8d8775508450ae`  
		Last Modified: Tue, 25 Oct 2022 01:53:11 GMT  
		Size: 4.8 MB (4756567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d68484c344b8650efe9be82c4354b43b79c802c8d9bf93722123e5c3881b9f`  
		Last Modified: Tue, 25 Oct 2022 01:53:10 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f7ed463735c7515ccf5e53f9f11ecb965c358c3c62eb0be96ff7994687582b`  
		Last Modified: Tue, 25 Oct 2022 01:53:10 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6bf69440a2a92b3633d1651c79e0a62ee6db216c30dc6cafdb0f995dba1871`  
		Last Modified: Tue, 25 Oct 2022 01:53:10 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:ecc9599c6083d660954554c662039feba162e63849b27526878b778b1a20d76e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7832442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3946c21e7d54f760243b7fe6da3fa1f3e09a59649bf464ad052c616407f7efc`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 04 Apr 2022 23:50:18 GMT
ADD file:a62ad8c2b01195a2d42109e23b6d8ce69e2a816702518b2d823139f28c0ff799 in / 
# Mon, 04 Apr 2022 23:50:19 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 02:05:11 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 02:05:11 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 02:05:55 GMT
ENV INSTALLDIR=/notary/signer
# Fri, 06 May 2022 02:05:55 GMT
EXPOSE 4444
# Fri, 06 May 2022 02:05:55 GMT
EXPOSE 7899
# Fri, 06 May 2022 02:05:56 GMT
WORKDIR /notary/signer
# Fri, 06 May 2022 02:06:20 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --version
# Fri, 06 May 2022 02:06:21 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Fri, 06 May 2022 02:06:21 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Fri, 06 May 2022 02:06:23 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 02:06:23 GMT
USER notary
# Fri, 06 May 2022 02:06:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Fri, 06 May 2022 02:06:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 02:06:25 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:6c4809594a4b80d650b9951499cc7be9a90fc7b306e1dd8052f821b60733ae0c`  
		Last Modified: Mon, 04 Apr 2022 23:52:09 GMT  
		Size: 2.6 MB (2605389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97413f849b39c68cf917253d769bfb48a252f9a5bfbae0bea43eef9dbbba6faf`  
		Last Modified: Fri, 06 May 2022 02:07:10 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391b456a9486091521ee65ecf7b8e9a5137eb9e6f3812873383016b612e4e0af`  
		Last Modified: Fri, 06 May 2022 02:07:14 GMT  
		Size: 5.2 MB (5224994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668a57ee2bed83f59845981c57d3e90a8738c1b5639c2007a1b9092a81a5eac0`  
		Last Modified: Fri, 06 May 2022 02:07:10 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82410eb437488395040d7b0b4553beb7b1ca392267473dfbc4dd3464e6213846`  
		Last Modified: Fri, 06 May 2022 02:07:11 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d33fb84c26d75e7d4b61c2bc1209a34c90463e06b2abef8f24d9e80f26ca3e0`  
		Last Modified: Fri, 06 May 2022 02:07:10 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:7a9a154671aae54e66ae934eda9d351a9f0e94e6f6051e25152fd89557207154
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7841091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cef4bf442a1e88d5a920d55d9dd600f99ba2784e4c81a33821ceb0ec4220c6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:53 GMT
ADD file:a2a992b7f6af1e6f8f5648f329f4a4058d8c4377417ac23ae211290c0cdc8f4b in / 
# Mon, 04 Apr 2022 23:39:53 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 01:04:59 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 01:05:00 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 01:05:31 GMT
ENV INSTALLDIR=/notary/signer
# Fri, 06 May 2022 01:05:31 GMT
EXPOSE 4444
# Fri, 06 May 2022 01:05:32 GMT
EXPOSE 7899
# Fri, 06 May 2022 01:05:33 GMT
WORKDIR /notary/signer
# Fri, 06 May 2022 01:05:46 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --version
# Fri, 06 May 2022 01:05:48 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Fri, 06 May 2022 01:05:49 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Fri, 06 May 2022 01:05:49 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 01:05:50 GMT
USER notary
# Fri, 06 May 2022 01:05:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Fri, 06 May 2022 01:05:52 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 01:05:53 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:0eeab5c200691bd777e227c6eea27f7ca3c8232b67118a76edac2dcde3186aa1`  
		Last Modified: Mon, 04 Apr 2022 23:41:02 GMT  
		Size: 2.7 MB (2716243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cf437e97bb18b23e8738bd6a0b24c57c968229af758dedf8b88b43bfa29d71`  
		Last Modified: Fri, 06 May 2022 01:06:26 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8de63c68835afb5132d090b373b5f01a96af21d75898f7d83c864542cfda612`  
		Last Modified: Fri, 06 May 2022 01:06:27 GMT  
		Size: 5.1 MB (5122824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addcd789570140c19b150e5762cf103cae080a8afe76d68fef8343278994ba36`  
		Last Modified: Fri, 06 May 2022 01:06:26 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5183beb303d6ceff1b263a554d7672189d3c9289feb6ab244e1927a892d16ae`  
		Last Modified: Fri, 06 May 2022 01:06:26 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a0736d73a7eab449dff23e209e70596bfb2cbaecb420c43af812eb10d5cec`  
		Last Modified: Fri, 06 May 2022 01:06:26 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:3bf2e3e5f997f20c914c26a7cf8e8df4722b7360fd4ec45837a1d26efeb50da8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8140731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31a389c769d279bad2efe63a14376da2e2c1e974aac94ce7d03ace8db49a4d7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:44 GMT
ADD file:c1616ef1514518ef1f90874b6fab7c42951a5736600b54942fd4ad4338a24b11 in / 
# Mon, 04 Apr 2022 23:38:44 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 01:53:33 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 01:53:34 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 01:54:04 GMT
ENV INSTALLDIR=/notary/signer
# Fri, 06 May 2022 01:54:05 GMT
EXPOSE 4444
# Fri, 06 May 2022 01:54:06 GMT
EXPOSE 7899
# Fri, 06 May 2022 01:54:07 GMT
WORKDIR /notary/signer
# Fri, 06 May 2022 01:54:20 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --version
# Fri, 06 May 2022 01:54:22 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Fri, 06 May 2022 01:54:23 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Fri, 06 May 2022 01:54:23 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 01:54:24 GMT
USER notary
# Fri, 06 May 2022 01:54:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Fri, 06 May 2022 01:54:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 01:54:27 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:6f153ea7cf9623ea20df5792c26f8dfd80af131fecab00e40983e554e495421e`  
		Last Modified: Mon, 04 Apr 2022 23:39:57 GMT  
		Size: 2.8 MB (2798126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9771b285e704a9bcfed3caf1883e833870862183e8e96a407ea0e7f22ebacc39`  
		Last Modified: Fri, 06 May 2022 01:54:58 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e40381195b49324230c92a904af28546b44616df3c2b304a3063338f61e946`  
		Last Modified: Fri, 06 May 2022 01:54:59 GMT  
		Size: 5.3 MB (5340578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2278e8233aaa0be43027a19ccdec3ad0a653158c3c66ba7f4fb4d35bd199b380`  
		Last Modified: Fri, 06 May 2022 01:54:58 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6fc02ebfb9b86df12f26ab0aeb99c4d823e9c0db6452495eaade43b9ba9b15`  
		Last Modified: Fri, 06 May 2022 01:54:58 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b53293a74204d6f4cb670ed5ca76b6b009700011c785dffb863d982a793021`  
		Last Modified: Fri, 06 May 2022 01:54:58 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:f9e05866c3f37b70a1ca602fa70173f3bcf428b70b9f5423d342bec7ee19dd53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7850404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974555b30dc83be4d8f3540998769870dd78f8a8fc7cacf1f1c7cce357210d74`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 05 Apr 2022 00:24:09 GMT
ADD file:53d4ef78df099d878ecfe359308c0a3ee650850966fefbe1fd7c05f3b2d89e1b in / 
# Tue, 05 Apr 2022 00:24:11 GMT
CMD ["/bin/sh"]
# Fri, 06 May 2022 01:48:47 GMT
ENV TAG=v0.7.0
# Fri, 06 May 2022 01:48:49 GMT
ENV NOTARYPKG=github.com/theupdateframework/notary
# Fri, 06 May 2022 01:50:42 GMT
ENV INSTALLDIR=/notary/signer
# Fri, 06 May 2022 01:50:48 GMT
EXPOSE 4444
# Fri, 06 May 2022 01:50:54 GMT
EXPOSE 7899
# Fri, 06 May 2022 01:51:03 GMT
WORKDIR /notary/signer
# Fri, 06 May 2022 01:52:07 GMT
RUN set -eux;     apk add --no-cache --virtual build-deps git go make musl-dev;     export GOPATH=/go GOCACHE=/go/cache;     mkdir -p ${GOPATH}/src/${NOTARYPKG};     git clone -b ${TAG} --depth 1 https://${NOTARYPKG} ${GOPATH}/src/${NOTARYPKG};     make -C ${GOPATH}/src/${NOTARYPKG} SKIPENVCHECK=1 PREFIX=. ./bin/static/notary-signer;     cp -vL ${GOPATH}/src/${NOTARYPKG}/bin/static/notary-signer ./;     apk del --no-network build-deps;     rm -rf ${GOPATH};     ./notary-signer --version
# Fri, 06 May 2022 01:52:11 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Fri, 06 May 2022 01:52:12 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Fri, 06 May 2022 01:52:21 GMT
RUN adduser -D -H -g "" notary
# Fri, 06 May 2022 01:52:27 GMT
USER notary
# Fri, 06 May 2022 01:52:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Fri, 06 May 2022 01:52:35 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 May 2022 01:52:45 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:57c1475d5a6dc8e68a1b09bd09db22cc33e8f163a3841ce5100e0569acefcabe`  
		Last Modified: Tue, 05 Apr 2022 00:25:31 GMT  
		Size: 2.8 MB (2806745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eb2f6a2acaca474fa57ed221c8af545cb3427bac48728f5c70f290aa41bd6b`  
		Last Modified: Fri, 06 May 2022 01:53:32 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7742f817347981ecc0a3f52f67d4ceab6bf4efa2500da0ba0374f3f05b13090e`  
		Last Modified: Fri, 06 May 2022 01:53:33 GMT  
		Size: 5.0 MB (5041595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920db4815a208e2208166e0eba0142dd5b1482e797804a0ee3f73073b1dd9831`  
		Last Modified: Fri, 06 May 2022 01:53:32 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5ae35dd84126fb8dd98d4f50f77ae759328e7ce783394b59439efe31a25057`  
		Last Modified: Fri, 06 May 2022 01:53:33 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153896dbbb4d18a59a23b52989f2d3b868c82a9a0915a5c3b3fda53ccc195c73`  
		Last Modified: Fri, 06 May 2022 01:53:32 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:db12a82c9b66296e5ed9c95a15ed0b7ffd4e7df3ff1f755674065c0828e78762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079db5b5438125037c313d032802e63377417286edfc666e1572380b504ac40e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 01:21:39 GMT
RUN RUN /bin/sh -c adduser -D -H -g "" notary # buildkit
# Tue, 25 Oct 2022 01:22:14 GMT
RUN EXPOSE map[4444/tcp:{}]
# Tue, 25 Oct 2022 01:22:14 GMT
RUN EXPOSE map[7899/tcp:{}]
# Tue, 25 Oct 2022 01:22:14 GMT
RUN ENV INSTALLDIR=/notary/signer
# Tue, 25 Oct 2022 01:22:14 GMT
RUN ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Tue, 25 Oct 2022 01:22:14 GMT
RUN WORKDIR /notary/signer
# Tue, 25 Oct 2022 01:22:14 GMT
RUN COPY /notary-signer ./ # buildkit
# Tue, 25 Oct 2022 01:22:14 GMT
RUN RUN /bin/sh -c ./notary-signer --version # buildkit
# Tue, 25 Oct 2022 01:22:14 GMT
RUN COPY ./signer-config.json . # buildkit
# Tue, 25 Oct 2022 01:22:14 GMT
RUN COPY ./entrypoint.sh . # buildkit
# Tue, 25 Oct 2022 01:22:14 GMT
RUN USER notary
# Tue, 25 Oct 2022 01:22:14 GMT
RUN ENTRYPOINT ["entrypoint.sh"]
# Tue, 25 Oct 2022 01:22:14 GMT
RUN CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e57b7c2a2dbd108e38c96fd7b110170d3b57a921f34c3b015736a93b17e5ad`  
		Last Modified: Tue, 25 Oct 2022 01:22:34 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc551ab4c025f7c0eea7a8a1e22a13f7c353f3db3a08e4cae43a782e73d9b89a`  
		Last Modified: Tue, 25 Oct 2022 01:22:40 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914ee92749a07541df36795929204e1db4dde0af26dbffebcd68c5280d62380c`  
		Last Modified: Tue, 25 Oct 2022 01:22:41 GMT  
		Size: 4.6 MB (4601261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337c5b8b7050aa5b72729655bbe4b7cebfe80b809f416bc9975de2c4024c81ce`  
		Last Modified: Tue, 25 Oct 2022 01:22:40 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0bfe5e7ce871451593a461f32f992f2ed637f9bcedf2a46624e62da2d1b4aa`  
		Last Modified: Tue, 25 Oct 2022 01:22:40 GMT  
		Size: 351.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced1e547d1f2398fd325b348d5c6bf9f71864266123f6eb5cd293c199a3f5e35`  
		Last Modified: Tue, 25 Oct 2022 01:22:40 GMT  
		Size: 376.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
