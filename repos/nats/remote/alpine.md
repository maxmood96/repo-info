## `nats:alpine`

```console
$ docker pull nats@sha256:0e4a4ad77463c65a4716c204d48a563b0b7a3cb3818a4f3432a3bdf59c6e2d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:79f20bf7572a9763a44766834077189f1c775889653cd06074cd253411e57a61
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7630738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1cf25eec293c91bbdbf8b721d5bf624068f661f44e98e1e205e8c229cab087`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 20:44:58 GMT
ENV NATS_SERVER=2.4.0
# Fri, 27 Aug 2021 20:45:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='eb510dd016cb1a9e9b1fae88a3471029048cb75dcc4ad83a4f5b1e3665f24a20' ;; 		armhf) natsArch='arm6'; sha256='76ac66cd86217a43bc227220eb054aac8a5744890d43c76156075d68a684d9e0' ;; 		armv7) natsArch='arm7'; sha256='e7521841d59f55fcef6172aa8f22d3af7ba1776bd67109a23c29d34d18d44bd6' ;; 		x86_64) natsArch='amd64'; sha256='f6841c89fcf99302bc7ac295ddc1e75322385f861d55abee79733976c8eb9bc7' ;; 		x86) natsArch='386'; sha256='c7e6e2b73d402e841b3abb57e26e2ef53350b44e385255bf289b08182058076a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 27 Aug 2021 20:45:01 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 27 Aug 2021 20:45:01 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Aug 2021 20:45:01 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Aug 2021 20:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Aug 2021 20:45:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959ebfdebb025023622bfeb78dc3a9beb3090fa18b8697942c7dc6f0b87afa99`  
		Last Modified: Fri, 27 Aug 2021 20:45:51 GMT  
		Size: 4.8 MB (4815326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f228a428ebd569f8107874e30b71d5b203f766eba63c7978d3c235ba9b2c275f`  
		Last Modified: Fri, 27 Aug 2021 20:45:50 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1003110185dc217624a0a61a29d552bff59dd5db5fb81644dfe9638e12c14a`  
		Last Modified: Fri, 27 Aug 2021 20:45:50 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:c516621cb4dc61ad9db1927cdcec7210328be6d7b813acb688016584d61be212
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7121422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c48580010dc9af32e7a019914f078134ae513ef77280b7877fe7fd47665426b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 09 Sep 2021 23:49:46 GMT
ENV NATS_SERVER=2.5.0
# Thu, 09 Sep 2021 23:49:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='93f64cd14f04b4e7f6c3a2c10d09888be653406b7bc1a41f399ae44746388a5c' ;; 		armhf) natsArch='arm6'; sha256='12f38f6881cdcf27c0faebb7ab6580b40253c36dc1531d499a29c4998a009494' ;; 		armv7) natsArch='arm7'; sha256='fb3611b57a932f5c75310dee66597057ab65b442eb84d73b2c5fd9389eb6e518' ;; 		x86_64) natsArch='amd64'; sha256='4d2f4abb15b45618ce772659c9f3eca60f25266dfc976f0354430ad67c8fd886' ;; 		x86) natsArch='386'; sha256='776aecc77c33146d88e6b3cb1787097f9817122182f49f7243c0ea3fd62ad029' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 09 Sep 2021 23:49:51 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 09 Sep 2021 23:49:52 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Sep 2021 23:49:52 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Sep 2021 23:49:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Sep 2021 23:49:53 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b214a44f07577985e2f01798e9acf02be903c28022f74d244b22418b31e815`  
		Last Modified: Thu, 09 Sep 2021 23:52:03 GMT  
		Size: 4.5 MB (4493006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d232ac6d6c1f822be800be02acbb341f7abe35b05bd13a0857df02fd1cc600a6`  
		Last Modified: Thu, 09 Sep 2021 23:52:01 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e364400828db299d750b3bcc80b1e3b1df2f7abe62c5d6293f3c7e22d93e20a`  
		Last Modified: Thu, 09 Sep 2021 23:52:00 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:9fdddb77b45992dd28913e9dfa6bc38fbec5529bd6e2ebfee5a3062adb65d3db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6909360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f14d25a2d94b56f2a9f861be0b92583a98fa9ea527df32150655256018ff97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:57:31 GMT
ADD file:a7da7992ccea54d3295231027614f138aa45c4d4a25ea6ec9bf7b316b9f67d95 in / 
# Fri, 27 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:12:43 GMT
ENV NATS_SERVER=2.4.0
# Fri, 27 Aug 2021 21:12:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='eb510dd016cb1a9e9b1fae88a3471029048cb75dcc4ad83a4f5b1e3665f24a20' ;; 		armhf) natsArch='arm6'; sha256='76ac66cd86217a43bc227220eb054aac8a5744890d43c76156075d68a684d9e0' ;; 		armv7) natsArch='arm7'; sha256='e7521841d59f55fcef6172aa8f22d3af7ba1776bd67109a23c29d34d18d44bd6' ;; 		x86_64) natsArch='amd64'; sha256='f6841c89fcf99302bc7ac295ddc1e75322385f861d55abee79733976c8eb9bc7' ;; 		x86) natsArch='386'; sha256='c7e6e2b73d402e841b3abb57e26e2ef53350b44e385255bf289b08182058076a' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 27 Aug 2021 21:12:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 27 Aug 2021 21:12:49 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 27 Aug 2021 21:12:49 GMT
EXPOSE 4222 6222 8222
# Fri, 27 Aug 2021 21:12:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Aug 2021 21:12:50 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a14774a5a62e0f454febaec7cb603e18a6a8e25ef9da4a4da85b155bdd5e5a7a`  
		Last Modified: Fri, 27 Aug 2021 17:59:00 GMT  
		Size: 2.4 MB (2430419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5966a7cedc8cd3fd86581316ea0c056ee1beab3cece3b6cc4dd672fc46540baf`  
		Last Modified: Fri, 27 Aug 2021 21:14:56 GMT  
		Size: 4.5 MB (4477972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad6a30f2c8e55902fd5341442838c84cedf23c949539cdfd87d76f6176d5dda`  
		Last Modified: Fri, 27 Aug 2021 21:14:53 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6c2ea642bdc0a92a6797a6e2ea5891f8e13439fd7eeba41e56b6ffda56bb68`  
		Last Modified: Fri, 27 Aug 2021 21:14:53 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:88b4d8f2f54f207d5400e8d3e9037d55ca8d2969b126e07d833c6d3464f93300
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7156798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f803b2b0ed9b56df4cac8c3a03dfd789e480a622c1f3a282ecee5fd0f937d9e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Thu, 09 Sep 2021 23:40:02 GMT
ENV NATS_SERVER=2.5.0
# Thu, 09 Sep 2021 23:40:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='93f64cd14f04b4e7f6c3a2c10d09888be653406b7bc1a41f399ae44746388a5c' ;; 		armhf) natsArch='arm6'; sha256='12f38f6881cdcf27c0faebb7ab6580b40253c36dc1531d499a29c4998a009494' ;; 		armv7) natsArch='arm7'; sha256='fb3611b57a932f5c75310dee66597057ab65b442eb84d73b2c5fd9389eb6e518' ;; 		x86_64) natsArch='amd64'; sha256='4d2f4abb15b45618ce772659c9f3eca60f25266dfc976f0354430ad67c8fd886' ;; 		x86) natsArch='386'; sha256='776aecc77c33146d88e6b3cb1787097f9817122182f49f7243c0ea3fd62ad029' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 09 Sep 2021 23:40:05 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 09 Sep 2021 23:40:05 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 09 Sep 2021 23:40:05 GMT
EXPOSE 4222 6222 8222
# Thu, 09 Sep 2021 23:40:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Sep 2021 23:40:06 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49450e2f2462d1e207a865d4a084154f6a3c5edc2b3b4954d34d4e1ce75d38f2`  
		Last Modified: Thu, 09 Sep 2021 23:41:18 GMT  
		Size: 4.4 MB (4444005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edeb0b05b16add9a16e4a8bc8c1eced6c1f60f58ac669216dbbf93cb9bce40d2`  
		Last Modified: Thu, 09 Sep 2021 23:41:18 GMT  
		Size: 555.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67be552e94a6cfc686543e5bfa0c1a6bca72bc9dce939fb9f3e43c4a77f5e6e3`  
		Last Modified: Thu, 09 Sep 2021 23:41:18 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
