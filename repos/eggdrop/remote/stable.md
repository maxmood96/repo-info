## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:007d34d1b35694197b76d8a75df2e83fc01d28e2eb3ada236017c5d3f53aab79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:89053e8a7d150a1456ff6665b763fc69a606d8bc86b13690845f18a0cdc3635e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9170190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1ec9e253a6998de8999eec3ceb85219e6a8859e3c7953a7e6d5b53565c3f42`
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
# Tue, 17 Mar 2020 22:12:48 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 17 Mar 2020 22:13:42 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.4.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.4.tar.gz.asc eggdrop-1.8.4.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.8.4.tar.gz.asc   && tar -zxvf eggdrop-1.8.4.tar.gz   && rm eggdrop-1.8.4.tar.gz   && ( cd eggdrop-1.8.4     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.4   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 17 Mar 2020 22:13:42 GMT
ENV NICK=
# Tue, 17 Mar 2020 22:13:43 GMT
ENV SERVER=
# Tue, 17 Mar 2020 22:13:43 GMT
ENV LISTEN=3333
# Tue, 17 Mar 2020 22:13:43 GMT
ENV OWNER=
# Tue, 17 Mar 2020 22:13:43 GMT
ENV USERFILE=eggdrop.user
# Tue, 17 Mar 2020 22:13:43 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 17 Mar 2020 22:13:43 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 17 Mar 2020 22:13:44 GMT
EXPOSE 3333
# Tue, 17 Mar 2020 22:13:44 GMT
COPY file:f8d85155d39ecdefdd2ce710ca8c1211edaffb7c3fbbde0877da166dd3aaa579 in /home/eggdrop/eggdrop 
# Tue, 17 Mar 2020 22:13:44 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 17 Mar 2020 22:13:44 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 17 Mar 2020 22:13:44 GMT
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
	-	`sha256:af4a32147b9bd138104734517903dc5f35b1058917628022c6646e30e8368df9`  
		Last Modified: Tue, 17 Mar 2020 22:13:58 GMT  
		Size: 2.7 MB (2684265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b599b7186a029d109ba9701c0efa53ff5deec379c0ac9ea4b1ab07b64d2db6`  
		Last Modified: Tue, 17 Mar 2020 22:13:58 GMT  
		Size: 3.7 MB (3669571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f82a842b1ff9893c27c854692c241a6fa2eef94857e19b147a29aa40648a469`  
		Last Modified: Tue, 17 Mar 2020 22:13:58 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bed48c0ced303da2154f21dc3e115d32ff508ed949084e51a22017fcb81333e`  
		Last Modified: Tue, 17 Mar 2020 22:13:58 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
