## `erlang:28-slim`

```console
$ docker pull erlang@sha256:dd97165967dcbcaef890751031287ed22395d1fc993bf3f2644d81fce0644686
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `erlang:28-slim` - linux; amd64

```console
$ docker pull erlang@sha256:2ddb243f7e021aefc6f3861df5c6254df3f0987bb47c067fbacb8dde639097fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128205581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1660883d8dd52e3d7564577a299a897efcb86c5fa3cacc65578aff7b4493cd`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:42:11 GMT
ENV OTP_VERSION=28.4.1 REBAR3_VERSION=3.26.0
# Mon, 16 Mar 2026 22:42:11 GMT
LABEL org.opencontainers.image.version=28.4.1
# Mon, 16 Mar 2026 22:42:11 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="fb2aa0bd8d4118a275895d4a0ea5b24e40e9e1e27a7b29e001377d7660fd9ecf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:11 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568dfca27037ff23a63688c8b84172f4d784027225d2c2b397b07d10c99f406f`  
		Last Modified: Mon, 16 Mar 2026 22:42:24 GMT  
		Size: 78.9 MB (78908051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9af325cf09133396ef2d8774e67dc55f6ef9c2d156ad6bb560da510cb335ce36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce55bcadd796e44720ac87ccb494b04fa15d26d55974054e9eb4d11649e2457`

```dockerfile
```

-	Layers:
	-	`sha256:6020ee9a99cb14a79fe678876bd11ae33a3414e99ebd69981ecb436b4d2dea5a`  
		Last Modified: Mon, 16 Mar 2026 22:42:22 GMT  
		Size: 3.3 MB (3283912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66efe806b77cf4fb46278458c459cb2b320634b5bb24017c9c3fde9dbbb1cb16`  
		Last Modified: Mon, 16 Mar 2026 22:42:22 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:a39ad327568e6305b7947d5af40be3ccff028406d1b6fe5ae09360087705500d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116520549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1db88b03c116383fa6128933d2873a28686dca13b07ef258462bbc5dfb176f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 19:26:57 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Thu, 11 Dec 2025 19:26:57 GMT
LABEL org.opencontainers.image.version=28.3
# Thu, 11 Dec 2025 19:26:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 19:26:57 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a635f54eaf3a9fce0549b1b49b875e73326ccbc501c3133d86c2ac8fd7828fb8`  
		Last Modified: Mon, 08 Dec 2025 22:16:05 GMT  
		Size: 46.0 MB (46015801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ce423db1f019b525b3f032b6fef20b9ca668f921e9a278644993feda24180e`  
		Last Modified: Thu, 11 Dec 2025 19:27:12 GMT  
		Size: 70.5 MB (70504748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:f5d71c46a31fcb491a3f28b257dcbd6ade19ef1be29034247659d4c9a96f2c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98e5ec52e64190a335b62cdc2a09370e752ce5e106d9968eb44fa7016e03d1a`

```dockerfile
```

-	Layers:
	-	`sha256:717f830040cd9acc87c686ba14ecb6ba4427998c620725ec6f6f7891d768fe3a`  
		Last Modified: Thu, 11 Dec 2025 19:27:10 GMT  
		Size: 3.8 MB (3828056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c5c634919ee052cca6214dffc2f5e111b8da281edd273274bf2fa89fbfa702`  
		Last Modified: Thu, 11 Dec 2025 19:27:10 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:05dcdea6ee03a8ea2a384738a1054a84ce0e8b301a5f7edf16c55ad89174324a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114110349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d61aa65b4db3d6c4d7ed5f0db802624de9b6d86945cb6203a9e2b37f829f91`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 19:26:05 GMT
ENV OTP_VERSION=28.3 REBAR3_VERSION=3.25.0
# Thu, 11 Dec 2025 19:26:05 GMT
LABEL org.opencontainers.image.version=28.3
# Thu, 11 Dec 2025 19:26:05 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="1956ad6584678b631ab4f9b8aebe2dac037cd7401abb44564a01134ff0ac5bed" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 19:26:05 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:36 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e656ea89dded4641f3cfae04edeb56bdaf27e5ade23d29c71bf377d6a3a515ba`  
		Last Modified: Thu, 11 Dec 2025 19:26:19 GMT  
		Size: 69.9 MB (69914283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:dceef99c554f807f9b33461f23cedd54ed45738dd3d906ea7367dc879f4bfb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4996cdad3d8836236b202b8365be7a35de4d5d179dce1a7a87915bad40241f9`

```dockerfile
```

-	Layers:
	-	`sha256:f51c09700ce8338cf3893f56b3ade685efb3768a90807543513803bff0bf9f79`  
		Last Modified: Thu, 11 Dec 2025 19:26:17 GMT  
		Size: 3.8 MB (3826481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55afd26957dc4411249f6d93d18e207551aba20237ad22c9b3a2549da2001ee`  
		Last Modified: Thu, 11 Dec 2025 19:26:17 GMT  
		Size: 14.0 KB (14010 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:c54f309a6b213f4260ca9b2ded562771a38b8ef38d3724c555e7e941be3d6818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127122383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6f6e970342602be3422538b27042d542406a5a1e64d5c630cd07f05fd950e0`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:29 GMT
ENV OTP_VERSION=28.4.1 REBAR3_VERSION=3.26.0
# Mon, 16 Mar 2026 22:44:29 GMT
LABEL org.opencontainers.image.version=28.4.1
# Mon, 16 Mar 2026 22:44:29 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="fb2aa0bd8d4118a275895d4a0ea5b24e40e9e1e27a7b29e001377d7660fd9ecf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:29 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0f96d7da729d0377be51d3efb009f828058669f8ca81bef6b6ea719a31ce10`  
		Last Modified: Mon, 16 Mar 2026 22:44:45 GMT  
		Size: 77.5 MB (77457430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e6535222a87a47dc5040f125de1e1795eed1c1f21d04920af2fb5951a391eada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad8a47da4b62af1cd011710941d5d609a7cf64d85c42659b95a5d1e784a2a08`

```dockerfile
```

-	Layers:
	-	`sha256:feb0263a5c0a4c2d32a7e47c0df1455e1bf3f02c7609b09bedfbc498ea83c4e5`  
		Last Modified: Mon, 16 Mar 2026 22:44:43 GMT  
		Size: 3.3 MB (3285447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3939668f5ea94f4acb530fc9550e71965913bfbc43518581ae80b5b90142ca`  
		Last Modified: Mon, 16 Mar 2026 22:44:43 GMT  
		Size: 14.0 KB (14038 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; 386

```console
$ docker pull erlang@sha256:fa08d05517c03246a8bb6548765ecc623f9d97e156f528620e5e42370a1c7d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120207249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594af1f689941dafa2f14230a29dcbfd99b74cae5a95e0c4e7738212feffc15a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:46:14 GMT
ENV OTP_VERSION=28.4.1 REBAR3_VERSION=3.26.0
# Mon, 16 Mar 2026 22:46:14 GMT
LABEL org.opencontainers.image.version=28.4.1
# Mon, 16 Mar 2026 22:46:14 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="fb2aa0bd8d4118a275895d4a0ea5b24e40e9e1e27a7b29e001377d7660fd9ecf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:14 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ddbf94cfa62b4af1dbc2673289dc594fcbb41fe815b26e45785c88f8a0540d`  
		Last Modified: Mon, 16 Mar 2026 22:46:27 GMT  
		Size: 69.4 MB (69388457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:115baadb5a22ab39ec8c6d553c367e57786dd9ef47124aa516f78422facf09d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a82759f75a6164330a554ea48086f3b9497666e918e53eda360846d36af4b14`

```dockerfile
```

-	Layers:
	-	`sha256:afa9e1b86e9cfe084511ade40b0cd4aca960cd3c7ceba7aada5d92985dcf7492`  
		Last Modified: Mon, 16 Mar 2026 22:46:26 GMT  
		Size: 3.3 MB (3281082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a01d5db16521ca0c0cc79c6b0a17e3ebe3727d2c65c4a57777a41efd5ff1464`  
		Last Modified: Mon, 16 Mar 2026 22:46:25 GMT  
		Size: 13.9 KB (13885 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:b1254f94a5afe5291b29e729de010c0881835ce06b186538da61dca89e797ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123460982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ac00c0c4a4243ab84f623a355271a4a74c82717f2a84e2892daff2259211b8`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Fri, 13 Mar 2026 17:16:27 GMT
ENV OTP_VERSION=28.4.1 REBAR3_VERSION=3.26.0
# Fri, 13 Mar 2026 17:16:27 GMT
LABEL org.opencontainers.image.version=28.4.1
# Fri, 13 Mar 2026 17:16:27 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="fb2aa0bd8d4118a275895d4a0ea5b24e40e9e1e27a7b29e001377d7660fd9ecf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 13 Mar 2026 17:16:27 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83885ba4eee0e53b98dd51a27e5337e0e404fa6c34d159f1872589e27356857f`  
		Last Modified: Fri, 13 Mar 2026 17:16:57 GMT  
		Size: 70.3 MB (70348721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:5805e5766d6e50b534aac6b64adccba94b78e23c504242b526d4cdb3e98b9b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba41bd01a2fc5d84710d0a5ef10109a70b4adb2e1c8fcdb1fc97c19a851075b`

```dockerfile
```

-	Layers:
	-	`sha256:6a013c08a7e71bccc8a28c9589d69d731857da85d8ea09879d202153d315b798`  
		Last Modified: Fri, 13 Mar 2026 17:16:55 GMT  
		Size: 3.3 MB (3287467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4a373ac8aa2e6b7d65f76ce112943337e9037e58f6869aad66df80b3f9be448`  
		Last Modified: Fri, 13 Mar 2026 17:16:55 GMT  
		Size: 14.0 KB (13972 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:28-slim` - linux; s390x

```console
$ docker pull erlang@sha256:f3b48b84bbf9f6b3a4509ec3b619ba4895924ba15218cc74b87b439538644424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119602984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e80105877d8fb785e85e318549219d4028321f3f8f6fd7b4ec754c55526a43`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:49:58 GMT
ENV OTP_VERSION=28.4.1 REBAR3_VERSION=3.26.0
# Mon, 16 Mar 2026 23:49:58 GMT
LABEL org.opencontainers.image.version=28.4.1
# Mon, 16 Mar 2026 23:49:58 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="fb2aa0bd8d4118a275895d4a0ea5b24e40e9e1e27a7b29e001377d7660fd9ecf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:49:58 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a5ab2e5a4e2a07d2112983473da16ff517f92f85b08ca9f54156bfe056419a`  
		Last Modified: Mon, 16 Mar 2026 23:50:20 GMT  
		Size: 70.2 MB (70238209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:28-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:e5b9574107c5b80674934a84037a7fe62cbd64c80985f8058ed14e4227420932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cd3e42f046f81decc08b09d1c8b0374e4a743161052cefd882e969f7be79a01`

```dockerfile
```

-	Layers:
	-	`sha256:5b36bdaa02c30089f7ec681f3c1151433e528df838c7b2b9f55f36b16552d3c0`  
		Last Modified: Mon, 16 Mar 2026 23:50:18 GMT  
		Size: 3.3 MB (3285353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:924fc2922efd0dcd4e75bf70c2cfe8d2d85536e3eea9ee76fb91436ccce95847`  
		Last Modified: Mon, 16 Mar 2026 23:50:18 GMT  
		Size: 13.9 KB (13922 bytes)  
		MIME: application/vnd.in-toto+json
