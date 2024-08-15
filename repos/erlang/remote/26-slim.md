## `erlang:26-slim`

```console
$ docker pull erlang@sha256:ed5ab769aa730eee0763dd5c4599d9a5d330b4f2a79b878412dd924909aabfbf
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
$ docker pull erlang@sha256:2a31d8faae5280960c846e23ed7d410c164e4dde60e7c00520c51a8dc66d1599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119870339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9448d8fb7b4af4609958d4a912c66238fd8713968df6ddd9a22000a0718b9fcd`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:09 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Tue, 13 Aug 2024 00:20:09 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d3022252fea3ccbd815390466214cb8221c85ebe8c2ed98c09b052e2ccb9fa`  
		Last Modified: Tue, 13 Aug 2024 20:09:13 GMT  
		Size: 70.3 MB (70316259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:8f4cbad3d24c939c725a56ad7b551d171a44e04d3a17c81a4a1fe389d735a4e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3711036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96aa21f19abff63d47c2c110716ffac7fce12b4a5b4c1e1fe5710a2a22afbe67`

```dockerfile
```

-	Layers:
	-	`sha256:56cca9a7800d356a8bf8a91fa018af3776be29b9887b231b6e12fdb9c47997f8`  
		Last Modified: Tue, 13 Aug 2024 20:09:12 GMT  
		Size: 3.7 MB (3697668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5529a1127079b8ad86020001ddd2ae582479438de45f7a175081651ef5243149`  
		Last Modified: Tue, 13 Aug 2024 20:09:11 GMT  
		Size: 13.4 KB (13368 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:15747dc6e86c8b23d5c631feea4217c4e758ca0e3aa15ab35d7e490d02903754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107737818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4506d44de6461ce1b3d4a44503d910b68ca3e3009f46397384449252a304ca09`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:20 GMT
ADD file:d0d1a7bef1e6f926632190db50e475c494faeae7f507fe25bbc44d83e4cacf61 in / 
# Tue, 13 Aug 2024 00:55:20 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7b23500f0d545573a069afd72bb54ddd68dc094fc52cede45c3d6d99ab4ce614`  
		Last Modified: Tue, 13 Aug 2024 00:58:03 GMT  
		Size: 47.3 MB (47320194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c2b1b800bfd0d9be164c6ffb75b8c931a609d6d275d7cbebc7539e17300720`  
		Last Modified: Tue, 13 Aug 2024 23:56:28 GMT  
		Size: 60.4 MB (60417624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:fafaccf3c78dcb5d07ac1ebae9fbe3cd0719544b82916d702a82d08055e70912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3714499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481c4483368ec1326b9a915cb9a09fc4b3f7d548a7d148ec7561e4d9100de9c4`

```dockerfile
```

-	Layers:
	-	`sha256:e01c3d6f938878f024beee0a0068dbcb30ec9890902d63f50c767e1bbb624147`  
		Last Modified: Tue, 13 Aug 2024 23:56:26 GMT  
		Size: 3.7 MB (3701061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0b743dd77d32a29ab94d043f0cbedd629af142fbeb220f220eaf6728a72915d`  
		Last Modified: Tue, 13 Aug 2024 23:56:26 GMT  
		Size: 13.4 KB (13438 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:9004d1fd4c7b186647e42a12c55137d436b000cc6ed7559b47145b49b5f7c907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105192609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0671b1f4ba16f25d290522c7b4dc0015a076b78eabf2cf1b2aba6b18af5df9`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:26 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Tue, 13 Aug 2024 00:57:26 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da4bafb4a3a63756c1e3faeca7bdad5cd7514aa305fc91abae788a0518b8ec4`  
		Last Modified: Wed, 14 Aug 2024 01:36:58 GMT  
		Size: 60.0 MB (60044449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6a510a744131a237b62cd1bc595ec9c0841eea7e565a940951a64903c8c06636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3713339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828ca0cbbbf7c585ffffd2fb42310e88dfe06fbddf69cbfed510febdbc77b02e`

```dockerfile
```

-	Layers:
	-	`sha256:606ba8525164d2c75ab792c2ea61465116e135cce64748348da26344d57024df`  
		Last Modified: Wed, 14 Aug 2024 01:36:56 GMT  
		Size: 3.7 MB (3699900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee4fd5d63ccfda6cd7060033a7e6a5c6f8da44bf59e55e2365c150c41c39d4a5`  
		Last Modified: Wed, 14 Aug 2024 01:36:55 GMT  
		Size: 13.4 KB (13439 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:a0245b594c8a6a884d705414d5232e268b5d7062eafb1b98225415d2b55dc0e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117536666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9c7d1628118be4b5774ef3f875dbcf002723cc06d3d74b6869c5775e7edc09`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Tue, 13 Aug 2024 00:39:43 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2e025713139fa5c991c9bf9d00b7fbde00d8f0ab83e504d780d21d6b6685cc`  
		Last Modified: Tue, 13 Aug 2024 21:16:06 GMT  
		Size: 67.9 MB (67948074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7312846d0293805c23e209f88c93cfb73dfeaa192073747680da50fe0fe474a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3711601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a530c020d25be9ca96778122355955e18847e425a86ae37893ca25dee412d53`

```dockerfile
```

-	Layers:
	-	`sha256:f5586dcf1ef0c215a20401a21bdad484553691079b279961b4afd97aa5cf64d1`  
		Last Modified: Tue, 13 Aug 2024 21:16:04 GMT  
		Size: 3.7 MB (3697928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a954f5872d91fee8f3d12e3fa5af02f12cbfdb3b8a937e59f02e930cd6233d3`  
		Last Modified: Tue, 13 Aug 2024 21:16:03 GMT  
		Size: 13.7 KB (13673 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; 386

```console
$ docker pull erlang@sha256:f9c846aebe6008b0823cff1a59cd4b5febac6c6d81434938ada712f4db6144c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111641307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51cb6f95b45f384eebef67ff09c7f826c65e5628a6f60cc7109ddd6ce1d3e16`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 00:38:44 GMT
ADD file:186aa300689d339d1d06b70259642fdc3a3f05cf379dd7bc9113d1706442ac74 in / 
# Tue, 13 Aug 2024 00:38:46 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0fb95c9c136baa9709f12d568ef1c0ddb37d3820dbe74a35da128350ee89d900`  
		Last Modified: Tue, 13 Aug 2024 00:42:11 GMT  
		Size: 50.6 MB (50579430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4e90ae0b3562cf5e2617eb407bdb229889f969cb7823b04eac56cd9b68612`  
		Last Modified: Tue, 13 Aug 2024 20:09:28 GMT  
		Size: 61.1 MB (61061877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:22a236e65158198b548917c98bfcab2f10d4e6cafa215e4093e348a6ba77cd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3708126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786be2a7e6c90f36fb642425497af04aec5e4358059966a4ab58564d6aa6dab4`

```dockerfile
```

-	Layers:
	-	`sha256:3d49e0ec0bc4175885abd506a7a3614dca31b174da47f649825900d6e0720031`  
		Last Modified: Tue, 13 Aug 2024 20:09:26 GMT  
		Size: 3.7 MB (3694787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf17895fa2c48efe52bbb78e38d16fcef06b9787e981928163b5818786225808`  
		Last Modified: Tue, 13 Aug 2024 20:09:26 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:3a6c0d13e41caf5446dc382264d89f66aa29654edcebccd3fd806362388d5265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110584746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7e28564a90d0b23a619cb7722ec942c573c7d69bc7e467f7e557c32bf81768`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 00:10:27 GMT
ADD file:42b5546fc536a0937c9332001326b56edcfad5a5db46bb873f84f73c3bda9b67 in / 
# Tue, 13 Aug 2024 00:10:33 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:192d8664ef287a4c7c8030bb7f9fd54f06a0ee665114437e01bd957247249b59`  
		Last Modified: Tue, 13 Aug 2024 00:21:46 GMT  
		Size: 49.6 MB (49563201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5873de8b9c7ca81257fcd7539e5713ca26c8ac869a8845aaee6f73ae63bf104`  
		Last Modified: Thu, 15 Aug 2024 00:25:25 GMT  
		Size: 61.0 MB (61021545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a79c180ba03595eb78c4056533143e48375567becdfb70c89905474456b9aa20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ffca7c81444be69564209e076f3e260fedab5bcb12221b3f517f6cfa01bc3d`

```dockerfile
```

-	Layers:
	-	`sha256:ffa7f51b540d1cfbee25e3e1dd5bd4fc0365495c6cf75f39f464b75e9e3de609`  
		Last Modified: Thu, 15 Aug 2024 00:25:19 GMT  
		Size: 13.2 KB (13207 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:3e22ebb42eee7af1dab68de2d2f9c45764c89d47ca5e331e00ab846d58058e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115695649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabb6c9af6ce580c93d9d58c0b4288fec96b9fcd792273c04e8a6d9f5d319b12`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 00:21:45 GMT
ADD file:ab0e4226a337b1961b7d55136a14b66759f90bba2db5d26f8732ebbc319429f0 in / 
# Tue, 13 Aug 2024 00:21:48 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b0024b855a69137bba16353fc7a6011f930a151823178a16a296ac1608c06e1d`  
		Last Modified: Tue, 13 Aug 2024 00:25:56 GMT  
		Size: 53.6 MB (53556969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af558aa89768acfcea55de959dc28ffdb379a80417ea44e5a94b599c8624f08`  
		Last Modified: Tue, 13 Aug 2024 23:44:46 GMT  
		Size: 62.1 MB (62138680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7823bd80b7cd279b3e719c389130fd38b01569adc91610b3ec5c975079ff9d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa407db09380287cf36f40e4263b8f403b57c574b16db52d266f8e0ca8e02f1e`

```dockerfile
```

-	Layers:
	-	`sha256:79ae78e9f179aa1b0f121e724a2276b6546ce33623ee03ff6eaba9699a849e73`  
		Last Modified: Tue, 13 Aug 2024 23:44:44 GMT  
		Size: 3.7 MB (3702007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4bacae9c4fddb471245a3ff7d9e3caea858061ad3ad7aaa95b16779b3ec39e`  
		Last Modified: Tue, 13 Aug 2024 23:44:43 GMT  
		Size: 13.4 KB (13407 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:26-slim` - linux; s390x

```console
$ docker pull erlang@sha256:d0c8c2f0c0e38dd809bb186b09df342c98f7c9f20b76f0c49ca9ce34f3281995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.8 MB (108777888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56bcb34f642dfef3232d0b7dc799bd98c615bddf4b6aab48981beb34d3648258`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:19 GMT
ADD file:5b6a24a7099d06f537e95320f30a6d6e0a68ad8f3d736974423a162d38166bbc in / 
# Tue, 13 Aug 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 13:58:20 GMT
ENV OTP_VERSION=26.2.5.2 REBAR3_VERSION=3.23.0
# Tue, 13 Aug 2024 13:58:20 GMT
LABEL org.opencontainers.image.version=26.2.5.2
# Tue, 13 Aug 2024 13:58:20 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="8e537e2d984770796cc7f0c7c079a9e5fbc67b8c368e0dcd9aa2ceaeb2844da2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 13:58:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ea8614b3f892649521ca59d97829a6db2b909ea5240504ff4f238e1d5967f5c4`  
		Last Modified: Tue, 13 Aug 2024 00:47:14 GMT  
		Size: 47.9 MB (47931410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80d134f48a355b15bb71b180fe53ad01ce6f6663fd4673c932f496c66a1b9d4`  
		Last Modified: Tue, 13 Aug 2024 22:40:08 GMT  
		Size: 60.8 MB (60846478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:26-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d7d50c7cd569ada167362300677d188afa359c4a3da4d58fd78c00bba07daa10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cf33b724640716550ebf83a135ea60f9c77f006e7cf2a384ec7e33d285420a`

```dockerfile
```

-	Layers:
	-	`sha256:144972f9a03c49c141126f2500f8730a05dba7893a489e0dc833263df2e6219e`  
		Last Modified: Tue, 13 Aug 2024 22:40:07 GMT  
		Size: 3.7 MB (3697495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4f29ba764ad993973395d35a9095041420a37b664b744d3e6cacf1c878b65fe`  
		Last Modified: Tue, 13 Aug 2024 22:40:07 GMT  
		Size: 13.4 KB (13369 bytes)  
		MIME: application/vnd.in-toto+json
