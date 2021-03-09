## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:e40815528f3fe7b6955716a9dda3a9e2fd95f29a589fa6f1d8f4f0778c729383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:92aaee5e8f4b22286869ac6b36f72117f53dc6e91ab58bcb7c008b4d083265e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8799822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e79a63611bd2432ac3913be4222cf87bb2d2cd6c435fd58bbeedd8700b1f02e`
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
# Tue, 09 Mar 2021 01:20:32 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 09 Mar 2021 01:21:30 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Mar 2021 01:21:30 GMT
ENV NICK=
# Tue, 09 Mar 2021 01:21:30 GMT
ENV SERVER=
# Tue, 09 Mar 2021 01:21:31 GMT
ENV LISTEN=3333
# Tue, 09 Mar 2021 01:21:31 GMT
ENV OWNER=
# Tue, 09 Mar 2021 01:21:31 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Mar 2021 01:21:31 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Mar 2021 01:21:31 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Mar 2021 01:21:31 GMT
EXPOSE 3333
# Tue, 09 Mar 2021 01:21:32 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Tue, 09 Mar 2021 01:21:32 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Mar 2021 01:21:32 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Mar 2021 01:21:32 GMT
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
	-	`sha256:deb2e4415e906a8d8c91b3405e5c1fa9ee80645f05e3b0c507697154b59e685f`  
		Last Modified: Tue, 09 Mar 2021 01:22:06 GMT  
		Size: 2.7 MB (2685359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6189f647208426e25e642fb594dc26156e2aa3a8a6b0e0ad54854c658e23aa6`  
		Last Modified: Tue, 09 Mar 2021 01:22:06 GMT  
		Size: 3.3 MB (3285735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96afb762714705f05196da015ec7008d94069ff0ca4be5fca41984682cde2e6f`  
		Last Modified: Tue, 09 Mar 2021 01:22:05 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e73704c68282c2d20ee6c320e8db1ca415f6fe8158f2dbd7f24303c81629cc`  
		Last Modified: Tue, 09 Mar 2021 01:22:05 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
