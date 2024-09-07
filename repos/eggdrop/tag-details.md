<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.10.0rc1`](#eggdrop1100rc1)
-	[`eggdrop:1.9`](#eggdrop19)
-	[`eggdrop:1.9.5`](#eggdrop195)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.10.0rc1`

```console
$ docker pull eggdrop@sha256:57f892e08dac96bb3af82cd7e908a2c0594cc02784b4b461f3ff4358bf81209a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8

### `eggdrop:1.10.0rc1` - linux; amd64

```console
$ docker pull eggdrop@sha256:b191f9cf3b6d4047f958d7d0830ee6018371e0ed9d14ea83b9cd3f025e9dc4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17456644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf52d801807de0a50f4a5ed06d11e49d2a2c294a69d774c134cd183e4cfb680`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:45:15 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 15:45:15 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0rc1.tar.gz.asc eggdrop-1.10.0rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.0rc1.tar.gz   && rm eggdrop-1.10.0rc1.tar.gz   && ( cd eggdrop-1.10.0rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10rc1.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:45:15 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:45:15 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:45:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:45:15 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:45:15 GMT
COPY entrypoint.sh ./ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
COPY docker.tcl ./scripts/ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b750e6e553fd499f187baca7481d56c05e607495da9e14e6212942c2c8d6960`  
		Last Modified: Fri, 06 Sep 2024 23:19:04 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db68c2e4736fcb94b873e0357b0fc84e90968e34abdc6ccf138c5ca7885d819`  
		Last Modified: Fri, 06 Sep 2024 23:19:04 GMT  
		Size: 1.1 MB (1115384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92f307d16d862612d0c8a7395faa433bb8e330b36d2cb4ec6e3e4326d64d95b`  
		Last Modified: Fri, 06 Sep 2024 23:19:04 GMT  
		Size: 12.7 MB (12713384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1212f275cba947f888921219eb6945920d60748274075d64209538413b236c2`  
		Last Modified: Fri, 06 Sep 2024 23:19:04 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7dc5b4ac2b66fbfa201675935d7e31a732fb3694ee3de7e462b2379a3a0dbe`  
		Last Modified: Fri, 06 Sep 2024 23:19:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0rc1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:cbd750cecce0603f553661e13ded1dddf2b8e2187c4128b424cc9e193bc69b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 KB (153778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf989ad575829c2a1431b5456407a6c9981a49cca86501d5dc30b211d597aef`

```dockerfile
```

-	Layers:
	-	`sha256:caa6eae48b9fe043a06f7b4c32a97fae15d56ee4fa661170cd55f7a914a7177f`  
		Last Modified: Fri, 06 Sep 2024 23:19:04 GMT  
		Size: 136.0 KB (136043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c9fcf267f830160625cafcda11db5ad53540f9af9293c075466f0b907011ed7`  
		Last Modified: Fri, 06 Sep 2024 23:19:04 GMT  
		Size: 17.7 KB (17735 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.0rc1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:761f5b201a511413d41c97eec2b7bbe4f36fa1d0e34127ef0cb4a13b4c67305a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18999609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c1dc89f26487c258c5f02f76ec62b2dac726932b4c795b6e3713a6eea4f0fa`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 15:45:15 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0rc1.tar.gz.asc eggdrop-1.10.0rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.0rc1.tar.gz   && rm eggdrop-1.10.0rc1.tar.gz   && ( cd eggdrop-1.10.0rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10rc1.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:45:15 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:45:15 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:45:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:45:15 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:45:15 GMT
COPY entrypoint.sh ./ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
COPY docker.tcl ./scripts/ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515d11fe5ed07f0771a0f823866375c1d173ce2c6c82575208e8c39a43ec7020`  
		Last Modified: Fri, 06 Sep 2024 21:03:15 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3abe0d0188fbfa3e981d45905f4897f98d4b70258463b3c7a5faac03f562eea`  
		Last Modified: Fri, 06 Sep 2024 21:03:15 GMT  
		Size: 3.1 MB (3075692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e99684e3310e3b913150852f52800f4283d52d2ad6e8f270488335cdf637ca`  
		Last Modified: Fri, 06 Sep 2024 21:11:57 GMT  
		Size: 12.6 MB (12554654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb658dcde8cac33fca9c261a978cbc7aa45ec92228840dd2b718f5194f343a`  
		Last Modified: Fri, 06 Sep 2024 21:11:57 GMT  
		Size: 1.9 KB (1950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5484b9dbe6e8ef7e2b5f10db98b9f0ca92815f17dc4c0c28d90c296acebfbf32`  
		Last Modified: Fri, 06 Sep 2024 21:11:57 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.0rc1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:7fbcf9dd82c03a97e2d52e27843bb3801d322eff3d0093e93600a4baf28aba76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9b9b42dead3170eb5675363f38dd961eebd40899c1bfb163e356530a9ed488`

```dockerfile
```

-	Layers:
	-	`sha256:a7943038048381bc0744f1dee2b23ff44a263e1a23fcbe826475dc18130091ce`  
		Last Modified: Fri, 06 Sep 2024 21:11:56 GMT  
		Size: 17.6 KB (17587 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.0rc1` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:46ea6d2c159b3b9bc6f3128655a67bc7fd717768635c20eca2842de432d6057c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18151504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea179d9eee100a0012f2ef16e8dc6728b333f11c4d67256b4641d13a177238f7`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:43:37 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 19:43:38 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop
# Thu, 08 Aug 2024 19:43:39 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl
# Thu, 08 Aug 2024 19:51:30 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.0rc1.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.0rc1.tar.gz.asc eggdrop-1.10.0rc1.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.10.0rc1.tar.gz.asc   && tar -zxvf eggdrop-1.10.0rc1.tar.gz   && rm eggdrop-1.10.0rc1.tar.gz   && ( cd eggdrop-1.10.0rc1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10rc1.0   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps
# Thu, 08 Aug 2024 19:51:30 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:51:30 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:51:30 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:51:30 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:51:30 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:51:30 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:51:31 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:51:31 GMT
COPY file:15b1df22891b2d819093301ed85a114b9e76e06ecf7eba8f403edb7908e4aebf in ./ 
# Thu, 08 Aug 2024 19:51:31 GMT
COPY file:61da6bdf6e84c41c8486cddfad6cc1d25ced9bbeaa056bab87034428f2134436 in ./scripts/ 
# Thu, 08 Aug 2024 19:51:31 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:51:31 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df1fbd90925124f99f470d0e8fb64bb807608c5c0bbe563414aaec386a6b0ca`  
		Last Modified: Thu, 08 Aug 2024 19:51:52 GMT  
		Size: 966.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1131de528037c7182c2a886926b7114abcc3062bddced8c87d376e2afe96a63`  
		Last Modified: Thu, 08 Aug 2024 19:51:53 GMT  
		Size: 1.2 MB (1210745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be04448f413a85c8ce43c1d1c20b472d29e43641fce6d89a581cef503000c96`  
		Last Modified: Thu, 08 Aug 2024 19:52:17 GMT  
		Size: 12.8 MB (12849778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15eef4afabf88334bfa97a962b51f53fa76289169d4482bedb76dab3204718f`  
		Last Modified: Thu, 08 Aug 2024 19:52:15 GMT  
		Size: 2.0 KB (1954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b21e083e2d9b1229a3690ffa8d4c5a42ac50664a7dd6bfd72c10e09033a83f7`  
		Last Modified: Thu, 08 Aug 2024 19:52:15 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9`

```console
$ docker pull eggdrop@sha256:dfdff3fc1468d8ca30be6b70fc9b72c8d0f51a00f73015cbff995b2a628a7118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8

### `eggdrop:1.9` - linux; amd64

```console
$ docker pull eggdrop@sha256:464fa69cb45f5509980cd7b70bdf33209d893d95c3fd4e1a4cd6a2e1416564f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12298795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d06db72b6c7a18beee096a1b8fba98574219450ef740740bcce13e71ef7e771`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97044ed21665bdc39e4fb6615c274aed679f6b8f55e5465fae4f555719965f9b`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687876d96a0d41fb3e048eac436131b2b6815643c88e7bd077811d7b63bddc04`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 10.8 KB (10830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7353807a5a9d0ab0b70534e9de509c882d3c03958adccae7962bab12d41a030f`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 2.9 MB (2900184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab05178db53ad0b2b8818dbb268a624880309ac9d286fc96d24df5b593b348b`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 6.0 MB (5964265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102028674158922bccbfdcd6d7ea8994766105a27d363f4f71273a20d0010fd`  
		Last Modified: Fri, 06 Sep 2024 23:18:46 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a05837526fe00223759e8d4a997d16345eadd06e863fa822ff79f7b5243343`  
		Last Modified: Fri, 06 Sep 2024 23:18:46 GMT  
		Size: 699.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:cf8a57886874429df642e8168365c3ecb7a063d42bb23e7f1f2c1e19dc68cd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93173c29b543a157fcdd4fbac48cdaf4aca24e2c09177e19d20f7987b6e468c`

```dockerfile
```

-	Layers:
	-	`sha256:bfa78d355a05f618bcb520a2ee2043fa052ec431140c725530bf4ad0b42484c1`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 1.0 MB (1044135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2336848c7176ed259cdb0ee73a90625f3667393472804f7ec51bc8d9841dbda2`  
		Last Modified: Fri, 06 Sep 2024 23:18:44 GMT  
		Size: 19.7 KB (19747 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:03e1314ed57502af97e01e97c0530d74d0f81f18ff9c53ecd3b5cace76bfe7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13701136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e664fe986d5565c68c790bb5b1e86fbb994d849c253e356ee2e98184ae1dd6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
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
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dcb41c61459f2a403456e5891620aef35c65ef74050994aad2af1ab6e621b6`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fb7c554f9f18b4618cc72ab1fed00f4121ad7e1f19cb89319885fea95384e`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 11.0 KB (10961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e65e8815edf970cf2b1ba307821854aba8a638c33dc95e77482ca36a3bb36b`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 4.7 MB (4651897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b62939420f89f5597cd9908110297efcce3d765484ff819723acdf395f9385`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 5.9 MB (5858807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49a673f5e0325c4cc20f8ca46ea2efa50c34eed5724a10f2cb17c838b5b5e93`  
		Last Modified: Fri, 06 Sep 2024 21:08:40 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b304f35d5545678f352755b28b9b4e423273fd847dd98fce2d02d2996c44af79`  
		Last Modified: Fri, 06 Sep 2024 21:08:40 GMT  
		Size: 696.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9` - unknown; unknown

```console
$ docker pull eggdrop@sha256:bb3ced9249e06c250f433eace6c28018f6213010a13281ac9a3738be6f8d9a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1528fc5c91f6e1fe0cde4e03a377210ac3235b05dcee62afd9dab11d0c504d5e`

```dockerfile
```

-	Layers:
	-	`sha256:4b7c8ae76836ae228ff763e3141b1f28fb9911025ac4aa9e2a8c2e8f24463546`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 19.6 KB (19637 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:64166b3cf2df01a17e431db880b621810acda5b0fd0ddbba6ba59105e2b82fd8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12424083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d293d71c94643df7ec3252594eca670575e13b9d2d9c0bf18a71aea03b02a8d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:45:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 19:45:45 GMT
RUN adduser -S eggdrop
# Thu, 08 Aug 2024 19:45:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 08 Aug 2024 19:45:48 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 08 Aug 2024 19:49:18 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 08 Aug 2024 19:49:18 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:49:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 19:49:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:49:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:49:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:49:19 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 08 Aug 2024 19:49:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:49:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3af4066f123f44c2fb98e2f28964f982bc14db4ba15906ad8cc3887a867266`  
		Last Modified: Thu, 08 Aug 2024 19:52:03 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ccffd445d45c37456f285a0ce2105caf980a691a88a750da9d0b219b008a86`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 11.4 KB (11395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0587e228beafa54aa50b93967977861c70914e0ddedcd401e31b42fd0c0e733`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 3.0 MB (3034852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dfbf35befd934b3269c7f9f9c391974da4d1dca33f36515bd2dfa7352f5d1e`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 6.0 MB (6015601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6a4d43f2f43e12cbd85ae7f616403e0c64a507c111410e4fa39fb99153592`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae77733354b0d53d2c6134cf545bf14ed540dec92c819344b15a4ab36c0a228c`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:1.9.5`

```console
$ docker pull eggdrop@sha256:dfdff3fc1468d8ca30be6b70fc9b72c8d0f51a00f73015cbff995b2a628a7118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8

### `eggdrop:1.9.5` - linux; amd64

```console
$ docker pull eggdrop@sha256:464fa69cb45f5509980cd7b70bdf33209d893d95c3fd4e1a4cd6a2e1416564f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12298795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d06db72b6c7a18beee096a1b8fba98574219450ef740740bcce13e71ef7e771`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97044ed21665bdc39e4fb6615c274aed679f6b8f55e5465fae4f555719965f9b`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687876d96a0d41fb3e048eac436131b2b6815643c88e7bd077811d7b63bddc04`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 10.8 KB (10830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7353807a5a9d0ab0b70534e9de509c882d3c03958adccae7962bab12d41a030f`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 2.9 MB (2900184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab05178db53ad0b2b8818dbb268a624880309ac9d286fc96d24df5b593b348b`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 6.0 MB (5964265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102028674158922bccbfdcd6d7ea8994766105a27d363f4f71273a20d0010fd`  
		Last Modified: Fri, 06 Sep 2024 23:18:46 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a05837526fe00223759e8d4a997d16345eadd06e863fa822ff79f7b5243343`  
		Last Modified: Fri, 06 Sep 2024 23:18:46 GMT  
		Size: 699.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:cf8a57886874429df642e8168365c3ecb7a063d42bb23e7f1f2c1e19dc68cd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93173c29b543a157fcdd4fbac48cdaf4aca24e2c09177e19d20f7987b6e468c`

```dockerfile
```

-	Layers:
	-	`sha256:bfa78d355a05f618bcb520a2ee2043fa052ec431140c725530bf4ad0b42484c1`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 1.0 MB (1044135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2336848c7176ed259cdb0ee73a90625f3667393472804f7ec51bc8d9841dbda2`  
		Last Modified: Fri, 06 Sep 2024 23:18:44 GMT  
		Size: 19.7 KB (19747 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9.5` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:03e1314ed57502af97e01e97c0530d74d0f81f18ff9c53ecd3b5cace76bfe7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13701136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e664fe986d5565c68c790bb5b1e86fbb994d849c253e356ee2e98184ae1dd6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
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
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dcb41c61459f2a403456e5891620aef35c65ef74050994aad2af1ab6e621b6`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fb7c554f9f18b4618cc72ab1fed00f4121ad7e1f19cb89319885fea95384e`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 11.0 KB (10961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e65e8815edf970cf2b1ba307821854aba8a638c33dc95e77482ca36a3bb36b`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 4.7 MB (4651897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b62939420f89f5597cd9908110297efcce3d765484ff819723acdf395f9385`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 5.9 MB (5858807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49a673f5e0325c4cc20f8ca46ea2efa50c34eed5724a10f2cb17c838b5b5e93`  
		Last Modified: Fri, 06 Sep 2024 21:08:40 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b304f35d5545678f352755b28b9b4e423273fd847dd98fce2d02d2996c44af79`  
		Last Modified: Fri, 06 Sep 2024 21:08:40 GMT  
		Size: 696.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.9.5` - unknown; unknown

```console
$ docker pull eggdrop@sha256:bb3ced9249e06c250f433eace6c28018f6213010a13281ac9a3738be6f8d9a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1528fc5c91f6e1fe0cde4e03a377210ac3235b05dcee62afd9dab11d0c504d5e`

```dockerfile
```

-	Layers:
	-	`sha256:4b7c8ae76836ae228ff763e3141b1f28fb9911025ac4aa9e2a8c2e8f24463546`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 19.6 KB (19637 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.9.5` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:64166b3cf2df01a17e431db880b621810acda5b0fd0ddbba6ba59105e2b82fd8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12424083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d293d71c94643df7ec3252594eca670575e13b9d2d9c0bf18a71aea03b02a8d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:45:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 19:45:45 GMT
RUN adduser -S eggdrop
# Thu, 08 Aug 2024 19:45:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 08 Aug 2024 19:45:48 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 08 Aug 2024 19:49:18 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 08 Aug 2024 19:49:18 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:49:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 19:49:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:49:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:49:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:49:19 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 08 Aug 2024 19:49:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:49:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3af4066f123f44c2fb98e2f28964f982bc14db4ba15906ad8cc3887a867266`  
		Last Modified: Thu, 08 Aug 2024 19:52:03 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ccffd445d45c37456f285a0ce2105caf980a691a88a750da9d0b219b008a86`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 11.4 KB (11395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0587e228beafa54aa50b93967977861c70914e0ddedcd401e31b42fd0c0e733`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 3.0 MB (3034852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dfbf35befd934b3269c7f9f9c391974da4d1dca33f36515bd2dfa7352f5d1e`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 6.0 MB (6015601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6a4d43f2f43e12cbd85ae7f616403e0c64a507c111410e4fa39fb99153592`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae77733354b0d53d2c6134cf545bf14ed540dec92c819344b15a4ab36c0a228c`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:5d1bbaeef0470adf9a3d6cc187522f5d46a5b5ec921a29e0ce35be043da41fb6
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
$ docker pull eggdrop@sha256:e35a60699d0a9d8fd305a5ecc44b2f9a3673c2a3d5923116834b79437d0e0c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16410625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bac9601bf3a0ea9df0d8cb4c39aab7d4f819ea81ccf60895582c6e9180da064`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:45:15 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 15:45:15 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV EGGDROP_SHA256=d185512ad282aeee49a75328e847f604c762e94be19fb1e01a7e8a4f927730b8
# Thu, 08 Aug 2024 15:45:15 GMT
ENV EGGDROP_COMMIT=f80f8ae468fd7bcec83407134ef5941225131104
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:45:15 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:45:15 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:45:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:45:15 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:45:15 GMT
COPY entrypoint.sh ./ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
COPY docker.tcl ./scripts/ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb209af1764bcbfa0c48f2a65dde47657f4c675b7e5057a08e0aa5848d873a69`  
		Last Modified: Fri, 06 Sep 2024 23:17:42 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630d7778d2e0f9a12663737b02fd1fb5fb0a0a7ae5e5d345a88026b9d744c2d9`  
		Last Modified: Fri, 06 Sep 2024 23:17:42 GMT  
		Size: 1.1 MB (1115387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d842f35428ec42446199c23e29c853f224985bed198b70aebc2d43d30bfea77e`  
		Last Modified: Fri, 06 Sep 2024 23:17:43 GMT  
		Size: 11.7 MB (11667370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fc40472f1c1aba83f44cd0cb87bfb11fcef0ebee915a583ea9ec78cbe89e44`  
		Last Modified: Fri, 06 Sep 2024 23:17:42 GMT  
		Size: 1.9 KB (1943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a761a8fc913603544268c090bf12a12aba2e1fe908e680bd84121078493a44`  
		Last Modified: Fri, 06 Sep 2024 23:17:43 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d580133230e25693533e6667d990b3cb77d3d04b8dc757e2e80d30b0b5e6f8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 KB (153176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6970303d5fa6fc06468129aed534dca0d9cf4f28735757fb534a225b052622e7`

```dockerfile
```

-	Layers:
	-	`sha256:1f633f4305ad71fbcab58f89a16a9a558b51ebc891f7dd5dd906beecf88601a6`  
		Last Modified: Fri, 06 Sep 2024 23:17:43 GMT  
		Size: 136.0 KB (136039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e817be8d5d55f1b25595aeebae172ea3d367c5bdb3a7eb830a822dcc7c55153`  
		Last Modified: Fri, 06 Sep 2024 23:17:43 GMT  
		Size: 17.1 KB (17137 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:0b228dceaa39d65a1164b51d637377b4a05a6eee934ea39ea7ebc9405313aaa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17927129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e295197fc40132cedd4041ca86595f85980c04ae3609464083b1b71482fd3be3`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 15:45:15 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV EGGDROP_SHA256=d185512ad282aeee49a75328e847f604c762e94be19fb1e01a7e8a4f927730b8
# Thu, 08 Aug 2024 15:45:15 GMT
ENV EGGDROP_COMMIT=f80f8ae468fd7bcec83407134ef5941225131104
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:45:15 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:45:15 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:45:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:45:15 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:45:15 GMT
COPY entrypoint.sh ./ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
COPY docker.tcl ./scripts/ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515d11fe5ed07f0771a0f823866375c1d173ce2c6c82575208e8c39a43ec7020`  
		Last Modified: Fri, 06 Sep 2024 21:03:15 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3abe0d0188fbfa3e981d45905f4897f98d4b70258463b3c7a5faac03f562eea`  
		Last Modified: Fri, 06 Sep 2024 21:03:15 GMT  
		Size: 3.1 MB (3075692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80966a853bb829892668f068520e8474fe64bfddf4e98df32577efcc88fa58d`  
		Last Modified: Fri, 06 Sep 2024 21:03:16 GMT  
		Size: 11.5 MB (11482176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a80597857fdde4477dd87a5d9bd022a95f1624c45fdb75030e38c60ebfa0d6`  
		Last Modified: Fri, 06 Sep 2024 21:03:15 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72adf7a86ef79aaa59b4d0ecf87669aba3b0de286e7600fbeaf0592a7130ec19`  
		Last Modified: Fri, 06 Sep 2024 21:03:16 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:f885eecd896d17b6651b131f73c423f62ea863bc3392031b17237bce91193246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (16990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428cb074ab6c258cca15e2dd248b8b6567521235bcfe9456a5c02d8e5c386c`

```dockerfile
```

-	Layers:
	-	`sha256:ee5ae62a4a61c021426de7b4f4dccc49c7887ec520c8a75e4c9f63bea8f8cdc1`  
		Last Modified: Fri, 06 Sep 2024 21:03:15 GMT  
		Size: 17.0 KB (16990 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:10404346ebe84c0a3e1284c1520f9f5bfb028da95b652ff475320321c950b180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19691828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04faecc878c513320b7b2dd111aa0936379a3a9a7e47ac2531449f77dc7c3ce8`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Thu, 08 Aug 2024 15:45:15 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV EGGDROP_SHA256=d185512ad282aeee49a75328e847f604c762e94be19fb1e01a7e8a4f927730b8
# Thu, 08 Aug 2024 15:45:15 GMT
ENV EGGDROP_COMMIT=f80f8ae468fd7bcec83407134ef5941225131104
# Thu, 08 Aug 2024 15:45:15 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.13-src.tar.gz" -O tcl8.6.13-src.tar.gz --progress=dot:giga   && tar -zxf tcl8.6.13-src.tar.gz   && ( cd tcl8.6.13     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl8.6.13-src.tar.gz   && rm -rf tcl8.6.13   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENV NICK=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV SERVER=
# Thu, 08 Aug 2024 15:45:15 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 15:45:15 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 15:45:15 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 15:45:15 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 15:45:15 GMT
EXPOSE map[3333/tcp:{}]
# Thu, 08 Aug 2024 15:45:15 GMT
COPY entrypoint.sh ./ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
COPY docker.tcl ./scripts/ # buildkit
# Thu, 08 Aug 2024 15:45:15 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 15:45:15 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0202e46c7eaaa3458319ea625e1b1f0f395e4f26ea1c18d8499037c9a6b52b8a`  
		Last Modified: Fri, 06 Sep 2024 21:53:05 GMT  
		Size: 969.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d90021f9b06c4f6889543781e83377c49ee76d2e58106decd025eabaa9e181`  
		Last Modified: Fri, 06 Sep 2024 21:53:06 GMT  
		Size: 3.9 MB (3899862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c66e69595c791ff1bb0e6b981a48f8f1c24365372f8b7f558ae7fbb627fcb5`  
		Last Modified: Fri, 06 Sep 2024 21:53:07 GMT  
		Size: 11.7 MB (11700962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d12e9f784ce42ad980c85295ea3eb3144c5464de595c044fb9fed4d83b4eb72`  
		Last Modified: Fri, 06 Sep 2024 21:53:06 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e6facd6c5699da79c670cac9dfc3e5c487f6f775d9991e956a770b2c46c72`  
		Last Modified: Fri, 06 Sep 2024 21:53:06 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:61c1e9cf583c20b4ac97351ef7eb2cda57eef37855fc7e606c2339ffcd61d7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 KB (153460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04293dbf50e139e1331444b5ef75e5cec396b4754eb80e9b3e3e1c68ea254ac`

```dockerfile
```

-	Layers:
	-	`sha256:afcb3c8b3e4fcc113af26ffa6e6746ca6d2af83ceb11d2ce812d3431e3217135`  
		Last Modified: Fri, 06 Sep 2024 21:53:05 GMT  
		Size: 136.1 KB (136059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d2054ca69dda263c3d356f0a25380012fd5c4f9f87129a0846b6a509e5d8491`  
		Last Modified: Fri, 06 Sep 2024 21:53:05 GMT  
		Size: 17.4 KB (17401 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:dfdff3fc1468d8ca30be6b70fc9b72c8d0f51a00f73015cbff995b2a628a7118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:464fa69cb45f5509980cd7b70bdf33209d893d95c3fd4e1a4cd6a2e1416564f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12298795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d06db72b6c7a18beee096a1b8fba98574219450ef740740bcce13e71ef7e771`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97044ed21665bdc39e4fb6615c274aed679f6b8f55e5465fae4f555719965f9b`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687876d96a0d41fb3e048eac436131b2b6815643c88e7bd077811d7b63bddc04`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 10.8 KB (10830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7353807a5a9d0ab0b70534e9de509c882d3c03958adccae7962bab12d41a030f`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 2.9 MB (2900184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab05178db53ad0b2b8818dbb268a624880309ac9d286fc96d24df5b593b348b`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 6.0 MB (5964265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102028674158922bccbfdcd6d7ea8994766105a27d363f4f71273a20d0010fd`  
		Last Modified: Fri, 06 Sep 2024 23:18:46 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a05837526fe00223759e8d4a997d16345eadd06e863fa822ff79f7b5243343`  
		Last Modified: Fri, 06 Sep 2024 23:18:46 GMT  
		Size: 699.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:cf8a57886874429df642e8168365c3ecb7a063d42bb23e7f1f2c1e19dc68cd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93173c29b543a157fcdd4fbac48cdaf4aca24e2c09177e19d20f7987b6e468c`

```dockerfile
```

-	Layers:
	-	`sha256:bfa78d355a05f618bcb520a2ee2043fa052ec431140c725530bf4ad0b42484c1`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 1.0 MB (1044135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2336848c7176ed259cdb0ee73a90625f3667393472804f7ec51bc8d9841dbda2`  
		Last Modified: Fri, 06 Sep 2024 23:18:44 GMT  
		Size: 19.7 KB (19747 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:03e1314ed57502af97e01e97c0530d74d0f81f18ff9c53ecd3b5cace76bfe7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13701136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e664fe986d5565c68c790bb5b1e86fbb994d849c253e356ee2e98184ae1dd6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
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
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dcb41c61459f2a403456e5891620aef35c65ef74050994aad2af1ab6e621b6`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fb7c554f9f18b4618cc72ab1fed00f4121ad7e1f19cb89319885fea95384e`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 11.0 KB (10961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e65e8815edf970cf2b1ba307821854aba8a638c33dc95e77482ca36a3bb36b`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 4.7 MB (4651897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b62939420f89f5597cd9908110297efcce3d765484ff819723acdf395f9385`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 5.9 MB (5858807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49a673f5e0325c4cc20f8ca46ea2efa50c34eed5724a10f2cb17c838b5b5e93`  
		Last Modified: Fri, 06 Sep 2024 21:08:40 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b304f35d5545678f352755b28b9b4e423273fd847dd98fce2d02d2996c44af79`  
		Last Modified: Fri, 06 Sep 2024 21:08:40 GMT  
		Size: 696.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:bb3ced9249e06c250f433eace6c28018f6213010a13281ac9a3738be6f8d9a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1528fc5c91f6e1fe0cde4e03a377210ac3235b05dcee62afd9dab11d0c504d5e`

```dockerfile
```

-	Layers:
	-	`sha256:4b7c8ae76836ae228ff763e3141b1f28fb9911025ac4aa9e2a8c2e8f24463546`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 19.6 KB (19637 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:64166b3cf2df01a17e431db880b621810acda5b0fd0ddbba6ba59105e2b82fd8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12424083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d293d71c94643df7ec3252594eca670575e13b9d2d9c0bf18a71aea03b02a8d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:45:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 19:45:45 GMT
RUN adduser -S eggdrop
# Thu, 08 Aug 2024 19:45:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 08 Aug 2024 19:45:48 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 08 Aug 2024 19:49:18 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 08 Aug 2024 19:49:18 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:49:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 19:49:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:49:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:49:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:49:19 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 08 Aug 2024 19:49:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:49:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3af4066f123f44c2fb98e2f28964f982bc14db4ba15906ad8cc3887a867266`  
		Last Modified: Thu, 08 Aug 2024 19:52:03 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ccffd445d45c37456f285a0ce2105caf980a691a88a750da9d0b219b008a86`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 11.4 KB (11395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0587e228beafa54aa50b93967977861c70914e0ddedcd401e31b42fd0c0e733`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 3.0 MB (3034852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dfbf35befd934b3269c7f9f9c391974da4d1dca33f36515bd2dfa7352f5d1e`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 6.0 MB (6015601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6a4d43f2f43e12cbd85ae7f616403e0c64a507c111410e4fa39fb99153592`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae77733354b0d53d2c6134cf545bf14ed540dec92c819344b15a4ab36c0a228c`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:dfdff3fc1468d8ca30be6b70fc9b72c8d0f51a00f73015cbff995b2a628a7118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8

### `eggdrop:stable` - linux; amd64

```console
$ docker pull eggdrop@sha256:464fa69cb45f5509980cd7b70bdf33209d893d95c3fd4e1a4cd6a2e1416564f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12298795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d06db72b6c7a18beee096a1b8fba98574219450ef740740bcce13e71ef7e771`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 08 Aug 2024 15:14:19 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97044ed21665bdc39e4fb6615c274aed679f6b8f55e5465fae4f555719965f9b`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687876d96a0d41fb3e048eac436131b2b6815643c88e7bd077811d7b63bddc04`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 10.8 KB (10830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7353807a5a9d0ab0b70534e9de509c882d3c03958adccae7962bab12d41a030f`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 2.9 MB (2900184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab05178db53ad0b2b8818dbb268a624880309ac9d286fc96d24df5b593b348b`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 6.0 MB (5964265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e102028674158922bccbfdcd6d7ea8994766105a27d363f4f71273a20d0010fd`  
		Last Modified: Fri, 06 Sep 2024 23:18:46 GMT  
		Size: 1.8 KB (1831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a05837526fe00223759e8d4a997d16345eadd06e863fa822ff79f7b5243343`  
		Last Modified: Fri, 06 Sep 2024 23:18:46 GMT  
		Size: 699.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:cf8a57886874429df642e8168365c3ecb7a063d42bb23e7f1f2c1e19dc68cd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93173c29b543a157fcdd4fbac48cdaf4aca24e2c09177e19d20f7987b6e468c`

```dockerfile
```

-	Layers:
	-	`sha256:bfa78d355a05f618bcb520a2ee2043fa052ec431140c725530bf4ad0b42484c1`  
		Last Modified: Fri, 06 Sep 2024 23:18:45 GMT  
		Size: 1.0 MB (1044135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2336848c7176ed259cdb0ee73a90625f3667393472804f7ec51bc8d9841dbda2`  
		Last Modified: Fri, 06 Sep 2024 23:18:44 GMT  
		Size: 19.7 KB (19747 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:03e1314ed57502af97e01e97c0530d74d0f81f18ff9c53ecd3b5cace76bfe7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13701136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e664fe986d5565c68c790bb5b1e86fbb994d849c253e356ee2e98184ae1dd6`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:22 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
# Mon, 22 Jul 2024 21:49:22 GMT
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
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dcb41c61459f2a403456e5891620aef35c65ef74050994aad2af1ab6e621b6`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961fb7c554f9f18b4618cc72ab1fed00f4121ad7e1f19cb89319885fea95384e`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 11.0 KB (10961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e65e8815edf970cf2b1ba307821854aba8a638c33dc95e77482ca36a3bb36b`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 4.7 MB (4651897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b62939420f89f5597cd9908110297efcce3d765484ff819723acdf395f9385`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 5.9 MB (5858807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49a673f5e0325c4cc20f8ca46ea2efa50c34eed5724a10f2cb17c838b5b5e93`  
		Last Modified: Fri, 06 Sep 2024 21:08:40 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b304f35d5545678f352755b28b9b4e423273fd847dd98fce2d02d2996c44af79`  
		Last Modified: Fri, 06 Sep 2024 21:08:40 GMT  
		Size: 696.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:bb3ced9249e06c250f433eace6c28018f6213010a13281ac9a3738be6f8d9a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 KB (19637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1528fc5c91f6e1fe0cde4e03a377210ac3235b05dcee62afd9dab11d0c504d5e`

```dockerfile
```

-	Layers:
	-	`sha256:4b7c8ae76836ae228ff763e3141b1f28fb9911025ac4aa9e2a8c2e8f24463546`  
		Last Modified: Fri, 06 Sep 2024 21:08:39 GMT  
		Size: 19.6 KB (19637 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:64166b3cf2df01a17e431db880b621810acda5b0fd0ddbba6ba59105e2b82fd8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12424083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d293d71c94643df7ec3252594eca670575e13b9d2d9c0bf18a71aea03b02a8d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:18 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Mon, 22 Jul 2024 21:44:18 GMT
CMD ["/bin/sh"]
# Thu, 08 Aug 2024 19:45:45 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Thu, 08 Aug 2024 19:45:45 GMT
RUN adduser -S eggdrop
# Thu, 08 Aug 2024 19:45:47 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Thu, 08 Aug 2024 19:45:48 GMT
RUN apk add --no-cache tcl bash openssl
# Thu, 08 Aug 2024 19:49:18 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl8.6.12-src.tar.gz" -O tcl8.6.12-src.tar.gz   && tar -zxf tcl8.6.12-src.tar.gz   && ( cd tcl8.6.12     && sed -i "/define TCL_UTF_MAX/c\#define TCL_UTF_MAX 6" generic/tcl.h     && cd unix     && ./configure     && make     && make install )   && rm tcl8.6.12-src.tar.gz   && rm -rf tcl8.6.12   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.9/eggdrop-1.9.5.tar.gz.asc   && gpg --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.9.5.tar.gz.asc eggdrop-1.9.5.tar.gz   && command -v gpgconf > /dev/null   && gpgconf --kill all   && rm eggdrop-1.9.5.tar.gz.asc   && tar -zxvf eggdrop-1.9.5.tar.gz   && rm eggdrop-1.9.5.tar.gz   && ( cd eggdrop-1.9.5     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.9.5   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Thu, 08 Aug 2024 19:49:18 GMT
ENV NICK=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV SERVER=
# Thu, 08 Aug 2024 19:49:18 GMT
ENV LISTEN=3333
# Thu, 08 Aug 2024 19:49:19 GMT
ENV OWNER=
# Thu, 08 Aug 2024 19:49:19 GMT
ENV USERFILE=eggdrop.user
# Thu, 08 Aug 2024 19:49:19 GMT
ENV CHANFILE=eggdrop.chan
# Thu, 08 Aug 2024 19:49:19 GMT
WORKDIR /home/eggdrop/eggdrop
# Thu, 08 Aug 2024 19:49:19 GMT
EXPOSE 3333
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:ddb4d88d0de0ae2531972fbd491e6c611f0bb89ff8457bc01e4e61ae7f66cd46 in /home/eggdrop/eggdrop 
# Thu, 08 Aug 2024 19:49:19 GMT
COPY file:b76e92fb28997fa3fd71a3b880ff3b73567ca05021b617d51ebdcefd8c31b457 in /home/eggdrop/eggdrop/scripts/ 
# Thu, 08 Aug 2024 19:49:19 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Thu, 08 Aug 2024 19:49:19 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3af4066f123f44c2fb98e2f28964f982bc14db4ba15906ad8cc3887a867266`  
		Last Modified: Thu, 08 Aug 2024 19:52:03 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ccffd445d45c37456f285a0ce2105caf980a691a88a750da9d0b219b008a86`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 11.4 KB (11395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0587e228beafa54aa50b93967977861c70914e0ddedcd401e31b42fd0c0e733`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 3.0 MB (3034852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dfbf35befd934b3269c7f9f9c391974da4d1dca33f36515bd2dfa7352f5d1e`  
		Last Modified: Thu, 08 Aug 2024 19:52:02 GMT  
		Size: 6.0 MB (6015601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d6a4d43f2f43e12cbd85ae7f616403e0c64a507c111410e4fa39fb99153592`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae77733354b0d53d2c6134cf545bf14ed540dec92c819344b15a4ab36c0a228c`  
		Last Modified: Thu, 08 Aug 2024 19:52:01 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
