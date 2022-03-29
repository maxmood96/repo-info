## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:5b10997c6073911238c5c8b8b353f5fe68bf0f4ef8e9c5ce92aa8fd402436fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:1aeebd57ae1707c3710b46b7e33409e2b0fbfe6493731ea692e380dba408e394
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39770851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4694c76ab607e85da34b92dae862739842f70ab6d675902bacd27bbab2b959`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:58:38 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 11:58:39 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 11:58:40 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 11:58:40 GMT
ENV EGGDROP_SHA256=85700bdd1e5e709e7ac44fc4cac3bf06ab674ead4fb1df99f1ba8cb892c27a3c
# Tue, 29 Mar 2022 11:58:40 GMT
ENV EGGDROP_COMMIT=6959f1943659db6117b93262d18b27dd98313206
# Tue, 29 Mar 2022 11:58:41 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 29 Mar 2022 12:02:29 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 12:02:29 GMT
ENV NICK=
# Tue, 29 Mar 2022 12:02:29 GMT
ENV SERVER=
# Tue, 29 Mar 2022 12:02:29 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 12:02:30 GMT
ENV OWNER=
# Tue, 29 Mar 2022 12:02:30 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 12:02:30 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 12:02:30 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 12:02:30 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 12:02:30 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 12:02:30 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 12:02:30 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 12:02:30 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fb61010abf5a69cbde6fef350ccb3f1cccdb738a529a130007939fb12aa7bc`  
		Last Modified: Tue, 29 Mar 2022 12:04:07 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ca98fe50b6a7460ca0403abdbdfe56f9f0f65ad028d0646a1c426a65a2af26`  
		Last Modified: Tue, 29 Mar 2022 12:04:04 GMT  
		Size: 10.9 KB (10947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f973893e5f0430443a84b87f5d35b80d20b2609e7a32d53ff3b71851430c41`  
		Last Modified: Tue, 29 Mar 2022 12:04:05 GMT  
		Size: 1.1 MB (1089643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dc78d5804f959f865916cd011afe1cf55cbd14a725b5559f15dbff9c3dffe9`  
		Last Modified: Tue, 29 Mar 2022 12:04:10 GMT  
		Size: 35.9 MB (35851903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf69ecc0001bcbe74f66625dd25d9afecaa67722bfbb0385c300e9d9363fb542`  
		Last Modified: Tue, 29 Mar 2022 12:04:04 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa21b18065fc4618ccc656606eb3a3bab4b10bafb95838f61fd9181e2aca745`  
		Last Modified: Tue, 29 Mar 2022 12:04:04 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:36f6b063b1ae647368fb44b152165fa6fc54a61c5224ba4e8f497bf28e086a36
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39165960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff18f6351921aba72532c6816d77b850e26a75f3e98ff7f99e50e4f3e09ad8d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:24:20 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 12:24:21 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 12:24:24 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 12:24:24 GMT
ENV EGGDROP_SHA256=85700bdd1e5e709e7ac44fc4cac3bf06ab674ead4fb1df99f1ba8cb892c27a3c
# Tue, 29 Mar 2022 12:24:25 GMT
ENV EGGDROP_COMMIT=6959f1943659db6117b93262d18b27dd98313206
# Tue, 29 Mar 2022 12:24:27 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 29 Mar 2022 12:34:43 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 12:34:44 GMT
ENV NICK=
# Tue, 29 Mar 2022 12:34:45 GMT
ENV SERVER=
# Tue, 29 Mar 2022 12:34:45 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 12:34:45 GMT
ENV OWNER=
# Tue, 29 Mar 2022 12:34:46 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 12:34:46 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 12:34:47 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 12:34:47 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 12:34:48 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 12:34:48 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 12:34:48 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 12:34:49 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63240a16b38668f610edc5128f225a877039b118ae7f255a574b811a91b15e92`  
		Last Modified: Tue, 29 Mar 2022 12:38:16 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc9e6b8e28e12fa0728973197f40a2838c284d504a3db2249220cbc7ef19c42`  
		Last Modified: Tue, 29 Mar 2022 12:38:15 GMT  
		Size: 10.7 KB (10650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ffdfc75128ae9df071d1d654315e4d2ed9cd461e8c20b786ffbb24ec887cfe`  
		Last Modified: Tue, 29 Mar 2022 12:38:15 GMT  
		Size: 1.0 MB (1032375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed0edfb653bf36be23398e354e32830ee8a056d774e1bd208c0a2fa6dcbae01`  
		Last Modified: Tue, 29 Mar 2022 12:38:38 GMT  
		Size: 35.5 MB (35497132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a898162cb59c4690bd86db28d5e445f2d6495573c05c0e574ee4c9c269f50302`  
		Last Modified: Tue, 29 Mar 2022 12:38:15 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166051ee680cb8f2fb7f955de719075cc4131997e69246cc7db6f22cd1babb34`  
		Last Modified: Tue, 29 Mar 2022 12:38:15 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:bc754a00e69a169738dffcf72c407b245523b362270176024c41263ad49c351b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39840405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df4ec45f1c8cb1603eacfbb9975b2cc0340b1725074f2c3fd4b1bdd6a013e66`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 08:35:52 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 08:35:52 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 08:35:54 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 08:35:55 GMT
ENV EGGDROP_SHA256=85700bdd1e5e709e7ac44fc4cac3bf06ab674ead4fb1df99f1ba8cb892c27a3c
# Tue, 29 Mar 2022 08:35:56 GMT
ENV EGGDROP_COMMIT=6959f1943659db6117b93262d18b27dd98313206
# Tue, 29 Mar 2022 08:35:58 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 29 Mar 2022 08:43:43 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 08:43:43 GMT
ENV NICK=
# Tue, 29 Mar 2022 08:43:44 GMT
ENV SERVER=
# Tue, 29 Mar 2022 08:43:45 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 08:43:46 GMT
ENV OWNER=
# Tue, 29 Mar 2022 08:43:47 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 08:43:48 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 08:43:49 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 08:43:50 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 08:43:52 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 08:43:53 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 08:43:53 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 08:43:54 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425a67c2147c2518b3b50438a8d7490f7866e871f0eb779610655a1b089bde1f`  
		Last Modified: Tue, 29 Mar 2022 08:46:49 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc043abf221001c0161e89995789abe1b76005b6060c22f369b6e9c530e41f8`  
		Last Modified: Tue, 29 Mar 2022 08:46:47 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83de456a90a49bc3b5e97b1c59d545af8c85be9178b0ae791b3da36ebfcb3da9`  
		Last Modified: Tue, 29 Mar 2022 08:46:47 GMT  
		Size: 1.1 MB (1087187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a2b2d1d1dfc653139f172efdea79f3b49ea8d5474feb7534d100891a687a99`  
		Last Modified: Tue, 29 Mar 2022 08:46:52 GMT  
		Size: 36.0 MB (36022359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dde69589821aa666fa837ac41c1393d1368181edb56005f1bb1d99f204bd5e`  
		Last Modified: Tue, 29 Mar 2022 08:46:47 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0fcaa949de0630a27dda0655eeb28a12857d10fbd1f08737550eddc03d691e`  
		Last Modified: Tue, 29 Mar 2022 08:46:47 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
