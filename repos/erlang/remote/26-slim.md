## `erlang:26-slim`

```console
$ docker pull erlang@sha256:ce02c345cbd363d2c6f1bb2cd55c0c4686660a95d5e03af978d768266285626c
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

### `erlang:26-slim` - linux; amd64

```console
$ docker pull erlang@sha256:a849ed5aab3c429178242d9fd8ef7e9cf3fb46a48c94fc1e3b5f3af335daa2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118909943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea3b7f34175e1f29b8fb53424a3529cfdf5bca4d41f1ac8f7a897b1b10f6e7`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bae2dbcc9225f26a78c3d2bbee5e42a389ba633f92b2b8b38e609f61159739`  
		Last Modified: Tue, 21 Oct 2025 01:48:19 GMT  
		Size: 70.4 MB (70429380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:28bb1b5b03142be89b9890d6b7e1860c06d291233d68213b7d2157d7f124a079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a0a2d8de4942a84e32a078dad5db72a724e29a89ba866a8930e44bf4192edf`

```dockerfile
```

-	Layers:
	-	`sha256:dc0ec48c4c0ed5d94cc90288104cb0ffdf1e294b056443ea58d88a425a559544`  
		Last Modified: Tue, 21 Oct 2025 10:48:02 GMT  
		Size: 3.8 MB (3825336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d18e7019bb689d436858095f2723d3f9d50fba8ea9c97a96f2e5d997eb9d729b`  
		Last Modified: Tue, 21 Oct 2025 10:48:03 GMT  
		Size: 13.6 KB (13605 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:1961a4ff54e8f1b617c6de899f6015a7d1af200c3ae227c85c1eb5f17f693800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106556557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a60e983f6045afb461908663d63922524ee1e587dcb89b53cd608c37ab216a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:32:51 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 01:32:51 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 01:32:51 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:51 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d0780482d9b97d506bfd55bf3b805f2de1b9731c75e1b5800b5d53bb5388e1d8`  
		Last Modified: Tue, 04 Nov 2025 00:12:37 GMT  
		Size: 46.0 MB (46016089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1031d5329a25cce710451804e2478dc695fa21334f3c026a7ce2aacdebcc51`  
		Last Modified: Tue, 04 Nov 2025 01:33:15 GMT  
		Size: 60.5 MB (60540468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:71a19e31e1daa2a56b7164ed6c8e05dbf5c61214836fa0781fbf3bfc561bb823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a1a3dddb026b2c8009c36bafa07b668ac30af5e61281a42f66cb9f67cd42f5`

```dockerfile
```

-	Layers:
	-	`sha256:81bfbc0d180dc8ddf8fb209fe52faddfffb4b04f91cef43cbe019686124b2032`  
		Last Modified: Tue, 04 Nov 2025 08:46:51 GMT  
		Size: 3.8 MB (3829144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dd9d6ae76beb37e68ab09afb855a33445704ddaf61e5902ac870986e14335d7`  
		Last Modified: Tue, 04 Nov 2025 08:46:52 GMT  
		Size: 13.6 KB (13642 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:b9a7a6991ce5ffb4e24254b91f65ad338e9e158b5454b916a4f4d42e6c8f2fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104359022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac62835fc830083dace379a48e54b68b525437b8b53b76aa27c1ddbe83683eb`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd86a6bfa69ccb68a83307ba02100742b57a75533ee773bee3a606fa40ab4fd`  
		Last Modified: Tue, 21 Oct 2025 02:56:22 GMT  
		Size: 60.2 MB (60163112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:da247efd131f9c7e691abf4d0da646ac8c56eedab7d3df2eb7852f51db6a8b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3841254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2260743395c579c3c15e033d00d4d66dc7a1ccda7d6cab836f5145454880dbdd`

```dockerfile
```

-	Layers:
	-	`sha256:efd4d5439e123fe10651b9eb2fcd1fa7b6c10f93763dac089e21772fed420b88`  
		Last Modified: Tue, 21 Oct 2025 07:47:13 GMT  
		Size: 3.8 MB (3827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b16577203c523b1fe543bc5a3c45156f56d5c80152aa4bb04003738278469c6`  
		Last Modified: Tue, 21 Oct 2025 07:47:13 GMT  
		Size: 13.7 KB (13685 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:37442512a854bf2c0197d8e9e1e79a5df7bc18e5bb6af5d2b87b6d85d07020fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116430521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:397cf52e60ed1a37a432d4d95ad90f0b391d4a6cceb3f3df4da7230333378aef`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7861654472c0fe73ea88cb0d563a2b1dab8246de215cce22016b676ff8f4d3ba`  
		Last Modified: Tue, 21 Oct 2025 01:52:26 GMT  
		Size: 68.1 MB (68071525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:5eb791e0ed44b3010d6f9214c274a9c65fdc5b3b57d424ba2f7634c53c1e4b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3839306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63acc148d55dfa3e203d7de128686850038d2b43d006c5e305e1c70383956cdd`

```dockerfile
```

-	Layers:
	-	`sha256:f3b0774168247dd27149c5dec0b2ac75ff6c7d59dc3813817d745b42a910c1a0`  
		Last Modified: Tue, 21 Oct 2025 09:52:27 GMT  
		Size: 3.8 MB (3825597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a79929292e732eb418bd388361a479dfcb67489f87be57f5aca3534e6cbd805`  
		Last Modified: Tue, 21 Oct 2025 09:52:27 GMT  
		Size: 13.7 KB (13709 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; 386

```console
$ docker pull erlang@sha256:41c7a7a8e106f317a3b4e371e076a6fee3eee4cdfaad94077ac85fe2bb1b8675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110622185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f3efe4e133b277bbd4d72df3792163b47cc2ae1b6c495ad85f902c33187eac`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3426ba65368da59a25d050cab9d7713d7873264014ab6dfaa6b0c33f0632cb80`  
		Last Modified: Tue, 21 Oct 2025 00:20:21 GMT  
		Size: 49.5 MB (49466720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b911b7cf1d7855fcf03fe575678dd6008f59a24f292352f9bf709eba7aa3a3`  
		Last Modified: Tue, 21 Oct 2025 01:57:45 GMT  
		Size: 61.2 MB (61155465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:3cd3af4d2c3b58bab6db19861a6508d0382824108b6ae3b6ea5d1f4152e399a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3836071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4342cb783603831b5d402fcfc5a6633268e80f5b014416344039daae2ab008`

```dockerfile
```

-	Layers:
	-	`sha256:acda4f753c141ae0b49c4103941961385b1704618c1225f527d48dc48877b36d`  
		Last Modified: Tue, 21 Oct 2025 10:48:15 GMT  
		Size: 3.8 MB (3822498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:745d69751489dcf09f33adae753959be5b54ac7ce8ed4b7f4b3de5934db73166`  
		Last Modified: Tue, 21 Oct 2025 10:48:16 GMT  
		Size: 13.6 KB (13573 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:cbb35272b1e5e08bddb115229055f6ad9257d49c1aafbb0486ce9a07d527b5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109896501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e853c9db5f525aa9d208dda8a95989d550812c32294404b67f9cb72beefdc063`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 13 Sep 2025 01:06:53 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Sat, 13 Sep 2025 01:06:53 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Sat, 13 Sep 2025 01:06:53 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Sat, 13 Sep 2025 01:06:53 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 13 Sep 2025 01:06:53 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:4ff7a7a0be4afa0c088333063434d872e5a67b49bc2165e0d5f1c8b45e31c387`  
		Last Modified: Tue, 21 Oct 2025 00:19:28 GMT  
		Size: 48.8 MB (48760743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a69c4691215261f1844195ed8e45bd0112300e5934dc8abfdd8eb5f461ce6cc`  
		Last Modified: Tue, 21 Oct 2025 18:20:36 GMT  
		Size: 61.1 MB (61135758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:fa0b0aae1d42e771a2ae4b4047830cfe10a293cdae50a9f0c105a9712790fbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de87e0712c9692325ade94910c283115576c082a1488bc806e690085481550c9`

```dockerfile
```

-	Layers:
	-	`sha256:ebbb8796a3b137c7d4bbe39b2f4a0419a032f9ee4159696e141dda8cafbb3fa1`  
		Last Modified: Tue, 21 Oct 2025 19:46:52 GMT  
		Size: 13.5 KB (13456 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:ebb938ad39ba1e2697bdf0df397196be633c422d683bb2ae9e969c816105686f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114578845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1e814993e0a05a0e05bfc4f4e019fb532a0cf1f979492a440de749142a9ee`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:39:59 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 00:39:59 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 00:39:59 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:39:59 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afb768048b5899bc97639cb39d9c29e9e3751572e57337a265b88b0083dffa9`  
		Last Modified: Tue, 04 Nov 2025 00:40:55 GMT  
		Size: 62.3 MB (62251565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7e255a9daf4d326ab3ff4e5781a8a1d9df26da1472765668198506e6bbae3b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3843390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc130b0a1bbfc955d69025f15435b60a962f38ea9bc2b5b207db810361decc58`

```dockerfile
```

-	Layers:
	-	`sha256:aaad6f55ca9b817eb8fbe1db0e1bead6862aa4c06dbdf54fcf1d8353281d9efa`  
		Last Modified: Tue, 04 Nov 2025 08:47:19 GMT  
		Size: 3.8 MB (3829784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2fa29166ea9c6d131f419ad2acf2ab5eeb3fb565ccff2366ca3b9bd78bd301`  
		Last Modified: Tue, 04 Nov 2025 08:47:20 GMT  
		Size: 13.6 KB (13606 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; s390x

```console
$ docker pull erlang@sha256:9a311e5a4b337e32eb00d02869fe560a80d2eefef5abee61abe9ea784e403616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108098491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ee2eb6daec3b47a3a2e2c301ce6145952a23fc9ab42e5f860f7f7f3197d2ad`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:32:11 GMT
ENV OTP_VERSION=26.2.5.15 REBAR3_VERSION=3.25.0
# Tue, 04 Nov 2025 03:32:11 GMT
LABEL org.opencontainers.image.version=26.2.5.15
# Tue, 04 Nov 2025 03:32:11 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="aa38b8b50873722929791d985716d47769a59232241f617b91580248670c52f9" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 03:32:11 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e1dbfe59ae33319104649a00234b8446d2118b230747b863202aa24e3f31a1`  
		Last Modified: Tue, 04 Nov 2025 03:32:40 GMT  
		Size: 61.0 MB (60960398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4f3116fe38d4859e4b16cdd44914408044a3c55aa1d0c4de07ef0cf297e3cc1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c27924d2e2dd313927004bef3f9612291fc8d26a78163dfc6c8731ee03d489`

```dockerfile
```

-	Layers:
	-	`sha256:ad31a967156f51c76cc11897d038926f02ad6ca9f25032c94aed233e0504c9f2`  
		Last Modified: Tue, 04 Nov 2025 08:47:24 GMT  
		Size: 3.8 MB (3822164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:206b950691feeca0e15287ec9ff45f97bf1f77739bbfa53b655b64686af78de5`  
		Last Modified: Tue, 04 Nov 2025 08:47:25 GMT  
		Size: 13.6 KB (13562 bytes)  
		MIME: application/vnd.in-toto+json
