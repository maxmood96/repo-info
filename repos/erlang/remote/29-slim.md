## `erlang:29-slim`

```console
$ docker pull erlang@sha256:f81db9600dcd4bc4d55d7d9790125532f3dbfce3c2fff2ad552a09d314f61fa2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
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
$ docker pull erlang@sha256:84afd0c2756128300e280ad9b8199afd438e12baba38e770ee17d531880070f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129580408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccff7c1f73e4ab1452dab746ef40caff8a0a3a1b81181a76336ab652e670f321`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:23:49 GMT
ENV OTP_VERSION=29.0-rc1 REBAR3_VERSION=3.26.0
# Tue, 24 Feb 2026 19:23:49 GMT
LABEL org.opencontainers.image.version=29.0-rc1
# Tue, 24 Feb 2026 19:23:49 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ea98c87f975c12ffeb4fcb75d2b618cefea77ca02d3c2fca31a47e6d3d4db951" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:23:49 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189352a1e0038cbad76a116331a8aae9e46ac13f06f7e9c92bf958a6dfe09646`  
		Last Modified: Tue, 24 Feb 2026 19:24:04 GMT  
		Size: 80.3 MB (80287284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:bd05ab0b22e00525bf118cf76a6cca9fafac8cccdfda744a60b237c9e5eeddaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a34fe337aff1f5230b7b0f0c1d9f3bbbb5c3906c4098b174f630f72697aa6d`

```dockerfile
```

-	Layers:
	-	`sha256:9582fc7e31ab533bc0b4a7be2da3255cdf835fd1f3b8e508f310b4ae44fe2a95`  
		Last Modified: Tue, 24 Feb 2026 19:24:02 GMT  
		Size: 3.3 MB (3283426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9556799bb3ade4336d8cf849f99b80a35f563f6c670ce655655bd2dea5eb8b`  
		Last Modified: Tue, 24 Feb 2026 19:24:02 GMT  
		Size: 14.2 KB (14187 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:522a3d216eb53a4410324fd951740d153522f071f83233f50b4caee3bd44a970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127908481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e657a2bc508087da6bff76c1ff8daa3716b7e003362825fcc570399a3dd4b5e`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:28:36 GMT
ENV OTP_VERSION=29.0-rc1 REBAR3_VERSION=3.26.0
# Tue, 24 Feb 2026 19:28:36 GMT
LABEL org.opencontainers.image.version=29.0-rc1
# Tue, 24 Feb 2026 19:28:36 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ea98c87f975c12ffeb4fcb75d2b618cefea77ca02d3c2fca31a47e6d3d4db951" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:28:36 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe74d2e6a9f1aea2f4b18a5df3b89f3e7de11619f65eb4d8120b8d3600f119d`  
		Last Modified: Tue, 24 Feb 2026 19:28:51 GMT  
		Size: 78.3 MB (78256313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b3ef23337338dccee4f4157895a14f3a152102ad77b54988befdc88723433614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3083428dc6af60026a62d3e88c95d5ff12cb5f702d5095b09558cae4599a7d`

```dockerfile
```

-	Layers:
	-	`sha256:3de147fad7168db48eb528165669a83ac0d10b849990f0c3d7b1b638e2136ad8`  
		Last Modified: Tue, 24 Feb 2026 19:28:49 GMT  
		Size: 3.3 MB (3284949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:648b2037028d044d767eca3952680927f643ebd53d987d390f5280428558a193`  
		Last Modified: Tue, 24 Feb 2026 19:28:48 GMT  
		Size: 14.3 KB (14290 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; 386

```console
$ docker pull erlang@sha256:5ab3f4f7b0f7d8cb77450ea4e5c2429710f131c11f037e01460ab704486b3659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120881299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb491987b4fa324486526b456967f73ad6d235dcfcc32a58c41fcfd4fa888e9f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:26:46 GMT
ENV OTP_VERSION=29.0-rc1 REBAR3_VERSION=3.26.0
# Tue, 24 Feb 2026 19:26:46 GMT
LABEL org.opencontainers.image.version=29.0-rc1
# Tue, 24 Feb 2026 19:26:46 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ea98c87f975c12ffeb4fcb75d2b618cefea77ca02d3c2fca31a47e6d3d4db951" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:46 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:cdaf5c618b8ff25cb29f813a6c008ca0cb7de6fe5f93f3ba4939cc9fc10fc6cc`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 50.8 MB (50805272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5600368760773bd41273061ed80aeeb928f43c44d84241a9c3a0bf8a1169b0`  
		Last Modified: Tue, 24 Feb 2026 19:26:59 GMT  
		Size: 70.1 MB (70076027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a440fdbe9065f3b893f2dde83a57240f7b7393f20a1f0efe86a1d872331caa86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300be085d290c046ab96d81d7cdc52a49e82785c12e19c28c3315cb01e085697`

```dockerfile
```

-	Layers:
	-	`sha256:536db3eee23645803b606f29b9277ac22596c8f875d44c443a3085698d839133`  
		Last Modified: Tue, 24 Feb 2026 19:26:57 GMT  
		Size: 3.3 MB (3280601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d0d29b6f2cd1fec81085920e08ee71e6a1b5eab6690c5a137ed4ebc160f9661`  
		Last Modified: Tue, 24 Feb 2026 19:26:57 GMT  
		Size: 14.2 KB (14155 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:9ab589cfac55fa264f48e1e0346c23d0b6cd18b331b8456a52b2b8145946a7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124167679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b0572995e721ee4fab4d5190cd6cf746db9ce94632dd6005b66a3efe443d5c`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 20 Feb 2026 19:01:01 GMT
ENV OTP_VERSION=29.0-rc1 REBAR3_VERSION=3.26.0
# Fri, 20 Feb 2026 19:01:01 GMT
LABEL org.opencontainers.image.version=29.0-rc1
# Fri, 20 Feb 2026 19:01:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ea98c87f975c12ffeb4fcb75d2b618cefea77ca02d3c2fca31a47e6d3d4db951" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Fri, 20 Feb 2026 19:01:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a0225743f416507cb3200c7539174a74497af0e1e5e1c12e383a37489b459b`  
		Last Modified: Fri, 20 Feb 2026 19:02:03 GMT  
		Size: 71.1 MB (71055564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d86682e12824d7cc775a35b481444a6607cdb6ef38057f85f48dc26627a00790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb90ed7d27a7428398e6e2d6162160e561fac6387cb311928550b0d97345c0ae`

```dockerfile
```

-	Layers:
	-	`sha256:5f8ad6df0b0a49b3754aff969731fcebbf9120659d625b362fc4383c463c1d30`  
		Last Modified: Fri, 20 Feb 2026 19:02:01 GMT  
		Size: 3.3 MB (3287011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f7459d800dcb6e2df156af2b9eb8eb5b2100242f737370fbb8bb9d0d7e0d1d9`  
		Last Modified: Fri, 20 Feb 2026 19:02:00 GMT  
		Size: 14.2 KB (14231 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; s390x

```console
$ docker pull erlang@sha256:7ea4f5428597391d6951a7b6c2ef326e6159a0e61d8930a0e00433e0f2b10dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120289841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84b476a02e02a733b8358bf68ca6dd840b34cc4aa342b9a33a73366f87c1a12`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:06:51 GMT
ENV OTP_VERSION=29.0-rc1 REBAR3_VERSION=3.26.0
# Tue, 24 Feb 2026 21:06:51 GMT
LABEL org.opencontainers.image.version=29.0-rc1
# Tue, 24 Feb 2026 21:06:51 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ea98c87f975c12ffeb4fcb75d2b618cefea77ca02d3c2fca31a47e6d3d4db951" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="a151dc4a07805490e9f217a099e597ac9774814875f55da2c66545c333fdff64" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& sed -i "s|warnings_as_errors|nowarn_deprecated_catch|g" rebar.config 	&& sed -i "s|{overrides, \[{|{overrides, [{override, [{erl_opts, [nowarn_deprecated_catch]}]},{|g" rebar.config 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:06:51 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71103f0491a680ec12b758b315e820531a3d95dd53a85a093d7d4d1b95a6aafc`  
		Last Modified: Tue, 24 Feb 2026 21:07:20 GMT  
		Size: 70.9 MB (70935307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:db05db2587160bb5c31f8a64b0363418f25eda7771934e9c0678cca4da512677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d36123ec4620673bdc17eed8e72aa270185c018d51beb47081a5c4bcea279c`

```dockerfile
```

-	Layers:
	-	`sha256:cee12cc632e30cbe1d502a5c814edd2976b4a40ec5757d38509bbb3e7643a74b`  
		Last Modified: Tue, 24 Feb 2026 21:07:19 GMT  
		Size: 3.3 MB (3284867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:025d9455854e942cfeee56c376266815ba3ae170af380af614d02c566a17f77a`  
		Last Modified: Tue, 24 Feb 2026 21:07:19 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json
