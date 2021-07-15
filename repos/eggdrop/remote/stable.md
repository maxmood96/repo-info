## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:c1bfc6d7635fb78eb5b3ebfcb48186d0c17c2b3b0691af075b0557a864da06b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:51b3ef47ca8b09e0a8670e81741a7db345f341ccae1d55aae151313ebfa5b365
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 MB (8676697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09112261a150b58dcde08ca4b1b9c9903ec3d35ac6ec7578443847dd4a61a851`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:28:52 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:28:54 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:28:57 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 20:29:00 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:21:38 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:21:38 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:21:38 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:21:38 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:21:39 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:21:39 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:21:39 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:21:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:21:40 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:21:40 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:21:40 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:21:40 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:21:40 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac1d9ab058af7106893a1ba77f9ca0b3a58052b9ae5066905c6f7ae26c94434`  
		Last Modified: Wed, 14 Apr 2021 20:31:26 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76394ca5ad9f94b4ac3d2cb72f4bcd6e7eb23df13adb36a6b732b4e11bf4e9a3`  
		Last Modified: Wed, 14 Apr 2021 20:31:23 GMT  
		Size: 10.1 KB (10113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb74bc16f4c16d3b897fd84478f8df97a60b755eee63f8202139c5e4937537d`  
		Last Modified: Wed, 14 Apr 2021 20:31:24 GMT  
		Size: 2.7 MB (2724472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c114180b4ff20542b47e87dddd4e279a6a1c5b93a5fdb4657bda142baa1ef6`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 3.1 MB (3126334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5184da22eb5974602eeb414a05aa7e2c7b32d466f6737b6bd24b920345229d35`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938251404b7a9828161193fdee8efa6acbb84fd990876aeb173ffe1b9bfc259e`  
		Last Modified: Fri, 02 Jul 2021 17:22:07 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:cb2857b4f08efcdc1fe4c3453e4f2681c370cc986a4aa90d75feff218e2b879f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8374923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8231bbbcc5827a63173e69ca178c549755fb7bb7f25c379925c3ea7789b017b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Fri, 02 Jul 2021 17:52:27 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 02 Jul 2021 17:52:29 GMT
RUN adduser -S eggdrop
# Fri, 02 Jul 2021 17:52:31 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 02 Jul 2021 17:52:35 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:54:56 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:54:56 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:54:57 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:54:57 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:54:58 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:54:58 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:54:59 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:55:00 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:55:00 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:55:01 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:55:01 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:55:02 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:55:02 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde3d0442928db4e3f1dc1a2010597a09612b4f1eb31218ef74cfc446970579f`  
		Last Modified: Fri, 02 Jul 2021 17:55:54 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabc0f0341eb96eca7c7ecd27e3c208cc939745bedad90ed4513d11be419b4bd`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 9.8 KB (9833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c0b9d868b661bfa23dd60b3676248d157e8431770bbae4677d622e2680c1db`  
		Last Modified: Fri, 02 Jul 2021 17:55:55 GMT  
		Size: 2.7 MB (2652125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe78ec41b27bf431ccc00eff90efc248d26ad67423e09b418211f5d53cd3e742`  
		Last Modified: Fri, 02 Jul 2021 17:55:55 GMT  
		Size: 3.1 MB (3087038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9bd7137c26119576b933cf2679217767e61f3b3cf60813c85108a34f8e8073`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43999f10c3c2695ace77755e1632d119b78f8b54b257f3b632b434c02635bbb`  
		Last Modified: Fri, 02 Jul 2021 17:55:52 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:7b36070ed17d1cf8345ae28df628c1f4e503f7fa363c3920bfc3594fd8ffdada
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8609230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1598a06a352e8e3bd10b91634ce2a1258cfc4a386bfd693f6428850636862c86`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:30:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 15 Jun 2021 23:30:50 GMT
RUN adduser -S eggdrop
# Tue, 15 Jun 2021 23:30:52 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 15 Jun 2021 23:30:53 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:42:07 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:42:07 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:42:07 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:42:08 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:42:08 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:42:08 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:42:08 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:42:08 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:42:09 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:42:09 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:42:09 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:42:09 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:42:09 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3db2720b6273728863ce64bb67670c4aae649525cf85a5bc0834bd557c60028`  
		Last Modified: Tue, 15 Jun 2021 23:32:42 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960848fa3748666f162fe523f04c331adba985f24d63933d5aaf1e2a0e75c5b`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 10.0 KB (9996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ebe6949c44b5c5569f8ee4c4dfe8132fc69db2ae59ed92a76bdcbbc5e5784`  
		Last Modified: Tue, 15 Jun 2021 23:32:40 GMT  
		Size: 2.8 MB (2752462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fa19ca3b45bab88854e50ddd795bed53f87dc0bff57b2a313377aa740f0f12`  
		Last Modified: Fri, 02 Jul 2021 17:42:39 GMT  
		Size: 3.1 MB (3130930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71fa519e4578f3ab87690779bc55cb283cecaaed9cb745e64661de22660e341`  
		Last Modified: Fri, 02 Jul 2021 17:42:38 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350e82783e7834ea302f5f705d827daedd7ef7ceff73bb2382d25f2eadeca8dd`  
		Last Modified: Fri, 02 Jul 2021 17:42:38 GMT  
		Size: 706.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
