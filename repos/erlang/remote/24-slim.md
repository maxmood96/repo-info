## `erlang:24-slim`

```console
$ docker pull erlang@sha256:6b940d302ae81ce3fc1455f75063a940a22ba771e00e2a20eda7eae3482259d0
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

### `erlang:24-slim` - linux; amd64

```console
$ docker pull erlang@sha256:b8ebfd120375c20a100f0c42b2b52118f152467877d83c8e1768f2a7180963fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118980295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50505747edcd25452469a789c0bf5637debbf07fac01ba7b5812eb5a64a60e10`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdd30f6c28fb6d2fe56501a3534238d501ab13016ce33903ae1af08bb073ef6`  
		Last Modified: Tue, 14 Jan 2025 02:40:06 GMT  
		Size: 65.2 MB (65241131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a0ef0e792fd708ef3e6b704eee252e1689ef93cac1594a2a903ea5eb604eb03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04bee5a4f57a85719054d445dba7c028182dfbd32c8cf7f7027bc324d5a8bdc`

```dockerfile
```

-	Layers:
	-	`sha256:3163dc5934dc6c96b6086d101a61149e149464adc09d3e58f81891f317c815da`  
		Last Modified: Tue, 14 Jan 2025 02:40:04 GMT  
		Size: 4.0 MB (3991216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3835717178253d3373dac59f903e9b9ae0c02dc1c7c49e030dd592c74225ae12`  
		Last Modified: Tue, 14 Jan 2025 02:40:04 GMT  
		Size: 13.6 KB (13611 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:d0c1a1adf7de94e7efcabc74b5ad5776dcbfa763c3d814513ea8d4c8ec79c191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106250147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d5fbee9b85ca2b1e401bd9acd6b73e468e4d91b5f3a072461c8eed511613a0`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 24 Dec 2024 21:34:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276a3655d64628f8685379e91d423b551c26c4e6151a7663562f9f1e14d82fb5`  
		Last Modified: Wed, 25 Dec 2024 04:10:18 GMT  
		Size: 57.2 MB (57225381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2ff1421f9de916b886ce2829e9d354a0af42e73064c7d30b68df95fdbe2d892d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0d652c05dac0910728362f95614499fc3fb1ae1a107c7f04ad9dadc45902c5`

```dockerfile
```

-	Layers:
	-	`sha256:861f63ac68d5e7c76d4695d7e3740324ddc4d305c85d47e254bc6d5eec69e3a2`  
		Last Modified: Wed, 25 Dec 2024 04:10:17 GMT  
		Size: 4.0 MB (3992817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5164aae062b906929b8ac3a714bd8b3cb66c49883d0cadc44ca3c004494b86bd`  
		Last Modified: Wed, 25 Dec 2024 04:10:16 GMT  
		Size: 13.7 KB (13684 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:bb3c5b69bf411d1b751a8e3c7a9bb0ee29220c8cdc81acca7a4a88f6ff0bbd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110322294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659c744ea9f97b2c78a522d4240b249952b92a2295855728b5d4f60d69a37cdd`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfbe9152ccf077047cc3c5bbdc26c703dca9336024919ffa3657e72de7668cb`  
		Last Modified: Wed, 25 Dec 2024 02:12:32 GMT  
		Size: 58.1 MB (58076596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:929bd5ae7dcc79cc077950b3b9f7203377cde4cfb4aa0349693aa48f465a5f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547c4c75d0a47dade36421c6cf7bef125bb613083d31a15f085139242104eb9d`

```dockerfile
```

-	Layers:
	-	`sha256:bfd76fa63e7353805caa330b9c24ec302b76c2da25c02dcb7b5e4ca14c2ae0ef`  
		Last Modified: Wed, 25 Dec 2024 02:12:31 GMT  
		Size: 4.0 MB (3990837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5831c05ac060c320dd784b94ba46374d2be40d8a6869312bab16ca0b2b32d4a6`  
		Last Modified: Wed, 25 Dec 2024 02:12:31 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; 386

```console
$ docker pull erlang@sha256:e5cf193647013465bc8eb26928c331b9f69a8d8e1d1f00deb61ba4af58211119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112380914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c267d5ecd5048117922c58a9b1c0d32e4a6dddf74bb9cc9493449cf530278b43`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b72c0b254e0d45985d121f47650a88f2ee35fbb4ff596c396ee98094e0a26d1b`  
		Last Modified: Tue, 14 Jan 2025 01:33:19 GMT  
		Size: 54.7 MB (54676276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc98e88ed60c09789cfd27e290a6861b2f8d4752391828c5a8f1cb65f15814a`  
		Last Modified: Tue, 14 Jan 2025 02:23:31 GMT  
		Size: 57.7 MB (57704638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2743802eda730a769176a5d9e580403ff2bd94cc2cbe6f754d9af5ef0d16fb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3521efdd7344b5080dbb4a558c4966d84c04a5900aa671bf4dbb12ebc9e57f84`

```dockerfile
```

-	Layers:
	-	`sha256:63cf6c2571ac3ee7174fe1cc82b4477cbceb0dd3c7ccf8d2d12e4297ed901c0f`  
		Last Modified: Tue, 14 Jan 2025 02:23:30 GMT  
		Size: 4.0 MB (3987694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0e66d66b929cbce753fde932a8962ec46fa8957ca16c8df1ab9228670a2cbc5`  
		Last Modified: Tue, 14 Jan 2025 02:23:30 GMT  
		Size: 13.6 KB (13579 bytes)  
		MIME: application/vnd.in-toto+json
