## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:78170f6417446248d6f84fb23b6cf56a11a8195d51e70343a09094f90298e220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:2ab816999da538e9f94ca9d61a1d9eb7217dc8f2c9208716e4fafea284284a9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13967159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708829750388821816f955df9e88872264718c0b8692ac727d6f7600f71ef45f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:26:38 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 20:26:39 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 20:26:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 02 Jul 2021 17:19:42 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Fri, 02 Jul 2021 17:19:42 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Fri, 02 Jul 2021 17:19:45 GMT
RUN apk --update add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:20:35 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:20:35 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:20:36 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:20:36 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:20:36 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:20:36 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:20:36 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:20:37 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:20:37 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:20:37 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:20:37 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:20:37 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:20:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9b60f543dd32d2ac2d7575d5ad495a35a0796146dbf47fd6c76f083f30d599`  
		Last Modified: Wed, 14 Apr 2021 20:31:00 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1714e89337f555b15f73058aa485a830db0f4a0bd40a36eccd6e66bf949c0259`  
		Last Modified: Wed, 14 Apr 2021 20:30:58 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd72365e83b32d0746f4c0050d60fe8a0facbe94088cf5b589e82b40202bae1`  
		Last Modified: Fri, 02 Jul 2021 17:21:57 GMT  
		Size: 2.7 MB (2685326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312819311fd72def7d8d65cdeb2fae083b1d64371f456d40d94a658afe094ad7`  
		Last Modified: Fri, 02 Jul 2021 17:21:58 GMT  
		Size: 8.5 MB (8452134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d3c5febc67a911d07cb73a9fc366d56581bdb0b744a222709c596ae9b3119c`  
		Last Modified: Fri, 02 Jul 2021 17:21:56 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2f081372a6166ad1ce90579062dc37c4e687a49c2b854d79da9ecafcd2fca5`  
		Last Modified: Fri, 02 Jul 2021 17:21:56 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:349e68f9d8b74146ff745e0f0cc3a21e5c52a083c528e37f89c8abd3a2eb25fb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13626210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1e85ffc7a8e21b7bf572ba96e3f188e8c47887230b499edc5d84ebfe768333`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:47 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Tue, 15 Jun 2021 22:57:47 GMT
CMD ["/bin/sh"]
# Fri, 02 Jul 2021 17:49:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 02 Jul 2021 17:49:42 GMT
RUN adduser -S eggdrop
# Fri, 02 Jul 2021 17:49:46 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 02 Jul 2021 17:49:46 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Fri, 02 Jul 2021 17:49:47 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Fri, 02 Jul 2021 17:49:51 GMT
RUN apk --update add --no-cache tcl bash openssl
# Fri, 02 Jul 2021 17:52:11 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 02 Jul 2021 17:52:11 GMT
ENV NICK=
# Fri, 02 Jul 2021 17:52:12 GMT
ENV SERVER=
# Fri, 02 Jul 2021 17:52:12 GMT
ENV LISTEN=3333
# Fri, 02 Jul 2021 17:52:13 GMT
ENV OWNER=
# Fri, 02 Jul 2021 17:52:13 GMT
ENV USERFILE=eggdrop.user
# Fri, 02 Jul 2021 17:52:14 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 02 Jul 2021 17:52:14 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 02 Jul 2021 17:52:15 GMT
EXPOSE 3333
# Fri, 02 Jul 2021 17:52:15 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Fri, 02 Jul 2021 17:52:16 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 02 Jul 2021 17:52:16 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 02 Jul 2021 17:52:16 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a19728eec432014213ee2238d2d2987f76b1aedf389f3d48ec0a81c426e913`  
		Last Modified: Fri, 02 Jul 2021 17:55:41 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0051ea1d18bb74c8ef22d384ba405fa2b858271ef119d0e7903d31c72fdfda68`  
		Last Modified: Fri, 02 Jul 2021 17:55:39 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbff33951f6cd1cfd2db6ba353068d028c0c5c3865fae1bac1c434a9b9e70816`  
		Last Modified: Fri, 02 Jul 2021 17:55:41 GMT  
		Size: 2.6 MB (2608755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd4c1a1643b6116ec93916f92c9d9d7b0f2173db2dd8b63caa5eb6fd9504ed3`  
		Last Modified: Fri, 02 Jul 2021 17:55:44 GMT  
		Size: 8.4 MB (8382295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928dc582c0585d29dd4b646801e06d99732873c6d11b4b224044fd6b9dc382ad`  
		Last Modified: Fri, 02 Jul 2021 17:55:39 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08997fdb04a278dafdd7f2c2d1332d473c61ced42b9daceccf3a702b581a13d6`  
		Last Modified: Fri, 02 Jul 2021 17:55:39 GMT  
		Size: 701.0 B  
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
