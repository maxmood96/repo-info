## `elixir:slim`

```console
$ docker pull elixir@sha256:e94ca9b575e0bfba4edac96b065463b7e3471a5e1deba7b4041cc2ba6a03e571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `elixir:slim` - linux; amd64

```console
$ docker pull elixir@sha256:88250afb0513a19c93f16c6664ede77ff9549fe3ad67236adb09b02ae698ca9c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116999213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ecc497dc2848302eab239748b259852e45cab7b8418eeed6348f709a41b1c4`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:08 GMT
ADD file:d6d0bdf8cb07a7a0dc32e9df50ac80ca1a524c3fa48136892ded195061f2194c in / 
# Sat, 28 Dec 2019 04:21:09 GMT
CMD ["bash"]
# Wed, 29 Jan 2020 01:32:30 GMT
ENV OTP_VERSION=22.2.4
# Wed, 29 Jan 2020 01:32:30 GMT
LABEL org.opencontainers.image.version=22.2.4
# Wed, 29 Jan 2020 01:48:08 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7aab2285b46462332a7fdad395d4629e6465d5da324cf7e081e8d62fdb5b38f1" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 29 Jan 2020 01:48:08 GMT
CMD ["erl"]
# Thu, 30 Jan 2020 23:23:57 GMT
ENV ELIXIR_VERSION=v1.10.0 LANG=C.UTF-8
# Thu, 30 Jan 2020 23:25:21 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6f0d35acfcbede5ef7dced3e37f016fd122c2779000ca9dcaf92975b220737b7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 30 Jan 2020 23:25:22 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:8f0fdd3eaac017684c880d836abdaf02f9db7ac8ecca970356482e3d8e315650`  
		Last Modified: Sat, 28 Dec 2019 04:25:39 GMT  
		Size: 50.4 MB (50379720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63947aeb6e514353841ca0df1b9d2d8fc87b717e7b7bb4bb6a4635e730d27aaf`  
		Last Modified: Wed, 29 Jan 2020 02:10:10 GMT  
		Size: 59.4 MB (59397496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a4266fbdb0df3cc387be2b44bd1b0d927eec5d7146bbf3e13436ffeb905081`  
		Last Modified: Thu, 30 Jan 2020 23:28:26 GMT  
		Size: 7.2 MB (7221997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:72dd21352a373e3e8223df8bd42d7cfc514fcdd4fa5ce6c6952d4f11a1364094
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108231846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183ed2788d48141d0fde9a2ebdb857bfddd7fecacdb7dc8d41af90f657068bed`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 28 Dec 2019 04:58:42 GMT
ADD file:26fba5cd6ba1fe45f19fb80d1c8e54eac5189e2b93e521b2ba6d5a6b54175e81 in / 
# Sat, 28 Dec 2019 04:58:45 GMT
CMD ["bash"]
# Wed, 29 Jan 2020 02:07:20 GMT
ENV OTP_VERSION=22.2.4
# Wed, 29 Jan 2020 02:07:21 GMT
LABEL org.opencontainers.image.version=22.2.4
# Wed, 29 Jan 2020 02:13:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7aab2285b46462332a7fdad395d4629e6465d5da324cf7e081e8d62fdb5b38f1" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 29 Jan 2020 02:13:43 GMT
CMD ["erl"]
# Thu, 30 Jan 2020 23:00:06 GMT
ENV ELIXIR_VERSION=v1.10.0 LANG=C.UTF-8
# Thu, 30 Jan 2020 23:02:38 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6f0d35acfcbede5ef7dced3e37f016fd122c2779000ca9dcaf92975b220737b7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 30 Jan 2020 23:02:40 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:760e5af4a2ec2472d42b6773d075af9d2a006e0b7725ba9992e530f561d326f8`  
		Last Modified: Sat, 28 Dec 2019 05:07:11 GMT  
		Size: 45.9 MB (45859628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d812b5d2300255c745878f2ace159c872b47072f17a302d68d1f9509d3a1ea9f`  
		Last Modified: Wed, 29 Jan 2020 02:21:49 GMT  
		Size: 55.2 MB (55150548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7375d43426057823aaf8ca80d96dbf7c28dd46469b82b3cfb34def5a904bb224`  
		Last Modified: Thu, 30 Jan 2020 23:07:05 GMT  
		Size: 7.2 MB (7221670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:7c1107c6ce32a1756d2bd218a553b2e7135bf0cf045f1ac608365c31d857afcd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112701524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca677d11da248d0baec086216b069262ae8ce1c5a5ab331f377be25ccb53342`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 28 Dec 2019 04:40:41 GMT
ADD file:88b3d02fc98aa9138e694bee7d5d1b61b295e4a1c7fae399bf24e52eeff7a5ae in / 
# Sat, 28 Dec 2019 04:40:45 GMT
CMD ["bash"]
# Wed, 29 Jan 2020 01:48:42 GMT
ENV OTP_VERSION=22.2.4
# Wed, 29 Jan 2020 01:48:42 GMT
LABEL org.opencontainers.image.version=22.2.4
# Wed, 29 Jan 2020 01:54:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7aab2285b46462332a7fdad395d4629e6465d5da324cf7e081e8d62fdb5b38f1" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 29 Jan 2020 01:54:49 GMT
CMD ["erl"]
# Thu, 30 Jan 2020 22:42:35 GMT
ENV ELIXIR_VERSION=v1.10.0 LANG=C.UTF-8
# Thu, 30 Jan 2020 22:44:55 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6f0d35acfcbede5ef7dced3e37f016fd122c2779000ca9dcaf92975b220737b7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 30 Jan 2020 22:44:56 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:627706d65d1d9b4038d8fd40db52238d4f11d9130a01f23ffae9bf5d41ac5933`  
		Last Modified: Sat, 28 Dec 2019 04:46:38 GMT  
		Size: 49.2 MB (49171876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be2d84de2bd7756a66ed84cadc579e5f07b1691e15461209bfbe659f55708057`  
		Last Modified: Wed, 29 Jan 2020 02:03:19 GMT  
		Size: 56.3 MB (56307791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7450cbe4e6870d7b00c501512549123f0b9662b49f28f80de54a797c4c2ee634`  
		Last Modified: Thu, 30 Jan 2020 22:49:21 GMT  
		Size: 7.2 MB (7221857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; 386

```console
$ docker pull elixir@sha256:5f9b9aa664a578340fcf67a2c27ae3163fc0550f301f025ed81cf1b6e66c698a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117118727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df87f3b2a897e8ef385778ec9559ae518ddb0a3ffe9413739515075bcc95413`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:20 GMT
ADD file:c2d3c2cbbc436161afbcdcab7f07d11962ae8a6e99f8ed2c4ff2bcc92455a406 in / 
# Sat, 28 Dec 2019 04:39:21 GMT
CMD ["bash"]
# Wed, 29 Jan 2020 02:03:54 GMT
ENV OTP_VERSION=22.2.4
# Wed, 29 Jan 2020 02:03:54 GMT
LABEL org.opencontainers.image.version=22.2.4
# Wed, 29 Jan 2020 02:18:11 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7aab2285b46462332a7fdad395d4629e6465d5da324cf7e081e8d62fdb5b38f1" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 29 Jan 2020 02:18:11 GMT
CMD ["erl"]
# Thu, 30 Jan 2020 22:40:09 GMT
ENV ELIXIR_VERSION=v1.10.0 LANG=C.UTF-8
# Thu, 30 Jan 2020 22:41:37 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6f0d35acfcbede5ef7dced3e37f016fd122c2779000ca9dcaf92975b220737b7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 30 Jan 2020 22:41:37 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:b3ff5188aae7f0986a4e7385f8249878f585ef70be99706b3262795514448afc`  
		Last Modified: Sat, 28 Dec 2019 04:44:08 GMT  
		Size: 51.1 MB (51141961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2031fbcfc4b4918e16e0b56d7d1ec78d606c7d27d298685bc1a0fcb13926ba`  
		Last Modified: Wed, 29 Jan 2020 02:35:53 GMT  
		Size: 58.8 MB (58754937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff8ba5a306086d091f8dc03b145629c933bcd1199d2cd731afe2a9c34532d5f`  
		Last Modified: Thu, 30 Jan 2020 22:45:06 GMT  
		Size: 7.2 MB (7221829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:e4a84b44bcb75bc0cd2accfb35623a35cad259072f466758103d903c871a09bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118559603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf13a7f6b407f693a3427ece8c99c4230cf9ee245a4c22334a43ac7a985001a`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:12 GMT
ADD file:7c5858835ffb42e32df47084d7f85ba9392c5e37ee636e19dfae15d858c5b6c4 in / 
# Sat, 28 Dec 2019 04:20:17 GMT
CMD ["bash"]
# Wed, 29 Jan 2020 02:30:10 GMT
ENV OTP_VERSION=22.2.4
# Wed, 29 Jan 2020 02:30:13 GMT
LABEL org.opencontainers.image.version=22.2.4
# Wed, 29 Jan 2020 02:40:11 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7aab2285b46462332a7fdad395d4629e6465d5da324cf7e081e8d62fdb5b38f1" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 29 Jan 2020 02:40:19 GMT
CMD ["erl"]
# Thu, 30 Jan 2020 23:19:46 GMT
ENV ELIXIR_VERSION=v1.10.0 LANG=C.UTF-8
# Thu, 30 Jan 2020 23:23:11 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6f0d35acfcbede5ef7dced3e37f016fd122c2779000ca9dcaf92975b220737b7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 30 Jan 2020 23:23:15 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0a9adf09915c3544b1264f206aec99890c8e5e5c358fc4327886fbdab3c9eecc`  
		Last Modified: Sat, 28 Dec 2019 04:27:21 GMT  
		Size: 54.1 MB (54132515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a57c6afb8312b450d41d5078c52b9705d85248b0917434e5842e01b5aaa01d8`  
		Last Modified: Wed, 29 Jan 2020 02:50:34 GMT  
		Size: 57.2 MB (57204376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c28f3cae7bc78a8791232f396a1e2e9e2d73f7fcbfced432a9c076048d218af`  
		Last Modified: Thu, 30 Jan 2020 23:28:28 GMT  
		Size: 7.2 MB (7222712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; s390x

```console
$ docker pull elixir@sha256:0296d3550439665a0a0b49f1343cc41c0be03d8604b10ae284811ca45e853328
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112499144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a240456d3ebe75908718b3efd3c2ddaa0a47c4b6837940317ad9103d154ea7`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:51 GMT
ADD file:aeaf0b11195b2ba7eb7890ce128ad93c114a8e183a516cf2e4ea42da324c57ea in / 
# Sat, 28 Dec 2019 04:41:51 GMT
CMD ["bash"]
# Wed, 29 Jan 2020 01:48:45 GMT
ENV OTP_VERSION=22.2.4
# Wed, 29 Jan 2020 01:48:46 GMT
LABEL org.opencontainers.image.version=22.2.4
# Wed, 29 Jan 2020 01:52:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="7aab2285b46462332a7fdad395d4629e6465d5da324cf7e081e8d62fdb5b38f1" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 29 Jan 2020 01:52:38 GMT
CMD ["erl"]
# Thu, 30 Jan 2020 22:43:18 GMT
ENV ELIXIR_VERSION=v1.10.0 LANG=C.UTF-8
# Thu, 30 Jan 2020 22:44:14 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="6f0d35acfcbede5ef7dced3e37f016fd122c2779000ca9dcaf92975b220737b7" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 30 Jan 2020 22:44:14 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3596c5a237f76c32832c1879a3d0c763989cb13fac0024673b03e9b549b868ea`  
		Last Modified: Sat, 28 Dec 2019 04:44:54 GMT  
		Size: 49.0 MB (48954508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc886e8c55eb1682d0bba8a86f214869836e3f7495a32ceedee4bf6de5fd388d`  
		Last Modified: Wed, 29 Jan 2020 01:59:07 GMT  
		Size: 56.3 MB (56323069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed96d03843eaef77b4e3af02782be1b63dd6650afea48d63c42a970ca5f0200f`  
		Last Modified: Thu, 30 Jan 2020 22:47:20 GMT  
		Size: 7.2 MB (7221567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
