## `erlang:25-slim`

```console
$ docker pull erlang@sha256:5eab3959e3bf5613143931595e4806968be3c43312cc55080339aca6cb0fcbaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `erlang:25-slim` - linux; amd64

```console
$ docker pull erlang@sha256:595b600b885435b4f6f4e9f8abbdf460435b1d831ff03c91a9a156257758059b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119718662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddac3c29f6f1fd172e7a21e95466245f5dd0c4e4a0e622f23476cb7dc93292e`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:43:58 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Wed, 22 Apr 2026 01:43:58 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Wed, 22 Apr 2026 01:43:58 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:58 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99245d1ccb4a17929806e4127338077a76e8222d3e9ff47e6360d00827e87c8`  
		Last Modified: Wed, 22 Apr 2026 01:44:12 GMT  
		Size: 66.0 MB (65955510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d9890186cf5f5e575256af2578a339f1f3da1e2742af8295d709c740ab92220a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe83ea184bec7a489b1b30d1a3f2e0b7785bb6c86da7bdf90a36256008a113d`

```dockerfile
```

-	Layers:
	-	`sha256:48f5065ad69358eb602616d57f4e08ddd0c75645806f1e19bf23465770888379`  
		Last Modified: Wed, 22 Apr 2026 01:44:10 GMT  
		Size: 4.1 MB (4098886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6164ada4a4e45ddc3cd9ee2a97ccac2a94f5bde8dec0ab84d680414da91a2b`  
		Last Modified: Wed, 22 Apr 2026 01:44:10 GMT  
		Size: 13.6 KB (13568 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:85f0869b30d4deadc19452294ab3b9faa7f25a6a4dae8837eb7031cd64bd5c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106322027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f467a5ea94b7afe14a5f8d3809b8b6c1bd85e5e6ce6a5cfb1592629ee1459c9c`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:14:25 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Tue, 07 Apr 2026 02:14:25 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Tue, 07 Apr 2026 02:14:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:14:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:dc8695d526078f14ae00d8def0c6b77226df91b02937f7fe93806b494d0eed07`  
		Last Modified: Tue, 07 Apr 2026 00:59:40 GMT  
		Size: 49.1 MB (49053930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb76dcb33ceb83c4a141da727071e2ea50d5e400d55ae06e15bb01e7432061d`  
		Last Modified: Tue, 07 Apr 2026 02:14:38 GMT  
		Size: 57.3 MB (57268097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:eb5892bc853f5914ee123f292df493e3527f3e3fae309a8bd742aa9d639823b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4030ee5b830d07e1576240b3739d6fe9e395265c3d43e8a0b2ed6a3f2e157f65`

```dockerfile
```

-	Layers:
	-	`sha256:53bd058b6e0650cfb954a113a6004a23e02f3e917d33de8c7baeef1d59f1e521`  
		Last Modified: Tue, 07 Apr 2026 02:14:37 GMT  
		Size: 4.1 MB (4100487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad8ad44ffeb316165136d72474f05a19d9065f2d0a2bef026e51cc942b3d2d3b`  
		Last Modified: Tue, 07 Apr 2026 02:14:37 GMT  
		Size: 13.6 KB (13648 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bb73d5ea38e1765c2a68f9dd6c427f66634f04b452fed373818524c47ff6d46a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116594399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7703ba1d37b9398dda953b659286b11d3cd847afcfdba7f238c52fca9eb5cc3`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:59:08 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Tue, 07 Apr 2026 01:59:08 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Tue, 07 Apr 2026 01:59:08 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:08 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08be1c1814607d7bf3bc93f8a6a811bc42b8334f78569d6d9625ac98a5e84d51`  
		Last Modified: Tue, 07 Apr 2026 01:59:23 GMT  
		Size: 64.3 MB (64346784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:df6e334a3e46955188c02f24bb630e2b44d028fc26ce74c509d76d18f9325c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bcc3cde24c3b4ab066498282da04c66f75582604390b91247b84b4c83ca345`

```dockerfile
```

-	Layers:
	-	`sha256:72fdcb9cbf420f6a10d1f0b7cbdc42940af1cd92a8ab3f839292372beee52d6f`  
		Last Modified: Tue, 07 Apr 2026 01:59:22 GMT  
		Size: 4.1 MB (4098507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23185e313e7a316b4a92d48d12a999f570373553f6011a1d03fe5c6fded8299e`  
		Last Modified: Tue, 07 Apr 2026 01:59:22 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; 386

```console
$ docker pull erlang@sha256:da1e939af6d2f8ca10691f1d95346f01c65c583ee4dba92004d1d2dd9e4c1f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112340875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd767b1cf57828b715d3a322eaafb70401ed50db137c59027c503fd6f007b828`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:50:37 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Tue, 07 Apr 2026 01:50:37 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Tue, 07 Apr 2026 01:50:37 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:50:37 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:17c3ebdef14b8265937ec7a01f6bd551a86fc0903b2144405f77b14942f88fac`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 54.7 MB (54702589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a673b93146042960cb7705440d86161412ac98f0d91588d60305627703f4f3`  
		Last Modified: Tue, 07 Apr 2026 01:50:48 GMT  
		Size: 57.6 MB (57638286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9221400c797533572d7d0a12d790f514bc8a73bb8512305c907fe03a65b4ba74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf56efcdf14fb7e947b34599e03ec89480115e5baca244d26d5c0c1e1345dc6`

```dockerfile
```

-	Layers:
	-	`sha256:76c188fadc16f340ac7f1aa750c2c4309dd45bd42bd9bb13fbff33f780df4a16`  
		Last Modified: Tue, 07 Apr 2026 01:50:47 GMT  
		Size: 4.1 MB (4095414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1341e30e1d9aff2ab84eb6848b90491c17ceb135b5f18dddadd980bb0a1a39a0`  
		Last Modified: Tue, 07 Apr 2026 01:50:47 GMT  
		Size: 13.5 KB (13536 bytes)  
		MIME: application/vnd.in-toto+json
