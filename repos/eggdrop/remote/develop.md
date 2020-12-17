## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:d3977629f4b138b072d88749a458f73be1ae4a01bfb000fd7458dfcb701ef669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:075ac1b940cd44864b8ca5408cf08d75907b293b5a80ad5f64cf5bc398fd1c38
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13229449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d48351a13e51ee145c77cf30f9b65bd4ddfc3eb1fda136c8051815df17df61`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:21:14 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Fri, 24 Apr 2020 14:21:15 GMT
RUN adduser -S eggdrop
# Fri, 24 Apr 2020 14:21:16 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 29 Oct 2020 18:19:35 GMT
ENV EGGDROP_SHA256=c03b55ff977b671d5d43bfc2956294ec31bda1936ec0520b260c7e7020c6f656
# Thu, 29 Oct 2020 18:19:35 GMT
ENV EGGDROP_COMMIT=a2bd85e40c85a6dcfaf8d0f11bb7967f82ac67a1
# Thu, 29 Oct 2020 18:19:36 GMT
RUN apk --update add --no-cache tcl bash openssl
# Thu, 29 Oct 2020 18:20:33 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 29 Oct 2020 18:20:33 GMT
ENV NICK=
# Thu, 29 Oct 2020 18:20:33 GMT
ENV SERVER=
# Thu, 29 Oct 2020 18:20:34 GMT
ENV LISTEN=3333
# Thu, 29 Oct 2020 18:20:34 GMT
ENV OWNER=
# Thu, 29 Oct 2020 18:20:34 GMT
ENV USERFILE=eggdrop.user
# Thu, 29 Oct 2020 18:20:34 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 29 Oct 2020 18:20:34 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 29 Oct 2020 18:20:35 GMT
EXPOSE 3333
# Thu, 29 Oct 2020 18:20:35 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Thu, 29 Oct 2020 18:20:35 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 29 Oct 2020 18:20:35 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 29 Oct 2020 18:20:35 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0cdf0ff845235e19454000f632a4d9bf6d978c7948da54b51bf3962d766f4c`  
		Last Modified: Fri, 24 Apr 2020 14:23:40 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05e553ff44d8d1344fff59fed8897d80984977807b655be3d15128815d5bcf0`  
		Last Modified: Fri, 24 Apr 2020 14:23:38 GMT  
		Size: 9.6 KB (9573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a949cc28cd9cf9019880fd8c36705e696b7d085bb54a9deeae8c234e35299af0`  
		Last Modified: Thu, 29 Oct 2020 18:20:48 GMT  
		Size: 2.7 MB (2685008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818a418e65bd8fdd52d06302d489bdf88c0cb7332839c5e8204de9b5f20a4205`  
		Last Modified: Thu, 29 Oct 2020 18:20:49 GMT  
		Size: 7.7 MB (7717723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c154fb957a3cf4f88473f05e485108ae9423bd3b3b758fddac43879beb978af`  
		Last Modified: Thu, 29 Oct 2020 18:20:48 GMT  
		Size: 1.9 KB (1888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf84d87b4a63bc74493f01f6ed30547171e39b866fca484e05af2228a766a9f2`  
		Last Modified: Thu, 29 Oct 2020 18:20:48 GMT  
		Size: 707.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:6cacb0cc8579625a00fa587793165b49dac436f015a0340dbe930c86777425e9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12901828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16acecdff96c633acb143dc1768fc524e456c1824a6fc124ba575f6b753bedd`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:53 GMT
ADD file:e3a6f7566ee3c2ba61d27d801d3522e045a4be64a42f32ee52d933b68338d06f in / 
# Wed, 16 Dec 2020 23:49:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:11:55 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 17 Dec 2020 01:11:57 GMT
RUN adduser -S eggdrop
# Thu, 17 Dec 2020 01:12:00 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 17 Dec 2020 01:12:01 GMT
ENV EGGDROP_SHA256=c03b55ff977b671d5d43bfc2956294ec31bda1936ec0520b260c7e7020c6f656
# Thu, 17 Dec 2020 01:12:01 GMT
ENV EGGDROP_COMMIT=a2bd85e40c85a6dcfaf8d0f11bb7967f82ac67a1
# Thu, 17 Dec 2020 01:12:05 GMT
RUN apk --update add --no-cache tcl bash openssl
# Thu, 17 Dec 2020 01:14:03 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 17 Dec 2020 01:14:04 GMT
ENV NICK=
# Thu, 17 Dec 2020 01:14:05 GMT
ENV SERVER=
# Thu, 17 Dec 2020 01:14:06 GMT
ENV LISTEN=3333
# Thu, 17 Dec 2020 01:14:07 GMT
ENV OWNER=
# Thu, 17 Dec 2020 01:14:08 GMT
ENV USERFILE=eggdrop.user
# Thu, 17 Dec 2020 01:14:08 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 17 Dec 2020 01:14:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 17 Dec 2020 01:14:10 GMT
EXPOSE 3333
# Thu, 17 Dec 2020 01:14:10 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Thu, 17 Dec 2020 01:14:11 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 17 Dec 2020 01:14:12 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 17 Dec 2020 01:14:13 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:56fec67ad66eea034cf5b7d0d0ffd355c0fe87611bad132ac5a952fcaa52138b`  
		Last Modified: Wed, 16 Dec 2020 23:50:34 GMT  
		Size: 2.6 MB (2620769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246d33d7e776a09750998663c72dbd23c110005878d82ca6abe5c6dcefc0967c`  
		Last Modified: Thu, 17 Dec 2020 01:14:39 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2db78c4c9d4fc9a1b9f1c23b518a7c867aa525407d02463fe69990aa5ecc860`  
		Last Modified: Thu, 17 Dec 2020 01:14:38 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dbd5777040de4ab2583b43f8d2949eed182a6f60cdb0740546e6df35369fb4`  
		Last Modified: Thu, 17 Dec 2020 01:14:37 GMT  
		Size: 2.6 MB (2608674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb871ccf8cdbd8a91e9cc1fd2e2b981520da51ca5564ef5fe51c3c59d7fef93`  
		Last Modified: Thu, 17 Dec 2020 01:14:40 GMT  
		Size: 7.7 MB (7659149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5b7a25c9dd1601e3cfe947ad0fea862d3141aab6f35df8afb6a93633be5d4e`  
		Last Modified: Thu, 17 Dec 2020 01:14:36 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b123264128fba40c616ddca02c7408a168925ff266201d28c2dd064b6273899c`  
		Last Modified: Thu, 17 Dec 2020 01:14:36 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2f20bd899cf1c0fa3ddc2bc4e11ec8da8feb86566751063e5ca1773e393d6488
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13196257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40eed0cf9c5db647ae8f6395b95b9e7a9a8d92d0019e6e5fad19bc43ae25e444`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:32:14 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 17 Dec 2020 01:32:17 GMT
RUN adduser -S eggdrop
# Thu, 17 Dec 2020 01:32:20 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 17 Dec 2020 01:32:20 GMT
ENV EGGDROP_SHA256=c03b55ff977b671d5d43bfc2956294ec31bda1936ec0520b260c7e7020c6f656
# Thu, 17 Dec 2020 01:32:22 GMT
ENV EGGDROP_COMMIT=a2bd85e40c85a6dcfaf8d0f11bb7967f82ac67a1
# Thu, 17 Dec 2020 01:32:27 GMT
RUN apk --update add --no-cache tcl bash openssl
# Thu, 17 Dec 2020 01:34:21 GMT
RUN apk --update add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256  develop.tar.gz" | sha256sum -c -   && tar -zxvf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 17 Dec 2020 01:34:22 GMT
ENV NICK=
# Thu, 17 Dec 2020 01:34:23 GMT
ENV SERVER=
# Thu, 17 Dec 2020 01:34:25 GMT
ENV LISTEN=3333
# Thu, 17 Dec 2020 01:34:27 GMT
ENV OWNER=
# Thu, 17 Dec 2020 01:34:27 GMT
ENV USERFILE=eggdrop.user
# Thu, 17 Dec 2020 01:34:28 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 17 Dec 2020 01:34:29 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 17 Dec 2020 01:34:30 GMT
EXPOSE 3333
# Thu, 17 Dec 2020 01:34:30 GMT
COPY file:4b2e5310f8e2b48c1ffa7bba797207637a35204a73634e98dc622889d320f394 in /home/eggdrop/eggdrop 
# Thu, 17 Dec 2020 01:34:31 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 17 Dec 2020 01:34:32 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 17 Dec 2020 01:34:33 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ed9edd80b941cb09da42270ec30fac48f2e333f20c112a31ceb4f07bbc5061`  
		Last Modified: Thu, 17 Dec 2020 01:34:58 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1b41d127cfd4f5f711232eeaaaaa19a7df724524428ce4e8bb07e85e0f4d0c`  
		Last Modified: Thu, 17 Dec 2020 01:34:54 GMT  
		Size: 9.5 KB (9514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9681cad244c6e2e165bdfb21360dc94cdef99de5ed2005f727c50413e6509c6e`  
		Last Modified: Thu, 17 Dec 2020 01:34:55 GMT  
		Size: 2.7 MB (2722540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1659aaa2f15dfbcb14f3daa30f8d04e477d66145cb127066cdc1b015059582c9`  
		Last Modified: Thu, 17 Dec 2020 01:34:57 GMT  
		Size: 7.7 MB (7735136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b21fb9dfb3f62df79797c1dbd01d48f0acd8925e1cad2f29583dc3bf5cbdf1`  
		Last Modified: Thu, 17 Dec 2020 01:34:54 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d73481b5f7d9d62f99f3a4779c2629d551023fe1ea1d23ff4379582b633a7c`  
		Last Modified: Thu, 17 Dec 2020 01:34:54 GMT  
		Size: 705.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
