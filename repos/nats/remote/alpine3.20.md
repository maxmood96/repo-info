## `nats:alpine3.20`

```console
$ docker pull nats@sha256:770f6e7a0565d7c5d9033b1c808caa3ed55236fd3c357bc741027dccd8193bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine3.20` - linux; amd64

```console
$ docker pull nats@sha256:dcc12c914dfb359cf44ce445b84e8fb3fc3b92da6759513abfcb2630b04f79d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9825063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248fa754086bfb74af5bb121f1373e4738e365581c145f5489cbd372133e483e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:20:09 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:20:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:20:12 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:20:12 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:20:12 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2475ce9b769e29981af5e7232a389f137a4c1533873815d93c52e2aaf3e602`  
		Last Modified: Thu, 29 Aug 2024 22:20:46 GMT  
		Size: 6.2 MB (6201197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20992ade76bdbd285d9e0e262d78edaf1ea539fa7d1866594e2f7a46b2b36bf`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbda6ab02f361692238c77f1f6162010d17bf7b326ef7f7093dd796b8e6d3c`  
		Last Modified: Thu, 29 Aug 2024 22:20:45 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v6

```console
$ docker pull nats@sha256:e4ec9a598379a01d012b074aa1afcfb0cee2e972e5a8a4d4003b5991b0b27fc3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9236397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2f15851054b34821d07e965a95306940f6f7ca65914f5c80efaf477a91450e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:49:22 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:49:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:49:25 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:49:26 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:49:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:49:26 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d844310096296ddfeff9bf8b789e1605cdd3d88f81004963a38b99610026e`  
		Last Modified: Thu, 29 Aug 2024 22:49:51 GMT  
		Size: 5.9 MB (5870233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db9f1f00ff662402f84a8efce662ef6470b32e343dd7699199c2d9a6f7a81ea`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63106dbd5eb184e54cdfd7ca28fa95d8dcf6ba2abcc39544a29cf0eea77a1c`  
		Last Modified: Thu, 29 Aug 2024 22:49:49 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm variant v7

```console
$ docker pull nats@sha256:1c00d5e97f0d9b4af3827be2570daa9a02ac643c1ba4cdba4261b2f881bd10eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8956381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5cc688ff632c5b4b0d12ec9314358d150b0a1601349ac83a4a9ceb62e2393af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:58:26 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:58:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:58:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:58:30 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:58:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:58:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656b9bb5cc23aa40134f714451fef7c8726ec7db6764229cf25839e4391dfe2f`  
		Last Modified: Thu, 29 Aug 2024 22:59:01 GMT  
		Size: 5.9 MB (5860447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a9fa0f3d1dfe5d39f6ed34a98ff3b4f9f9ec6c03634143e1f76c27a2c507cb`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8832301372733a23d348505bc75af2ba91ab64d592d0b8ec77898090eacbe0a8`  
		Last Modified: Thu, 29 Aug 2024 22:59:00 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e9749524d4e44184743f8ce18293df42840d5b6508953b5761f9806a51371d7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9854965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea236d09a5781c6b19d0f3d6b9e5d3e84def068bac4bf3341e4e2676d9c3fcb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:39:48 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:39:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:39:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:39:51 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:39:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:39:51 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e48df3d142b6418d5bae4758ef077cdbe2bb20bf938689133c89d58d3d10057`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 5.8 MB (5767058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430feb76dca7a840872bc51fb707fb86429df4aec672c7430986bdb7c925382c`  
		Last Modified: Thu, 29 Aug 2024 22:40:24 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd37dcb19cd7bfc9cb5747400c866c148e0b83723ca9e5f197fee32ddd19881`  
		Last Modified: Thu, 29 Aug 2024 22:40:25 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; ppc64le

```console
$ docker pull nats@sha256:b4b56f90791576b19982c4589698d5ace1d4599edc9b5bbde096e2c06a85c66b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12ecb3a27c7f49d639e310f045ca767a6043e6da75e9b38cd897be06bc8e5a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:17:59 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:18:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:18:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:18:03 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:18:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f7352e34126f64a6ce8f30da6c0275cf2f3a6715f4cf89c6d6d01f78e230f`  
		Last Modified: Thu, 29 Aug 2024 22:18:31 GMT  
		Size: 5.7 MB (5740166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc584c29c5e3317464d7b35f0d7e6486ae7e4cbc373798f2fd91760d787f787a`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 561.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1123204e772767dcaab31c57da3e74a0c259eb281dff364e5d3086dd39d4ec`  
		Last Modified: Thu, 29 Aug 2024 22:18:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.20` - linux; s390x

```console
$ docker pull nats@sha256:dea187b901e59ef69ae603dc6366a4b9494916c5bee4dff8507cb410805be9f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9523925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a44c5fc82129f3053913065069906e76f32462ae77d9b5c0736a4cda26aa257`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 22:42:57 GMT
ENV NATS_SERVER=2.10.20
# Thu, 29 Aug 2024 22:43:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='f12b65d736dcd6c58d1cd39a2378a1c72041b3b2ba158ab9665cac137c4c7be4' ;; 		armhf) natsArch='arm6'; sha256='ad74598418d186e51562bc8419c5cd481e06ab0374848b7bb31271c0176ebdb3' ;; 		armv7) natsArch='arm7'; sha256='acc0c0a628252a5b6b5bf663f149626072041d7e7b9c18f2c6611769041ab8fb' ;; 		x86_64) natsArch='amd64'; sha256='979c6e633fb03987771b8f7baf99041b574638486ead35acdb868f6a7187a164' ;; 		x86) natsArch='386'; sha256='715663e909d86152698c7fd12d42a06da580f0e9aa205582228237bbc2d01d9c' ;; 		s390x) natsArch='s390x'; sha256='725df3feb668c5c44cdcbe5e6e0d080ee4c51e034c83b596a111b4473dbbf078' ;; 		ppc64le) natsArch='ppc64le'; sha256='1acac043d7b66ee2236615bf526df8a013bd292bca2ca6f3b59eee8456b92468' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 29 Aug 2024 22:43:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 29 Aug 2024 22:43:00 GMT
EXPOSE 4222 6222 8222
# Thu, 29 Aug 2024 22:43:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Aug 2024 22:43:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc57d16bacb8a6c57ed6057588b90b6a9ad526100e8eb57786a15e20691db53`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 6.1 MB (6061888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3f85e7bf4dcf9e6c1184fdc39e15518f6a13601a3f0eb7cecf21315e82e0c9`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3683297e34ea57f695a79c8c45d3f68461b35339640395a1a1fdebe059fcc400`  
		Last Modified: Thu, 29 Aug 2024 22:43:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
