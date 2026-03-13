## `erlang:27-slim`

```console
$ docker pull erlang@sha256:f71d3c0d32210668f20d5f981280062e7d81ad51e37e7cb6ed72d67bc34785c1
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
$ docker pull erlang@sha256:dc00a4580fde5ea855c53b2ecbacb98460d204bd02baeede25bddf069e00c6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124536860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e0c9897f5551fc88fc830fd9b5f93c65e297776190338bacac81f018f0c645`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Fri, 13 Mar 2026 17:15:21 GMT
ENV OTP_VERSION=27.3.4.9 REBAR3_VERSION=3.26.0
# Fri, 13 Mar 2026 17:15:21 GMT
LABEL org.opencontainers.image.version=27.3.4.9
# Fri, 13 Mar 2026 17:15:21 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="62e964290041eed1182e1a1dbf934193aacd2e124b315cd5b9ffd9dd0d3b0f8f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 13 Mar 2026 17:15:21 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422e85a8f83be72936593f0abd7a0b21b89d2b13e9dea4fb674e900598703e52`  
		Last Modified: Fri, 13 Mar 2026 17:15:36 GMT  
		Size: 76.0 MB (76048083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:748a103d76dea003ed55c803f31b26a2824017b9133324effe7fc42f169480c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e9dad6c38db0896cc7d448bff0ed15fffb37971652a3faf461b04a6d3a294b`

```dockerfile
```

-	Layers:
	-	`sha256:d6106ffbbf89758962bb8d00389778fc970ef4305ec8d9052855b7afa301e647`  
		Last Modified: Fri, 13 Mar 2026 17:15:34 GMT  
		Size: 3.8 MB (3824777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d165217528e2f336719a27c6925a55514c8ef6efe85e6d5ce89b84b215a7904c`  
		Last Modified: Fri, 13 Mar 2026 17:15:34 GMT  
		Size: 13.6 KB (13636 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:24e3014ad1546389c932931a960cde44816157d933ba085ab35e7188760ab535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111559485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9517e09e8af0a57adf285d04e3b5ea9d5953b72ae8ccd41d14df4e49a10419`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1771804800'
# Fri, 13 Mar 2026 17:15:47 GMT
ENV OTP_VERSION=27.3.4.9 REBAR3_VERSION=3.26.0
# Fri, 13 Mar 2026 17:15:47 GMT
LABEL org.opencontainers.image.version=27.3.4.9
# Fri, 13 Mar 2026 17:15:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="62e964290041eed1182e1a1dbf934193aacd2e124b315cd5b9ffd9dd0d3b0f8f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 13 Mar 2026 17:15:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e6dff74bad3c0a4d20c6ddf48bb9ccf82f570d23f324336b4a4e2168c71b093e`  
		Last Modified: Tue, 24 Feb 2026 18:41:45 GMT  
		Size: 46.0 MB (46021660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef00d863e0d421fe124f637986535a2426112b13f2b29fd886890fe40d9fbb4b`  
		Last Modified: Fri, 13 Mar 2026 17:16:00 GMT  
		Size: 65.5 MB (65537825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7d82dd8c0518e02dbe02a75ca562d4e5d2af03508f1d3ca28bbb76b3c55f0e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af697b0b809e679cce29fbeb626e1ada0fd046c5204e03fde0cead498348d810`

```dockerfile
```

-	Layers:
	-	`sha256:d76f321dd70e3391117deba74ac4a09040c49ae0d3bd40409b66a2aa49827834`  
		Last Modified: Fri, 13 Mar 2026 17:15:59 GMT  
		Size: 3.8 MB (3828585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31d1c2e30ec8dda2511285ad01ce69aa2f83b4195441223013135bd2e2cfa4df`  
		Last Modified: Fri, 13 Mar 2026 17:15:59 GMT  
		Size: 13.7 KB (13716 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:f396a049e96e25855a5df0e5b3d49b2b5eec612ef3b2dea5c936cdf06e58a5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109366798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c99a9c45a536e08053357892d68de919f20533f505aed848d332674ba165c2`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Fri, 13 Mar 2026 17:16:00 GMT
ENV OTP_VERSION=27.3.4.9 REBAR3_VERSION=3.26.0
# Fri, 13 Mar 2026 17:16:00 GMT
LABEL org.opencontainers.image.version=27.3.4.9
# Fri, 13 Mar 2026 17:16:00 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="62e964290041eed1182e1a1dbf934193aacd2e124b315cd5b9ffd9dd0d3b0f8f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 13 Mar 2026 17:16:00 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa2abbd47f6c966b703d6a814909b9f0be9b5bae14728026fb4b2f90837de95`  
		Last Modified: Fri, 13 Mar 2026 17:16:14 GMT  
		Size: 65.2 MB (65158980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2daf959c2c4452f5218ddb0449e639a23c3c0f3d13014701f5cf16ba142edbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46203c826fbac3cfeaaa512503e4dc1a9fbf2b89dba78402995fba14715c1ee`

```dockerfile
```

-	Layers:
	-	`sha256:7c8f36c1108a581a9a8235d5c7911c22c29656d6808988e86b26c757dd9b6639`  
		Last Modified: Fri, 13 Mar 2026 17:16:12 GMT  
		Size: 3.8 MB (3827010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b9cb37e1aec89631e28dab6a75fca84e86683c546d9a4e93d80473754a423e4`  
		Last Modified: Fri, 13 Mar 2026 17:16:11 GMT  
		Size: 13.7 KB (13716 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:3e228c0abdf4c451bdfa375a4fd323c0125d380cde9cfddfd0a617d422f7273a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122160493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecc5ae8e6292037e61abf864c87683868683c775479ba35a2eb21a26d7b3ef7`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Fri, 13 Mar 2026 17:15:19 GMT
ENV OTP_VERSION=27.3.4.9 REBAR3_VERSION=3.26.0
# Fri, 13 Mar 2026 17:15:19 GMT
LABEL org.opencontainers.image.version=27.3.4.9
# Fri, 13 Mar 2026 17:15:19 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="62e964290041eed1182e1a1dbf934193aacd2e124b315cd5b9ffd9dd0d3b0f8f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 13 Mar 2026 17:15:19 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f39fd17e74bb006f78e373b69e50d6370162250a6999100017d6dbe0eb3830e`  
		Last Modified: Fri, 13 Mar 2026 17:15:35 GMT  
		Size: 73.8 MB (73787283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:8910710a008e50e8b5f8acf26f3bc37fda2b2b488fdd5e0d02646181fe3ffd6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3306c7f3c77b7fe882fb3f2b056367070c8ab11bb1e603e1ac9ccfd0845d0d9e`

```dockerfile
```

-	Layers:
	-	`sha256:4ed1d3a833c78356a98c59e4dbbc28942e9499158b6298da71664f60df863485`  
		Last Modified: Fri, 13 Mar 2026 17:15:33 GMT  
		Size: 3.8 MB (3825038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1857fd77c6e1a30287da7151d6a80a4846fc2818e459ea4c393db58834e3631`  
		Last Modified: Fri, 13 Mar 2026 17:15:33 GMT  
		Size: 13.7 KB (13740 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:d350ffc215593453d9c8a67724857235dc5734129c081e1b58652c2c3015a4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115674702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499a76eefbe50219eb69ae4e089207c0cdc44f4bc0c9096080d68529933b317e`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Fri, 13 Mar 2026 17:15:53 GMT
ENV OTP_VERSION=27.3.4.9 REBAR3_VERSION=3.26.0
# Fri, 13 Mar 2026 17:15:53 GMT
LABEL org.opencontainers.image.version=27.3.4.9
# Fri, 13 Mar 2026 17:15:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="62e964290041eed1182e1a1dbf934193aacd2e124b315cd5b9ffd9dd0d3b0f8f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 13 Mar 2026 17:15:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:443394a7d911f581670ce4df7959c82f7e8f0be02b5a7ba3c71bc5958012963d`  
		Last Modified: Tue, 24 Feb 2026 18:41:48 GMT  
		Size: 49.5 MB (49477853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735bfdca712ead5f49511a41876ff0a80bacd31c7ab774ecd95a4504aa92e93c`  
		Last Modified: Fri, 13 Mar 2026 17:16:07 GMT  
		Size: 66.2 MB (66196849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:533dc9a0a2df030677e40cc08814d6f0aba958ae7d21f49ef488f98f760f4364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1dece1698481a1bba701d0505d47fd7c1c6ce5ccf565d6767cf68942852958f`

```dockerfile
```

-	Layers:
	-	`sha256:7e46dd2070e693a20a8723793ee47fe506f45b92e8acfdb4be727a9fb84c77b8`  
		Last Modified: Fri, 13 Mar 2026 17:16:05 GMT  
		Size: 3.8 MB (3821938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7e44a7e183142e3560fc96545f47321f525fc16981c4d16e83ab5eb4abbe3c`  
		Last Modified: Fri, 13 Mar 2026 17:16:04 GMT  
		Size: 13.6 KB (13604 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:b9d8b72f93a197f615bd30980d8f4b67d89fec7afdef9514bffb55eceb082a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114895094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b4d1b7a51d9632aa49c5fff9959d10bdfe6e756dfeb79ed1e34f89a63dc85c`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1771804800'
# Fri, 13 Mar 2026 17:42:44 GMT
ENV OTP_VERSION=27.3.4.9 REBAR3_VERSION=3.26.0
# Fri, 13 Mar 2026 17:42:44 GMT
LABEL org.opencontainers.image.version=27.3.4.9
# Fri, 13 Mar 2026 17:42:44 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="62e964290041eed1182e1a1dbf934193aacd2e124b315cd5b9ffd9dd0d3b0f8f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 13 Mar 2026 17:42:44 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6ec71ee94fb878725e70f6a21c20349985b89066361ee1f753b3854cfa2c839a`  
		Last Modified: Tue, 24 Feb 2026 18:41:37 GMT  
		Size: 48.8 MB (48782510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c648817e0f3ff560edc8f5e19a0dacfa541e0946191fa941386dd17af4de27`  
		Last Modified: Fri, 13 Mar 2026 17:43:52 GMT  
		Size: 66.1 MB (66112584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2db668ddf80cc836c3c0dfc387619b355df4c0156d9397795f4014a15f83bfa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e46600e82c40bfbdf8f50de7d0882829584e7e3d1b5249844a29cbbf9e408f`

```dockerfile
```

-	Layers:
	-	`sha256:60daef81952755b2fe9f64655f421528980f129450c06057dc65ccaa9352cec4`  
		Last Modified: Fri, 13 Mar 2026 17:43:44 GMT  
		Size: 13.5 KB (13487 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:f0de098a78e46c713bab3777c0ca35470853e4de20fff5618940506136981b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.6 MB (119608466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b03f561d59fe37fbcdbcb890236e713ea901de1f43c346df0b680b14dc37ac7`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Fri, 13 Mar 2026 17:24:33 GMT
ENV OTP_VERSION=27.3.4.9 REBAR3_VERSION=3.26.0
# Fri, 13 Mar 2026 17:24:33 GMT
LABEL org.opencontainers.image.version=27.3.4.9
# Fri, 13 Mar 2026 17:24:33 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="62e964290041eed1182e1a1dbf934193aacd2e124b315cd5b9ffd9dd0d3b0f8f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 13 Mar 2026 17:24:33 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e071ff0d6f6073c88882de5af80c40f774b7ab6b4ef0fd6e0014ea4e255f38`  
		Last Modified: Fri, 13 Mar 2026 17:25:00 GMT  
		Size: 67.3 MB (67271669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9fe81408bd0386bb961a3920d5ce29b849a28f56f6e4686cc94b638b017b1392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360b07d21ffb9dbd91a80408574bddc11707a8dd73f62c7e98a3c3e1c1a8dc50`

```dockerfile
```

-	Layers:
	-	`sha256:22d026a73ab52e89331ea9dd01fbd91075960b6f25d91e537f7f9fdbf6a81f9f`  
		Last Modified: Fri, 13 Mar 2026 17:24:58 GMT  
		Size: 3.8 MB (3829227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be11a203365e7ba0582e588f0e9eba814bb7f9b5d90542ec6051fe608b6c2116`  
		Last Modified: Fri, 13 Mar 2026 17:24:58 GMT  
		Size: 13.7 KB (13679 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; s390x

```console
$ docker pull erlang@sha256:a3eb665ec5a3f5d8e0281ab0f02b4b80457fa34e5ba0b4e0deedd226dd47eccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113085614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a9644ebd3f736ebabbcc7b337fdd9c2d3438930b96ea8af3e368977a42f01d`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Fri, 13 Mar 2026 17:17:26 GMT
ENV OTP_VERSION=27.3.4.9 REBAR3_VERSION=3.26.0
# Fri, 13 Mar 2026 17:17:26 GMT
LABEL org.opencontainers.image.version=27.3.4.9
# Fri, 13 Mar 2026 17:17:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="62e964290041eed1182e1a1dbf934193aacd2e124b315cd5b9ffd9dd0d3b0f8f" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 13 Mar 2026 17:17:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a4518337d4050c21e7693bed21cd4b468a584d6d959431b5081655053f28ae`  
		Last Modified: Fri, 13 Mar 2026 17:17:49 GMT  
		Size: 65.9 MB (65937527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c0213b70f7ad36bc683e6b99b21f2c8c1769fff07ccb36c48d889c493f76b346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34990744e790527b4206b90903c357563d906804a2ddab5c2e51ae5998b2161c`

```dockerfile
```

-	Layers:
	-	`sha256:edad08077e7aa37196164b0d35a9c15f2628a59d47aa3053ff00e5acb0a4c75f`  
		Last Modified: Fri, 13 Mar 2026 17:17:48 GMT  
		Size: 3.8 MB (3821605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e07329425cec01c9eb897146408ce4600165c82a4f8ccf784db8446c840e7a`  
		Last Modified: Fri, 13 Mar 2026 17:17:48 GMT  
		Size: 13.6 KB (13636 bytes)  
		MIME: application/vnd.in-toto+json
