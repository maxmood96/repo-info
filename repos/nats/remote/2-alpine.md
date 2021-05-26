## `nats:2-alpine`

```console
$ docker pull nats@sha256:7b65c778de18fe7a0e849098344166a05738caadb1d5a914cc4e8489b9b00a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9d2f79cec13b773e5677cec0f3272e52e55be44210e9f5b4917c623166394f34
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491da5634208d92e0c0a052128e76069f3d086b42582b2a07515f1b2284e1b62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Tue, 25 May 2021 01:38:13 GMT
ENV NATS_SERVER=2.2.6
# Tue, 25 May 2021 01:38:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='779d7f363fb0244071e67bf146c7169a8e3c35af2746c0a01323a3c5fd12bf31' ;; 		armhf) natsArch='arm6'; sha256='ed7211f56fa3928e3664ed92df632b0e7480bd1b4a91c239cb26a0f55831c815' ;; 		armv7) natsArch='arm7'; sha256='a55335b1329248912e80d8e68b5dd6b6a48c4742de089c4226f503d7e8357f2c' ;; 		x86_64) natsArch='amd64'; sha256='fc67ce0b4c748fa16ff92414c7d6be18a9285824c21d9629684c0093cf074f77' ;; 		x86) natsArch='386'; sha256='386811034531cea6e794e4764fdd70b0b948fdf7212064e8c176663992c46f2e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 25 May 2021 01:38:16 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 25 May 2021 01:38:16 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 25 May 2021 01:38:16 GMT
EXPOSE 4222 6222 8222
# Tue, 25 May 2021 01:38:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 01:38:17 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cf50b10150a20d88392a1085f9599e8af8f5a3018685f039e7c0e5dd7288d4`  
		Last Modified: Tue, 25 May 2021 01:39:00 GMT  
		Size: 4.5 MB (4532213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ee7d5e3ce0eae646fccf205b9550e978ab7664d6926dbb673199ef0f8835fd`  
		Last Modified: Tue, 25 May 2021 01:38:59 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a7f22a12d626460f4a81bc8142154fd148479c9c6d9c9513863790fc54ec43`  
		Last Modified: Tue, 25 May 2021 01:38:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:1c73109d6f0f4df4a01946b56cb9ee820e00ccab3a53a313fa455132eb429c5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6817138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610510cf73d587ce2492ee376849f1ad1c1aa9c4302164b35201671f17e814f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 13 May 2021 17:51:13 GMT
ENV NATS_SERVER=2.2.4
# Thu, 13 May 2021 17:51:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='88ad3d5fbef04ad3298ab528a1dc59f8531e313a0b47dc39606d8fbe29e71341' ;; 		armhf) natsArch='arm6'; sha256='cbcf6db915022c723149b609706d5fcf87f02ddca1c0dd0367870e394005b89d' ;; 		armv7) natsArch='arm7'; sha256='80be30d9caba8aa4661ed50fe64eeb454ff023f54a3687b85293f55bf6725d33' ;; 		x86_64) natsArch='amd64'; sha256='419b3a8761d1120c40851e2ac6d820695ca6b300e95933d88603cbd1255043fa' ;; 		x86) natsArch='386'; sha256='fd82800d141072f27f2c9e34ac287b40b3f086be4dca5a159611ce0e03f04ec2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 13 May 2021 17:51:25 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 13 May 2021 17:51:27 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 May 2021 17:51:28 GMT
EXPOSE 4222 6222 8222
# Thu, 13 May 2021 17:51:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 May 2021 17:51:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3f71d1e179b53574a4255bcfcd71fe370c624cd262a2ab7aaffd8e5d31720a`  
		Last Modified: Thu, 13 May 2021 17:55:46 GMT  
		Size: 4.2 MB (4194035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e8d47bbf0baab0970aae54c06f1e44815789587f8278d70e26399b9c5b6a52`  
		Last Modified: Thu, 13 May 2021 17:55:44 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36205a7a8707754144c7268ec085628e59b88815290a05666849b317dc5cf11b`  
		Last Modified: Thu, 13 May 2021 17:55:44 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:91d2dbf930b400b44b948361b60920659e74b28370d38b384bda56985d7d172c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6617719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02dc5ea95004c286602940e81b2950f498ef35217e01e1da4e372194c8a65d45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Tue, 25 May 2021 22:22:45 GMT
ENV NATS_SERVER=2.2.6
# Tue, 25 May 2021 22:22:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='779d7f363fb0244071e67bf146c7169a8e3c35af2746c0a01323a3c5fd12bf31' ;; 		armhf) natsArch='arm6'; sha256='ed7211f56fa3928e3664ed92df632b0e7480bd1b4a91c239cb26a0f55831c815' ;; 		armv7) natsArch='arm7'; sha256='a55335b1329248912e80d8e68b5dd6b6a48c4742de089c4226f503d7e8357f2c' ;; 		x86_64) natsArch='amd64'; sha256='fc67ce0b4c748fa16ff92414c7d6be18a9285824c21d9629684c0093cf074f77' ;; 		x86) natsArch='386'; sha256='386811034531cea6e794e4764fdd70b0b948fdf7212064e8c176663992c46f2e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 25 May 2021 22:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 25 May 2021 22:22:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 25 May 2021 22:22:49 GMT
EXPOSE 4222 6222 8222
# Tue, 25 May 2021 22:22:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 May 2021 22:22:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8fd93bac31720120ec97ee8f514ace788f281711084b9532b4d152e8fa3514`  
		Last Modified: Tue, 25 May 2021 22:24:21 GMT  
		Size: 4.2 MB (4192604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f240e54fb35db3d43766365af298a4fcd1eaab7acbfda0fd141a242fc1feaeb5`  
		Last Modified: Tue, 25 May 2021 22:24:21 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfddeffbc3b0f30d139487df21b514ec7bc915cbca61e31ee793eed0d9472e16`  
		Last Modified: Tue, 25 May 2021 22:24:20 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5d118edac8396ee73f73a2db080f4d870c52a48d1b7dfe932a8e3ec399e10ce5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6878882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f7d4fedb21f182edb7ca233e3ca03ce7ce1ffc9da57a002a1c6fc3d470b9ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 13 May 2021 18:39:53 GMT
ENV NATS_SERVER=2.2.4
# Thu, 13 May 2021 18:39:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='88ad3d5fbef04ad3298ab528a1dc59f8531e313a0b47dc39606d8fbe29e71341' ;; 		armhf) natsArch='arm6'; sha256='cbcf6db915022c723149b609706d5fcf87f02ddca1c0dd0367870e394005b89d' ;; 		armv7) natsArch='arm7'; sha256='80be30d9caba8aa4661ed50fe64eeb454ff023f54a3687b85293f55bf6725d33' ;; 		x86_64) natsArch='amd64'; sha256='419b3a8761d1120c40851e2ac6d820695ca6b300e95933d88603cbd1255043fa' ;; 		x86) natsArch='386'; sha256='fd82800d141072f27f2c9e34ac287b40b3f086be4dca5a159611ce0e03f04ec2' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 13 May 2021 18:39:59 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 13 May 2021 18:40:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 13 May 2021 18:40:00 GMT
EXPOSE 4222 6222 8222
# Thu, 13 May 2021 18:40:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 May 2021 18:40:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0a5de4d48d58b6e52e98523137e1c70f8edaa9edaba04eef99d76177962a7f`  
		Last Modified: Thu, 13 May 2021 18:51:28 GMT  
		Size: 4.2 MB (4165884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8bc18d6dca6719f9820cf0786282a7083a2b6ba41f6004e3a6b4e9aef5db72`  
		Last Modified: Thu, 13 May 2021 18:51:28 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f454ed6fd75994bba5f04bf38710b744a0804d5bec911593148cd24993d73d86`  
		Last Modified: Thu, 13 May 2021 18:51:28 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
