## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:26370f2980837f6755712d00d80e6e98734619faf418b07ae443555763485e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:863a1dca7315a511d83332073aacfa18fac03397358b5fe5ba2e7b8a75a276e5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13903044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576dc66e6ec6201c1e65dcb5da0e0c2fa11511e7a1501fbe397e97153707e91c`
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
# Wed, 14 Apr 2021 20:26:41 GMT
ENV EGGDROP_SHA256=ef482116819630aa65127d1c3d04e3762cbf45827bc66d7d505d481960209448
# Wed, 14 Apr 2021 20:26:41 GMT
ENV EGGDROP_COMMIT=d7729c4bbfb30e831e879da3985832e1db503dff
# Wed, 14 Apr 2021 20:26:42 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 20:27:33 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 20:27:33 GMT
ENV NICK=
# Wed, 14 Apr 2021 20:27:34 GMT
ENV SERVER=
# Wed, 14 Apr 2021 20:27:34 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 20:27:34 GMT
ENV OWNER=
# Wed, 14 Apr 2021 20:27:34 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 20:27:34 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 20:27:35 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 20:27:35 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 20:27:35 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 20:27:35 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 20:27:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 20:27:36 GMT
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
	-	`sha256:3e603a0c1dc60f9e4445917bed7c38bd060a3e336da983bab83ed39e1d071ec3`  
		Last Modified: Wed, 14 Apr 2021 20:31:00 GMT  
		Size: 2.7 MB (2685312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43656001cc97fbe42d47f6244dd22e9dc0d4091492bd2a44536fcb0aa27a7f4`  
		Last Modified: Wed, 14 Apr 2021 20:30:59 GMT  
		Size: 8.4 MB (8388045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6b5e043a85370cf7210f1f8531dbc218be306517c005b8eae5be566056b7f6`  
		Last Modified: Wed, 14 Apr 2021 20:30:58 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3914a952f41a10e7c83dd041fa5773f3c6328b582d6ea304077875cb445d9d06`  
		Last Modified: Wed, 14 Apr 2021 20:31:00 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:c3bf9c2cdda221f8f156f3057dd408719ef78bff09878a6c82205fd7b26d7d76
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13560543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08412b7b45976542614516e11642429bae78a720cfd2198019236710aa3dc69`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:58 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Wed, 14 Apr 2021 18:49:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:53:23 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:53:38 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:53:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:53:49 GMT
ENV EGGDROP_SHA256=ef482116819630aa65127d1c3d04e3762cbf45827bc66d7d505d481960209448
# Wed, 14 Apr 2021 19:53:52 GMT
ENV EGGDROP_COMMIT=d7729c4bbfb30e831e879da3985832e1db503dff
# Wed, 14 Apr 2021 19:54:07 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:56:19 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:56:21 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:56:24 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:56:26 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:56:27 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:56:29 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:56:31 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:56:32 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:56:34 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:56:36 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:56:39 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:56:40 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:56:41 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22d78ffb0e230408fd608629b875c877407afeedd0a45af9c9ed2169117984a`  
		Last Modified: Wed, 14 Apr 2021 20:00:04 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c9123ad8d661005614f22f8c8a3d8e82e151f2596a6b93ce83809a14465b9b`  
		Last Modified: Wed, 14 Apr 2021 20:00:02 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d2497d083ecbb0cc42823a3ca7c0f6ad3b17b85d126e8bd66a9fdac142d9a3`  
		Last Modified: Wed, 14 Apr 2021 20:00:04 GMT  
		Size: 2.6 MB (2608740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca996bb7fde0998b70d0a1136b7178cce6ed3fe68b18596b71e73446dc5aa649`  
		Last Modified: Wed, 14 Apr 2021 20:00:05 GMT  
		Size: 8.3 MB (8316642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dd72ae776e770eebcfd03df0c40615a2bdcc024cfe43b8e8e08c4ed405c121`  
		Last Modified: Wed, 14 Apr 2021 20:00:02 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78dc612d9cb44bd8c9252e2c38ca1cc514123fa1a8af2c91306702bd2b6e3680`  
		Last Modified: Wed, 14 Apr 2021 20:00:02 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:850252afe44da6dab30835de33df0e0272f31a8e27faa61b07eb6fa95da1e050
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13869702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f40ebf6796d89015db913a8e3ef2b45e2aa1c4c6d58221f8aa89338eadf4d3`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:36:29 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 14 Apr 2021 19:36:31 GMT
RUN adduser -S eggdrop
# Wed, 14 Apr 2021 19:36:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 14 Apr 2021 19:36:34 GMT
ENV EGGDROP_SHA256=ef482116819630aa65127d1c3d04e3762cbf45827bc66d7d505d481960209448
# Wed, 14 Apr 2021 19:36:35 GMT
ENV EGGDROP_COMMIT=d7729c4bbfb30e831e879da3985832e1db503dff
# Wed, 14 Apr 2021 19:36:39 GMT
RUN apk --update add --no-cache tcl bash openssl
# Wed, 14 Apr 2021 19:38:32 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 14 Apr 2021 19:38:33 GMT
ENV NICK=
# Wed, 14 Apr 2021 19:38:35 GMT
ENV SERVER=
# Wed, 14 Apr 2021 19:38:36 GMT
ENV LISTEN=3333
# Wed, 14 Apr 2021 19:38:37 GMT
ENV OWNER=
# Wed, 14 Apr 2021 19:38:38 GMT
ENV USERFILE=eggdrop.user
# Wed, 14 Apr 2021 19:38:39 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 14 Apr 2021 19:38:40 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 14 Apr 2021 19:38:41 GMT
EXPOSE 3333
# Wed, 14 Apr 2021 19:38:42 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Wed, 14 Apr 2021 19:38:43 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 14 Apr 2021 19:38:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 14 Apr 2021 19:38:45 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b997aad343dbd28650ee0bcb299c642ad54a09abb3b0cf217846adcdee4a68`  
		Last Modified: Wed, 14 Apr 2021 19:41:47 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45ce3889961128acbf24016684d8ea750fc7b4f4b7896eda664f96033f0f11f`  
		Last Modified: Wed, 14 Apr 2021 19:41:45 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a607909297e6f6a696926e7263bf92de9005af01c3bac0e8039bcd663d5e92`  
		Last Modified: Wed, 14 Apr 2021 19:41:46 GMT  
		Size: 2.7 MB (2722578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f5323a1ed5b8a53964900fa41cbaab40682b4315811604f7ce33e64e176290`  
		Last Modified: Wed, 14 Apr 2021 19:41:47 GMT  
		Size: 8.4 MB (8406817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f9df699f58db3c3d1f9926c52a6a610e80b1a751e60a18976d7aa4945a21ad`  
		Last Modified: Wed, 14 Apr 2021 19:41:45 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f056d5429942f9902fa6ce8c9b6858ff7cc00d8238c6fd694ad28f2a20ae65f8`  
		Last Modified: Wed, 14 Apr 2021 19:41:45 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
