## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:6d18916acaeeae792391419a40077992468030c96afc738cad47dea41666e56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:6e892a67931479b599c272a667e2938484206e52d7264ff14d7b7db016f37b30
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8289929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15447097e0374d1ea165db47231adde6fb63ff6480b16f30134b7a313a3b43e9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:49:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 01 Sep 2021 00:49:05 GMT
RUN adduser -S eggdrop
# Wed, 01 Sep 2021 00:49:07 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 00:49:10 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 01 Sep 2021 00:50:26 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 01 Sep 2021 00:50:26 GMT
ENV NICK=
# Wed, 01 Sep 2021 00:50:27 GMT
ENV SERVER=
# Wed, 01 Sep 2021 00:50:27 GMT
ENV LISTEN=3333
# Wed, 01 Sep 2021 00:50:27 GMT
ENV OWNER=
# Wed, 01 Sep 2021 00:50:27 GMT
ENV USERFILE=eggdrop.user
# Wed, 01 Sep 2021 00:50:27 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 01 Sep 2021 00:50:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 01 Sep 2021 00:50:28 GMT
EXPOSE 3333
# Wed, 01 Sep 2021 00:50:28 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 01 Sep 2021 00:50:28 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 01 Sep 2021 00:50:29 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 01 Sep 2021 00:50:29 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2739640d4bb626124033590fe2bf187a76c1f09fc23aa7686e7c3fab1ea81d84`  
		Last Modified: Wed, 01 Sep 2021 00:51:19 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738ab5f4a6a9c53e0f6ed425003f94b60df8ec4e166993682419cfe0a94a62f5`  
		Last Modified: Wed, 01 Sep 2021 00:51:16 GMT  
		Size: 10.1 KB (10118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0880ee1cbcc03493b50e3d163c452ce2bbb7b3de40bf0f955c9744388500b821`  
		Last Modified: Wed, 01 Sep 2021 00:51:17 GMT  
		Size: 2.7 MB (2724823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734b1d2617820fb511e667242f74784e1a91e810da7643c518373cea683dc9f5`  
		Last Modified: Wed, 01 Sep 2021 00:51:17 GMT  
		Size: 2.7 MB (2737114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2384c732a6a65e03999103c3cb481f0e361b99732133b52e23f57be3a24759`  
		Last Modified: Wed, 01 Sep 2021 00:51:16 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4ab1d804e5474fe3998c40986e14f69650bea83115a3f78da3e35a49da8219`  
		Last Modified: Wed, 01 Sep 2021 00:51:16 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:256bf1e8371ae1436bd7b27b318801ba886744ed2a1225293f5d586fac79f541
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7984703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c777347de3a39dff1a465be9c70eeda9ba5de814025ba8d418620d17956a5a7b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 01:40:18 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 01 Sep 2021 01:40:20 GMT
RUN adduser -S eggdrop
# Wed, 01 Sep 2021 01:40:22 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 01:40:25 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 01 Sep 2021 01:42:54 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 01 Sep 2021 01:42:54 GMT
ENV NICK=
# Wed, 01 Sep 2021 01:42:55 GMT
ENV SERVER=
# Wed, 01 Sep 2021 01:42:55 GMT
ENV LISTEN=3333
# Wed, 01 Sep 2021 01:42:56 GMT
ENV OWNER=
# Wed, 01 Sep 2021 01:42:56 GMT
ENV USERFILE=eggdrop.user
# Wed, 01 Sep 2021 01:42:56 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 01 Sep 2021 01:42:57 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 01 Sep 2021 01:42:57 GMT
EXPOSE 3333
# Wed, 01 Sep 2021 01:42:58 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 01 Sep 2021 01:42:58 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 01 Sep 2021 01:42:59 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 01 Sep 2021 01:42:59 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f046c2415fb1127f8d46523c533c6d2cce3bd492e0d68c48c260d220336ca952`  
		Last Modified: Wed, 01 Sep 2021 01:43:59 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf336ff3aa2db3f62c40723c1adc70b28e83510d2314cff15dcb5e218e1c2af`  
		Last Modified: Wed, 01 Sep 2021 01:43:57 GMT  
		Size: 9.8 KB (9833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87713f793a04367c6610fc1476e6a6f31d2e474ebb4598fde28a9728dbd06ae`  
		Last Modified: Wed, 01 Sep 2021 01:43:59 GMT  
		Size: 2.7 MB (2652189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7192b1f59b63dc171f423af626fa69dc717358b1645dd0db5b1ed1fb3cbbb2bc`  
		Last Modified: Wed, 01 Sep 2021 01:43:59 GMT  
		Size: 2.7 MB (2695121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c74d83e6f19d90b93b685a87dd4c0c1b522bc2338d4fe8c56b9806a195ca45`  
		Last Modified: Wed, 01 Sep 2021 01:43:57 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6402fc12bd28bda7948b0b77e3a48bd0ebb3f7d2ce610b45949fcfc92e8e478a`  
		Last Modified: Wed, 01 Sep 2021 01:43:57 GMT  
		Size: 700.0 B  
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
