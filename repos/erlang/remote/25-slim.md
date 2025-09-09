## `erlang:25-slim`

```console
$ docker pull erlang@sha256:b848e564410e21f5901e8e8f59d6914aba58956e8726cccb76d880a9ee28ffe7
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
$ docker pull erlang@sha256:d44eaaa4b8df3eba5dce566bac8201f3023714ced1a552a8170c4ae80ce9d27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119712609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9916fdb0337ea4d5bece0962af499c597ccbbcc44d7e82bf944902e075b2ba9a`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Jul 2025 17:34:23 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Wed, 09 Jul 2025 17:34:23 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Wed, 09 Jul 2025 17:34:23 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Wed, 09 Jul 2025 17:34:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 17:34:23 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6253fa86209404c0c2c8c5700f56d5fc70e3bee96b511ff41e2cd14757475a`  
		Last Modified: Mon, 08 Sep 2025 22:02:10 GMT  
		Size: 66.0 MB (65957213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:39f7fbbeff20f276707feccc6f29f44093c6ff322118f2251b7345573e837bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69fde3bc738f059b4202683bb1b4d3fc8672a765811106819293e3e826b7272`

```dockerfile
```

-	Layers:
	-	`sha256:504e90a547dc32109ff88893d8bf161c85f6421f4bb9c09e5a71cdcee8e44c77`  
		Last Modified: Mon, 08 Sep 2025 22:46:48 GMT  
		Size: 4.1 MB (4098886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84da31db500b12d56ea76bef2697a6eb95e4ab2d0693890f3cb161f0c0ce8e31`  
		Last Modified: Mon, 08 Sep 2025 22:46:48 GMT  
		Size: 13.6 KB (13611 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:eb759843dfa628c2ea700fcfa387efc33903d4ee2cc6e710d6e9aef9d5ce98c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106313968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec8fdb37e5d4a4ee43e1f72d347ad85aff12ade6bfd38f58ab78d7a1d8e1e80`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Jul 2025 17:34:23 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1757289600'
# Wed, 09 Jul 2025 17:34:23 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Wed, 09 Jul 2025 17:34:23 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Wed, 09 Jul 2025 17:34:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 17:34:23 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8274f5d2891e4b4a199e88ea54bf64be2b431cff01268ebaebfacd12519d655d`  
		Last Modified: Mon, 08 Sep 2025 21:14:50 GMT  
		Size: 49.0 MB (49044356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4de055622a04b3df353b8ef5fcd97abb773f62e247f8b34fbad7a6ef7659700`  
		Last Modified: Mon, 08 Sep 2025 22:50:35 GMT  
		Size: 57.3 MB (57269612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a6d7881a6c14538facdefdff7a8836d758f101205d05e2bc8c9b51fa5771b95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9749b38b66665dafbea96dfdb8cdb513193ea3eaaa8c1428aa886ffce4d34db9`

```dockerfile
```

-	Layers:
	-	`sha256:39dead494250e443f5e3667e85540804f180e4d3f7a6e034da703979a6a24ca7`  
		Last Modified: Tue, 09 Sep 2025 01:47:00 GMT  
		Size: 4.1 MB (4100487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5aad0ed1385fb75fd4de351782209cfc09904b243e5d7df8e9ad76e11cb7a71`  
		Last Modified: Tue, 09 Sep 2025 01:47:01 GMT  
		Size: 13.7 KB (13691 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:8ce82624f6f7da5089a0345203bcdd3efe8cc6047783e06af7a14e98ad7e39b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116597112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166539ef97e0fd704664596da38fa9698c5946929199a33227e9d2f728b74830`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Jul 2025 17:34:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Wed, 09 Jul 2025 17:34:23 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Wed, 09 Jul 2025 17:34:23 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Wed, 09 Jul 2025 17:34:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 17:34:23 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39321b5162623e03059636e5a95a11ef3c44f9622540e096e1401ceed82a2a6`  
		Last Modified: Tue, 09 Sep 2025 01:46:08 GMT  
		Size: 64.3 MB (64348742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:86e2df8855859d8d2d9876480a2e3fdb5cc90d4cf0038939160c60412f205ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9f9ab38d61a61b4e602e1d74feb64cf1c4d941118fb41eb8fb09413ee35e18`

```dockerfile
```

-	Layers:
	-	`sha256:917a8dd00e81b36df9207d732cad9e89282b3231793146631a89f158309e2c7a`  
		Last Modified: Mon, 08 Sep 2025 22:46:59 GMT  
		Size: 4.1 MB (4098507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e478922ee552941b52c88a8f166701b3923d8bc77f6cd071efe82746ef309a0`  
		Last Modified: Mon, 08 Sep 2025 22:47:00 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; 386

```console
$ docker pull erlang@sha256:d343e59118abb29d1ba3c32529a3b895ec7bf5f01f131458c636f6e67159f91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112330311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955d3e7e9f49369ca93c45862b37147a0cd5315191c8e3e1f7d6196f77ae648d`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 09 Jul 2025 17:34:23 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1757289600'
# Wed, 09 Jul 2025 17:34:23 GMT
ENV OTP_VERSION=25.3.2.21 REBAR3_VERSION=3.24.0
# Wed, 09 Jul 2025 17:34:23 GMT
LABEL org.opencontainers.image.version=25.3.2.21
# Wed, 09 Jul 2025 17:34:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="6761432927a9be4f5c13c4019acd6fa3d2f4363198f790947328023aece1986f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 09 Jul 2025 17:34:23 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:21d761bd0e7544a956d2e6eb27c7a89e081fa93136574d1836ddae535c60eb08`  
		Last Modified: Mon, 08 Sep 2025 21:20:56 GMT  
		Size: 54.7 MB (54690513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8251a0aa087c5ee42afea4f09d3fe443597bf116b596507d8233b46f3a51bca6`  
		Last Modified: Mon, 08 Sep 2025 22:01:49 GMT  
		Size: 57.6 MB (57639798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:8622b7a3bf43c05af7e6f4a8ba1fc36da90a72197443860c66f529a1ab2f9adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f16093b0f7481fee5a545965b4cb7bea0ddbf7f01b42bb544fc78d7b48d8bc`

```dockerfile
```

-	Layers:
	-	`sha256:421fbac5fef6d3df59b9754db6eae07a49f0906313c21ee8abecca562c882b0e`  
		Last Modified: Mon, 08 Sep 2025 22:47:05 GMT  
		Size: 4.1 MB (4095414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10861cc7be4db62df4f4cf95018f7abb11d307b0e45f51d3a76fd939135c0a26`  
		Last Modified: Mon, 08 Sep 2025 22:47:06 GMT  
		Size: 13.6 KB (13579 bytes)  
		MIME: application/vnd.in-toto+json
