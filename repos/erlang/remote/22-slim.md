## `erlang:22-slim`

```console
$ docker pull erlang@sha256:bf57d060fdb0902361f10851101fab0dd18fadeb8174154570108597dd7b2723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `erlang:22-slim` - linux; amd64

```console
$ docker pull erlang@sha256:f2f018ff520259b1e11e431cd564a2f0bc3dd621363947a94b61b553641ce86e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109898262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5600ed2159ad5740163809c121840c779d6e51511a7cbd3f0b3aa3674eb6ab3c`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 31 Mar 2020 01:20:44 GMT
ADD file:c027885123a178148eb4f51f10f4924740859f1f6e941e55580517f6d234e935 in / 
# Tue, 31 Mar 2020 01:20:45 GMT
CMD ["bash"]
# Thu, 09 Apr 2020 18:50:35 GMT
ENV OTP_VERSION=22.3.2
# Thu, 09 Apr 2020 18:50:36 GMT
LABEL org.opencontainers.image.version=22.3.2
# Thu, 09 Apr 2020 19:15:31 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4a3719c71a7998e4f57e73920439b4b1606f7c045e437a0f0f9f1613594d3eaa" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 09 Apr 2020 19:15:31 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f15005b0235fa8bd31cc6988c4f2758016fe412d696e81aecf73e52be079f19e`  
		Last Modified: Tue, 31 Mar 2020 01:26:22 GMT  
		Size: 50.4 MB (50382041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11afcd48df5d959701edbdbe9763249caf1ff44a8e3b54a73fc7c6a4cc7dd502`  
		Last Modified: Thu, 09 Apr 2020 19:40:37 GMT  
		Size: 59.5 MB (59516221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:22-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:a98b92206b46c9ce59027546f947b18e28b79ccc6ed267b5e2f055ad1d583cd8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101154738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed18a2711e7fa0b642013a8fa00caca5451f82411fe9d98bed4b9441cbd05f41`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 31 Mar 2020 01:47:44 GMT
ADD file:57841d22461f051368fcd3488aab2f2ce27ec7583af772026a228feeb5d00cd9 in / 
# Tue, 31 Mar 2020 01:47:47 GMT
CMD ["bash"]
# Thu, 09 Apr 2020 19:09:00 GMT
ENV OTP_VERSION=22.3.2
# Thu, 09 Apr 2020 19:09:01 GMT
LABEL org.opencontainers.image.version=22.3.2
# Thu, 09 Apr 2020 19:15:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4a3719c71a7998e4f57e73920439b4b1606f7c045e437a0f0f9f1613594d3eaa" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 09 Apr 2020 19:15:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a893843c75627d21c8a132a2b8559c62371e185dc82e30169102b547264b4f20`  
		Last Modified: Tue, 31 Mar 2020 01:56:02 GMT  
		Size: 45.9 MB (45862803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be961d2fd213a42386a952d4b50ffc98b346143bdd0a50853d38206963736643`  
		Last Modified: Thu, 09 Apr 2020 19:23:45 GMT  
		Size: 55.3 MB (55291935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:22-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:ecef52272279e8e8cad15fb10ec16fa3a8e160c4e2314788116b724c3908f588
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.6 MB (105610036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103a04e501d904b1fee69b1a6a8a688fbba39ca1efcafab53331c6cd312e1910`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 31 Mar 2020 02:05:07 GMT
ADD file:d0df7ac13226f8d35c078941a20d8a465b09a4e226c5ca37709fa23599cd56dc in / 
# Tue, 31 Mar 2020 02:05:09 GMT
CMD ["bash"]
# Thu, 09 Apr 2020 19:06:49 GMT
ENV OTP_VERSION=22.3.2
# Thu, 09 Apr 2020 19:06:49 GMT
LABEL org.opencontainers.image.version=22.3.2
# Thu, 09 Apr 2020 19:13:27 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4a3719c71a7998e4f57e73920439b4b1606f7c045e437a0f0f9f1613594d3eaa" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 09 Apr 2020 19:13:29 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5767fbcc7692f25971758138978eed9bd3add831a79561cd58bf281e60a5159f`  
		Last Modified: Tue, 31 Mar 2020 02:11:54 GMT  
		Size: 49.2 MB (49169998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899a362771d17299ff0e5e0b0126e392a748c3e315a96b06875bddaccc800d28`  
		Last Modified: Thu, 09 Apr 2020 19:22:02 GMT  
		Size: 56.4 MB (56440038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:22-slim` - linux; 386

```console
$ docker pull erlang@sha256:e54459582aab7856bcd3091161712d7dc0c85b6af87c367c67674632b97e953f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110036865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b9ee622f0d0e55d9abd28e53c8b920a5919937fca2d402065feabaa0622695`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 31 Mar 2020 00:39:25 GMT
ADD file:3dbe042e711d452b61bbca02798da5695de980649d3fd51ae6983b2445eaa792 in / 
# Tue, 31 Mar 2020 00:39:25 GMT
CMD ["bash"]
# Thu, 09 Apr 2020 20:32:33 GMT
ENV OTP_VERSION=22.3.2
# Thu, 09 Apr 2020 20:32:33 GMT
LABEL org.opencontainers.image.version=22.3.2
# Thu, 09 Apr 2020 20:46:14 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4a3719c71a7998e4f57e73920439b4b1606f7c045e437a0f0f9f1613594d3eaa" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 09 Apr 2020 20:46:15 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:acd641cee0ec134334632eecb48cf0c487a224a27ad5661fcd7eed50b0a1ab34`  
		Last Modified: Tue, 31 Mar 2020 00:45:15 GMT  
		Size: 51.1 MB (51146119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a4e6c841435687c10f1f72a7120bb4853ff9283d69bcf17937fe4fe5987344`  
		Last Modified: Thu, 09 Apr 2020 21:01:38 GMT  
		Size: 58.9 MB (58890746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:22-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:ccd8d00fed3b319b697c3274ed72f761bdac49b28952b8f639293f884b4492d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111480716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01773d17d1164ff0a65a33cb53f73baaafdf44275cc2c6b44731e3ceec07e2b`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 31 Mar 2020 01:32:00 GMT
ADD file:ccb86d1c4380ce5c6d0f26560ca6d637d15f7a9dd5a3e56977bcf80edcac69ac in / 
# Tue, 31 Mar 2020 01:32:04 GMT
CMD ["bash"]
# Thu, 09 Apr 2020 18:34:27 GMT
ENV OTP_VERSION=22.3.2
# Thu, 09 Apr 2020 18:34:29 GMT
LABEL org.opencontainers.image.version=22.3.2
# Thu, 09 Apr 2020 18:47:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4a3719c71a7998e4f57e73920439b4b1606f7c045e437a0f0f9f1613594d3eaa" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 09 Apr 2020 18:47:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2ee2adf89ee904a62d0e8993a1c564c340ff8a0d3ae152066c13e15fbae902ea`  
		Last Modified: Tue, 31 Mar 2020 01:44:47 GMT  
		Size: 54.1 MB (54138582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88df62d289f3f9871dccee69e71f17418c0b29a79fc0b7508363becb088c4c6b`  
		Last Modified: Thu, 09 Apr 2020 18:58:42 GMT  
		Size: 57.3 MB (57342134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:22-slim` - linux; s390x

```console
$ docker pull erlang@sha256:bbe52bd9f59887c6f6992e41fd4c1a32dbda0f7cd1a892693c9c1cd78825db41
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105422526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3253ee810d8925821d0dbe029f19c21f8c914cf004ba4c1b84122a3acc79e189`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 31 Mar 2020 01:08:46 GMT
ADD file:a2690e2e8794d163493c5a6daa8b6503432365b11e48372e175d855c28ec64db in / 
# Tue, 31 Mar 2020 01:08:49 GMT
CMD ["bash"]
# Thu, 09 Apr 2020 19:45:37 GMT
ENV OTP_VERSION=22.3.2
# Thu, 09 Apr 2020 19:45:37 GMT
LABEL org.opencontainers.image.version=22.3.2
# Thu, 09 Apr 2020 19:49:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4a3719c71a7998e4f57e73920439b4b1606f7c045e437a0f0f9f1613594d3eaa" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 09 Apr 2020 19:49:44 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e5611e94178b5632fbdf7d00655f2a077f35fbef849c9665429c154c52784cd2`  
		Last Modified: Tue, 31 Mar 2020 01:12:24 GMT  
		Size: 49.0 MB (48958144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0804787a00b09364351827174e6079a87f1104af628d1e96c3b4fb5688af4ba9`  
		Last Modified: Thu, 09 Apr 2020 19:55:58 GMT  
		Size: 56.5 MB (56464382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
