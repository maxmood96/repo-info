## `nats:alpine`

```console
$ docker pull nats@sha256:7109340f95ac01c95ad15adc3fd98f065aa1a106289e541604d95c454ecba2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:8d3613218b0924df72a1bdf02b969797d0741ca670077a636e00a2ff77e72f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9572054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b81a17fb41b7d411e73cdc0846fda5e35b9035e01da68fcc4ac975ebc12cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 16 Feb 2024 20:02:00 GMT
ENV NATS_SERVER=2.10.11
# Fri, 16 Feb 2024 20:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='52e603af6c249b716509ad7effb32033560e93578558c9e39420c15ab8d35fc5' ;; 		armhf) natsArch='arm6'; sha256='cf9d1668e00efba64e5f9bef36d950fcdfc99b99ec436282da2207ddbf63d35f' ;; 		armv7) natsArch='arm7'; sha256='582e77659441481f9a0dcd5bb3a8337137120448036db8601713b1769e19d1c2' ;; 		x86_64) natsArch='amd64'; sha256='4b85a83a8d3b5f919e4915fc68a43186eda37eb2f7b893c1690b3cabd1e24562' ;; 		x86) natsArch='386'; sha256='765acca88e27db4052b22eea63422f501e671a257da49bf955a54a52b2e314d4' ;; 		s390x) natsArch='s390x'; sha256='e534bcc6ee8d70090d8b60a0686970b1d6a0a79df2acdb32f367a4e9589e19ae' ;; 		ppc64le) natsArch='ppc64le'; sha256='f0dd6e4c8c2e1c1bfc4c058e7461bb776e62473cc35f12c8db844e2a57d4eb1b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Fri, 16 Feb 2024 20:02:03 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 16 Feb 2024 20:02:03 GMT
EXPOSE 4222 6222 8222
# Fri, 16 Feb 2024 20:02:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2024 20:02:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f13f7c1823b0fdcddc2b0fec414533005a5efc3e6e7766963fe84039e823a60`  
		Last Modified: Fri, 16 Feb 2024 20:03:17 GMT  
		Size: 6.2 MB (6162326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbc9ba69a09f76d72b908edb77f5a63055758de23920557ccf6b7e669e39321`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f29ff33d7557dcf701ec025a0b38765a7cf4663531132ddf52469f10c39da9`  
		Last Modified: Fri, 16 Feb 2024 20:03:16 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6e93abf037354dbe3af08ece7d516f8a4e61c675fbab84594adf10b108082777
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9051274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075217343e913477fcd44713b6ae36fa6c55e5a333eca26c9e952a97e51a14f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:49:24 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:49:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:49:28 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:49:28 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:49:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:49:28 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b7bd072e2424f96ed51dee5137cd95e43686fc4624f2d2feee365fd304f5fc`  
		Last Modified: Wed, 13 Mar 2024 00:50:00 GMT  
		Size: 5.9 MB (5884880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd491dd798da6f6a27555feb3be80ea1e29262571e10acde00300ee332740f`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568e37ef91f5962c31828a2adc1588dcec32dbe5859699372ff1656c5659a915`  
		Last Modified: Wed, 13 Mar 2024 00:49:59 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:06913e056cdc6c1997068e0fe2e6355f571c04f12afd48f9e02cea1f16554016
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8795654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbc0f10b6a6c92c2a77318fa3a4f9b73f5dc9a8e0304b5475f614294196d6d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:35:35 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:35:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:35:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:35:39 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:35:39 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55a741d01acaf5448cb8ffa39243f9f34261fd88e914772554124224189cc81`  
		Last Modified: Wed, 13 Mar 2024 00:36:23 GMT  
		Size: 5.9 MB (5875752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d61266118e4acdda142cd2ac76a4ef35e24e7502ec60b4cf26cf49a145acdc`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 590.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e59e375c0cd803e4186b41a2566a69e1f0a8b88ba1cf0954a5a00d33af0d2`  
		Last Modified: Wed, 13 Mar 2024 00:36:18 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:62b700c1d94d9c9164795d902681026f20a4c2c215e70dea7661f632c43f93b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9088728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b8a7d9375b33a34c6019c8a05fc253872624aaba1066208fa1ae728471c370`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 00:40:21 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 00:40:23 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 00:40:23 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 00:40:24 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 00:40:24 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 00:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 00:40:24 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46909e9837d35c1cb85abbf0a81ed8df7ac00f9ac7df67d275bd7edb87fdc88b`  
		Last Modified: Wed, 13 Mar 2024 00:41:06 GMT  
		Size: 5.7 MB (5740016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a74044cf86ca3325a7a324fbd7d08694e721bad44f2f7865d35ed3b3ce23b4`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f776b77a6001c5e0fd42db5610aa2acfeecb867c59a3559a2cd6983a5067ad6c`  
		Last Modified: Wed, 13 Mar 2024 00:41:05 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:e73b5c826fe9e8fc554f8e4440d8ae0504b4f7899d6c5bc38c6b68a0d9e705d0
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9078995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96541c86763ab33908efa9617f909b1b23853fc66f5740829aaa97d4fb819d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:28:25 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:28:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:28:30 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:28:31 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:28:32 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:28:33 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd4d0c36112be2592baa66fdba8327cff756029be8e96f803015fce9a8bfab7`  
		Last Modified: Wed, 13 Mar 2024 01:29:22 GMT  
		Size: 5.7 MB (5719643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217c8e169d797596a8b822f912ec2ba564e491f6949ecd95a5a405d275c5a5a6`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad20a946927156b80304d831d9d123a0ba902501570002869968e92231bbd32`  
		Last Modified: Wed, 13 Mar 2024 01:29:21 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:49f1c4fa564a8f8073315103db29d373273c7e703c43d6f275a1acc3ab010a3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9296162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7420d0049b07e2c363f050c33e0ac3ba0fe39fe6d0bee0ffea5c71f2fdf0749`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 13 Mar 2024 01:14:00 GMT
ENV NATS_SERVER=2.10.12
# Wed, 13 Mar 2024 01:14:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='df353b32cc8813cc84b9a5fe131d702136bfbbcd3394d83cefe2dd59ecf9078c' ;; 		armhf) natsArch='arm6'; sha256='665cd325e302b6536a846a0c4565f7c2fa2b83bed271ecda4255d508172920de' ;; 		armv7) natsArch='arm7'; sha256='d5ff696d94dc0adc5a2d9863b42c139369b12c2b00e9768bc136d4f7dc50cbc2' ;; 		x86_64) natsArch='amd64'; sha256='462584768f2e734d6be3cb5f24d817abef5191f3575091612e849e4718aac5dd' ;; 		x86) natsArch='386'; sha256='bb991c52017b1b54568fb69420f7c6a127eb6a8f84c18dfe2e47a0ff29db42e4' ;; 		s390x) natsArch='s390x'; sha256='84654e1d959e36c1549f47f36d7cb8f8a1395691ebf7c30ccc3ef8a0966f65fe' ;; 		ppc64le) natsArch='ppc64le'; sha256='0c390ad5de7828c727428731c4ccc8f67ae7db7a4b68b7d3c07db0c8e595ecd6' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 13 Mar 2024 01:14:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 13 Mar 2024 01:14:03 GMT
EXPOSE 4222 6222 8222
# Wed, 13 Mar 2024 01:14:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 Mar 2024 01:14:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d4a8da7be6313cc596f154b85b638749ab970144f58575af5bef288a9e44ce`  
		Last Modified: Wed, 13 Mar 2024 01:16:34 GMT  
		Size: 6.1 MB (6052529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c87220ce1b5f8a7ed2e5ab6caf39ac9028ba6d25133711633f25a21b60c4b24`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f30dc994a90cc1c2a38e8a5176d279817dd3d25ffe3d8ac67b665c606f3b3`  
		Last Modified: Wed, 13 Mar 2024 01:16:33 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
