## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:2bc0c3cea857f5dfcc25291376e061b033358062d9f8b044c1ba87cad5fe50f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:7c1f07fb2993db2d23c2e3a8e823129712498b74c5e45e56f55b7404c92e592f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8300472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce82528bfca421aca6084f8346db146a3916779e591d66c47ae07885ca8e46d6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:14 GMT
ADD file:7fd90c097e2c4587dee91726d71abc02fa1aa6a3a3395c862206a4e14e0c299c in / 
# Tue, 09 Aug 2022 17:20:14 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:33:57 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:33:58 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:33:59 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:34:00 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 09 Aug 2022 18:34:52 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:34:53 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:34:53 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:34:53 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:34:53 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:34:53 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:34:53 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:34:53 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:34:54 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:34:54 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:34:54 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:72cfd02ff4d01b1f319eed108b53120dea0185b916d2abeb4e6121879cbf7a65`  
		Last Modified: Tue, 09 Aug 2022 17:21:16 GMT  
		Size: 2.8 MB (2827571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c64dbfdb30e6f2bd91f9d7ba689f3dd89f62125a424c3c17fcee5620b2020a3`  
		Last Modified: Tue, 09 Aug 2022 18:36:41 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d40371db7868456b4ab64cfe248665bd0667efb13b1d7f88c53d2c2b119809`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 10.7 KB (10692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6657ec397289e21433c76381c67362a8917b0a8a27d3fed327a468a29c51d1c`  
		Last Modified: Tue, 09 Aug 2022 18:36:39 GMT  
		Size: 2.7 MB (2726758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a22238d642dd432a127e2b9748eca1a5c7257af11d7e79d3ab7fcff4d7ae94d`  
		Last Modified: Tue, 09 Aug 2022 18:36:40 GMT  
		Size: 2.7 MB (2731661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23a4112d585d674763eebdc058f2e3c60c68d8ae5d07c49b0b2c83965298a4`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f38d0f5cf90ae3f376a3e1abb98ea29aed2da199c6fd97b39df16deb70fc968`  
		Last Modified: Tue, 09 Aug 2022 18:36:38 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:e37161cd4b8b5bed14a49cfdad3e2a9c48b7313e94c982463c045ad10aca8c31
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc95519b4a1c840f914d74fc894264484613be3a619f55381b34c446cafd39c0`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:40 GMT
ADD file:541b767b21b9e0c4dab118d5e000990da3dbb81b547c1ee9941e2cf7edc5edd6 in / 
# Tue, 09 Aug 2022 17:49:40 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:51:03 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Tue, 09 Aug 2022 18:51:03 GMT
RUN adduser -S eggdrop
# Tue, 09 Aug 2022 18:51:05 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 09 Aug 2022 18:51:06 GMT
RUN apk add --no-cache tcl bash openssl
# Tue, 09 Aug 2022 18:52:08 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Tue, 09 Aug 2022 18:52:08 GMT
ENV NICK=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV SERVER=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV LISTEN=3333
# Tue, 09 Aug 2022 18:52:09 GMT
ENV OWNER=
# Tue, 09 Aug 2022 18:52:09 GMT
ENV USERFILE=eggdrop.user
# Tue, 09 Aug 2022 18:52:09 GMT
ENV CHANFILE=eggdrop.chan
# Tue, 09 Aug 2022 18:52:09 GMT
WORKDIR /home/eggdrop/eggdrop
# Tue, 09 Aug 2022 18:52:09 GMT
EXPOSE 3333
# Tue, 09 Aug 2022 18:52:10 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Tue, 09 Aug 2022 18:52:10 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Tue, 09 Aug 2022 18:52:10 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Tue, 09 Aug 2022 18:52:10 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:b423ab447fbb66b194458908339addbb5dd52e4aa7d04a42b387cdc07bbd92a1`  
		Last Modified: Tue, 09 Aug 2022 17:51:16 GMT  
		Size: 2.6 MB (2633535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ab43c4ab8ce3acf894fb689d3fab3e352715d608c94c7ee0ee865b529cec6d`  
		Last Modified: Tue, 09 Aug 2022 18:54:29 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511cfb58f000c475f12763f9367d55beb8423621bb6a35bf8a7f715cd1fb1a30`  
		Last Modified: Tue, 09 Aug 2022 18:54:27 GMT  
		Size: 10.4 KB (10408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfec0ee07b8315970755477fe547e30ce338e99e7c00565c182a9ca59b5c8a8`  
		Last Modified: Tue, 09 Aug 2022 18:54:28 GMT  
		Size: 2.7 MB (2653209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfdb869195492c054c5600ff7528f0f9520281927b6ca195486d47254674c16`  
		Last Modified: Tue, 09 Aug 2022 18:54:28 GMT  
		Size: 2.7 MB (2686830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2676ad94b7d2ef8b194fb1d5a76635d4965833ee34cd876da2d48abdd5bcaa`  
		Last Modified: Tue, 09 Aug 2022 18:54:26 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f913ef8822c4a99179c9d88e1dfe63f9c4eeac5c6295fbaff2d605b4524077c0`  
		Last Modified: Tue, 09 Aug 2022 18:54:27 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:e84f7c32f517ff5fa326176eec3e8991d9f7ad57cd995146ffdedb2ced0b2e33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8214605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cd5d289cea5264914c2a7e5cf3c85ce2fcfe30ac7add56e14d5c6335169141`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Aug 2022 17:40:07 GMT
ADD file:f23c059b4312458fbf0fc018d4695f36157a3eb6e5a83167912a39f9a738f4eb in / 
# Tue, 09 Aug 2022 17:40:07 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 05:04:21 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 10 Aug 2022 05:04:21 GMT
RUN adduser -S eggdrop
# Wed, 10 Aug 2022 05:04:23 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 10 Aug 2022 05:04:24 GMT
RUN apk add --no-cache tcl bash openssl
# Wed, 10 Aug 2022 05:05:28 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.2.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.2.tar.gz.asc eggdrop-1.9.2.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.2.tar.gz.asc   && tar -zxvf eggdrop-1.9.2.tar.gz   && rm eggdrop-1.9.2.tar.gz   && ( cd eggdrop-1.9.2     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.2   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Wed, 10 Aug 2022 05:05:29 GMT
ENV NICK=
# Wed, 10 Aug 2022 05:05:30 GMT
ENV SERVER=
# Wed, 10 Aug 2022 05:05:31 GMT
ENV LISTEN=3333
# Wed, 10 Aug 2022 05:05:32 GMT
ENV OWNER=
# Wed, 10 Aug 2022 05:05:33 GMT
ENV USERFILE=eggdrop.user
# Wed, 10 Aug 2022 05:05:34 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 10 Aug 2022 05:05:35 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 10 Aug 2022 05:05:36 GMT
EXPOSE 3333
# Wed, 10 Aug 2022 05:05:38 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Wed, 10 Aug 2022 05:05:39 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Wed, 10 Aug 2022 05:05:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 10 Aug 2022 05:05:40 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:25f523f0e93b2b5fa676c15d91b90f08ee4de7a160874e6c52ea452929d5a7cc`  
		Last Modified: Tue, 09 Aug 2022 17:41:17 GMT  
		Size: 2.7 MB (2722126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d4e5c15d1b63bb42af14ab1d05e88a264191d91d568570fc217c4f41639b1d`  
		Last Modified: Wed, 10 Aug 2022 05:07:59 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b532fe332af24e16afb922b6f543ca7cbc3153b97333268f346d074928301ea8`  
		Last Modified: Wed, 10 Aug 2022 05:07:56 GMT  
		Size: 10.5 KB (10480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaba5f7182f1cf21fda5d7174b627bc3ed3d5cee7b3433a83993011f3775ba4`  
		Last Modified: Wed, 10 Aug 2022 05:07:57 GMT  
		Size: 2.8 MB (2752049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abeecfdff7817bcf92437925c707e098d03c374783e88064205c3d43c242696`  
		Last Modified: Wed, 10 Aug 2022 05:07:57 GMT  
		Size: 2.7 MB (2726176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27f771566730a5a92d3e29322c479cd5e0d467beae1053752bf284585bd9bdf`  
		Last Modified: Wed, 10 Aug 2022 05:07:56 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0cb3e4a00d0a0b267e7deec108a85a81e48e705e8f9c0125c3ca23822fbecd`  
		Last Modified: Wed, 10 Aug 2022 05:07:56 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
