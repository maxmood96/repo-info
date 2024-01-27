## `nats:alpine3.19`

```console
$ docker pull nats@sha256:4124a12fc312a2de1fe63b4419d5e5b3cf65391adefdb7ffdc0d9f6290181a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; s390x

### `nats:alpine3.19` - linux; amd64

```console
$ docker pull nats@sha256:c0c430e0aa1b87821733618efec270d3cb5a20b71559c4fba2879d753891828f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e05ceb561818dacde34670ae562d6b3b2745cf68917727bb8a95801c35a15c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 18:25:51 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 18:25:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 18:25:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 18:25:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 18:25:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 18:25:54 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c79310a28618d1a0b0421504ba7da5db20beeb46960dbb3aab67472347335cd`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 6.1 MB (6124232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea0dcdc4802d37c3deab3ca75e7dad4153c55b7e05f51b842212a71d1d70346`  
		Last Modified: Thu, 11 Jan 2024 18:27:06 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cc2ac8e2501159d5e7f568fb055284f4cc0e2c5518643ec586238322564deb`  
		Last Modified: Thu, 11 Jan 2024 18:27:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v6

```console
$ docker pull nats@sha256:f42d42ffb85f1e0f61418b300bdc8522cd644d773bd72bbc2bc4d7ffc3f86050
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9009514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2130d4da569d02f232417ecabfc3ecd3792704e0119698a6031f6fbffeaea8f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:54:46 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:54:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:54:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:54:49 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:54:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:54:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106a5d30cb7cbf14363d518f6a41b332092a8d4842fc703ee81a75e7ec5adc39`  
		Last Modified: Thu, 11 Jan 2024 17:55:18 GMT  
		Size: 5.8 MB (5843372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a31bbe9bb94ec043c1d0b7e86dfa90be04fb01972ea637bf97eaffc9b6662cf`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32644e63c787562b603d71fa4739b93464a62b138af2e17be91dc99831cfac0`  
		Last Modified: Thu, 11 Jan 2024 17:55:17 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; arm variant v7

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

### `nats:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:f5aee58d3073e664a39ff38ba61858dec19787157fc757f53aed3bc426e3063c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (9049105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537033fdea47ee163598dd4a73fb37282f2b7cf0b6368f49c660e105c584ad94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:43:34 GMT
ENV NATS_SERVER=2.10.9
# Sat, 27 Jan 2024 00:43:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Sat, 27 Jan 2024 00:43:37 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Sat, 27 Jan 2024 00:43:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Sat, 27 Jan 2024 00:43:37 GMT
EXPOSE 4222 6222 8222
# Sat, 27 Jan 2024 00:43:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:43:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f71c5b9752589bb94dcff71fe4c72ca6cd65e98681844bd030029a108bafedc`  
		Last Modified: Sat, 27 Jan 2024 00:44:08 GMT  
		Size: 5.7 MB (5700389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc99a3810b1020ed575c7b5bc935470098d9c857f4c307f5c90a71358b0ed698`  
		Last Modified: Sat, 27 Jan 2024 00:44:07 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97992205c35ccf28e41e718ca7ec4e190bdacac1cad55c59a87bfd47be8f056c`  
		Last Modified: Sat, 27 Jan 2024 00:44:07 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.19` - linux; s390x

```console
$ docker pull nats@sha256:51e421189989bcbb74800e1ae3a0ca15878d2c620d05a4cbf3e6831f9e774d08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9252730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb016590dfbe6012a0db1e32d435b002c314702c0b1e161859005ef758a93c14`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Thu, 11 Jan 2024 17:53:40 GMT
ENV NATS_SERVER=2.10.9
# Thu, 11 Jan 2024 17:53:43 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='7cfaa8547137e6df8b791c831fbdda49c527ff6b81ce71f4ece085ac993df9d7' ;; 		armhf) natsArch='arm6'; sha256='d971b43a59dcbc99e2fa2b18fa3595de2de510d8562a77b8e40f1fea1c6de469' ;; 		armv7) natsArch='arm7'; sha256='a84e3794f0e4a94e211499c0af6c60e0135eab505f03d0d568dec3ba3cfffbab' ;; 		x86_64) natsArch='amd64'; sha256='5920e2d3935c1a1f19aa7eeaab95dabfe4cd0b98de7417b9af5023361de92626' ;; 		x86) natsArch='386'; sha256='56a1e8491102f32e78d15ebea619fbef59d5a470a8655ab2417c41eb51229098' ;; 		s390x) natsArch='s390x'; sha256='2fc697734b08bfcb53b9be613518ecf611d631c4dd39fa4874265830487188a7' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 11 Jan 2024 17:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 11 Jan 2024 17:53:44 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 17:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jan 2024 17:53:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0117eb130f42f836abf0877b24a75e47e6b88c568853bfd8fa17262fc9b91fd`  
		Last Modified: Thu, 11 Jan 2024 17:54:31 GMT  
		Size: 6.0 MB (6009399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6454d9a429577acbc85b8fcad82bd1b9db46fe94ce5bafb87d63c031869fb49f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8451318dd5eddb786b363142cb4ff3250e35bf72cd3faea8719cdca1470c933f`  
		Last Modified: Thu, 11 Jan 2024 17:54:30 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
