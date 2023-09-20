## `nats:2-alpine`

```console
$ docker pull nats@sha256:4ee781bd309006469c84d088c93db6172e8a94439239d28865dcd23791defdc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:756a55661288407f688c52224ac8b12d008f0fec9343c68281b04bb59cbcc427
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9270382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb9252d07acfbe3ac9083449c0fef74561021019d85c2993f5bce02c7a16201`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Wed, 06 Sep 2023 23:19:53 GMT
ENV NATS_SERVER=2.9.22
# Wed, 06 Sep 2023 23:19:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 06 Sep 2023 23:19:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 06 Sep 2023 23:19:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 06 Sep 2023 23:19:55 GMT
EXPOSE 4222 6222 8222
# Wed, 06 Sep 2023 23:19:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 23:19:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fdd304ec17c2cf1f7629eefc922e04fae260b6d902e4fd42c81a5e5ce9d5dc`  
		Last Modified: Wed, 06 Sep 2023 23:20:32 GMT  
		Size: 5.9 MB (5867770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2863800c65f086f618bf3df0e7855997aea26ba27f4c759cf8bfae94da866bb`  
		Last Modified: Wed, 06 Sep 2023 23:20:31 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e32a641538132ed9885ca87c473fe9ff71415289c1f5276ba1157bb0760bd04`  
		Last Modified: Wed, 06 Sep 2023 23:20:31 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c5be15c45e97c30c95cbc26f2c8ba147e8bb32d3b8c260bc40f4a0df66a5290c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8948962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2743d89a0540f70cf9435ec0e9f20c05691f60ef613397302919c83c2ec38c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2023 23:49:18 GMT
ENV NATS_SERVER=2.10.0
# Tue, 19 Sep 2023 23:49:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59456ee8d222213c0f713e5b571156ec053db15288ee9035b3a7ad01e226c0bb' ;; 		armhf) natsArch='arm6'; sha256='c12c5cde86dba95fa4b433b58af3b9568893e3c7814fa22feae85eb47a9bb2bd' ;; 		armv7) natsArch='arm7'; sha256='748eb00c8d29c674bb4f98371a1afd8be9fba59336be9ef24d24fff148f1e7a4' ;; 		x86_64) natsArch='amd64'; sha256='76f5798ba3923dbc4f170bbae0055d3267d5c604179b2c644f6e7c79cc970d76' ;; 		x86) natsArch='386'; sha256='7f151267f76948293a5721e642b489e1135aecbeb2399dd23d00b04e6a609191' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 19 Sep 2023 23:49:22 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 19 Sep 2023 23:49:22 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 19 Sep 2023 23:49:22 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Sep 2023 23:49:22 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c753d5ce31439aa7996e62e4188edf43c2b39ad361ecfeb2392ebae52ca2bc84`  
		Last Modified: Tue, 19 Sep 2023 23:49:54 GMT  
		Size: 5.8 MB (5803150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d290ef1548f16e9c210921d118381b17a21f4e5b5e75bece4d8fd7f74c860f9`  
		Last Modified: Tue, 19 Sep 2023 23:49:53 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c288f3decbd4fe57a3fa3b18915d201e3c0e8b1ffb8db9b3f6ec219a47ff7320`  
		Last Modified: Tue, 19 Sep 2023 23:49:53 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9ca6685d1ad99fa588f9d4dc05ffe27569ed660b735218fd38795568fe508c73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8492829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0271598ef211f3df61073ff64c769275b4bb72b68b984931c8a7af1706fe80c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Wed, 06 Sep 2023 22:57:29 GMT
ENV NATS_SERVER=2.9.22
# Wed, 06 Sep 2023 22:57:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='811e5a3c8187d937a753f182bd5ae2035c91604bda11a3b11023e5eea0504c41' ;; 		armhf) natsArch='arm6'; sha256='4d6f2f8ee9faf43de9fed5b43a0a5db836ad81797146065777b06a59f90cf1b0' ;; 		armv7) natsArch='arm7'; sha256='b8c83cd825b05d8d0610fc9352804fe810ae6bd9d8f0d814a39b0f152ec2ba79' ;; 		x86_64) natsArch='amd64'; sha256='9550278e34e94aebd410ec401bc145d3538e430ec2a40d5213fffdf9fdd49c27' ;; 		x86) natsArch='386'; sha256='a8ccdd37eac64b031ea96762d7f72a74445e9a708c0363549ba7e119fa79e52c' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 06 Sep 2023 22:57:32 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 06 Sep 2023 22:57:32 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 06 Sep 2023 22:57:32 GMT
EXPOSE 4222 6222 8222
# Wed, 06 Sep 2023 22:57:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Sep 2023 22:57:32 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1962026ec365b08ba406dd0e38e57c06dcd04f2225faffcc17883ed87716cdc8`  
		Last Modified: Wed, 06 Sep 2023 22:58:03 GMT  
		Size: 5.6 MB (5592351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578cf75378460664df525d3b5d1412e778f7b8cdc5f3c31207b3bbc2f6c074f5`  
		Last Modified: Wed, 06 Sep 2023 22:58:01 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bf3e24d68a6cadd0880ce3163738934bf8e5b267923da68dd6922cd6b98a31`  
		Last Modified: Wed, 06 Sep 2023 22:58:01 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:3741a37c4eee94956307d7020343acd984e3cc57e818836de28b8140710b4985
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8985845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fd1017a8724cc2b2ea9715ad739a4c8115e0f5d255d3ea8f32afe5b1865140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Tue, 19 Sep 2023 23:42:32 GMT
ENV NATS_SERVER=2.10.0
# Tue, 19 Sep 2023 23:42:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='59456ee8d222213c0f713e5b571156ec053db15288ee9035b3a7ad01e226c0bb' ;; 		armhf) natsArch='arm6'; sha256='c12c5cde86dba95fa4b433b58af3b9568893e3c7814fa22feae85eb47a9bb2bd' ;; 		armv7) natsArch='arm7'; sha256='748eb00c8d29c674bb4f98371a1afd8be9fba59336be9ef24d24fff148f1e7a4' ;; 		x86_64) natsArch='amd64'; sha256='76f5798ba3923dbc4f170bbae0055d3267d5c604179b2c644f6e7c79cc970d76' ;; 		x86) natsArch='386'; sha256='7f151267f76948293a5721e642b489e1135aecbeb2399dd23d00b04e6a609191' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Tue, 19 Sep 2023 23:42:35 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Tue, 19 Sep 2023 23:42:35 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 19 Sep 2023 23:42:35 GMT
EXPOSE 4222 6222 8222
# Tue, 19 Sep 2023 23:42:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Sep 2023 23:42:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e6ea7267789f2929636c3fb0112e8911a41bdcb706cdcb27da3c12a901cc89`  
		Last Modified: Tue, 19 Sep 2023 23:43:29 GMT  
		Size: 5.7 MB (5654080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf1c8bac84139e093707d14ffdf2ca062be0a00111931c736cd845ad2e48806`  
		Last Modified: Tue, 19 Sep 2023 23:43:28 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6e83eac367a9a299357e1ce2a1f465883c94d0449ca1fb623617d9c21b123c`  
		Last Modified: Tue, 19 Sep 2023 23:43:28 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
