<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.10`](#eggdrop110)
-	[`eggdrop:1.10.0`](#eggdrop1100)
-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.5`](#eggdrop195)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.10`

```console
$ docker pull eggdrop@sha256:1d021af09fc6b335e8ea949270cf7a54b806b5b24866d9a057c6a138f8d30f05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.10` - linux; amd64

```console
$ docker pull eggdrop@sha256:252fef8f4674db29dbef6efe0bc8fca2e8204067d25c1a566ce7fef9e6b3f011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad355cd0826d4f00e2adb90ce79426822c8976e785d4ddfb63f49ecfc4291f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218cdc53cb6ea10a45c5a146c668fbb9524c28ade07376af7b4ab701561bdd7a`  
		Last Modified: Tue, 07 Jan 2025 03:18:14 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cbc9aca64aad13c1bdab9bf8b07a57e2ae2920bcc2606f6acfdaa841243520`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 1.1 MB (1115384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4631e8311e35d39893a97f134637a19872dea48770f5ff12aa20a996957dbd7a`  
		Size: 12.7 MB (12719108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80323b392cd4ad927810eca7e0b11ec2d8dd7604b3ccf4bb12391d6b779f99f2`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1341f3e5b237d9adc22646c6ce2818d7f2e2f48557f99cfaf9d73e7737ca3b0`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:b6fe0374f54c544f69b4f8403c641737c9865517d350fd69abe178f6ff455a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 KB (157535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f745c424c568d08a21366fcb3f7a0f296ec900fc8c88e95650a3edd7c3d3e041`

```dockerfile
```

-	Layers:
	-	`sha256:881a932e81e716a7b00195e3644f8aa1233475ce9be9d65961224804668500ae`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 138.8 KB (138764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2065ff5353ade8036f62c1d02d1dffb721272a67018ded9399d8b968d27866b9`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b8d2e3cbcb9a2cb3681d6c7301de4c18586f1ba0f753cb7473192bba80ed627e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17058170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b449786e64fa60a401e21ee13f3975c91ebafedaef4c9ec82cd47366d9f0022`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87c49c56e3d5c9303824a8cad20f5b05da63b8c632ee40628c3929f67d96cac`  
		Last Modified: Tue, 07 Jan 2025 03:41:06 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff887413f70f9ad52edadcf99d87efb7034a0479a51ab3dbfce367e24df84f0`  
		Last Modified: Tue, 07 Jan 2025 03:41:07 GMT  
		Size: 1.1 MB (1129559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066a79e578efc48121cd7ecf1a2a7dab91a745976bf8a39bf1f21dab825f55dc`  
		Last Modified: Tue, 07 Jan 2025 03:49:21 GMT  
		Size: 12.6 MB (12560590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d533c9c557185da954a345b2e99603427489f36113aa72bc26005df4944f0a68`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57980c8622b60855176cf792e318d3222a64c01141570ba18004c564de38f62e`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:0f2d1d9db0a7c3019d94927700824e94d2d7ddc06f919d1868c6d811be14e4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76393351c93a2081d88863f200559b1157f34e64d61d32e2d7ea7ff594e8618`

```dockerfile
```

-	Layers:
	-	`sha256:e66653e79f8153ba3e8ae3178c5f8acac0eecb1356fb2c84bf69f152bc127452`  
		Last Modified: Tue, 07 Jan 2025 03:49:16 GMT  
		Size: 18.7 KB (18658 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:cde577b4d2f2fe326ffbf4470cc1b563354e0e17b271db25104cf2d7dc6eb176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18155441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf81282b168ce87f4b1238311649e2fffbb72e652ea2cdfc3452c81bd69eb5f7`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adba3ad06ebd31a48135af820872fd883c103f9fd47fb46b953a0d826867c58`  
		Last Modified: Tue, 07 Jan 2025 04:03:52 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6504725a30a01dfb79c3839e72991ba0790ded436ec4b8b28f5b2a462d5297`  
		Last Modified: Tue, 07 Jan 2025 04:03:53 GMT  
		Size: 1.2 MB (1210975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8924a6ff021d35b2a990093f6873fd81752352e73a34525e3745e9ee23784`  
		Last Modified: Tue, 07 Jan 2025 04:10:09 GMT  
		Size: 12.9 MB (12853706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2275c94babe8d4ae787dec6b0a0e00650296d046bb82ed20863a6a2623aaa40`  
		Last Modified: Tue, 07 Jan 2025 04:10:09 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3e1e29765384f88e226f621ccf019e19493966727c332aa83c60b8027cc412`  
		Last Modified: Tue, 07 Jan 2025 04:10:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d0b5932270e88f7434a49b3d134ca8295cb84f09a0808e45cc111941c6dbe14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 KB (157725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ba6c476080f48073c51278234586a50e88214c2bcad90d80a0c7db2148bc75`

```dockerfile
```

-	Layers:
	-	`sha256:e95d59eb7daed26d83539a3f877304467c1236a438db609726e22813e808a174`  
		Last Modified: Tue, 07 Jan 2025 04:10:08 GMT  
		Size: 138.8 KB (138820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a17090e74a6d50268d8142352a0f3c61eec903c1618e4f7a889fc6ea1fb7a4`  
		Last Modified: Tue, 07 Jan 2025 04:10:11 GMT  
		Size: 18.9 KB (18905 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.10.0`

```console
$ docker pull eggdrop@sha256:1d021af09fc6b335e8ea949270cf7a54b806b5b24866d9a057c6a138f8d30f05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.10.0` - linux; amd64

```console
$ docker pull eggdrop@sha256:252fef8f4674db29dbef6efe0bc8fca2e8204067d25c1a566ce7fef9e6b3f011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad355cd0826d4f00e2adb90ce79426822c8976e785d4ddfb63f49ecfc4291f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218cdc53cb6ea10a45c5a146c668fbb9524c28ade07376af7b4ab701561bdd7a`  
		Last Modified: Tue, 07 Jan 2025 03:18:14 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cbc9aca64aad13c1bdab9bf8b07a57e2ae2920bcc2606f6acfdaa841243520`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 1.1 MB (1115384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4631e8311e35d39893a97f134637a19872dea48770f5ff12aa20a996957dbd7a`  
		Size: 12.7 MB (12719108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80323b392cd4ad927810eca7e0b11ec2d8dd7604b3ccf4bb12391d6b779f99f2`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1341f3e5b237d9adc22646c6ce2818d7f2e2f48557f99cfaf9d73e7737ca3b0`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0` - unknown; unknown

```console
$ docker pull eggdrop@sha256:b6fe0374f54c544f69b4f8403c641737c9865517d350fd69abe178f6ff455a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 KB (157535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f745c424c568d08a21366fcb3f7a0f296ec900fc8c88e95650a3edd7c3d3e041`

```dockerfile
```

-	Layers:
	-	`sha256:881a932e81e716a7b00195e3644f8aa1233475ce9be9d65961224804668500ae`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 138.8 KB (138764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2065ff5353ade8036f62c1d02d1dffb721272a67018ded9399d8b968d27866b9`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.0` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b8d2e3cbcb9a2cb3681d6c7301de4c18586f1ba0f753cb7473192bba80ed627e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17058170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b449786e64fa60a401e21ee13f3975c91ebafedaef4c9ec82cd47366d9f0022`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87c49c56e3d5c9303824a8cad20f5b05da63b8c632ee40628c3929f67d96cac`  
		Last Modified: Tue, 07 Jan 2025 03:41:06 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff887413f70f9ad52edadcf99d87efb7034a0479a51ab3dbfce367e24df84f0`  
		Last Modified: Tue, 07 Jan 2025 03:41:07 GMT  
		Size: 1.1 MB (1129559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066a79e578efc48121cd7ecf1a2a7dab91a745976bf8a39bf1f21dab825f55dc`  
		Last Modified: Tue, 07 Jan 2025 03:49:21 GMT  
		Size: 12.6 MB (12560590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d533c9c557185da954a345b2e99603427489f36113aa72bc26005df4944f0a68`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57980c8622b60855176cf792e318d3222a64c01141570ba18004c564de38f62e`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0` - unknown; unknown

```console
$ docker pull eggdrop@sha256:0f2d1d9db0a7c3019d94927700824e94d2d7ddc06f919d1868c6d811be14e4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76393351c93a2081d88863f200559b1157f34e64d61d32e2d7ea7ff594e8618`

```dockerfile
```

-	Layers:
	-	`sha256:e66653e79f8153ba3e8ae3178c5f8acac0eecb1356fb2c84bf69f152bc127452`  
		Last Modified: Tue, 07 Jan 2025 03:49:16 GMT  
		Size: 18.7 KB (18658 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.0` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:cde577b4d2f2fe326ffbf4470cc1b563354e0e17b271db25104cf2d7dc6eb176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18155441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf81282b168ce87f4b1238311649e2fffbb72e652ea2cdfc3452c81bd69eb5f7`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adba3ad06ebd31a48135af820872fd883c103f9fd47fb46b953a0d826867c58`  
		Last Modified: Tue, 07 Jan 2025 04:03:52 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6504725a30a01dfb79c3839e72991ba0790ded436ec4b8b28f5b2a462d5297`  
		Last Modified: Tue, 07 Jan 2025 04:03:53 GMT  
		Size: 1.2 MB (1210975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8924a6ff021d35b2a990093f6873fd81752352e73a34525e3745e9ee23784`  
		Last Modified: Tue, 07 Jan 2025 04:10:09 GMT  
		Size: 12.9 MB (12853706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2275c94babe8d4ae787dec6b0a0e00650296d046bb82ed20863a6a2623aaa40`  
		Last Modified: Tue, 07 Jan 2025 04:10:09 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3e1e29765384f88e226f621ccf019e19493966727c332aa83c60b8027cc412`  
		Last Modified: Tue, 07 Jan 2025 04:10:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d0b5932270e88f7434a49b3d134ca8295cb84f09a0808e45cc111941c6dbe14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 KB (157725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ba6c476080f48073c51278234586a50e88214c2bcad90d80a0c7db2148bc75`

```dockerfile
```

-	Layers:
	-	`sha256:e95d59eb7daed26d83539a3f877304467c1236a438db609726e22813e808a174`  
		Last Modified: Tue, 07 Jan 2025 04:10:08 GMT  
		Size: 138.8 KB (138820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a17090e74a6d50268d8142352a0f3c61eec903c1618e4f7a889fc6ea1fb7a4`  
		Last Modified: Tue, 07 Jan 2025 04:10:11 GMT  
		Size: 18.9 KB (18905 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:d6c33147f2594478379e1796db38711acb81f53709f5083b9cc2c1f9676e52fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:59c8aa4db5bad5b774ed0863e793626502b1e5fb90440ca502d4a516c131450d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12267751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f616a81e004889be87bc99a41fd7cc33e4c9d9e975aa7200b47c888d173dd65`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Wed, 08 Jan 2025 03:16:29 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e73bca2ae2289fd661d1428fb61ba9b3edf24f2743f8f44542a0cbe9e633921`  
		Last Modified: Tue, 07 Jan 2025 03:17:43 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd18935c8babaee91be6909b2f200ffbc71f1dce2b726929acd549558a4085e`  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37887064c4796239f99c4ec431fc27b839b087ed3f68a61fbc95b1bb9d88399e`  
		Last Modified: Tue, 07 Jan 2025 03:17:44 GMT  
		Size: 2.9 MB (2886333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ee9624c788488d4eb6905ccb5653649601031703dc7d2f75526313b8483c93`  
		Last Modified: Tue, 07 Jan 2025 03:17:44 GMT  
		Size: 6.0 MB (5953505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170cdb6f121a3c47c7f669e9ced3b1f9be6be9ba26f33fdee48c0588a632c067`  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe806fc73442e5f2bdefc91f3cc78c0842484eb15b1671b07cc9ad4a50bb3ed`  
		Last Modified: Tue, 07 Jan 2025 03:17:44 GMT  
		Size: 698.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:0f283a8fd7c443e7e8d45672aabcd6ed44594695f8cdfc2cd050e8ffa68ce14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920c39c7459a1a6f121e00185204937cab811db13441bf52c90a66f2af1619c4`

```dockerfile
```

-	Layers:
	-	`sha256:194553012e941cbe1e3e9a15ad021f79ee4809012c7dacbd9e1d80fd608700e5`  
		Last Modified: Tue, 07 Jan 2025 03:17:43 GMT  
		Size: 1.0 MB (1043182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7336aa81ee1d931670df84a3d91831d3ea0d7b502b3c1d9cf65ce8ff67d53af0`  
		Last Modified: Tue, 07 Jan 2025 03:17:43 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:40531623d4f715000d44f2119bda5e2cafda4ffb31b79a84eb584dd24bd62120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11924036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecc6ec4fc13c3d3cbe9e3aee159ff3b1130e2a04259647d251bee556012e927`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.5-armhf.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:7ebe2b3dea80a0cf44722451c51fa37efc40b0c599e291ba324046244780a76f`  
		Last Modified: Tue, 07 Jan 2025 02:30:01 GMT  
		Size: 3.2 MB (3169627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2b8e877a15714d642264e38aec232054224f7e6ba8b0109c9e4c81a2e5bfdf`  
		Last Modified: Wed, 08 Jan 2025 02:30:17 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe273814a702499f005f595fadccf3f504560c4ea5952e8f7f506520b14b4180`  
		Last Modified: Tue, 07 Jan 2025 03:46:07 GMT  
		Size: 11.0 KB (10962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74727567a52885ab8aca0dc1a1324d70630ece75df88e9e1e39208d0491c006a`  
		Last Modified: Tue, 07 Jan 2025 03:46:08 GMT  
		Size: 2.9 MB (2889050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fc257af633959c0b9ef83f304c69fd7df4ef5f37e1791654afa84874893dda`  
		Last Modified: Tue, 07 Jan 2025 03:46:08 GMT  
		Size: 5.9 MB (5850594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7239241051528a1b46d04c5ec865993dc1e25a9e80107964efa3d43344fd9e2a`  
		Last Modified: Tue, 07 Jan 2025 03:46:08 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32b513181d311ca2cf3af11db151c00b5db7ada5bb1b7ba85f73fec9fe283d4`  
		Last Modified: Tue, 07 Jan 2025 03:46:08 GMT  
		Size: 694.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:a49dce43702d4fd6adaf06d04e50adf9e69a666faf59ae2e51fd2ae6d24a5536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636e4e71363617e632ef76024cde881862faceb2d085ae5d06442cff4972dc1a`

```dockerfile
```

-	Layers:
	-	`sha256:b26d99e612d5a1e8b7aa2d27d03bb734d6765d8472e9e27d22fade73f42fd336`  
		Last Modified: Tue, 07 Jan 2025 03:46:07 GMT  
		Size: 19.2 KB (19240 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:7046acbe2260f7eb39ff3fb5e0373d361e59bf2e9d703d29b2bd7ce265a89eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12395014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d79b13b68fc9b7be0c553c8ffb4e5912027abf687922f9d73cd90259f0e71a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Last Modified: Tue, 07 Jan 2025 03:03:15 GMT  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8ee183b60f208b9bc1d65216f96bc4a5594ea0fe9d35a65276ed5f5713571`  
		Last Modified: Tue, 07 Jan 2025 04:07:46 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6338651ebd00c79ac3efd1d59da84b325de0ed48b2cea6f07e515b63fbb7d0f`  
		Last Modified: Tue, 07 Jan 2025 04:07:46 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0195ff4b2dc21903281b604a271f5dbd39b3412d5b6f9be743aa34af8a0880cd`  
		Last Modified: Tue, 07 Jan 2025 04:07:47 GMT  
		Size: 3.0 MB (3020975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d5bb5a869ff7b54c422c57c8dcfafc997d23caed89bdbd55334da4e831ecf5`  
		Last Modified: Tue, 07 Jan 2025 04:07:47 GMT  
		Size: 6.0 MB (6006931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ffc3090f0e79f2b0baa240a313064874567ad00cf9590a23bffe5479396e82`  
		Last Modified: Tue, 07 Jan 2025 04:07:47 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32cfdb3fda2168b3279caded813141a5d4e5ccf6f614dd9d8c6a3b4dd39548`  
		Last Modified: Tue, 07 Jan 2025 04:07:47 GMT  
		Size: 699.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:c3cfba28c242c65219731f9f08dd14f22e19d04acdff5d415ca0c7e8cd64d0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c0ffa7243fddf544d7a2e237c61b0ba673ae14d20767bf958a655a7fba27ba`

```dockerfile
```

-	Layers:
	-	`sha256:90b331565adfda663eef148211dabca4d8f9c01c13439faa5c1d61cd2ceb6c23`  
		Last Modified: Tue, 07 Jan 2025 04:07:47 GMT  
		Size: 1.0 MB (1043214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9b6d0b135bda2b671e281de392701bf8ca9def64806f44adff32924f8c3148`  
		Last Modified: Tue, 07 Jan 2025 04:07:46 GMT  
		Size: 19.5 KB (19481 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.9.5`

```console
$ docker pull eggdrop@sha256:d6c33147f2594478379e1796db38711acb81f53709f5083b9cc2c1f9676e52fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.9.5` - linux; amd64

```console
$ docker pull eggdrop@sha256:59c8aa4db5bad5b774ed0863e793626502b1e5fb90440ca502d4a516c131450d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12267751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f616a81e004889be87bc99a41fd7cc33e4c9d9e975aa7200b47c888d173dd65`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Wed, 08 Jan 2025 03:16:29 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e73bca2ae2289fd661d1428fb61ba9b3edf24f2743f8f44542a0cbe9e633921`  
		Last Modified: Tue, 07 Jan 2025 03:17:43 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd18935c8babaee91be6909b2f200ffbc71f1dce2b726929acd549558a4085e`  
		Size: 10.8 KB (10833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37887064c4796239f99c4ec431fc27b839b087ed3f68a61fbc95b1bb9d88399e`  
		Last Modified: Tue, 07 Jan 2025 03:17:44 GMT  
		Size: 2.9 MB (2886333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ee9624c788488d4eb6905ccb5653649601031703dc7d2f75526313b8483c93`  
		Last Modified: Tue, 07 Jan 2025 03:17:44 GMT  
		Size: 6.0 MB (5953505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170cdb6f121a3c47c7f669e9ced3b1f9be6be9ba26f33fdee48c0588a632c067`  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe806fc73442e5f2bdefc91f3cc78c0842484eb15b1671b07cc9ad4a50bb3ed`  
		Last Modified: Tue, 07 Jan 2025 03:17:44 GMT  
		Size: 698.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:0f283a8fd7c443e7e8d45672aabcd6ed44594695f8cdfc2cd050e8ffa68ce14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920c39c7459a1a6f121e00185204937cab811db13441bf52c90a66f2af1619c4`

```dockerfile
```

-	Layers:
	-	`sha256:194553012e941cbe1e3e9a15ad021f79ee4809012c7dacbd9e1d80fd608700e5`  
		Last Modified: Tue, 07 Jan 2025 03:17:43 GMT  
		Size: 1.0 MB (1043182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7336aa81ee1d931670df84a3d91831d3ea0d7b502b3c1d9cf65ce8ff67d53af0`  
		Last Modified: Tue, 07 Jan 2025 03:17:43 GMT  
		Size: 19.4 KB (19356 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9.5` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:40531623d4f715000d44f2119bda5e2cafda4ffb31b79a84eb584dd24bd62120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11924036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecc6ec4fc13c3d3cbe9e3aee159ff3b1130e2a04259647d251bee556012e927`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.5-armhf.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:7ebe2b3dea80a0cf44722451c51fa37efc40b0c599e291ba324046244780a76f`  
		Last Modified: Tue, 07 Jan 2025 02:30:01 GMT  
		Size: 3.2 MB (3169627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2b8e877a15714d642264e38aec232054224f7e6ba8b0109c9e4c81a2e5bfdf`  
		Last Modified: Wed, 08 Jan 2025 02:30:17 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe273814a702499f005f595fadccf3f504560c4ea5952e8f7f506520b14b4180`  
		Last Modified: Tue, 07 Jan 2025 03:46:07 GMT  
		Size: 11.0 KB (10962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74727567a52885ab8aca0dc1a1324d70630ece75df88e9e1e39208d0491c006a`  
		Last Modified: Tue, 07 Jan 2025 03:46:08 GMT  
		Size: 2.9 MB (2889050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fc257af633959c0b9ef83f304c69fd7df4ef5f37e1791654afa84874893dda`  
		Last Modified: Tue, 07 Jan 2025 03:46:08 GMT  
		Size: 5.9 MB (5850594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7239241051528a1b46d04c5ec865993dc1e25a9e80107964efa3d43344fd9e2a`  
		Last Modified: Tue, 07 Jan 2025 03:46:08 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32b513181d311ca2cf3af11db151c00b5db7ada5bb1b7ba85f73fec9fe283d4`  
		Last Modified: Tue, 07 Jan 2025 03:46:08 GMT  
		Size: 694.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:a49dce43702d4fd6adaf06d04e50adf9e69a666faf59ae2e51fd2ae6d24a5536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636e4e71363617e632ef76024cde881862faceb2d085ae5d06442cff4972dc1a`

```dockerfile
```

-	Layers:
	-	`sha256:b26d99e612d5a1e8b7aa2d27d03bb734d6765d8472e9e27d22fade73f42fd336`  
		Last Modified: Tue, 07 Jan 2025 03:46:07 GMT  
		Size: 19.2 KB (19240 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9.5` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:7046acbe2260f7eb39ff3fb5e0373d361e59bf2e9d703d29b2bd7ce265a89eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12395014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d79b13b68fc9b7be0c553c8ffb4e5912027abf687922f9d73cd90259f0e71a`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 15:14:19 GMT
RUN adduser -S eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache tcl bash openssl # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:14:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 15:14:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:14:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:14:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:14:19 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:14:19 GMT
COPY entrypoint.sh /home/eggdrop/eggdrop # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
COPY docker.tcl /home/eggdrop/eggdrop/scripts/ # buildkit
# Thu, 08 Aug 2024 15:14:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:14:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Last Modified: Tue, 07 Jan 2025 03:03:15 GMT  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8ee183b60f208b9bc1d65216f96bc4a5594ea0fe9d35a65276ed5f5713571`  
		Last Modified: Tue, 07 Jan 2025 04:07:46 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6338651ebd00c79ac3efd1d59da84b325de0ed48b2cea6f07e515b63fbb7d0f`  
		Last Modified: Tue, 07 Jan 2025 04:07:46 GMT  
		Size: 11.4 KB (11353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0195ff4b2dc21903281b604a271f5dbd39b3412d5b6f9be743aa34af8a0880cd`  
		Last Modified: Tue, 07 Jan 2025 04:07:47 GMT  
		Size: 3.0 MB (3020975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d5bb5a869ff7b54c422c57c8dcfafc997d23caed89bdbd55334da4e831ecf5`  
		Last Modified: Tue, 07 Jan 2025 04:07:47 GMT  
		Size: 6.0 MB (6006931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ffc3090f0e79f2b0baa240a313064874567ad00cf9590a23bffe5479396e82`  
		Last Modified: Tue, 07 Jan 2025 04:07:47 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32cfdb3fda2168b3279caded813141a5d4e5ccf6f614dd9d8c6a3b4dd39548`  
		Last Modified: Tue, 07 Jan 2025 04:07:47 GMT  
		Size: 699.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:c3cfba28c242c65219731f9f08dd14f22e19d04acdff5d415ca0c7e8cd64d0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c0ffa7243fddf544d7a2e237c61b0ba673ae14d20767bf958a655a7fba27ba`

```dockerfile
```

-	Layers:
	-	`sha256:90b331565adfda663eef148211dabca4d8f9c01c13439faa5c1d61cd2ceb6c23`  
		Last Modified: Tue, 07 Jan 2025 04:07:47 GMT  
		Size: 1.0 MB (1043214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9b6d0b135bda2b671e281de392701bf8ca9def64806f44adff32924f8c3148`  
		Last Modified: Tue, 07 Jan 2025 04:07:46 GMT  
		Size: 19.5 KB (19481 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:d23b5417b34961010a3893691d517f023757fc949ecde98f3af6393e6c20f274
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:develop` - linux; amd64

```console
$ docker pull eggdrop@sha256:729927695d6b2733b5f38e504ec604d2c9c8f80172eddc8ccb192b225103224f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12702028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9401764e0065d8945dc3388e63c29e65d8b689ba5e66e5216bb87244d889a7`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV EGGDROP_SHA256=34c09905c2e9df1e8ca4bae5bc395a8c60f4ca93123599788bae5164ebd8f8f5
# Sun, 05 Jan 2025 16:36:07 GMT
ENV EGGDROP_COMMIT=0f5599e1fafa97454dc7a8b147c6076638e95ba8
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b15aa9d6bb751bc2ece118d1ceeac1fd953ae91ce5115ffcdb0dcc56737a9a`  
		Last Modified: Tue, 07 Jan 2025 03:18:03 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76175a7efd4beb0a08f7c5063e39f1d5c80c933c9e7d5107b381732ce74d001`  
		Last Modified: Tue, 07 Jan 2025 03:18:03 GMT  
		Size: 1.1 MB (1115388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727fa829d75cb787449e0e3594665a300878adedfe696bfa08e71ed6a0ac8f50`  
		Last Modified: Tue, 07 Jan 2025 03:18:03 GMT  
		Size: 8.0 MB (7968570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7fbc78fac6b8fd4e84b93e1fa4c5c884efca69c43b42ea0b79bcbb0c3a8f0f`  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dbe94fac61f2cfba4aaeca506a96bf634db016fa2f575d15824422978e32ea`  
		Last Modified: Tue, 07 Jan 2025 03:18:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:807bbe9848a3195e9aea8fe4d0f8de4d85a59aadabd8f7a8e8a5462efa8bda86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 KB (153052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7665172d5d5443041b175bcdafef08c78c5473ff43e9853d4090c4a680393b6f`

```dockerfile
```

-	Layers:
	-	`sha256:5010838aef7880701b352f6ad3add65d197cdebc42c1c81bad39f597d4450568`  
		Size: 136.0 KB (135961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20056e31e28aea909b171c218ea154a9ee39e5ae364a1bfa1c130d6bad19a12c`  
		Size: 17.1 KB (17091 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b7b6b09ebd2f02a2cd293bddf0bbc8debd665445d5b70128928525c6b4d21cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12307747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc558c82cabfc6caa6ecd1a7c80ec47f29168063bc9e3bba8bbfbd46364659`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV EGGDROP_SHA256=34c09905c2e9df1e8ca4bae5bc395a8c60f4ca93123599788bae5164ebd8f8f5
# Sun, 05 Jan 2025 16:36:07 GMT
ENV EGGDROP_COMMIT=0f5599e1fafa97454dc7a8b147c6076638e95ba8
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87c49c56e3d5c9303824a8cad20f5b05da63b8c632ee40628c3929f67d96cac`  
		Last Modified: Tue, 07 Jan 2025 03:41:06 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff887413f70f9ad52edadcf99d87efb7034a0479a51ab3dbfce367e24df84f0`  
		Last Modified: Tue, 07 Jan 2025 03:41:07 GMT  
		Size: 1.1 MB (1129559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df10738378fc797ed8a92e24288f8705f31564312ebfd5ae09b1d7ab4dba8b16`  
		Last Modified: Tue, 07 Jan 2025 03:41:07 GMT  
		Size: 7.8 MB (7810172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d116c4f58f7dda53eb922ff7292f3786748682a17d0c924c893881f9498dc88d`  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7829735c271e7a6b3d77e05fc88df3b3192cea9230ccc12c38433cae1f5548a`  
		Last Modified: Tue, 07 Jan 2025 03:41:07 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:8b8b5931e6aa45504808ed42f3fa770e88bfa03b30cd1be92ccfe712e8ee28a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (16954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddb7acee4888f793ae1577df1c8f14a6f85254f4786bc6d35217fecd70ae306`

```dockerfile
```

-	Layers:
	-	`sha256:5fa8568ba8b239621bf35ae9442bc99692e1f7eb94655f84ec6d4ecf62921509`  
		Last Modified: Tue, 07 Jan 2025 03:41:06 GMT  
		Size: 17.0 KB (16954 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:a3350406045f7d6b859918a7683d2d57ca06880b4849faba54e86806d549760e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13316342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3abac401f8439ce552a61ed6c1a9e17b701103a39db0cf2fa755d2a4e8bb573`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV EGGDROP_SHA256=34c09905c2e9df1e8ca4bae5bc395a8c60f4ca93123599788bae5164ebd8f8f5
# Sun, 05 Jan 2025 16:36:07 GMT
ENV EGGDROP_COMMIT=0f5599e1fafa97454dc7a8b147c6076638e95ba8
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adba3ad06ebd31a48135af820872fd883c103f9fd47fb46b953a0d826867c58`  
		Last Modified: Tue, 07 Jan 2025 04:03:52 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6504725a30a01dfb79c3839e72991ba0790ded436ec4b8b28f5b2a462d5297`  
		Last Modified: Tue, 07 Jan 2025 04:03:53 GMT  
		Size: 1.2 MB (1210975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300703333265e1956b3afca6b0dadc62a0cbcb6c0e5b689c5a72f152be0b8570`  
		Last Modified: Tue, 07 Jan 2025 04:03:53 GMT  
		Size: 8.0 MB (8014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fad5d492ce46807009d3fc2d44ae9a1149700e436e2f9b5430ba0b1a04571c`  
		Last Modified: Tue, 07 Jan 2025 04:03:53 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45782f8ec381ea791c592888c258bb51bb0430b51cde85b19625728336aec985`  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:4376743a3b70242a30ec81364d7d96e5f86385150421a38e4dcfaf5ef2c6cd4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 KB (153169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9b2411c3aa324a99ac14bbad73487660a4f7e0dd6113c8a318a88e02347f4d`

```dockerfile
```

-	Layers:
	-	`sha256:cef8090bb5cb0d18ee43925e291fd53947605cdc575a6657f2a35fceee074ff7`  
		Last Modified: Tue, 07 Jan 2025 04:03:53 GMT  
		Size: 136.0 KB (135981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:040e8e3fdc8363e8ef0704ab8249897dd37cd31aba4b3aa405e4d38300e939eb`  
		Last Modified: Tue, 07 Jan 2025 04:03:52 GMT  
		Size: 17.2 KB (17188 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:1d021af09fc6b335e8ea949270cf7a54b806b5b24866d9a057c6a138f8d30f05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:252fef8f4674db29dbef6efe0bc8fca2e8204067d25c1a566ce7fef9e6b3f011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad355cd0826d4f00e2adb90ce79426822c8976e785d4ddfb63f49ecfc4291f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218cdc53cb6ea10a45c5a146c668fbb9524c28ade07376af7b4ab701561bdd7a`  
		Last Modified: Tue, 07 Jan 2025 03:18:14 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cbc9aca64aad13c1bdab9bf8b07a57e2ae2920bcc2606f6acfdaa841243520`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 1.1 MB (1115384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4631e8311e35d39893a97f134637a19872dea48770f5ff12aa20a996957dbd7a`  
		Size: 12.7 MB (12719108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80323b392cd4ad927810eca7e0b11ec2d8dd7604b3ccf4bb12391d6b779f99f2`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1341f3e5b237d9adc22646c6ce2818d7f2e2f48557f99cfaf9d73e7737ca3b0`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:b6fe0374f54c544f69b4f8403c641737c9865517d350fd69abe178f6ff455a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 KB (157535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f745c424c568d08a21366fcb3f7a0f296ec900fc8c88e95650a3edd7c3d3e041`

```dockerfile
```

-	Layers:
	-	`sha256:881a932e81e716a7b00195e3644f8aa1233475ce9be9d65961224804668500ae`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 138.8 KB (138764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2065ff5353ade8036f62c1d02d1dffb721272a67018ded9399d8b968d27866b9`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b8d2e3cbcb9a2cb3681d6c7301de4c18586f1ba0f753cb7473192bba80ed627e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17058170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b449786e64fa60a401e21ee13f3975c91ebafedaef4c9ec82cd47366d9f0022`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87c49c56e3d5c9303824a8cad20f5b05da63b8c632ee40628c3929f67d96cac`  
		Last Modified: Tue, 07 Jan 2025 03:41:06 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff887413f70f9ad52edadcf99d87efb7034a0479a51ab3dbfce367e24df84f0`  
		Last Modified: Tue, 07 Jan 2025 03:41:07 GMT  
		Size: 1.1 MB (1129559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066a79e578efc48121cd7ecf1a2a7dab91a745976bf8a39bf1f21dab825f55dc`  
		Last Modified: Tue, 07 Jan 2025 03:49:21 GMT  
		Size: 12.6 MB (12560590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d533c9c557185da954a345b2e99603427489f36113aa72bc26005df4944f0a68`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57980c8622b60855176cf792e318d3222a64c01141570ba18004c564de38f62e`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:0f2d1d9db0a7c3019d94927700824e94d2d7ddc06f919d1868c6d811be14e4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76393351c93a2081d88863f200559b1157f34e64d61d32e2d7ea7ff594e8618`

```dockerfile
```

-	Layers:
	-	`sha256:e66653e79f8153ba3e8ae3178c5f8acac0eecb1356fb2c84bf69f152bc127452`  
		Last Modified: Tue, 07 Jan 2025 03:49:16 GMT  
		Size: 18.7 KB (18658 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:cde577b4d2f2fe326ffbf4470cc1b563354e0e17b271db25104cf2d7dc6eb176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18155441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf81282b168ce87f4b1238311649e2fffbb72e652ea2cdfc3452c81bd69eb5f7`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adba3ad06ebd31a48135af820872fd883c103f9fd47fb46b953a0d826867c58`  
		Last Modified: Tue, 07 Jan 2025 04:03:52 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6504725a30a01dfb79c3839e72991ba0790ded436ec4b8b28f5b2a462d5297`  
		Last Modified: Tue, 07 Jan 2025 04:03:53 GMT  
		Size: 1.2 MB (1210975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8924a6ff021d35b2a990093f6873fd81752352e73a34525e3745e9ee23784`  
		Last Modified: Tue, 07 Jan 2025 04:10:09 GMT  
		Size: 12.9 MB (12853706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2275c94babe8d4ae787dec6b0a0e00650296d046bb82ed20863a6a2623aaa40`  
		Last Modified: Tue, 07 Jan 2025 04:10:09 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3e1e29765384f88e226f621ccf019e19493966727c332aa83c60b8027cc412`  
		Last Modified: Tue, 07 Jan 2025 04:10:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d0b5932270e88f7434a49b3d134ca8295cb84f09a0808e45cc111941c6dbe14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 KB (157725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ba6c476080f48073c51278234586a50e88214c2bcad90d80a0c7db2148bc75`

```dockerfile
```

-	Layers:
	-	`sha256:e95d59eb7daed26d83539a3f877304467c1236a438db609726e22813e808a174`  
		Last Modified: Tue, 07 Jan 2025 04:10:08 GMT  
		Size: 138.8 KB (138820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a17090e74a6d50268d8142352a0f3c61eec903c1618e4f7a889fc6ea1fb7a4`  
		Last Modified: Tue, 07 Jan 2025 04:10:11 GMT  
		Size: 18.9 KB (18905 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:1d021af09fc6b335e8ea949270cf7a54b806b5b24866d9a057c6a138f8d30f05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:252fef8f4674db29dbef6efe0bc8fca2e8204067d25c1a566ce7fef9e6b3f011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17452561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daad355cd0826d4f00e2adb90ce79426822c8976e785d4ddfb63f49ecfc4291f`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218cdc53cb6ea10a45c5a146c668fbb9524c28ade07376af7b4ab701561bdd7a`  
		Last Modified: Tue, 07 Jan 2025 03:18:14 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cbc9aca64aad13c1bdab9bf8b07a57e2ae2920bcc2606f6acfdaa841243520`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 1.1 MB (1115384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4631e8311e35d39893a97f134637a19872dea48770f5ff12aa20a996957dbd7a`  
		Size: 12.7 MB (12719108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80323b392cd4ad927810eca7e0b11ec2d8dd7604b3ccf4bb12391d6b779f99f2`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1341f3e5b237d9adc22646c6ce2818d7f2e2f48557f99cfaf9d73e7737ca3b0`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:b6fe0374f54c544f69b4f8403c641737c9865517d350fd69abe178f6ff455a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 KB (157535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f745c424c568d08a21366fcb3f7a0f296ec900fc8c88e95650a3edd7c3d3e041`

```dockerfile
```

-	Layers:
	-	`sha256:881a932e81e716a7b00195e3644f8aa1233475ce9be9d65961224804668500ae`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 138.8 KB (138764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2065ff5353ade8036f62c1d02d1dffb721272a67018ded9399d8b968d27866b9`  
		Last Modified: Tue, 07 Jan 2025 03:18:15 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:b8d2e3cbcb9a2cb3681d6c7301de4c18586f1ba0f753cb7473192bba80ed627e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17058170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b449786e64fa60a401e21ee13f3975c91ebafedaef4c9ec82cd47366d9f0022`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87c49c56e3d5c9303824a8cad20f5b05da63b8c632ee40628c3929f67d96cac`  
		Last Modified: Tue, 07 Jan 2025 03:41:06 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff887413f70f9ad52edadcf99d87efb7034a0479a51ab3dbfce367e24df84f0`  
		Last Modified: Tue, 07 Jan 2025 03:41:07 GMT  
		Size: 1.1 MB (1129559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066a79e578efc48121cd7ecf1a2a7dab91a745976bf8a39bf1f21dab825f55dc`  
		Last Modified: Tue, 07 Jan 2025 03:49:21 GMT  
		Size: 12.6 MB (12560590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d533c9c557185da954a345b2e99603427489f36113aa72bc26005df4944f0a68`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 2.0 KB (1952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57980c8622b60855176cf792e318d3222a64c01141570ba18004c564de38f62e`  
		Last Modified: Tue, 07 Jan 2025 03:49:17 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:0f2d1d9db0a7c3019d94927700824e94d2d7ddc06f919d1868c6d811be14e4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76393351c93a2081d88863f200559b1157f34e64d61d32e2d7ea7ff594e8618`

```dockerfile
```

-	Layers:
	-	`sha256:e66653e79f8153ba3e8ae3178c5f8acac0eecb1356fb2c84bf69f152bc127452`  
		Last Modified: Tue, 07 Jan 2025 03:49:16 GMT  
		Size: 18.7 KB (18658 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:cde577b4d2f2fe326ffbf4470cc1b563354e0e17b271db25104cf2d7dc6eb176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18155441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf81282b168ce87f4b1238311649e2fffbb72e652ea2cdfc3452c81bd69eb5f7`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["/bin/sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Sun, 05 Jan 2025 16:36:07 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENV NICK=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV SERVER=
# Sun, 05 Jan 2025 16:36:07 GMT
ENV LISTEN=3333
# Sun, 05 Jan 2025 16:36:07 GMT
ENV USERFILE=eggdrop.user
# Sun, 05 Jan 2025 16:36:07 GMT
ENV CHANFILE=eggdrop.chan
# Sun, 05 Jan 2025 16:36:07 GMT
WORKDIR /home/eggdrop/eggdrop
# Sun, 05 Jan 2025 16:36:07 GMT
EXPOSE map[3333/tcp:{}]
# Sun, 05 Jan 2025 16:36:07 GMT
COPY entrypoint.sh ./ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
COPY docker.tcl ./scripts/ # buildkit
# Sun, 05 Jan 2025 16:36:07 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Sun, 05 Jan 2025 16:36:07 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adba3ad06ebd31a48135af820872fd883c103f9fd47fb46b953a0d826867c58`  
		Last Modified: Tue, 07 Jan 2025 04:03:52 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6504725a30a01dfb79c3839e72991ba0790ded436ec4b8b28f5b2a462d5297`  
		Last Modified: Tue, 07 Jan 2025 04:03:53 GMT  
		Size: 1.2 MB (1210975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8924a6ff021d35b2a990093f6873fd81752352e73a34525e3745e9ee23784`  
		Last Modified: Tue, 07 Jan 2025 04:10:09 GMT  
		Size: 12.9 MB (12853706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2275c94babe8d4ae787dec6b0a0e00650296d046bb82ed20863a6a2623aaa40`  
		Last Modified: Tue, 07 Jan 2025 04:10:09 GMT  
		Size: 2.0 KB (1951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3e1e29765384f88e226f621ccf019e19493966727c332aa83c60b8027cc412`  
		Last Modified: Tue, 07 Jan 2025 04:10:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d0b5932270e88f7434a49b3d134ca8295cb84f09a0808e45cc111941c6dbe14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 KB (157725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ba6c476080f48073c51278234586a50e88214c2bcad90d80a0c7db2148bc75`

```dockerfile
```

-	Layers:
	-	`sha256:e95d59eb7daed26d83539a3f877304467c1236a438db609726e22813e808a174`  
		Last Modified: Tue, 07 Jan 2025 04:10:08 GMT  
		Size: 138.8 KB (138820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a17090e74a6d50268d8142352a0f3c61eec903c1618e4f7a889fc6ea1fb7a4`  
		Last Modified: Tue, 07 Jan 2025 04:10:11 GMT  
		Size: 18.9 KB (18905 bytes)  
		MIME: application/vnd.in-toto+json
