## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:45d3e7afb77c53904aa3d7ff7f975b30977cf9f923cd65bf2dc1b29b7385bf91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:ac51c0945714354a18de779773d2a06aea0eba1a5db4f39a59afa998af0f2d54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13971126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18f8406444915774df8bc7fde6cb77d2d7cfdb1f8efbd11c34dfcd931fa42e4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:17 GMT
ADD file:efe2d94a88cdbbd01c3ef095f0a2473cec9e74804b49cd6fb9b837d362631409 in / 
# Fri, 12 Nov 2021 17:20:17 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:16:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 12 Nov 2021 22:16:42 GMT
RUN adduser -S eggdrop
# Fri, 12 Nov 2021 22:16:44 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 12 Nov 2021 22:16:44 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Fri, 12 Nov 2021 22:16:45 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Fri, 12 Nov 2021 22:16:48 GMT
RUN apk --update add --no-cache tcl bash openssl
# Fri, 12 Nov 2021 22:18:15 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 12 Nov 2021 22:18:15 GMT
ENV NICK=
# Fri, 12 Nov 2021 22:18:15 GMT
ENV SERVER=
# Fri, 12 Nov 2021 22:18:16 GMT
ENV LISTEN=3333
# Fri, 12 Nov 2021 22:18:16 GMT
ENV OWNER=
# Fri, 12 Nov 2021 22:18:16 GMT
ENV USERFILE=eggdrop.user
# Fri, 12 Nov 2021 22:18:16 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 12 Nov 2021 22:18:17 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 12 Nov 2021 22:18:17 GMT
EXPOSE 3333
# Fri, 12 Nov 2021 22:18:17 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Fri, 12 Nov 2021 22:18:17 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 12 Nov 2021 22:18:17 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 12 Nov 2021 22:18:18 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:79e9f2f55bf5465a02ee6a6170e66005b20c7aa6b115af6fcd04fad706ea651a`  
		Last Modified: Fri, 12 Nov 2021 17:21:24 GMT  
		Size: 2.8 MB (2817409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81adda6e9eba444737eb924c547e315175df5a0ce22872ddefa8d3e84e6d8426`  
		Last Modified: Fri, 12 Nov 2021 23:38:59 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c6691f36cfa95bda1f875a9e50901e42545817a24e6fd9cb8463d931f68075`  
		Last Modified: Fri, 12 Nov 2021 23:38:57 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1745cf1ed4da7a73fcd90fbf3034e047ac1ddcfc9cafd47e6bec219875fd02b9`  
		Last Modified: Fri, 12 Nov 2021 23:38:57 GMT  
		Size: 2.7 MB (2685370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df75c7a1bacde78f2df7ea75d7a042759a70bdc1a2e64625cf00980990a9b4da`  
		Last Modified: Fri, 12 Nov 2021 23:38:58 GMT  
		Size: 8.5 MB (8454906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3a328dd9ff12c659f26cf5675153e3f8cfd0d2b31419e4d27dac84638dc1cd`  
		Last Modified: Fri, 12 Nov 2021 23:38:57 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb35aaa19b161c31605b0557e35b5f89b077501a6006bf5d840e6cfc255fa07e`  
		Last Modified: Fri, 12 Nov 2021 23:38:56 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:80d8796e48b3d3949de691838f905fcb69e73b391334049e68d0f0b3796ddff5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13628662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf786dc53d037fdd74a82d889b18bb506c5930153260e490c66497d4efdc424`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:57 GMT
ADD file:3e83d6b5df3a951968e475c7326baf5ef90a22f04163693db34f3b4fc5812434 in / 
# Tue, 31 Aug 2021 22:30:57 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 01:37:30 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 01 Sep 2021 01:37:32 GMT
RUN adduser -S eggdrop
# Wed, 01 Sep 2021 01:37:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 01:37:34 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Wed, 01 Sep 2021 01:37:35 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Wed, 01 Sep 2021 01:37:38 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 01 Sep 2021 01:39:57 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 01 Sep 2021 01:39:57 GMT
ENV NICK=
# Wed, 01 Sep 2021 01:39:58 GMT
ENV SERVER=
# Wed, 01 Sep 2021 01:39:58 GMT
ENV LISTEN=3333
# Wed, 01 Sep 2021 01:39:58 GMT
ENV OWNER=
# Wed, 01 Sep 2021 01:39:59 GMT
ENV USERFILE=eggdrop.user
# Wed, 01 Sep 2021 01:39:59 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 01 Sep 2021 01:40:00 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 01 Sep 2021 01:40:00 GMT
EXPOSE 3333
# Wed, 01 Sep 2021 01:40:01 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Wed, 01 Sep 2021 01:40:01 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 01 Sep 2021 01:40:02 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 01 Sep 2021 01:40:02 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:7fe987b00bcb1f14c5b65f89813475143c021e2f5c156705ac3525abe1b397a1`  
		Last Modified: Tue, 31 Aug 2021 22:32:38 GMT  
		Size: 2.6 MB (2623044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6dd069ebad3ad600a5cca2d74c3ad787846847f6632100ebec5c84edd0f2ef`  
		Last Modified: Wed, 01 Sep 2021 01:43:46 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41231715f4355826a61f9bd9185a0aea868443b6ad7204af06dd8d51a0862274`  
		Last Modified: Wed, 01 Sep 2021 01:43:43 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e663e4511cb4deee82fdc4628d95ac09cdb02f325c1aae273d2640de7e0e6f2`  
		Last Modified: Wed, 01 Sep 2021 01:43:46 GMT  
		Size: 2.6 MB (2608714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d64f077b97874c7ea3af332b7ca1ccdce3972fe69f0742049a2b9ecfbdf2728`  
		Last Modified: Wed, 01 Sep 2021 01:43:49 GMT  
		Size: 8.4 MB (8383658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae48121573bcf358e0189bd7e6fcdebedbe09d8f3526866509e52e047603c5b0`  
		Last Modified: Wed, 01 Sep 2021 01:43:43 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fe2b0c418f3c99112e873b436447c754f54ee32091888b467586f070eb8cb9`  
		Last Modified: Wed, 01 Sep 2021 01:43:44 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:e505c5f85c44687ef35b02910322074b8c65d61a82f04aeae22ebfc9b3e1f01e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13934190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68182d0dd58f674d6ac3c36dcf19e644a13c6cb64f62d1c5e3fc310dc44cf840`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:59 GMT
ADD file:da6c0ac7cb9f819998546d88fb489b746004eb2ad6da64a39210696ef0e66e54 in / 
# Wed, 01 Sep 2021 02:50:59 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 15:14:23 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 01 Sep 2021 15:14:24 GMT
RUN adduser -S eggdrop
# Wed, 01 Sep 2021 15:14:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 01 Sep 2021 15:14:25 GMT
ENV EGGDROP_SHA256=f977f8f586d1b65d2bae581b5b5828d79193a29a217f617c4c74d1868a566c7f
# Wed, 01 Sep 2021 15:14:25 GMT
ENV EGGDROP_COMMIT=886c2ff6f943952018000c16cb48c08b8ab99127
# Wed, 01 Sep 2021 15:14:27 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 01 Sep 2021 15:15:27 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 01 Sep 2021 15:15:27 GMT
ENV NICK=
# Wed, 01 Sep 2021 15:15:27 GMT
ENV SERVER=
# Wed, 01 Sep 2021 15:15:27 GMT
ENV LISTEN=3333
# Wed, 01 Sep 2021 15:15:28 GMT
ENV OWNER=
# Wed, 01 Sep 2021 15:15:28 GMT
ENV USERFILE=eggdrop.user
# Wed, 01 Sep 2021 15:15:28 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 01 Sep 2021 15:15:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 01 Sep 2021 15:15:28 GMT
EXPOSE 3333
# Wed, 01 Sep 2021 15:15:29 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Wed, 01 Sep 2021 15:15:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 01 Sep 2021 15:15:29 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 01 Sep 2021 15:15:29 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:07d756952c5cd45726cf9e8a292a3e05ca67eee5da176df7d632be8c5bb0ad04`  
		Last Modified: Wed, 01 Sep 2021 02:52:00 GMT  
		Size: 2.7 MB (2728407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77992e9a0ea5be6e3c6bbfa4fa595266bfdf5c5cef3e6840258c42dc9bdd24a8`  
		Last Modified: Wed, 01 Sep 2021 15:17:20 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c7ddce6f5c878efe0df3e540ebeaf6a5a4765fff701d369356f318e54f6195`  
		Last Modified: Wed, 01 Sep 2021 15:17:18 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159a45924b16715996a6631dfe560eba72540f8931745dbd27a8369c07da408c`  
		Last Modified: Wed, 01 Sep 2021 15:17:18 GMT  
		Size: 2.7 MB (2722569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751cd66fcc38103b489118ba1351d649d3b6df2f725220e230124f9863c2609b`  
		Last Modified: Wed, 01 Sep 2021 15:17:19 GMT  
		Size: 8.5 MB (8469835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3348c9013c05531db307f682233367518ce245cb2856edf89ba2ff0abcdb9ad2`  
		Last Modified: Wed, 01 Sep 2021 15:17:17 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef6d655d3c74b3761cd764d92a63f137fcfa4d4fa388acc830322f434d4abe3`  
		Last Modified: Wed, 01 Sep 2021 15:17:18 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
