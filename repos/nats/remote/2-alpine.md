## `nats:2-alpine`

```console
$ docker pull nats@sha256:c6d778a0df2aeeec2399f1e1ce558d7b65e70adc7ef5ca13f2cf06b1f7654a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:d6a47f89f52342be07d213d493e0b71a80fc94ccc19edc9c8b17169e8d887fbe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9494811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18e20b07c9925b57a0846b64bffdab236ff0d02728bea2661094cb2f1088d89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Mon, 09 Oct 2023 23:20:15 GMT
ENV NATS_SERVER=2.10.2
# Mon, 09 Oct 2023 23:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='26b3816709136a8d061e5147cfb217abb577d1fd79e08689417c9b0fa2806533' ;; 		armhf) natsArch='arm6'; sha256='189131c2b890446d88b508cc7e8aa937c38fef81dbd3f4b4d3d205af41edb5ab' ;; 		armv7) natsArch='arm7'; sha256='33374ac52531ac0a8c57c2f111d098eb99c42120fedfad57317817e6d48d70d2' ;; 		x86_64) natsArch='amd64'; sha256='8929b053d2dca2b62756982951c51147b69be984b55a7a850affa86a66c6bfc9' ;; 		x86) natsArch='386'; sha256='b11c6bded174332b3fc88ac40c3632448d58e8d58dc92551d9655407ce0107e8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 09 Oct 2023 23:20:17 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 09 Oct 2023 23:20:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 09 Oct 2023 23:20:17 GMT
EXPOSE 4222 6222 8222
# Mon, 09 Oct 2023 23:20:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Oct 2023 23:20:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793ee3203ddeae4265feedfeeb0176c5d046487786e6430ec414b466b7342687`  
		Last Modified: Mon, 09 Oct 2023 23:21:01 GMT  
		Size: 6.1 MB (6091846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dd902fefeb39726cbb9025e935fabe591af4d39f448ddad514c70eb56a6002`  
		Last Modified: Mon, 09 Oct 2023 23:21:00 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7a1bcf5bcb5ad0317a82f43795966d7b0cf297054e112bc548fe8d0c881df9`  
		Last Modified: Mon, 09 Oct 2023 23:21:00 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6d9d5fd5f91a7c3e45e2cac23df6f50393e2024ea69495d9233df8ba9503bdc8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8958058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11708ece1d9ad1b7baf64c1f3c5e3b7a38ef5d66e87c24ba859eb6272bc2694f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Mon, 09 Oct 2023 23:49:18 GMT
ENV NATS_SERVER=2.10.2
# Mon, 09 Oct 2023 23:49:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='26b3816709136a8d061e5147cfb217abb577d1fd79e08689417c9b0fa2806533' ;; 		armhf) natsArch='arm6'; sha256='189131c2b890446d88b508cc7e8aa937c38fef81dbd3f4b4d3d205af41edb5ab' ;; 		armv7) natsArch='arm7'; sha256='33374ac52531ac0a8c57c2f111d098eb99c42120fedfad57317817e6d48d70d2' ;; 		x86_64) natsArch='amd64'; sha256='8929b053d2dca2b62756982951c51147b69be984b55a7a850affa86a66c6bfc9' ;; 		x86) natsArch='386'; sha256='b11c6bded174332b3fc88ac40c3632448d58e8d58dc92551d9655407ce0107e8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 09 Oct 2023 23:49:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 09 Oct 2023 23:49:21 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 09 Oct 2023 23:49:21 GMT
EXPOSE 4222 6222 8222
# Mon, 09 Oct 2023 23:49:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Oct 2023 23:49:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dece2e91316626c2aeb73fab796c9095ba11a38f43e17e03f3cea33bada9941e`  
		Last Modified: Mon, 09 Oct 2023 23:49:58 GMT  
		Size: 5.8 MB (5811761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0164ce1b0fe0ce335f0348dbf1ef83dca670a9bb6c3036586e38f45c257ab3`  
		Last Modified: Mon, 09 Oct 2023 23:49:57 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a6185289b767b3266aeff451a57e88263f01cbb1544b137dd118ad2aa87d88`  
		Last Modified: Mon, 09 Oct 2023 23:49:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:56973c518df167ff13997d599dd6f0f488eb2a00380d161395d001cbd82ef4f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8701812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c71794277a3ea4fd3358f79bd24730e7bff545f116dbae54391ff86f7b5ba91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Mon, 09 Oct 2023 23:57:29 GMT
ENV NATS_SERVER=2.10.2
# Mon, 09 Oct 2023 23:57:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='26b3816709136a8d061e5147cfb217abb577d1fd79e08689417c9b0fa2806533' ;; 		armhf) natsArch='arm6'; sha256='189131c2b890446d88b508cc7e8aa937c38fef81dbd3f4b4d3d205af41edb5ab' ;; 		armv7) natsArch='arm7'; sha256='33374ac52531ac0a8c57c2f111d098eb99c42120fedfad57317817e6d48d70d2' ;; 		x86_64) natsArch='amd64'; sha256='8929b053d2dca2b62756982951c51147b69be984b55a7a850affa86a66c6bfc9' ;; 		x86) natsArch='386'; sha256='b11c6bded174332b3fc88ac40c3632448d58e8d58dc92551d9655407ce0107e8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 09 Oct 2023 23:57:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 09 Oct 2023 23:57:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 09 Oct 2023 23:57:31 GMT
EXPOSE 4222 6222 8222
# Mon, 09 Oct 2023 23:57:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Oct 2023 23:57:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1577c013973725bb512b6e87006f323da7dece18dc8d5cddf516ac8ac1bd3690`  
		Last Modified: Mon, 09 Oct 2023 23:58:15 GMT  
		Size: 5.8 MB (5800912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2989475d4fcb37e49592f48904864c46ac84f25ca502bbddacc54bddf27ec9a3`  
		Last Modified: Mon, 09 Oct 2023 23:58:14 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dca18857ae02bbc23b7a6d389a1036fd7822d30861d1f065a1fce1b2662745e`  
		Last Modified: Mon, 09 Oct 2023 23:58:14 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:a1cc118cb20105a3d28409f6f0134779e37d691cdfc8340e26aa21bf5c1fcecb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8999244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c690558bd2217d60e3ef1f45a02405b0c52118f1c91dda8b42c091696af68306`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Mon, 09 Oct 2023 23:39:44 GMT
ENV NATS_SERVER=2.10.2
# Mon, 09 Oct 2023 23:39:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='26b3816709136a8d061e5147cfb217abb577d1fd79e08689417c9b0fa2806533' ;; 		armhf) natsArch='arm6'; sha256='189131c2b890446d88b508cc7e8aa937c38fef81dbd3f4b4d3d205af41edb5ab' ;; 		armv7) natsArch='arm7'; sha256='33374ac52531ac0a8c57c2f111d098eb99c42120fedfad57317817e6d48d70d2' ;; 		x86_64) natsArch='amd64'; sha256='8929b053d2dca2b62756982951c51147b69be984b55a7a850affa86a66c6bfc9' ;; 		x86) natsArch='386'; sha256='b11c6bded174332b3fc88ac40c3632448d58e8d58dc92551d9655407ce0107e8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 09 Oct 2023 23:39:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 09 Oct 2023 23:39:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 09 Oct 2023 23:39:47 GMT
EXPOSE 4222 6222 8222
# Mon, 09 Oct 2023 23:39:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Oct 2023 23:39:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149e016e40994857a38606186dc8f2061ac54ed621273f59128aa5c6d060fb22`  
		Last Modified: Mon, 09 Oct 2023 23:40:22 GMT  
		Size: 5.7 MB (5666417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15cff88ae624a30801728dd1b20bb84f6e871846c236cf2613ec7c7fb6008f1`  
		Last Modified: Mon, 09 Oct 2023 23:40:22 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68049c030ad10066e6a3a63f9d02398f98a4b8bf2104c8d22adb9aed0ff83e1`  
		Last Modified: Mon, 09 Oct 2023 23:40:22 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
