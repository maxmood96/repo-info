## `erlang:25-slim`

```console
$ docker pull erlang@sha256:806748d6dab29e9822509cd82c8013dcaa5dbdd9ee4eeafe16edd1e516a1e899
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
$ docker pull erlang@sha256:547a4578f85b5c42c90cbbba0ca62f93b0fa04841074afa082dc091025214cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119684589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4257c6f2e429dac68f57072260c3fbb3adccc335855d051d0eb752ca5bf6f381`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe51744f37d44d4adab0db27c917b0e8ca2bb1968574727d72adb40c7bc68e9`  
		Last Modified: Tue, 14 Jan 2025 02:40:04 GMT  
		Size: 65.9 MB (65945425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0dabe7be51b2dd0dc9a97e7a8539c00a84f2014cadc6914be333ba07876e1442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a7bcb463fa8ae7b8a85d9d3de6150e4437eb2561e5267a2172c11363a79c08`

```dockerfile
```

-	Layers:
	-	`sha256:82696c5aa7260b53c0248dab088fce49f234d9015dc66fa864918ef3382a01d8`  
		Last Modified: Tue, 14 Jan 2025 02:40:03 GMT  
		Size: 4.0 MB (3991231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3244a61e26b14e9803d292b8f9ce556634388907e7ee707141d5fe3d8adbf6b4`  
		Last Modified: Tue, 14 Jan 2025 02:40:03 GMT  
		Size: 13.6 KB (13611 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:8ac235e103ba495212f334b985d37ebc9484d6e98a424b9b640a4b88bc118aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106281776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636ff295c6227032ebb7402c211f771447107c4517cd5dad57d0174cd8818171`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
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
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd16918f3a5e0954b0a55b46f1193881cf174e64723153c94a7ab3d3d3c0ecb`  
		Last Modified: Tue, 14 Jan 2025 09:20:50 GMT  
		Size: 57.3 MB (57256714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0551a272f1c2b64381430f9c805a5f111bcd54ac7c456d1f37e33502924ed802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829b6475ebc186fef9480a77ecc58c29c3e3447203ae93a72a4f53b599fd4e02`

```dockerfile
```

-	Layers:
	-	`sha256:d681aa5d5eb18010edd37b5fe39910eaa7482f24d7efa08d08cdc386e7d78d62`  
		Last Modified: Tue, 14 Jan 2025 09:20:48 GMT  
		Size: 4.0 MB (3992832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d843f02f332b7583fb9487c26ec585c9d4fb79790e583802a2613fbd946811d`  
		Last Modified: Tue, 14 Jan 2025 09:20:47 GMT  
		Size: 13.7 KB (13687 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:49e36562782cdf384c90280d4eccf786f173568482fc18aaf70f4038d3090335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116582452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91059e0633d95ddad5e7da09c9952e3ed3b2ebd3ab5fc5cd93393a85aa757da4`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafeabe50fd229f86c63bd9f8481c6aa7879a46645242b62a8e2e799450b489e`  
		Last Modified: Tue, 14 Jan 2025 20:34:30 GMT  
		Size: 64.3 MB (64336392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c7cad06b06a8d7274bf4661a0ea7e368510dec20b946200a6e3376cf413303ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc336f7aed80d19afc2b0956119c3ebbf15a72ecb34691451f90933f6eb6513`

```dockerfile
```

-	Layers:
	-	`sha256:6f744d6b15baa5c54c01cff244da0a07af0c3d365ac22718331565f6cf2f365a`  
		Last Modified: Tue, 14 Jan 2025 07:19:30 GMT  
		Size: 4.0 MB (3990852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f04705f2471cb883da648dc600df276018b5ecd86a6c7e1a5002a276aacf9609`  
		Last Modified: Tue, 14 Jan 2025 07:19:29 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; 386

```console
$ docker pull erlang@sha256:2897e77b1d87ce6705d1cd4efd74a2bf9555b1353e5a529475210a6d45e14c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112309795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be059dd75106bddb8b94659bfcb8f6a126c2367951d0beb1baddf592fb3ce94`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 04 Jan 2025 18:55:45 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
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
	-	`sha256:b72c0b254e0d45985d121f47650a88f2ee35fbb4ff596c396ee98094e0a26d1b`  
		Last Modified: Tue, 14 Jan 2025 21:24:03 GMT  
		Size: 54.7 MB (54676276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ad6e43986d87e461d5de168c101afa38ae99b4d0cde3a26794f01c9f667c98`  
		Last Modified: Tue, 14 Jan 2025 02:38:42 GMT  
		Size: 57.6 MB (57633519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:761528032a533ecc2cd369231e60248594b9aec22226ba61d485fe3e7d7f0a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cbc40d132a42845c2a3de926622cfaba62b844f776fa9d7d095054b9b543a3`

```dockerfile
```

-	Layers:
	-	`sha256:b890eb1e7637a97a307189e6078f3dad4bf7505206948f1e65595ae9d139c0f2`  
		Last Modified: Tue, 14 Jan 2025 02:38:40 GMT  
		Size: 4.0 MB (3987709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78346c320dc958f302642bd1f6ccba3fc9dc498fbdb89ed10a6844e3c8aa5f7b`  
		Last Modified: Tue, 14 Jan 2025 02:38:40 GMT  
		Size: 13.6 KB (13579 bytes)  
		MIME: application/vnd.in-toto+json
