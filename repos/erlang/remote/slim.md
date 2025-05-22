## `erlang:slim`

```console
$ docker pull erlang@sha256:b2514bd3b4e8237fce5ca63bea487d55e87d03a1e3debba11d3ff21e4f23ccc4
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

### `erlang:slim` - linux; amd64

```console
$ docker pull erlang@sha256:7582799b78c14cc8ea1afd7bfb78b9299ad39ef4d1cd295f20ef3325369dc115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128322897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a849f8a9838f472955d1db74e72c1b5bfe83a82daf876439217d39ec56e308`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b0bc1520738354dda297bfac5f8a30ae052deef27d5caef97ac84667bfa829`  
		Last Modified: Thu, 22 May 2025 16:45:04 GMT  
		Size: 79.8 MB (79834652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:607e1287b192eb78345e70b007b59aceed0a5dadeae3dbb5edeb90ad875ee6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b6314f66f301f40fec9de60ff76c05f832d10f534d2a40729b9dd8dbdedce0`

```dockerfile
```

-	Layers:
	-	`sha256:7201a3828eb578eb949763de2e5af357d74896533ff7be2e3b13d9586f8546db`  
		Last Modified: Thu, 22 May 2025 16:45:03 GMT  
		Size: 3.7 MB (3726581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20b427f2abfd90de3b43d8a38afb7942348105fe2bb8a29d0ffff14edc0987a3`  
		Last Modified: Thu, 22 May 2025 16:45:03 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:cb945b5233df5a442f5378835a157f686ddf841161d1dcd2ef3b5c0adbcb543e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115534392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126cd79142b63dcfcdf7498abc44d5c8bd75c976c2867400a608095c5fdc1ac9`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d34b66573dd99436757429c603646ae3e6d1948a3fa85413a39cf069620a7229`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 46.0 MB (46021484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7202fa27afdce2d6f3cfeced69aa7e60f039e8b6e799dc7553343ab9a56628dc`  
		Last Modified: Thu, 22 May 2025 18:41:39 GMT  
		Size: 69.5 MB (69512908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7af1f72aa48952210df2b1b5ae591abfc4c6712dcf8d6b311e2d273715bc7645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e224ef4867f3b1a829f1a47ff0de7915d6c6b8931e8999d4c3635f50d07796`

```dockerfile
```

-	Layers:
	-	`sha256:1804feb6f653fabee24fcb0edf4e6b6309bf8c8bd4bda51f95f695a729deb3a3`  
		Last Modified: Thu, 22 May 2025 18:41:37 GMT  
		Size: 3.7 MB (3730397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959d7dd62fd70215a6e2a4df18df02223c6ed02c93bd5dac49de057f8e4902f3`  
		Last Modified: Thu, 22 May 2025 18:41:36 GMT  
		Size: 14.0 KB (14049 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:fdd1082beb82b537fe72f490e5f8e13fc53f4b28d72ca62c75934265a2b45878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109305222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6be861177f389810ac2cb296cbbb48e1f48dc7550ebdf9f0472491ab328a463`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 21 May 2025 03:51:36 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.24.0
# Wed, 21 May 2025 03:51:36 GMT
LABEL org.opencontainers.image.version=27.3.4
# Wed, 21 May 2025 03:51:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 03:51:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Wed, 21 May 2025 22:27:37 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4056b24923370ab4a3c97776cd28a77d8c5015a0cba802d50d1263ab7a07149c`  
		Last Modified: Thu, 22 May 2025 02:44:26 GMT  
		Size: 65.1 MB (65102451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:acf60dfee4fde75a256be36923080e22d4069f74ee4d4ad2f64294fb1ba3efe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff743142ac9cf3d86484ca089e9e7a9991b55fa1e72ba37ff720a609e342ec1`

```dockerfile
```

-	Layers:
	-	`sha256:d95c432c6d2ec693c27f990f348b22dc7bc4962540f0e903e78edecc1e8d782d`  
		Last Modified: Thu, 22 May 2025 02:44:24 GMT  
		Size: 3.7 MB (3728964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c686a6e69f86c8616abba21aa8ae9ca898280fc093930668bfff478dc24a7f60`  
		Last Modified: Thu, 22 May 2025 02:44:23 GMT  
		Size: 14.1 KB (14050 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:75faf032f7175f217e863a227e4434e0eb7417f9da378f2591c5d02d5071476c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122042335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dea886b91d087f2a3749da08b6525e1ffeb75022f5786d189ad6e5907bd6b0`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 21 May 2025 03:51:36 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.24.0
# Wed, 21 May 2025 03:51:36 GMT
LABEL org.opencontainers.image.version=27.3.4
# Wed, 21 May 2025 03:51:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 03:51:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f204126c24e8ca10364bad2de3a02ad951a5617703fbb99d9b2a7e787468a8`  
		Last Modified: Thu, 22 May 2025 02:59:31 GMT  
		Size: 73.7 MB (73715154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:8b0b9deff513c1eee1afeebb5e30592aec7dc1124e3dd7e664a6073a175923f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4153be7f294ecfd9aaec5b8dc00b1cbd068a1dc2f35c98d3025403628bb8c249`

```dockerfile
```

-	Layers:
	-	`sha256:21916f38a987e935833adc4e05606a0a5d77549c7473dc79bb30036a4c6cceae`  
		Last Modified: Thu, 22 May 2025 02:59:29 GMT  
		Size: 3.7 MB (3726996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3182554f32ee98e195a38eb49e41ddd8080667f6ee02e6f434d07122a58fdd12`  
		Last Modified: Thu, 22 May 2025 02:59:28 GMT  
		Size: 14.1 KB (14082 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:a545189d84d176d6c7cd00ea3e81e7fd22a2cd8f0e96988ff7d7de33600424e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119520837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c1de65292665e84d5669e7a92e4b43104762df614d6c99b75deb873dead094`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ca1131da27fa92df7d859e539db268d5742ced8bdc8ac24f39131dd8cc32b7`  
		Last Modified: Thu, 22 May 2025 16:45:05 GMT  
		Size: 70.0 MB (70049275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:80d4c303c05111becf88207b4fe025473b7507c1fbfb7d497cd91051c2a7dd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7537b522a68d848280de8e5aa6ff8c6fe7d676bbb393fe977cbc7c0990dd4f`

```dockerfile
```

-	Layers:
	-	`sha256:84afd50da7c0e9cae144dc74f3b17a6e3b494726fa70a44f6b13d2c9375870c0`  
		Last Modified: Thu, 22 May 2025 16:45:03 GMT  
		Size: 3.7 MB (3723743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6a162d3169c903594074ed6cbefb8e5948f1f4178fc1cd6ae13b4cf5f69393`  
		Last Modified: Thu, 22 May 2025 16:45:03 GMT  
		Size: 13.9 KB (13928 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; mips64le

```console
$ docker pull erlang@sha256:4d79b53107ba848f541375830278b72a5cd34e0bad148a32ed737a0e4e56ba4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.8 MB (114826577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63581ac736ed1daa6052daa14f9f0ee69a7ce740367452874a255f33be2a2e0`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Wed, 21 May 2025 03:51:36 GMT
ENV OTP_VERSION=27.3.4 REBAR3_VERSION=3.24.0
# Wed, 21 May 2025 03:51:36 GMT
LABEL org.opencontainers.image.version=27.3.4
# Wed, 21 May 2025 03:51:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="c3a0a0b51df08f877eed88378f3d2da7026a75b8559803bd78071bb47cd4783b" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 21 May 2025 03:51:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d480a40975e955224ed64be37e82f220f731f0379d20a7b8c36be0e47e31d8df`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 48.8 MB (48769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51416a61254901b7d3598caf4c21885679cf3cbf93ce400f93c37e616ed79c50`  
		Last Modified: Thu, 22 May 2025 06:44:13 GMT  
		Size: 66.1 MB (66056824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7eaf4a05a1d91be87242c8b04b1171fbb923c317d365102f0942d98500198568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87886579940542a4af169a4264944dec17956e2aadc403b5de3b68a9c396e76`

```dockerfile
```

-	Layers:
	-	`sha256:4f51650e3b58b94bd0a4827d8581c4ba67ed8334b77890d7c74e0e2fafaa6793`  
		Last Modified: Thu, 22 May 2025 06:44:06 GMT  
		Size: 13.8 KB (13827 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:4119147da31b5ba5d3eb5e9988ac20dd9343bfadb5bfc13f613c61de811e811b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123397387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373698f6de69451b114576901b31a27cf6e0222c02a0c92b88167011ee5cad3b`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88547891be63f2b608bc231c7557fba2fe192759467fb6e214874d634a320bc`  
		Last Modified: Thu, 22 May 2025 17:06:09 GMT  
		Size: 71.1 MB (71065768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d379d06d3adb9d2268dba5132049a3d023f9d27ab3cd5d7e2e4aa8fe5bea11b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5542904b38b6f9a19974fe2dd6ee3f270ace31fe32dd34c27d4e40f27c3dec4`

```dockerfile
```

-	Layers:
	-	`sha256:16767e63f46254c48c4f3116ef66e90d4618e26ee894350e33f0bcdce969b177`  
		Last Modified: Thu, 22 May 2025 17:06:06 GMT  
		Size: 3.7 MB (3731025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f09b786e7a8d3a6c90f2b301aca4027cadae1fa1cb353d1932d01df018a8ea10`  
		Last Modified: Thu, 22 May 2025 17:06:06 GMT  
		Size: 14.0 KB (14015 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:436b7224ec58b514a23386b2a7a0f21aeda0eeb09e44630e86917c6302626886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116817598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137881c201df44843d8247479d0e6bab45f8936116d43a344836c43788167f9c`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026a57d20a879fb2b3cd9a28d1261babfd12a99e574be1263c4b77d06a8af598`  
		Last Modified: Thu, 22 May 2025 18:40:27 GMT  
		Size: 69.7 MB (69673756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6d28544c48a693ba5696ed3489c2b6a5e972e5ff8fd7db60cac6e790dbc067ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6765af1b738d89251669dca5fd472b6d36cb1b623cef8db2a8777e04afc3840c`

```dockerfile
```

-	Layers:
	-	`sha256:78dd46fdc6b2cae2c29d43de2681ca95226357e4b7438db2bcb53c5dbaf4fd55`  
		Last Modified: Thu, 22 May 2025 18:40:25 GMT  
		Size: 3.7 MB (3726301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c6dadba143685d19e7628d128fd66183e9514d9b6f4223869ee76035aa3d19`  
		Last Modified: Thu, 22 May 2025 18:40:25 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json
