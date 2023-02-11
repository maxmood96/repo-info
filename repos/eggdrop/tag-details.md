<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.4`](#eggdrop194)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:7894b941d338db107cecf5d70ff99870f215da85604df9155f390d82c0a0b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:9bd4adb3f737baa8bfa4bdd21695badd88ac8888e96f09ce3222a5fd00ed3b8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12096201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea8761751c3b6130b136e2142d22239339bde7c9cb0a5c5d297cb1f5bbf1113`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:20:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 12 Nov 2022 05:20:03 GMT
RUN adduser -S eggdrop
# Sat, 12 Nov 2022 05:20:04 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 05:20:06 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 13 Jan 2023 00:27:34 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 13 Jan 2023 00:27:35 GMT
ENV NICK=
# Fri, 13 Jan 2023 00:27:35 GMT
ENV SERVER=
# Fri, 13 Jan 2023 00:27:35 GMT
ENV LISTEN=3333
# Fri, 13 Jan 2023 00:27:35 GMT
ENV OWNER=
# Fri, 13 Jan 2023 00:27:35 GMT
ENV USERFILE=eggdrop.user
# Fri, 13 Jan 2023 00:27:35 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 13 Jan 2023 00:27:35 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 13 Jan 2023 00:27:35 GMT
EXPOSE 3333
# Fri, 13 Jan 2023 00:27:36 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 13 Jan 2023 00:27:36 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 13 Jan 2023 00:27:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 13 Jan 2023 00:27:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdb365c6f8a662a987df4b9f8aa0a038b4ccf8835a9cf6a10c487d137c48493`  
		Last Modified: Sat, 12 Nov 2022 05:21:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc68fd90aec1c649bae31b0426236225d421b45b0010bc88add392ee53e0dcf0`  
		Last Modified: Sat, 12 Nov 2022 05:21:19 GMT  
		Size: 10.9 KB (10938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cc94fc4b8d42ca4dc27cfd6217256fb76fdab0a0f617ee8f065a731a48c63c`  
		Last Modified: Sat, 12 Nov 2022 05:21:20 GMT  
		Size: 2.8 MB (2757973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd82489832074ca9c453adef2c15f26a9c00b91e6f98130d05e597c73885e612`  
		Last Modified: Fri, 13 Jan 2023 00:28:02 GMT  
		Size: 6.5 MB (6517191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af6b466438ad682744d9ff6379d0062b9be29c597fc38be177850eaeb68caaf`  
		Last Modified: Fri, 13 Jan 2023 00:28:00 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81deeebc195165168a6834c0c1777bb6d0dcea1c7f888b8ae6a67a03251648e`  
		Last Modified: Fri, 13 Jan 2023 00:28:00 GMT  
		Size: 709.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:2e6713a770f040c96b1348ae867ddf680945961f20e56296fb648e44334d094a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11351107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76418ad6dd2e2504889a37074cfee45862977582faa2f84176fa28655678086d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:42:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 10 Feb 2023 21:42:51 GMT
RUN adduser -S eggdrop
# Fri, 10 Feb 2023 21:42:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 10 Feb 2023 21:42:54 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 10 Feb 2023 21:47:45 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 10 Feb 2023 21:47:46 GMT
ENV NICK=
# Fri, 10 Feb 2023 21:47:46 GMT
ENV SERVER=
# Fri, 10 Feb 2023 21:47:46 GMT
ENV LISTEN=3333
# Fri, 10 Feb 2023 21:47:46 GMT
ENV OWNER=
# Fri, 10 Feb 2023 21:47:46 GMT
ENV USERFILE=eggdrop.user
# Fri, 10 Feb 2023 21:47:46 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 10 Feb 2023 21:47:46 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 10 Feb 2023 21:47:46 GMT
EXPOSE 3333
# Fri, 10 Feb 2023 21:47:46 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 10 Feb 2023 21:47:47 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 10 Feb 2023 21:47:47 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 10 Feb 2023 21:47:47 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebba4b8c34971e6a498979c6107bc2c520916759d9a60021708a684d6172e9f`  
		Last Modified: Fri, 10 Feb 2023 21:48:31 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eeabe531729b75a7f7a7be996edbbec2c25c2367d4a84b90d6b6ccc034aced`  
		Last Modified: Fri, 10 Feb 2023 21:48:29 GMT  
		Size: 10.6 KB (10638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e948308e6dcabd05ef9e0fc8fffe8bf9cd89f6411ed40c8c9d2b5d9d57f833f`  
		Last Modified: Fri, 10 Feb 2023 21:48:30 GMT  
		Size: 2.7 MB (2679697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d260cac25ffd7a3a755e0ef262e9f8792b1e5e5d425113c3860ba914b43bb195`  
		Last Modified: Fri, 10 Feb 2023 21:48:31 GMT  
		Size: 6.0 MB (6040214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1328d505b49745606af0c5bfce492c547fb94c06b991f9adc37fc98833dc9f73`  
		Last Modified: Fri, 10 Feb 2023 21:48:29 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f48efa80887cfac5596e7b2d79128ee8c363e21ffbe087b223fdb9b6fe84db`  
		Last Modified: Fri, 10 Feb 2023 21:48:29 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:1c7967dde971d677a4171a266645bebd6cc600eef70813b3accd66d4d2b45ae2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11668449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4af97b3fefa9ed49c50147740fa45b6aefa32e3af0099bdef5807c5c6ea782`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:57 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 10 Feb 2023 22:14:58 GMT
RUN adduser -S eggdrop
# Fri, 10 Feb 2023 22:14:59 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 10 Feb 2023 22:15:00 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 10 Feb 2023 22:18:43 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 10 Feb 2023 22:18:43 GMT
ENV NICK=
# Fri, 10 Feb 2023 22:18:43 GMT
ENV SERVER=
# Fri, 10 Feb 2023 22:18:43 GMT
ENV LISTEN=3333
# Fri, 10 Feb 2023 22:18:44 GMT
ENV OWNER=
# Fri, 10 Feb 2023 22:18:44 GMT
ENV USERFILE=eggdrop.user
# Fri, 10 Feb 2023 22:18:44 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 10 Feb 2023 22:18:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 10 Feb 2023 22:18:44 GMT
EXPOSE 3333
# Fri, 10 Feb 2023 22:18:44 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 10 Feb 2023 22:18:44 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 10 Feb 2023 22:18:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 10 Feb 2023 22:18:44 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb182a5cc1394eccbeeef59c5ad5d259ed5ddd4cdd2a1d4c5ad107256b7a2ee`  
		Last Modified: Fri, 10 Feb 2023 22:19:08 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59923206b30ea4054c1bb753aa8a5404a199d12f865dc365b1f8eb66fdb817b`  
		Last Modified: Fri, 10 Feb 2023 22:19:06 GMT  
		Size: 10.7 KB (10747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dd68e4187ad121351dbe2536603e4802110332e9e21ecccff44b92d2ea68b5`  
		Last Modified: Fri, 10 Feb 2023 22:19:07 GMT  
		Size: 2.8 MB (2776467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7285c61bf7d00d3cc40563b07cc910cfc6f1cbf6c20e0aa7b1b56e3ed8c069d`  
		Last Modified: Fri, 10 Feb 2023 22:19:07 GMT  
		Size: 6.2 MB (6167927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14d023f19ac2bdabff1a6f56426d0cd6782fe4048edf76831b7c32e64f915b2`  
		Last Modified: Fri, 10 Feb 2023 22:19:06 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282c5ded3cb4dd851d61d8a68894034bc8279f449025b2ad2c0b4a6e9361cc6`  
		Last Modified: Fri, 10 Feb 2023 22:19:06 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.4`

```console
$ docker pull eggdrop@sha256:7894b941d338db107cecf5d70ff99870f215da85604df9155f390d82c0a0b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.4` - linux; amd64

```console
$ docker pull eggdrop@sha256:9bd4adb3f737baa8bfa4bdd21695badd88ac8888e96f09ce3222a5fd00ed3b8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12096201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea8761751c3b6130b136e2142d22239339bde7c9cb0a5c5d297cb1f5bbf1113`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:20:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 12 Nov 2022 05:20:03 GMT
RUN adduser -S eggdrop
# Sat, 12 Nov 2022 05:20:04 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 05:20:06 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 13 Jan 2023 00:27:34 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 13 Jan 2023 00:27:35 GMT
ENV NICK=
# Fri, 13 Jan 2023 00:27:35 GMT
ENV SERVER=
# Fri, 13 Jan 2023 00:27:35 GMT
ENV LISTEN=3333
# Fri, 13 Jan 2023 00:27:35 GMT
ENV OWNER=
# Fri, 13 Jan 2023 00:27:35 GMT
ENV USERFILE=eggdrop.user
# Fri, 13 Jan 2023 00:27:35 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 13 Jan 2023 00:27:35 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 13 Jan 2023 00:27:35 GMT
EXPOSE 3333
# Fri, 13 Jan 2023 00:27:36 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 13 Jan 2023 00:27:36 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 13 Jan 2023 00:27:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 13 Jan 2023 00:27:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdb365c6f8a662a987df4b9f8aa0a038b4ccf8835a9cf6a10c487d137c48493`  
		Last Modified: Sat, 12 Nov 2022 05:21:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc68fd90aec1c649bae31b0426236225d421b45b0010bc88add392ee53e0dcf0`  
		Last Modified: Sat, 12 Nov 2022 05:21:19 GMT  
		Size: 10.9 KB (10938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cc94fc4b8d42ca4dc27cfd6217256fb76fdab0a0f617ee8f065a731a48c63c`  
		Last Modified: Sat, 12 Nov 2022 05:21:20 GMT  
		Size: 2.8 MB (2757973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd82489832074ca9c453adef2c15f26a9c00b91e6f98130d05e597c73885e612`  
		Last Modified: Fri, 13 Jan 2023 00:28:02 GMT  
		Size: 6.5 MB (6517191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af6b466438ad682744d9ff6379d0062b9be29c597fc38be177850eaeb68caaf`  
		Last Modified: Fri, 13 Jan 2023 00:28:00 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81deeebc195165168a6834c0c1777bb6d0dcea1c7f888b8ae6a67a03251648e`  
		Last Modified: Fri, 13 Jan 2023 00:28:00 GMT  
		Size: 709.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.4` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:2e6713a770f040c96b1348ae867ddf680945961f20e56296fb648e44334d094a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11351107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76418ad6dd2e2504889a37074cfee45862977582faa2f84176fa28655678086d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:42:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 10 Feb 2023 21:42:51 GMT
RUN adduser -S eggdrop
# Fri, 10 Feb 2023 21:42:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 10 Feb 2023 21:42:54 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 10 Feb 2023 21:47:45 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 10 Feb 2023 21:47:46 GMT
ENV NICK=
# Fri, 10 Feb 2023 21:47:46 GMT
ENV SERVER=
# Fri, 10 Feb 2023 21:47:46 GMT
ENV LISTEN=3333
# Fri, 10 Feb 2023 21:47:46 GMT
ENV OWNER=
# Fri, 10 Feb 2023 21:47:46 GMT
ENV USERFILE=eggdrop.user
# Fri, 10 Feb 2023 21:47:46 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 10 Feb 2023 21:47:46 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 10 Feb 2023 21:47:46 GMT
EXPOSE 3333
# Fri, 10 Feb 2023 21:47:46 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 10 Feb 2023 21:47:47 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 10 Feb 2023 21:47:47 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 10 Feb 2023 21:47:47 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebba4b8c34971e6a498979c6107bc2c520916759d9a60021708a684d6172e9f`  
		Last Modified: Fri, 10 Feb 2023 21:48:31 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eeabe531729b75a7f7a7be996edbbec2c25c2367d4a84b90d6b6ccc034aced`  
		Last Modified: Fri, 10 Feb 2023 21:48:29 GMT  
		Size: 10.6 KB (10638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e948308e6dcabd05ef9e0fc8fffe8bf9cd89f6411ed40c8c9d2b5d9d57f833f`  
		Last Modified: Fri, 10 Feb 2023 21:48:30 GMT  
		Size: 2.7 MB (2679697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d260cac25ffd7a3a755e0ef262e9f8792b1e5e5d425113c3860ba914b43bb195`  
		Last Modified: Fri, 10 Feb 2023 21:48:31 GMT  
		Size: 6.0 MB (6040214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1328d505b49745606af0c5bfce492c547fb94c06b991f9adc37fc98833dc9f73`  
		Last Modified: Fri, 10 Feb 2023 21:48:29 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f48efa80887cfac5596e7b2d79128ee8c363e21ffbe087b223fdb9b6fe84db`  
		Last Modified: Fri, 10 Feb 2023 21:48:29 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.4` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:1c7967dde971d677a4171a266645bebd6cc600eef70813b3accd66d4d2b45ae2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11668449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4af97b3fefa9ed49c50147740fa45b6aefa32e3af0099bdef5807c5c6ea782`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:57 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 10 Feb 2023 22:14:58 GMT
RUN adduser -S eggdrop
# Fri, 10 Feb 2023 22:14:59 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 10 Feb 2023 22:15:00 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 10 Feb 2023 22:18:43 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 10 Feb 2023 22:18:43 GMT
ENV NICK=
# Fri, 10 Feb 2023 22:18:43 GMT
ENV SERVER=
# Fri, 10 Feb 2023 22:18:43 GMT
ENV LISTEN=3333
# Fri, 10 Feb 2023 22:18:44 GMT
ENV OWNER=
# Fri, 10 Feb 2023 22:18:44 GMT
ENV USERFILE=eggdrop.user
# Fri, 10 Feb 2023 22:18:44 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 10 Feb 2023 22:18:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 10 Feb 2023 22:18:44 GMT
EXPOSE 3333
# Fri, 10 Feb 2023 22:18:44 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 10 Feb 2023 22:18:44 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 10 Feb 2023 22:18:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 10 Feb 2023 22:18:44 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb182a5cc1394eccbeeef59c5ad5d259ed5ddd4cdd2a1d4c5ad107256b7a2ee`  
		Last Modified: Fri, 10 Feb 2023 22:19:08 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59923206b30ea4054c1bb753aa8a5404a199d12f865dc365b1f8eb66fdb817b`  
		Last Modified: Fri, 10 Feb 2023 22:19:06 GMT  
		Size: 10.7 KB (10747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dd68e4187ad121351dbe2536603e4802110332e9e21ecccff44b92d2ea68b5`  
		Last Modified: Fri, 10 Feb 2023 22:19:07 GMT  
		Size: 2.8 MB (2776467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7285c61bf7d00d3cc40563b07cc910cfc6f1cbf6c20e0aa7b1b56e3ed8c069d`  
		Last Modified: Fri, 10 Feb 2023 22:19:07 GMT  
		Size: 6.2 MB (6167927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14d023f19ac2bdabff1a6f56426d0cd6782fe4048edf76831b7c32e64f915b2`  
		Last Modified: Fri, 10 Feb 2023 22:19:06 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282c5ded3cb4dd851d61d8a68894034bc8279f449025b2ad2c0b4a6e9361cc6`  
		Last Modified: Fri, 10 Feb 2023 22:19:06 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:4c5b8b5635127f5b9bfc67c8c808b1ff2b23f52bc52fdca70526b67a0bd1ad2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:60922ed1b032320672c726959583f441dfd9990c236a79a5d99a34f876dc45ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16092986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd3ae787c0421886ce74d9bcc4b90717abd197520e31ccda45c5ea03f5d5c61`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:37:01 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:37:02 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:37:03 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Mon, 02 Jan 2023 18:23:23 GMT
ENV EGGDROP_SHA256=caafc1ad001e2e77793dca37998cb94d88efadb4ec9c3de44c1004b04f15aa6e
# Mon, 02 Jan 2023 18:23:23 GMT
ENV EGGDROP_COMMIT=2a6a36888f5aa2204d84a9e6282d35e5421c2c8a
# Mon, 02 Jan 2023 18:23:24 GMT
RUN apk --update add --no-cache bash openssl
# Fri, 13 Jan 2023 00:23:19 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 13 Jan 2023 00:23:20 GMT
ENV NICK=
# Fri, 13 Jan 2023 00:23:20 GMT
ENV SERVER=
# Fri, 13 Jan 2023 00:23:20 GMT
ENV LISTEN=3333
# Fri, 13 Jan 2023 00:23:20 GMT
ENV OWNER=
# Fri, 13 Jan 2023 00:23:20 GMT
ENV USERFILE=eggdrop.user
# Fri, 13 Jan 2023 00:23:20 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 13 Jan 2023 00:23:20 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 13 Jan 2023 00:23:20 GMT
EXPOSE 3333
# Fri, 13 Jan 2023 00:23:20 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Fri, 13 Jan 2023 00:23:21 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 13 Jan 2023 00:23:21 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 13 Jan 2023 00:23:21 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd629a2e1daaf15d9fdb2bd171b0a8c0622c4f982e7a6b1059c076fb9e1b42e5`  
		Last Modified: Thu, 06 Oct 2022 20:42:28 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfd741c22df00a71bc308727ead4698aa665f26cbf98ae6e3899b5c94acef40`  
		Last Modified: Thu, 06 Oct 2022 20:42:26 GMT  
		Size: 10.9 KB (10941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689efdd2fe8f24ef5736ec9110f67ae9b0ac450c5533cce1bad38d76192346ea`  
		Last Modified: Mon, 02 Jan 2023 18:27:42 GMT  
		Size: 1.1 MB (1090156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f209da62c6cf69bb823010f5b7b7dba2cd98a91117e48010158d182f57d10e8`  
		Last Modified: Fri, 13 Jan 2023 00:27:55 GMT  
		Size: 12.2 MB (12164137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde85e25a2f72925b67e83b6b733c02a82c0a0910dcbb35025e4407b853b086c`  
		Last Modified: Fri, 13 Jan 2023 00:27:53 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c61de8ba182741492a2713fbe554efca0f46e0cde9e062ece7eede0a388e847`  
		Last Modified: Fri, 13 Jan 2023 00:27:53 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:e0fa47cfd9fa6dc31a394322cfd13f9987f5d25b1a5a0a712cf4fa2e3ddb9184
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14206582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8ae3b78dc040b9b8f8cf2e7a0686df86b57d49f1aefa5d90915c0335ea9b5d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:37:52 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 10 Feb 2023 21:37:53 GMT
RUN adduser -S eggdrop
# Fri, 10 Feb 2023 21:37:54 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 10 Feb 2023 21:37:54 GMT
ENV EGGDROP_SHA256=caafc1ad001e2e77793dca37998cb94d88efadb4ec9c3de44c1004b04f15aa6e
# Fri, 10 Feb 2023 21:37:54 GMT
ENV EGGDROP_COMMIT=2a6a36888f5aa2204d84a9e6282d35e5421c2c8a
# Fri, 10 Feb 2023 21:37:55 GMT
RUN apk --update add --no-cache bash openssl
# Fri, 10 Feb 2023 21:42:32 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 10 Feb 2023 21:42:32 GMT
ENV NICK=
# Fri, 10 Feb 2023 21:42:32 GMT
ENV SERVER=
# Fri, 10 Feb 2023 21:42:32 GMT
ENV LISTEN=3333
# Fri, 10 Feb 2023 21:42:32 GMT
ENV OWNER=
# Fri, 10 Feb 2023 21:42:32 GMT
ENV USERFILE=eggdrop.user
# Fri, 10 Feb 2023 21:42:32 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 10 Feb 2023 21:42:33 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 10 Feb 2023 21:42:33 GMT
EXPOSE 3333
# Fri, 10 Feb 2023 21:42:33 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Fri, 10 Feb 2023 21:42:33 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 10 Feb 2023 21:42:33 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 10 Feb 2023 21:42:33 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f307beb202bf7bcb9f58f8618b7432e52e14968b9385535f4e39797968d74f8b`  
		Last Modified: Fri, 10 Feb 2023 21:48:21 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a354c31f5821795ab52a25590b1f334e39b185b48944b37a40bf24f00adae7b`  
		Last Modified: Fri, 10 Feb 2023 21:48:19 GMT  
		Size: 10.7 KB (10664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7c85aa1c4a6fd356326cfbd33efa281fbe307459395fa44f8c93d2153dbabe`  
		Last Modified: Fri, 10 Feb 2023 21:48:20 GMT  
		Size: 1.0 MB (1032643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f546ee4bee6b79f21ef60660bef00537300c078242686b5c1d674b037c5710`  
		Last Modified: Fri, 10 Feb 2023 21:48:22 GMT  
		Size: 10.5 MB (10525426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63c8e523cbc37eca1c7d4c4fa5fc103e59c9967de70527dfb74123834a4573aa`  
		Last Modified: Fri, 10 Feb 2023 21:48:19 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5047508085650a4453fb14e59e7833d27def38a4274ab51871b3ffd257d5c4`  
		Last Modified: Fri, 10 Feb 2023 21:48:19 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:26af7de37409a702a7bd1048793bcd79b6f4e09009b868fc8416b8f5b56dbf93
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14550585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ba771920e448dac75c2718eefb8f3804c256a950370983d0267c774f31e5b4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:10:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 10 Feb 2023 22:10:50 GMT
RUN adduser -S eggdrop
# Fri, 10 Feb 2023 22:10:51 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 10 Feb 2023 22:10:51 GMT
ENV EGGDROP_SHA256=caafc1ad001e2e77793dca37998cb94d88efadb4ec9c3de44c1004b04f15aa6e
# Fri, 10 Feb 2023 22:10:51 GMT
ENV EGGDROP_COMMIT=2a6a36888f5aa2204d84a9e6282d35e5421c2c8a
# Fri, 10 Feb 2023 22:10:52 GMT
RUN apk --update add --no-cache bash openssl
# Fri, 10 Feb 2023 22:14:41 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 10 Feb 2023 22:14:41 GMT
ENV NICK=
# Fri, 10 Feb 2023 22:14:41 GMT
ENV SERVER=
# Fri, 10 Feb 2023 22:14:41 GMT
ENV LISTEN=3333
# Fri, 10 Feb 2023 22:14:41 GMT
ENV OWNER=
# Fri, 10 Feb 2023 22:14:41 GMT
ENV USERFILE=eggdrop.user
# Fri, 10 Feb 2023 22:14:42 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 10 Feb 2023 22:14:42 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 10 Feb 2023 22:14:42 GMT
EXPOSE 3333
# Fri, 10 Feb 2023 22:14:42 GMT
COPY file:35e05bb72116a1848ec779e3fbc4ea6bbcd95ceb11059751f608c8543e18cde7 in /home/eggdrop/eggdrop 
# Fri, 10 Feb 2023 22:14:42 GMT
COPY file:f30bcb89ff6df7709069d6cc97353d72cdbbebc6530d8d350cbb3ae4dad79129 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 10 Feb 2023 22:14:42 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 10 Feb 2023 22:14:42 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8186b969b70bfd3a8f8529034203efaf95ad8eddf3c33fb41cf503890b1700b`  
		Last Modified: Fri, 10 Feb 2023 22:19:00 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212afe5219f2149a8e95b00c1346982e164235c46e289d221ac1897ca9048c2f`  
		Last Modified: Fri, 10 Feb 2023 22:18:58 GMT  
		Size: 10.8 KB (10769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166b6dcf0dd4056b6515bde1969fd9a9008e4ada399c4be2c520075ebedf32c1`  
		Last Modified: Fri, 10 Feb 2023 22:18:59 GMT  
		Size: 1.1 MB (1087885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574ab5da52d2e1338b4d9359da1ce06f3ac8e7c13ca6642062bd8c97bb50784a`  
		Last Modified: Fri, 10 Feb 2023 22:19:00 GMT  
		Size: 10.7 MB (10726155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0658130289555357b4bcc32867d0e841e43ac3fd260ec6a79cea1100c2137330`  
		Last Modified: Fri, 10 Feb 2023 22:18:59 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3515ad107ce1fa3f7bc67db346f13973d805d0f9d98ffbe4de99c20385698aa7`  
		Last Modified: Fri, 10 Feb 2023 22:18:58 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:7894b941d338db107cecf5d70ff99870f215da85604df9155f390d82c0a0b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:9bd4adb3f737baa8bfa4bdd21695badd88ac8888e96f09ce3222a5fd00ed3b8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12096201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea8761751c3b6130b136e2142d22239339bde7c9cb0a5c5d297cb1f5bbf1113`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:20:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 12 Nov 2022 05:20:03 GMT
RUN adduser -S eggdrop
# Sat, 12 Nov 2022 05:20:04 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 05:20:06 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 13 Jan 2023 00:27:34 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 13 Jan 2023 00:27:35 GMT
ENV NICK=
# Fri, 13 Jan 2023 00:27:35 GMT
ENV SERVER=
# Fri, 13 Jan 2023 00:27:35 GMT
ENV LISTEN=3333
# Fri, 13 Jan 2023 00:27:35 GMT
ENV OWNER=
# Fri, 13 Jan 2023 00:27:35 GMT
ENV USERFILE=eggdrop.user
# Fri, 13 Jan 2023 00:27:35 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 13 Jan 2023 00:27:35 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 13 Jan 2023 00:27:35 GMT
EXPOSE 3333
# Fri, 13 Jan 2023 00:27:36 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 13 Jan 2023 00:27:36 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 13 Jan 2023 00:27:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 13 Jan 2023 00:27:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdb365c6f8a662a987df4b9f8aa0a038b4ccf8835a9cf6a10c487d137c48493`  
		Last Modified: Sat, 12 Nov 2022 05:21:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc68fd90aec1c649bae31b0426236225d421b45b0010bc88add392ee53e0dcf0`  
		Last Modified: Sat, 12 Nov 2022 05:21:19 GMT  
		Size: 10.9 KB (10938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cc94fc4b8d42ca4dc27cfd6217256fb76fdab0a0f617ee8f065a731a48c63c`  
		Last Modified: Sat, 12 Nov 2022 05:21:20 GMT  
		Size: 2.8 MB (2757973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd82489832074ca9c453adef2c15f26a9c00b91e6f98130d05e597c73885e612`  
		Last Modified: Fri, 13 Jan 2023 00:28:02 GMT  
		Size: 6.5 MB (6517191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af6b466438ad682744d9ff6379d0062b9be29c597fc38be177850eaeb68caaf`  
		Last Modified: Fri, 13 Jan 2023 00:28:00 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81deeebc195165168a6834c0c1777bb6d0dcea1c7f888b8ae6a67a03251648e`  
		Last Modified: Fri, 13 Jan 2023 00:28:00 GMT  
		Size: 709.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:2e6713a770f040c96b1348ae867ddf680945961f20e56296fb648e44334d094a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11351107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76418ad6dd2e2504889a37074cfee45862977582faa2f84176fa28655678086d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:42:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 10 Feb 2023 21:42:51 GMT
RUN adduser -S eggdrop
# Fri, 10 Feb 2023 21:42:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 10 Feb 2023 21:42:54 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 10 Feb 2023 21:47:45 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 10 Feb 2023 21:47:46 GMT
ENV NICK=
# Fri, 10 Feb 2023 21:47:46 GMT
ENV SERVER=
# Fri, 10 Feb 2023 21:47:46 GMT
ENV LISTEN=3333
# Fri, 10 Feb 2023 21:47:46 GMT
ENV OWNER=
# Fri, 10 Feb 2023 21:47:46 GMT
ENV USERFILE=eggdrop.user
# Fri, 10 Feb 2023 21:47:46 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 10 Feb 2023 21:47:46 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 10 Feb 2023 21:47:46 GMT
EXPOSE 3333
# Fri, 10 Feb 2023 21:47:46 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 10 Feb 2023 21:47:47 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 10 Feb 2023 21:47:47 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 10 Feb 2023 21:47:47 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebba4b8c34971e6a498979c6107bc2c520916759d9a60021708a684d6172e9f`  
		Last Modified: Fri, 10 Feb 2023 21:48:31 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eeabe531729b75a7f7a7be996edbbec2c25c2367d4a84b90d6b6ccc034aced`  
		Last Modified: Fri, 10 Feb 2023 21:48:29 GMT  
		Size: 10.6 KB (10638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e948308e6dcabd05ef9e0fc8fffe8bf9cd89f6411ed40c8c9d2b5d9d57f833f`  
		Last Modified: Fri, 10 Feb 2023 21:48:30 GMT  
		Size: 2.7 MB (2679697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d260cac25ffd7a3a755e0ef262e9f8792b1e5e5d425113c3860ba914b43bb195`  
		Last Modified: Fri, 10 Feb 2023 21:48:31 GMT  
		Size: 6.0 MB (6040214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1328d505b49745606af0c5bfce492c547fb94c06b991f9adc37fc98833dc9f73`  
		Last Modified: Fri, 10 Feb 2023 21:48:29 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f48efa80887cfac5596e7b2d79128ee8c363e21ffbe087b223fdb9b6fe84db`  
		Last Modified: Fri, 10 Feb 2023 21:48:29 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:1c7967dde971d677a4171a266645bebd6cc600eef70813b3accd66d4d2b45ae2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11668449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4af97b3fefa9ed49c50147740fa45b6aefa32e3af0099bdef5807c5c6ea782`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:57 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 10 Feb 2023 22:14:58 GMT
RUN adduser -S eggdrop
# Fri, 10 Feb 2023 22:14:59 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 10 Feb 2023 22:15:00 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 10 Feb 2023 22:18:43 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 10 Feb 2023 22:18:43 GMT
ENV NICK=
# Fri, 10 Feb 2023 22:18:43 GMT
ENV SERVER=
# Fri, 10 Feb 2023 22:18:43 GMT
ENV LISTEN=3333
# Fri, 10 Feb 2023 22:18:44 GMT
ENV OWNER=
# Fri, 10 Feb 2023 22:18:44 GMT
ENV USERFILE=eggdrop.user
# Fri, 10 Feb 2023 22:18:44 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 10 Feb 2023 22:18:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 10 Feb 2023 22:18:44 GMT
EXPOSE 3333
# Fri, 10 Feb 2023 22:18:44 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 10 Feb 2023 22:18:44 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 10 Feb 2023 22:18:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 10 Feb 2023 22:18:44 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb182a5cc1394eccbeeef59c5ad5d259ed5ddd4cdd2a1d4c5ad107256b7a2ee`  
		Last Modified: Fri, 10 Feb 2023 22:19:08 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59923206b30ea4054c1bb753aa8a5404a199d12f865dc365b1f8eb66fdb817b`  
		Last Modified: Fri, 10 Feb 2023 22:19:06 GMT  
		Size: 10.7 KB (10747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dd68e4187ad121351dbe2536603e4802110332e9e21ecccff44b92d2ea68b5`  
		Last Modified: Fri, 10 Feb 2023 22:19:07 GMT  
		Size: 2.8 MB (2776467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7285c61bf7d00d3cc40563b07cc910cfc6f1cbf6c20e0aa7b1b56e3ed8c069d`  
		Last Modified: Fri, 10 Feb 2023 22:19:07 GMT  
		Size: 6.2 MB (6167927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14d023f19ac2bdabff1a6f56426d0cd6782fe4048edf76831b7c32e64f915b2`  
		Last Modified: Fri, 10 Feb 2023 22:19:06 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282c5ded3cb4dd851d61d8a68894034bc8279f449025b2ad2c0b4a6e9361cc6`  
		Last Modified: Fri, 10 Feb 2023 22:19:06 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:7894b941d338db107cecf5d70ff99870f215da85604df9155f390d82c0a0b4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:9bd4adb3f737baa8bfa4bdd21695badd88ac8888e96f09ce3222a5fd00ed3b8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12096201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea8761751c3b6130b136e2142d22239339bde7c9cb0a5c5d297cb1f5bbf1113`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:20:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 12 Nov 2022 05:20:03 GMT
RUN adduser -S eggdrop
# Sat, 12 Nov 2022 05:20:04 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 12 Nov 2022 05:20:06 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 13 Jan 2023 00:27:34 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 13 Jan 2023 00:27:35 GMT
ENV NICK=
# Fri, 13 Jan 2023 00:27:35 GMT
ENV SERVER=
# Fri, 13 Jan 2023 00:27:35 GMT
ENV LISTEN=3333
# Fri, 13 Jan 2023 00:27:35 GMT
ENV OWNER=
# Fri, 13 Jan 2023 00:27:35 GMT
ENV USERFILE=eggdrop.user
# Fri, 13 Jan 2023 00:27:35 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 13 Jan 2023 00:27:35 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 13 Jan 2023 00:27:35 GMT
EXPOSE 3333
# Fri, 13 Jan 2023 00:27:36 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 13 Jan 2023 00:27:36 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 13 Jan 2023 00:27:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 13 Jan 2023 00:27:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cdb365c6f8a662a987df4b9f8aa0a038b4ccf8835a9cf6a10c487d137c48493`  
		Last Modified: Sat, 12 Nov 2022 05:21:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc68fd90aec1c649bae31b0426236225d421b45b0010bc88add392ee53e0dcf0`  
		Last Modified: Sat, 12 Nov 2022 05:21:19 GMT  
		Size: 10.9 KB (10938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cc94fc4b8d42ca4dc27cfd6217256fb76fdab0a0f617ee8f065a731a48c63c`  
		Last Modified: Sat, 12 Nov 2022 05:21:20 GMT  
		Size: 2.8 MB (2757973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd82489832074ca9c453adef2c15f26a9c00b91e6f98130d05e597c73885e612`  
		Last Modified: Fri, 13 Jan 2023 00:28:02 GMT  
		Size: 6.5 MB (6517191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af6b466438ad682744d9ff6379d0062b9be29c597fc38be177850eaeb68caaf`  
		Last Modified: Fri, 13 Jan 2023 00:28:00 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81deeebc195165168a6834c0c1777bb6d0dcea1c7f888b8ae6a67a03251648e`  
		Last Modified: Fri, 13 Jan 2023 00:28:00 GMT  
		Size: 709.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:2e6713a770f040c96b1348ae867ddf680945961f20e56296fb648e44334d094a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11351107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76418ad6dd2e2504889a37074cfee45862977582faa2f84176fa28655678086d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:42:51 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 10 Feb 2023 21:42:51 GMT
RUN adduser -S eggdrop
# Fri, 10 Feb 2023 21:42:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 10 Feb 2023 21:42:54 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 10 Feb 2023 21:47:45 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 10 Feb 2023 21:47:46 GMT
ENV NICK=
# Fri, 10 Feb 2023 21:47:46 GMT
ENV SERVER=
# Fri, 10 Feb 2023 21:47:46 GMT
ENV LISTEN=3333
# Fri, 10 Feb 2023 21:47:46 GMT
ENV OWNER=
# Fri, 10 Feb 2023 21:47:46 GMT
ENV USERFILE=eggdrop.user
# Fri, 10 Feb 2023 21:47:46 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 10 Feb 2023 21:47:46 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 10 Feb 2023 21:47:46 GMT
EXPOSE 3333
# Fri, 10 Feb 2023 21:47:46 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 10 Feb 2023 21:47:47 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 10 Feb 2023 21:47:47 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 10 Feb 2023 21:47:47 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebba4b8c34971e6a498979c6107bc2c520916759d9a60021708a684d6172e9f`  
		Last Modified: Fri, 10 Feb 2023 21:48:31 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eeabe531729b75a7f7a7be996edbbec2c25c2367d4a84b90d6b6ccc034aced`  
		Last Modified: Fri, 10 Feb 2023 21:48:29 GMT  
		Size: 10.6 KB (10638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e948308e6dcabd05ef9e0fc8fffe8bf9cd89f6411ed40c8c9d2b5d9d57f833f`  
		Last Modified: Fri, 10 Feb 2023 21:48:30 GMT  
		Size: 2.7 MB (2679697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d260cac25ffd7a3a755e0ef262e9f8792b1e5e5d425113c3860ba914b43bb195`  
		Last Modified: Fri, 10 Feb 2023 21:48:31 GMT  
		Size: 6.0 MB (6040214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1328d505b49745606af0c5bfce492c547fb94c06b991f9adc37fc98833dc9f73`  
		Last Modified: Fri, 10 Feb 2023 21:48:29 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f48efa80887cfac5596e7b2d79128ee8c363e21ffbe087b223fdb9b6fe84db`  
		Last Modified: Fri, 10 Feb 2023 21:48:29 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:1c7967dde971d677a4171a266645bebd6cc600eef70813b3accd66d4d2b45ae2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11668449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4af97b3fefa9ed49c50147740fa45b6aefa32e3af0099bdef5807c5c6ea782`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:14:57 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 10 Feb 2023 22:14:58 GMT
RUN adduser -S eggdrop
# Fri, 10 Feb 2023 22:14:59 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 10 Feb 2023 22:15:00 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 10 Feb 2023 22:18:43 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.4.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.4.tar.gz.asc eggdrop-1.9.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.4.tar.gz.asc   && tar -zxvf eggdrop-1.9.4.tar.gz   && rm eggdrop-1.9.4.tar.gz   && ( cd eggdrop-1.9.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 10 Feb 2023 22:18:43 GMT
ENV NICK=
# Fri, 10 Feb 2023 22:18:43 GMT
ENV SERVER=
# Fri, 10 Feb 2023 22:18:43 GMT
ENV LISTEN=3333
# Fri, 10 Feb 2023 22:18:44 GMT
ENV OWNER=
# Fri, 10 Feb 2023 22:18:44 GMT
ENV USERFILE=eggdrop.user
# Fri, 10 Feb 2023 22:18:44 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 10 Feb 2023 22:18:44 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 10 Feb 2023 22:18:44 GMT
EXPOSE 3333
# Fri, 10 Feb 2023 22:18:44 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 10 Feb 2023 22:18:44 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 10 Feb 2023 22:18:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 10 Feb 2023 22:18:44 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb182a5cc1394eccbeeef59c5ad5d259ed5ddd4cdd2a1d4c5ad107256b7a2ee`  
		Last Modified: Fri, 10 Feb 2023 22:19:08 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59923206b30ea4054c1bb753aa8a5404a199d12f865dc365b1f8eb66fdb817b`  
		Last Modified: Fri, 10 Feb 2023 22:19:06 GMT  
		Size: 10.7 KB (10747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dd68e4187ad121351dbe2536603e4802110332e9e21ecccff44b92d2ea68b5`  
		Last Modified: Fri, 10 Feb 2023 22:19:07 GMT  
		Size: 2.8 MB (2776467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7285c61bf7d00d3cc40563b07cc910cfc6f1cbf6c20e0aa7b1b56e3ed8c069d`  
		Last Modified: Fri, 10 Feb 2023 22:19:07 GMT  
		Size: 6.2 MB (6167927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14d023f19ac2bdabff1a6f56426d0cd6782fe4048edf76831b7c32e64f915b2`  
		Last Modified: Fri, 10 Feb 2023 22:19:06 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b282c5ded3cb4dd851d61d8a68894034bc8279f449025b2ad2c0b4a6e9361cc6`  
		Last Modified: Fri, 10 Feb 2023 22:19:06 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
