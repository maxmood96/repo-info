## `elixir:slim`

```console
$ docker pull elixir@sha256:756919094a2fee4524e07a5504cf61a09a7004a80feff1ac88fb6ed90f2dc3de
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
$ docker pull elixir@sha256:dee5ac69d52f75e75b3d55bf5fa7052b51b730c5e02f082f25d8db9f814f9416
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116992699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc07e5e3387ac072ce557a4a76c8cd9caff957f9fee67fac2aab9aa89542e08`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:38 GMT
ADD file:a5ec219cbfc4e0c31e7df48cc51abd9a5b92754e15403b2ab726e25042041680 in / 
# Sat, 01 Feb 2020 17:20:39 GMT
CMD ["bash"]
# Tue, 18 Feb 2020 23:34:01 GMT
ENV OTP_VERSION=22.2.7
# Tue, 18 Feb 2020 23:34:01 GMT
LABEL org.opencontainers.image.version=22.2.7
# Tue, 18 Feb 2020 23:51:19 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="29487837a2dd6e3184257cdec067cd3f5c0cd9517fbfb2ffc962589d46afbf75" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 18 Feb 2020 23:51:19 GMT
CMD ["erl"]
# Wed, 19 Feb 2020 00:31:24 GMT
ENV ELIXIR_VERSION=v1.10.1 LANG=C.UTF-8
# Wed, 19 Feb 2020 00:33:57 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="bf10dc5cb084382384d69cc26b4f670a3eb0a97a6491182f4dcf540457f06c07" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Feb 2020 00:33:58 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:dc65f448a2e2f2ea557e69ed9ac65aa8ac0e16f1bce68f90de910b4d5a2f1ba1`  
		Last Modified: Sat, 01 Feb 2020 17:26:04 GMT  
		Size: 50.4 MB (50379770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20938c515635915d93ce1c9cb8bb24f8336c7b999ad53abe39a77fe64e7c6ddd`  
		Last Modified: Wed, 19 Feb 2020 00:12:55 GMT  
		Size: 59.4 MB (59389811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f44979fbfd7e809842bac16bbe72df23eae0041c2460d723117865d685ec69`  
		Last Modified: Wed, 19 Feb 2020 00:44:46 GMT  
		Size: 7.2 MB (7223118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:6ba47a63e6c17ac140ec449c5ba4e647f6a661d436964add6c3cd2091309bda5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108237272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98f9c4fafd94008db0c93a024b490845f4df3e01caa1f71025639b83689aa3b`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 01 Feb 2020 17:00:06 GMT
ADD file:a57a312731f174c4b03031908ff95f49d7055d8c196439f0ed07ed9c4834d993 in / 
# Sat, 01 Feb 2020 17:00:08 GMT
CMD ["bash"]
# Wed, 19 Feb 2020 00:07:16 GMT
ENV OTP_VERSION=22.2.7
# Wed, 19 Feb 2020 00:07:17 GMT
LABEL org.opencontainers.image.version=22.2.7
# Wed, 19 Feb 2020 00:13:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="29487837a2dd6e3184257cdec067cd3f5c0cd9517fbfb2ffc962589d46afbf75" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 19 Feb 2020 00:13:35 GMT
CMD ["erl"]
# Wed, 19 Feb 2020 00:40:21 GMT
ENV ELIXIR_VERSION=v1.10.1 LANG=C.UTF-8
# Wed, 19 Feb 2020 00:42:39 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="bf10dc5cb084382384d69cc26b4f670a3eb0a97a6491182f4dcf540457f06c07" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Feb 2020 00:42:40 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:9bbb41bca8c6254da5088d03354297b1309dc75c2ccc738416025f89709ae5ee`  
		Last Modified: Sat, 01 Feb 2020 17:07:28 GMT  
		Size: 45.9 MB (45859700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68186bc5e2da9316a256c496069664c287dbd015e03dd23e8cff9e5a00f3d60`  
		Last Modified: Wed, 19 Feb 2020 00:21:50 GMT  
		Size: 55.2 MB (55155023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74028dd499bd1c79c4ae884a01a89410aa5d162e3f4e77f5e0c893fa1054bae1`  
		Last Modified: Wed, 19 Feb 2020 00:57:13 GMT  
		Size: 7.2 MB (7222549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:b12c6c41f916f7b3df86d7ea8f0a1d90073581dfcd2df31ce35779968511e491
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112704561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbeecfdb6ead6fd020e2248bab1f5aa87a6666618d2c89f3a4c4d160fbd9e34`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 01 Feb 2020 16:40:50 GMT
ADD file:b423f4b0ed41dfe1334031fe9b21f7e1c88ccb031d7e8f2ff165d618323424d7 in / 
# Sat, 01 Feb 2020 16:40:53 GMT
CMD ["bash"]
# Tue, 18 Feb 2020 23:48:34 GMT
ENV OTP_VERSION=22.2.7
# Tue, 18 Feb 2020 23:48:35 GMT
LABEL org.opencontainers.image.version=22.2.7
# Tue, 18 Feb 2020 23:54:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="29487837a2dd6e3184257cdec067cd3f5c0cd9517fbfb2ffc962589d46afbf75" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 18 Feb 2020 23:54:56 GMT
CMD ["erl"]
# Wed, 19 Feb 2020 00:21:37 GMT
ENV ELIXIR_VERSION=v1.10.1 LANG=C.UTF-8
# Wed, 19 Feb 2020 00:24:06 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="bf10dc5cb084382384d69cc26b4f670a3eb0a97a6491182f4dcf540457f06c07" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Feb 2020 00:24:08 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:bc03a7ced18fc43ea9523dfb256d2c3fbb835dc0bb54bdb7fd309edf936a87e7`  
		Last Modified: Sat, 01 Feb 2020 16:46:06 GMT  
		Size: 49.2 MB (49171687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74782478f4d88dfa2693c6f471a44cf8ff396abaafa0928be2c851c079cbbd17`  
		Last Modified: Wed, 19 Feb 2020 00:03:18 GMT  
		Size: 56.3 MB (56310164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868f4efd4fe069fb126f4a40c53c634fb4c7c83d3fe0bff196873c630dc41117`  
		Last Modified: Wed, 19 Feb 2020 00:39:31 GMT  
		Size: 7.2 MB (7222710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; 386

```console
$ docker pull elixir@sha256:3ea523b2e33a5736f8d112ee751e9677d7dc5431eb4347ce104e2becda07b05d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117119942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35ede5abed2a2238b8824c0482d74eb1bbe23fe31038044fd6999cf4b326fc2`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:21 GMT
ADD file:b637f96d557a570f8ab83b28f7b9cdd128958359dd30dc2e03df70b799e132aa in / 
# Sat, 01 Feb 2020 16:39:21 GMT
CMD ["bash"]
# Wed, 19 Feb 2020 00:04:21 GMT
ENV OTP_VERSION=22.2.7
# Wed, 19 Feb 2020 00:04:21 GMT
LABEL org.opencontainers.image.version=22.2.7
# Wed, 19 Feb 2020 00:20:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="29487837a2dd6e3184257cdec067cd3f5c0cd9517fbfb2ffc962589d46afbf75" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 19 Feb 2020 00:20:02 GMT
CMD ["erl"]
# Wed, 19 Feb 2020 00:54:48 GMT
ENV ELIXIR_VERSION=v1.10.1 LANG=C.UTF-8
# Wed, 19 Feb 2020 00:56:16 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="bf10dc5cb084382384d69cc26b4f670a3eb0a97a6491182f4dcf540457f06c07" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Feb 2020 00:56:16 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:2b34644a479c82db66a603c0b0a1d990911345f8646498fa9b050f306d0e6bf2`  
		Last Modified: Sat, 01 Feb 2020 16:44:10 GMT  
		Size: 51.1 MB (51141949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e36e909e6f24e8b1b961029bf3a55cca7ee9f5c22ba8140c9dae68b68d8ad04`  
		Last Modified: Wed, 19 Feb 2020 00:37:37 GMT  
		Size: 58.8 MB (58755209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840797085d959f1b222890a605419b852e02d79ec54f6cb0eddea27582c88ce4`  
		Last Modified: Wed, 19 Feb 2020 01:06:21 GMT  
		Size: 7.2 MB (7222784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:d00935e802a79dede8b509d4f277a896d3b80ad12c5b71492689c9bdca2a35c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118559648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d15b7fc00f2b2fb75d969bcde8dde1c989d3719dcec949316e74c3764dc221`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 01 Feb 2020 17:17:37 GMT
ADD file:8e8c5417abc372541fe34cddec6fe8625ded93da51d1f5488e0aece309a3fd25 in / 
# Sat, 01 Feb 2020 17:17:45 GMT
CMD ["bash"]
# Tue, 18 Feb 2020 23:30:58 GMT
ENV OTP_VERSION=22.2.7
# Tue, 18 Feb 2020 23:31:01 GMT
LABEL org.opencontainers.image.version=22.2.7
# Tue, 18 Feb 2020 23:41:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="29487837a2dd6e3184257cdec067cd3f5c0cd9517fbfb2ffc962589d46afbf75" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 18 Feb 2020 23:41:23 GMT
CMD ["erl"]
# Wed, 19 Feb 2020 00:12:58 GMT
ENV ELIXIR_VERSION=v1.10.1 LANG=C.UTF-8
# Wed, 19 Feb 2020 00:16:40 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="bf10dc5cb084382384d69cc26b4f670a3eb0a97a6491182f4dcf540457f06c07" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Feb 2020 00:16:44 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:a2d5a5ee40c1df8706e6db684b090e0e4297581ff38256a81222ea8be61180fc`  
		Last Modified: Sat, 01 Feb 2020 17:25:27 GMT  
		Size: 54.1 MB (54132833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2072bfb472dba440e80d90e257d333e31b339366ae5a808db7cb7d162fde3abe`  
		Last Modified: Tue, 18 Feb 2020 23:54:04 GMT  
		Size: 57.2 MB (57203229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a6e6a9ef4bef4a5c7f82bac112d9f2954fca36d6512cc6e6e438d6c80c8489`  
		Last Modified: Wed, 19 Feb 2020 00:33:17 GMT  
		Size: 7.2 MB (7223586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elixir:slim` - linux; s390x

```console
$ docker pull elixir@sha256:0c438b65b1e15406d4c4ce080dded84ed8b06e7b395ac5c8d0276cfaca30c37b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112507201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe55af45ccd48b92f1a5d63d0771fb07f746c54903e19d112ab720eb0b17f93`
-	Default Command: `["iex"]`

```dockerfile
# Sat, 01 Feb 2020 16:42:14 GMT
ADD file:642aef2e391d18e3999374d6068f29ccc5ad62b25a0d18c852a6b5534daa18f7 in / 
# Sat, 01 Feb 2020 16:42:17 GMT
CMD ["bash"]
# Tue, 18 Feb 2020 23:52:12 GMT
ENV OTP_VERSION=22.2.7
# Tue, 18 Feb 2020 23:52:13 GMT
LABEL org.opencontainers.image.version=22.2.7
# Tue, 18 Feb 2020 23:59:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="29487837a2dd6e3184257cdec067cd3f5c0cd9517fbfb2ffc962589d46afbf75" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 19 Feb 2020 00:00:03 GMT
CMD ["erl"]
# Wed, 19 Feb 2020 00:28:15 GMT
ENV ELIXIR_VERSION=v1.10.1 LANG=C.UTF-8
# Wed, 19 Feb 2020 00:29:54 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="bf10dc5cb084382384d69cc26b4f670a3eb0a97a6491182f4dcf540457f06c07" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 19 Feb 2020 00:29:56 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6f3b736b312bfd59fd7947524542ae1d57ed4564aefaafdf0ccfb7d600f7978f`  
		Last Modified: Sat, 01 Feb 2020 16:45:36 GMT  
		Size: 49.0 MB (48954499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb3b3da1715043be457be7945c616aa9a904df556610fb3e7bd7b1c64da5553`  
		Last Modified: Wed, 19 Feb 2020 00:10:41 GMT  
		Size: 56.3 MB (56329947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198b4bd848552c902ab54b04640a0091b5e7cc7c8c54c908fecc4c0b787d56a8`  
		Last Modified: Wed, 19 Feb 2020 00:42:08 GMT  
		Size: 7.2 MB (7222755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
