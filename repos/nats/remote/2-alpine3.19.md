## `nats:2-alpine3.19`

```console
$ docker pull nats@sha256:753deafa5289c0bc8b92675bd2861e69a9061162cd0c6584a6f777e05df09de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:2-alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:79bfb095a2a29075819ebbd21420337f409d7d58d4230129318b612f0ec84c92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40b186cead18c79f854aa8b74737698e3dcb3bdea734ffd895da73010284e49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:59:27 GMT
ENV NATS_SERVER=2.10.9
# Sat, 27 Jan 2024 07:59:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 07:59:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 07:59:30 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 07:59:30 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 07:59:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 07:59:30 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a43a676978e1ee8774d416725cbbb52b789057dae207f7b067d9000f3ed3f1`  
		Last Modified: Sat, 27 Jan 2024 08:00:09 GMT  
		Size: 6.1 MB (6124234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f16b493abe09dc06b43101ca180ee2021ae778e01045209108b7a4bb4613f3f`  
		Last Modified: Sat, 27 Jan 2024 08:00:08 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388a8a3c31beaa997d3e1bb9e3240fbf75bd06f7dc5f1d00cbac1de3e6f8ee51`  
		Last Modified: Sat, 27 Jan 2024 08:00:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:8213d5ab00f14b73d0e7bb800cec52365803837914bdda31bad708870855cce4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9009710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24dd459bf3e12f1fd970c7173e819b4b60606a912eddda0db6ed67a4bf5c1088`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:22:59 GMT
ENV NATS_SERVER=2.10.9
# Sat, 27 Jan 2024 09:23:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 09:23:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 09:23:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 09:23:02 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 09:23:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:23:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2f3f48afd6c782d1185a19dc93137d9e73d2bb681a57d4319184ab3a3dc28f`  
		Last Modified: Sat, 27 Jan 2024 09:23:38 GMT  
		Size: 5.8 MB (5843316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bf38c6ddd661f94a42e09b4b1b355b4b037de702c2335fa81e985bd58b1932`  
		Last Modified: Sat, 27 Jan 2024 09:23:36 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f45d6179982d68e29f8cfcdebd37ddfbdf647bf693581b2bdcd39009c9e71e5`  
		Last Modified: Sat, 27 Jan 2024 09:23:36 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm variant v7

```console
$ docker pull nats@sha256:44db841880228e247be92f1137377799654988ea2b73f59397a6e9255b942a29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8753219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89740ed38a141941a84268cb68d35ff75dde880c83f29278b4c8b3a33852b1ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:16:19 GMT
ENV NATS_SERVER=2.10.9
# Sat, 27 Jan 2024 01:16:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 01:16:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 01:16:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 01:16:22 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 01:16:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:16:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e611fa09c4c007e46e9b16507dd1434a91a3166283087b862d3d3fe91d6874d`  
		Last Modified: Sat, 27 Jan 2024 01:17:10 GMT  
		Size: 5.8 MB (5833321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc753a9104d970ea2cd276e80c8df71eb3f00f1bc09c45dc14dbb4e40dde0569`  
		Last Modified: Sat, 27 Jan 2024 01:17:08 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3ada078a0a275cfe93b3c7f30466361982a8687ead5acf6bc869b0e10a0c2b`  
		Last Modified: Sat, 27 Jan 2024 01:17:08 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:580c391eee625b423e247682744a8c0389083f06d7d81cc1253224646f07d908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9076478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c304293ac0b240067684e0c9d3dd69cf577ff62cef21c89a58b4e304dafc54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 02 Feb 2024 21:53:44 GMT
ENV NATS_SERVER=2.10.10
# Fri, 02 Feb 2024 21:53:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='bbf8b7bc850580a370c9309d0e43ea2b2286e21fa9f5b33dfb751d219275e9e0' ;; 		armhf) natsArch='arm6'; sha256='9750cf2efb47afd8965a1ec9cd2a96c6d6af0cae70cfefc7b425e030799e1ac5' ;; 		armv7) natsArch='arm7'; sha256='3d9480c2bb3b0952f628d603855cbde234fe3768c498c5da89e11b8411d2be19' ;; 		x86_64) natsArch='amd64'; sha256='c8cd7e19b906a5f8a7f9f7e70fc4bfa492d66a069d9664c4db19fdee1b6aa640' ;; 		x86) natsArch='386'; sha256='99283c58577da02f6f9b0c104298308dfba18039dd48a782efc3be9d10b7bada' ;; 		s390x) natsArch='s390x'; sha256='e297977d1fc21c021aa989b1eda629dad9947d618558e14acc26f870ea86139a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 02 Feb 2024 21:53:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 02 Feb 2024 21:53:47 GMT
EXPOSE 4222 6222 8222
# Fri, 02 Feb 2024 21:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Feb 2024 21:53:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d644411492bc2bd9df7a2c3cb4b05ab05739ee7e9e4b45638e7ff4b47a0169a`  
		Last Modified: Fri, 02 Feb 2024 21:54:49 GMT  
		Size: 5.7 MB (5727764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe7fbf55209e2ea53f75ea3dd6a790bea3a6c838371ddba70bd252ba2d60bb9`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec8e8c754e8309a864da1769ebb19ff69b4fecef97a8d47fbb9a230722bfd71`  
		Last Modified: Fri, 02 Feb 2024 21:54:48 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:15f3887ac1a9fa368be6c8ba73ed9b059a242fc326fc69053314b35da04f3915
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9253015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf0ce78758845e9b2506bd7bfd961ace06fdc3057d98df941be3774fce987eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:36:18 GMT
ENV NATS_SERVER=2.10.9
# Sat, 27 Jan 2024 10:36:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 10:36:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 10:36:22 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 10:36:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 10:36:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93415b1cd5ad2d3093b7a9370b19168947165824ef7c8a93b740218a9b281944`  
		Last Modified: Sat, 27 Jan 2024 10:39:19 GMT  
		Size: 6.0 MB (6009384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7a825199ff1a8892808c6be4681c65539b570e5eff3e6aaf1d9c1e61ef0fc9`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76cdae9c9604eee0cfea93daa1e59038e6e713a09709a526e43d8313ab3fb39`  
		Last Modified: Sat, 27 Jan 2024 10:39:18 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
