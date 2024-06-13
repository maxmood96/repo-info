## `erlang:23-slim`

```console
$ docker pull erlang@sha256:a9e870ecbc463c268fc1290b0ac5986eff3a064a873db4cbe712d85e2d41ac9b
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

### `erlang:23-slim` - linux; amd64

```console
$ docker pull erlang@sha256:a7b4be6bec38f7e0948be61e025a8f357bb7ed2a5ef7abb95f470fa84c887553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112539827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2de5cbc44d25ae8ee7ce54299d23b6e230d6bed0a32ec47945a06d7b1e4dbb1`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=23.3.4.20 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=23.3.4.20
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="887859a686f3278e2a60435713ade724f97e6222cb7693a5f37c6a894ac42f8e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Thu, 13 Jun 2024 01:26:34 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e1fb3083306969d161bc8be9b59136dde06760f8558b606c3ee5c0614b4149`  
		Last Modified: Thu, 13 Jun 2024 18:21:34 GMT  
		Size: 61.9 MB (61882454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:23-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:110dcdbcc4e89c3c351fe832ca74ded7e7860a9178a11cd56cd2650920994c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f490796117510f405545f766df1f7917ac4e28c76ad876c4e5b7a37c1206bb34`

```dockerfile
```

-	Layers:
	-	`sha256:2c04b300d3d40fb11441e9d95454f41de41c738add4e5ae3b69500bd34b7a1cb`  
		Last Modified: Thu, 13 Jun 2024 18:21:33 GMT  
		Size: 4.0 MB (3988544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ee05757f53c40221aa868918cda12febf3c844b99b3843b3a0955f1f472bd1`  
		Last Modified: Thu, 13 Jun 2024 18:21:33 GMT  
		Size: 13.4 KB (13366 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:23-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:9ca8f446c42e43f9b5166a82c74f498c07001fd425512fa96593d61af89ab223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.5 MB (106475477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5009edfc297fac3023ad043eb09080cf43c463a380136de08192b7187de4f777`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:a412a8d68ab5b47e51cbbb8ae3797bc960802ae45716dda9d517985663677bd1 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=23.3.4.20 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=23.3.4.20
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="887859a686f3278e2a60435713ade724f97e6222cb7693a5f37c6a894ac42f8e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:36ba9c8baad7d50b1a4b523006966a56ab736274cf5108a528d21b65d3e5927b`  
		Last Modified: Thu, 13 Jun 2024 01:02:44 GMT  
		Size: 46.1 MB (46129853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f055d6620957eb7f8da7af5bc4f399a2b6b9717f1af95b1f3088729150064b`  
		Last Modified: Thu, 13 Jun 2024 13:13:06 GMT  
		Size: 60.3 MB (60345624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:23-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6900381659c7a9de9f090bc17f2bcc9203556cad0ea931d7d7bebc066cbda126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5227180fc1817d51a82d13bc3859c3abf055f313b02c52650e617b33100f7824`

```dockerfile
```

-	Layers:
	-	`sha256:63b816152e42b26e1835d9f917d8ec4d17179e003b095b38c6278387faa1b74b`  
		Last Modified: Thu, 13 Jun 2024 13:13:04 GMT  
		Size: 4.0 MB (3990613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c80914d5c090167813a30790579540c4cf87c96f2ac14a1a8437b514e7db4aa5`  
		Last Modified: Thu, 13 Jun 2024 13:13:04 GMT  
		Size: 13.4 KB (13436 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:23-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:7298d427f810b0f199b57d1aa41a92a82dc548f407810944b1da2bd4a182f8a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108233548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c48de113947f5d12cf6a7ff92566f5bcd3cb3ba8e82d033d529354013b347e6`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=23.3.4.20 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=23.3.4.20
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="887859a686f3278e2a60435713ade724f97e6222cb7693a5f37c6a894ac42f8e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bf6ad2d162d3449075e945e3a69f573a6674dcc390fbbdfbf5ce40a5d1fdd4`  
		Last Modified: Thu, 13 Jun 2024 13:12:19 GMT  
		Size: 58.8 MB (58780290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:23-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:70f29ed8830e507aadd416c70ffa8aa1240a5a8715a751c828dc300955402d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0d94fc36a87064be830704681e2ac76b0d4b1daa4da6f8cb43b18bd00d144e`

```dockerfile
```

-	Layers:
	-	`sha256:ad921749cc158c80e16940a5a492f95fde22b3153601483469d47bdff57b7273`  
		Last Modified: Thu, 13 Jun 2024 13:12:15 GMT  
		Size: 4.0 MB (3988749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f90923a469325cc3bb72237e1b1d8c8451c47ba03330e72d4f1fa7436a4be161`  
		Last Modified: Thu, 13 Jun 2024 13:12:14 GMT  
		Size: 13.7 KB (13668 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:23-slim` - linux; 386

```console
$ docker pull erlang@sha256:5c27ee997288e81a3db03e4ce0661b7045b040bf6395104b9c0a6d8a7d953634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112647732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42934afb56f1a6dacf3d230520412f392d9b9281fad3e6660cc5c60c483a10c`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=23.3.4.20 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=23.3.4.20
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="887859a686f3278e2a60435713ade724f97e6222cb7693a5f37c6a894ac42f8e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486f645d9190ffba05425a7be205012d1e5339fbbde1fb2102f4ad370066edef`  
		Last Modified: Thu, 13 Jun 2024 02:05:56 GMT  
		Size: 61.2 MB (61227819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:23-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4c3cbc9bc575d023547e5f1c2c39ddd247a7145a086892979f1b147ccc2a2e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3999123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81094fbfa185009fa2a2608fa1918eb00f8b66554fcbdf766ba225d26033637c`

```dockerfile
```

-	Layers:
	-	`sha256:161211743154ca8c4a101d5c198a751eb3778101822c763327e38c8915bf571e`  
		Last Modified: Thu, 13 Jun 2024 02:05:55 GMT  
		Size: 4.0 MB (3985787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdb94e931697b2fd9f47c0bf7e0796152b5f968520824dd3fca7ed53e324a489`  
		Last Modified: Thu, 13 Jun 2024 02:05:54 GMT  
		Size: 13.3 KB (13336 bytes)  
		MIME: application/vnd.in-toto+json
