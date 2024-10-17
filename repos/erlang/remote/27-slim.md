## `erlang:27-slim`

```console
$ docker pull erlang@sha256:52ce01e44d3b46831e8d52acfd160108174eb6533b67fefe07ead4fd4fe1ddee
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
$ docker pull erlang@sha256:1bf51672793d6aff1ef89cc8c8f656fe9d64b1419b1742a28f2575ae3f3bcfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125392801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cb7fe2cd347f7c64466944f8eb3012c94e183e1031743b1461eaa7403da0ff`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 02 Oct 2024 20:37:26 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 02 Oct 2024 20:37:26 GMT
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
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b795d563ca3a44eafd89becaab0d44b3053de5491d7eebd660bbeebf887c4440`  
		Last Modified: Thu, 17 Oct 2024 01:23:51 GMT  
		Size: 75.8 MB (75837778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:66bbac9c17425002e2bac49f86c00e223396b8b64c228b7957fc9998030cff63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eeeb8dcf946ce73b2ba6ab187a420437242d8a876c19ac875f3c4a46ef9f30`

```dockerfile
```

-	Layers:
	-	`sha256:55052f911ecf5c5d7b16d94c0cceb541683ca074572624d6867b084b8c75e9e8`  
		Last Modified: Thu, 17 Oct 2024 01:23:50 GMT  
		Size: 3.7 MB (3696792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e00204c35f2199dbddde95e97fd9a0e235d89e3ecf781e5755791ae9ec908a0`  
		Last Modified: Thu, 17 Oct 2024 01:23:50 GMT  
		Size: 13.7 KB (13695 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:702f154caa6669d3e3b6671263c37ee017317252bebc844de51168112c0ee9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112691973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34af5c4110b58f0de6aea95214a80a54dd31b29071405102ad90e58a2bae5d1`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 02 Oct 2024 20:37:26 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Wed, 02 Oct 2024 20:37:26 GMT
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
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f1cfbd35cf276d6218d5b31f61c4e4488969223b7486935daf6ec20aa7393c`  
		Last Modified: Thu, 17 Oct 2024 01:24:10 GMT  
		Size: 65.4 MB (65361452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a656d051103ec7dc54840cb83cd9eb86ee1fe4e4e88ca69ff7fda4baff279ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad73e28c75b4d0e8e983dd619e9e4c9c42b03a0011a1b987bd3ec504b485cf88`

```dockerfile
```

-	Layers:
	-	`sha256:ab7b5b8a110e7bbbdface7a8aafe9762cbf372632710b388fc8b43d0cd72c9d3`  
		Last Modified: Thu, 17 Oct 2024 01:24:08 GMT  
		Size: 3.7 MB (3700193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6cdb6d1fd8a1e60e7de1779d580c73f92a8dbea6326d01e718670a07ecc4e65`  
		Last Modified: Thu, 17 Oct 2024 01:24:07 GMT  
		Size: 13.8 KB (13773 bytes)  
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
$ docker pull erlang@sha256:a425fdca12a98280cf39891c18a23c41059082dcc0deb78c750c0ab6aa40712b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116577299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b83570759b426092bfe3ad57d75118ba502b50c335a0299c3625c557f63349`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 02 Oct 2024 20:37:26 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Wed, 02 Oct 2024 20:37:26 GMT
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
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e81da9c6a015e46f9a2b4a9b884c36df34ec6202a2cfe0126cce99cc81502e3`  
		Last Modified: Thu, 17 Oct 2024 01:23:57 GMT  
		Size: 66.0 MB (66000465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:05692cc51676a124c5498726da423776c49275dd7a137c797a072d278d10a7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3707567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e22a8e355fee9b4d96680831d3a950d2389ff64727d3395739894fee46b51b1`

```dockerfile
```

-	Layers:
	-	`sha256:e0f6229d8723df5728c4b1ac281242573688f5444b1dae840b7d36b2f6ca1c10`  
		Last Modified: Thu, 17 Oct 2024 01:23:56 GMT  
		Size: 3.7 MB (3693906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c7f3e32382461ddc6dbd2c66f87781f655feafd3e9e06c93c396f0a33bd1d22`  
		Last Modified: Thu, 17 Oct 2024 01:23:56 GMT  
		Size: 13.7 KB (13661 bytes)  
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
