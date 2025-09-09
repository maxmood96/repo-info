## `erlang:slim`

```console
$ docker pull erlang@sha256:bd7a34ec39ebe57cfaa0b8f84feba4f3a11522396af45157d84af90a3c84588d
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
$ docker pull erlang@sha256:9463b6442ea5adbf87e3b296c2d786dd931e799fa29e49a04170e9bdb4a99861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128831491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e075e68c47d7ea0f611c3a70e008e1be003f58240713728eb6aff19ee028bc2`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79bb253ae04cfb22f7bff275dd8768d5e8d9849d902c182d860268c09bbec5e`  
		Last Modified: Mon, 08 Sep 2025 22:02:12 GMT  
		Size: 80.4 MB (80350881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4948a4fc226a5b64350ec0f818ad464c346d1aae0e0c5b6c265582dfa5487a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab400b7dace3c42a2635bc8af92821b8dd91b6b8f520db6a10e22cce31a84d3`

```dockerfile
```

-	Layers:
	-	`sha256:ef6c77c44a2575f6f25b345a23b1cd31a2ebf6dcdef7be7b7a1935c910c282e5`  
		Last Modified: Mon, 08 Sep 2025 22:48:16 GMT  
		Size: 3.8 MB (3824232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f35bf9671979d0d49b5061ee262e2a7ef040ccba82d190c73c8263a8a76903f`  
		Last Modified: Mon, 08 Sep 2025 22:48:17 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:6fb1dda36905d4dcd52ce2d1b27062dc2675a3763a9d0fe4056b023cfcac06bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (116036916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558ac50e70841d7cf34caa2a89bfd2bc598d756cbf773db05caa9814cca2901c`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1757289600'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:cb78550743da54c438514c9643e672e9378df901e1cdbedec41078f3c369313d`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 46.0 MB (46015690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a5b1bd6e8b15f1f5684056d572c36481e67841560d27327b4dc3adb379ca9f`  
		Last Modified: Mon, 08 Sep 2025 22:48:11 GMT  
		Size: 70.0 MB (70021226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0683f5ffe283526e7a2eebea774498ada1e22f6221b97825f95503fd6bb2de6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ff3688427d62c42448f615321e95993f0020dc3bb9568ed9ccdb3ddcd4d9fb`

```dockerfile
```

-	Layers:
	-	`sha256:6d80a40fcbc3e594a8e5ef9149c2f4eeff45bc19a76ebd24ed283e3d6c18c6ee`  
		Last Modified: Mon, 08 Sep 2025 22:48:21 GMT  
		Size: 3.8 MB (3828048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:368c9bc79b7185248031a8e31b0b063f9c499b5afbf76c8590f190e4f482460a`  
		Last Modified: Mon, 08 Sep 2025 22:48:22 GMT  
		Size: 14.1 KB (14055 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:9f09e0e4ac717e88bfbf8e3a5b3f0172b3e1175090f3deece7ab13ff042ca546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113627028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab93867c0f2fa792ad06cb034e9071c469c03b62cda017bc8175ee298a08a57b`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f65d652edffc88f3a9b9e37d4391b94684d5df8dd7a16332b72e93d4f55ced`  
		Last Modified: Tue, 09 Sep 2025 03:37:52 GMT  
		Size: 69.4 MB (69431030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9ace0660d523448ca2e99ffd72c98c75748ff1e1b549bf2e6d4a9253e4ad31f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3840528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeadf7b8241b1328c485990604252f61677a43c245d10208c70d3dcba4c68df3`

```dockerfile
```

-	Layers:
	-	`sha256:6fd0e1b33e6c125fa79d5155f5b46d1ddcb4b2b0ac56791307c567a90048259e`  
		Last Modified: Tue, 09 Sep 2025 01:48:58 GMT  
		Size: 3.8 MB (3826473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68cdbe931ab53d693ac7bf655857543def9b7412e09c75a2d4a27096e9eba56d`  
		Last Modified: Tue, 09 Sep 2025 01:48:59 GMT  
		Size: 14.1 KB (14055 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:8ad94540518d03ee070d590f137f52f1b430d7b8a915edc44ec9f2d9e9142a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126505851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc90c2863681015d23e7994fdc89d7c4bab7803fa5cc90c19e8fe06a0d2a6217`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd27a6d8106affdafc26e72a100584eed3b8fcc640730167092c04d58f532c2`  
		Last Modified: Tue, 09 Sep 2025 01:17:30 GMT  
		Size: 78.1 MB (78146832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:06f01ee34a52dbd08379ae3764477ce835ed0d97d435173bbf7a08e6cffcbaf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3838588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192aef1cfe618e44ab20846cab028513dbf109c9511c3295cd9670f4d2ca2f3a`

```dockerfile
```

-	Layers:
	-	`sha256:0e8e367c9415f0a6a3b19111a9e0ce3aa9988d8e17e03b43eed7a3ea022b048f`  
		Last Modified: Mon, 08 Sep 2025 22:48:32 GMT  
		Size: 3.8 MB (3824505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f46cf6777b0ae9d5f89b0c7fffbaa723b2efb8f08a1272f80a1553fcff7425c5`  
		Last Modified: Mon, 08 Sep 2025 22:48:33 GMT  
		Size: 14.1 KB (14083 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:19f1ab0cbd87a08c1182237a44305a5febe07488e498a7c5f45bd1983c572a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120019504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90e637d9a0db2362519f56f8ae4c27cf7f62b2104a72408c1f0f0554c2a8fcc`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5538e96bb7df1a7ef01bd7fcbf51f4cbc041246109c06cf661f7058c203851af`  
		Last Modified: Mon, 08 Sep 2025 21:12:26 GMT  
		Size: 49.5 MB (49466684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9b7d1d652f565d813c0d31f4e796d09337dc78d2790b223fc062961c3debba`  
		Last Modified: Mon, 08 Sep 2025 21:58:40 GMT  
		Size: 70.6 MB (70552820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:93307eca1f2cbe2c4965cb3e036c16f3390893b3fc1f0b67e04fb039229b219a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6006a63c02528aec3643de709039c50d3fff15ece5f22b26f8e687b12f7df9`

```dockerfile
```

-	Layers:
	-	`sha256:97d91fe8871d90a923af21e7bbf9af745db510ea5517d346226909c7aa5c76d4`  
		Last Modified: Mon, 08 Sep 2025 22:48:37 GMT  
		Size: 3.8 MB (3821389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27748c1e35a912de26822b4e9647b07f429a65c2ab25769ec58d98e1bf82ee79`  
		Last Modified: Mon, 08 Sep 2025 22:48:39 GMT  
		Size: 13.9 KB (13930 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; mips64le

```console
$ docker pull erlang@sha256:8fee4941a0671ec25a4f41a6138aebca9138b478f3db50019b87d3a8f4def4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119265197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55214b886845052c14b627f82059d20a3fb09bc26a8e4160398b04f01b4f63c0`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:39ab9a968f454fda0ebffae415d31434cb4c4b3f4bb9da0e89f360bd60fa3275`  
		Last Modified: Tue, 12 Aug 2025 21:09:50 GMT  
		Size: 48.8 MB (48776657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28468c06ffa3d40773fe289dc95c153eca236372a993bb02666d7eb01f952de8`  
		Last Modified: Wed, 13 Aug 2025 06:53:48 GMT  
		Size: 70.5 MB (70488540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:81521391ed3875925443c40ce58ebd1e16149eedf6b35adf10c7ab4a16589f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8f8acb0c1a8914492bf9f427657584f3d8f840a86cf2d265d6a69b6c94d38c`

```dockerfile
```

-	Layers:
	-	`sha256:94644767f71517e1833da95c166821f2c83bcdc6cd4442b8f1f82672387fa148`  
		Last Modified: Wed, 13 Aug 2025 07:47:37 GMT  
		Size: 13.8 KB (13827 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:646156d99c395dfb536181bdf0310cf320188d384be4a18c302bcc1953bd20b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123897585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2761297ffaaa41a6cb0dc0e5f131076ed6d6390583a92352f4896679998e2a68`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e55e2b991d7bb40faf849257204fc1b46667469b9c3282014e96991105a1b4`  
		Last Modified: Tue, 09 Sep 2025 02:12:01 GMT  
		Size: 71.6 MB (71570763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d5b99fbca4bfeab06193366145aed30fd06c821f7d89078c6566315f4ed892cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3842702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc4da2cf192b0d732e6ffb4dc04bbd79451c78616f669c3ac5cf4d3354ef0f3`

```dockerfile
```

-	Layers:
	-	`sha256:a8f9928f0ee84097b6fc85fb90b7099efd6ec95328a17f02b8d1001b959283f5`  
		Last Modified: Tue, 09 Sep 2025 04:48:18 GMT  
		Size: 3.8 MB (3828686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f16a4860f184039c771251c560f9c2c879c28e045c15800f538f8ea7db2f7fa`  
		Last Modified: Tue, 09 Sep 2025 04:48:19 GMT  
		Size: 14.0 KB (14016 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:ac4d56f5a2cb862cb20637177c85fd3ae8f3df7aad8f4085fbfa79e32ebef218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.3 MB (117323971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79fc98af95cceb9e51fe87fb397fff642f433b6de80d8516ac283873370b749`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 19 Jul 2025 21:18:01 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Sat, 19 Jul 2025 21:18:01 GMT
ENV OTP_VERSION=28.0.2 REBAR3_VERSION=3.25.0
# Sat, 19 Jul 2025 21:18:01 GMT
LABEL org.opencontainers.image.version=28.0.2
# Sat, 19 Jul 2025 21:18:01 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="ce43dc8a29ad6bc1b6dbfc97f053d2e850b4a4c290eca065058d6b33ce476db5" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="7d3f42dc0e126e18fb73e4366129f11dd37bad14d404f461e0a3129ce8903440" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 19 Jul 2025 21:18:01 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fc31f60123fc51e4aa125950c1ada153d1a1310a02773f0a7d2a849a456f7a`  
		Last Modified: Tue, 09 Sep 2025 01:20:00 GMT  
		Size: 70.2 MB (70186432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:cdb50027b0799fce6f2e84ff257f8754c5c58bc24db1bf5d8250360a265693ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3835027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82612fc378e427b1f35040b79886bdb2b0c95c4c4314e75655405aa4485507ae`

```dockerfile
```

-	Layers:
	-	`sha256:66da17e992cc2287bb91e924a5059053991c0c4eea8467ad6dc59b8a281e9abd`  
		Last Modified: Tue, 09 Sep 2025 01:49:14 GMT  
		Size: 3.8 MB (3821060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e14a9a24ef59eaff51842aa73b8936b9d19b753f68fc8e7f88e55390d41c289`  
		Last Modified: Tue, 09 Sep 2025 01:49:14 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json
