## `erlang:25-slim`

```console
$ docker pull erlang@sha256:a9bb137b43b2ff04f59ccf932221e4be18469ae7374078c9fbb9dbe954a2b210
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
$ docker pull erlang@sha256:a7ac196bb0848939869bc0f93556608545f3dc6ebbabf80acf75fce9b86f582c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119711783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748a3ee72286166ca0b533c8dd6efc297503820f03a7067bc7922ba697ef894c`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3975946b691f8ce28f4c41f876802b1548351e2671b2203170aba0e25fbb85`  
		Last Modified: Wed, 09 Jul 2025 20:43:43 GMT  
		Size: 66.0 MB (65956961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a534a1650ae8f96a7e03008da541995cb89171282c18cd0c386b6efa82c95973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4eab70a5e3e49bcd8194326ddfb9b29bff440aeb1e17facedd89e56f73af1c2`

```dockerfile
```

-	Layers:
	-	`sha256:d037e6ae558427165858a4c32cc2de2ece05bff9744e7b560a1ccc8f006c275a`  
		Last Modified: Wed, 09 Jul 2025 22:46:57 GMT  
		Size: 4.1 MB (4098886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c09dbac609621b471d9bbf48201409d121a15f459134eb28297eddccf379fa1`  
		Last Modified: Wed, 09 Jul 2025 22:46:58 GMT  
		Size: 13.6 KB (13611 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:b361bf1ff538875d34cfd82ac0e2493159809ee8abb7a620c26e45a6d9d4e86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106313385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf64fbb7929efc048de5d0702aa92d4c6a7b529b862d5dd896ef9490e8b9a00b`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1751241600'
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
	-	`sha256:efcf40eae0046ccd92d3b47ff685e1e9cf7a34d0a92f6de893078f115e01f20f`  
		Last Modified: Tue, 01 Jul 2025 01:15:14 GMT  
		Size: 49.0 MB (49043960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc08306aaee193098a76134e7851fbe10dc064775b0f58258a420e5ce9322a7`  
		Last Modified: Wed, 09 Jul 2025 21:19:40 GMT  
		Size: 57.3 MB (57269425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:398fbf97dd96bbccc1af661b9145060281ba8df7114ae4d3cba44b23d10900ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa665a17c8b5b26207f4d4e1c69e9c8c4a9e6f2e63ef4cf9066d41f56fd385b`

```dockerfile
```

-	Layers:
	-	`sha256:6cd55a2ba46736af7fc418f0df1c93383156caa724d25ce9d0b8522f89f3e868`  
		Last Modified: Wed, 09 Jul 2025 22:47:03 GMT  
		Size: 4.1 MB (4100487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36702e02ab56d00d67a286f7ce7fcddda258725491a07ece9339b01d53e00ecd`  
		Last Modified: Wed, 09 Jul 2025 22:47:03 GMT  
		Size: 13.7 KB (13687 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:94adfba3f7880de6789d7a7b59905183af28bc20eb7d127f1e8f93b762930fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116600991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87462909668db4e08232fb3674b08541f2efdd1eef8439e5a5726faaafbcfa02`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5deb4933c663264ad754f588a45db47aa7993e0df3cb8eeea6b662c6eb9ab4`  
		Last Modified: Wed, 09 Jul 2025 21:13:05 GMT  
		Size: 64.3 MB (64348737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:17bfb2c66dec4b635b95ad6cf4be3da1393b3b9298df253ecf382a4ff869aea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd39a8c815948698eeb9cedffe8f27f126d0a159ad955fa1902b0b25b001db3`

```dockerfile
```

-	Layers:
	-	`sha256:91e1f395091058bb024cb5964bb2d720939e39ad68d2287aebcd6e8fbd780e57`  
		Last Modified: Wed, 09 Jul 2025 22:47:09 GMT  
		Size: 4.1 MB (4098507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c4a3c09a5d966ebd4b100a50941fe73d1a008843558b98ade3986c8e91916dd`  
		Last Modified: Wed, 09 Jul 2025 22:47:10 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; 386

```console
$ docker pull erlang@sha256:f1eb3b6f6c8a9d7fc9aa147c306a0d8ee6368c88e8284804a0846e11e2df0d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112329814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:154367c8f934b8ca251fcd1842eec78b8f6578697a96192ace79081d6199b79d`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
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
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086849d90fd0326e5298656d68c167568974d02f34eb0515b82e4fbab3f3c9e4`  
		Last Modified: Wed, 09 Jul 2025 20:44:05 GMT  
		Size: 57.6 MB (57639880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4dad98f4101c22f35e20b31efa746c2d56ea76312ef8aa550f54b2552bdeb914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d636a24a7035e56c8478d502443912c54e6ac9da0531df477e9d894ac67b75cb`

```dockerfile
```

-	Layers:
	-	`sha256:88f0ee1fad3395cd2a332ab7b13f8ac66f7fa1f777375d6382fbae017f39c36a`  
		Last Modified: Wed, 09 Jul 2025 22:47:13 GMT  
		Size: 4.1 MB (4095414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8dc1fae6ef29e141af73a259934dcf9b00ab51b90913b2094245aef2248ac94`  
		Last Modified: Wed, 09 Jul 2025 22:47:14 GMT  
		Size: 13.6 KB (13579 bytes)  
		MIME: application/vnd.in-toto+json
