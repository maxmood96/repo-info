## `erlang:slim`

```console
$ docker pull erlang@sha256:9fd68bd1bdec31d1ea370ee3862a39be7305e08bb1fc5b2bdca08dd153feeeff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `erlang:slim` - linux; amd64

```console
$ docker pull erlang@sha256:fa99fe3ad407a862a8dcbb82aee13041cbe728750b0ba6f8e6c657db20f50917
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (111020607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4781fcc2d5f259a476a7616bf0150721daa7034858def652cf8b2534206f9f2`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 10 Sep 2020 00:22:55 GMT
ADD file:07a6578d6f507bd9c51bdf4fe41402db5dcf3b9fdf51cd4315778c27da1add39 in / 
# Thu, 10 Sep 2020 00:22:55 GMT
CMD ["bash"]
# Fri, 25 Sep 2020 21:33:22 GMT
ENV OTP_VERSION=23.1
# Fri, 25 Sep 2020 21:33:22 GMT
LABEL org.opencontainers.image.version=23.1
# Fri, 25 Sep 2020 21:44:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="3591903503ea70be3ef1e42abc7a3e1f8af90f2c8989506bf9832175f091e6e5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 25 Sep 2020 21:44:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:57df1a1f1ad841deaf50c8f662d77e93b4b17af776ed66148116607f9aceffa8`  
		Last Modified: Thu, 10 Sep 2020 00:33:42 GMT  
		Size: 50.4 MB (50395913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f58ff7330c82f1c83c5c5aee968266e34587554edbfec9bafc3b4a64d2d8ff`  
		Last Modified: Fri, 25 Sep 2020 22:02:04 GMT  
		Size: 60.6 MB (60624694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:54a1dd3163ff69a9caa299ed061a04f8637a32ab7e1fe5badade4d7b252e6a73
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102309544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e359dd01284d7b3aed4a0a950d1bcee176ec080e0c8207d862e6b93b037d023c`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 10 Sep 2020 00:07:32 GMT
ADD file:340663c3add65bd8904ba51984e6080c6aa6d237bd845f4e0aa22626d31497b7 in / 
# Thu, 10 Sep 2020 00:07:35 GMT
CMD ["bash"]
# Fri, 25 Sep 2020 21:09:10 GMT
ENV OTP_VERSION=23.1
# Fri, 25 Sep 2020 21:09:11 GMT
LABEL org.opencontainers.image.version=23.1
# Fri, 25 Sep 2020 21:15:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="3591903503ea70be3ef1e42abc7a3e1f8af90f2c8989506bf9832175f091e6e5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 25 Sep 2020 21:15:30 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7d9beb74056b685831827b5f21351f021873d8ba1a1170b378e5edf5f46d114e`  
		Last Modified: Thu, 10 Sep 2020 00:17:29 GMT  
		Size: 45.9 MB (45869299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2458ae3b39a8d0fd818a4e0d6a266c5a88b634c18eab5c441a91108d25acc8e6`  
		Last Modified: Fri, 25 Sep 2020 21:24:17 GMT  
		Size: 56.4 MB (56440245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:cdc038c493b9e113e6ff4e41285cc8c2d8d3132bcda55adc5829b27cb2063cc6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106728676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d42501de1c97e628da81f680013fa455f742bbd1c823fca43996eb644c56afc8`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Sep 2020 23:50:21 GMT
ADD file:c8c11e622b1b8a1e31f32e2457ff4d1314d5cd4a7ad22b3991ab9d0542db23fd in / 
# Wed, 09 Sep 2020 23:50:22 GMT
CMD ["bash"]
# Fri, 25 Sep 2020 21:51:06 GMT
ENV OTP_VERSION=23.1
# Fri, 25 Sep 2020 21:51:07 GMT
LABEL org.opencontainers.image.version=23.1
# Fri, 25 Sep 2020 21:57:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="3591903503ea70be3ef1e42abc7a3e1f8af90f2c8989506bf9832175f091e6e5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 25 Sep 2020 21:57:23 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d3a32671b6316bd11f4bf18cb034394ac94d2bb3bc6d09de388b19b06fb94b91`  
		Last Modified: Wed, 09 Sep 2020 23:58:45 GMT  
		Size: 49.2 MB (49175549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af15bd1d187db1dc976de46f82da2d6e8ee15d12d3c68521b25986bd1c915afd`  
		Last Modified: Fri, 25 Sep 2020 22:07:14 GMT  
		Size: 57.6 MB (57553127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:c4c46b5f80b5aa90d87cd352209f7b14673eb2285e543f7dcbc0bab906c8e7b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.0 MB (110967226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee88ba80fd37eff423d9cbed5473b33968a27ee0ee3bbdb76b84acd6823a5cb`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Sep 2020 23:39:58 GMT
ADD file:39c4b1e1e5d34f52ad1f95b26bfbbf45f307b94a52d472a561496c440f96d8a2 in / 
# Wed, 09 Sep 2020 23:39:59 GMT
CMD ["bash"]
# Fri, 11 Sep 2020 22:25:15 GMT
ENV OTP_VERSION=23.0.4
# Fri, 11 Sep 2020 22:25:15 GMT
LABEL org.opencontainers.image.version=23.0.4
# Fri, 11 Sep 2020 22:36:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="29e92db80229ec7903f93e5b152c7ca721cc44b58519199ea60b8e0d583faf93" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 11 Sep 2020 22:36:16 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c89594b72f230eaccb7faa969906602c0f8e2667b7e30e66fe230243f1b5f1d0`  
		Last Modified: Wed, 09 Sep 2020 23:46:14 GMT  
		Size: 51.2 MB (51158853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192324ca39b0b1770808311c7fe256e2adcc7d0bc89c9a4620855af637f77901`  
		Last Modified: Fri, 11 Sep 2020 22:53:35 GMT  
		Size: 59.8 MB (59808373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:015177fd2cfb520f9a7df67cbda83e64b1ad1dad7cd8d803f14575dfad166ecf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112447112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d21685a485c94f571f9f3940b7301d6f3d5d203938e35af42e1e21855e076c`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 10 Sep 2020 01:04:56 GMT
ADD file:a2329a0372b3b40ca345795d86a78ab4cdaa3a1eeda3a5ece35a83881543db1a in / 
# Thu, 10 Sep 2020 01:05:18 GMT
CMD ["bash"]
# Fri, 11 Sep 2020 22:52:08 GMT
ENV OTP_VERSION=23.0.4
# Fri, 11 Sep 2020 22:52:10 GMT
LABEL org.opencontainers.image.version=23.0.4
# Fri, 11 Sep 2020 23:07:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="29e92db80229ec7903f93e5b152c7ca721cc44b58519199ea60b8e0d583faf93" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 11 Sep 2020 23:07:41 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:aff7fe9e9819c2b9d4338fae03bd06eb6784016bcf53b2eeab88c21e47dea428`  
		Last Modified: Thu, 10 Sep 2020 01:26:27 GMT  
		Size: 54.1 MB (54142644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee167e76f0a8e2f50b8b5be4947f3356d8fe1882b0d01a3592d3bb5d7c1fd44`  
		Last Modified: Fri, 11 Sep 2020 23:18:51 GMT  
		Size: 58.3 MB (58304468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:b6ce45b264f0eb3aef8cb7bf208697d61196b2792827731071bb028211b405a8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106546329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e44609164a3df09ea3cb6787ce6300d315c2e693e302fde8988cac64c4935f8`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Sep 2020 23:42:11 GMT
ADD file:67eedff26215ed3c8100b93d0201c563ec8efe2af7bdfff5c7717037f95057af in / 
# Wed, 09 Sep 2020 23:42:15 GMT
CMD ["bash"]
# Fri, 25 Sep 2020 21:48:39 GMT
ENV OTP_VERSION=23.1
# Fri, 25 Sep 2020 21:48:39 GMT
LABEL org.opencontainers.image.version=23.1
# Fri, 25 Sep 2020 21:52:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="3591903503ea70be3ef1e42abc7a3e1f8af90f2c8989506bf9832175f091e6e5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 25 Sep 2020 21:52:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4c594945c9b37f16bdb296d1c06754e5bbcc3c28a736d7aa6091f61a081b3cfb`  
		Last Modified: Wed, 09 Sep 2020 23:46:12 GMT  
		Size: 49.0 MB (48966294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84830748abed04619ec7e111efbc683b3ede696628992ecdd186904785f8feb6`  
		Last Modified: Fri, 25 Sep 2020 21:58:03 GMT  
		Size: 57.6 MB (57580035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
