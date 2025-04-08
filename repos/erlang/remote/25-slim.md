## `erlang:25-slim`

```console
$ docker pull erlang@sha256:000f2930b94eb7788ccc8ebd15ad7c2648fd73150f4b6c76344881d3ecc419cd
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
$ docker pull erlang@sha256:1885f54d7098d9fa4b7c65c2aa161d67e4c097cdac40bab58d78e0eb5e00b285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119695320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441f1ea96eea896e844b7047ec5e383cf218902b259fe2220a00cc4e5350bafe`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=25.3.2.16 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=25.3.2.16
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="15467c6da67f7f4cdbbbd478322c96b370c8d41b82f4b813dbfd8ebc87d4677f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430b7623525e8e72fdcd49fb042299bd6e5aa63a3062660aa8acaccc0c127259`  
		Last Modified: Tue, 08 Apr 2025 01:31:27 GMT  
		Size: 65.9 MB (65946791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0aaf3f71d280fdb4879f693847964fe279485048e07e0c4876d9d712b1ec13e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d384c366ed04a11242d16e65aa29f3985ffe95a8853780d4a0333e853117d29f`

```dockerfile
```

-	Layers:
	-	`sha256:d272a5b1f38f15382825e4ab5cf10da38327df688e35f8afa08de8399bd102ef`  
		Last Modified: Tue, 08 Apr 2025 01:31:25 GMT  
		Size: 4.0 MB (3993145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af1f65853bc98a8e5ac8b014e0eaf3542949b1c8b6d66ee4d49ac1c6bcfb3e1`  
		Last Modified: Tue, 08 Apr 2025 01:31:25 GMT  
		Size: 13.6 KB (13611 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:a0e86a781bd34a91a5a91beff54517d9218d3515493d4eb32779ef44aad1da27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106283272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71f29421ca975892b279f9afc264a09c6210911be0fd7fff77163fbb3f9109f`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=25.3.2.16 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=25.3.2.16
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="15467c6da67f7f4cdbbbd478322c96b370c8d41b82f4b813dbfd8ebc87d4677f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c0fd1793bf8bc1764ff6503ad6f86ae0f1151de2bd8b7285b28dc6f5cc6001c3`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 49.0 MB (49026561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd5a899d476bcdb54a0e4c5af6f910d82b0825f44dbc198193a4bafc21d3712`  
		Last Modified: Tue, 18 Mar 2025 05:28:39 GMT  
		Size: 57.3 MB (57256711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ea0fb1e8b43998a0df410a811a1ba1887823e2563a8e71b899d27fc3c94cb7cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5fbd837ffa79205794235d8afcf70256727c95d1da0b243168dd1cdee74d9`

```dockerfile
```

-	Layers:
	-	`sha256:5c09c8659caf4701c113195a5d119cab84cc9218581c236b936fddb25a80c38e`  
		Last Modified: Tue, 18 Mar 2025 05:28:38 GMT  
		Size: 4.0 MB (3992832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70a967994731fdc7d583a2307b06a63fa6ca1a535ea2145303432c6ad40dff0`  
		Last Modified: Tue, 18 Mar 2025 05:28:37 GMT  
		Size: 13.7 KB (13687 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:44c5d4a62f71aa0d0b779c8725e0a5331000d970a0d392c291890ebdb998f812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116584846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7bb8cab7aaa7dd3e318889ed7fd8c69558c2888a3d425aea42118287fa72f1`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=25.3.2.16 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=25.3.2.16
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="15467c6da67f7f4cdbbbd478322c96b370c8d41b82f4b813dbfd8ebc87d4677f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0f5038819432189ed4f7f564979dc427da5cded801c6d98beaf6489f7216e`  
		Last Modified: Tue, 18 Mar 2025 04:56:59 GMT  
		Size: 64.3 MB (64336452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:fa96165cd3b099e9f316e9a50ecc3e494b44bbd7de6b03eebb3206916ca62670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b0675f5bf756b31ca663b71107738bd14edc17cc5db22841cb651d79b9e13e`

```dockerfile
```

-	Layers:
	-	`sha256:e055ddadb37a7e8a16e21d76e979efcb4a6305e9e04aacbbe41fc3c7b48eaf47`  
		Last Modified: Tue, 18 Mar 2025 04:56:58 GMT  
		Size: 4.0 MB (3990852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:893471a7baef3765f6903d2c48c39ba2baf97addde891fe22b9aaf71a152e325`  
		Last Modified: Tue, 18 Mar 2025 04:56:57 GMT  
		Size: 13.7 KB (13714 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; 386

```console
$ docker pull erlang@sha256:eb3a1966d418e5f456ac16c61ccd377863a869891b622d1a1ca29af946eb586d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112318250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a645b8a93413b6ec3bc1d32ebfecb8af6d21d1fd7f57f4f410f89e22c18121`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Sat, 04 Jan 2025 18:55:45 GMT
ENV OTP_VERSION=25.3.2.16 REBAR3_VERSION=3.24.0
# Sat, 04 Jan 2025 18:55:45 GMT
LABEL org.opencontainers.image.version=25.3.2.16
# Sat, 04 Jan 2025 18:55:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="15467c6da67f7f4cdbbbd478322c96b370c8d41b82f4b813dbfd8ebc87d4677f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 04 Jan 2025 18:55:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e82c0d2b9b893b3957c98c31605595d803c7e985c9cc48f4499cd81fd8c53`  
		Last Modified: Tue, 08 Apr 2025 01:30:38 GMT  
		Size: 57.6 MB (57633785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:3a394de9588b566ac91efc15f684c12c97e3eaad4c75fe7253fa0b47720b8c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f695aec1fdd73e3844c4ca71a1d08fd4a6576910674ba301f6ae0e924a71892`

```dockerfile
```

-	Layers:
	-	`sha256:d54ab7b0bf3d1eff2004babe3e58f846b5a7f9d4e6da2dbeedfe788adc2e0e94`  
		Last Modified: Tue, 08 Apr 2025 01:30:36 GMT  
		Size: 4.0 MB (3989623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ceb4aa33eadb83ddcf5e8fea0abf55e1d77bd22ac8c56f5cc15579cf5218e6`  
		Last Modified: Tue, 08 Apr 2025 01:30:36 GMT  
		Size: 13.6 KB (13579 bytes)  
		MIME: application/vnd.in-toto+json
