## `erlang:25-slim`

```console
$ docker pull erlang@sha256:891852b83970cd3a513b78ebecb86a46ca0e18555b380ea71ea35fdda40ffbec
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
$ docker pull erlang@sha256:97d94a18c84bf6fc493364119a4e374f05de3ac591992a3b2daee7c78273a1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.7 MB (119697502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0d3b1758fdac21b518a3cc16b01fd2044a395f8530ac94cb4edf2ac1cbd9fd`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=25.3.2.20 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=25.3.2.20
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="513bd9d2fc9c792984314feead5d971bb19e6ee531b4e208d4d4fd30774523f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62271ee27e2dd6662689af02747984aae4bd79d4030dbbd1f42dd950aebb1a4`  
		Last Modified: Mon, 21 Apr 2025 22:38:04 GMT  
		Size: 65.9 MB (65948973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:18cff1d14f130d8bd77bed17baf07296360a9305d56e95393e3e421690c2dd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e3bde124ef6ff056954b62724f23c870e3785b3d144210c3d1ad4c93b88206`

```dockerfile
```

-	Layers:
	-	`sha256:a8021e605d81db38d53cca4022326160deb5e89b247c4ca7a396afd975c20264`  
		Last Modified: Mon, 21 Apr 2025 22:38:03 GMT  
		Size: 4.0 MB (3993145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45762bf1c87656ebc0224f995b4fc10737f91953967191d47a68a1c230410b12`  
		Last Modified: Mon, 21 Apr 2025 22:38:03 GMT  
		Size: 13.6 KB (13611 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:46ac4c1cec5fa87371310fc2808f2d4eabf3160ab4fdb104a40b3931ab65ad14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106289742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e51365172385e715ad38e88881fb98602aa7351a58d2a545c8f6c050c65af6`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=25.3.2.20 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=25.3.2.20
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="513bd9d2fc9c792984314feead5d971bb19e6ee531b4e208d4d4fd30774523f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8c2fc9e6d23f3debfa68416a2b96331b92d563b20272933315ecfbbada38e955`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 49.0 MB (49031449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a5282319efd792e02657a2b8a3513ea94db836bd704709ba26de95e3356aca`  
		Last Modified: Mon, 21 Apr 2025 23:25:07 GMT  
		Size: 57.3 MB (57258293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:dc6d9fcfe03e2c6b3dc90cb0af4aa59e76c5fab1577aacdbdfbc41339299f46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4008433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f33e0552a8dbcd5affae5a97f435d4a07f95820b01276ea9c6e4fd2df55b576`

```dockerfile
```

-	Layers:
	-	`sha256:f95f489560f8d5b105642362c0c99a782ac1ac1dac5a22d0356259fbf33e8d10`  
		Last Modified: Mon, 21 Apr 2025 23:25:05 GMT  
		Size: 4.0 MB (3994746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96c0cf3e8f0ca38d91d895771422b94dccad37c725ebbaa9138dfc684a25af22`  
		Last Modified: Mon, 21 Apr 2025 23:25:04 GMT  
		Size: 13.7 KB (13687 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:eeb9750c9dcdd4b5eae72bbebce9ddc7f514413eedb3b46a9b5d8616e0f7eb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116599217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8939f2b319f19a347d336d39badc16fe70224f92a97c7ed008356edcbcbe59f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=25.3.2.20 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=25.3.2.20
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="513bd9d2fc9c792984314feead5d971bb19e6ee531b4e208d4d4fd30774523f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48b2032e45ce476d33ef8a83b3484a0d27b164f85a89616b38c4807a298e952`  
		Last Modified: Mon, 21 Apr 2025 23:23:01 GMT  
		Size: 64.3 MB (64344995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c27358b9d3f182dfba0a3d1896719da105862080ebd42f19a36cb3416f47fec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2267471999bfad05847bb783e2ac49493c12a3f94a8b75ae060989f34dd93efb`

```dockerfile
```

-	Layers:
	-	`sha256:1a7a1207367bc730e7fdd650b636dd8ec5cc5c130ea5511d90f8d7ec3d6b5ca7`  
		Last Modified: Mon, 21 Apr 2025 23:22:59 GMT  
		Size: 4.0 MB (3992766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39bca97cccab86194d28e47aad2b43725004703190a82523c1a9657ad986f6e5`  
		Last Modified: Mon, 21 Apr 2025 23:22:58 GMT  
		Size: 13.7 KB (13715 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:25-slim` - linux; 386

```console
$ docker pull erlang@sha256:cd9112392a25c3ad6c9f23b216b6f3f7b812843fb7d0f876e90b48c60399588d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112314447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083ff3e1a69d387878b4306c760c3fbceba0debd8edc27125a740992049f00e0`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Sat, 19 Apr 2025 03:05:32 GMT
ENV OTP_VERSION=25.3.2.20 REBAR3_VERSION=3.24.0
# Sat, 19 Apr 2025 03:05:32 GMT
LABEL org.opencontainers.image.version=25.3.2.20
# Sat, 19 Apr 2025 03:05:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="513bd9d2fc9c792984314feead5d971bb19e6ee531b4e208d4d4fd30774523f6" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Apr 2025 03:05:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095896b53d4ec01411bd35b2b515665ccb74e9a93e03a46aea0a58f3a01f0522`  
		Last Modified: Mon, 21 Apr 2025 22:38:26 GMT  
		Size: 57.6 MB (57629982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:25-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:8f2fa6d4ff491ca0623712811f7ea21dcb298b09ba5fbe18625cf262d571a590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d1fa07849f9ecbff37b33d6193ba4c05ba0ba7f9aa626c7b4ec948e09088f9`

```dockerfile
```

-	Layers:
	-	`sha256:1ac7b07cfac7a877034b0459c95ee23c98fc79fa72cbf0b21bb1e4c45d21b3d5`  
		Last Modified: Mon, 21 Apr 2025 22:38:24 GMT  
		Size: 4.0 MB (3989623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29161ed9b022614071fbb35b8762943f2262d2ba2301c04b7e5d389f86e8204c`  
		Last Modified: Mon, 21 Apr 2025 22:38:24 GMT  
		Size: 13.6 KB (13579 bytes)  
		MIME: application/vnd.in-toto+json
