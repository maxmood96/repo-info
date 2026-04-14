## `erlang:27-slim`

```console
$ docker pull erlang@sha256:85fbf09eb259f0a382e90d24a3a382c0795f872a8f36bdb7dbf4ac9894efccb2
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

### `erlang:27-slim` - linux; amd64

```console
$ docker pull erlang@sha256:8a1da5b120e9baf924022c1379e27d8dc994c5344ca9ce6b9944aebc98d6616d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124542623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2081add0dba5ab19df7e8b48090812b50d0f16c11f1062f5c6a3a6fe2aa09f2`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Mon, 13 Apr 2026 20:49:05 GMT
ENV OTP_VERSION=27.3.4.10 REBAR3_VERSION=3.26.0
# Mon, 13 Apr 2026 20:49:05 GMT
LABEL org.opencontainers.image.version=27.3.4.10
# Mon, 13 Apr 2026 20:49:05 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c93905c73ddb7afdfc7f0a46c33f95590eeffe9c2a8c75086d24bb9fe8abe029" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 20:49:05 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77566afe4a6fa57ecb427d928338fea682deed5f2747a489644e9435a4dc27e`  
		Last Modified: Mon, 13 Apr 2026 20:49:19 GMT  
		Size: 76.1 MB (76053800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d47fb5f750c9add2377c7fd88db93ffdffe9b0c131faea4c4cd7c2b4fe2433cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8aa591c9ed3dde89bb3fa69bde4095a650056852fb621e7dbf5f58f80acab5d`

```dockerfile
```

-	Layers:
	-	`sha256:ac5b32cbb2d331d66b09d5b5ab464d36d335c60c75a7b27fbb132fba7bf8c19d`  
		Last Modified: Mon, 13 Apr 2026 20:49:18 GMT  
		Size: 3.8 MB (3824787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f887e018b6176d6e76168dafc8e9b5c3c83d456097a4988af14f03340f87abb9`  
		Last Modified: Mon, 13 Apr 2026 20:49:17 GMT  
		Size: 13.6 KB (13639 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:0a20940324bedc09a0cf8f6b3f85c662328305f50e9c0d02e02f7fc597ef731d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111572036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603941801b201bc917f8fb78ecb282294f689aa1a4ab2c788127e77fb1ca505f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Mon, 13 Apr 2026 21:14:07 GMT
ENV OTP_VERSION=27.3.4.10 REBAR3_VERSION=3.26.0
# Mon, 13 Apr 2026 21:14:07 GMT
LABEL org.opencontainers.image.version=27.3.4.10
# Mon, 13 Apr 2026 21:14:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c93905c73ddb7afdfc7f0a46c33f95590eeffe9c2a8c75086d24bb9fe8abe029" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 21:14:07 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c4564d3f444801f4c4ab3e01fd62e7dd3bd91054769ac22888b9bef61823a830`  
		Last Modified: Tue, 07 Apr 2026 00:10:20 GMT  
		Size: 46.0 MB (46021666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695458fc71724e27e356658d4ae893edb281f834130bff58c5af86ceb6d70f8f`  
		Last Modified: Mon, 13 Apr 2026 21:14:24 GMT  
		Size: 65.6 MB (65550370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0833eaf66fa5794f47002a94dc3f04d70130d24764f32dc1c7620d109cc14c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301dad40c22694e90f06c1b44790e9d517cea17115cbf0c240d6345fe8ec5c89`

```dockerfile
```

-	Layers:
	-	`sha256:052ca1a5567cbc17b8b8e08f4ab1d6db7f759598d4a9708bbe3302b72d8e8f24`  
		Last Modified: Mon, 13 Apr 2026 21:14:19 GMT  
		Size: 3.8 MB (3828595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a895ac52b6246935fc651a5d42d6eafbf604f3780ae3c55fce0adc6ea7e2c19`  
		Last Modified: Mon, 13 Apr 2026 21:14:19 GMT  
		Size: 13.7 KB (13719 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:4661ac0f89a4e2214c60e9976605fa6b36aa45006eec50dfedf2d098135fad39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109390323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b610a82448064c36ef49f8714a6ba4365c6016ac8998aa715114dd39f593dab9`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Mon, 13 Apr 2026 21:01:30 GMT
ENV OTP_VERSION=27.3.4.10 REBAR3_VERSION=3.26.0
# Mon, 13 Apr 2026 21:01:30 GMT
LABEL org.opencontainers.image.version=27.3.4.10
# Mon, 13 Apr 2026 21:01:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c93905c73ddb7afdfc7f0a46c33f95590eeffe9c2a8c75086d24bb9fe8abe029" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 21:01:30 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c1ace4017cae0729a37718487810d93b8a886e82c4685cb311c27c88d7a830`  
		Last Modified: Mon, 13 Apr 2026 21:01:44 GMT  
		Size: 65.2 MB (65182506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d30a8f2dc4c5e83bd4ff9fde014dc47602787a6f26f22a5c167636c83b328d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0788d4f4ea654573a00afb00d0353e7b29a05483a17905fca46b2ccc1f37dd82`

```dockerfile
```

-	Layers:
	-	`sha256:c348908ad4c2498d5dde7457af9cd811d33b6ead8257a409323e59d862c6288f`  
		Last Modified: Mon, 13 Apr 2026 21:01:42 GMT  
		Size: 3.8 MB (3827020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:719d03067decb104d03ac561d4cad0c9821c243d333703e671c1ded1e473183d`  
		Last Modified: Mon, 13 Apr 2026 21:01:42 GMT  
		Size: 13.7 KB (13718 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:b8b679aae32bc91e69fb9fb00ed474e00c18c927c09ec59eb8b15857968d4892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122172581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcfe6e6bdf2b2e6f04bb6c7fff50ff9ede9c815c460dbb05ac892df66f094db`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Mon, 13 Apr 2026 20:54:15 GMT
ENV OTP_VERSION=27.3.4.10 REBAR3_VERSION=3.26.0
# Mon, 13 Apr 2026 20:54:15 GMT
LABEL org.opencontainers.image.version=27.3.4.10
# Mon, 13 Apr 2026 20:54:15 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c93905c73ddb7afdfc7f0a46c33f95590eeffe9c2a8c75086d24bb9fe8abe029" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 20:54:15 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36755a79b1b6f91f8357f75baa411b254c7893daada81b8db574c48ab1fc62b7`  
		Last Modified: Mon, 13 Apr 2026 20:54:31 GMT  
		Size: 73.8 MB (73799319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e3c8a212e62158a1eb3c278b8c9c330777a94232393ae7d8253dff9abf34af35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e34b98af1599e575d1aef0f554e36220b895ffeea1b7f5a163f4ede7720207`

```dockerfile
```

-	Layers:
	-	`sha256:09dc321f53571c4d7194f7eeb43b5c09fb2813cee6790d302579c611d3dad427`  
		Last Modified: Mon, 13 Apr 2026 20:54:29 GMT  
		Size: 3.8 MB (3825048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00c05e9183727b1cb75f4ef0f38251fc7b05fa57b0d5b8a34ea0849452de7a90`  
		Last Modified: Mon, 13 Apr 2026 20:54:28 GMT  
		Size: 13.7 KB (13743 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:d13d76b696e284743456eb8619d4d9f1969332946ade9b3320cb26f4e539e7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115689870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cd6fffe24d98f0850b4b935db574bc9957595cd5a55b15e1982a02044ebef2`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Mon, 13 Apr 2026 21:28:25 GMT
ENV OTP_VERSION=27.3.4.10 REBAR3_VERSION=3.26.0
# Mon, 13 Apr 2026 21:28:25 GMT
LABEL org.opencontainers.image.version=27.3.4.10
# Mon, 13 Apr 2026 21:28:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c93905c73ddb7afdfc7f0a46c33f95590eeffe9c2a8c75086d24bb9fe8abe029" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 21:28:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6b838e591408b61fcf923bcc567649c4053d737a0dcf488cb215bcd633b7d70f`  
		Last Modified: Tue, 07 Apr 2026 00:10:40 GMT  
		Size: 49.5 MB (49477915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1082e4be1f5a1aedaeeacad1519ef1f61b939457f47a3e9585c98dfcc2c98bf4`  
		Last Modified: Mon, 13 Apr 2026 21:28:39 GMT  
		Size: 66.2 MB (66211955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ff064e980ef07f08e255013176601f7211eb70cfff58e74ab2ffea8ab59c00fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288da0846511d383e758c7f0f99276bd8cd675c7064ae29022c50e9b1f8fa664`

```dockerfile
```

-	Layers:
	-	`sha256:687f2084b107f14e5f6074c685bbaf9cf72c373343bdb3921220f07037fee4f5`  
		Last Modified: Mon, 13 Apr 2026 21:28:37 GMT  
		Size: 3.8 MB (3821948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60c147f4f19a7043f03492a6f455006ec76cd7b2a61b4e12946a7ed9412b891`  
		Last Modified: Mon, 13 Apr 2026 21:28:37 GMT  
		Size: 13.6 KB (13607 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:d1950414aa08dd72cd23acec8e22198f30597e60c68d814049ba7b778af1c649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114912481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b437d690300b74f81a3d8335be28e1dab5c796ba1302642c985fd8e5977a52`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Mon, 13 Apr 2026 21:41:58 GMT
ENV OTP_VERSION=27.3.4.10 REBAR3_VERSION=3.26.0
# Mon, 13 Apr 2026 21:41:58 GMT
LABEL org.opencontainers.image.version=27.3.4.10
# Mon, 13 Apr 2026 21:41:58 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c93905c73ddb7afdfc7f0a46c33f95590eeffe9c2a8c75086d24bb9fe8abe029" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 21:41:58 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7a9b4a7963b008240d9a254ca4fd1193c938bed0a9c6fe9c04630f13b1a17a44`  
		Last Modified: Tue, 07 Apr 2026 00:09:37 GMT  
		Size: 48.8 MB (48782593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95e57c35b8a1959222092a4be893c8c96fac6879214ab113bd9cc45e555d840`  
		Last Modified: Mon, 13 Apr 2026 21:43:06 GMT  
		Size: 66.1 MB (66129888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d9be81f1883367f3c6581c4d4e90b672173ea26987bec13cecc5b175e023b7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61348920f38cc028a565182b291960c3ab7e8b915a09eb4389160db5e23093fc`

```dockerfile
```

-	Layers:
	-	`sha256:e4aa1c365967a2702d04b09a5e6446b8bcc179014e3ac53577156b2603e65b5a`  
		Last Modified: Mon, 13 Apr 2026 21:42:58 GMT  
		Size: 13.5 KB (13490 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:8ec4a2d57641d089c17eb255bcda4aede1b195ecf722ba329f04f551f68660d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119627088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909a1a06d9e73299ce0f4702d30917dc1193c2022243286f507c16aaf8487190`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Mon, 13 Apr 2026 20:59:13 GMT
ENV OTP_VERSION=27.3.4.10 REBAR3_VERSION=3.26.0
# Mon, 13 Apr 2026 20:59:13 GMT
LABEL org.opencontainers.image.version=27.3.4.10
# Mon, 13 Apr 2026 20:59:13 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c93905c73ddb7afdfc7f0a46c33f95590eeffe9c2a8c75086d24bb9fe8abe029" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 13 Apr 2026 20:59:13 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b71cf0072e5c3f929df087e53604bd8e3939b25d72e7e679866333fd55ee79b`  
		Last Modified: Mon, 13 Apr 2026 20:59:46 GMT  
		Size: 67.3 MB (67290150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:028616fff03ec93e7896120c49f5ea008693aca745b5ea8ecb77b4404e66fd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e645dc20f3d532fc429c9d6b3803431466893b476bc94a5c98785b5da4adec4`

```dockerfile
```

-	Layers:
	-	`sha256:f7be0a254b512db21c8de73ecc95440b79fb6517a33225df6874cefe2727e86d`  
		Last Modified: Mon, 13 Apr 2026 20:59:45 GMT  
		Size: 3.8 MB (3829237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87508e8271fb8770b3a170ce64360c8c472d386e4f2e830c5ef66011edb7a065`  
		Last Modified: Mon, 13 Apr 2026 20:59:44 GMT  
		Size: 13.7 KB (13682 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; s390x

```console
$ docker pull erlang@sha256:f7711f0c52090c8acb93087df783d01a1368ba9b7acf5347dc8aa0644dfc7691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113085831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d776362bcb145f7c8130fffa2766e67daa0795b7eb0d51f8c8bae150ac991a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:13:41 GMT
ENV OTP_VERSION=27.3.4.9 REBAR3_VERSION=3.26.0
# Tue, 07 Apr 2026 03:13:41 GMT
LABEL org.opencontainers.image.version=27.3.4.9
# Tue, 07 Apr 2026 03:13:41 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="62e964290041eed1182e1a1dbf934193aacd2e124b315cd5b9ffd9dd0d3b0f8f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:13:41 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a499a563ee8a28bc2c1f1bdc9a76f2ba97ae4d47b072b0221697933233bdc5`  
		Last Modified: Tue, 07 Apr 2026 03:14:00 GMT  
		Size: 65.9 MB (65937747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f4c0273c3ca717626f3073f4220fe28be015565a7940bf134198fed25e0bf850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea09044b804cc8d1de9f379a36cd058fce2b7f3a00f1bd5979a1d5dcb9b3590`

```dockerfile
```

-	Layers:
	-	`sha256:a73a49b4d915326eaaa98ce3cd1b38770c2e4efaddadf07327673d375fef0784`  
		Last Modified: Tue, 07 Apr 2026 03:13:59 GMT  
		Size: 3.8 MB (3821605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4857c369087f7205ec1856e613e3d30780d1b26e71cd5c7a4bdb25e0c99527`  
		Last Modified: Tue, 07 Apr 2026 03:13:59 GMT  
		Size: 13.6 KB (13635 bytes)  
		MIME: application/vnd.in-toto+json
