<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `eggdrop`

-	[`eggdrop:1.10`](#eggdrop110)
-	[`eggdrop:1.10.1`](#eggdrop1101)
-	[`eggdrop:develop`](#eggdropdevelop)
-	[`eggdrop:latest`](#eggdroplatest)
-	[`eggdrop:stable`](#eggdropstable)

## `eggdrop:1.10`

```console
$ docker pull eggdrop@sha256:2028d25c44a8fa7dbbfee1e1c9db809c5ba23eaa6516fbe84eb86c44886e1e04
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
$ docker pull eggdrop@sha256:64da7a09d997e3b03ce2bd030fa54d14325da63f7df7391570e074fd5bd1f1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12802733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718de2fa6c06b5129ac5a811dc8441b23bb94c98231b303ac02f9ccbd5cb2c20`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:18 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 17 Apr 2026 00:15:18 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Fri, 17 Apr 2026 00:15:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
ENV NICK=
# Fri, 17 Apr 2026 00:18:32 GMT
ENV SERVER=
# Fri, 17 Apr 2026 00:18:32 GMT
ENV LISTEN=3333
# Fri, 17 Apr 2026 00:18:32 GMT
ENV USERFILE=eggdrop.user
# Fri, 17 Apr 2026 00:18:32 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 17 Apr 2026 00:18:32 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 17 Apr 2026 00:18:32 GMT
EXPOSE map[3333/tcp:{}]
# Fri, 17 Apr 2026 00:18:32 GMT
COPY entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
COPY docker.tcl ./scripts/ # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 17 Apr 2026 00:18:32 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f339cba84b981e1992cc557fb400cce5b960817ef6a6ea37d3679e32151c52d`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b54844e2f73941a03f5f1377b0108c701158c0206eadc611f9f0cde58cfd62`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 1.1 MB (1116762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f1258ab988d483973ca23059dfec49d66ea59ba160c20334542ca1dd7da1a8`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 8.0 MB (8035037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7d1919a67ebb69f4e586c1dd8cecb6332dee411ca6337a373011a666e2cdc`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3eae19d9f3bea0db98992720d3ca3ad36feb9b14d3aaccaeaa5d322e90f10`  
		Last Modified: Fri, 17 Apr 2026 00:18:39 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:1e16c97c5e56cc6861f6cc7fabc9a4a7a177078ad500159acd8f2108f30b58f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 KB (163325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36970bc6aaf3d383125e9b85289878fef3922f9d720404cd8c9b8753dd0dfa10`

```dockerfile
```

-	Layers:
	-	`sha256:ed8e5fe0d625549d9a976cd4048647e39ad76f3555e48ea0e4109bc60c28b960`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 145.0 KB (144975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdc2afd18987a9aa8aae1747b837845425d0a1289ce2f77ba657da307910f96`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5aca1ce17d31254d25f5dd5123df2b5fbb8a7ba5d4191b4df1a9e0ee96cd3175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12355218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3761451ba6fa939892112f0a02ba6fb597d891bcf3ed467e3ded6545ac9bec4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:38 GMT
ADD alpine-minirootfs-3.21.7-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:38 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:52 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 17 Apr 2026 00:14:52 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Fri, 17 Apr 2026 00:14:53 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Fri, 17 Apr 2026 00:19:41 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Fri, 17 Apr 2026 00:19:41 GMT
ENV NICK=
# Fri, 17 Apr 2026 00:19:41 GMT
ENV SERVER=
# Fri, 17 Apr 2026 00:19:41 GMT
ENV LISTEN=3333
# Fri, 17 Apr 2026 00:19:41 GMT
ENV USERFILE=eggdrop.user
# Fri, 17 Apr 2026 00:19:41 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 17 Apr 2026 00:19:41 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 17 Apr 2026 00:19:41 GMT
EXPOSE map[3333/tcp:{}]
# Fri, 17 Apr 2026 00:19:41 GMT
COPY entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:19:42 GMT
COPY docker.tcl ./scripts/ # buildkit
# Fri, 17 Apr 2026 00:19:42 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:42 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:f204fe7ddd292eb5d783ce14a8bc6c5a7defbb8adda2989da2c9dcf46b3e08e9`  
		Last Modified: Thu, 16 Apr 2026 23:53:42 GMT  
		Size: 3.4 MB (3369055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c374072ba32c01442f0bc881932103e1d3772d2bc00e8b062c7092cdc2e68`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a3fc78f147be0a6f75404b2223e3a66d9ed97bc8b88511cefff87c7fc3feb`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 1.1 MB (1129838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdae370e1d341a287804a804d34cc0acf80fd3cd119915268293b2d8ac176af8`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 7.9 MB (7852263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5c85741ba086a4b4bd0655ce6c6b9a28480970380dc9c143ce66d52d1a7cd1`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9ed8de466fe06402cb0fb11c925eb41da881155504ec1494fdc22c7694858c`  
		Last Modified: Fri, 17 Apr 2026 00:19:47 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:46de0444f5f0c5c64594207ffcf40cf79435a1e2d46ae6383bdb9d9a3bee73dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1185ee92ea1edfb662c66c485d29f135e59c101fd60fd7a0596e32a72008d077`

```dockerfile
```

-	Layers:
	-	`sha256:30709a5fd6cd3680779b0fb002e97d206a56433cf499550f767302d490ab0971`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 18.2 KB (18241 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2f41546c2c21a00307692dfacbe19b20b998c5c97248e0396c7285f504d9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13249767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb801cf5db8a542234bffb3b06d94385d41b5bade14ecc8ec7d4483d3e2bb26`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:47 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 17 Apr 2026 00:14:47 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Fri, 17 Apr 2026 00:14:48 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
ENV NICK=
# Fri, 17 Apr 2026 00:18:39 GMT
ENV SERVER=
# Fri, 17 Apr 2026 00:18:39 GMT
ENV LISTEN=3333
# Fri, 17 Apr 2026 00:18:39 GMT
ENV USERFILE=eggdrop.user
# Fri, 17 Apr 2026 00:18:39 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 17 Apr 2026 00:18:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 17 Apr 2026 00:18:39 GMT
EXPOSE map[3333/tcp:{}]
# Fri, 17 Apr 2026 00:18:39 GMT
COPY entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
COPY docker.tcl ./scripts/ # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 17 Apr 2026 00:18:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aa8e6d9529a22c42f62c196fbc14cff0b4b2f6f85731dc47791a26659a0f9d`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc20d43f4a698300a2fbd826d527be10d6228ff9e8e1fbe1641919449130ed2`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 1.2 MB (1171093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1e830796510795845e0874861d3017366dc761d855737f34104efb97f6cd9c`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 8.1 MB (8080153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5637df7552f34e0e16cc0e36d7ed5cd368a17cb61e1cfd7c45bc37cc84902faa`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78a01f4a689ba4d7fceb47a6386bacf8976ecd594b007f7e718bb9d152291b9`  
		Last Modified: Fri, 17 Apr 2026 00:18:46 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10` - unknown; unknown

```console
$ docker pull eggdrop@sha256:7b637fff83800b96b44a4bf88901779d06ead891ad3c150efd2d1605c0b88b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 KB (163515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd92da4846368041b6d4b65f9427406d8519e4373ccccd579a5b67c6106974f3`

```dockerfile
```

-	Layers:
	-	`sha256:005cad79de2c194f7f0f289f6ef0f8dde0aa123cd07299fa56b8f2724a2fbac3`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 145.0 KB (145031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b6dcbdb96fd698ddce7932c0f6009c0e06335c648bb933017f918fded4ebfe`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 18.5 KB (18484 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:1.10.1`

```console
$ docker pull eggdrop@sha256:2028d25c44a8fa7dbbfee1e1c9db809c5ba23eaa6516fbe84eb86c44886e1e04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `eggdrop:1.10.1` - linux; amd64

```console
$ docker pull eggdrop@sha256:64da7a09d997e3b03ce2bd030fa54d14325da63f7df7391570e074fd5bd1f1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12802733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718de2fa6c06b5129ac5a811dc8441b23bb94c98231b303ac02f9ccbd5cb2c20`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:18 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 17 Apr 2026 00:15:18 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Fri, 17 Apr 2026 00:15:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
ENV NICK=
# Fri, 17 Apr 2026 00:18:32 GMT
ENV SERVER=
# Fri, 17 Apr 2026 00:18:32 GMT
ENV LISTEN=3333
# Fri, 17 Apr 2026 00:18:32 GMT
ENV USERFILE=eggdrop.user
# Fri, 17 Apr 2026 00:18:32 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 17 Apr 2026 00:18:32 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 17 Apr 2026 00:18:32 GMT
EXPOSE map[3333/tcp:{}]
# Fri, 17 Apr 2026 00:18:32 GMT
COPY entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
COPY docker.tcl ./scripts/ # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 17 Apr 2026 00:18:32 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f339cba84b981e1992cc557fb400cce5b960817ef6a6ea37d3679e32151c52d`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b54844e2f73941a03f5f1377b0108c701158c0206eadc611f9f0cde58cfd62`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 1.1 MB (1116762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f1258ab988d483973ca23059dfec49d66ea59ba160c20334542ca1dd7da1a8`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 8.0 MB (8035037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7d1919a67ebb69f4e586c1dd8cecb6332dee411ca6337a373011a666e2cdc`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3eae19d9f3bea0db98992720d3ca3ad36feb9b14d3aaccaeaa5d322e90f10`  
		Last Modified: Fri, 17 Apr 2026 00:18:39 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:1e16c97c5e56cc6861f6cc7fabc9a4a7a177078ad500159acd8f2108f30b58f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 KB (163325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36970bc6aaf3d383125e9b85289878fef3922f9d720404cd8c9b8753dd0dfa10`

```dockerfile
```

-	Layers:
	-	`sha256:ed8e5fe0d625549d9a976cd4048647e39ad76f3555e48ea0e4109bc60c28b960`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 145.0 KB (144975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdc2afd18987a9aa8aae1747b837845425d0a1289ce2f77ba657da307910f96`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.1` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5aca1ce17d31254d25f5dd5123df2b5fbb8a7ba5d4191b4df1a9e0ee96cd3175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12355218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3761451ba6fa939892112f0a02ba6fb597d891bcf3ed467e3ded6545ac9bec4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:38 GMT
ADD alpine-minirootfs-3.21.7-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:38 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:52 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 17 Apr 2026 00:14:52 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Fri, 17 Apr 2026 00:14:53 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Fri, 17 Apr 2026 00:19:41 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Fri, 17 Apr 2026 00:19:41 GMT
ENV NICK=
# Fri, 17 Apr 2026 00:19:41 GMT
ENV SERVER=
# Fri, 17 Apr 2026 00:19:41 GMT
ENV LISTEN=3333
# Fri, 17 Apr 2026 00:19:41 GMT
ENV USERFILE=eggdrop.user
# Fri, 17 Apr 2026 00:19:41 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 17 Apr 2026 00:19:41 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 17 Apr 2026 00:19:41 GMT
EXPOSE map[3333/tcp:{}]
# Fri, 17 Apr 2026 00:19:41 GMT
COPY entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:19:42 GMT
COPY docker.tcl ./scripts/ # buildkit
# Fri, 17 Apr 2026 00:19:42 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:42 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:f204fe7ddd292eb5d783ce14a8bc6c5a7defbb8adda2989da2c9dcf46b3e08e9`  
		Last Modified: Thu, 16 Apr 2026 23:53:42 GMT  
		Size: 3.4 MB (3369055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c374072ba32c01442f0bc881932103e1d3772d2bc00e8b062c7092cdc2e68`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a3fc78f147be0a6f75404b2223e3a66d9ed97bc8b88511cefff87c7fc3feb`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 1.1 MB (1129838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdae370e1d341a287804a804d34cc0acf80fd3cd119915268293b2d8ac176af8`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 7.9 MB (7852263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5c85741ba086a4b4bd0655ce6c6b9a28480970380dc9c143ce66d52d1a7cd1`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9ed8de466fe06402cb0fb11c925eb41da881155504ec1494fdc22c7694858c`  
		Last Modified: Fri, 17 Apr 2026 00:19:47 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:46de0444f5f0c5c64594207ffcf40cf79435a1e2d46ae6383bdb9d9a3bee73dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1185ee92ea1edfb662c66c485d29f135e59c101fd60fd7a0596e32a72008d077`

```dockerfile
```

-	Layers:
	-	`sha256:30709a5fd6cd3680779b0fb002e97d206a56433cf499550f767302d490ab0971`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 18.2 KB (18241 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:1.10.1` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2f41546c2c21a00307692dfacbe19b20b998c5c97248e0396c7285f504d9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13249767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb801cf5db8a542234bffb3b06d94385d41b5bade14ecc8ec7d4483d3e2bb26`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:47 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 17 Apr 2026 00:14:47 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Fri, 17 Apr 2026 00:14:48 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
ENV NICK=
# Fri, 17 Apr 2026 00:18:39 GMT
ENV SERVER=
# Fri, 17 Apr 2026 00:18:39 GMT
ENV LISTEN=3333
# Fri, 17 Apr 2026 00:18:39 GMT
ENV USERFILE=eggdrop.user
# Fri, 17 Apr 2026 00:18:39 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 17 Apr 2026 00:18:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 17 Apr 2026 00:18:39 GMT
EXPOSE map[3333/tcp:{}]
# Fri, 17 Apr 2026 00:18:39 GMT
COPY entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
COPY docker.tcl ./scripts/ # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 17 Apr 2026 00:18:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aa8e6d9529a22c42f62c196fbc14cff0b4b2f6f85731dc47791a26659a0f9d`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc20d43f4a698300a2fbd826d527be10d6228ff9e8e1fbe1641919449130ed2`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 1.2 MB (1171093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1e830796510795845e0874861d3017366dc761d855737f34104efb97f6cd9c`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 8.1 MB (8080153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5637df7552f34e0e16cc0e36d7ed5cd368a17cb61e1cfd7c45bc37cc84902faa`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78a01f4a689ba4d7fceb47a6386bacf8976ecd594b007f7e718bb9d152291b9`  
		Last Modified: Fri, 17 Apr 2026 00:18:46 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:1.10.1` - unknown; unknown

```console
$ docker pull eggdrop@sha256:7b637fff83800b96b44a4bf88901779d06ead891ad3c150efd2d1605c0b88b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 KB (163515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd92da4846368041b6d4b65f9427406d8519e4373ccccd579a5b67c6106974f3`

```dockerfile
```

-	Layers:
	-	`sha256:005cad79de2c194f7f0f289f6ef0f8dde0aa123cd07299fa56b8f2724a2fbac3`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 145.0 KB (145031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b6dcbdb96fd698ddce7932c0f6009c0e06335c648bb933017f918fded4ebfe`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 18.5 KB (18484 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:develop`

```console
$ docker pull eggdrop@sha256:666e4a892765cda5c7c970df1af74a2a39fc8d666eb589dd7051da729fb277e8
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
$ docker pull eggdrop@sha256:e9950121ce910ba4202bad49480397ca324582ab5e488d198c40b19dd29d6713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11287423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b54173944d710f2d965fe321e1df5aa13d39e7b212cb477483bd6e6a1b0443d`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:13:43 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:13:43 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:13:45 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl tcl9 tcl9-dev # buildkit
# Wed, 15 Apr 2026 23:13:45 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Wed, 15 Apr 2026 23:13:45 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Wed, 15 Apr 2026 23:14:01 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:14:01 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:14:01 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:14:01 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:14:01 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:14:01 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:14:01 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:14:01 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:14:01 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:14:01 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:14:01 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:14:01 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d3f36bc274178e9cf0c997c9995ccae73b4483b90dc54812a57e09e58046a1`  
		Last Modified: Wed, 15 Apr 2026 23:14:07 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f29b577422ce2a44c969d5f946cf87c68ff68076d1d78010f2d2c5c9415ac`  
		Last Modified: Wed, 15 Apr 2026 23:14:07 GMT  
		Size: 4.7 MB (4749966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed8515cc3aa2ef55ff12dbb1b49aa29c23aff53788847667c63efd93d4e7bf9`  
		Last Modified: Wed, 15 Apr 2026 23:14:07 GMT  
		Size: 2.7 MB (2669196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1eec04bdb91d8c45196ec27e91a5f1c33ff97cae6e884d5472c92a5443a6baa`  
		Last Modified: Wed, 15 Apr 2026 23:14:07 GMT  
		Size: 2.0 KB (1963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8136ba79ce0f9fc46d084dccfc5ca0b7d51a4cdffa0f9db244156e6e4f86ab`  
		Last Modified: Wed, 15 Apr 2026 23:14:08 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:d34b0451d989c0795f490f73921baa3e35aa28105ef3d636365953e7e156d4d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **754.0 KB (754019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85d3eb681a399e7aa2394d95f91cb369f47a54899152646aa9b43005c5157ac`

```dockerfile
```

-	Layers:
	-	`sha256:8d18ab7f6050c0bf6a8a11a75e4e7ea14ac7fcdb9217f5b81996b79ac497353e`  
		Last Modified: Wed, 15 Apr 2026 23:14:07 GMT  
		Size: 738.2 KB (738227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe9f1842f8e1a6418f24751c4b4ae2a2c4307abdb88bf47ce573cc46e38fdea2`  
		Last Modified: Wed, 15 Apr 2026 23:14:07 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:0a9fd250fcab458c40735a85e42d6e95b0d63d775afd599b2d5d3f0943173497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10966036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0189d93460064e265df5513975bbffc3378bf4b85555dbdfc0a6b54ecb55b04`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:13:08 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:13:08 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:13:10 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl tcl9 tcl9-dev # buildkit
# Wed, 15 Apr 2026 23:13:10 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Wed, 15 Apr 2026 23:13:10 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Wed, 15 Apr 2026 23:13:30 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:13:30 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:13:30 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:13:30 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:13:30 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:13:30 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:13:31 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:13:31 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:13:31 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:13:31 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:13:31 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:13:31 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5ac7e0d6f968ff7f1963fd26ee579d9958c1bee0d2d5eb55acdaf5d5dd1126`  
		Last Modified: Wed, 15 Apr 2026 23:13:35 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7adba4b481ebecd1aa5ad5ddcd9208d17d014302c93399f60e89165aba3bc0`  
		Last Modified: Wed, 15 Apr 2026 23:13:36 GMT  
		Size: 4.7 MB (4708171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85d4f9a5f70b9df5160b0bafbe61fe83d8a4093998914c54e6711c3482df315`  
		Last Modified: Wed, 15 Apr 2026 23:13:36 GMT  
		Size: 2.7 MB (2681923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031ef5c760f5deaead1ed263ac8ed7fee8b59b5972c6985423643ef5b5869a14`  
		Last Modified: Wed, 15 Apr 2026 23:13:36 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196e78aca3c655572a461d79618618158cfac06449b877ade5987542f0a65b8d`  
		Last Modified: Wed, 15 Apr 2026 23:13:37 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:5857c7c4a8a6c8d948158bf9edc168b9945f6564da05c1420e64fe1034ebbbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 KB (15659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fb3668341d0ccb54bdc157fb98b9d76db15045ab5c9a04fcbdf0b60cd5c33b`

```dockerfile
```

-	Layers:
	-	`sha256:f5bd723bd399876662b1201a5b67868a6f07af8f01e39137bb5ab0d91243abb6`  
		Last Modified: Wed, 15 Apr 2026 23:13:35 GMT  
		Size: 15.7 KB (15659 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:develop` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2c9332a895e9b8a0cc500ccde5c1f1ef252dbdf354468727cdadd67757b6afd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11712810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83526d1b3273ce138fd04307fc90b68a37604dec4a5eaf712ee81952047f5e19`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:13:18 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Wed, 15 Apr 2026 23:13:18 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Wed, 15 Apr 2026 23:13:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl tcl9 tcl9-dev # buildkit
# Wed, 15 Apr 2026 23:13:19 GMT
ENV EGGDROP_SHA256=e42668f102c1446901b066d13fe0bf39622afca8d723f356ac2390d5faaf6e5e
# Wed, 15 Apr 2026 23:13:19 GMT
ENV EGGDROP_COMMIT=541e8ac17e549a40e177b5eea54e4abf24629a33
# Wed, 15 Apr 2026 23:13:35 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://github.com/eggheads/eggdrop/archive/$EGGDROP_COMMIT.tar.gz" -O develop.tar.gz   && echo "$EGGDROP_SHA256 *develop.tar.gz" | sha256sum -c -   && tar -zxf develop.tar.gz   && rm develop.tar.gz     && ( cd eggdrop-$EGGDROP_COMMIT     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-$EGGDROP_COMMIT   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Wed, 15 Apr 2026 23:13:35 GMT
ENV NICK=
# Wed, 15 Apr 2026 23:13:35 GMT
ENV SERVER=
# Wed, 15 Apr 2026 23:13:35 GMT
ENV LISTEN=3333
# Wed, 15 Apr 2026 23:13:35 GMT
ENV USERFILE=eggdrop.user
# Wed, 15 Apr 2026 23:13:35 GMT
ENV CHANFILE=eggdrop.chan
# Wed, 15 Apr 2026 23:13:35 GMT
WORKDIR /home/eggdrop/eggdrop
# Wed, 15 Apr 2026 23:13:35 GMT
EXPOSE map[3333/tcp:{}]
# Wed, 15 Apr 2026 23:13:35 GMT
COPY entrypoint.sh ./ # buildkit
# Wed, 15 Apr 2026 23:13:36 GMT
COPY docker.tcl ./scripts/ # buildkit
# Wed, 15 Apr 2026 23:13:36 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Wed, 15 Apr 2026 23:13:36 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0917f956f3193e362e9996b0aaf09dfcbec0dd4237ec2b5586573c8ad3d12300`  
		Last Modified: Wed, 15 Apr 2026 23:13:41 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f134e415348636293acd9fb5208ff982aaab8ffb1b9ade56a98396a8341732`  
		Last Modified: Wed, 15 Apr 2026 23:13:41 GMT  
		Size: 4.8 MB (4823830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c981992008899ae79291752bebfcf3e31ee3ab8fd8acb29ede1d35cf4746d6`  
		Last Modified: Wed, 15 Apr 2026 23:13:41 GMT  
		Size: 2.7 MB (2685032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3727664a4c7d8f3e385cd64bd918176db313d61d3d92239adb0c837994001c`  
		Last Modified: Wed, 15 Apr 2026 23:13:41 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acedb75c1470eb5b6132f256ccfb72bf3690eb28c816e1a485163f4650f42cd`  
		Last Modified: Wed, 15 Apr 2026 23:13:42 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:develop` - unknown; unknown

```console
$ docker pull eggdrop@sha256:cbe0b6a7ff924773eb2d6e31c5c853385cd434b14727163c10e1def4e208da6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.5 KB (753486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a98fb89a483b596747ffcc7616399dae88c944ce937478e178dbb4214c1077`

```dockerfile
```

-	Layers:
	-	`sha256:9dda099678bfba2422cf3d1510550671a2ae23b9485830b25af0c5c266af858a`  
		Last Modified: Wed, 15 Apr 2026 23:13:41 GMT  
		Size: 737.6 KB (737597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb426b300dfc66628ab8ddf6389d6b207dc8746ff469e1031db48a0b9799c3a6`  
		Last Modified: Wed, 15 Apr 2026 23:13:41 GMT  
		Size: 15.9 KB (15889 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:2028d25c44a8fa7dbbfee1e1c9db809c5ba23eaa6516fbe84eb86c44886e1e04
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
$ docker pull eggdrop@sha256:64da7a09d997e3b03ce2bd030fa54d14325da63f7df7391570e074fd5bd1f1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12802733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718de2fa6c06b5129ac5a811dc8441b23bb94c98231b303ac02f9ccbd5cb2c20`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:18 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 17 Apr 2026 00:15:18 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Fri, 17 Apr 2026 00:15:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
ENV NICK=
# Fri, 17 Apr 2026 00:18:32 GMT
ENV SERVER=
# Fri, 17 Apr 2026 00:18:32 GMT
ENV LISTEN=3333
# Fri, 17 Apr 2026 00:18:32 GMT
ENV USERFILE=eggdrop.user
# Fri, 17 Apr 2026 00:18:32 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 17 Apr 2026 00:18:32 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 17 Apr 2026 00:18:32 GMT
EXPOSE map[3333/tcp:{}]
# Fri, 17 Apr 2026 00:18:32 GMT
COPY entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
COPY docker.tcl ./scripts/ # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 17 Apr 2026 00:18:32 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f339cba84b981e1992cc557fb400cce5b960817ef6a6ea37d3679e32151c52d`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b54844e2f73941a03f5f1377b0108c701158c0206eadc611f9f0cde58cfd62`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 1.1 MB (1116762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f1258ab988d483973ca23059dfec49d66ea59ba160c20334542ca1dd7da1a8`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 8.0 MB (8035037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7d1919a67ebb69f4e586c1dd8cecb6332dee411ca6337a373011a666e2cdc`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3eae19d9f3bea0db98992720d3ca3ad36feb9b14d3aaccaeaa5d322e90f10`  
		Last Modified: Fri, 17 Apr 2026 00:18:39 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:1e16c97c5e56cc6861f6cc7fabc9a4a7a177078ad500159acd8f2108f30b58f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 KB (163325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36970bc6aaf3d383125e9b85289878fef3922f9d720404cd8c9b8753dd0dfa10`

```dockerfile
```

-	Layers:
	-	`sha256:ed8e5fe0d625549d9a976cd4048647e39ad76f3555e48ea0e4109bc60c28b960`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 145.0 KB (144975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdc2afd18987a9aa8aae1747b837845425d0a1289ce2f77ba657da307910f96`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5aca1ce17d31254d25f5dd5123df2b5fbb8a7ba5d4191b4df1a9e0ee96cd3175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12355218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3761451ba6fa939892112f0a02ba6fb597d891bcf3ed467e3ded6545ac9bec4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:38 GMT
ADD alpine-minirootfs-3.21.7-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:38 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:52 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 17 Apr 2026 00:14:52 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Fri, 17 Apr 2026 00:14:53 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Fri, 17 Apr 2026 00:19:41 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Fri, 17 Apr 2026 00:19:41 GMT
ENV NICK=
# Fri, 17 Apr 2026 00:19:41 GMT
ENV SERVER=
# Fri, 17 Apr 2026 00:19:41 GMT
ENV LISTEN=3333
# Fri, 17 Apr 2026 00:19:41 GMT
ENV USERFILE=eggdrop.user
# Fri, 17 Apr 2026 00:19:41 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 17 Apr 2026 00:19:41 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 17 Apr 2026 00:19:41 GMT
EXPOSE map[3333/tcp:{}]
# Fri, 17 Apr 2026 00:19:41 GMT
COPY entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:19:42 GMT
COPY docker.tcl ./scripts/ # buildkit
# Fri, 17 Apr 2026 00:19:42 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:42 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:f204fe7ddd292eb5d783ce14a8bc6c5a7defbb8adda2989da2c9dcf46b3e08e9`  
		Last Modified: Thu, 16 Apr 2026 23:53:42 GMT  
		Size: 3.4 MB (3369055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c374072ba32c01442f0bc881932103e1d3772d2bc00e8b062c7092cdc2e68`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a3fc78f147be0a6f75404b2223e3a66d9ed97bc8b88511cefff87c7fc3feb`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 1.1 MB (1129838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdae370e1d341a287804a804d34cc0acf80fd3cd119915268293b2d8ac176af8`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 7.9 MB (7852263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5c85741ba086a4b4bd0655ce6c6b9a28480970380dc9c143ce66d52d1a7cd1`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9ed8de466fe06402cb0fb11c925eb41da881155504ec1494fdc22c7694858c`  
		Last Modified: Fri, 17 Apr 2026 00:19:47 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:46de0444f5f0c5c64594207ffcf40cf79435a1e2d46ae6383bdb9d9a3bee73dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1185ee92ea1edfb662c66c485d29f135e59c101fd60fd7a0596e32a72008d077`

```dockerfile
```

-	Layers:
	-	`sha256:30709a5fd6cd3680779b0fb002e97d206a56433cf499550f767302d490ab0971`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 18.2 KB (18241 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:latest` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2f41546c2c21a00307692dfacbe19b20b998c5c97248e0396c7285f504d9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13249767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb801cf5db8a542234bffb3b06d94385d41b5bade14ecc8ec7d4483d3e2bb26`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:47 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 17 Apr 2026 00:14:47 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Fri, 17 Apr 2026 00:14:48 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
ENV NICK=
# Fri, 17 Apr 2026 00:18:39 GMT
ENV SERVER=
# Fri, 17 Apr 2026 00:18:39 GMT
ENV LISTEN=3333
# Fri, 17 Apr 2026 00:18:39 GMT
ENV USERFILE=eggdrop.user
# Fri, 17 Apr 2026 00:18:39 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 17 Apr 2026 00:18:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 17 Apr 2026 00:18:39 GMT
EXPOSE map[3333/tcp:{}]
# Fri, 17 Apr 2026 00:18:39 GMT
COPY entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
COPY docker.tcl ./scripts/ # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 17 Apr 2026 00:18:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aa8e6d9529a22c42f62c196fbc14cff0b4b2f6f85731dc47791a26659a0f9d`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc20d43f4a698300a2fbd826d527be10d6228ff9e8e1fbe1641919449130ed2`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 1.2 MB (1171093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1e830796510795845e0874861d3017366dc761d855737f34104efb97f6cd9c`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 8.1 MB (8080153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5637df7552f34e0e16cc0e36d7ed5cd368a17cb61e1cfd7c45bc37cc84902faa`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78a01f4a689ba4d7fceb47a6386bacf8976ecd594b007f7e718bb9d152291b9`  
		Last Modified: Fri, 17 Apr 2026 00:18:46 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:latest` - unknown; unknown

```console
$ docker pull eggdrop@sha256:7b637fff83800b96b44a4bf88901779d06ead891ad3c150efd2d1605c0b88b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 KB (163515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd92da4846368041b6d4b65f9427406d8519e4373ccccd579a5b67c6106974f3`

```dockerfile
```

-	Layers:
	-	`sha256:005cad79de2c194f7f0f289f6ef0f8dde0aa123cd07299fa56b8f2724a2fbac3`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 145.0 KB (145031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b6dcbdb96fd698ddce7932c0f6009c0e06335c648bb933017f918fded4ebfe`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 18.5 KB (18484 bytes)  
		MIME: application/vnd.in-toto+json

## `eggdrop:stable`

```console
$ docker pull eggdrop@sha256:2028d25c44a8fa7dbbfee1e1c9db809c5ba23eaa6516fbe84eb86c44886e1e04
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
$ docker pull eggdrop@sha256:64da7a09d997e3b03ce2bd030fa54d14325da63f7df7391570e074fd5bd1f1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12802733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718de2fa6c06b5129ac5a811dc8441b23bb94c98231b303ac02f9ccbd5cb2c20`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:15:18 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 17 Apr 2026 00:15:18 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Fri, 17 Apr 2026 00:15:19 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
ENV NICK=
# Fri, 17 Apr 2026 00:18:32 GMT
ENV SERVER=
# Fri, 17 Apr 2026 00:18:32 GMT
ENV LISTEN=3333
# Fri, 17 Apr 2026 00:18:32 GMT
ENV USERFILE=eggdrop.user
# Fri, 17 Apr 2026 00:18:32 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 17 Apr 2026 00:18:32 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 17 Apr 2026 00:18:32 GMT
EXPOSE map[3333/tcp:{}]
# Fri, 17 Apr 2026 00:18:32 GMT
COPY entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
COPY docker.tcl ./scripts/ # buildkit
# Fri, 17 Apr 2026 00:18:32 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 17 Apr 2026 00:18:32 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f339cba84b981e1992cc557fb400cce5b960817ef6a6ea37d3679e32151c52d`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b54844e2f73941a03f5f1377b0108c701158c0206eadc611f9f0cde58cfd62`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 1.1 MB (1116762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f1258ab988d483973ca23059dfec49d66ea59ba160c20334542ca1dd7da1a8`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 8.0 MB (8035037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7d1919a67ebb69f4e586c1dd8cecb6332dee411ca6337a373011a666e2cdc`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3eae19d9f3bea0db98992720d3ca3ad36feb9b14d3aaccaeaa5d322e90f10`  
		Last Modified: Fri, 17 Apr 2026 00:18:39 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:1e16c97c5e56cc6861f6cc7fabc9a4a7a177078ad500159acd8f2108f30b58f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 KB (163325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36970bc6aaf3d383125e9b85289878fef3922f9d720404cd8c9b8753dd0dfa10`

```dockerfile
```

-	Layers:
	-	`sha256:ed8e5fe0d625549d9a976cd4048647e39ad76f3555e48ea0e4109bc60c28b960`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 145.0 KB (144975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdc2afd18987a9aa8aae1747b837845425d0a1289ce2f77ba657da307910f96`  
		Last Modified: Fri, 17 Apr 2026 00:18:38 GMT  
		Size: 18.4 KB (18350 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm variant v6

```console
$ docker pull eggdrop@sha256:5aca1ce17d31254d25f5dd5123df2b5fbb8a7ba5d4191b4df1a9e0ee96cd3175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12355218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3761451ba6fa939892112f0a02ba6fb597d891bcf3ed467e3ded6545ac9bec4`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:38 GMT
ADD alpine-minirootfs-3.21.7-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:38 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:52 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 17 Apr 2026 00:14:52 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Fri, 17 Apr 2026 00:14:53 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Fri, 17 Apr 2026 00:19:41 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Fri, 17 Apr 2026 00:19:41 GMT
ENV NICK=
# Fri, 17 Apr 2026 00:19:41 GMT
ENV SERVER=
# Fri, 17 Apr 2026 00:19:41 GMT
ENV LISTEN=3333
# Fri, 17 Apr 2026 00:19:41 GMT
ENV USERFILE=eggdrop.user
# Fri, 17 Apr 2026 00:19:41 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 17 Apr 2026 00:19:41 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 17 Apr 2026 00:19:41 GMT
EXPOSE map[3333/tcp:{}]
# Fri, 17 Apr 2026 00:19:41 GMT
COPY entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:19:42 GMT
COPY docker.tcl ./scripts/ # buildkit
# Fri, 17 Apr 2026 00:19:42 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 17 Apr 2026 00:19:42 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:f204fe7ddd292eb5d783ce14a8bc6c5a7defbb8adda2989da2c9dcf46b3e08e9`  
		Last Modified: Thu, 16 Apr 2026 23:53:42 GMT  
		Size: 3.4 MB (3369055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c374072ba32c01442f0bc881932103e1d3772d2bc00e8b062c7092cdc2e68`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6a3fc78f147be0a6f75404b2223e3a66d9ed97bc8b88511cefff87c7fc3feb`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 1.1 MB (1129838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdae370e1d341a287804a804d34cc0acf80fd3cd119915268293b2d8ac176af8`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 7.9 MB (7852263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5c85741ba086a4b4bd0655ce6c6b9a28480970380dc9c143ce66d52d1a7cd1`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9ed8de466fe06402cb0fb11c925eb41da881155504ec1494fdc22c7694858c`  
		Last Modified: Fri, 17 Apr 2026 00:19:47 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:46de0444f5f0c5c64594207ffcf40cf79435a1e2d46ae6383bdb9d9a3bee73dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1185ee92ea1edfb662c66c485d29f135e59c101fd60fd7a0596e32a72008d077`

```dockerfile
```

-	Layers:
	-	`sha256:30709a5fd6cd3680779b0fb002e97d206a56433cf499550f767302d490ab0971`  
		Last Modified: Fri, 17 Apr 2026 00:19:46 GMT  
		Size: 18.2 KB (18241 bytes)  
		MIME: application/vnd.in-toto+json

### `eggdrop:stable` - linux; arm64 variant v8

```console
$ docker pull eggdrop@sha256:2f41546c2c21a00307692dfacbe19b20b998c5c97248e0396c7285f504d9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13249767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb801cf5db8a542234bffb3b06d94385d41b5bade14ecc8ec7d4483d3e2bb26`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:47 GMT
LABEL org.opencontainers.image.authors=Geo Van O <geo@eggheads.org> org.opencontainers.image.url=https://www.eggheads.org
# Fri, 17 Apr 2026 00:14:47 GMT
RUN addgroup -S -g 3333 eggdrop     && adduser -S -u 3333 eggdrop eggdrop # buildkit
# Fri, 17 Apr 2026 00:14:48 GMT
RUN apk add --no-cache 'su-exec>=0.2' bash openssl # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
RUN apk add --no-cache --virtual egg-deps wget ca-certificates make tar gnupg build-base openssl-dev bsd-compat-headers zlib-dev   && wget "https://prdownloads.sourceforge.net/tcl/tcl9.0.1-src.tar.gz" -O tcl9.0.1-src.tar.gz --progress=dot:giga   && tar -zxf tcl9.0.1-src.tar.gz   && ( cd tcl9.0.1     && cd unix     && ./configure     && nproc="$(nproc)"     && make -j"$nproc"     && make install )   && rm -rf tcl9.0.1-src.tar.gz   && rm -rf tcl9.0.1   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.10/eggdrop-1.10.1.tar.gz.asc   && gpg --batch --keyserver keyserver.ubuntu.com --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.10.1.tar.gz.asc eggdrop-1.10.1.tar.gz   && gpgconf --kill all   && rm eggdrop-1.10.1.tar.gz.asc   && tar -zxvf eggdrop-1.10.1.tar.gz   && rm eggdrop-1.10.1.tar.gz   && ( cd eggdrop-1.10.1     && ./configure     && make config     && nproc="$(nproc)"     && make -j"$nproc"     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.10.1   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del --no-network egg-deps # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
ENV NICK=
# Fri, 17 Apr 2026 00:18:39 GMT
ENV SERVER=
# Fri, 17 Apr 2026 00:18:39 GMT
ENV LISTEN=3333
# Fri, 17 Apr 2026 00:18:39 GMT
ENV USERFILE=eggdrop.user
# Fri, 17 Apr 2026 00:18:39 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 17 Apr 2026 00:18:39 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 17 Apr 2026 00:18:39 GMT
EXPOSE map[3333/tcp:{}]
# Fri, 17 Apr 2026 00:18:39 GMT
COPY entrypoint.sh ./ # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
COPY docker.tcl ./scripts/ # buildkit
# Fri, 17 Apr 2026 00:18:39 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 17 Apr 2026 00:18:39 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aa8e6d9529a22c42f62c196fbc14cff0b4b2f6f85731dc47791a26659a0f9d`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc20d43f4a698300a2fbd826d527be10d6228ff9e8e1fbe1641919449130ed2`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 1.2 MB (1171093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1e830796510795845e0874861d3017366dc761d855737f34104efb97f6cd9c`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 8.1 MB (8080153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5637df7552f34e0e16cc0e36d7ed5cd368a17cb61e1cfd7c45bc37cc84902faa`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78a01f4a689ba4d7fceb47a6386bacf8976ecd594b007f7e718bb9d152291b9`  
		Last Modified: Fri, 17 Apr 2026 00:18:46 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `eggdrop:stable` - unknown; unknown

```console
$ docker pull eggdrop@sha256:7b637fff83800b96b44a4bf88901779d06ead891ad3c150efd2d1605c0b88b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 KB (163515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd92da4846368041b6d4b65f9427406d8519e4373ccccd579a5b67c6106974f3`

```dockerfile
```

-	Layers:
	-	`sha256:005cad79de2c194f7f0f289f6ef0f8dde0aa123cd07299fa56b8f2724a2fbac3`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 145.0 KB (145031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b6dcbdb96fd698ddce7932c0f6009c0e06335c648bb933017f918fded4ebfe`  
		Last Modified: Fri, 17 Apr 2026 00:18:45 GMT  
		Size: 18.5 KB (18484 bytes)  
		MIME: application/vnd.in-toto+json
