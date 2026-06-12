## `erlang:29-slim`

```console
$ docker pull erlang@sha256:f1d3b12f707d3b8d2a5592c6f460ee5fabda49b729c5780fb5e234d1344fa877
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
$ docker pull erlang@sha256:6aa8cb1aa9101903a3fb1acacd2a6346ff42a89a4b34654fae4b0d8ae121c436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129596375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c85dccd22248d2363ef7723120dbf9e0da3b5bb1ebd2fa93b309043fed481e`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:11:19 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:11:19 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:11:19 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:11:19 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16980830617a3a7d5f9c6a100dd7f8f33166a7278d8f2d819fa056f496e419a`  
		Last Modified: Thu, 11 Jun 2026 19:11:35 GMT  
		Size: 80.3 MB (80279254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c085f8973eb59b7a1f98aa9d754f3edb04f39a61e41df3a3378aaa32263fa2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a4bce9a5b1c7733ee594e35a97c050ccadd8e279686bd20a2e03ea6615d610`

```dockerfile
```

-	Layers:
	-	`sha256:f37ee26fbe97e7796eb9df1590ea5300a556378283cfcc8ddc106392aea7c45b`  
		Last Modified: Thu, 11 Jun 2026 19:11:32 GMT  
		Size: 3.3 MB (3283864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331957a22b9c346ad02f921703f6dc04006c561870689066c96cd6530c5b9c47`  
		Last Modified: Thu, 11 Jun 2026 19:11:32 GMT  
		Size: 13.9 KB (13929 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:f515c5c5f6dda68304e5b6dd19cc0ac0dfb1105cd553925072de62517f7c2587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117930933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda26df26b5c47d2333901176cc27c12db985313fc0d477815db5e112c3b37a8`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:12:07 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:12:07 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:12:07 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:12:07 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f4fdc449648c31ec97234c27647662108b2d6bce3fe83032a1af88265bf2ff35`  
		Last Modified: Wed, 10 Jun 2026 23:40:32 GMT  
		Size: 47.5 MB (47494811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8685ff31f4b89547b35b367f90ca2ddd2e7adb61312790e63317bebec889a5a`  
		Last Modified: Thu, 11 Jun 2026 19:12:21 GMT  
		Size: 70.4 MB (70436122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ab189acef90bb8cbb821ad6aaded6e4cef572feff417c2a31ba3c8052d0f8134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5919d7b557388462a159fe0502a34667c609f32a8ef839ee43dd50432f74f6d`

```dockerfile
```

-	Layers:
	-	`sha256:e2dc70c858155dd541e500b03e124af58b9db38d1fccbc037bc0d8b474fd1f4f`  
		Last Modified: Thu, 11 Jun 2026 19:12:20 GMT  
		Size: 3.3 MB (3286839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dec2ee55fb0a5efb3cf5d07769bf7368986939543f64880cbd348366c44506e`  
		Last Modified: Thu, 11 Jun 2026 19:12:19 GMT  
		Size: 14.0 KB (14017 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:be00e9c792648c3bda2932ebe050751fd36eeeeace34c84553c10be8c2104fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115763839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab26cd4e22cd46535f7f0230ee28a288c93c5376098dc2fbb016449cecb0e8d`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:11:30 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:11:30 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:11:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:11:30 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:df041f2d52cc5410fddc569f8ab35cdfdd35a38e037f7aab971e409724bfd203`  
		Last Modified: Wed, 10 Jun 2026 23:42:20 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2018362f801edba824698b5f2648a3a189db020f84426a048942ee5b3385313`  
		Last Modified: Thu, 11 Jun 2026 19:11:45 GMT  
		Size: 70.0 MB (70015198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:3e1e78488b5297ea6d2be8b1876d46337785bd4a480ce1432f4e2948e92d4c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8997aa411c5f3fd1277e17f6ddd63df97b8cd3710b340598508ccfc01eff0ed6`

```dockerfile
```

-	Layers:
	-	`sha256:2017e7ad788b9931bb03e78b0568863d34555005b9fdce1880823b11a14e0568`  
		Last Modified: Thu, 11 Jun 2026 19:11:42 GMT  
		Size: 3.3 MB (3285288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3a58a3abbdff144a873589cac466bb55bce20534801ed232a1d2cc70434fed2`  
		Last Modified: Thu, 11 Jun 2026 19:11:42 GMT  
		Size: 14.0 KB (14016 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:aa91b89836381996645378285edaf51de6ac7914e74953ce9d12089769bac991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128428458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5577929a590350c7a0f967de13b3560167fd016b4b883f013f0ca3bedbb594`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:11:16 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:11:16 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:11:16 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:11:16 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5805b2e1ac43460a7157f342a003113a55b12cf9403058e744604fd612c9175f`  
		Last Modified: Thu, 11 Jun 2026 19:11:31 GMT  
		Size: 78.8 MB (78750289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:10a05ed61f516e77d414bf25c890989cefcae3eb8c313abc363f4318dbb511a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3298807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c111c9957ac4a2c48afe73311b5634eaf0132a787ab9235c2349e2d0ee547e8`

```dockerfile
```

-	Layers:
	-	`sha256:4a97f5fd1420c463775791dfdc4750fdbc28766083a86670e090c36f2f8ca225`  
		Last Modified: Thu, 11 Jun 2026 19:11:29 GMT  
		Size: 3.3 MB (3284762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43736aea5c8ce97b54f3858160458ec8d2bbf7de5899af4d76f01041e577fae9`  
		Last Modified: Thu, 11 Jun 2026 19:11:29 GMT  
		Size: 14.0 KB (14045 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; 386

```console
$ docker pull erlang@sha256:448fe66b1a56aa497fada59706e7984fb04f89a194659ef4bc1b5009db9978e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121256886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f36f937b6707784896f5e81feb486e0a5c740a43ece1bf192171f77a90556a`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:11:29 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:11:29 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:11:29 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:11:29 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72b7d40c6a7baae68b40b60d035cfcabf854955113d0833aea340674a975e7b`  
		Last Modified: Thu, 11 Jun 2026 19:11:43 GMT  
		Size: 70.4 MB (70421323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4e2b34f8c08f4dd4f122b4376a7ac1f52f921d3e0cf7f9c48a69b8c78a6a37d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecb2b4b3d029d9adc0d2c2bb815a308af27c28764748695e15a79cd4708cfba`

```dockerfile
```

-	Layers:
	-	`sha256:b90159a7158e8d6def716ece0fc53fa649ee83b281887626d22d341e0d97708a`  
		Last Modified: Thu, 11 Jun 2026 19:11:41 GMT  
		Size: 3.3 MB (3281034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307d6a589c72e5436229b77330398e6d66c0d04d98618234cb01ca1e027a5deb`  
		Last Modified: Thu, 11 Jun 2026 19:11:40 GMT  
		Size: 13.9 KB (13891 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:bc9c5fc4cfa0b8ff815d69fba64be5c72a3e67effaed064dd537d02326401f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124530638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad91831caea0243eab74c145bada6d41054eeeffa92cf3e7649dcebcdc665fe8`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 20:59:05 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 20:59:05 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 20:59:05 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 20:59:05 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a3dc5c0ec6a6387fce347d9f80e8f1f7c7ced0af1d02ffa21c4337cb6eb042`  
		Last Modified: Thu, 11 Jun 2026 20:59:31 GMT  
		Size: 71.4 MB (71392699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:49f8b03e5900c3101dbf0d6eaff75bc15be98d3c0e9466155eac3cd1cd5909b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd888687adee9d6b3e5b3f832c94e7aa638b82f5675da9296dd8c698db84573`

```dockerfile
```

-	Layers:
	-	`sha256:3b3e0305a957b77a0eb1cd03ffe3c50018e08dff529b674c8feb2db8e65de730`  
		Last Modified: Thu, 11 Jun 2026 20:59:29 GMT  
		Size: 3.3 MB (3287455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0052392ebc9c9ec60a6f35f1bebf083562dc0b5620b92d41737dc32f01ed4b90`  
		Last Modified: Thu, 11 Jun 2026 20:59:29 GMT  
		Size: 14.0 KB (13978 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; s390x

```console
$ docker pull erlang@sha256:090f059deda33cfd74485fab41db8816f15fdeacd2383f802e1259faea4301c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120656030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2d8f12e27e015d5d3c29cbd92dac7e065878acfb16fcbc1a5ef2a0161abee8`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 19:12:45 GMT
ENV OTP_VERSION=29.0.2 REBAR3_VERSION=3.27.0
# Thu, 11 Jun 2026 19:12:45 GMT
LABEL org.opencontainers.image.version=29.0.2
# Thu, 11 Jun 2026 19:12:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="b9a7714fdd282c4a7113651b1e2728a58799e60ffe20e545f5cc94c621527b15" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 19:12:45 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265009f51f3f73a7540ca4d2367a2844450f2e4b56e9d84aab8ba1710d156a3d`  
		Last Modified: Thu, 11 Jun 2026 19:13:04 GMT  
		Size: 71.3 MB (71270133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:8f252ef1f659baf4c8375ae59c968918c8d345f18ab8d37b1447b4fb56480f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8f6ec5a233dffe1af15e44d13d7f9fa189560fbb19f1e77f6e7c96f92fcc1d`

```dockerfile
```

-	Layers:
	-	`sha256:f6931c228fc3b8e2f70b97f043453cc353c5af916e361b60c24410259471b7c7`  
		Last Modified: Thu, 11 Jun 2026 19:13:02 GMT  
		Size: 3.3 MB (3285305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b5bf7438099cb6c143be7834a6a3bd0ef7000f91f00efca59d52b4fcbd145d`  
		Last Modified: Thu, 11 Jun 2026 19:13:02 GMT  
		Size: 13.9 KB (13929 bytes)  
		MIME: application/vnd.in-toto+json
