## `erlang:21-slim`

```console
$ docker pull erlang@sha256:e5a742c3a4e5f89dd5f01eaab404b7c4b16bff82af4e8deb8f5b7ab19894cc76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown

### `erlang:21-slim` - linux; amd64

```console
$ docker pull erlang@sha256:10c84ad88dd56ccdf3a6124aed9ceed5f5000594f3b77c204278ad46bcb7a8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109214401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281132b1fc96b99ef649e34b1c612e0f2a8a152c2cee1bd7217b3ab4b5d8d465`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 19 Jul 2022 11:55:46 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Tue, 19 Jul 2022 11:55:46 GMT
CMD ["bash"]
# Tue, 19 Jul 2022 11:55:46 GMT
ENV OTP_VERSION=21.3.8.24 REBAR3_VERSION=3.15.2
# Tue, 19 Jul 2022 11:55:46 GMT
LABEL org.opencontainers.image.version=21.3.8.24
# Tue, 19 Jul 2022 11:55:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="90017fe0b844cf3ba7dc9faf7f6f690050f3138f3d3f7532a9343174f5f9febc" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 19 Jul 2022 11:55:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de6e67d8db27418e746c877ed95d3c5838d01a057e5b0a802de5198f61be7c3`  
		Last Modified: Thu, 30 May 2024 21:03:42 GMT  
		Size: 58.6 MB (58557492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:21-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e3021cc6ca2ac32d5994c8bac3cb162442a83957bf199bf6cad1f56c026f3e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de32eb9ba44e98330d1bd487384591cd79979ad9eafaac4048f2d4b722aefea`

```dockerfile
```

-	Layers:
	-	`sha256:fcd3e7f29eefd833c623934ac7877f8b5d4ead8f05fbb79116c7588f6f36bbc1`  
		Last Modified: Thu, 30 May 2024 21:03:41 GMT  
		Size: 4.0 MB (3989850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc91f8e6099d15a084f6840d26beb700678e18ea44eec43ffc0aff9f93c5084`  
		Last Modified: Thu, 30 May 2024 21:03:41 GMT  
		Size: 13.3 KB (13316 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:21-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:d05d3897bef72dbf3ad99f17e2cc2e1b702b5da10e49f6d6543e886c891db5bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.5 MB (100529898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647aebccf7602af15b96e082b9f2bbcb264ce17c1505f53ccda79e80639e809f`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 14 May 2024 01:09:12 GMT
ADD file:a05edfdd56e92b1814d8e812ef81e814accd29893888392076dbc26b33b5ae41 in / 
# Tue, 14 May 2024 01:09:13 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:34:06 GMT
ENV OTP_VERSION=21.3.8.24 REBAR3_VERSION=3.15.2
# Tue, 14 May 2024 03:34:06 GMT
LABEL org.opencontainers.image.version=21.3.8.24
# Tue, 14 May 2024 03:38:55 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="90017fe0b844cf3ba7dc9faf7f6f690050f3138f3d3f7532a9343174f5f9febc" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 14 May 2024 03:38:55 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:66d6e1b7bddcb1c893c2c3e9b1ac8f5fca7c047037ed836079c97c9a917cd989`  
		Last Modified: Tue, 14 May 2024 01:13:47 GMT  
		Size: 46.1 MB (46129793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c21fc768777a26fcf2389d6e31121ae465c22f30b4c78657f2621062c2815e6`  
		Last Modified: Tue, 14 May 2024 03:57:43 GMT  
		Size: 54.4 MB (54400105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:21-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:747e4645033697f849980891291e87dcb106c321086881ef19b85d7e170b4926
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104881778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e77c049b08ea35fdb1a6de9637d97387905aab440e47d54c205a0da50e9295`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 14 May 2024 00:40:02 GMT
ADD file:da8c3a2d966487a4e1bc0646a771d18df585d75dc24f095a1aaa762ce0841747 in / 
# Tue, 14 May 2024 00:40:02 GMT
CMD ["bash"]
# Tue, 14 May 2024 08:50:45 GMT
ENV OTP_VERSION=21.3.8.24 REBAR3_VERSION=3.15.2
# Tue, 14 May 2024 08:50:45 GMT
LABEL org.opencontainers.image.version=21.3.8.24
# Tue, 14 May 2024 08:54:05 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="90017fe0b844cf3ba7dc9faf7f6f690050f3138f3d3f7532a9343174f5f9febc" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 14 May 2024 08:54:06 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0a8090f4fec79fd213192f5f5c31c70546878a20b6c7ca023ff9001fb788f828`  
		Last Modified: Tue, 14 May 2024 00:43:49 GMT  
		Size: 49.5 MB (49453094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a4fd3ac4828200943609e27e14aee3ccc1b080618386b7b735821086affd2c`  
		Last Modified: Tue, 14 May 2024 09:09:14 GMT  
		Size: 55.4 MB (55428684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:21-slim` - linux; 386

```console
$ docker pull erlang@sha256:519ba2d7fb458691d0d063b0509707ee5dbbbb96d9d8c5e6b16ffab1629471a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109459243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c3220939cd651dae743296fc44d9cf7e42a1e14d717ad479f8515a7a9cde33`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 19 Jul 2022 11:55:46 GMT
ADD file:5e59addfe8663b7c16cce40874c2a3c8601e20e80f5a0897c86b64ba463c10e9 in / 
# Tue, 19 Jul 2022 11:55:46 GMT
CMD ["bash"]
# Tue, 19 Jul 2022 11:55:46 GMT
ENV OTP_VERSION=21.3.8.24 REBAR3_VERSION=3.15.2
# Tue, 19 Jul 2022 11:55:46 GMT
LABEL org.opencontainers.image.version=21.3.8.24
# Tue, 19 Jul 2022 11:55:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="90017fe0b844cf3ba7dc9faf7f6f690050f3138f3d3f7532a9343174f5f9febc" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 19 Jul 2022 11:55:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1a892f56e4b10aaecbb51b3219d90bd0d8a1e955acd0624a6ef27ed086ba168c`  
		Last Modified: Tue, 14 May 2024 00:53:06 GMT  
		Size: 51.4 MB (51419713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0199625cc0dd83457d2d625ed300a4936139bd76a23f1b9da86afd1b2ff08b`  
		Last Modified: Thu, 30 May 2024 21:04:24 GMT  
		Size: 58.0 MB (58039530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:21-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c1ccc59f629158c64ef7da860c1901e2c38455e69595321c18e4d48e76e026fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72690ca4033374fce7ad344ae470892cc6e1b79128041ed0e8b0dbcf51318441`

```dockerfile
```

-	Layers:
	-	`sha256:770992cf000fe88dee2415f38cf5859a0918fcca30ffe5c586d3c8fa18807c3d`  
		Last Modified: Thu, 30 May 2024 21:04:22 GMT  
		Size: 4.0 MB (3987093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:913f677623277b7b64de47b39ac68a4fb3bdb786c6a49d48af1cebf5e0c197d7`  
		Last Modified: Thu, 30 May 2024 21:04:22 GMT  
		Size: 13.3 KB (13288 bytes)  
		MIME: application/vnd.in-toto+json
