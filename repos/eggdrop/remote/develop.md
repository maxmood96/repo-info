## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:6ee7a52bcd0a0df36a9d0d879f9163f4bb7a27622f44664d7458327bbd35aa59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:f3a796e0eed734f042c301033e0d380cdde7d24d7a50fd6e42da4582ec0c9b88
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13891828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f279cd52cc620f1b9c9159a45b4685fe6efa6a8e94c413c3667e19fb4e894c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Tue, 09 Mar 2021 01:19:30 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Mar 2021 01:19:31 GMT
RUN adduser -S eggdrop
# Tue, 09 Mar 2021 01:19:32 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Mar 2021 01:19:33 GMT
ENV EGGDROP_SHA256=2968824d5184d54bc2b0d6d3c746ca41cc8342523d919671f33ea2446fef0f36
# Tue, 09 Mar 2021 01:19:33 GMT
ENV EGGDROP_COMMIT=d01a34e163c47641eb9516ed918699b8822a7855
# Tue, 09 Mar 2021 01:19:34 GMT
RUN apk --update add --no-cache tcl bash openssl
# Tue, 09 Mar 2021 01:20:25 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Mar 2021 01:20:26 GMT
ENV NICK=
# Tue, 09 Mar 2021 01:20:26 GMT
ENV SERVER=
# Tue, 09 Mar 2021 01:20:26 GMT
ENV LISTEN=3333
# Tue, 09 Mar 2021 01:20:26 GMT
ENV OWNER=
# Tue, 09 Mar 2021 01:20:26 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Mar 2021 01:20:26 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Mar 2021 01:20:27 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Mar 2021 01:20:27 GMT
EXPOSE 3333
# Tue, 09 Mar 2021 01:20:27 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Tue, 09 Mar 2021 01:20:27 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Mar 2021 01:20:27 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Mar 2021 01:20:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24290d578d867a16df81fd07d9f0e95be4d141556d98cb53c0604378c0639b1e`  
		Last Modified: Tue, 09 Mar 2021 01:21:55 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e1f81881d5436a8846534949079dfb93f5548b9c25288fef08b0103015d3cb`  
		Last Modified: Tue, 09 Mar 2021 01:21:52 GMT  
		Size: 9.6 KB (9577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04d7d08d903f75e4c6ebe09363aa98bbb660881823b2722827e266b250fdbf6`  
		Last Modified: Tue, 09 Mar 2021 01:21:53 GMT  
		Size: 2.7 MB (2685306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dcea5841c269a5a3e82a958bb4690e7d1563cdde4c594cfece1b44045d32555`  
		Last Modified: Tue, 09 Mar 2021 01:21:53 GMT  
		Size: 8.4 MB (8377793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea2de41cea3d2bf1a8ff4ae66a771fb47fed97d0211433c5584a8a6b1ceb4cb`  
		Last Modified: Tue, 09 Mar 2021 01:21:52 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3033fd427c75ce43900555f6841a8ffe8abd67fbdc772c7a195e268381044406`  
		Last Modified: Tue, 09 Mar 2021 01:21:52 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b9c0898de30826dfd8e356e20fb0244d60e159dcb8e960f924485e0bbad14597
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13552601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f07d72e32ed608c48963a7301aef39fa6a18696b4359be55e2efd721f620ddb`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:45 GMT
ADD file:72743cfd9913f13553e700f9d9cfdc17b9dc793ebeeb337fd5fe02dc962d4b63 in / 
# Wed, 24 Feb 2021 20:50:46 GMT
CMD ["/bin/sh"]
# Thu, 25 Feb 2021 00:28:14 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 25 Feb 2021 00:28:19 GMT
RUN adduser -S eggdrop
# Thu, 25 Feb 2021 00:28:26 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Mar 2021 01:49:30 GMT
ENV EGGDROP_SHA256=2968824d5184d54bc2b0d6d3c746ca41cc8342523d919671f33ea2446fef0f36
# Tue, 09 Mar 2021 01:49:31 GMT
ENV EGGDROP_COMMIT=d01a34e163c47641eb9516ed918699b8822a7855
# Tue, 09 Mar 2021 01:49:37 GMT
RUN apk --update add --no-cache tcl bash openssl
# Tue, 09 Mar 2021 01:51:41 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Mar 2021 01:51:42 GMT
ENV NICK=
# Tue, 09 Mar 2021 01:51:43 GMT
ENV SERVER=
# Tue, 09 Mar 2021 01:51:43 GMT
ENV LISTEN=3333
# Tue, 09 Mar 2021 01:51:44 GMT
ENV OWNER=
# Tue, 09 Mar 2021 01:51:45 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Mar 2021 01:51:45 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Mar 2021 01:51:46 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Mar 2021 01:51:47 GMT
EXPOSE 3333
# Tue, 09 Mar 2021 01:51:48 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Tue, 09 Mar 2021 01:51:49 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Mar 2021 01:51:50 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Mar 2021 01:51:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:10e3bc1a9288f315752811ab2f438cb080f27de72c30375566135a542c8e03a1`  
		Last Modified: Wed, 24 Feb 2021 20:51:26 GMT  
		Size: 2.6 MB (2621066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe21623383fe574b3935c80d4ce081e4d39972c5dc4ad9c8c4bf20e6217d48e`  
		Last Modified: Thu, 25 Feb 2021 00:31:24 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616eb1b2593f122b2ec5a336cdbcd5303f22e4f03d6ebf4330df96aa5f49bac7`  
		Last Modified: Thu, 25 Feb 2021 00:31:22 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49dc8e2ccca88a5e6ace164e099f0218bb2160b3aa12c686d297f5667da32a7`  
		Last Modified: Tue, 09 Mar 2021 01:52:08 GMT  
		Size: 2.6 MB (2608773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b249b95eef3b1bce416a752bfe62355c2f4de9551589b046ec82aebaa7a57ff`  
		Last Modified: Tue, 09 Mar 2021 01:52:10 GMT  
		Size: 8.3 MB (8309505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad43df36b650e0085cc4e8684af55fe1bf6a5f1c380054b91615f832a90a835`  
		Last Modified: Tue, 09 Mar 2021 01:52:08 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63c97cb0e17099d84669e47b98f9728169dd422bd5a9fed7e750cbbbef3a4b0`  
		Last Modified: Tue, 09 Mar 2021 01:52:10 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:fcc89f9c240a07767aea937ca06421f175cb7c15f8c9de088a1f0c45b82106b8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13859308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b7b6148f1f196c2d376c3263acf190ea7abcf90a810edc1f186630f0a426fc`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:40:21 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 24 Feb 2021 21:40:23 GMT
RUN adduser -S eggdrop
# Wed, 24 Feb 2021 21:40:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Mar 2021 01:39:34 GMT
ENV EGGDROP_SHA256=2968824d5184d54bc2b0d6d3c746ca41cc8342523d919671f33ea2446fef0f36
# Tue, 09 Mar 2021 01:39:35 GMT
ENV EGGDROP_COMMIT=d01a34e163c47641eb9516ed918699b8822a7855
# Tue, 09 Mar 2021 01:39:38 GMT
RUN apk --update add --no-cache tcl bash openssl
# Tue, 09 Mar 2021 01:41:27 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Mar 2021 01:41:28 GMT
ENV NICK=
# Tue, 09 Mar 2021 01:41:29 GMT
ENV SERVER=
# Tue, 09 Mar 2021 01:41:29 GMT
ENV LISTEN=3333
# Tue, 09 Mar 2021 01:41:30 GMT
ENV OWNER=
# Tue, 09 Mar 2021 01:41:31 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Mar 2021 01:41:31 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Mar 2021 01:41:32 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Mar 2021 01:41:33 GMT
EXPOSE 3333
# Tue, 09 Mar 2021 01:41:33 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Tue, 09 Mar 2021 01:41:34 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Mar 2021 01:41:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Mar 2021 01:41:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d7e620a18c70da62d98fd84649c1aa6e9bace50def7eb2c177a1e5bd7a5a88`  
		Last Modified: Wed, 24 Feb 2021 21:42:46 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473de84245e87f528cf9f16d91909982599e6ba23d12d914bf8aa0770f103bb4`  
		Last Modified: Wed, 24 Feb 2021 21:42:45 GMT  
		Size: 9.5 KB (9517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484679a578fcdbee283e00db4d76667334d08af1f5b4849ab32a38a6b8f461ad`  
		Last Modified: Tue, 09 Mar 2021 01:41:57 GMT  
		Size: 2.7 MB (2722586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da5d4ecc15b2fa9c31f072b7890370a0761bc8b371d8ceeedcf6cadee86094d`  
		Last Modified: Tue, 09 Mar 2021 01:41:58 GMT  
		Size: 8.4 MB (8397535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1f789549528b8a88b0e61c77a191496998a63850c2e9f1cad962c0906fce39`  
		Last Modified: Tue, 09 Mar 2021 01:41:56 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2ea8f7887fd591fbf00520749320885d8d2f817fe6ac482769a23b64dfb8b1`  
		Last Modified: Tue, 09 Mar 2021 01:41:56 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
