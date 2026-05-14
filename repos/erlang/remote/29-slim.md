## `erlang:29-slim`

```console
$ docker pull erlang@sha256:9adcf0f7064062d301cc121d5a8a4e51ada63811692a7b0b324c459de2642b78
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

### `erlang:29-slim` - linux; amd64

```console
$ docker pull erlang@sha256:4b18a65620d8476c9ffce39e7af119e991b641a1ee452440f056f6cb4640bce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129594594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05308d6761c7a3004cb7d569b80eb5a617c64c2ae5e944acc49cfc70e50ed79`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 16:54:16 GMT
ENV OTP_VERSION=29.0 REBAR3_VERSION=3.27.0
# Thu, 14 May 2026 16:54:16 GMT
LABEL org.opencontainers.image.version=29.0
# Thu, 14 May 2026 16:54:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="149bb67708427ae50fce861d54ff676134e003438012efb41187d28122938564" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 16:54:16 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaf6e260eb9be8ddf4a89c9af584ece834cc59191d131824659459b34faacb9`  
		Last Modified: Thu, 14 May 2026 16:54:31 GMT  
		Size: 80.3 MB (80292274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6d61d673ab728366563da8fee4614031e1c3fee61e79b50ff29bb709ca11fba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a829ba930cde7b56300c569ccb826676cffaf3242c523150e690976ebe51c9`

```dockerfile
```

-	Layers:
	-	`sha256:9d05cc2ab3ab70325a075f4dcdbd0f1773d8efd86fd056727c590f2fa519843d`  
		Last Modified: Thu, 14 May 2026 16:54:28 GMT  
		Size: 3.3 MB (3283746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2878618709c13e872a4fa03b295ed9d750ab21adb2d53b9750498e50d166eb1`  
		Last Modified: Thu, 14 May 2026 16:54:28 GMT  
		Size: 13.9 KB (13922 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:30b4fbbc14b4fd7e4c64a508a830ee24dacbdcebc62579a50235bb110b9fe7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117901794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c2284536785bb6b38974c51921b7be31ff1a46e0e31690fd2a7d5a3a652307`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 16:54:03 GMT
ENV OTP_VERSION=29.0 REBAR3_VERSION=3.27.0
# Thu, 14 May 2026 16:54:03 GMT
LABEL org.opencontainers.image.version=29.0
# Thu, 14 May 2026 16:54:03 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="149bb67708427ae50fce861d54ff676134e003438012efb41187d28122938564" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 16:54:03 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ab1ea4901b2e5ef4c23bc85e77bccd29b5e37409a6599c547024038487caa48a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 47.5 MB (47466292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8bacb1e1edbafd39e5b9d621e2d8df4b1e5038153de928e5048948ac62e376`  
		Last Modified: Thu, 14 May 2026 16:54:18 GMT  
		Size: 70.4 MB (70435502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6081aee2d166d82052604d77d137f8490219683d0c8d5482c9318756b63bc29d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29bae2b86f48fcfb52656616fc54b40e3a6de2f327021a708d8ec390bc75420`

```dockerfile
```

-	Layers:
	-	`sha256:7da703468fe6103588d2d9533b3c1e19c59a74dd3e72e1cd64952de983d110b1`  
		Last Modified: Thu, 14 May 2026 16:54:16 GMT  
		Size: 3.3 MB (3286721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45c2be8ec745006b5646cf17270233321295ab9f87d0ba40b1b3662c59c108c7`  
		Last Modified: Thu, 14 May 2026 16:54:15 GMT  
		Size: 14.0 KB (14011 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:03fdaaf4986461f8f50375d8c58387d90cdacee83f7855f9199c457cdc3e6ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115757741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7774f30b9c2b25e7adf099e4f90c3fa8024c1b368bcdb5bfa382a21a2be5e181`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 16:54:45 GMT
ENV OTP_VERSION=29.0 REBAR3_VERSION=3.27.0
# Thu, 14 May 2026 16:54:45 GMT
LABEL org.opencontainers.image.version=29.0
# Thu, 14 May 2026 16:54:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="149bb67708427ae50fce861d54ff676134e003438012efb41187d28122938564" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 16:54:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:54e91da80876b5fdcd3d8cbdf1cebc52bdf513f8a587b419fa82f5fb473a2b30`  
		Last Modified: Fri, 08 May 2026 18:37:56 GMT  
		Size: 45.7 MB (45738425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97285a8ed87e3377d49ef4af5f71ede7a0dcf32010c12ac2de16ef9bf04d07ee`  
		Last Modified: Thu, 14 May 2026 16:55:00 GMT  
		Size: 70.0 MB (70019316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b810f690bed3f64c6935e9fd95e20e0189f24a14692c519b22aa2f3912c2b1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6967d1d049b7ff7c9f39b602b00f98b9607a3f75926d3855545ffdab22b523`

```dockerfile
```

-	Layers:
	-	`sha256:4356a97a96efa4c322f7b0f18e51a57714a61a0ae1b5cb9a888cd97b8cc2396c`  
		Last Modified: Thu, 14 May 2026 16:54:58 GMT  
		Size: 3.3 MB (3285170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf7b0a917fb567b436cd0ace1db93facc21cf866f9397b3435a1cbf4f548617`  
		Last Modified: Thu, 14 May 2026 16:54:57 GMT  
		Size: 14.0 KB (14011 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:cbb3d8e7ec20f0e484b00b86872679e6ea1598b69efade677d3dfe5c3e491071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128424767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf0ea8170e456d2bc67d65e1d815b0365854a9309a7ed0e76c17bb754511930`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 16:54:11 GMT
ENV OTP_VERSION=29.0 REBAR3_VERSION=3.27.0
# Thu, 14 May 2026 16:54:11 GMT
LABEL org.opencontainers.image.version=29.0
# Thu, 14 May 2026 16:54:11 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="149bb67708427ae50fce861d54ff676134e003438012efb41187d28122938564" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 16:54:11 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cdaf17e6638321f3ec6c27593b21bea3f7d2e3f6c2a11ed76072fa4e5dbcc2`  
		Last Modified: Thu, 14 May 2026 16:54:26 GMT  
		Size: 78.8 MB (78755322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:8b719b39644110f01deb54ed537dea4d58d575b1e684ac340b8051d3a1c372f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3b51a1842362a8429df0e0ed74e158408c6f5e7e5bc7b45eaa6bb77d369d50`

```dockerfile
```

-	Layers:
	-	`sha256:d1816c7276cf5d86b99e4cf40f70dfcb75dfd38bcbb27f94e76b598597955123`  
		Last Modified: Thu, 14 May 2026 16:54:24 GMT  
		Size: 3.3 MB (3285281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c03464cfbf4b74668e462e79b941223acaa7d6fe6026b31a9fd9a04147acbc01`  
		Last Modified: Thu, 14 May 2026 16:54:24 GMT  
		Size: 14.0 KB (14039 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; 386

```console
$ docker pull erlang@sha256:cba974cef4d5142ed9c056537daf2e524ba4725b6396c58b2508cdba4119e4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121245218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b8b361e0d1802c617edf3e22c477ac09d3814edba337ba0966f50b3593b298`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 16:54:32 GMT
ENV OTP_VERSION=29.0 REBAR3_VERSION=3.27.0
# Thu, 14 May 2026 16:54:32 GMT
LABEL org.opencontainers.image.version=29.0
# Thu, 14 May 2026 16:54:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="149bb67708427ae50fce861d54ff676134e003438012efb41187d28122938564" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 16:54:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44aa18d5fb926f19c94b5e447311e61f15b95a5464db45eee9881c112e8eb5ed`  
		Last Modified: Thu, 14 May 2026 16:54:47 GMT  
		Size: 70.4 MB (70419637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ed513dc6ae65af1c7a20db100a8ef2b89a5471c395f185e4769b3129566bd8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7699bd0ced095d73b9c24240666fe6461c2808025cd9742cf70b415c91a762ab`

```dockerfile
```

-	Layers:
	-	`sha256:031c10e0f7a6262251d1b87923a3626d905cf2de1f1fc32b6e3aeebf25194444`  
		Last Modified: Thu, 14 May 2026 16:54:44 GMT  
		Size: 3.3 MB (3280916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9af5ffb8ff5fabc4677ebd92cdbd1de2a150ad788a297c85efe2d4fdc168a0`  
		Last Modified: Thu, 14 May 2026 16:54:44 GMT  
		Size: 13.9 KB (13885 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:613e970e8384b89ecbd0a53a18ad6b047c08e53dd9b136fec8a50a097449e6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124521792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3219d82fbd536cd9d45d8699ecb3d47ed9ce65339e33b9cbde0278796b6f0d87`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 16:53:34 GMT
ENV OTP_VERSION=29.0 REBAR3_VERSION=3.27.0
# Thu, 14 May 2026 16:53:34 GMT
LABEL org.opencontainers.image.version=29.0
# Thu, 14 May 2026 16:53:34 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="149bb67708427ae50fce861d54ff676134e003438012efb41187d28122938564" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 16:53:34 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4bfde762ecfe2e6f5121f5a42767ca8adff7e2b2aeb0e6f21586e6795ce8b8`  
		Last Modified: Thu, 14 May 2026 16:54:03 GMT  
		Size: 71.4 MB (71398627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ca7e9610db7f030e3c624db84f394f167ff2a149f015d2b8950abba126366235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5016935c98b8ef82701eede3a383651b021894cf9b0359c135478ab592cb705a`

```dockerfile
```

-	Layers:
	-	`sha256:a5684914e8f0e64c17992c92686e924409497cda2c6409e2ac30df46a5ba3f42`  
		Last Modified: Thu, 14 May 2026 16:54:01 GMT  
		Size: 3.3 MB (3287337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe046d361cf7b4a6bb3d3f4ed1a38fab42cb081b393be45c6a1ea0fb8620d98a`  
		Last Modified: Thu, 14 May 2026 16:54:01 GMT  
		Size: 14.0 KB (13973 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; s390x

```console
$ docker pull erlang@sha256:916ab28f873c768b2628d44f4f53d4babaf7d4c5876ac65022b4f9604a398571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120648239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60056e5a9c0ff683daae35ffe1b4dbbef39603b6687d74eecc8defe667036c59`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 16:53:23 GMT
ENV OTP_VERSION=29.0 REBAR3_VERSION=3.27.0
# Thu, 14 May 2026 16:53:23 GMT
LABEL org.opencontainers.image.version=29.0
# Thu, 14 May 2026 16:53:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="149bb67708427ae50fce861d54ff676134e003438012efb41187d28122938564" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 16:53:23 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a59b6b4cfbd07c15b21af045b9e811b9c8592a2919c74aad7e8b85ba4a896c`  
		Last Modified: Thu, 14 May 2026 16:53:43 GMT  
		Size: 71.3 MB (71275935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:efd13f095e79cdb28ed2b502cf5d839dab5527aff97d35715dba38c6f5544f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f892972d6b8521e93985cad179f1db253b4fbb77e0bc93aa871a742d3d0542`

```dockerfile
```

-	Layers:
	-	`sha256:3ffab01d9316f039fe7c41b0fae1dd3a99eab4e54eec5264dd7d2473167ba2ca`  
		Last Modified: Thu, 14 May 2026 16:53:41 GMT  
		Size: 3.3 MB (3285187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29023ad04679cdd374ed31d333a59082e937ec30c9fe34645b66044918c936d0`  
		Last Modified: Thu, 14 May 2026 16:53:41 GMT  
		Size: 13.9 KB (13923 bytes)  
		MIME: application/vnd.in-toto+json
