## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:a588887021cf9b28adc336d096f5852412ae70e3ffdeda2f8fddc4821d570fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:e861d26089709e3df1db6e61fb8635ca714228100c889c08ebf6c93c6f4697bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13890589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7440ba6ea0be9b877530daae0bc0c90adc22a5537e63e6db546476a19568008b`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 02:56:54 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 26 Mar 2021 02:56:55 GMT
RUN adduser -S eggdrop
# Fri, 26 Mar 2021 02:56:56 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 26 Mar 2021 02:56:57 GMT
ENV EGGDROP_SHA256=2968824d5184d54bc2b0d6d3c746ca41cc8342523d919671f33ea2446fef0f36
# Fri, 26 Mar 2021 02:56:57 GMT
ENV EGGDROP_COMMIT=d01a34e163c47641eb9516ed918699b8822a7855
# Fri, 26 Mar 2021 02:56:58 GMT
RUN apk --update add --no-cache tcl bash openssl
# Fri, 26 Mar 2021 02:57:51 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 26 Mar 2021 02:57:51 GMT
ENV NICK=
# Fri, 26 Mar 2021 02:57:51 GMT
ENV SERVER=
# Fri, 26 Mar 2021 02:57:52 GMT
ENV LISTEN=3333
# Fri, 26 Mar 2021 02:57:52 GMT
ENV OWNER=
# Fri, 26 Mar 2021 02:57:52 GMT
ENV USERFILE=eggdrop.user
# Fri, 26 Mar 2021 02:57:52 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 26 Mar 2021 02:57:52 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 26 Mar 2021 02:57:53 GMT
EXPOSE 3333
# Fri, 26 Mar 2021 02:57:53 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Fri, 26 Mar 2021 02:57:53 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 26 Mar 2021 02:57:53 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 26 Mar 2021 02:57:53 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142b4d4bcce7665a93979e1fe1f1091a8834f5695ba6201d0c301b29be4441e4`  
		Last Modified: Fri, 26 Mar 2021 02:59:30 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469ffc84df54c5381e18d169f6e0df862c133266f5b281787b3246642568fc70`  
		Last Modified: Fri, 26 Mar 2021 02:59:27 GMT  
		Size: 9.6 KB (9578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c347f6db0e956d7f05d59096bd85841990c222eb5c9427621e27bc26bdc912bb`  
		Last Modified: Fri, 26 Mar 2021 02:59:28 GMT  
		Size: 2.7 MB (2685278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4721886e46f29e798ba9af371c77658679047472bd3ddb0bebcce398b738ea`  
		Last Modified: Fri, 26 Mar 2021 02:59:29 GMT  
		Size: 8.4 MB (8376554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d864c0cb17983d491e934975067a04927d00ad20bb52484b9e3a4522cd10d4`  
		Last Modified: Fri, 26 Mar 2021 02:59:27 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfd828f273f315bb85145acb808d2918f7806976b8d19743fef395d3fab75b9`  
		Last Modified: Fri, 26 Mar 2021 02:59:27 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:2548c2daf1a05b5124faa0c5b77d459908b6ea54567a393bbecf2a0915f2f522
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13552235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d6ea09914af4883130381515d5a4b24da869a8a90049760f9f90511f5ddc7c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 25 Mar 2021 22:51:39 GMT
ADD file:f9e7465b7bf9cb6b234d24519c80b22b9da7894ea0337e0ac44920114773c8a9 in / 
# Thu, 25 Mar 2021 22:51:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 00:18:05 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 26 Mar 2021 00:18:08 GMT
RUN adduser -S eggdrop
# Fri, 26 Mar 2021 00:18:11 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Fri, 26 Mar 2021 00:18:11 GMT
ENV EGGDROP_SHA256=2968824d5184d54bc2b0d6d3c746ca41cc8342523d919671f33ea2446fef0f36
# Fri, 26 Mar 2021 00:18:12 GMT
ENV EGGDROP_COMMIT=d01a34e163c47641eb9516ed918699b8822a7855
# Fri, 26 Mar 2021 00:18:16 GMT
RUN apk --update add --no-cache tcl bash openssl
# Fri, 26 Mar 2021 00:20:19 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 26 Mar 2021 00:20:20 GMT
ENV NICK=
# Fri, 26 Mar 2021 00:20:21 GMT
ENV SERVER=
# Fri, 26 Mar 2021 00:20:22 GMT
ENV LISTEN=3333
# Fri, 26 Mar 2021 00:20:23 GMT
ENV OWNER=
# Fri, 26 Mar 2021 00:20:24 GMT
ENV USERFILE=eggdrop.user
# Fri, 26 Mar 2021 00:20:24 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 26 Mar 2021 00:20:25 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 26 Mar 2021 00:20:27 GMT
EXPOSE 3333
# Fri, 26 Mar 2021 00:20:28 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Fri, 26 Mar 2021 00:20:29 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 26 Mar 2021 00:20:30 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 26 Mar 2021 00:20:31 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:275240b4b3a35cb935b35bfb1a8700e2b9ca100cd6e33ca8a6f83d056016bd61`  
		Last Modified: Thu, 25 Mar 2021 22:55:29 GMT  
		Size: 2.6 MB (2621328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34be1b52d02353764116f4b71c27c3531ae363dea14dd7f7ec291e807459551`  
		Last Modified: Fri, 26 Mar 2021 00:20:46 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df3fec63b7b30cda31cc85a0837f550ae13c58ce96c042da4c668890e54fc73`  
		Last Modified: Fri, 26 Mar 2021 00:20:44 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09496abf0e0bf9e30341d8888b8a79b7d50c18e514fc0e3041006a7be99b2aa3`  
		Last Modified: Fri, 26 Mar 2021 00:20:47 GMT  
		Size: 2.6 MB (2608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a46396485f46f779c6aeaaa93314d5bf131701a5e2886f49a37e134c69cde6`  
		Last Modified: Fri, 26 Mar 2021 00:20:48 GMT  
		Size: 8.3 MB (8308927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64847b2cc99cbc138c19a266e263c3d53889f69db52e951540d7a9bb664dc5`  
		Last Modified: Fri, 26 Mar 2021 00:20:47 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb675fc149be21eb1ff95b9da69e635c095fdfad5ba6cd0b5e6734adf835813`  
		Last Modified: Fri, 26 Mar 2021 00:20:44 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:9b444990f210bf605ed4ae90bb3a075df7694122793e1c581406ec1e0521931a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13859504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f7daab6b5d3a17bd302333f0704b8e28fd71a7cb40df39381838e7962fb67c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 25 Mar 2021 22:41:33 GMT
ADD file:6fca680ab44d711c282deb126e7ad2f7ab51d84a6364192a4913e178f7d393a0 in / 
# Thu, 25 Mar 2021 22:41:38 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 23:57:18 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 25 Mar 2021 23:57:41 GMT
RUN adduser -S eggdrop
# Thu, 25 Mar 2021 23:58:24 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 25 Mar 2021 23:58:55 GMT
ENV EGGDROP_SHA256=2968824d5184d54bc2b0d6d3c746ca41cc8342523d919671f33ea2446fef0f36
# Thu, 25 Mar 2021 23:59:24 GMT
ENV EGGDROP_COMMIT=d01a34e163c47641eb9516ed918699b8822a7855
# Fri, 26 Mar 2021 00:00:04 GMT
RUN apk --update add --no-cache tcl bash openssl
# Fri, 26 Mar 2021 00:02:19 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 26 Mar 2021 00:02:22 GMT
ENV NICK=
# Fri, 26 Mar 2021 00:02:26 GMT
ENV SERVER=
# Fri, 26 Mar 2021 00:02:31 GMT
ENV LISTEN=3333
# Fri, 26 Mar 2021 00:02:34 GMT
ENV OWNER=
# Fri, 26 Mar 2021 00:02:39 GMT
ENV USERFILE=eggdrop.user
# Fri, 26 Mar 2021 00:02:42 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 26 Mar 2021 00:02:47 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 26 Mar 2021 00:02:51 GMT
EXPOSE 3333
# Fri, 26 Mar 2021 00:02:53 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Fri, 26 Mar 2021 00:02:54 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Fri, 26 Mar 2021 00:03:00 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 26 Mar 2021 00:03:03 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:47185b9379cb432a7a6711ec279fdcb33fe0426be145e1bf61879568c9b54054`  
		Last Modified: Thu, 25 Mar 2021 22:45:46 GMT  
		Size: 2.7 MB (2725878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016b21c12c3099ed521797a14ada34ef399a4c317694fda20c5c7b800f40d8a6`  
		Last Modified: Fri, 26 Mar 2021 00:03:33 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002c4ae16ae920d6a492c4d547d7a976f7560f0b85134e15660d9260ba12bf09`  
		Last Modified: Fri, 26 Mar 2021 00:03:30 GMT  
		Size: 9.5 KB (9514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c950aede66670e24ca5ba703c18bd8bcc9e6b797fbaf0a3945ca6daee0332c`  
		Last Modified: Fri, 26 Mar 2021 00:03:33 GMT  
		Size: 2.7 MB (2722595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffdf7ce175cc943983615132a18618cff03de917f73dbe466b7df2a7b0fc46d2`  
		Last Modified: Fri, 26 Mar 2021 00:03:33 GMT  
		Size: 8.4 MB (8397668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab5b1aa60ad91826e6b56a32b2d3ab1a8a465de3758de93e62d71c59b087131`  
		Last Modified: Fri, 26 Mar 2021 00:03:29 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d0d1a0719d19bc3f476352299d88b5fa59e7c8392711cfacdbdb2043f3e071`  
		Last Modified: Fri, 26 Mar 2021 00:03:29 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
