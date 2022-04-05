## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:eac0d90c9d9332b31c04b2e47c7702ded31e015a2f5961d2a1247cae966d0ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:1aeebd57ae1707c3710b46b7e33409e2b0fbfe6493731ea692e380dba408e394
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39770851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4694c76ab607e85da34b92dae862739842f70ab6d675902bacd27bbab2b959`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 11:58:38 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 29 Mar 2022 11:58:39 GMT
RUN adduser -S eggdrop
# Tue, 29 Mar 2022 11:58:40 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 29 Mar 2022 11:58:40 GMT
ENV EGGDROP_SHA256=85700bdd1e5e709e7ac44fc4cac3bf06ab674ead4fb1df99f1ba8cb892c27a3c
# Tue, 29 Mar 2022 11:58:40 GMT
ENV EGGDROP_COMMIT=6959f1943659db6117b93262d18b27dd98313206
# Tue, 29 Mar 2022 11:58:41 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 29 Mar 2022 12:02:29 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 29 Mar 2022 12:02:29 GMT
ENV NICK=
# Tue, 29 Mar 2022 12:02:29 GMT
ENV SERVER=
# Tue, 29 Mar 2022 12:02:29 GMT
ENV LISTEN=3333
# Tue, 29 Mar 2022 12:02:30 GMT
ENV OWNER=
# Tue, 29 Mar 2022 12:02:30 GMT
ENV USERFILE=eggdrop.user
# Tue, 29 Mar 2022 12:02:30 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 29 Mar 2022 12:02:30 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 29 Mar 2022 12:02:30 GMT
EXPOSE 3333
# Tue, 29 Mar 2022 12:02:30 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 29 Mar 2022 12:02:30 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 29 Mar 2022 12:02:30 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 29 Mar 2022 12:02:30 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fb61010abf5a69cbde6fef350ccb3f1cccdb738a529a130007939fb12aa7bc`  
		Last Modified: Tue, 29 Mar 2022 12:04:07 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ca98fe50b6a7460ca0403abdbdfe56f9f0f65ad028d0646a1c426a65a2af26`  
		Last Modified: Tue, 29 Mar 2022 12:04:04 GMT  
		Size: 10.9 KB (10947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f973893e5f0430443a84b87f5d35b80d20b2609e7a32d53ff3b71851430c41`  
		Last Modified: Tue, 29 Mar 2022 12:04:05 GMT  
		Size: 1.1 MB (1089643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66dc78d5804f959f865916cd011afe1cf55cbd14a725b5559f15dbff9c3dffe9`  
		Last Modified: Tue, 29 Mar 2022 12:04:10 GMT  
		Size: 35.9 MB (35851903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf69ecc0001bcbe74f66625dd25d9afecaa67722bfbb0385c300e9d9363fb542`  
		Last Modified: Tue, 29 Mar 2022 12:04:04 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa21b18065fc4618ccc656606eb3a3bab4b10bafb95838f61fd9181e2aca745`  
		Last Modified: Tue, 29 Mar 2022 12:04:04 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d44ee11b7644f8abc0a45dd6a217bf889ba0609c4d821752f914b82f36f906f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39165975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3b0ecf2e6aae1404fb2c832457e6b21f9104ad254f831964b14b688212fb09`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:31:44 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 03:31:46 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 03:31:48 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 03:31:49 GMT
ENV EGGDROP_SHA256=85700bdd1e5e709e7ac44fc4cac3bf06ab674ead4fb1df99f1ba8cb892c27a3c
# Tue, 05 Apr 2022 03:31:49 GMT
ENV EGGDROP_COMMIT=6959f1943659db6117b93262d18b27dd98313206
# Tue, 05 Apr 2022 03:31:52 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 05 Apr 2022 03:42:15 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 03:42:16 GMT
ENV NICK=
# Tue, 05 Apr 2022 03:42:16 GMT
ENV SERVER=
# Tue, 05 Apr 2022 03:42:17 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 03:42:17 GMT
ENV OWNER=
# Tue, 05 Apr 2022 03:42:18 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 03:42:18 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 03:42:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 03:42:19 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 03:42:20 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 03:42:20 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 03:42:21 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 03:42:21 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f46acd206d1b9854dd7a69f3dd94d51ffb03228b347337d6755524e938f848d`  
		Last Modified: Tue, 05 Apr 2022 03:45:57 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ab9123d31326e4f773e35061abb57883ec6b6221e6df8719354fc8598c9123`  
		Last Modified: Tue, 05 Apr 2022 03:45:55 GMT  
		Size: 10.6 KB (10643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f62deb3100b6e70cd59c7464cb4b29e2b0838161967661ab0f746b51836a177`  
		Last Modified: Tue, 05 Apr 2022 03:45:56 GMT  
		Size: 1.0 MB (1032380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc277f2652bea54f29023ad9ac96a2bb389a9ccf2e329165f706ec56ea3f56f9`  
		Last Modified: Tue, 05 Apr 2022 03:46:16 GMT  
		Size: 35.5 MB (35497123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c017a0ffbca5f124cc57390d8252246ef4d6816998bb3a6a2803283b7c410e4`  
		Last Modified: Tue, 05 Apr 2022 03:45:55 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbe5ead144b0f664d6067b076f6aafeee3934feae5435527f1094d3c70d7dee`  
		Last Modified: Tue, 05 Apr 2022 03:45:55 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:58f83502c20b55f1671395b5223199de3f924fb00bac184289616356097c3538
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39840336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517417f6c33ea4e8eda7d28e039ac194c20d366292a9fcaacb84af1a9c259985`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:03:36 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 05 Apr 2022 04:03:37 GMT
RUN adduser -S eggdrop
# Tue, 05 Apr 2022 04:03:38 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 05 Apr 2022 04:03:39 GMT
ENV EGGDROP_SHA256=85700bdd1e5e709e7ac44fc4cac3bf06ab674ead4fb1df99f1ba8cb892c27a3c
# Tue, 05 Apr 2022 04:03:40 GMT
ENV EGGDROP_COMMIT=6959f1943659db6117b93262d18b27dd98313206
# Tue, 05 Apr 2022 04:03:41 GMT
RUN apk --update add --no-cache bash openssl
# Tue, 05 Apr 2022 04:08:22 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 05 Apr 2022 04:08:22 GMT
ENV NICK=
# Tue, 05 Apr 2022 04:08:23 GMT
ENV SERVER=
# Tue, 05 Apr 2022 04:08:24 GMT
ENV LISTEN=3333
# Tue, 05 Apr 2022 04:08:25 GMT
ENV OWNER=
# Tue, 05 Apr 2022 04:08:26 GMT
ENV USERFILE=eggdrop.user
# Tue, 05 Apr 2022 04:08:27 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 05 Apr 2022 04:08:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 05 Apr 2022 04:08:29 GMT
EXPOSE 3333
# Tue, 05 Apr 2022 04:08:31 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Tue, 05 Apr 2022 04:08:32 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 05 Apr 2022 04:08:32 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 05 Apr 2022 04:08:33 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687fbd14cec7fbb8ee2d3dfd1bedd832165c780a579635649359ea5d966007c3`  
		Last Modified: Tue, 05 Apr 2022 04:10:33 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778e0ebd563495b9fbda0eb57ed55b539e2a45c085cbb1dc1866b09b01007cb8`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 10.7 KB (10674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97dd87a81b82b563a55309efc83e5bd1449b7594eca26057853510451078447f`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 1.1 MB (1087188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf6a2b0c72c2b5112ebe5cf3034eb8be33586e208322d0534280410057a0766`  
		Last Modified: Tue, 05 Apr 2022 04:10:36 GMT  
		Size: 36.0 MB (36022170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b64c592a79e2e4db70bb2315b6a98f3746dffe89a10745de53586994195e89`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b44e16d37a27f754c949073353a7972c76ba0ef406b0b24db57f8fca427df18`  
		Last Modified: Tue, 05 Apr 2022 04:10:31 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
