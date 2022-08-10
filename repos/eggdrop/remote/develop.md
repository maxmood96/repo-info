## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:32207e2959b886220926d923c6306064b4a08cf3ba4470b3c68fc095d01c0cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:c782c9d94bb89c734c3277fb534f9e1aada70acfd368de7b8ad2ac3ccab46d5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 MB (39697640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc2a3ddd459b82cc505383ba6f2229104d60e5b5807640dc36903f373930dbb`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:29:49 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:29:50 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:29:51 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:29:51 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Tue, 09 Aug 2022 18:29:51 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Tue, 09 Aug 2022 18:29:52 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 09 Aug 2022 18:33:47 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:33:48 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:33:48 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:33:48 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:33:48 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:33:48 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:33:48 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:33:49 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:33:49 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:33:49 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:33:49 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:33:49 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:33:49 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c168c83c5b7cbf66a9e59b6eeb2681bba349bbfcfb2210a9e498fbd081911b8`  
		Last Modified: Tue, 09 Aug 2022 18:36:28 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ada8ef30839b781a7752202bb0508c0b31289da9d6c8e2c579b714517f21ca`  
		Last Modified: Tue, 09 Aug 2022 18:36:26 GMT  
		Size: 10.9 KB (10938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5a6827106d9ac255c1074ade8a834fad1c2c24c59abbaa036c30ea7e50bc68`  
		Last Modified: Tue, 09 Aug 2022 18:36:26 GMT  
		Size: 1.1 MB (1089939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd6758e0fde641f96ae3752b918e7005398fc332b5ba08b3fa03ab91e77df9a`  
		Last Modified: Tue, 09 Aug 2022 18:36:31 GMT  
		Size: 35.8 MB (35769404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34e9bb594cf5cb810d65d664e8bd68f3a0c975d4d4b00154b7d9f40f8439680`  
		Last Modified: Tue, 09 Aug 2022 18:36:26 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3664d2d4b6b34c02f920ac62c60d8a02b7f86ad43518170e9f6669027382bb85`  
		Last Modified: Tue, 09 Aug 2022 18:36:25 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5708b3cdfd986537b8e3ea8d34cda88cd993f5bfb5cc6785c14136c4698e3e9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39089261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ee4e6c23206e9a11d221ab76fb1562f8ca76c71216c6363694cbc051e50f89`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:46:24 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:46:24 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:46:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:46:26 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Tue, 09 Aug 2022 18:46:26 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Tue, 09 Aug 2022 18:46:27 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 09 Aug 2022 18:50:43 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:50:44 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:50:44 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:50:44 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:50:44 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:50:44 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:50:45 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:50:45 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:50:45 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:50:45 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:50:45 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:50:45 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:50:45 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b0548d2e71c5e0d69a7d82b4707fa752adad30ef06fb8d34592c20144b1904`  
		Last Modified: Tue, 09 Aug 2022 18:54:11 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efa052f331402356a00e0435bf34e783a18b22cb899d2daf4ec7ed61bea0727`  
		Last Modified: Tue, 09 Aug 2022 18:54:09 GMT  
		Size: 10.7 KB (10653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e349162c85bd03d527832a51a9da69584af33d92d8edf9a2207c4ddbc958d10`  
		Last Modified: Tue, 09 Aug 2022 18:54:09 GMT  
		Size: 1.0 MB (1032556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c61638079e5b7979624aeb3f087b465bbffad1dfb59d11b92390d10a9dc478`  
		Last Modified: Tue, 09 Aug 2022 18:54:18 GMT  
		Size: 35.4 MB (35411073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2eb13384450fae5712b634f4008cea093f07ea7f518bac5a47507283fe8a9e8`  
		Last Modified: Tue, 09 Aug 2022 18:54:09 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf747ffa38af6270fefdb2f9235b0c6e9e21c8f7f51ad1c2c9047c14c55acb8a`  
		Last Modified: Tue, 09 Aug 2022 18:54:09 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2e35d4ccbf3d3a654b178fc0ce2df4ac4a0cb5e885b322c8e26c8bf98cb590bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39757425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf55c9b4a88358382abd5183bb7898690851e52c9a2018ca64b74edd4e4237b5`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 04:59:08 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 10 Aug 2022 04:59:08 GMT
RUN adduser -S eggdrop
# Wed, 10 Aug 2022 04:59:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 10 Aug 2022 04:59:11 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Wed, 10 Aug 2022 04:59:12 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Wed, 10 Aug 2022 04:59:14 GMT
RUN apk --update add --no-cache bash openssl
# Wed, 10 Aug 2022 05:03:55 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 10 Aug 2022 05:03:55 GMT
ENV NICK=
# Wed, 10 Aug 2022 05:03:56 GMT
ENV SERVER=
# Wed, 10 Aug 2022 05:03:57 GMT
ENV LISTEN=3333
# Wed, 10 Aug 2022 05:03:58 GMT
ENV OWNER=
# Wed, 10 Aug 2022 05:03:59 GMT
ENV USERFILE=eggdrop.user
# Wed, 10 Aug 2022 05:04:00 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 10 Aug 2022 05:04:01 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 10 Aug 2022 05:04:02 GMT
EXPOSE 3333
# Wed, 10 Aug 2022 05:04:04 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Wed, 10 Aug 2022 05:04:05 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 10 Aug 2022 05:04:05 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 10 Aug 2022 05:04:06 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3060b0beffa155d47f83aa9efbeacec6ff79bac5cc8b070e9868ebffa09ead2`  
		Last Modified: Wed, 10 Aug 2022 05:07:45 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08703e462ddacbe7b062f32a8efb3072e14041ab9fceadda1ee1d6d2f4895d34`  
		Last Modified: Wed, 10 Aug 2022 05:07:43 GMT  
		Size: 10.7 KB (10676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf23a7adbff6c5611472068f39789bfe48eaf8c20057baf39a5b86f74fd1eb7`  
		Last Modified: Wed, 10 Aug 2022 05:07:43 GMT  
		Size: 1.1 MB (1087550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d69885b947f14c765b071206397a32172ee716a33d2b09aef236df53a024b45`  
		Last Modified: Wed, 10 Aug 2022 05:07:48 GMT  
		Size: 35.9 MB (35936934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d466ea643bb6263ee7a392eb704ff1e5d54ace0c25e6916f888a7e5957bc619`  
		Last Modified: Wed, 10 Aug 2022 05:07:43 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac95e2c27e9c1ad1af9d4b700e56ba878784e113c6e009d69602b3b3313ae399`  
		Last Modified: Wed, 10 Aug 2022 05:07:43 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
