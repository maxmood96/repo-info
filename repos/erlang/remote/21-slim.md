## `erlang:21-slim`

```console
$ docker pull erlang@sha256:b893e4e139ed3a245ee2f95e32ed27ffd699d285f756ffa4448d6dc6a4ec31b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `erlang:21-slim` - linux; amd64

```console
$ docker pull erlang@sha256:608f17e3a4862220fae06ff1f3b9e6b7a5a7530bd3dc444b024c578da705885f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107591222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699ff74ed0c80725eab694914334b56d5fb50c4bdaa8ee264c9a187abc6c3aca`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 13 May 2020 21:23:35 GMT
ADD file:82e0eb87c6ff97b66f86c9fee44884c4cf1b08f5721f36878fc7a15a125b5079 in / 
# Wed, 13 May 2020 21:23:35 GMT
CMD ["bash"]
# Thu, 14 May 2020 01:03:45 GMT
ENV OTP_VERSION=21.3.8.15
# Thu, 14 May 2020 01:03:45 GMT
LABEL org.opencontainers.image.version=21.3.8.15
# Thu, 14 May 2020 01:21:11 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7004876880504323eda7a1ed9de89697ec5810936f0224af05e798bd57878b09" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 14 May 2020 01:21:12 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e6ce7b04634a37b5c20274b3cc1469490cb28f734448d2c84d01454465418e1f`  
		Last Modified: Wed, 13 May 2020 21:29:57 GMT  
		Size: 45.4 MB (45375936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0632f41d33b0f2d317bf38136a0e60e8ad6a96210dead3ad8f53ec44a58c7b9e`  
		Last Modified: Thu, 14 May 2020 03:19:48 GMT  
		Size: 62.2 MB (62215286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:21-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:5d476351bbb54732b694d91f79a6e251b0e8be66f6fc8078caec72600177b1c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99167593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398d134284f7a209e2bef68d0951ee860148ed67680ad23784d41a22419ba87b`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 13 May 2020 21:18:55 GMT
ADD file:22401e33698b1bb830736dfb4dcfcae97faee4aeb57fbc910c50a0806fb726e3 in / 
# Wed, 13 May 2020 21:18:57 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:43:02 GMT
ENV OTP_VERSION=21.3.8.15
# Wed, 13 May 2020 22:43:04 GMT
LABEL org.opencontainers.image.version=21.3.8.15
# Wed, 13 May 2020 22:49:50 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7004876880504323eda7a1ed9de89697ec5810936f0224af05e798bd57878b09" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 13 May 2020 22:49:52 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6d01aee5144e594ba9bd007624dc3b8437510d15e6c34689c8475bf2d6b5c3e4`  
		Last Modified: Wed, 13 May 2020 21:28:12 GMT  
		Size: 42.1 MB (42101107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5598a5c70082d7198dad197ce047e0f0dd2014dc86eed340f309805d845e4ac1`  
		Last Modified: Wed, 13 May 2020 23:18:31 GMT  
		Size: 57.1 MB (57066486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:21-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:c631cd242217ae48f11ae22d954bd9974a036e1221f5356b7bca6350efcc31f9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101445810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122ca839516b9b88fcf53d382faf109ec4fdc342d7d3815c2b1d877a3c8806ba`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 13 May 2020 21:47:38 GMT
ADD file:e7776aac0b87be303e31e5947db89f835a4e17175e339ec23becf5fe4a9548a5 in / 
# Wed, 13 May 2020 21:47:41 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:29:38 GMT
ENV OTP_VERSION=21.3.8.15
# Wed, 13 May 2020 23:29:39 GMT
LABEL org.opencontainers.image.version=21.3.8.15
# Wed, 13 May 2020 23:36:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7004876880504323eda7a1ed9de89697ec5810936f0224af05e798bd57878b09" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 13 May 2020 23:36:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0480c895dd1d5b237cb931426f18706cbe8dac16e19ed583f3010f3655094efa`  
		Last Modified: Wed, 13 May 2020 21:56:03 GMT  
		Size: 43.2 MB (43158976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca1627548b40b2dd96490287e0aa9078950599291d28e126fcb3c7efbf56dd9`  
		Last Modified: Thu, 14 May 2020 00:44:57 GMT  
		Size: 58.3 MB (58286834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:21-slim` - linux; 386

```console
$ docker pull erlang@sha256:04d2f9a9aabd6a98b09c3725465f3adea4d5420f3b52143dbc1a2b56e2c56171
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111309092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24509f0167bc11b5c8a0ea7dfdf70fa1d764589ea5f1ab57cfd3c2f722cb95a5`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 13 May 2020 21:42:23 GMT
ADD file:0d501ab6846646b4793ce31bd08a81ee75bf7ca50e44fad4f41d38ea73217f94 in / 
# Wed, 13 May 2020 21:42:23 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:34:41 GMT
ENV OTP_VERSION=21.3.8.15
# Wed, 13 May 2020 22:34:42 GMT
LABEL org.opencontainers.image.version=21.3.8.15
# Wed, 13 May 2020 22:48:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7004876880504323eda7a1ed9de89697ec5810936f0224af05e798bd57878b09" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 13 May 2020 22:48:33 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:738ccd27fcd21d91d1826e5bb5ee29ef3a82a770de7e1407c86b04395fdd1335`  
		Last Modified: Wed, 13 May 2020 21:49:47 GMT  
		Size: 46.1 MB (46095041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9933cc8f01e13d87d7af8cbae448532560473eddfe23957caf909cbe4f34fea5`  
		Last Modified: Wed, 13 May 2020 23:36:09 GMT  
		Size: 65.2 MB (65214051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:21-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:dcf7c222ced80384821331e000088a9762611a9fb11378331a42e1d315f1e53c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104820341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd505eb17da6cb0b4c7a30464660f9ca67377577f06212c1bfbadae8a331309`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 13 May 2020 22:39:29 GMT
ADD file:fa4c7e3ca04f092e53cc791a32c929663412df3f68de2733bb867053577bf1d1 in / 
# Wed, 13 May 2020 22:39:34 GMT
CMD ["bash"]
# Thu, 14 May 2020 03:14:09 GMT
ENV OTP_VERSION=21.3.8.15
# Thu, 14 May 2020 03:14:12 GMT
LABEL org.opencontainers.image.version=21.3.8.15
# Thu, 14 May 2020 03:22:49 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7004876880504323eda7a1ed9de89697ec5810936f0224af05e798bd57878b09" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 14 May 2020 03:22:55 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7732483b686efe14a1cf8add89a1568b83892e243798fba30808f1fc6287210b`  
		Last Modified: Wed, 13 May 2020 23:02:10 GMT  
		Size: 45.6 MB (45646193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31024a167786fa40c06af7fd092a8ca500d87b5c833b7eb55e350fa8b92e61cb`  
		Last Modified: Thu, 14 May 2020 03:54:14 GMT  
		Size: 59.2 MB (59174148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:21-slim` - linux; s390x

```console
$ docker pull erlang@sha256:8514b022c925097d5d6c1c2a24613a4215cd7ca6785e89d3b565a86e506c7641
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105988165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7035a96e6911f449d4b37d776c5281ae39b7555d3187f1d2c883869724a6ec`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 13 May 2020 21:44:18 GMT
ADD file:80db5381a461bb249455c6e92a06f91a777c0d8db654106cc55f91d6252c3c44 in / 
# Wed, 13 May 2020 21:44:20 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:14:11 GMT
ENV OTP_VERSION=21.3.8.15
# Wed, 13 May 2020 22:14:11 GMT
LABEL org.opencontainers.image.version=21.3.8.15
# Wed, 13 May 2020 22:18:44 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7004876880504323eda7a1ed9de89697ec5810936f0224af05e798bd57878b09" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 13 May 2020 22:18:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:dd38adf1f4e3b358b79e0f6559fa135ec376d7abbcc3f8bf0b62a2d19d972cbc`  
		Last Modified: Wed, 13 May 2020 21:48:31 GMT  
		Size: 45.2 MB (45232705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f99dba7b64ce8bf0c411a26db7604ef7b2a7ec5376b24bac1be259ff207d371`  
		Last Modified: Wed, 13 May 2020 22:35:26 GMT  
		Size: 60.8 MB (60755460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
