## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:d18e01b39eef86795361e654ffce2a3cd8eaaca83e1fc98dbf85f9e4e8316ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:b5f0aa4a382738465ce3819b26e74d0c29f12c972a9862b876ae19502f913b39
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14677850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181b71fb5255242e24b7e0216f272851d00f48cc01909af55399dd6db60b980d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 07 Mar 2019 22:19:53 GMT
ADD file:aa17928040e31624cad9c7ed19ac277c5402c4b9ba39f834250affca40c4046e in / 
# Thu, 07 Mar 2019 22:19:53 GMT
CMD ["/bin/sh"]
# Fri, 08 Mar 2019 02:47:47 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 08 Mar 2019 02:47:48 GMT
RUN adduser -S eggdrop
# Fri, 08 Mar 2019 02:47:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 15 Oct 2019 00:29:10 GMT
ENV EGGDROP_SHA256=4e7fc37600dea432a905ccf56c15ef7bb46a3724786eeb08a4bbc1736595214e
# Tue, 15 Oct 2019 00:29:10 GMT
ENV EGGDROP_COMMIT=1b58814e2a4c9ca73c7f6c1b9301681cba8d9af2
# Tue, 15 Oct 2019 00:29:12 GMT
RUN apk --update add --no-cache tcl bash openssl
# Tue, 15 Oct 2019 00:30:02 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 15 Oct 2019 00:30:02 GMT
ENV NICK=
# Tue, 15 Oct 2019 00:30:03 GMT
ENV SERVER=
# Tue, 15 Oct 2019 00:30:03 GMT
ENV LISTEN=3333
# Tue, 15 Oct 2019 00:30:03 GMT
ENV OWNER=
# Tue, 15 Oct 2019 00:30:03 GMT
ENV USERFILE=eggdrop.user
# Tue, 15 Oct 2019 00:30:03 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 15 Oct 2019 00:30:03 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 15 Oct 2019 00:30:04 GMT
EXPOSE 3333
# Tue, 15 Oct 2019 00:30:04 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Tue, 15 Oct 2019 00:30:04 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 15 Oct 2019 00:30:04 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 15 Oct 2019 00:30:04 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:5d20c808ce198565ff70b3ed23a991dd49afac45dece63474b27ce6ed036adc6`  
		Last Modified: Thu, 07 Mar 2019 22:20:24 GMT  
		Size: 2.1 MB (2107098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82912a788c2f6120ebbc3d22526200b675392adcd31b5066f625ab176cd0beae`  
		Last Modified: Fri, 08 Mar 2019 02:51:39 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057ac5e0e765a7a6291e39f11b1a53339da0594768640890795bf3e061643bc8`  
		Last Modified: Fri, 08 Mar 2019 02:51:38 GMT  
		Size: 8.8 KB (8849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f552c2ecc2e3ce41e42787077dfe3308b21e58282595b64b52348f739c5daf2`  
		Last Modified: Tue, 15 Oct 2019 00:30:23 GMT  
		Size: 4.4 MB (4405459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b1f6195b970ac45c21fc56f613292a29ab9e1c73ead151f922bbf8b0690180`  
		Last Modified: Tue, 15 Oct 2019 00:30:23 GMT  
		Size: 8.2 MB (8152588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae846d6da50bff53da263b2a7d022b2da3b070325a20990ca5e873ef5e55f1dc`  
		Last Modified: Tue, 15 Oct 2019 00:30:21 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebdc416a95bd24fca0968373d3867ff13e484011cb215022267254777685e959`  
		Last Modified: Tue, 15 Oct 2019 00:30:22 GMT  
		Size: 706.0 B  
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
