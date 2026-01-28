## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:089a3e8f8fc63237fc84283d3a01763908e8163659a9d8f16eb9165b28a19576
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
$ docker pull eggdrop@sha256:75604f971a95fc3315b618630920ed7b16ad0bad4e32423780835c1a935a392e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17470125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484fb7a359f5cd0eb36db932e8d7f9182ab4da24806051e57c4f620ac46b14cf`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:55 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:55 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:56 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:17:39 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:17:39 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:17:39 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:17:39 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:17:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:17:39 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:17:39 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:17:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:17:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b447b85aab30cbd4e93becaad9e1208b0a764b53c40aef3dfe59eb276d774865`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b578563d5af8bbbd476ae5c994768e549362f58ca6a42f53e6440b2ae6c51ad`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 MB (1115911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6114e6e6716e78dd8ac2824cf6a70806321dff723fffd1656200948827841b75`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 12.7 MB (12722284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697ebd10c79fa694752b817a0ead2f05dd1ec5caee6852a4bdaa8f9e747e00d1`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e27ee35abd6ced910bc0bdcc35503e055d42386a5bb1f31c7e240238603af7`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:3d366e9f3a29c9637105b4ff5da62b54f062494788ce8ad4735e44976af31a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 KB (159261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3a7312cd85c5d86bcf78a88b83a605d2398a6835dc69268e4c9a5f167aea1d`

```dockerfile
```

-	Layers:
	-	`sha256:0fca8dee8c5827f93ecc12b6f7d0d95290c0e133f5296c03e4639a7de5582959`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 140.5 KB (140534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23404d87d4058c8ee642ae3af674a727b34422f5928d2b394f9a879c069c8df3`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:a8d21059c7bbff95c6fbcb8669d4d54e5d6ca6a3c29c7f43af95d89b8b3ea7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17076274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5049a5338cb8d03826b6ef2eb20fe56b1fff5c42e261713748a10c84c9de92cc`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Sun, 05 Jan 2025 16:36:07 GMT
ADD alpine-minirootfs-3.20.8-armhf.tar.gz / # buildkit
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
	-	`sha256:4d3ea13a40ffa4399bfa8db9b7de868ea73e3273e5d3a36611db57f42b62213c`  
		Last Modified: Wed, 08 Oct 2025 21:00:29 GMT  
		Size: 3.4 MB (3371145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cca15b0d60a69ae3c9fe85609cc2280bd54f663348c1173479b30243da18174`  
		Last Modified: Wed, 08 Oct 2025 21:35:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78bdc93c9660244511056bf87eddfa706742b6d416b2912c6839707f2bf6b22`  
		Last Modified: Wed, 08 Oct 2025 21:35:05 GMT  
		Size: 1.1 MB (1130246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efeaae033b267e83657e36c933344c4107e0864e354ca8e7c433c08fbf7b57f`  
		Last Modified: Wed, 08 Oct 2025 21:35:06 GMT  
		Size: 12.6 MB (12570812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19cdb36d616ba5f1950925bc449bc4fd414dc306f91bc59d215b19579a5e4c5`  
		Last Modified: Wed, 08 Oct 2025 21:35:06 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24088101cee5454d8aa675ff3dea5852472f182b8efd8e1fbc6ec3eca26a99b8`  
		Last Modified: Wed, 08 Oct 2025 21:35:07 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:8bc3118510adb2010e1362ec2f0fd41e4a6b391d3445dea1bf4f4e1ac3189558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb853a8a44148735eed6ab58af33f401b5c47d59131ea92df1bd9eecb0572bf`

```dockerfile
```

-	Layers:
	-	`sha256:84a1456da57981ed861a07122bf9bbe5775a209e9826174b80f655f5bb150760`  
		Last Modified: Wed, 08 Oct 2025 21:35:05 GMT  
		Size: 18.7 KB (18662 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:38cf62d26331fd049ca2f5d5b3019cf0e01276ff8b924d2ff848652214fb15c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18163420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ecb88b3c8f94581811f88893f650787301460f320a0029e84d2adfd9575313`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:19 GMT
ADD alpine-minirootfs-3.20.9-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:19 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:15:34 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 28 Jan 2026 02:15:34 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 28 Jan 2026 02:15:34 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0.tar.gz.asc eggdrop-1.10.0.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0.tar.gz.asc   && tar -zxvf eggdrop-1.10.0.tar.gz   && rm eggdrop-1.10.0.tar.gz   && ( cd eggdrop-1.10.0     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
ENV NICK=
# Wed, 28 Jan 2026 02:17:38 GMT
ENV SERVER=
# Wed, 28 Jan 2026 02:17:38 GMT
ENV LISTEN=3333
# Wed, 28 Jan 2026 02:17:38 GMT
ENV USERFILE=eggdrop.user
# Wed, 28 Jan 2026 02:17:38 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 28 Jan 2026 02:17:38 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 28 Jan 2026 02:17:38 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 28 Jan 2026 02:17:38 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 28 Jan 2026 02:17:38 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 28 Jan 2026 02:17:38 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:83b2d7e29698161422a104647ffb26568fe86648ff3609d1b60a4f9e9de38074`  
		Last Modified: Wed, 28 Jan 2026 01:18:24 GMT  
		Size: 4.1 MB (4089958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d19a964560edb0c0f83f231cc87e7375585adcaac10463b06bbdc93ed314fc7`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec72b194072ac61d9d30264898bae7ca9508d13766fa4228956f974885de617`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.2 MB (1211877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bcdaddba9569dddc649c66079b31b6dbf3e6c25bba18a9e9b77a4836b46a9a`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 12.9 MB (12857520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a7c818db83516965e8cb1105908c2931829f0d2cb6bddfa294d6c151c6e5a`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430dc418511aaa4f733285115389bdb5cb0aff5941295ea7d11a1d3d415f50da`  
		Last Modified: Wed, 28 Jan 2026 02:17:46 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:8434220176204ec11de29cc19482ccfab749781a4547957352170e7729b67e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 KB (159452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e6d47e09077cff93d54cd320b9ad09c71530d36298b6acad1bebef65166527`

```dockerfile
```

-	Layers:
	-	`sha256:fa324f4563bba4f1b5e8bf6dfac63e2c19b3d54e389c94ac161f7de7e6bc5944`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 140.6 KB (140590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe221b196f9139c99e479c14b73b286f065f2f9ab7233d397462f48bcba7b1b3`  
		Last Modified: Wed, 28 Jan 2026 02:17:45 GMT  
		Size: 18.9 KB (18862 bytes)  
		MIME: application/vnd.in-toto+json
