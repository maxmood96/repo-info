## `elixir:slim`

```console
$ docker pull elixir@sha256:fad4c90a86da973bd25f826174f752f18553ba994255af9b438c0c1490c375b2
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
$ docker pull elixir@sha256:d3c38ed696be7cd50f79505a9b8539fe09872c0061752b3ddd1e70397671ea8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118755585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a755a651ff42f689284b9c00cfdacb3d22e5e8014dbe65f7b50f844fc68f7b7`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:40 GMT
ADD file:8f75f11b2bd2d50e5912359ae750de06a7b49506df3756c19baf4cc63d900c4f in / 
# Tue, 09 Feb 2021 02:20:40 GMT
CMD ["bash"]
# Tue, 16 Feb 2021 23:41:29 GMT
ENV OTP_VERSION=23.2.5
# Tue, 16 Feb 2021 23:41:29 GMT
LABEL org.opencontainers.image.version=23.2.5
# Tue, 16 Feb 2021 23:53:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="00587a60bc97a26060265b201f69dd7059ddd04506f6502e8e78c5f00e1b1db7" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 16 Feb 2021 23:53:57 GMT
CMD ["erl"]
# Wed, 17 Feb 2021 00:32:07 GMT
ENV ELIXIR_VERSION=v1.11.3 LANG=C.UTF-8
# Wed, 17 Feb 2021 00:34:34 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d961305e893f4fe1a177fa00233762c34598bc62ff88b32dcee8af27e36f0564" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Feb 2021 00:34:34 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0ecb575e629cd60aa802266a3bc6847dcf4073aa2a6d7d43f717dd61e7b90e0b`  
		Last Modified: Tue, 09 Feb 2021 02:26:22 GMT  
		Size: 50.4 MB (50400198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe92be8699ac8ccbae3b1988179833d3ff340dbeede4416e0d055f882e9b9bf`  
		Last Modified: Wed, 17 Feb 2021 00:09:56 GMT  
		Size: 60.9 MB (60866211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bd284ace67983be04b41af8886c1733219cecdc6d3b072d3aa3af96b9aa094`  
		Last Modified: Wed, 17 Feb 2021 00:39:52 GMT  
		Size: 7.5 MB (7489176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:4f6211ab68e62a0bc8445aabd8ee06437f1d6b4039fcb32853571fd1f350d008
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110014909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c0d796909d17690422e47091398eeb196df8c851535a984fd596741187956f`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 09 Feb 2021 03:00:29 GMT
ADD file:817a4ff41fcac0be44e95d3f0a51c9fa878d16dac7cdab68bfc445f630c43c22 in / 
# Tue, 09 Feb 2021 03:00:33 GMT
CMD ["bash"]
# Fri, 26 Feb 2021 01:33:00 GMT
ENV OTP_VERSION=23.2.6
# Fri, 26 Feb 2021 01:33:00 GMT
LABEL org.opencontainers.image.version=23.2.6
# Fri, 26 Feb 2021 01:39:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5bc6b31b36b949bf06e84d51986311fc1d2ace5e717aae3186dc057d4838445d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 26 Feb 2021 01:39:18 GMT
CMD ["erl"]
# Fri, 26 Feb 2021 02:51:22 GMT
ENV ELIXIR_VERSION=v1.11.3 LANG=C.UTF-8
# Fri, 26 Feb 2021 02:54:00 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d961305e893f4fe1a177fa00233762c34598bc62ff88b32dcee8af27e36f0564" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Feb 2021 02:54:02 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:4c2a0a79594a20b9c2f0bfbd535f875ca1b079625052cdd801afb1cc0362d6d0`  
		Last Modified: Tue, 09 Feb 2021 03:09:18 GMT  
		Size: 45.9 MB (45867053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175150629f1055f077dfd14c8716ca548796ba41ef9e5b62d1431adac3952b91`  
		Last Modified: Fri, 26 Feb 2021 02:29:35 GMT  
		Size: 56.7 MB (56659200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997a1db441e8b54f2dd8879f92d5a78838d6b2c2f4a893740aad78e2bc63fb9b`  
		Last Modified: Fri, 26 Feb 2021 03:20:36 GMT  
		Size: 7.5 MB (7488656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:faa8d39fc30305896dd112fe8649bd1543b248ed31665a9b013a52e221edbe3b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114440389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1d82707ee4b4a7e42df65cacb7def9b1488fc1336aed001dd19477ab10bace`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 09 Feb 2021 02:40:45 GMT
ADD file:78412ee35e3dc6fb5fdfce41eb05dd273ba1d49328ab327465639bfa4821aa51 in / 
# Tue, 09 Feb 2021 02:40:50 GMT
CMD ["bash"]
# Tue, 16 Feb 2021 23:50:40 GMT
ENV OTP_VERSION=23.2.5
# Tue, 16 Feb 2021 23:50:41 GMT
LABEL org.opencontainers.image.version=23.2.5
# Tue, 16 Feb 2021 23:56:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="00587a60bc97a26060265b201f69dd7059ddd04506f6502e8e78c5f00e1b1db7" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 16 Feb 2021 23:56:56 GMT
CMD ["erl"]
# Wed, 17 Feb 2021 00:26:57 GMT
ENV ELIXIR_VERSION=v1.11.3 LANG=C.UTF-8
# Wed, 17 Feb 2021 00:29:40 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d961305e893f4fe1a177fa00233762c34598bc62ff88b32dcee8af27e36f0564" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Feb 2021 00:29:42 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c78c297fb0d010ee085f95ae439636ecb167b050c1acb4273bd576998cf94a83`  
		Last Modified: Tue, 09 Feb 2021 02:47:03 GMT  
		Size: 49.2 MB (49183229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a1691f44f4b67697884bc85a5b82f2aebda023c4d0555e35d6cbecf2a62288`  
		Last Modified: Wed, 17 Feb 2021 00:07:17 GMT  
		Size: 57.8 MB (57768283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5083c81e775a21cd3e40298c0e269c2c6f48f5fa008aba3010069068fcaedba5`  
		Last Modified: Wed, 17 Feb 2021 00:35:17 GMT  
		Size: 7.5 MB (7488877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; 386

```console
$ docker pull elixir@sha256:d4df3c2b70ee616fed419c0bc9d6723f282b4be72f481fa5504f05e9a60cfffe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118860448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d488928ebff389b4a73eca62770b647999a4e9c634515b4537f65fe8872af3`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:32 GMT
ADD file:174c1471a32619d54d725ea84d52c784b0093e0fa3327988de11aa4c7a1a74f8 in / 
# Tue, 09 Feb 2021 02:39:32 GMT
CMD ["bash"]
# Wed, 17 Feb 2021 01:21:12 GMT
ENV OTP_VERSION=23.2.5
# Wed, 17 Feb 2021 01:21:13 GMT
LABEL org.opencontainers.image.version=23.2.5
# Wed, 17 Feb 2021 01:33:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="00587a60bc97a26060265b201f69dd7059ddd04506f6502e8e78c5f00e1b1db7" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 17 Feb 2021 01:33:45 GMT
CMD ["erl"]
# Wed, 17 Feb 2021 02:32:57 GMT
ENV ELIXIR_VERSION=v1.11.3 LANG=C.UTF-8
# Wed, 17 Feb 2021 02:34:41 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d961305e893f4fe1a177fa00233762c34598bc62ff88b32dcee8af27e36f0564" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Feb 2021 02:34:42 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:ddc66558221fdd621c8a9a9b10318a2be0e73e6e9b5201713c51d24dc672e99f`  
		Last Modified: Tue, 09 Feb 2021 02:45:29 GMT  
		Size: 51.2 MB (51163172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5147e12ebaa4ea84678cd2888281599386a467afc82e5fb193fa36f735a9b8e1`  
		Last Modified: Wed, 17 Feb 2021 01:46:25 GMT  
		Size: 60.2 MB (60208403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42857b13b0d409c3ff33826381ae12d713e3aec6177ade105cc39c0b29269453`  
		Last Modified: Wed, 17 Feb 2021 02:38:47 GMT  
		Size: 7.5 MB (7488873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:3ab8b3f354c06ad79df665b5cbc27a6dc742ad5be937e25477306bc4bf87bb75
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120336192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feba46faa879b99ae3b5a8e9082f9c5f12e3bbaace73a4976aced3a0380533d1`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 09 Feb 2021 02:18:34 GMT
ADD file:0fc1572a1f7f423ae98036bea9f9d1f9237ea74bf582a925ecf956383f7dc8e1 in / 
# Tue, 09 Feb 2021 02:18:46 GMT
CMD ["bash"]
# Wed, 17 Feb 2021 00:08:48 GMT
ENV OTP_VERSION=23.2.5
# Wed, 17 Feb 2021 00:08:54 GMT
LABEL org.opencontainers.image.version=23.2.5
# Wed, 17 Feb 2021 00:24:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="00587a60bc97a26060265b201f69dd7059ddd04506f6502e8e78c5f00e1b1db7" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 17 Feb 2021 00:24:37 GMT
CMD ["erl"]
# Wed, 17 Feb 2021 00:59:38 GMT
ENV ELIXIR_VERSION=v1.11.3 LANG=C.UTF-8
# Wed, 17 Feb 2021 01:04:59 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d961305e893f4fe1a177fa00233762c34598bc62ff88b32dcee8af27e36f0564" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Feb 2021 01:05:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:9311932ee2fcc8fed8d2911fda20f73ee92ea26879166cf6cc3192522e83fd0a`  
		Last Modified: Tue, 09 Feb 2021 02:27:25 GMT  
		Size: 54.1 MB (54135809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede8d3f4975fde22220d11df36431fc565db7811315dfa5f00f74e1994abce8e`  
		Last Modified: Wed, 17 Feb 2021 00:34:29 GMT  
		Size: 58.7 MB (58710208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3038edd2b79936c8977abb8839c503471ba3b32c507a1ea7a3c39e87c6cd8822`  
		Last Modified: Wed, 17 Feb 2021 01:09:35 GMT  
		Size: 7.5 MB (7490175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; s390x

```console
$ docker pull elixir@sha256:9fc81f43f5087e834f2192f86aa95e86e0689542139d035d1fb57a6713f41b9e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114266992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00277406e90a70e4c296dac087bd5fa72e886ebe8da23aea224ed19d421c71ce`
-	Default Command: `["iex"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:56 GMT
ADD file:f390b371893461fffed2fb48d65b6c930137539a82b9c5329410cef322a5a9ea in / 
# Tue, 09 Feb 2021 02:41:59 GMT
CMD ["bash"]
# Fri, 26 Feb 2021 02:20:18 GMT
ENV OTP_VERSION=23.2.6
# Fri, 26 Feb 2021 02:20:19 GMT
LABEL org.opencontainers.image.version=23.2.6
# Fri, 26 Feb 2021 02:27:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="5bc6b31b36b949bf06e84d51986311fc1d2ace5e717aae3186dc057d4838445d" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Fri, 26 Feb 2021 02:27:54 GMT
CMD ["erl"]
# Fri, 26 Feb 2021 03:14:49 GMT
ENV ELIXIR_VERSION=v1.11.3 LANG=C.UTF-8
# Fri, 26 Feb 2021 03:16:54 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="d961305e893f4fe1a177fa00233762c34598bc62ff88b32dcee8af27e36f0564" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Feb 2021 03:16:56 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:fb61e252baf0cdce361b288d8df47eab4b2adb45935d61331700aa9281372c74`  
		Last Modified: Tue, 09 Feb 2021 02:45:12 GMT  
		Size: 49.0 MB (48970386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588eda1f8229aa63437db1cd9dfad4556661e7f32fbd38ce4bec5c740bafc8f8`  
		Last Modified: Fri, 26 Feb 2021 02:52:55 GMT  
		Size: 57.8 MB (57807706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e4fdc9fa06dd14b31c449e06e6a71279363e08a04f1092fb16270ebb345cab`  
		Last Modified: Fri, 26 Feb 2021 03:26:19 GMT  
		Size: 7.5 MB (7488900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
