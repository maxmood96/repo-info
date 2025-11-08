## `elixir:otp-26-slim`

```console
$ docker pull elixir@sha256:144399e28313b6b1814535962b6453f49b83a07ba8c195ed4e9b4c448eaa066a
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

### `elixir:otp-26-slim` - linux; amd64

```console
$ docker pull elixir@sha256:189a4f82b57a21444a5e1e0be7bf54d89204815777f59f0da8caa3b2ec256bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127140596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abd8111ef9189839951835e4c57575fc248914166118e9d253ed82972dac229`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:33:16 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:33:16 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 00:33:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:16 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 18:05:38 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 18:05:38 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:05:38 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b136921fb2227afde0e4ec5cec26465aabbe22bd913d1abee2ff746dae9a80b`  
		Last Modified: Tue, 04 Nov 2025 00:33:41 GMT  
		Size: 70.4 MB (70430306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bee3166ee776bf51aca1f1ad10e6a7e50eb6185d0090b1f6743948a1c1d34d`  
		Last Modified: Sat, 08 Nov 2025 18:05:50 GMT  
		Size: 8.2 MB (8229234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:e36c29f98b68d1a0a76cd37388def5fa7390d32db49b64a0dd74f2306d8328b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c099e0d11175f0e28308a374c9374ee7b586f82d60b83f0faa97db0e52acd2`

```dockerfile
```

-	Layers:
	-	`sha256:87b5fcbe0966506148679a6caf7e1e8d882489e8cbbfb1fb6271ad639a89a07c`  
		Last Modified: Sat, 08 Nov 2025 19:45:46 GMT  
		Size: 3.8 MB (3832374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9b96babb28254ae45714cd3610ea9b0c0192fc8e832434f6423433b816e7e58`  
		Last Modified: Sat, 08 Nov 2025 19:45:46 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:7f38d60de7e234cd5b7df1b2dc2ff3116a34b8b870fdc9be153cd208f3ee5bae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112587839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5632fa49ffb08cdd60177fee7e2a59f6c6d417bea24d2df11d32ba7498f276d`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:47:55 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:47:55 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 00:47:55 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:47:55 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 18:05:00 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 18:05:00 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:05:00 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e0c7fb0ae6db9b2cc75862c0a4ebf823d28b39ad9c45533c446faa027182e7`  
		Last Modified: Tue, 04 Nov 2025 00:48:20 GMT  
		Size: 60.2 MB (60162778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a29f70a7eb54d74eaf7320595e1a5f6fb815c79dc0af6ef967548975dd77fee`  
		Last Modified: Sat, 08 Nov 2025 18:05:16 GMT  
		Size: 8.2 MB (8228624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:ffcb0a5c68fb83b9ad9b34e044dc0f98f8a02147e11a04e7eed5e46566ef348a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3844418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff56240da3401b5291cbf1f9707b0cf0d9a444829453857863a2cff8b86e20f`

```dockerfile
```

-	Layers:
	-	`sha256:647a042af19d4ad18150c92040ee5a4bf42224cb65573e75aed350ab3127178d`  
		Last Modified: Sat, 08 Nov 2025 19:45:51 GMT  
		Size: 3.8 MB (3834599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31551490f13b4bd866b71685a640f32f40264dd1866cd06e5e87dc8b505a4a85`  
		Last Modified: Sat, 08 Nov 2025 19:45:52 GMT  
		Size: 9.8 KB (9819 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:603d79fb0d709e12861f6cc0cec9bcce8e7407b8e33436949732246854eeb233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124659323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024e0f7c2fadc6e98918b666d07b669c4b55cbaaf6413474ec5b3aac94540d3f`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:34:54 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:34:54 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 00:34:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:34:54 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 18:04:55 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 18:04:55 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 18:04:55 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623ee7d32f43dda583537ae1cda285669839d35c4475ea85f044bf2a93a8a14b`  
		Last Modified: Tue, 04 Nov 2025 00:35:21 GMT  
		Size: 68.1 MB (68070765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0cb90143563d20708d4ad7231595a32df93dce84652deeba2a94d55e5cd5da`  
		Last Modified: Sat, 08 Nov 2025 18:05:12 GMT  
		Size: 8.2 MB (8229080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:c06f744a21127c584e8721f72107f6bc4181800dd839597ba513c971c522dcfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4736cb9edfd437f5c6b7177194157d9334c6fcb9a15e579f158cab6e1505b4`

```dockerfile
```

-	Layers:
	-	`sha256:d1df8f9d63f7ea08849ad714e0e6cbc389adf09c979996871c55b9b6625e8b6a`  
		Last Modified: Sat, 08 Nov 2025 19:45:56 GMT  
		Size: 3.8 MB (3832623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6173ba3aec1f5098c1caf0cc8a82385b987b2c115b049604d4ebdec895a0faec`  
		Last Modified: Sat, 08 Nov 2025 19:45:56 GMT  
		Size: 9.8 KB (9839 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; 386

```console
$ docker pull elixir@sha256:21a44def30852697bc744c2f813e536485049493b26d94e1f27536da940ee736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118850560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbade52fd6a903ecf6c130b94dead7197fab7976949fde3bfb781e302a688053`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:17 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:30:17 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 00:30:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:30:17 GMT
CMD ["erl"]
# Sat, 08 Nov 2025 17:59:52 GMT
ENV ELIXIR_VERSION=v1.19.2 LANG=C.UTF-8
# Sat, 08 Nov 2025 17:59:52 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="3bb6ceadf0174ece79649743bccf208e9708c5a9e1570228ff25c8f7347a2209" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 08 Nov 2025 17:59:52 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:3a9907ae02a89d2535bb875a11c05038e0be4fa333c35747cd42f6f7b49e018d`  
		Last Modified: Tue, 04 Nov 2025 00:12:58 GMT  
		Size: 49.5 MB (49467114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72391287dfd25f0f21acf2ed7c85e4225a39d24bb12601d929828b0a644ba2dd`  
		Last Modified: Tue, 04 Nov 2025 00:30:42 GMT  
		Size: 61.2 MB (61154810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86404869ee0e8e69275837b921d21375c6b0e5d68458634b498bf488f464210`  
		Last Modified: Sat, 08 Nov 2025 18:00:07 GMT  
		Size: 8.2 MB (8228636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:c99f91b59d8372f97b4c99c7cde213202d0b8dd27528e8291be8a61559188e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab075c9b951158fa9a0e22ef5e40847eedd1d7a34b1ae2280545945215a6677`

```dockerfile
```

-	Layers:
	-	`sha256:00f3fb45774774efd06bf17463121f90d812b4c6740668e89016e50468ea1654`  
		Last Modified: Sat, 08 Nov 2025 19:46:01 GMT  
		Size: 3.8 MB (3829541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3531929fce9e5af9f47e92235f3a57e27554820b13aa1ccb86a6e7b65e944fb`  
		Last Modified: Sat, 08 Nov 2025 19:46:01 GMT  
		Size: 9.7 KB (9720 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:91fddbf5fe89dfb076583bbadd5a31453f5e5fa479abbbcc9b6b2b4eb8e396af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122887186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551d16a796f7a88cc904032d572dafc2f11fe4e30224b1571879acec292bacee`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:39:59 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:39:59 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 00:39:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:39:59 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 14:03:15 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Tue, 04 Nov 2025 14:03:15 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 14:03:15 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afb768048b5899bc97639cb39d9c29e9e3751572e57337a265b88b0083dffa9`  
		Last Modified: Tue, 04 Nov 2025 00:40:55 GMT  
		Size: 62.3 MB (62251565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a11ad69857545c727ee5474028ce4440ca3d296bcb4d53e7162bb541c18d16`  
		Last Modified: Tue, 04 Nov 2025 14:03:43 GMT  
		Size: 8.3 MB (8308341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:8c930f1ac15f6aea66d34f00be467eb98fd27532b4751713bfbb519ac5a5c965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3846591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7537e2dbe32e0880cfb69da5186c96ea532b479d5e63c354751d7d2bf0dfcb70`

```dockerfile
```

-	Layers:
	-	`sha256:0506afd69993df89d67a2b062e006c280fc4f47067a8e63d1ff280fd0f82d72c`  
		Last Modified: Tue, 04 Nov 2025 16:48:34 GMT  
		Size: 3.8 MB (3836806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b28f10f602834404bbb1a1a711b21813867713ad001e5e724610adbe09b2ff34`  
		Last Modified: Tue, 04 Nov 2025 16:48:35 GMT  
		Size: 9.8 KB (9785 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; s390x

```console
$ docker pull elixir@sha256:74f1431b6f47018fe387b94bf61f4d214aabd3fdfce558dde2cee59e94377631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116406003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4400dddba084cfcd04fdb5f4d38847645d8a25e36488ba18ff7ea2d5e5a8292`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:32:11 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 03:32:11 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 03:32:11 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:32:11 GMT
CMD ["erl"]
# Tue, 04 Nov 2025 13:15:55 GMT
ENV ELIXIR_VERSION=v1.19.1 LANG=C.UTF-8
# Tue, 04 Nov 2025 13:15:55 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4dfbfa2d0863bb3809109757a599b453e78ea890f31fa54456a2d81b40bc930f" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 13:15:55 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e1dbfe59ae33319104649a00234b8446d2118b230747b863202aa24e3f31a1`  
		Last Modified: Tue, 04 Nov 2025 03:32:40 GMT  
		Size: 61.0 MB (60960398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c147b27d6fc1a1375c72bc6b11967820b0a98b43c50534f7de8b84e95bf2c5ae`  
		Last Modified: Tue, 04 Nov 2025 13:16:17 GMT  
		Size: 8.3 MB (8307512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:0e95222d94ced29730d9f26c08cd852288203c9e5a152205f5bc5a3cbae761c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01072b147f32caf69ac3fa84644fba7fbe064091ff83c369f57856792b7d9fb0`

```dockerfile
```

-	Layers:
	-	`sha256:3e877ef89655f6344ef2e3a27938a3e73ee1d847f33b58aaef15c4c645450e3e`  
		Last Modified: Tue, 04 Nov 2025 16:48:39 GMT  
		Size: 3.8 MB (3829192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26762c923651d1f2909c038b069ec4c1847dde6e7de50b5f6653f224370eaff6`  
		Last Modified: Tue, 04 Nov 2025 16:48:40 GMT  
		Size: 9.7 KB (9745 bytes)  
		MIME: application/vnd.in-toto+json
