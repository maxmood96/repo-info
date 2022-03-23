## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:448d2e9884d2bd1de2a22846c5bb263ed025e4d7e7323d79a468b75c7cc92e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:6dc7f987a543bd5af3b3630819b63c393f4b50718993b1e83d83cb922f07b5b8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39769225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca91a541c054b2e7ce3e6a9c5a8538842c22be50b07e940b6c413c00c1fad5e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 23 Mar 2022 15:21:21 GMT
ADD file:7386ad893672007cca2d73cec1862d582a69d581ca1d155d4599cb2aa54d5498 in / 
# Wed, 23 Mar 2022 15:21:21 GMT
CMD ["/bin/sh"]
# Wed, 23 Mar 2022 18:00:24 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 23 Mar 2022 18:00:24 GMT
RUN adduser -S eggdrop
# Wed, 23 Mar 2022 18:00:25 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 23 Mar 2022 18:00:25 GMT
ENV EGGDROP_SHA256=85700bdd1e5e709e7ac44fc4cac3bf06ab674ead4fb1df99f1ba8cb892c27a3c
# Wed, 23 Mar 2022 18:00:25 GMT
ENV EGGDROP_COMMIT=6959f1943659db6117b93262d18b27dd98313206
# Wed, 23 Mar 2022 18:00:26 GMT
RUN apk --update add --no-cache bash openssl
# Wed, 23 Mar 2022 18:04:14 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 23 Mar 2022 18:04:14 GMT
ENV NICK=
# Wed, 23 Mar 2022 18:04:14 GMT
ENV SERVER=
# Wed, 23 Mar 2022 18:04:15 GMT
ENV LISTEN=3333
# Wed, 23 Mar 2022 18:04:15 GMT
ENV OWNER=
# Wed, 23 Mar 2022 18:04:15 GMT
ENV USERFILE=eggdrop.user
# Wed, 23 Mar 2022 18:04:15 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 23 Mar 2022 18:04:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 23 Mar 2022 18:04:15 GMT
EXPOSE 3333
# Wed, 23 Mar 2022 18:04:15 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Wed, 23 Mar 2022 18:04:15 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 23 Mar 2022 18:04:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 23 Mar 2022 18:04:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:3aa4d0bbde192bfaba75f2d124d8cf2e6de452ae03e55d54105e46b06eb8127e`  
		Last Modified: Wed, 23 Mar 2022 15:21:44 GMT  
		Size: 2.8 MB (2812689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255d707abd67e2212c0fc03a42dec647e762d447679bc356b91ee54e0d6a2279`  
		Last Modified: Wed, 23 Mar 2022 18:04:46 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14c34e2c83cb8386f15d815f78551415b0902c87b29d55d6cf6d927d447e905`  
		Last Modified: Wed, 23 Mar 2022 18:04:43 GMT  
		Size: 11.0 KB (10951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5822447b6736a6926d59167c3028d4b67485d04cb49b0d51c1f9f9a56de5a2d`  
		Last Modified: Wed, 23 Mar 2022 18:04:44 GMT  
		Size: 1.1 MB (1089640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd5c879203d7fc23ea2576276c36cb94b1eb1bc2145bb9ab0604d2ce145fac6`  
		Last Modified: Wed, 23 Mar 2022 18:04:49 GMT  
		Size: 35.9 MB (35852104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5a15c9f725267f25678469c1126908993d96012c017bdc13a955eb42a79674`  
		Last Modified: Wed, 23 Mar 2022 18:04:43 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7d93b5f91d9637631b5c443044c61c7f7985d546ad0b9ed44d60dbc72c2222`  
		Last Modified: Wed, 23 Mar 2022 18:04:43 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:24d74c58a4f0284360af9c6e90eac4a24bc33243f7a37eb2c33751412fe57b9c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39168942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9a53a52110af0ab7d4e6b839b07dcfe527eb869a861240cc09c9ab5aa33e09`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 17 Mar 2022 02:26:45 GMT
ADD file:9c8618405ef54d562132919ffe49c862d014b402e0e4813b87bf01574fa04c0e in / 
# Thu, 17 Mar 2022 02:26:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 05:28:28 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 17 Mar 2022 05:28:30 GMT
RUN adduser -S eggdrop
# Thu, 17 Mar 2022 05:28:32 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 17 Mar 2022 05:28:33 GMT
ENV EGGDROP_SHA256=85700bdd1e5e709e7ac44fc4cac3bf06ab674ead4fb1df99f1ba8cb892c27a3c
# Thu, 17 Mar 2022 05:28:33 GMT
ENV EGGDROP_COMMIT=6959f1943659db6117b93262d18b27dd98313206
# Thu, 17 Mar 2022 05:28:35 GMT
RUN apk --update add --no-cache bash openssl
# Thu, 17 Mar 2022 05:38:44 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 17 Mar 2022 05:38:45 GMT
ENV NICK=
# Thu, 17 Mar 2022 05:38:46 GMT
ENV SERVER=
# Thu, 17 Mar 2022 05:38:46 GMT
ENV LISTEN=3333
# Thu, 17 Mar 2022 05:38:46 GMT
ENV OWNER=
# Thu, 17 Mar 2022 05:38:47 GMT
ENV USERFILE=eggdrop.user
# Thu, 17 Mar 2022 05:38:47 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 17 Mar 2022 05:38:48 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 17 Mar 2022 05:38:48 GMT
EXPOSE 3333
# Thu, 17 Mar 2022 05:38:49 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Thu, 17 Mar 2022 05:38:49 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 17 Mar 2022 05:38:49 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 17 Mar 2022 05:38:50 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:787f016efa9bc7812361be134f731e845b97fba19169cf3615e7048c0412380e`  
		Last Modified: Thu, 17 Mar 2022 02:28:24 GMT  
		Size: 2.6 MB (2624973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b68efa6a1997325a5ae45e779e3a144141f203b55e7238ffdf2a34e7054a53`  
		Last Modified: Thu, 17 Mar 2022 05:39:47 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8edf584a6d64b54a3f3ec767c0e0998424b3d5e97db05836574741e8de66c09`  
		Last Modified: Thu, 17 Mar 2022 05:39:45 GMT  
		Size: 10.7 KB (10663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0864307a79503dd64dc6fe912a977e1f5db6f1cb81d972b229d718aa4d5adb`  
		Last Modified: Thu, 17 Mar 2022 05:39:46 GMT  
		Size: 1.0 MB (1032374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1248ce657c21528dfe5b7bbcde4402928c58776f5d5f78e9d4d009c95cad32a9`  
		Last Modified: Thu, 17 Mar 2022 05:40:10 GMT  
		Size: 35.5 MB (35497075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00c9b64037e1a3a6d789a32a21f951a6970d05d37e8c73cac695c5a446d8278`  
		Last Modified: Thu, 17 Mar 2022 05:39:45 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306d1e09adf54334b46c6ceed7b7b9f39b6c7b659b494314db12588a00ac8a5e`  
		Last Modified: Thu, 17 Mar 2022 05:39:45 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:c76047585ccd86aca955c0e6bc42a3411c75416e2852eba414f25b1390f333b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39838487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e456e828f6873a23e76e6c5f10ef1a9bca164127e919c17ad41e52a79036e1d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 17 Mar 2022 03:19:52 GMT
ADD file:cd7d91362950471ca4678cf3833dc47119ab519dea51424c847bbbb21e1649d4 in / 
# Thu, 17 Mar 2022 03:19:52 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 06:48:56 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 17 Mar 2022 06:48:57 GMT
RUN adduser -S eggdrop
# Thu, 17 Mar 2022 06:48:59 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 17 Mar 2022 06:48:59 GMT
ENV EGGDROP_SHA256=85700bdd1e5e709e7ac44fc4cac3bf06ab674ead4fb1df99f1ba8cb892c27a3c
# Thu, 17 Mar 2022 06:49:00 GMT
ENV EGGDROP_COMMIT=6959f1943659db6117b93262d18b27dd98313206
# Thu, 17 Mar 2022 06:49:01 GMT
RUN apk --update add --no-cache bash openssl
# Thu, 17 Mar 2022 06:53:49 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 17 Mar 2022 06:53:49 GMT
ENV NICK=
# Thu, 17 Mar 2022 06:53:50 GMT
ENV SERVER=
# Thu, 17 Mar 2022 06:53:51 GMT
ENV LISTEN=3333
# Thu, 17 Mar 2022 06:53:52 GMT
ENV OWNER=
# Thu, 17 Mar 2022 06:53:53 GMT
ENV USERFILE=eggdrop.user
# Thu, 17 Mar 2022 06:53:54 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 17 Mar 2022 06:53:55 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 17 Mar 2022 06:53:56 GMT
EXPOSE 3333
# Thu, 17 Mar 2022 06:53:58 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Thu, 17 Mar 2022 06:53:59 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 17 Mar 2022 06:53:59 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 17 Mar 2022 06:54:00 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:148d739a8e6b9342daa1f5b428d3a3c6118f340f21df28c16e06f918ef150147`  
		Last Modified: Thu, 17 Mar 2022 03:20:45 GMT  
		Size: 2.7 MB (2714807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49fc19ed302ad49df1bc3ac497157d115745e9ed6cf702ccc18ab6489dc1d8e`  
		Last Modified: Thu, 17 Mar 2022 06:54:29 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa846be34df0900bdf403c5c5f07bbd0a2fb3585e0eecd8b6b4a760a75448ba8`  
		Last Modified: Thu, 17 Mar 2022 06:54:27 GMT  
		Size: 10.7 KB (10673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21934b1a15b075daf87e07d881760d39a0a6f0cd143cff973fa2a64cc382f1a8`  
		Last Modified: Thu, 17 Mar 2022 06:54:27 GMT  
		Size: 1.1 MB (1087192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab5070e3f7ae4612ff31aa43e7241f726f60ca30e131e3dd5a2b0c946b5e485`  
		Last Modified: Thu, 17 Mar 2022 06:54:32 GMT  
		Size: 36.0 MB (36021980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585fe8df42b6a33034dff05c622b4c544c0d759c6b66bd6a320a418cf441c6b3`  
		Last Modified: Thu, 17 Mar 2022 06:54:27 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92dc54c4e71ff38f1db4507e6c33a3ce6f4707945d7ac42d1eca7708011f86af`  
		Last Modified: Thu, 17 Mar 2022 06:54:27 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
