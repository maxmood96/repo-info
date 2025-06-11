## `erlang:slim`

```console
$ docker pull erlang@sha256:093329bce41b575f3b2a4c7532d9252fbfcae12aa3eca5e9bcdaf9c02243e3ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `erlang:slim` - linux; amd64

```console
$ docker pull erlang@sha256:0b70cd2aaff09e3af5e182641f03ab3e7bd506ea7aa121d24ccad53f3e3f32b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128328971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163be2164b890a2f282eacb864e67ed95e902654cf26e5b888e15d337efedf59`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 22 May 2025 12:07:47 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a079fc42b6e6fdc2b7d095ae6e5d2a10faa8a3b589b0eef3a28d112c72d994b0`  
		Last Modified: Wed, 11 Jun 2025 00:12:48 GMT  
		Size: 79.8 MB (79834699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:355e72423acb3c2903ed5c6fa63b06fec56a66a58132f095d38e19c146cd9184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ea945d7b5c0e90b9051bbc7032dce8341e5e24137b821219c4cba7e21afeb5`

```dockerfile
```

-	Layers:
	-	`sha256:f334ac9c30d6ba944eca7f58aa0a95db9a4fa1cd91a04f2c810d5e7b1ba1e79e`  
		Last Modified: Wed, 11 Jun 2025 01:47:47 GMT  
		Size: 3.8 MB (3817575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8024830e4270629c2a6e21d1b129f0e7da97678f569b74cd4bb828e574366c`  
		Last Modified: Wed, 11 Jun 2025 01:47:48 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:694a038a9cc1997623e0728e86da395671452d25b43f864321bd780ad6d6be2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115539083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d844d0b18bb40626892bf623e8b27d687c09e7ea29a18ba084697d93fe8f83`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 22 May 2025 12:07:47 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fe4bc1cbdee9e4aabbc6c58a2156f300e4c3158cfb501698b1878215892a8763`  
		Last Modified: Wed, 11 Jun 2025 00:30:31 GMT  
		Size: 46.0 MB (46026587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291054a07089a69e3ce135e3af12f92e2bb77fd9a76db3b9dce8e82cc86ba683`  
		Last Modified: Wed, 11 Jun 2025 03:17:03 GMT  
		Size: 69.5 MB (69512496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:bad7e6737c640fe63305a78e85f5f7186e913213087ffbe337e0ef2951ff460c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcaefe288512ba695867b1661df392ea3f38a783e21d2f6529d1b46652ed41cd`

```dockerfile
```

-	Layers:
	-	`sha256:6fd03115ae1a53144319585ff6790be6ead5c55e1c9cec191751aadc8a1a2d5e`  
		Last Modified: Wed, 11 Jun 2025 04:48:34 GMT  
		Size: 3.8 MB (3821391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba5fed47a3ebaf9cd36d49d4e2644b11e57716bdd12a0502c48c35e090007e65`  
		Last Modified: Wed, 11 Jun 2025 04:48:35 GMT  
		Size: 14.0 KB (14049 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:d89f89db52e7d077bdf8919619aba04884c7b55e36959fdfd5fbc79fd498332d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113125386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068c7dc49ab3828ea9af49487fea2f538858f50a481eb12273380d81372e6046`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 22 May 2025 12:07:47 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cc47439c21644fb4f89a06147ca284b794e14bac1f3d6a85b0a0673bef974c`  
		Last Modified: Wed, 11 Jun 2025 05:06:42 GMT  
		Size: 68.9 MB (68917176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7f81c8bf8d7ca3e7e6afd6bc333cfcb4c65c49f488021526fc1c10f6f2ce8459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5680b227f91d41338df5f9e742135292263ceb9c65bb6d35b3d34183616c8e1`

```dockerfile
```

-	Layers:
	-	`sha256:9cccc092ceace810f50c24d6def3e59e292c1a3a73ecc9e773a5b77be6d496c6`  
		Last Modified: Wed, 11 Jun 2025 07:47:46 GMT  
		Size: 3.8 MB (3819816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a7d58e9f8311be6f2da78ae57121fff58bb936837f4581298b432809e1d68ff`  
		Last Modified: Wed, 11 Jun 2025 07:47:47 GMT  
		Size: 14.0 KB (14048 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f33f733a7694fec425bfd5543e43b03941c1f7d2cdb2a2b03f873fa078e34b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125968720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f01e5046f9f53df33129f5bdd4f1244cb7b8b6cb00702c011556ad2d10d4602`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 22 May 2025 12:07:47 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eea0493cb17f2e8943b73497195ae4124f2b7cf7ba2c14c3231e529820fa892`  
		Last Modified: Wed, 11 Jun 2025 03:05:54 GMT  
		Size: 77.6 MB (77629868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d89e7508e2b86556b5343935814b2f20e0014c5501a988da80320b42365bc787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089c6812e2b0c8e917c281a16273fcf2944440059aadfda8b44b19acde1668e7`

```dockerfile
```

-	Layers:
	-	`sha256:a6b0a4b22e8405094a916eb37ae7c12a66e7a017aa39d90114cbd3ebd3b641c8`  
		Last Modified: Wed, 11 Jun 2025 04:48:42 GMT  
		Size: 3.8 MB (3817848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ef87f2bbbaa10202e272d4e8ddbf5045e5e4eaa2c9fe9e0da6e4f40f1c6aff`  
		Last Modified: Wed, 11 Jun 2025 04:48:43 GMT  
		Size: 14.1 KB (14081 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:2c05d255ba459d644d15c679e889312e3343a9ce59fc2ef5a7d8d20ffadb60cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119525818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0a236cedb79e71c47efea0f9eafe7059f2feb63b80414c15fe0ef5fb3117a3`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 22 May 2025 12:07:47 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe04d804d5c2eb71dd0442ee0b7f4c88d270098b93419218fbdea4af53beb73`  
		Last Modified: Tue, 10 Jun 2025 23:39:26 GMT  
		Size: 70.0 MB (70048344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:907619a392bfa383118a6a8cc78ea7da3daf05d11a5ad004669afc522b3c6bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e68274f30f0255b46260c6f3e322258d5275a1fd1140082653296a87be3f07c`

```dockerfile
```

-	Layers:
	-	`sha256:0b16c98e963cebb5c7e1653e9ddb073feb7e2ea4ee76c068087d0b18c00c2fec`  
		Last Modified: Wed, 11 Jun 2025 01:48:13 GMT  
		Size: 3.8 MB (3814737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45409250402a194d8b75fac28e7ccadf0b669a245850eb5ae8c64bb1ab043c3e`  
		Last Modified: Wed, 11 Jun 2025 01:48:14 GMT  
		Size: 13.9 KB (13928 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; mips64le

```console
$ docker pull erlang@sha256:2ff9df14514effa3a38632939f14dbaad2d8b5eecac16551390a7b7d6fc63ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118752849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64351edd35a81e334535535520c85253ab947e83e508ca9ea41a9b5aa18bb8ed`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d480a40975e955224ed64be37e82f220f731f0379d20a7b8c36be0e47e31d8df`  
		Last Modified: Tue, 03 Jun 2025 14:36:18 GMT  
		Size: 48.8 MB (48769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f78183eb7a632b7f8a07be89d4adbf76f64d751a359289eff75a1001013d2f9`  
		Last Modified: Fri, 23 May 2025 04:56:59 GMT  
		Size: 70.0 MB (69983096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:24556f34ec03fd8cb5d0a3d5b80eac65c511c7e4fe80d5c417ff1dccff76a37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6767c6c70a6452f844cb40f7f691969f5a76ba87cb0291437077731edaac9554`

```dockerfile
```

-	Layers:
	-	`sha256:2565619da21dd0e74b34140858329eba1e3b302d664c4055884454ed4756ea3a`  
		Last Modified: Wed, 11 Jun 2025 01:48:19 GMT  
		Size: 13.8 KB (13825 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:bd6cec462fb888525d42650291d38bb71ed27f9b1863b21b88becc6263a47dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123402823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7454eb831c47ab7e1c64b52ed36c4c1056246d85e21f30e170f2e9e7e85bdf7`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 22 May 2025 12:07:47 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee74a28f2507fc0b6b0ee7c533de3d004b6e5c03135f49a03f9e65832deb5c74`  
		Last Modified: Wed, 11 Jun 2025 04:59:23 GMT  
		Size: 71.1 MB (71065466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:15c9fa8d05ee6db3008a5ec6a4441d6e26ec3181797ec3417101407848e8014c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148c00b288a50373f935d5af97c831daaf53679d193f4b77cc4604619923821c`

```dockerfile
```

-	Layers:
	-	`sha256:f76df546d353a4385680917f903876944bdb4e4a07908d34cfa11bce40042e5a`  
		Last Modified: Wed, 11 Jun 2025 07:47:59 GMT  
		Size: 3.8 MB (3822019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97533fd6263aacec0c0e4a46a4492e0627430c25e708f5028b43465c53e33f44`  
		Last Modified: Wed, 11 Jun 2025 07:48:00 GMT  
		Size: 14.0 KB (14015 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:e71728a5dd0050ffe2b3b022ead6c339c7d2e7f263458cb8c0582c806de6a9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116822805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed7fd1f19b91627dd2ddd46f3dbdfac41d49dbb911b4e1256c70730f8860536`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 22 May 2025 12:07:47 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77316a4b22ffacff52f6706eeb48e693c255f6099ea5bba93b23ee09f950ca96`  
		Last Modified: Wed, 11 Jun 2025 02:57:37 GMT  
		Size: 69.7 MB (69673397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9818d1f883b9307859a0c93b9abd64c12550125800b219205111906693b96e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6b5994f339f38d4f010a199e6d002816e3e55d30b908050277fead2b31f4d0`

```dockerfile
```

-	Layers:
	-	`sha256:7d2102d206756107c43b04ebd7a2f20b74e4c66704989300c96a8c3e86207178`  
		Last Modified: Wed, 11 Jun 2025 04:48:56 GMT  
		Size: 3.8 MB (3814403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5840861e280e90946831700ea847beade5721f158de2768143af8bb2b3ccadd6`  
		Last Modified: Wed, 11 Jun 2025 04:48:57 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json
