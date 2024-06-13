## `erlang:22-slim`

```console
$ docker pull erlang@sha256:8a74ab1470938bc0a88fa2d118ef8f5356f98afef679fb9c30b396754705cbe5
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

### `erlang:22-slim` - linux; amd64

```console
$ docker pull erlang@sha256:90bddd23d950143de5cba52080d33bf66bab6deea11a6e08e6cf19ea378a7f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.1 MB (111123510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66917381b5a94a4e78b68e8b099f22cde6edb3e67ef146dcecd2a4929def1580`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:82f06126089fd0ca482c29baeb90ef37ac3a9f5f6a0f2f5c968a605846627d47 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=22.3.4.27 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=22.3.4.27
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0fb5dc388a4d6f1c7c0e250b5a44466727f35794b0566cad4190cd7c68ca5062" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3892befd2c3f36ceb247ba7d906de12601d69b806597e65c4c837cf3d93df119`  
		Last Modified: Thu, 13 Jun 2024 01:26:34 GMT  
		Size: 50.7 MB (50657373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932fe466cc2abe095ce33dc9c17459ef0b4ae1ded9848ef185c82d585be402b8`  
		Last Modified: Thu, 13 Jun 2024 18:22:45 GMT  
		Size: 60.5 MB (60466137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:22-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1b5c551f0fe9618172a1ad5647c7712ce86ea555efa2dca48a11ed98d234002e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4002906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc37e0ed1d497e3c9ac5a4ae3d785515138fff4849da8d8097628a856775ed45`

```dockerfile
```

-	Layers:
	-	`sha256:41ccc85471e0edf69243948a6cc4d61c49d547852ff0125d1849a20432e9f07f`  
		Last Modified: Thu, 13 Jun 2024 18:22:44 GMT  
		Size: 4.0 MB (3989540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b601c524825d355e59f1a380d4368d3a2b1560bca448a8aff0cf0100219b2dc`  
		Last Modified: Thu, 13 Jun 2024 18:22:44 GMT  
		Size: 13.4 KB (13366 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:22-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:59d3e1497eac29d8553dec44c04a8dd0955583913fa2777ba0442030afaced90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102347764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d08b7b103cb6f72f49df1bd6c2eaae8f22de040254845ac8433dc548d67668`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:a412a8d68ab5b47e51cbbb8ae3797bc960802ae45716dda9d517985663677bd1 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=22.3.4.27 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=22.3.4.27
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0fb5dc388a4d6f1c7c0e250b5a44466727f35794b0566cad4190cd7c68ca5062" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:36ba9c8baad7d50b1a4b523006966a56ab736274cf5108a528d21b65d3e5927b`  
		Last Modified: Thu, 13 Jun 2024 01:02:44 GMT  
		Size: 46.1 MB (46129853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e835087322c9a5d572a1415db7fc758eb412933a94f2a8391d72817072680d8e`  
		Last Modified: Thu, 13 Jun 2024 13:32:33 GMT  
		Size: 56.2 MB (56217911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:22-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1f207de59514032639d162c966d09eb48bedddb85adf1724bb6b64670251f59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4005045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6774ce3d7edbc771054b451878cbeb90ae71518e97f0376d4d545b1b72834599`

```dockerfile
```

-	Layers:
	-	`sha256:10e4994032b4038caa09e4093080b3c01cd989a5f20f39c3c76dc2d2beeaa51c`  
		Last Modified: Thu, 13 Jun 2024 13:32:31 GMT  
		Size: 4.0 MB (3991609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f3f130c1fcd565ea9463ab52fc6b80cfbb8636138a8ccb9331a8373c8ce4366`  
		Last Modified: Thu, 13 Jun 2024 13:32:31 GMT  
		Size: 13.4 KB (13436 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:22-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:f7c5c7228b1a057dd537d025b24ef2f8f0b3dcceb95bfb96ce2fc7dc767add7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106819803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c615f513a9b22c03d1205ec3a43d5105271e5faa2f4203caf870c438247e8f`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:fab836e338e4004f9cd2a02c2be38bf1bae832de12dd4fd657c94cbfb739e7f0 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=22.3.4.27 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=22.3.4.27
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0fb5dc388a4d6f1c7c0e250b5a44466727f35794b0566cad4190cd7c68ca5062" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6fd6935d93f420effd7ed408f8df1ad31990dc3cf356be01e2e5ed55ee6ee084`  
		Last Modified: Thu, 13 Jun 2024 00:44:12 GMT  
		Size: 49.5 MB (49453258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9049be007dbe1d42bf1daac98997a523caf01a8ee885d0bf9d69a3a67bd00e1b`  
		Last Modified: Thu, 13 Jun 2024 13:21:24 GMT  
		Size: 57.4 MB (57366545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:22-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0caa60df3e89517b9c656cf2d42032bd8f131f23031cea63df7357ef9e71eecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3007a18aa618e5acb7be4966f6c2584ba04715fdd699cfc319a90a29905224d`

```dockerfile
```

-	Layers:
	-	`sha256:7be4956decb9c11934fd595b66bff3ac055032b48743ae54ef4de80f2606893c`  
		Last Modified: Thu, 13 Jun 2024 13:21:22 GMT  
		Size: 4.0 MB (3989745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e0c1610cd50c5a32471fda903adc03f1713fcdbce47553662e979b4702aabf`  
		Last Modified: Thu, 13 Jun 2024 13:21:22 GMT  
		Size: 13.7 KB (13668 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:22-slim` - linux; 386

```console
$ docker pull erlang@sha256:d10f78a26601fcbef765fb87b6a2801a53689012eebe1d0d2602748a12fa34df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111215778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1763fce83649322a3a99f912c9147aa617d46ef032ff7ba1b041a1b58a8adcc4`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 11 Apr 2024 00:48:02 GMT
ADD file:669a83c91875a1d1eb004c86873e9d21ebfb93383de70d69b09b54c9b77c3136 in / 
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["bash"]
# Thu, 11 Apr 2024 00:48:02 GMT
ENV OTP_VERSION=22.3.4.27 REBAR3_VERSION=3.23.0
# Thu, 11 Apr 2024 00:48:02 GMT
LABEL org.opencontainers.image.version=22.3.4.27
# Thu, 11 Apr 2024 00:48:02 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="0fb5dc388a4d6f1c7c0e250b5a44466727f35794b0566cad4190cd7c68ca5062" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Apr 2024 00:48:02 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:56417c7163bdf20fbda4fcf20a45320ba1e467ed7427850fd8cdad8f6ed0e5a8`  
		Last Modified: Thu, 13 Jun 2024 00:44:28 GMT  
		Size: 51.4 MB (51419913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b5b79bae1a99f8948baa3fd897b8425e4128b64a6a1efd007956717a8ef4a1`  
		Last Modified: Thu, 13 Jun 2024 02:07:35 GMT  
		Size: 59.8 MB (59795865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:22-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:082613f2a277c9240d5f3c6c26d85f9544c6be99604cc01944ae7752426a222b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a790715349c2ec354fadc5d30b0754f15102a200317d796f2af974015d71d9`

```dockerfile
```

-	Layers:
	-	`sha256:7a73bc8729aad417b9764aacf05e0f76a25e1843ce4216df17bbfdbd0c8a947c`  
		Last Modified: Thu, 13 Jun 2024 02:07:33 GMT  
		Size: 4.0 MB (3986783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be5846c1cbe1de9c82b854568264a52886e3e0ef743fe0117e2eb23564f36cf6`  
		Last Modified: Thu, 13 Jun 2024 02:07:33 GMT  
		Size: 13.3 KB (13337 bytes)  
		MIME: application/vnd.in-toto+json
