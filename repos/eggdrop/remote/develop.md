## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:5b12d0540557321accba7a80a0586774c6fad7c73c906bd472a3394527fc0924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:ce39bc19b5da9e4d11ff676f2502a7f35efbb36dc30d450a1a387838eac571ea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13545253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f275da570aba93576c2ece3440e19a461da1c25fb2dfde7d0ada3d0a98a1d5`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2020 22:11:32 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 17 Mar 2020 22:11:33 GMT
RUN adduser -S eggdrop
# Tue, 17 Mar 2020 22:11:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 17 Mar 2020 22:11:34 GMT
ENV EGGDROP_SHA256=12f560ad31e27f1ad631964f6d4ca43e97de6b11c35d4b733a44d21216d83bb4
# Tue, 17 Mar 2020 22:11:35 GMT
ENV EGGDROP_COMMIT=7a490c534fd53af99cbf33a85d907785e9156629
# Tue, 17 Mar 2020 22:11:36 GMT
RUN apk --update add --no-cache tcl bash openssl
# Tue, 17 Mar 2020 22:12:33 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 17 Mar 2020 22:12:33 GMT
ENV NICK=
# Tue, 17 Mar 2020 22:12:33 GMT
ENV SERVER=
# Tue, 17 Mar 2020 22:12:33 GMT
ENV LISTEN=3333
# Tue, 17 Mar 2020 22:12:33 GMT
ENV OWNER=
# Tue, 17 Mar 2020 22:12:34 GMT
ENV USERFILE=eggdrop.user
# Tue, 17 Mar 2020 22:12:34 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 17 Mar 2020 22:12:34 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 17 Mar 2020 22:12:34 GMT
EXPOSE 3333
# Tue, 17 Mar 2020 22:12:34 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Tue, 17 Mar 2020 22:12:35 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 17 Mar 2020 22:12:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 17 Mar 2020 22:12:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3868cffd2872233427ba71e3bb0781dd26004c37d485e2532644bf02f38a4f0`  
		Last Modified: Tue, 17 Mar 2020 22:13:54 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff09a9dc8a837eada2a7c22c3a8266772d223841e7be7af20237d48304d7a2a`  
		Last Modified: Tue, 17 Mar 2020 22:13:53 GMT  
		Size: 9.6 KB (9579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabbefdc7699e05a7315c409546136b8d67d3792a8905f66bcb23aba9fa84bcb`  
		Last Modified: Tue, 17 Mar 2020 22:13:54 GMT  
		Size: 2.7 MB (2684248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2507cc63c6ed1baf93feb6367158b34b23a58af5c0dd3af6027b86267bbe3a`  
		Last Modified: Tue, 17 Mar 2020 22:13:55 GMT  
		Size: 8.0 MB (8044654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fa7d6315486c06f0b6efb7c5a2eca1bffe734fdaf4a61bf93f73e05f8f8923`  
		Last Modified: Tue, 17 Mar 2020 22:13:54 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4a9277de066b8a525ebe37087c010e5849830a86d5e9cb76c7fbb2dd60bc79`  
		Last Modified: Tue, 17 Mar 2020 22:13:53 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:08af0a72774f383ae7034f04a3eeaff64577414bbd9f8c81832584087be613d8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13221846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f7c94554c8fc702561614c50ca824f037affa28d8e1f79a8b017476b38980a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2020 17:50:32 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 17 Mar 2020 17:50:36 GMT
RUN adduser -S eggdrop
# Tue, 17 Mar 2020 17:50:40 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 17 Mar 2020 17:50:41 GMT
ENV EGGDROP_SHA256=12f560ad31e27f1ad631964f6d4ca43e97de6b11c35d4b733a44d21216d83bb4
# Tue, 17 Mar 2020 17:50:42 GMT
ENV EGGDROP_COMMIT=7a490c534fd53af99cbf33a85d907785e9156629
# Tue, 17 Mar 2020 17:50:45 GMT
RUN apk --update add --no-cache tcl bash openssl
# Tue, 17 Mar 2020 17:52:37 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 17 Mar 2020 17:52:38 GMT
ENV NICK=
# Tue, 17 Mar 2020 17:52:39 GMT
ENV SERVER=
# Tue, 17 Mar 2020 17:52:40 GMT
ENV LISTEN=3333
# Tue, 17 Mar 2020 17:52:40 GMT
ENV OWNER=
# Tue, 17 Mar 2020 17:52:41 GMT
ENV USERFILE=eggdrop.user
# Tue, 17 Mar 2020 17:52:42 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 17 Mar 2020 17:52:42 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 17 Mar 2020 17:52:43 GMT
EXPOSE 3333
# Tue, 17 Mar 2020 17:52:44 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Tue, 17 Mar 2020 17:52:44 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 17 Mar 2020 17:52:45 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 17 Mar 2020 17:52:46 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40521c432970389515ca9aa325c8d2165a4dfe1ef96c50a5db4f9682711c62e`  
		Last Modified: Tue, 17 Mar 2020 17:52:56 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6047ed14cca4884d08d3bf9134d3558904d56488b2a91d574e14fbbe99dfa96`  
		Last Modified: Tue, 17 Mar 2020 17:52:54 GMT  
		Size: 9.4 KB (9396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce83812801babe05207b48cd9a569e256795cf425ecd822a3e58fb64481e8746`  
		Last Modified: Tue, 17 Mar 2020 17:52:55 GMT  
		Size: 2.6 MB (2608571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f37183248148f53aa91448f1ba874cce5727787699e450991e0143f24f59bd`  
		Last Modified: Tue, 17 Mar 2020 17:52:56 GMT  
		Size: 8.0 MB (7982469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe06de6a15975cc3e505085b0da4347f902ec1e57ad2f774ac2c80e15dc7b806`  
		Last Modified: Tue, 17 Mar 2020 17:52:55 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893ec7c95e964d0c8d1a7b6136f96b50048794b894bfec05b5c643f84413c0bd`  
		Last Modified: Tue, 17 Mar 2020 17:52:54 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:4fb2b476a4cbdcc91f026dfd49bcc65c4d15fae9f548a7b2f6bfd4be6daca734
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13532372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4a327b681064d41c67045cb288eed845112b528a4a660f8a0ac180a839b5d2`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2020 20:25:06 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 17 Mar 2020 20:25:08 GMT
RUN adduser -S eggdrop
# Tue, 17 Mar 2020 20:25:10 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 17 Mar 2020 20:25:11 GMT
ENV EGGDROP_SHA256=12f560ad31e27f1ad631964f6d4ca43e97de6b11c35d4b733a44d21216d83bb4
# Tue, 17 Mar 2020 20:25:12 GMT
ENV EGGDROP_COMMIT=7a490c534fd53af99cbf33a85d907785e9156629
# Tue, 17 Mar 2020 20:25:15 GMT
RUN apk --update add --no-cache tcl bash openssl
# Tue, 17 Mar 2020 20:27:00 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 17 Mar 2020 20:27:01 GMT
ENV NICK=
# Tue, 17 Mar 2020 20:27:02 GMT
ENV SERVER=
# Tue, 17 Mar 2020 20:27:04 GMT
ENV LISTEN=3333
# Tue, 17 Mar 2020 20:27:05 GMT
ENV OWNER=
# Tue, 17 Mar 2020 20:27:06 GMT
ENV USERFILE=eggdrop.user
# Tue, 17 Mar 2020 20:27:07 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 17 Mar 2020 20:27:08 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 17 Mar 2020 20:27:09 GMT
EXPOSE 3333
# Tue, 17 Mar 2020 20:27:10 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Tue, 17 Mar 2020 20:27:11 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 17 Mar 2020 20:27:12 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 17 Mar 2020 20:27:12 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023eff843843c3eb2c037a95c40d59df67d67cd4dcd872526f25a6c1d27c3791`  
		Last Modified: Tue, 17 Mar 2020 20:27:29 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49e784103657670f26f010358c2fa61d817c2dfd862c95d46357e810491a2dc`  
		Last Modified: Tue, 17 Mar 2020 20:27:26 GMT  
		Size: 9.5 KB (9514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bee62275276c944739a0951168cff5fdd8ab95b8ddabbcb8e6bc54df48f6fc`  
		Last Modified: Tue, 17 Mar 2020 20:27:27 GMT  
		Size: 2.7 MB (2722244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c2deec776e8074682593077421753942e86c43c9dbae865a6be4f7445f4bf1`  
		Last Modified: Tue, 17 Mar 2020 20:27:28 GMT  
		Size: 8.1 MB (8073688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2536ccb9a86a1e58dd0c461fd291274dc08510ad5e6bdd03b2861d094fa4a763`  
		Last Modified: Tue, 17 Mar 2020 20:27:26 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e2a20dd8cdd78976b7279e69909fc70ffe02b7f0630e681be38aea4a0f4ebb`  
		Last Modified: Tue, 17 Mar 2020 20:27:26 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
