## `elixir:otp-27-slim`

```console
$ docker pull elixir@sha256:17e6f5e5f06dd263f8d53154be57d48e206f0dc4b287ce719482f9e1139d15a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `elixir:otp-27-slim` - linux; amd64

```console
$ docker pull elixir@sha256:4c42366276d38b03ccc3b9d51afbc85880d05b9a5f91f453f0ae6eb51873dfd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132759776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e7db2ccfab73b208c74c91e0dd92cadbd82439dcdf409675780424a9920e7a`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Mon, 23 Feb 2026 21:31:06 GMT
ENV OTP_VERSION=27.3.4.8 REBAR3_VERSION=3.26.0
# Mon, 23 Feb 2026 21:31:06 GMT
LABEL org.opencontainers.image.version=27.3.4.8
# Mon, 23 Feb 2026 21:31:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="354243af8095a5e567931490b7b0ffe7b22cf12ee49b65c36e9187501ca03e8e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:31:06 GMT
CMD ["erl"]
# Mon, 23 Feb 2026 21:35:18 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Mon, 23 Feb 2026 21:35:18 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:35:18 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1131c92043ef0dfcb96858896de8cf99e69bd2423420cf40376657572b5282d7`  
		Last Modified: Mon, 23 Feb 2026 21:31:22 GMT  
		Size: 76.0 MB (76037648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0bd50826cad8aaef340ce72954a441f44bd580cbc12af8d0d9fdee30494982`  
		Last Modified: Mon, 23 Feb 2026 21:35:26 GMT  
		Size: 8.2 MB (8240645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:a2a3b44c0223c1eb6cf69f1b231e270d2749c247546e60a5b6b74929eccd53e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69d056bcbc21d637c8fe8938e60125e4e2547b0349957d4045af517f67fe3e6`

```dockerfile
```

-	Layers:
	-	`sha256:98062cb4a3541221c9810804a4ded5e466e35594fdb6a475e877e42e3b172d89`  
		Last Modified: Mon, 23 Feb 2026 21:35:25 GMT  
		Size: 3.8 MB (3831807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f420642f6cdd4e6733af0a84cc3fcc600de6906b02b83341612993212dc0c2f7`  
		Last Modified: Mon, 23 Feb 2026 21:35:24 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:dee366555c9b10260a96e2c4f10e753d43a2808aedf6596946282c3412ee95fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117596883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1dfcf85a5fb4d3da11a0ca0b0040950b02839a879b41025fb62e5c00aeefdd`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Mon, 23 Feb 2026 21:31:52 GMT
ENV OTP_VERSION=27.3.4.8 REBAR3_VERSION=3.26.0
# Mon, 23 Feb 2026 21:31:52 GMT
LABEL org.opencontainers.image.version=27.3.4.8
# Mon, 23 Feb 2026 21:31:52 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="354243af8095a5e567931490b7b0ffe7b22cf12ee49b65c36e9187501ca03e8e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:31:52 GMT
CMD ["erl"]
# Mon, 23 Feb 2026 21:34:39 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Mon, 23 Feb 2026 21:34:39 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:34:39 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:424cab4c9a6a41cd57ee6de8e95726c4d76fe3e913bd9c7731865fd244771971`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 44.2 MB (44198733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74edc08b33792c0913dfe2e8c660795277b8220b2f7768f79ff96ce51ccfa2a7`  
		Last Modified: Mon, 23 Feb 2026 21:32:06 GMT  
		Size: 65.2 MB (65158049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf108282a0b1a762be8879670837059ef565d4d768af903fe710e06ffba3993`  
		Last Modified: Mon, 23 Feb 2026 21:34:47 GMT  
		Size: 8.2 MB (8240101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:296f1c6551a460b3e9824e58d84068d1ec83cee3393754bccdd033cb39ca7406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3843847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb4ae0fa32ce3b7f44e49fe9a0e734ba5cd1a16c76f5d1ed1c2830544034599`

```dockerfile
```

-	Layers:
	-	`sha256:6b1c575c2bb2acccb6f4010b726eda82df9a3461d2ba11dce11bc0be649c1bbf`  
		Last Modified: Mon, 23 Feb 2026 21:34:47 GMT  
		Size: 3.8 MB (3834032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c3d69d1eaf39ecc04930ec29dd8aafa726eb5420d6a35c0fe26ccaa75462f0d`  
		Last Modified: Mon, 23 Feb 2026 21:34:47 GMT  
		Size: 9.8 KB (9815 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:3a6d42f69f5840ea6427ab2a36fd461e9e768c5e554fa8d2b555cf0c8e741e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130386843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09390f215bbf09822a77bc71c1a5268c6f4766ef7582f4c439c7e901bf142981`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Mon, 23 Feb 2026 21:32:13 GMT
ENV OTP_VERSION=27.3.4.8 REBAR3_VERSION=3.26.0
# Mon, 23 Feb 2026 21:32:13 GMT
LABEL org.opencontainers.image.version=27.3.4.8
# Mon, 23 Feb 2026 21:32:13 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="354243af8095a5e567931490b7b0ffe7b22cf12ee49b65c36e9187501ca03e8e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:32:13 GMT
CMD ["erl"]
# Mon, 23 Feb 2026 21:38:34 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Mon, 23 Feb 2026 21:38:34 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:38:34 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f090cfab6bcec64348ea7e4deab8333ca3a82ff825759eec0a6fe97b9ca663`  
		Last Modified: Mon, 23 Feb 2026 21:32:28 GMT  
		Size: 73.8 MB (73780333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e9bded5e7d58e3c5a7ec18e8b8078ffab93fa229701b386035f724523f87a3`  
		Last Modified: Mon, 23 Feb 2026 21:38:44 GMT  
		Size: 8.2 MB (8240554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:f493c2660b6ae13e8f14982cef680b15ad11c3812f9b5520f3ce56370ee33d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f41d346fe178e02e3bb3e02eeb724e25830b6019d21b4077fc9ddde0eb8f74`

```dockerfile
```

-	Layers:
	-	`sha256:77c7fea8b17ae2c3d635f2b572aca4a6a7da227108aa348fecbbc9cbe37dfc82`  
		Last Modified: Mon, 23 Feb 2026 21:38:42 GMT  
		Size: 3.8 MB (3832056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db64c06cf1b4783fc41ae26cb0ed08d4999cd4615cd1fe5044fe8d6271e160e5`  
		Last Modified: Mon, 23 Feb 2026 21:38:41 GMT  
		Size: 9.8 KB (9838 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; 386

```console
$ docker pull elixir@sha256:aff6f1c1c21997f9f08ac62ed4652c4d63d41d80137835e6de10ba8a120cf653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123911240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57eed461d01da680ec296dfb2d35b795060ffd875754aebe15f12e10741eef4`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:26:34 GMT
ENV OTP_VERSION=27.3.4.8 REBAR3_VERSION=3.26.0
# Tue, 24 Feb 2026 19:26:34 GMT
LABEL org.opencontainers.image.version=27.3.4.8
# Tue, 24 Feb 2026 19:26:34 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="354243af8095a5e567931490b7b0ffe7b22cf12ee49b65c36e9187501ca03e8e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:34 GMT
CMD ["erl"]
# Tue, 24 Feb 2026 20:10:08 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Tue, 24 Feb 2026 20:10:08 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:10:08 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:443394a7d911f581670ce4df7959c82f7e8f0be02b5a7ba3c71bc5958012963d`  
		Last Modified: Tue, 24 Feb 2026 18:41:48 GMT  
		Size: 49.5 MB (49477853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7640fc38d130fc0aff6a0ed412bdea2ab9e431dde77aa428986c18a3213be4`  
		Last Modified: Tue, 24 Feb 2026 19:26:46 GMT  
		Size: 66.2 MB (66193259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a7f63112bd7450bbe65e2f7015fab10379c1444489552f399394043c0c8ae1`  
		Last Modified: Tue, 24 Feb 2026 20:10:17 GMT  
		Size: 8.2 MB (8240128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:b8c5d19d5f4b41438978673286afc2e83bf59e83997c5ed1da67e03d9fd21a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3891022946fabee0c936d4c51330050ffa99194d1052c1dbb85bf4a956636908`

```dockerfile
```

-	Layers:
	-	`sha256:1f0e62e4bab15da1600e3deac65447e8898006ab75fedd113644919216f1157b`  
		Last Modified: Tue, 24 Feb 2026 20:10:17 GMT  
		Size: 3.8 MB (3828973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b033fc16481f992c3d7c871f387a3ff5a18cdadc487c3db16c730c0dc38099`  
		Last Modified: Tue, 24 Feb 2026 20:10:17 GMT  
		Size: 9.7 KB (9719 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:04575d4b410631ea571c6a2d037956872226100aa4782448268f3df09d8c132d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127836868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c032f5ffcc0bc3acbbd43d6ffe7e1451b40ef326ce568b0482c626218d42824`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Mon, 23 Feb 2026 21:39:58 GMT
ENV OTP_VERSION=27.3.4.8 REBAR3_VERSION=3.26.0
# Mon, 23 Feb 2026 21:39:58 GMT
LABEL org.opencontainers.image.version=27.3.4.8
# Mon, 23 Feb 2026 21:39:58 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="354243af8095a5e567931490b7b0ffe7b22cf12ee49b65c36e9187501ca03e8e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:39:58 GMT
CMD ["erl"]
# Mon, 23 Feb 2026 22:14:48 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Mon, 23 Feb 2026 22:14:48 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 22:14:48 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a9830e4eb2e957070da9f2df29f346a3f04891dcf11ba9407dd959d586791a`  
		Last Modified: Mon, 23 Feb 2026 21:40:25 GMT  
		Size: 67.3 MB (67268833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5dea17c12bb07cfeee4b13b12633b0e0abc6033ab4203bf17d9f477d5fa6597`  
		Last Modified: Mon, 23 Feb 2026 22:15:06 GMT  
		Size: 8.2 MB (8240746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:ae39d953dff68248016346eb78383d4f2e9387c45d9be149772adab3fe05c55d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3846035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d35f44d67fbdae9bf42a14f5f9ffd18ecd830e209faa3a6626ef29658e06d79`

```dockerfile
```

-	Layers:
	-	`sha256:47a84c459cf377c428caa8b41a5443d1eb0f3ebf45b192cf9b81c5839207c9e2`  
		Last Modified: Mon, 23 Feb 2026 22:15:06 GMT  
		Size: 3.8 MB (3836251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1578b9a5019611324960bb6c187477a094e5777f93d0cb3f4fb6fdb7e1439c4d`  
		Last Modified: Mon, 23 Feb 2026 22:15:05 GMT  
		Size: 9.8 KB (9784 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-27-slim` - linux; s390x

```console
$ docker pull elixir@sha256:736592c400c2b70e57ba72974206243c72eed2de7e2140f9895292db4f6d1231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121316546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81fd1880e48e05a0d10971759c2a8b542ad5077291aa02e09efe91b330d5df7`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Mon, 23 Feb 2026 21:35:41 GMT
ENV OTP_VERSION=27.3.4.8 REBAR3_VERSION=3.26.0
# Mon, 23 Feb 2026 21:35:41 GMT
LABEL org.opencontainers.image.version=27.3.4.8
# Mon, 23 Feb 2026 21:35:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="354243af8095a5e567931490b7b0ffe7b22cf12ee49b65c36e9187501ca03e8e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:35:41 GMT
CMD ["erl"]
# Mon, 23 Feb 2026 21:44:26 GMT
ENV ELIXIR_VERSION=v1.19.5 LANG=C.UTF-8
# Mon, 23 Feb 2026 21:44:26 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="10750b8bd74b10ac1e25afab6df03e3d86999890fa359b5f02aa81de18a78e36" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 21:44:26 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e35f2380f5dd985131a6ddf3b20e78a1efd418e948a1640d0ac114deb16e39`  
		Last Modified: Mon, 23 Feb 2026 21:36:11 GMT  
		Size: 65.9 MB (65937773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4234ddb28d4646662be5fcd6a1f901b144cb1af8a1e76554cecb0f9d5c86f75`  
		Last Modified: Mon, 23 Feb 2026 21:44:43 GMT  
		Size: 8.2 MB (8240430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-27-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:449b7fb83154791f28a3ecfa969022825d2f5c34d2254553708ccdc33e47bd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d05d4ae20c0c6582329c560ee2de3bb687cfcd649a122bef75bbe789918178`

```dockerfile
```

-	Layers:
	-	`sha256:f240bcbbe155d0ec7c88997c20d1ce35fc152743c553edee8a8e955fec77959d`  
		Last Modified: Mon, 23 Feb 2026 21:44:43 GMT  
		Size: 3.8 MB (3828635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac9fa5c6ef50c4c261b87ade7497d2cf63010bd00e9ac9a434d1de3a38695af2`  
		Last Modified: Mon, 23 Feb 2026 21:44:43 GMT  
		Size: 9.7 KB (9745 bytes)  
		MIME: application/vnd.in-toto+json
