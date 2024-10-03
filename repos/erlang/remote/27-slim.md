## `erlang:27-slim`

```console
$ docker pull erlang@sha256:d6ee685fb365f373ac449ad268b25564fded3d4dbae6bc6eb3b5d69edf9f79d2
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
$ docker pull erlang@sha256:ff0957a90df7a181244f92523bee4588440e8c48d00b6b8cf2da28be9f1f65d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125393697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf12abe919c840293b8e192d3a6cb83a997b1d87a5879a21a3b1b2beeee32be`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 20:37:26 GMT
ENV OTP_VERSION=27.1.1 REBAR3_VERSION=3.23.0
# Wed, 02 Oct 2024 20:37:26 GMT
LABEL org.opencontainers.image.version=27.1.1
# Wed, 02 Oct 2024 20:37:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="315552992ebbc86f27b54b4267616ad49b10fa2ef6bc4ec2a6992f7054c9157e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 02 Oct 2024 20:37:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76770afe8feca4328c23c58a19040fbd569b1de76da5d1878f9aaa664b6c08b8`  
		Last Modified: Thu, 03 Oct 2024 01:05:22 GMT  
		Size: 75.8 MB (75838646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:211ef2737b08fa8c815d11d51faa83666e0d0a9e6dece6747294933c4c1609de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7dcf5ff9ec167b7fb572d501f4a6a7a917e83a6c5071d7ee389df5d375ec35`

```dockerfile
```

-	Layers:
	-	`sha256:e82a72a1643ec305057c205fb93ecd7168b36884348035cbf44855b8159e22b1`  
		Last Modified: Thu, 03 Oct 2024 01:05:21 GMT  
		Size: 3.7 MB (3696792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef578674273d579cdb9ce1413ead86495a61aeb120a5fc898e9559b232ada280`  
		Last Modified: Thu, 03 Oct 2024 01:05:21 GMT  
		Size: 13.7 KB (13662 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:e3460cea9a3c842a68c31aae988e483457a2f7d2f35dd19a8405ae6f971fd449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112692690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0031e7cbfb5ab82e907f473b9bd2a2c8a26da6c0960c040c593ca9eb5a8e04`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:10 GMT
ADD file:36a0f7a5e52e53b077089591b55dc92129f570865422246d0966d3c18c3f513c in / 
# Fri, 27 Sep 2024 03:19:11 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 20:37:26 GMT
ENV OTP_VERSION=27.1.1 REBAR3_VERSION=3.23.0
# Wed, 02 Oct 2024 20:37:26 GMT
LABEL org.opencontainers.image.version=27.1.1
# Wed, 02 Oct 2024 20:37:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="315552992ebbc86f27b54b4267616ad49b10fa2ef6bc4ec2a6992f7054c9157e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 02 Oct 2024 20:37:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d626bb1012b033dbfe95f5814e86f482c8f185c492cd6beab98600b43d8e3c08`  
		Last Modified: Fri, 27 Sep 2024 03:21:23 GMT  
		Size: 47.3 MB (47330755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474363430e2618eb0cd7fde20e216ac7a3bc8eff4dcbed126199a772ab3e202f`  
		Last Modified: Thu, 03 Oct 2024 01:14:02 GMT  
		Size: 65.4 MB (65361935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:5e5a2ada06d59fbea4aa6df575f8914f55fc86139a20355152bf0e4012b37491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23eba90e2f0792097d36ae97fe0282f707c23ac54a572bd00cde2de64c4ce417`

```dockerfile
```

-	Layers:
	-	`sha256:823570f16db6dbad776a07f41fb434cd0f4ebd850eec06ba647eff00df22113a`  
		Last Modified: Thu, 03 Oct 2024 01:14:00 GMT  
		Size: 3.7 MB (3700193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9093449cbcf3d8d8b805785ecd5ecb0c2d6a33664b951ef26a47d42aee2683ff`  
		Last Modified: Thu, 03 Oct 2024 01:14:00 GMT  
		Size: 13.7 KB (13740 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:294b029e33683032f692f6b4511e3d006375243b5b9a072f3bc8595e177a1d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110124334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5efac4ec481de6926bffd5f3450dd4ba71ba1815b6910a75a8426547f5278d44`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:34 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Fri, 27 Sep 2024 05:13:34 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 20:37:26 GMT
ENV OTP_VERSION=27.1.1 REBAR3_VERSION=3.23.0
# Wed, 02 Oct 2024 20:37:26 GMT
LABEL org.opencontainers.image.version=27.1.1
# Wed, 02 Oct 2024 20:37:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="315552992ebbc86f27b54b4267616ad49b10fa2ef6bc4ec2a6992f7054c9157e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 02 Oct 2024 20:37:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45f03d914d56e58c85c91da75b603bd60a740d4dc34b283e547b7751943a502`  
		Last Modified: Thu, 03 Oct 2024 01:12:41 GMT  
		Size: 65.0 MB (64976421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:eb9d32cffbfe2cf823b3bd7c17a85e59294061600e1eee7e5b27eb3429c26fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3712772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1ebf4a64332a320d3bbac3350f6cafb573a904d20fe7c6fbd8a8f1498d813e`

```dockerfile
```

-	Layers:
	-	`sha256:5f84549f4ecf64244b1d10dd82a6e096737ec09d24d695806289aab130a6332c`  
		Last Modified: Thu, 03 Oct 2024 01:12:39 GMT  
		Size: 3.7 MB (3699032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d14c9f2daf71d4512d30a84c49f79559292573230ca26dab5b383ac68dc1983`  
		Last Modified: Thu, 03 Oct 2024 01:12:38 GMT  
		Size: 13.7 KB (13740 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:cb25a8c54af6c246b091b788ae4d93a528a393da90dc92c5c35b3c9b54815b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123166825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cfc18b909e6576d98897094b70469f3461c03c0801aa403d2f7023f8be3379`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:09 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 27 Sep 2024 04:38:10 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 20:37:26 GMT
ENV OTP_VERSION=27.1.1 REBAR3_VERSION=3.23.0
# Wed, 02 Oct 2024 20:37:26 GMT
LABEL org.opencontainers.image.version=27.1.1
# Wed, 02 Oct 2024 20:37:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="315552992ebbc86f27b54b4267616ad49b10fa2ef6bc4ec2a6992f7054c9157e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 02 Oct 2024 20:37:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e4e5a7a6f3889ad8dd49344d1ddc8d3fd4dfa0ade15bd3b17118ffa7a40560`  
		Last Modified: Thu, 03 Oct 2024 01:07:56 GMT  
		Size: 73.6 MB (73581939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:de5d14cb57da269f3970885da51c1240af88de0bd8b2aacac275b92958e3f64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926527feff78b39faa6ee7b5e425a49ded8c6a89bc78ede0ba2be9237d5d1c5f`

```dockerfile
```

-	Layers:
	-	`sha256:d8f5971ec78e2b5884d6805e980834cb7c633cefb115bc9d2608969e62de8e25`  
		Last Modified: Thu, 03 Oct 2024 01:07:54 GMT  
		Size: 3.7 MB (3697064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361f56ed93df10cfb787d35fbb918993e5324ebdbcdac59d9ec07aec04987aa3`  
		Last Modified: Thu, 03 Oct 2024 01:07:54 GMT  
		Size: 13.8 KB (13771 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:4afc6729afe67ebdd62289eea7dac1f3687cc76d7084a528b0aa3402b65c82e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116577654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cecdb78c3fe3ae833fbf5f570f63c1866186b9f09da587d655ae818f5e24d89`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 27 Sep 2024 07:22:48 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 27 Sep 2024 07:22:49 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 20:37:26 GMT
ENV OTP_VERSION=27.1.1 REBAR3_VERSION=3.23.0
# Wed, 02 Oct 2024 20:37:26 GMT
LABEL org.opencontainers.image.version=27.1.1
# Wed, 02 Oct 2024 20:37:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="315552992ebbc86f27b54b4267616ad49b10fa2ef6bc4ec2a6992f7054c9157e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 02 Oct 2024 20:37:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcd6ed1b9112e68dcba26ae3db803ad1b23bcb4d5bfe589ed1e2490e2b308e7`  
		Last Modified: Thu, 03 Oct 2024 01:05:36 GMT  
		Size: 66.0 MB (66001013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:3880fc4b6f34b7e0a62af444fb7af0bb8b0ff70fa29052907d30c5e9d0c873ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fd7e8c88e7ff7b238fcbc5b994761909b4f344523517743c00603848530f0e`

```dockerfile
```

-	Layers:
	-	`sha256:315a2a9b02215125b397d16ed00b7c9bb38f7bcb4fd61d02d45f60fb1ce4816c`  
		Last Modified: Thu, 03 Oct 2024 01:05:34 GMT  
		Size: 3.7 MB (3693906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6d94ce9a97091f3ad533c4a7e070916846ae7356f53bbec68d187f6df6e938`  
		Last Modified: Thu, 03 Oct 2024 01:05:33 GMT  
		Size: 13.6 KB (13627 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:ee62f2dd7a67f963745594a835d1bce7bed795ad44b2c9d1d248b9a09cb7af14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115488175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9509f2b80d08a539472fc55d8d06185bf5eea54357f6b1520e7fcc5d8ce94e`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 27 Sep 2024 09:02:13 GMT
ADD file:6f3430cc82064e0f2b15b01e40de05ae0823abf169e966aa55cc0c0ca4257c22 in / 
# Fri, 27 Sep 2024 09:02:19 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 20:37:26 GMT
ENV OTP_VERSION=27.1.1 REBAR3_VERSION=3.23.0
# Wed, 02 Oct 2024 20:37:26 GMT
LABEL org.opencontainers.image.version=27.1.1
# Wed, 02 Oct 2024 20:37:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="315552992ebbc86f27b54b4267616ad49b10fa2ef6bc4ec2a6992f7054c9157e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 02 Oct 2024 20:37:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8e971619a39dae5a1330b75e3fc755af3e819283336ace59f4eb8cd8574c0ed6`  
		Last Modified: Fri, 27 Sep 2024 09:10:53 GMT  
		Size: 49.6 MB (49561615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f0a45a9a72f603c252a97f14a03de5fb4e02032d8c9fbaa065ec44c049582`  
		Last Modified: Thu, 03 Oct 2024 02:00:09 GMT  
		Size: 65.9 MB (65926560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:91659c0782081dcc87b37c39aabd89f078a2f1ba83bf04fb5c8d1b12cc233cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ba1292a69b3ddcd93e8741d9a8150362957fcb1be33d94d689ac40933e0203`

```dockerfile
```

-	Layers:
	-	`sha256:b436a84673073f2a9a535af3ca34dd7468c0a2dca96c0b04842d782105f3d9cc`  
		Last Modified: Thu, 03 Oct 2024 02:00:03 GMT  
		Size: 13.5 KB (13509 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:1e4c154b9c91b81e4f64644a2583006edc4ed8635f395535dcae69cab5434185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120649363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b6040dad36e4174281b7c77fd6b1536853a9f8b6506a0a1c80c0efd861b29c`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 27 Sep 2024 05:32:50 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Fri, 27 Sep 2024 05:32:53 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 20:37:26 GMT
ENV OTP_VERSION=27.1.1 REBAR3_VERSION=3.23.0
# Wed, 02 Oct 2024 20:37:26 GMT
LABEL org.opencontainers.image.version=27.1.1
# Wed, 02 Oct 2024 20:37:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="315552992ebbc86f27b54b4267616ad49b10fa2ef6bc4ec2a6992f7054c9157e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 02 Oct 2024 20:37:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b5e5b039c042fa5a4b7ef3c15aed74569ba3b1392c6430eea49a1e4ab311fe`  
		Last Modified: Thu, 03 Oct 2024 01:14:04 GMT  
		Size: 67.1 MB (67094206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:181c4417fc7d44c035b169b63524629ce161df848a9a9075c521a020196a4f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60637b64f9df936813576eca852493244ea7268109936c020baed92263e1f7b3`

```dockerfile
```

-	Layers:
	-	`sha256:5b3809c62399bf3ac142a7bb923d4317211d2d314909df3faf5d9a5aca8d73e2`  
		Last Modified: Thu, 03 Oct 2024 01:14:03 GMT  
		Size: 3.7 MB (3701137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88f15b0d695e6fdd01f20f213a86f2d4976eb8ee62c5660bd8b225f135c1d426`  
		Last Modified: Thu, 03 Oct 2024 01:14:02 GMT  
		Size: 13.7 KB (13706 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; s390x

```console
$ docker pull erlang@sha256:e15eb9ab16fda5e1c368bc333e38acdf7b2371fd27aea9a22d31189e4569223a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.7 MB (113697291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f684f6b778c7de0fdee731abb6b270b0b2cab32561a71c80ab3aac88277ffbc`
-	Default Command: `["erl"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:05 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Fri, 27 Sep 2024 02:43:07 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 20:37:26 GMT
ENV OTP_VERSION=27.1.1 REBAR3_VERSION=3.23.0
# Wed, 02 Oct 2024 20:37:26 GMT
LABEL org.opencontainers.image.version=27.1.1
# Wed, 02 Oct 2024 20:37:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="315552992ebbc86f27b54b4267616ad49b10fa2ef6bc4ec2a6992f7054c9157e" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Wed, 02 Oct 2024 20:37:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3c2463fd2cb48ca91a0537162a7ef11d33dc91bc3a04cfea8686466fb7a561`  
		Last Modified: Thu, 03 Oct 2024 01:19:37 GMT  
		Size: 65.8 MB (65758621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7827f9114a10bab42bd5633d065e0581d49702f8e1a51079982169a32b51a35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d604facfbde682f0a5f2b103ce619a3f550ad47dd35c378ebb42ea32038a8a6`

```dockerfile
```

-	Layers:
	-	`sha256:8d2d9fe938865cc3312ed933967e90fc9b3fecbd499329fe5ee59962370434e7`  
		Last Modified: Thu, 03 Oct 2024 01:19:36 GMT  
		Size: 3.7 MB (3696619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ff04ac617745e5a0894949b1b8d79fc8c5e31418df589abeeae7ad36628550`  
		Last Modified: Thu, 03 Oct 2024 01:19:35 GMT  
		Size: 13.7 KB (13662 bytes)  
		MIME: application/vnd.in-toto+json
