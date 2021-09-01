<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.8`](#eggdrop18)
-	[`eggdrop:1.8.4`](#eggdrop184)
-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.1`](#eggdrop191)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.8`

```console
$ docker pull eggdrop@sha256:20e9e88de9ad7aaa3c7d6beb98dbd5b2c2ed6b4863847bee489b020ec035b4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eggdrop:1.8` - linux; amd64

```console
$ docker pull eggdrop@sha256:3515bc8d05ff6214c16fa920bd27f66468844e616e114a44a9c5968cc810adff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8801912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:158d1a7aca7e5a2c0c5e721c885f80379ad74b38e0f936d81f764950730c8b58`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:31 GMT
ADD file:9d14b11183983923090d9e6d15cc51ee210466296e913bfefbfd580b3de59c95 in / 
# Tue, 31 Aug 2021 23:18:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:45:26 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 01 Sep 2021 00:45:27 GMT
RUN adduser -S eggdrop
# Wed, 01 Sep 2021 00:45:29 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 00:47:24 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 01 Sep 2021 00:48:53 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 01 Sep 2021 00:48:54 GMT
ENV NICK=
# Wed, 01 Sep 2021 00:48:54 GMT
ENV SERVER=
# Wed, 01 Sep 2021 00:48:54 GMT
ENV LISTEN=3333
# Wed, 01 Sep 2021 00:48:55 GMT
ENV OWNER=
# Wed, 01 Sep 2021 00:48:55 GMT
ENV USERFILE=eggdrop.user
# Wed, 01 Sep 2021 00:48:55 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 01 Sep 2021 00:48:56 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 01 Sep 2021 00:48:56 GMT
EXPOSE 3333
# Wed, 01 Sep 2021 00:48:57 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Wed, 01 Sep 2021 00:48:57 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 01 Sep 2021 00:48:58 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 01 Sep 2021 00:48:58 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6a428f9f83b0a29f1fdd2ccccca19a9bab805a925b8eddf432a5a3d3da04afbc`  
		Last Modified: Tue, 31 Aug 2021 23:19:15 GMT  
		Size: 2.8 MB (2817307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f20f9fdd96b050b7674a3c80fab08aa90a03ade7cdb1605902daa948fda52a2`  
		Last Modified: Wed, 01 Sep 2021 00:50:59 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd70c5c8eea46f41315a10333d6c4180d7330668d5d9a03a677e69f00dc72e`  
		Last Modified: Wed, 01 Sep 2021 00:50:56 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2574265c46e1bcf9b75a096f4c4ba73e414b625819aed53a53f373e11e016dc`  
		Last Modified: Wed, 01 Sep 2021 00:51:07 GMT  
		Size: 2.7 MB (2685358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c786a5b4be16b348ab37d1166a4e4c7d64fb1c801787034e017600ff03553208`  
		Last Modified: Wed, 01 Sep 2021 00:51:07 GMT  
		Size: 3.3 MB (3285797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f54e33975937b1852cb665d7c706121b1e18b1182d603de1f5dc8c9ed981e7`  
		Last Modified: Wed, 01 Sep 2021 00:51:06 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6541232161c3bb1d26a43c96019ab8d7689d531648c648bb4d7125d21ae39`  
		Last Modified: Wed, 01 Sep 2021 00:51:06 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.8.4`

```console
$ docker pull eggdrop@sha256:20e9e88de9ad7aaa3c7d6beb98dbd5b2c2ed6b4863847bee489b020ec035b4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eggdrop:1.8.4` - linux; amd64

```console
$ docker pull eggdrop@sha256:3515bc8d05ff6214c16fa920bd27f66468844e616e114a44a9c5968cc810adff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8801912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:158d1a7aca7e5a2c0c5e721c885f80379ad74b38e0f936d81f764950730c8b58`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:31 GMT
ADD file:9d14b11183983923090d9e6d15cc51ee210466296e913bfefbfd580b3de59c95 in / 
# Tue, 31 Aug 2021 23:18:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:45:26 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 01 Sep 2021 00:45:27 GMT
RUN adduser -S eggdrop
# Wed, 01 Sep 2021 00:45:29 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 00:47:24 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 01 Sep 2021 00:48:53 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 01 Sep 2021 00:48:54 GMT
ENV NICK=
# Wed, 01 Sep 2021 00:48:54 GMT
ENV SERVER=
# Wed, 01 Sep 2021 00:48:54 GMT
ENV LISTEN=3333
# Wed, 01 Sep 2021 00:48:55 GMT
ENV OWNER=
# Wed, 01 Sep 2021 00:48:55 GMT
ENV USERFILE=eggdrop.user
# Wed, 01 Sep 2021 00:48:55 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 01 Sep 2021 00:48:56 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 01 Sep 2021 00:48:56 GMT
EXPOSE 3333
# Wed, 01 Sep 2021 00:48:57 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Wed, 01 Sep 2021 00:48:57 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 01 Sep 2021 00:48:58 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 01 Sep 2021 00:48:58 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6a428f9f83b0a29f1fdd2ccccca19a9bab805a925b8eddf432a5a3d3da04afbc`  
		Last Modified: Tue, 31 Aug 2021 23:19:15 GMT  
		Size: 2.8 MB (2817307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f20f9fdd96b050b7674a3c80fab08aa90a03ade7cdb1605902daa948fda52a2`  
		Last Modified: Wed, 01 Sep 2021 00:50:59 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd70c5c8eea46f41315a10333d6c4180d7330668d5d9a03a677e69f00dc72e`  
		Last Modified: Wed, 01 Sep 2021 00:50:56 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2574265c46e1bcf9b75a096f4c4ba73e414b625819aed53a53f373e11e016dc`  
		Last Modified: Wed, 01 Sep 2021 00:51:07 GMT  
		Size: 2.7 MB (2685358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c786a5b4be16b348ab37d1166a4e4c7d64fb1c801787034e017600ff03553208`  
		Last Modified: Wed, 01 Sep 2021 00:51:07 GMT  
		Size: 3.3 MB (3285797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f54e33975937b1852cb665d7c706121b1e18b1182d603de1f5dc8c9ed981e7`  
		Last Modified: Wed, 01 Sep 2021 00:51:06 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6541232161c3bb1d26a43c96019ab8d7689d531648c648bb4d7125d21ae39`  
		Last Modified: Wed, 01 Sep 2021 00:51:06 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:fe6a8132324ef603f18a2cc6bd1616eb899eb990a414299d173b190f514d8a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

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

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:9e7f537499175c84d1019180b1f519833944ed059373e2bd6ef02ea799286d30
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8374845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fad159c32b68cd1e1cbd4b9bcf4e3724e255d0df411b3fdcd5137b4e025cf1e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:55 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Fri, 30 Jul 2021 17:49:55 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 00:21:46 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 31 Jul 2021 00:21:48 GMT
RUN adduser -S eggdrop
# Sat, 31 Jul 2021 00:21:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 31 Jul 2021 00:21:53 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 31 Jul 2021 00:24:14 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 31 Jul 2021 00:24:15 GMT
ENV NICK=
# Sat, 31 Jul 2021 00:24:15 GMT
ENV SERVER=
# Sat, 31 Jul 2021 00:24:16 GMT
ENV LISTEN=3333
# Sat, 31 Jul 2021 00:24:16 GMT
ENV OWNER=
# Sat, 31 Jul 2021 00:24:17 GMT
ENV USERFILE=eggdrop.user
# Sat, 31 Jul 2021 00:24:17 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 31 Jul 2021 00:24:17 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 31 Jul 2021 00:24:18 GMT
EXPOSE 3333
# Sat, 31 Jul 2021 00:24:18 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 31 Jul 2021 00:24:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 31 Jul 2021 00:24:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 31 Jul 2021 00:24:20 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80840070f57969182984e039953c1bb5900b194ba70cf6bc89da3ce7080b1034`  
		Last Modified: Sat, 31 Jul 2021 00:25:13 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1732a159cb79be0235f98ec94d99d0af2a5ee6988775b0db702fb70bc7f26092`  
		Last Modified: Sat, 31 Jul 2021 00:25:11 GMT  
		Size: 9.8 KB (9834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d72c33cb9d3e4077276c3fc20f34063b72084acaf06b2115aa7a2f42a2b104`  
		Last Modified: Sat, 31 Jul 2021 00:25:13 GMT  
		Size: 2.7 MB (2652130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d79e26a12344ce4127afd2725523ed56d1cb38aa82163defa87fa3ab1841ec`  
		Last Modified: Sat, 31 Jul 2021 00:25:13 GMT  
		Size: 3.1 MB (3086944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62504abca636304557a5cb64071d3f3e9101d1ca1ac24a698706470fbb308f90`  
		Last Modified: Sat, 31 Jul 2021 00:25:11 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f30b21b6d88562e0397aca8d8f59864b17715a966f7ae1ab98cff6ea7de668`  
		Last Modified: Sat, 31 Jul 2021 00:25:11 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

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

## `eggdrop:1.9.1`

```console
$ docker pull eggdrop@sha256:fe6a8132324ef603f18a2cc6bd1616eb899eb990a414299d173b190f514d8a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.1` - linux; amd64

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

### `eggdrop:1.9.1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:9e7f537499175c84d1019180b1f519833944ed059373e2bd6ef02ea799286d30
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8374845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fad159c32b68cd1e1cbd4b9bcf4e3724e255d0df411b3fdcd5137b4e025cf1e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:55 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Fri, 30 Jul 2021 17:49:55 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 00:21:46 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 31 Jul 2021 00:21:48 GMT
RUN adduser -S eggdrop
# Sat, 31 Jul 2021 00:21:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 31 Jul 2021 00:21:53 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 31 Jul 2021 00:24:14 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 31 Jul 2021 00:24:15 GMT
ENV NICK=
# Sat, 31 Jul 2021 00:24:15 GMT
ENV SERVER=
# Sat, 31 Jul 2021 00:24:16 GMT
ENV LISTEN=3333
# Sat, 31 Jul 2021 00:24:16 GMT
ENV OWNER=
# Sat, 31 Jul 2021 00:24:17 GMT
ENV USERFILE=eggdrop.user
# Sat, 31 Jul 2021 00:24:17 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 31 Jul 2021 00:24:17 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 31 Jul 2021 00:24:18 GMT
EXPOSE 3333
# Sat, 31 Jul 2021 00:24:18 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 31 Jul 2021 00:24:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 31 Jul 2021 00:24:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 31 Jul 2021 00:24:20 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80840070f57969182984e039953c1bb5900b194ba70cf6bc89da3ce7080b1034`  
		Last Modified: Sat, 31 Jul 2021 00:25:13 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1732a159cb79be0235f98ec94d99d0af2a5ee6988775b0db702fb70bc7f26092`  
		Last Modified: Sat, 31 Jul 2021 00:25:11 GMT  
		Size: 9.8 KB (9834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d72c33cb9d3e4077276c3fc20f34063b72084acaf06b2115aa7a2f42a2b104`  
		Last Modified: Sat, 31 Jul 2021 00:25:13 GMT  
		Size: 2.7 MB (2652130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d79e26a12344ce4127afd2725523ed56d1cb38aa82163defa87fa3ab1841ec`  
		Last Modified: Sat, 31 Jul 2021 00:25:13 GMT  
		Size: 3.1 MB (3086944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62504abca636304557a5cb64071d3f3e9101d1ca1ac24a698706470fbb308f90`  
		Last Modified: Sat, 31 Jul 2021 00:25:11 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f30b21b6d88562e0397aca8d8f59864b17715a966f7ae1ab98cff6ea7de668`  
		Last Modified: Sat, 31 Jul 2021 00:25:11 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.1` - linux; arm64 variant v8

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

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:fbb1a7909a64560298d6823e56b54ffce02cd5ce3c8fefdf22dd86ce34f9552b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:ac313d620f14ba79aaf04ea37893c884eecda0ab74bc1c8504392949f06e265e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13971057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c678c6c2ef4c384635313ea7010639ae5bcd84ff82a4c0232e4d03872319f2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:31 GMT
ADD file:9d14b11183983923090d9e6d15cc51ee210466296e913bfefbfd580b3de59c95 in / 
# Tue, 31 Aug 2021 23:18:31 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:45:26 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 01 Sep 2021 00:45:27 GMT
RUN adduser -S eggdrop
# Wed, 01 Sep 2021 00:45:29 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 00:45:29 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Wed, 01 Sep 2021 00:45:30 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Wed, 01 Sep 2021 00:45:32 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 01 Sep 2021 00:47:07 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 01 Sep 2021 00:47:07 GMT
ENV NICK=
# Wed, 01 Sep 2021 00:47:08 GMT
ENV SERVER=
# Wed, 01 Sep 2021 00:47:08 GMT
ENV LISTEN=3333
# Wed, 01 Sep 2021 00:47:08 GMT
ENV OWNER=
# Wed, 01 Sep 2021 00:47:09 GMT
ENV USERFILE=eggdrop.user
# Wed, 01 Sep 2021 00:47:09 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 01 Sep 2021 00:47:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 01 Sep 2021 00:47:09 GMT
EXPOSE 3333
# Wed, 01 Sep 2021 00:47:10 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Wed, 01 Sep 2021 00:47:10 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 01 Sep 2021 00:47:10 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 01 Sep 2021 00:47:11 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6a428f9f83b0a29f1fdd2ccccca19a9bab805a925b8eddf432a5a3d3da04afbc`  
		Last Modified: Tue, 31 Aug 2021 23:19:15 GMT  
		Size: 2.8 MB (2817307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f20f9fdd96b050b7674a3c80fab08aa90a03ade7cdb1605902daa948fda52a2`  
		Last Modified: Wed, 01 Sep 2021 00:50:59 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd70c5c8eea46f41315a10333d6c4180d7330668d5d9a03a677e69f00dc72e`  
		Last Modified: Wed, 01 Sep 2021 00:50:56 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06195f163e0e173103bdbd7895dad3e16cd83d0bea4b387e8ba0a279675c6c7f`  
		Last Modified: Wed, 01 Sep 2021 00:50:57 GMT  
		Size: 2.7 MB (2685319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b39ea5b87e596e6b07a2ad6917fe4dc53c15e522b7284f084d1594f143d80e`  
		Last Modified: Wed, 01 Sep 2021 00:50:58 GMT  
		Size: 8.5 MB (8454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c5a2dde7490e58c609dc03eec26f76472c035e792e785fabde507ec82220f3`  
		Last Modified: Wed, 01 Sep 2021 00:50:56 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe69b5152010e5eee368deff14a0392844761ff7f0dde5eb3d4004a7fb1c2c0`  
		Last Modified: Wed, 01 Sep 2021 00:50:56 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:7081a16164cf837efcaa2350db5eeeda9b514a63edcab404c6e97c1ac1093686
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13626202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7196c0eae3a8be4ab8cb952d0026f62fa2f331151330e742750ac94a055ccb13`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:50:16 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Fri, 30 Jul 2021 17:50:17 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 00:18:58 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 31 Jul 2021 00:19:00 GMT
RUN adduser -S eggdrop
# Sat, 31 Jul 2021 00:19:02 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 31 Jul 2021 00:19:03 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Sat, 31 Jul 2021 00:19:03 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Sat, 31 Jul 2021 00:19:06 GMT
RUN apk --update add --no-cache tcl bash openssl
# Sat, 31 Jul 2021 00:21:25 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 31 Jul 2021 00:21:25 GMT
ENV NICK=
# Sat, 31 Jul 2021 00:21:26 GMT
ENV SERVER=
# Sat, 31 Jul 2021 00:21:26 GMT
ENV LISTEN=3333
# Sat, 31 Jul 2021 00:21:27 GMT
ENV OWNER=
# Sat, 31 Jul 2021 00:21:27 GMT
ENV USERFILE=eggdrop.user
# Sat, 31 Jul 2021 00:21:27 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 31 Jul 2021 00:21:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 31 Jul 2021 00:21:28 GMT
EXPOSE 3333
# Sat, 31 Jul 2021 00:21:29 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Sat, 31 Jul 2021 00:21:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 31 Jul 2021 00:21:30 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 31 Jul 2021 00:21:30 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89bf6e41540921108eeecf3fbf4a8db821ca6d53c55f3294f805d5080fdf745f`  
		Last Modified: Sat, 31 Jul 2021 00:24:59 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28639963e18c0fe3d9227f63cb8da003e6b3f7570f7ca06df541c0e641d825d`  
		Last Modified: Sat, 31 Jul 2021 00:24:57 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ef5833a8b056e3ab3bb8624064245b09eaf6fbed3a7c9a37c550509fe899cd`  
		Last Modified: Sat, 31 Jul 2021 00:24:59 GMT  
		Size: 2.6 MB (2608744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:998f6fb9fb2bd08ed73325e5a10af96e9286277ae65c4d10b2ffb0c41eb19d75`  
		Last Modified: Sat, 31 Jul 2021 00:25:03 GMT  
		Size: 8.4 MB (8382301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8904f19c2e982d37932eb9095241cd857d690a6b72ebf168f100131a737c4f`  
		Last Modified: Sat, 31 Jul 2021 00:24:57 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9d7d6cf5cb597621ccf6110ad5a18bdf134abb2988e112f7403a1663cb0a86`  
		Last Modified: Sat, 31 Jul 2021 00:24:57 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:c70ac0a13f955edd79ed236bca0dbdc36e97187f05a9354f7c94ef52fda6a006
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13931532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa5d0df8630f3024bd782a7f72e9e5b4fa6b68003b9f8265f3681cf9cacdae4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:29:36 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 15 Jun 2021 23:29:37 GMT
RUN adduser -S eggdrop
# Tue, 15 Jun 2021 23:29:38 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 02 Jul 2021 17:39:48 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Fri, 02 Jul 2021 17:39:48 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Fri, 02 Jul 2021 17:39:50 GMT
RUN apk --update add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:40:53 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:40:53 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:40:53 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:40:53 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:40:54 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:40:54 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:40:54 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:40:54 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:40:54 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:40:55 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:40:55 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:40:55 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:40:55 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c7539bf8879d1a52593f00c732dcc06de9183953717c4b4951f6b8d29cbbc1`  
		Last Modified: Tue, 15 Jun 2021 23:32:32 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7414aa2d3258c5ce8af602a09967cff2107fdb7e678a330b48e092a0cfca4a44`  
		Last Modified: Tue, 15 Jun 2021 23:32:29 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5b09a183e39b602bd66f2775c80e61270e350bfb739fc1dd6263c5410a5ced`  
		Last Modified: Fri, 02 Jul 2021 17:42:30 GMT  
		Size: 2.7 MB (2722582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fda6c805fe8d9feb0a57de280acfb2501a580dcd55c37fec52394d2732bfde4`  
		Last Modified: Fri, 02 Jul 2021 17:42:30 GMT  
		Size: 8.5 MB (8468643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed23ead9fb4f46dd5c0c877ce2f44670feea4fd533bf5f89b0f04ef62581426`  
		Last Modified: Fri, 02 Jul 2021 17:42:29 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05ba0af66353010b8adc3027934e3e8c6fd0bcb8ace7841ec086de17864bd5b`  
		Last Modified: Fri, 02 Jul 2021 17:42:29 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:fe6a8132324ef603f18a2cc6bd1616eb899eb990a414299d173b190f514d8a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

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

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:9e7f537499175c84d1019180b1f519833944ed059373e2bd6ef02ea799286d30
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8374845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fad159c32b68cd1e1cbd4b9bcf4e3724e255d0df411b3fdcd5137b4e025cf1e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:55 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Fri, 30 Jul 2021 17:49:55 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 00:21:46 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 31 Jul 2021 00:21:48 GMT
RUN adduser -S eggdrop
# Sat, 31 Jul 2021 00:21:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 31 Jul 2021 00:21:53 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 31 Jul 2021 00:24:14 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 31 Jul 2021 00:24:15 GMT
ENV NICK=
# Sat, 31 Jul 2021 00:24:15 GMT
ENV SERVER=
# Sat, 31 Jul 2021 00:24:16 GMT
ENV LISTEN=3333
# Sat, 31 Jul 2021 00:24:16 GMT
ENV OWNER=
# Sat, 31 Jul 2021 00:24:17 GMT
ENV USERFILE=eggdrop.user
# Sat, 31 Jul 2021 00:24:17 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 31 Jul 2021 00:24:17 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 31 Jul 2021 00:24:18 GMT
EXPOSE 3333
# Sat, 31 Jul 2021 00:24:18 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 31 Jul 2021 00:24:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 31 Jul 2021 00:24:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 31 Jul 2021 00:24:20 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80840070f57969182984e039953c1bb5900b194ba70cf6bc89da3ce7080b1034`  
		Last Modified: Sat, 31 Jul 2021 00:25:13 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1732a159cb79be0235f98ec94d99d0af2a5ee6988775b0db702fb70bc7f26092`  
		Last Modified: Sat, 31 Jul 2021 00:25:11 GMT  
		Size: 9.8 KB (9834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d72c33cb9d3e4077276c3fc20f34063b72084acaf06b2115aa7a2f42a2b104`  
		Last Modified: Sat, 31 Jul 2021 00:25:13 GMT  
		Size: 2.7 MB (2652130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d79e26a12344ce4127afd2725523ed56d1cb38aa82163defa87fa3ab1841ec`  
		Last Modified: Sat, 31 Jul 2021 00:25:13 GMT  
		Size: 3.1 MB (3086944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62504abca636304557a5cb64071d3f3e9101d1ca1ac24a698706470fbb308f90`  
		Last Modified: Sat, 31 Jul 2021 00:25:11 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f30b21b6d88562e0397aca8d8f59864b17715a966f7ae1ab98cff6ea7de668`  
		Last Modified: Sat, 31 Jul 2021 00:25:11 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

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

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:fe6a8132324ef603f18a2cc6bd1616eb899eb990a414299d173b190f514d8a92
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
$ docker pull eggdrop@sha256:9e7f537499175c84d1019180b1f519833944ed059373e2bd6ef02ea799286d30
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8374845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fad159c32b68cd1e1cbd4b9bcf4e3724e255d0df411b3fdcd5137b4e025cf1e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:55 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Fri, 30 Jul 2021 17:49:55 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 00:21:46 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Sat, 31 Jul 2021 00:21:48 GMT
RUN adduser -S eggdrop
# Sat, 31 Jul 2021 00:21:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Sat, 31 Jul 2021 00:21:53 GMT
RUN apk add --no-cache tcl bash openssl
# Sat, 31 Jul 2021 00:24:14 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.1.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.1.tar.gz.asc eggdrop-1.9.1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.1.tar.gz.asc   && tar -zxvf eggdrop-1.9.1.tar.gz   && rm eggdrop-1.9.1.tar.gz   && ( cd eggdrop-1.9.1     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Sat, 31 Jul 2021 00:24:15 GMT
ENV NICK=
# Sat, 31 Jul 2021 00:24:15 GMT
ENV SERVER=
# Sat, 31 Jul 2021 00:24:16 GMT
ENV LISTEN=3333
# Sat, 31 Jul 2021 00:24:16 GMT
ENV OWNER=
# Sat, 31 Jul 2021 00:24:17 GMT
ENV USERFILE=eggdrop.user
# Sat, 31 Jul 2021 00:24:17 GMT
ENV CHANFILE=eggdrop.chan
# Sat, 31 Jul 2021 00:24:17 GMT
WORKDIR /home/eggdrop/eggdrop
# Sat, 31 Jul 2021 00:24:18 GMT
EXPOSE 3333
# Sat, 31 Jul 2021 00:24:18 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Sat, 31 Jul 2021 00:24:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Sat, 31 Jul 2021 00:24:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sat, 31 Jul 2021 00:24:20 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80840070f57969182984e039953c1bb5900b194ba70cf6bc89da3ce7080b1034`  
		Last Modified: Sat, 31 Jul 2021 00:25:13 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1732a159cb79be0235f98ec94d99d0af2a5ee6988775b0db702fb70bc7f26092`  
		Last Modified: Sat, 31 Jul 2021 00:25:11 GMT  
		Size: 9.8 KB (9834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d72c33cb9d3e4077276c3fc20f34063b72084acaf06b2115aa7a2f42a2b104`  
		Last Modified: Sat, 31 Jul 2021 00:25:13 GMT  
		Size: 2.7 MB (2652130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d79e26a12344ce4127afd2725523ed56d1cb38aa82163defa87fa3ab1841ec`  
		Last Modified: Sat, 31 Jul 2021 00:25:13 GMT  
		Size: 3.1 MB (3086944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62504abca636304557a5cb64071d3f3e9101d1ca1ac24a698706470fbb308f90`  
		Last Modified: Sat, 31 Jul 2021 00:25:11 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f30b21b6d88562e0397aca8d8f59864b17715a966f7ae1ab98cff6ea7de668`  
		Last Modified: Sat, 31 Jul 2021 00:25:11 GMT  
		Size: 702.0 B  
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
