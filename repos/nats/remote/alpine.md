## `nats:alpine`

```console
$ docker pull nats@sha256:31cdbee42d2a7a9b85a20b32fa47014716f0dd7593327e9ee44bdfe9d39c0cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:f67ef794683ba4fcddc40bf871ad70eb258221443adcf1927b0270f257e73a74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7701879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57eb300f225ba4543fcd1c479ef7191723cf877d51078fa0d82de48cdff5c640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 01:29:02 GMT
ENV NATS_SERVER=2.8.4
# Wed, 10 Aug 2022 01:29:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 10 Aug 2022 01:29:04 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 10 Aug 2022 01:29:04 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 10 Aug 2022 01:29:04 GMT
EXPOSE 4222 6222 8222
# Wed, 10 Aug 2022 01:29:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 01:29:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c1a3defde00a6a87bb6d1f724a28b2cc109a3d0e6b086dc01265ecf07abf3b`  
		Last Modified: Wed, 10 Aug 2022 01:29:38 GMT  
		Size: 4.9 MB (4877365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5c2bde7b7ca5bd606ae2db561e93e1addd87b05802f031fa6ec7a82f2828b0`  
		Last Modified: Wed, 10 Aug 2022 01:29:37 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a153c5b56febe9e8cc9d9df0925d160671c9aaffc633a61bdd7f368d42a1b96f`  
		Last Modified: Wed, 10 Aug 2022 01:29:37 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:ce1a0d5feba1dea7b75d42a2cf9f0db37008aa23611208f0636d2e854f3e4e39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7141995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787a0f7c8f446c6de7f76a546e1b7816713946ff4446c8b8ab3300a076b84ea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 19 Jul 2022 22:49:49 GMT
ADD file:4958b5356608921fe85d83047b74d1cb4a53de78c3465039ac4e60a68329da64 in / 
# Tue, 19 Jul 2022 22:49:50 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 04:34:53 GMT
ENV NATS_SERVER=2.8.4
# Wed, 20 Jul 2022 04:34:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 20 Jul 2022 04:34:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 20 Jul 2022 04:34:57 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 20 Jul 2022 04:34:58 GMT
EXPOSE 4222 6222 8222
# Wed, 20 Jul 2022 04:34:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 Jul 2022 04:34:59 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fcc62ebebb3542c1aad49c3cc072a98cf619f67e914baba1ea7dfeadcb32cbdd`  
		Last Modified: Tue, 19 Jul 2022 22:51:27 GMT  
		Size: 2.6 MB (2622400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d8cdff31cbcbff5a77bad319304be00f6bfee5e7a0b3e79bb5098a172211b1`  
		Last Modified: Wed, 20 Jul 2022 04:37:01 GMT  
		Size: 4.5 MB (4518598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f94963426fbd74891e24cad2378e102449638365b7c4d30dea2b2a42afa3964`  
		Last Modified: Wed, 20 Jul 2022 04:36:58 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6849175061bf5248fac59f399e2663721962abef73263e1e4055ef7d1878e6`  
		Last Modified: Wed, 20 Jul 2022 04:36:58 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a86957d0ea21981ed74f78c988f8b5202243dab5a43f68f0cd4d09be0e03acf7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6963329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a19e2d0d29009797ec24843b88e7a35ebb4ca64c9a7b624b6be3290ec5f730`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:52 GMT
ADD file:0bd18306f21937a9572e68c768f05f4a9d8341b40c2379a7bfcb857c77734a14 in / 
# Tue, 09 Aug 2022 16:57:52 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 22:35:52 GMT
ENV NATS_SERVER=2.8.4
# Tue, 09 Aug 2022 22:35:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 09 Aug 2022 22:35:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 09 Aug 2022 22:35:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 09 Aug 2022 22:35:56 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Aug 2022 22:35:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 22:35:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:59775c20a906b1a49edcdc41a700a795998979d6ecf8f8d9cd7cbdf45e686d81`  
		Last Modified: Tue, 09 Aug 2022 16:59:12 GMT  
		Size: 2.4 MB (2435092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55d1d06353a20f9de5b52fd408cb1d36cb23aea75e779350590565a5a4dea90`  
		Last Modified: Tue, 09 Aug 2022 22:37:42 GMT  
		Size: 4.5 MB (4527236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e8be9dffb2c65f4e861ee01ddc4ec8362d0a2ca4ac53ad84fa5baf7b28b2d3`  
		Last Modified: Tue, 09 Aug 2022 22:37:41 GMT  
		Size: 589.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de94a2ef272b2e3ef327e7dbc685dfc8c6b58775169e3ec47a94fd5407841bf1`  
		Last Modified: Tue, 09 Aug 2022 22:37:41 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:1d7154e4491475ff8fb864a26874ba8b4b250864ad515419c96432134b79a03a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7234771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff14469067b8205c1030c0740c47b13a4cd70a4cb3cd3e3f02472b056353df3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:52:27 GMT
ENV NATS_SERVER=2.8.4
# Tue, 09 Aug 2022 20:52:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 09 Aug 2022 20:52:31 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 09 Aug 2022 20:52:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 09 Aug 2022 20:52:32 GMT
EXPOSE 4222 6222 8222
# Tue, 09 Aug 2022 20:52:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:52:34 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0beb1bc3611827acd1326750497c2cc98b9160ed5aec13a1112ad88b6ba136`  
		Last Modified: Tue, 09 Aug 2022 20:53:33 GMT  
		Size: 4.5 MB (4515360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a20f9bb5cbf9bb42bf80058089fa2cc11fe7eaad0e4342ef69340f9421360e9`  
		Last Modified: Tue, 09 Aug 2022 20:53:31 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b065ba618e0c23dec2ae44bb9555ee098a0827cf44bc5f30ae1d9448e11f668`  
		Last Modified: Tue, 09 Aug 2022 20:53:31 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
