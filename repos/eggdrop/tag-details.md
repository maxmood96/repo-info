<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.3`](#eggdrop193)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:51b72394950be4f5f8ff1cf27c7d85dae09e6fe0de081cdbee423daab4b2baf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:e4d91474210dd34a83e1b0b2ac471a84976d9a561810352f0274534afdc674de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8185645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e242b5d3f669db45a6704607e67e8f090ddcaf9db6695faad34ef83b5c8d719c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:35:06 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:35:07 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:35:08 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:35:09 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 11 Aug 2022 18:20:27 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3.tar.gz.asc eggdrop-1.9.3.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3.tar.gz.asc   && tar -zxvf eggdrop-1.9.3.tar.gz   && rm eggdrop-1.9.3.tar.gz   && ( cd eggdrop-1.9.3     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 11 Aug 2022 18:20:27 GMT
ENV NICK=
# Thu, 11 Aug 2022 18:20:27 GMT
ENV SERVER=
# Thu, 11 Aug 2022 18:20:27 GMT
ENV LISTEN=3333
# Thu, 11 Aug 2022 18:20:27 GMT
ENV OWNER=
# Thu, 11 Aug 2022 18:20:28 GMT
ENV USERFILE=eggdrop.user
# Thu, 11 Aug 2022 18:20:28 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 11 Aug 2022 18:20:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 11 Aug 2022 18:20:28 GMT
EXPOSE 3333
# Thu, 11 Aug 2022 18:20:28 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 11 Aug 2022 18:20:28 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 11 Aug 2022 18:20:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 11 Aug 2022 18:20:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d156f1e73a5c09ea7d595552f2886c32e46f8b9da1f7aa8637bedabca35b3c`  
		Last Modified: Tue, 09 Aug 2022 18:36:58 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57ccd21dcf7fc4a0b414bb17cdea42bfce6902ff9a7a98d94e67738bec46e0`  
		Last Modified: Tue, 09 Aug 2022 18:36:56 GMT  
		Size: 10.9 KB (10918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf7f0646fedf1539fbc291c21fd990c5d286f406bd9340846de181384ab68a2`  
		Last Modified: Tue, 09 Aug 2022 18:36:56 GMT  
		Size: 2.8 MB (2757888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b642e6e4779584f77f712c6ce3b67feaf58462cd78bbb9790ae8c95c8b144a13`  
		Last Modified: Thu, 11 Aug 2022 18:20:40 GMT  
		Size: 2.6 MB (2606968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ae6d28c1594d3c233b9b4c5a08fb052a45efa8fedecedaddf1b858f05e0b9c`  
		Last Modified: Thu, 11 Aug 2022 18:20:40 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e086a4b671dd33a66d9f7ab92fc6aa6ee7331b6d7bf23df137fc744f259370`  
		Last Modified: Thu, 11 Aug 2022 18:20:40 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d4fabdb3e976aa66622e3304ba3e45201849cb039c9aadc5be30a1a40f822eff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7924541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07ae53f2697dbd7bd75df44c817e148c7c37de3a457c5da742f1f94fa0cb73a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:07:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:07:40 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:07:42 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 06 Oct 2022 20:07:44 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 06 Oct 2022 20:08:49 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3.tar.gz.asc eggdrop-1.9.3.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3.tar.gz.asc   && tar -zxvf eggdrop-1.9.3.tar.gz   && rm eggdrop-1.9.3.tar.gz   && ( cd eggdrop-1.9.3     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 06 Oct 2022 20:08:49 GMT
ENV NICK=
# Thu, 06 Oct 2022 20:08:50 GMT
ENV SERVER=
# Thu, 06 Oct 2022 20:08:50 GMT
ENV LISTEN=3333
# Thu, 06 Oct 2022 20:08:50 GMT
ENV OWNER=
# Thu, 06 Oct 2022 20:08:50 GMT
ENV USERFILE=eggdrop.user
# Thu, 06 Oct 2022 20:08:50 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 06 Oct 2022 20:08:50 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 06 Oct 2022 20:08:50 GMT
EXPOSE 3333
# Thu, 06 Oct 2022 20:08:51 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 06 Oct 2022 20:08:51 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 06 Oct 2022 20:08:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 06 Oct 2022 20:08:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e522f2ab682b3bbcaf5b0ffe381c2b022a524480aa4784d881ab3d9cd52996`  
		Last Modified: Thu, 06 Oct 2022 20:09:37 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64737932742df1c344b9efb4586bf884743317b594c35c30019d111d7d042cb4`  
		Last Modified: Thu, 06 Oct 2022 20:09:35 GMT  
		Size: 10.6 KB (10602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d45b29c260fc6da08182aa8e5f2074252c460a7389e49ee0d2438285a0ba3c`  
		Last Modified: Thu, 06 Oct 2022 20:09:36 GMT  
		Size: 2.7 MB (2679942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de07fbfe2f3a15e71977f870cf5b35010ff2e88230757f61b66e377cc4b0203d`  
		Last Modified: Thu, 06 Oct 2022 20:09:36 GMT  
		Size: 2.6 MB (2616220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7392333083693a6f52b4b97fb61fdabc59695f9315697282f33f88d40b5bb324`  
		Last Modified: Thu, 06 Oct 2022 20:09:35 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dace29cedee18da0ce71636558a089f32ae57a7208f6f18d4b250bd30c2a56`  
		Last Modified: Thu, 06 Oct 2022 20:09:35 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:9318f18ed8a4ee8aa6ef1f06df5d5955dd3e4f4af614b4ec50ff11d7f722c5bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8132046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a3677760db85cafb703d323e9c38547a8845f91bde110a912806c557ccb4f9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:00 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:15:01 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:15:02 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 06 Oct 2022 20:15:04 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 06 Oct 2022 20:16:12 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3.tar.gz.asc eggdrop-1.9.3.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3.tar.gz.asc   && tar -zxvf eggdrop-1.9.3.tar.gz   && rm eggdrop-1.9.3.tar.gz   && ( cd eggdrop-1.9.3     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 06 Oct 2022 20:16:13 GMT
ENV NICK=
# Thu, 06 Oct 2022 20:16:14 GMT
ENV SERVER=
# Thu, 06 Oct 2022 20:16:15 GMT
ENV LISTEN=3333
# Thu, 06 Oct 2022 20:16:16 GMT
ENV OWNER=
# Thu, 06 Oct 2022 20:16:17 GMT
ENV USERFILE=eggdrop.user
# Thu, 06 Oct 2022 20:16:18 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 06 Oct 2022 20:16:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 06 Oct 2022 20:16:20 GMT
EXPOSE 3333
# Thu, 06 Oct 2022 20:16:22 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 06 Oct 2022 20:16:23 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 06 Oct 2022 20:16:23 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 06 Oct 2022 20:16:24 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efee3d631e04e4eab9c66de7d4c47b64f9cef29853541f1f5620115a0f561f78`  
		Last Modified: Thu, 06 Oct 2022 20:17:10 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8b617f3b978f5b945dcb21e77de70179052e253c97717beb004ee86406326e`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 10.6 KB (10630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf73d74d35365f0fa2022e278a33c69c1fb460936f26633106cfc5085d782b8f`  
		Last Modified: Thu, 06 Oct 2022 20:17:09 GMT  
		Size: 2.8 MB (2775939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc343a563af9c69340a6790f1b98333d9efb49be616a4ce377c6d19a31e4d03`  
		Last Modified: Thu, 06 Oct 2022 20:17:09 GMT  
		Size: 2.6 MB (2634027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a6420fbed1f37070ece7b3553f835f9264720866bd2e02d958a6b1739b418a`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d679e4bfbe94b527b4910ade655d2d46ac7ace8ced5e81676c349e7d5a025c1`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.3`

```console
$ docker pull eggdrop@sha256:51b72394950be4f5f8ff1cf27c7d85dae09e6fe0de081cdbee423daab4b2baf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:1.9.3` - linux; amd64

```console
$ docker pull eggdrop@sha256:e4d91474210dd34a83e1b0b2ac471a84976d9a561810352f0274534afdc674de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8185645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e242b5d3f669db45a6704607e67e8f090ddcaf9db6695faad34ef83b5c8d719c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:35:06 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:35:07 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:35:08 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:35:09 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 11 Aug 2022 18:20:27 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3.tar.gz.asc eggdrop-1.9.3.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3.tar.gz.asc   && tar -zxvf eggdrop-1.9.3.tar.gz   && rm eggdrop-1.9.3.tar.gz   && ( cd eggdrop-1.9.3     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 11 Aug 2022 18:20:27 GMT
ENV NICK=
# Thu, 11 Aug 2022 18:20:27 GMT
ENV SERVER=
# Thu, 11 Aug 2022 18:20:27 GMT
ENV LISTEN=3333
# Thu, 11 Aug 2022 18:20:27 GMT
ENV OWNER=
# Thu, 11 Aug 2022 18:20:28 GMT
ENV USERFILE=eggdrop.user
# Thu, 11 Aug 2022 18:20:28 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 11 Aug 2022 18:20:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 11 Aug 2022 18:20:28 GMT
EXPOSE 3333
# Thu, 11 Aug 2022 18:20:28 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 11 Aug 2022 18:20:28 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 11 Aug 2022 18:20:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 11 Aug 2022 18:20:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d156f1e73a5c09ea7d595552f2886c32e46f8b9da1f7aa8637bedabca35b3c`  
		Last Modified: Tue, 09 Aug 2022 18:36:58 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57ccd21dcf7fc4a0b414bb17cdea42bfce6902ff9a7a98d94e67738bec46e0`  
		Last Modified: Tue, 09 Aug 2022 18:36:56 GMT  
		Size: 10.9 KB (10918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf7f0646fedf1539fbc291c21fd990c5d286f406bd9340846de181384ab68a2`  
		Last Modified: Tue, 09 Aug 2022 18:36:56 GMT  
		Size: 2.8 MB (2757888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b642e6e4779584f77f712c6ce3b67feaf58462cd78bbb9790ae8c95c8b144a13`  
		Last Modified: Thu, 11 Aug 2022 18:20:40 GMT  
		Size: 2.6 MB (2606968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ae6d28c1594d3c233b9b4c5a08fb052a45efa8fedecedaddf1b858f05e0b9c`  
		Last Modified: Thu, 11 Aug 2022 18:20:40 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e086a4b671dd33a66d9f7ab92fc6aa6ee7331b6d7bf23df137fc744f259370`  
		Last Modified: Thu, 11 Aug 2022 18:20:40 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.3` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d4fabdb3e976aa66622e3304ba3e45201849cb039c9aadc5be30a1a40f822eff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7924541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07ae53f2697dbd7bd75df44c817e148c7c37de3a457c5da742f1f94fa0cb73a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:07:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:07:40 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:07:42 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 06 Oct 2022 20:07:44 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 06 Oct 2022 20:08:49 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3.tar.gz.asc eggdrop-1.9.3.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3.tar.gz.asc   && tar -zxvf eggdrop-1.9.3.tar.gz   && rm eggdrop-1.9.3.tar.gz   && ( cd eggdrop-1.9.3     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 06 Oct 2022 20:08:49 GMT
ENV NICK=
# Thu, 06 Oct 2022 20:08:50 GMT
ENV SERVER=
# Thu, 06 Oct 2022 20:08:50 GMT
ENV LISTEN=3333
# Thu, 06 Oct 2022 20:08:50 GMT
ENV OWNER=
# Thu, 06 Oct 2022 20:08:50 GMT
ENV USERFILE=eggdrop.user
# Thu, 06 Oct 2022 20:08:50 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 06 Oct 2022 20:08:50 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 06 Oct 2022 20:08:50 GMT
EXPOSE 3333
# Thu, 06 Oct 2022 20:08:51 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 06 Oct 2022 20:08:51 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 06 Oct 2022 20:08:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 06 Oct 2022 20:08:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e522f2ab682b3bbcaf5b0ffe381c2b022a524480aa4784d881ab3d9cd52996`  
		Last Modified: Thu, 06 Oct 2022 20:09:37 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64737932742df1c344b9efb4586bf884743317b594c35c30019d111d7d042cb4`  
		Last Modified: Thu, 06 Oct 2022 20:09:35 GMT  
		Size: 10.6 KB (10602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d45b29c260fc6da08182aa8e5f2074252c460a7389e49ee0d2438285a0ba3c`  
		Last Modified: Thu, 06 Oct 2022 20:09:36 GMT  
		Size: 2.7 MB (2679942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de07fbfe2f3a15e71977f870cf5b35010ff2e88230757f61b66e377cc4b0203d`  
		Last Modified: Thu, 06 Oct 2022 20:09:36 GMT  
		Size: 2.6 MB (2616220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7392333083693a6f52b4b97fb61fdabc59695f9315697282f33f88d40b5bb324`  
		Last Modified: Thu, 06 Oct 2022 20:09:35 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dace29cedee18da0ce71636558a089f32ae57a7208f6f18d4b250bd30c2a56`  
		Last Modified: Thu, 06 Oct 2022 20:09:35 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:1.9.3` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:9318f18ed8a4ee8aa6ef1f06df5d5955dd3e4f4af614b4ec50ff11d7f722c5bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8132046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a3677760db85cafb703d323e9c38547a8845f91bde110a912806c557ccb4f9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:00 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:15:01 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:15:02 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 06 Oct 2022 20:15:04 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 06 Oct 2022 20:16:12 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3.tar.gz.asc eggdrop-1.9.3.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3.tar.gz.asc   && tar -zxvf eggdrop-1.9.3.tar.gz   && rm eggdrop-1.9.3.tar.gz   && ( cd eggdrop-1.9.3     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 06 Oct 2022 20:16:13 GMT
ENV NICK=
# Thu, 06 Oct 2022 20:16:14 GMT
ENV SERVER=
# Thu, 06 Oct 2022 20:16:15 GMT
ENV LISTEN=3333
# Thu, 06 Oct 2022 20:16:16 GMT
ENV OWNER=
# Thu, 06 Oct 2022 20:16:17 GMT
ENV USERFILE=eggdrop.user
# Thu, 06 Oct 2022 20:16:18 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 06 Oct 2022 20:16:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 06 Oct 2022 20:16:20 GMT
EXPOSE 3333
# Thu, 06 Oct 2022 20:16:22 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 06 Oct 2022 20:16:23 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 06 Oct 2022 20:16:23 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 06 Oct 2022 20:16:24 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efee3d631e04e4eab9c66de7d4c47b64f9cef29853541f1f5620115a0f561f78`  
		Last Modified: Thu, 06 Oct 2022 20:17:10 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8b617f3b978f5b945dcb21e77de70179052e253c97717beb004ee86406326e`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 10.6 KB (10630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf73d74d35365f0fa2022e278a33c69c1fb460936f26633106cfc5085d782b8f`  
		Last Modified: Thu, 06 Oct 2022 20:17:09 GMT  
		Size: 2.8 MB (2775939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc343a563af9c69340a6790f1b98333d9efb49be616a4ce377c6d19a31e4d03`  
		Last Modified: Thu, 06 Oct 2022 20:17:09 GMT  
		Size: 2.6 MB (2634027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a6420fbed1f37070ece7b3553f835f9264720866bd2e02d958a6b1739b418a`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d679e4bfbe94b527b4910ade655d2d46ac7ace8ced5e81676c349e7d5a025c1`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:b4f8731caaff74e431578c555b9ade522cf1b36651a5b759e258c8f4a6a740ef
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
$ docker pull eggdrop@sha256:56d92d7d1b3fb19da36e36a0c6ecb10e9f82841988d391b219f2062074c16ee5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 MB (39089475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14abf1fb3ac41c0aa0f75edb489f24709b9b3b72cd93a7e86a1f8f1d0c60b3a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:03:00 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:03:00 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:03:01 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 06 Oct 2022 20:03:02 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Thu, 06 Oct 2022 20:03:02 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Thu, 06 Oct 2022 20:03:03 GMT
RUN apk --update add --no-cache bash openssl
# Thu, 06 Oct 2022 20:07:22 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 06 Oct 2022 20:07:22 GMT
ENV NICK=
# Thu, 06 Oct 2022 20:07:22 GMT
ENV SERVER=
# Thu, 06 Oct 2022 20:07:22 GMT
ENV LISTEN=3333
# Thu, 06 Oct 2022 20:07:22 GMT
ENV OWNER=
# Thu, 06 Oct 2022 20:07:23 GMT
ENV USERFILE=eggdrop.user
# Thu, 06 Oct 2022 20:07:23 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 06 Oct 2022 20:07:23 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 06 Oct 2022 20:07:23 GMT
EXPOSE 3333
# Thu, 06 Oct 2022 20:07:23 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Thu, 06 Oct 2022 20:07:23 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 06 Oct 2022 20:07:23 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 06 Oct 2022 20:07:23 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26b6e2ab9ed4e4939d215dc6c3a329a190b6bf7a1050fc2024e0308a06a3973`  
		Last Modified: Thu, 06 Oct 2022 20:09:21 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a90839ec2ad222a22d0f9266a297ee245744be011bac966e48c813c6b6382a`  
		Last Modified: Thu, 06 Oct 2022 20:09:19 GMT  
		Size: 10.7 KB (10655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1945403abbd221018a4262a7bf5c3b8293f43ab856e8d6866225d4b6e0e6c5`  
		Last Modified: Thu, 06 Oct 2022 20:09:20 GMT  
		Size: 1.0 MB (1032562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f17059a2c6014977c812871493885f8e770eb0f47d9a4db96ef62c2387171c`  
		Last Modified: Thu, 06 Oct 2022 20:09:27 GMT  
		Size: 35.4 MB (35411278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3927f9b97979f383b7066540afeea1bd7ee3260578222c0e53586ef2330de97c`  
		Last Modified: Thu, 06 Oct 2022 20:09:19 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a420f0b5e336bb077b3a6a10d1d1fb836736bb865456b41069e459ce07592b`  
		Last Modified: Thu, 06 Oct 2022 20:09:19 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2f4f47fb5fb7d10a35c1aa6328abe42690cbc858fa37c05b0a832413a55dbd4e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.8 MB (39757335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a75ff50f216be7e43914539a9ea25d0f596f427bc8ad65662211665fb38e75e`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:09:47 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:09:48 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:09:49 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 06 Oct 2022 20:09:50 GMT
ENV EGGDROP_SHA256=34915a9bf1870bb3759c68520df62443ba45e01558a53c991d2fb03db9b4ec72
# Thu, 06 Oct 2022 20:09:51 GMT
ENV EGGDROP_COMMIT=47962f7f15a1840b3f3c9ad1a6c247647d16de56
# Thu, 06 Oct 2022 20:09:52 GMT
RUN apk --update add --no-cache bash openssl
# Thu, 06 Oct 2022 20:14:31 GMT
RUN apk --update add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 06 Oct 2022 20:14:31 GMT
ENV NICK=
# Thu, 06 Oct 2022 20:14:32 GMT
ENV SERVER=
# Thu, 06 Oct 2022 20:14:33 GMT
ENV LISTEN=3333
# Thu, 06 Oct 2022 20:14:34 GMT
ENV OWNER=
# Thu, 06 Oct 2022 20:14:35 GMT
ENV USERFILE=eggdrop.user
# Thu, 06 Oct 2022 20:14:36 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 06 Oct 2022 20:14:37 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 06 Oct 2022 20:14:38 GMT
EXPOSE 3333
# Thu, 06 Oct 2022 20:14:40 GMT
COPY file:adf94c8c97044786e05e265ac7a3db4da2f14483f49d1d5b4e825de9c263b6f7 in /home/eggdrop/eggdrop 
# Thu, 06 Oct 2022 20:14:41 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 06 Oct 2022 20:14:41 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 06 Oct 2022 20:14:42 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ae7c1c7a9cf57ec4ef5bc0d760e018a0311f072731e1e901545c9782fd65c8`  
		Last Modified: Thu, 06 Oct 2022 20:16:57 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b485351e4651f72208d60653a9cb6c36bb54c79f68b2425fb5a56abb2841ded3`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87ea7cd947be80731b8ff53dd407cde03c2cd85241c969335c1daf35ad11612`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 1.1 MB (1087561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820c7adbda228ebb750dd06ea1218347eb8ae7b23508e6e321a7acbe411493a7`  
		Last Modified: Thu, 06 Oct 2022 20:17:00 GMT  
		Size: 35.9 MB (35936831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea50726c4310e7b95883f40ab4219d7a46d83f5cab0ee0225e591d207709d83`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225cbb6c09999045b9e86ec94dedb3192bed5f338120ee7b752a73a6e0df34fe`  
		Last Modified: Thu, 06 Oct 2022 20:16:55 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:51b72394950be4f5f8ff1cf27c7d85dae09e6fe0de081cdbee423daab4b2baf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:e4d91474210dd34a83e1b0b2ac471a84976d9a561810352f0274534afdc674de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8185645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e242b5d3f669db45a6704607e67e8f090ddcaf9db6695faad34ef83b5c8d719c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:35:06 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:35:07 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:35:08 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:35:09 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 11 Aug 2022 18:20:27 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3.tar.gz.asc eggdrop-1.9.3.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3.tar.gz.asc   && tar -zxvf eggdrop-1.9.3.tar.gz   && rm eggdrop-1.9.3.tar.gz   && ( cd eggdrop-1.9.3     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 11 Aug 2022 18:20:27 GMT
ENV NICK=
# Thu, 11 Aug 2022 18:20:27 GMT
ENV SERVER=
# Thu, 11 Aug 2022 18:20:27 GMT
ENV LISTEN=3333
# Thu, 11 Aug 2022 18:20:27 GMT
ENV OWNER=
# Thu, 11 Aug 2022 18:20:28 GMT
ENV USERFILE=eggdrop.user
# Thu, 11 Aug 2022 18:20:28 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 11 Aug 2022 18:20:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 11 Aug 2022 18:20:28 GMT
EXPOSE 3333
# Thu, 11 Aug 2022 18:20:28 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 11 Aug 2022 18:20:28 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 11 Aug 2022 18:20:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 11 Aug 2022 18:20:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d156f1e73a5c09ea7d595552f2886c32e46f8b9da1f7aa8637bedabca35b3c`  
		Last Modified: Tue, 09 Aug 2022 18:36:58 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57ccd21dcf7fc4a0b414bb17cdea42bfce6902ff9a7a98d94e67738bec46e0`  
		Last Modified: Tue, 09 Aug 2022 18:36:56 GMT  
		Size: 10.9 KB (10918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf7f0646fedf1539fbc291c21fd990c5d286f406bd9340846de181384ab68a2`  
		Last Modified: Tue, 09 Aug 2022 18:36:56 GMT  
		Size: 2.8 MB (2757888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b642e6e4779584f77f712c6ce3b67feaf58462cd78bbb9790ae8c95c8b144a13`  
		Last Modified: Thu, 11 Aug 2022 18:20:40 GMT  
		Size: 2.6 MB (2606968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ae6d28c1594d3c233b9b4c5a08fb052a45efa8fedecedaddf1b858f05e0b9c`  
		Last Modified: Thu, 11 Aug 2022 18:20:40 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e086a4b671dd33a66d9f7ab92fc6aa6ee7331b6d7bf23df137fc744f259370`  
		Last Modified: Thu, 11 Aug 2022 18:20:40 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d4fabdb3e976aa66622e3304ba3e45201849cb039c9aadc5be30a1a40f822eff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7924541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07ae53f2697dbd7bd75df44c817e148c7c37de3a457c5da742f1f94fa0cb73a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:07:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:07:40 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:07:42 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 06 Oct 2022 20:07:44 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 06 Oct 2022 20:08:49 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3.tar.gz.asc eggdrop-1.9.3.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3.tar.gz.asc   && tar -zxvf eggdrop-1.9.3.tar.gz   && rm eggdrop-1.9.3.tar.gz   && ( cd eggdrop-1.9.3     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 06 Oct 2022 20:08:49 GMT
ENV NICK=
# Thu, 06 Oct 2022 20:08:50 GMT
ENV SERVER=
# Thu, 06 Oct 2022 20:08:50 GMT
ENV LISTEN=3333
# Thu, 06 Oct 2022 20:08:50 GMT
ENV OWNER=
# Thu, 06 Oct 2022 20:08:50 GMT
ENV USERFILE=eggdrop.user
# Thu, 06 Oct 2022 20:08:50 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 06 Oct 2022 20:08:50 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 06 Oct 2022 20:08:50 GMT
EXPOSE 3333
# Thu, 06 Oct 2022 20:08:51 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 06 Oct 2022 20:08:51 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 06 Oct 2022 20:08:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 06 Oct 2022 20:08:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e522f2ab682b3bbcaf5b0ffe381c2b022a524480aa4784d881ab3d9cd52996`  
		Last Modified: Thu, 06 Oct 2022 20:09:37 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64737932742df1c344b9efb4586bf884743317b594c35c30019d111d7d042cb4`  
		Last Modified: Thu, 06 Oct 2022 20:09:35 GMT  
		Size: 10.6 KB (10602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d45b29c260fc6da08182aa8e5f2074252c460a7389e49ee0d2438285a0ba3c`  
		Last Modified: Thu, 06 Oct 2022 20:09:36 GMT  
		Size: 2.7 MB (2679942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de07fbfe2f3a15e71977f870cf5b35010ff2e88230757f61b66e377cc4b0203d`  
		Last Modified: Thu, 06 Oct 2022 20:09:36 GMT  
		Size: 2.6 MB (2616220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7392333083693a6f52b4b97fb61fdabc59695f9315697282f33f88d40b5bb324`  
		Last Modified: Thu, 06 Oct 2022 20:09:35 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dace29cedee18da0ce71636558a089f32ae57a7208f6f18d4b250bd30c2a56`  
		Last Modified: Thu, 06 Oct 2022 20:09:35 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:9318f18ed8a4ee8aa6ef1f06df5d5955dd3e4f4af614b4ec50ff11d7f722c5bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8132046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a3677760db85cafb703d323e9c38547a8845f91bde110a912806c557ccb4f9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:00 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:15:01 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:15:02 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 06 Oct 2022 20:15:04 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 06 Oct 2022 20:16:12 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3.tar.gz.asc eggdrop-1.9.3.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3.tar.gz.asc   && tar -zxvf eggdrop-1.9.3.tar.gz   && rm eggdrop-1.9.3.tar.gz   && ( cd eggdrop-1.9.3     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 06 Oct 2022 20:16:13 GMT
ENV NICK=
# Thu, 06 Oct 2022 20:16:14 GMT
ENV SERVER=
# Thu, 06 Oct 2022 20:16:15 GMT
ENV LISTEN=3333
# Thu, 06 Oct 2022 20:16:16 GMT
ENV OWNER=
# Thu, 06 Oct 2022 20:16:17 GMT
ENV USERFILE=eggdrop.user
# Thu, 06 Oct 2022 20:16:18 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 06 Oct 2022 20:16:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 06 Oct 2022 20:16:20 GMT
EXPOSE 3333
# Thu, 06 Oct 2022 20:16:22 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 06 Oct 2022 20:16:23 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 06 Oct 2022 20:16:23 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 06 Oct 2022 20:16:24 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efee3d631e04e4eab9c66de7d4c47b64f9cef29853541f1f5620115a0f561f78`  
		Last Modified: Thu, 06 Oct 2022 20:17:10 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8b617f3b978f5b945dcb21e77de70179052e253c97717beb004ee86406326e`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 10.6 KB (10630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf73d74d35365f0fa2022e278a33c69c1fb460936f26633106cfc5085d782b8f`  
		Last Modified: Thu, 06 Oct 2022 20:17:09 GMT  
		Size: 2.8 MB (2775939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc343a563af9c69340a6790f1b98333d9efb49be616a4ce377c6d19a31e4d03`  
		Last Modified: Thu, 06 Oct 2022 20:17:09 GMT  
		Size: 2.6 MB (2634027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a6420fbed1f37070ece7b3553f835f9264720866bd2e02d958a6b1739b418a`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d679e4bfbe94b527b4910ade655d2d46ac7ace8ced5e81676c349e7d5a025c1`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:51b72394950be4f5f8ff1cf27c7d85dae09e6fe0de081cdbee423daab4b2baf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:e4d91474210dd34a83e1b0b2ac471a84976d9a561810352f0274534afdc674de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8185645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e242b5d3f669db45a6704607e67e8f090ddcaf9db6695faad34ef83b5c8d719c`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:35:06 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:35:07 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:35:08 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:35:09 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 11 Aug 2022 18:20:27 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3.tar.gz.asc eggdrop-1.9.3.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3.tar.gz.asc   && tar -zxvf eggdrop-1.9.3.tar.gz   && rm eggdrop-1.9.3.tar.gz   && ( cd eggdrop-1.9.3     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 11 Aug 2022 18:20:27 GMT
ENV NICK=
# Thu, 11 Aug 2022 18:20:27 GMT
ENV SERVER=
# Thu, 11 Aug 2022 18:20:27 GMT
ENV LISTEN=3333
# Thu, 11 Aug 2022 18:20:27 GMT
ENV OWNER=
# Thu, 11 Aug 2022 18:20:28 GMT
ENV USERFILE=eggdrop.user
# Thu, 11 Aug 2022 18:20:28 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 11 Aug 2022 18:20:28 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 11 Aug 2022 18:20:28 GMT
EXPOSE 3333
# Thu, 11 Aug 2022 18:20:28 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 11 Aug 2022 18:20:28 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 11 Aug 2022 18:20:28 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 11 Aug 2022 18:20:28 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d156f1e73a5c09ea7d595552f2886c32e46f8b9da1f7aa8637bedabca35b3c`  
		Last Modified: Tue, 09 Aug 2022 18:36:58 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57ccd21dcf7fc4a0b414bb17cdea42bfce6902ff9a7a98d94e67738bec46e0`  
		Last Modified: Tue, 09 Aug 2022 18:36:56 GMT  
		Size: 10.9 KB (10918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf7f0646fedf1539fbc291c21fd990c5d286f406bd9340846de181384ab68a2`  
		Last Modified: Tue, 09 Aug 2022 18:36:56 GMT  
		Size: 2.8 MB (2757888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b642e6e4779584f77f712c6ce3b67feaf58462cd78bbb9790ae8c95c8b144a13`  
		Last Modified: Thu, 11 Aug 2022 18:20:40 GMT  
		Size: 2.6 MB (2606968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ae6d28c1594d3c233b9b4c5a08fb052a45efa8fedecedaddf1b858f05e0b9c`  
		Last Modified: Thu, 11 Aug 2022 18:20:40 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e086a4b671dd33a66d9f7ab92fc6aa6ee7331b6d7bf23df137fc744f259370`  
		Last Modified: Thu, 11 Aug 2022 18:20:40 GMT  
		Size: 702.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:d4fabdb3e976aa66622e3304ba3e45201849cb039c9aadc5be30a1a40f822eff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7924541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07ae53f2697dbd7bd75df44c817e148c7c37de3a457c5da742f1f94fa0cb73a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:07:40 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:07:40 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:07:42 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 06 Oct 2022 20:07:44 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 06 Oct 2022 20:08:49 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3.tar.gz.asc eggdrop-1.9.3.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3.tar.gz.asc   && tar -zxvf eggdrop-1.9.3.tar.gz   && rm eggdrop-1.9.3.tar.gz   && ( cd eggdrop-1.9.3     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 06 Oct 2022 20:08:49 GMT
ENV NICK=
# Thu, 06 Oct 2022 20:08:50 GMT
ENV SERVER=
# Thu, 06 Oct 2022 20:08:50 GMT
ENV LISTEN=3333
# Thu, 06 Oct 2022 20:08:50 GMT
ENV OWNER=
# Thu, 06 Oct 2022 20:08:50 GMT
ENV USERFILE=eggdrop.user
# Thu, 06 Oct 2022 20:08:50 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 06 Oct 2022 20:08:50 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 06 Oct 2022 20:08:50 GMT
EXPOSE 3333
# Thu, 06 Oct 2022 20:08:51 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 06 Oct 2022 20:08:51 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 06 Oct 2022 20:08:51 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 06 Oct 2022 20:08:51 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e522f2ab682b3bbcaf5b0ffe381c2b022a524480aa4784d881ab3d9cd52996`  
		Last Modified: Thu, 06 Oct 2022 20:09:37 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64737932742df1c344b9efb4586bf884743317b594c35c30019d111d7d042cb4`  
		Last Modified: Thu, 06 Oct 2022 20:09:35 GMT  
		Size: 10.6 KB (10602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d45b29c260fc6da08182aa8e5f2074252c460a7389e49ee0d2438285a0ba3c`  
		Last Modified: Thu, 06 Oct 2022 20:09:36 GMT  
		Size: 2.7 MB (2679942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de07fbfe2f3a15e71977f870cf5b35010ff2e88230757f61b66e377cc4b0203d`  
		Last Modified: Thu, 06 Oct 2022 20:09:36 GMT  
		Size: 2.6 MB (2616220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7392333083693a6f52b4b97fb61fdabc59695f9315697282f33f88d40b5bb324`  
		Last Modified: Thu, 06 Oct 2022 20:09:35 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62dace29cedee18da0ce71636558a089f32ae57a7208f6f18d4b250bd30c2a56`  
		Last Modified: Thu, 06 Oct 2022 20:09:35 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:9318f18ed8a4ee8aa6ef1f06df5d5955dd3e4f4af614b4ec50ff11d7f722c5bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8132046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a3677760db85cafb703d323e9c38547a8845f91bde110a912806c557ccb4f9`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 20:15:00 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 06 Oct 2022 20:15:01 GMT
RUN adduser -S eggdrop
# Thu, 06 Oct 2022 20:15:02 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 06 Oct 2022 20:15:04 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 06 Oct 2022 20:16:12 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gnupg build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.3.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.3.tar.gz.asc eggdrop-1.9.3.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.3.tar.gz.asc   && tar -zxvf eggdrop-1.9.3.tar.gz   && rm eggdrop-1.9.3.tar.gz   && ( cd eggdrop-1.9.3     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.3   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 06 Oct 2022 20:16:13 GMT
ENV NICK=
# Thu, 06 Oct 2022 20:16:14 GMT
ENV SERVER=
# Thu, 06 Oct 2022 20:16:15 GMT
ENV LISTEN=3333
# Thu, 06 Oct 2022 20:16:16 GMT
ENV OWNER=
# Thu, 06 Oct 2022 20:16:17 GMT
ENV USERFILE=eggdrop.user
# Thu, 06 Oct 2022 20:16:18 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 06 Oct 2022 20:16:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 06 Oct 2022 20:16:20 GMT
EXPOSE 3333
# Thu, 06 Oct 2022 20:16:22 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 06 Oct 2022 20:16:23 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 06 Oct 2022 20:16:23 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 06 Oct 2022 20:16:24 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efee3d631e04e4eab9c66de7d4c47b64f9cef29853541f1f5620115a0f561f78`  
		Last Modified: Thu, 06 Oct 2022 20:17:10 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8b617f3b978f5b945dcb21e77de70179052e253c97717beb004ee86406326e`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 10.6 KB (10630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf73d74d35365f0fa2022e278a33c69c1fb460936f26633106cfc5085d782b8f`  
		Last Modified: Thu, 06 Oct 2022 20:17:09 GMT  
		Size: 2.8 MB (2775939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc343a563af9c69340a6790f1b98333d9efb49be616a4ce377c6d19a31e4d03`  
		Last Modified: Thu, 06 Oct 2022 20:17:09 GMT  
		Size: 2.6 MB (2634027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a6420fbed1f37070ece7b3553f835f9264720866bd2e02d958a6b1739b418a`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d679e4bfbe94b527b4910ade655d2d46ac7ace8ced5e81676c349e7d5a025c1`  
		Last Modified: Thu, 06 Oct 2022 20:17:08 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
