## `elixir:otp-26-slim`

```console
$ docker pull elixir@sha256:f9acc374eefd704eb6cf6dc981b3e5848130bc34278e1bd35bf16b67b3d4c786
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
$ docker pull elixir@sha256:05db3bdda6f563c6717b8f2f0855e04d2d6f77a3e8bc6d257797a7ac2584ef41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126755545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d25ddd6877467b5c45348ccad292f98c1097bb59e9237d091b7bf07776a478`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3f3af508cdb50d7c303c5d72f27038f2274d6662fcddb4e056dead4a66304d`  
		Last Modified: Tue, 14 Jan 2025 20:40:33 GMT  
		Size: 70.4 MB (70378826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8a318acdafca1e0d69ec82be177f0fe9bdc5449d5b3e0aab118a36b8163b78`  
		Last Modified: Wed, 15 Jan 2025 00:07:04 GMT  
		Size: 7.9 MB (7896757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:6039c20e91a7cc79543b36740abcaa894838899f996d2c941bf7c678c7c280c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5db053de6361be5c94b8e21751754c5109bb66df78f225005d9a0e47f1869716`

```dockerfile
```

-	Layers:
	-	`sha256:5836e19aa6a69ae4c8d9b01afc66171d947c99d6640411694bd142307f5df767`  
		Last Modified: Tue, 14 Jan 2025 22:50:06 GMT  
		Size: 3.7 MB (3716380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d18e0ed238a28c8de43c08cfcd79b6ad22c13c65528cc414cf09cf3d3a47498`  
		Last Modified: Tue, 14 Jan 2025 22:50:30 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:1316c7981eaabd16cedbd589bd9932c5d1ccd146b3690cb61230b1e275d026ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112196116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547751bda9c7e344631e4228ad0b4790dd10bbbdb7f7c7b49b43da9d2dd8858c`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c0f65289344c846dda8bd4a958c6af32dbe4f0527dd363d424b2336788cc0b`  
		Last Modified: Tue, 14 Jan 2025 09:15:58 GMT  
		Size: 60.1 MB (60115890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabd7409ed29ba04cd37fc738575659b01681ded2fe00c1f118bf083db641d49`  
		Last Modified: Tue, 14 Jan 2025 21:07:43 GMT  
		Size: 7.9 MB (7896017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:2df5ddefff420a70bc164a8c5e1dd2fde0ef4513d32a919dbec6f17efa5c1d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c9bfa7072d369b16dda57e341c54edfd247fdfac327083a364968807054b26f`

```dockerfile
```

-	Layers:
	-	`sha256:19841faea3416c76d3def2a1b38c04eb1210522ffaa9149528f5ff246c158885`  
		Last Modified: Tue, 14 Jan 2025 22:50:32 GMT  
		Size: 3.7 MB (3718605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:500a9140f1d08ad8b965ed5ebdbae6b2ed11c712b0d5a965eea88e2853644a2e`  
		Last Modified: Tue, 14 Jan 2025 21:07:43 GMT  
		Size: 9.9 KB (9857 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:a2416abd349b26e7a7f4266bcc83e7f58a2130647ee3fdf4227a081bd9188ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124214102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb45adf0504af7de7dc931136f37d34b11e7ad0a4c044cf5913193601f33c48`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b7a5604f843830b75a28c39ec859d21831ed8cdfab23845a43bbb839bec8e9`  
		Last Modified: Tue, 14 Jan 2025 07:15:52 GMT  
		Size: 68.0 MB (68010512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8527a2a7e2c34289be12fd9b9a18b692b4be5d8d1cd6a770265d87e4bf5db71f`  
		Last Modified: Tue, 14 Jan 2025 16:14:39 GMT  
		Size: 7.9 MB (7896694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:06ae1a1169006cd42b190a7e9e5945cd74e8045c849d9a8f68edb7ddc643eae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbe3f5393fe1ff9234fa4831e7960cbc88af21849e3d3bedf31535cc899ddfc`

```dockerfile
```

-	Layers:
	-	`sha256:7a3c22b82b1b34a45433e351d7574770e1a0d7f4918c46a75ec19fefc016cfac`  
		Last Modified: Tue, 14 Jan 2025 22:50:11 GMT  
		Size: 3.7 MB (3716629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e316201cc95ae8721061229d834046153eed8e259e44bdb54528511458d94a`  
		Last Modified: Tue, 14 Jan 2025 22:50:12 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; 386

```console
$ docker pull elixir@sha256:4559cb8ceab5c32eaa5be177c3575545fc571db31ff40d5512ae35bf5d22cead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118469476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ec37af9dd99374487d147c79ad6c52484e10c02128725c541de57126de88d6`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd5e010075b3c7e91533ed703b8c21bddab162b508d7c6c889ef6964475ce36`  
		Last Modified: Tue, 14 Jan 2025 02:24:43 GMT  
		Size: 61.1 MB (61115574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db25c2374e508df9b47e2fa0ba6f3bf79e65311607be6d999f75792a65b0019d`  
		Last Modified: Tue, 14 Jan 2025 03:21:14 GMT  
		Size: 7.9 MB (7896157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:bb505c3e72251ec08a6ad2ac250c42d4c615b7504fcdabbbd3b1a8649f0e2901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2db3127700ce0c446237980b85212987e41604f39c0f90d0eb2e3d83e65b02`

```dockerfile
```

-	Layers:
	-	`sha256:545dd6f6dd3fa99fc5cc3ba72fd6cfed32664eedc583d6ded1ca9517d5dce396`  
		Last Modified: Tue, 14 Jan 2025 22:50:14 GMT  
		Size: 3.7 MB (3713505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28fdd9b2e925bcffafff01f5e3ff60307e3e4de284ee45c2a9a9911ae8322b82`  
		Last Modified: Tue, 14 Jan 2025 03:21:13 GMT  
		Size: 9.8 KB (9762 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:0aac97b1488d57390d2e8039a9b6748761650e3a6930bdd0d727496fd3336b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122412729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b678a39cd7addb5209fb3a98848ceacbcf61fee3e4599f13522ff70d2f394f32`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 20:37:16 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7ca3d64187888d7d15091240f2380913d56f962a6230774e20ec678640ca12`  
		Last Modified: Tue, 14 Jan 2025 05:47:05 GMT  
		Size: 62.2 MB (62202772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4060f6856bc3386eefab45d42feeafeb89a342856c547ed2e59fe28375c569d`  
		Last Modified: Tue, 14 Jan 2025 12:17:24 GMT  
		Size: 7.9 MB (7896820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:7383c732913c3df9a32cd16e63721643e8c7d2898213dce78332b753fb7c9c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92a9efb1af4f7d4facdfd000c23aaf9be40b7f40a5282b57034ae1e48199e29`

```dockerfile
```

-	Layers:
	-	`sha256:2f5a860444cd1931b39d9aa5d46024211140b7e0f310ac1b6a965daec8bf61f8`  
		Last Modified: Tue, 14 Jan 2025 22:50:16 GMT  
		Size: 3.7 MB (3720714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:621b4a5ae2bb48b01a37c9e39b96614af360f05087dbbf9c5f995640995a3422`  
		Last Modified: Tue, 14 Jan 2025 22:50:37 GMT  
		Size: 9.8 KB (9827 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:otp-26-slim` - linux; s390x

```console
$ docker pull elixir@sha256:ed0636217de280b6801ef1fb64f46eba9f406ee2e27e70db7606e76fb2a44a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115941392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7f8c12d086a7298d441b9b4b0eab049cbe5d876409fc63a547b22d45247683`
-	Default Command: `["iex"]`

```dockerfile
# Thu, 26 Dec 2024 17:16:07 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Thu, 26 Dec 2024 17:16:07 GMT
ENV OTP_VERSION=26.2.5.6 REBAR3_VERSION=3.24.0
# Thu, 26 Dec 2024 17:16:07 GMT
LABEL org.opencontainers.image.version=26.2.5.6
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="371e59b98de59822e45fdbe50c18c8d8dd4c872990e7aaaba8a819e167186d03" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["erl"]
# Thu, 26 Dec 2024 17:16:07 GMT
ENV ELIXIR_VERSION=v1.18.1 LANG=C.UTF-8
# Thu, 26 Dec 2024 17:16:07 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="4235a63c615c7c787d85a5167db28a58ec9f5a579f9b3fd853fc6f4d886c209e" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Dec 2024 17:16:07 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 20:37:18 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a0b479fcc2da5e4ce430df40cb6724861f44fb327346532857a5127735942e`  
		Last Modified: Tue, 14 Jan 2025 05:23:17 GMT  
		Size: 60.9 MB (60913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5014cd9a12721a61d4ff6a192aba47e632e43cc1c136ec405be1a404df2360f8`  
		Last Modified: Tue, 14 Jan 2025 10:45:05 GMT  
		Size: 7.9 MB (7896169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:otp-26-slim` - unknown; unknown

```console
$ docker pull elixir@sha256:a9f04116515b82a34efa5a07b81f4b3d51fb33a240fbcd7352cc0120f8affccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4342d39be6a305de18fcca7ad9022722f889351686eee61000c3bbdbff9baf2b`

```dockerfile
```

-	Layers:
	-	`sha256:49db5e82ec6325968cce32144c55942d6dede0aec23bada5ffe812967ad0b8e0`  
		Last Modified: Tue, 14 Jan 2025 22:50:18 GMT  
		Size: 3.7 MB (3716100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d92d4d3c62722250198bbc68750a3ed82ae8bdffbac815009b6fee045abbe7`  
		Last Modified: Tue, 14 Jan 2025 10:45:05 GMT  
		Size: 9.8 KB (9789 bytes)  
		MIME: application/vnd.in-toto+json
