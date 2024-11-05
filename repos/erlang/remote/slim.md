## `erlang:slim`

```console
$ docker pull erlang@sha256:e5145288a60075b6da9b6a9d45cd391eeccd5fef59c30536ccd625b480b95ce2
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
$ docker pull erlang@sha256:2bdadcc9c6d37461d3d60ed5b4d3649d50c210e1186dc7fe40204cb9d53ab1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125432926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a7c1bbb64688e06de19ecc619107cd7efab1fd10a7a2eec48b8a5523abb21e`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:17 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Thu, 17 Oct 2024 00:20:17 GMT
CMD ["bash"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74377689e61faef51f8d4f17df835fc462a02000a443d55e8caa214b57ea3bfb`  
		Last Modified: Mon, 04 Nov 2024 21:05:43 GMT  
		Size: 75.9 MB (75877903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2c3609f6651306ee69ac57bc351bfc461a82d07f9f594908f99ba95339c04577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b555dc7aea6b97c424a7db13089ba3cf33ea2c5d7db79db330607b4e8cc4a5`

```dockerfile
```

-	Layers:
	-	`sha256:2feb962e3c729ee16b7c04a2a124cbd8d0eaa5c7476b972dbf54e8eb2e7bd53e`  
		Last Modified: Mon, 04 Nov 2024 21:05:42 GMT  
		Size: 3.7 MB (3712791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccfcadedfc303c0148c52252d450d2bc981fb385bfd5f16f5c7e5067f5dfcd9a`  
		Last Modified: Mon, 04 Nov 2024 21:05:41 GMT  
		Size: 13.7 KB (13690 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:8b95563c05bfa3d6b55f30a96cc17ccd386f4dfed4dedac6672a458d5fda1e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.7 MB (112715778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6dd6c11ddb3d1c9a53eb7baa5f1bea69b83290c820dccacc5572c21e1b53b94`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:12 GMT
ADD file:f8dacf0eafc6476110951ab49fd75768d4262a1b61984cf9b4625bdd369500eb in / 
# Thu, 17 Oct 2024 00:54:13 GMT
CMD ["bash"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:638c60a841003707ab5971d86e3c262372536df80608e7e3641e6ad7f5dff43e`  
		Last Modified: Thu, 17 Oct 2024 00:57:04 GMT  
		Size: 47.3 MB (47330521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348f7d911889949bf28f48b067d1b243b5b1a04dd03ac4516d98c1a8cdb801d0`  
		Last Modified: Mon, 04 Nov 2024 21:13:47 GMT  
		Size: 65.4 MB (65385257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:3e1b90f13fdd422ebfdc14421b8cab939352513cdc2cd91fb40aa07a7d65d4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c29c3fd7696325ae824a1ebd9bb993a8d58c702914deb94a411dff6aee5521e`

```dockerfile
```

-	Layers:
	-	`sha256:112dcd81f0cff420662d91d97a6a1d17589236a4a3edea51bc278f024da7e24b`  
		Last Modified: Mon, 04 Nov 2024 21:13:45 GMT  
		Size: 3.7 MB (3716298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e64b80e068d87de8d9b633a42f7e6f0a19c2ffebfbae6b05bbcfdd06f704fb46`  
		Last Modified: Mon, 04 Nov 2024 21:13:44 GMT  
		Size: 13.8 KB (13767 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:91aa40ba8400a99fc7853638b71819fd8716999909221061c9f0b523f58548b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110149237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4dd9dcd63ec00a856119d2e1b5a315bc2483dfbc5d592a4b79d637b559e2504`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:11 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Thu, 17 Oct 2024 03:03:11 GMT
CMD ["bash"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e274555980bb7a8f9ffceaa01fc3f001b9825ed0c53d879ecda182d19c7e5f2`  
		Last Modified: Mon, 04 Nov 2024 21:12:22 GMT  
		Size: 65.0 MB (65001297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7368cfca36c06033d9569ce1e6e456b9b4ffa926d5dbf17d7a62cf3d50bef809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae22d244984f6af728493b391166b26112237e5771e44e739705c3f06421452`

```dockerfile
```

-	Layers:
	-	`sha256:104717ebb3f73c35d354a0326851cdc6eadc43fbb60a0e6f4f0ebabee66724be`  
		Last Modified: Mon, 04 Nov 2024 21:12:21 GMT  
		Size: 3.7 MB (3715031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055b93e9310829ace7e3c27151cae8e5ab51038885c5f2e810a4655a14a760a4`  
		Last Modified: Mon, 04 Nov 2024 21:12:20 GMT  
		Size: 13.8 KB (13769 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:6555cdceea793b563cc7cb85a8f133111e305161cf80dd708b4a0b2e87c70263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123189480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ac8db33c55e51cf7b3208122538203cd40b26a646300fa15d6ef3d2cd5cf6a`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:49 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 17 Oct 2024 01:11:50 GMT
CMD ["bash"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f13f211888c7ca137cdd0d527be97b3b80e0c7d4f9eecb2dd997f8226aefcf`  
		Last Modified: Mon, 04 Nov 2024 21:12:23 GMT  
		Size: 73.6 MB (73604502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0212ea492e9557943d97c273de877383bc2890df4ce08337f2b5a6ff6d9f33de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeaa8fa3e1b27401a0c5e816bfa885c6eb976a3153b6db89052424fa5ea4dd74`

```dockerfile
```

-	Layers:
	-	`sha256:f46a1cf5e2dc725dee5f904f4277e5d5100455c333ea570b38f63f632a97193a`  
		Last Modified: Mon, 04 Nov 2024 21:12:21 GMT  
		Size: 3.7 MB (3713063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60fd65a6ed59516ec05cdc9c35328f0f2cce7808ae10657c1088face7d43f5e0`  
		Last Modified: Mon, 04 Nov 2024 21:12:21 GMT  
		Size: 13.8 KB (13800 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:5d6802f9e2ebdd74822dbb491b6f905db7d7394816006e099df98db671a17a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116613487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9782c4a995a6955cb4f9be7b6123c797cbce20f2ff408426f62b729d4ae7ecfd`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 17 Oct 2024 00:38:42 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Thu, 17 Oct 2024 00:38:45 GMT
CMD ["bash"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c653022230f0d62d093c8499aaa17f70b9e658cc2530a4888a1cb5d5b3d0afa`  
		Last Modified: Mon, 04 Nov 2024 21:05:54 GMT  
		Size: 66.0 MB (66036653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:5f7646d318b145de829a175bb8679bf64ce301c56378c7d858fa9e05e3469cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3723562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d745328dcb5a5c63da92399532be5ab133bc52699579ea1989311d479f3d4c2b`

```dockerfile
```

-	Layers:
	-	`sha256:a6ef693a72d0bee3ae72f60d3ecbcfbafb401bfb2277eeb7abb6aedb8215c1d0`  
		Last Modified: Mon, 04 Nov 2024 21:05:53 GMT  
		Size: 3.7 MB (3709905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ebb3c75e4489b8f5ba19e4260798ea7319a0ac534f64e67d444133e6773a9c`  
		Last Modified: Mon, 04 Nov 2024 21:05:52 GMT  
		Size: 13.7 KB (13657 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; mips64le

```console
$ docker pull erlang@sha256:fd4a071d725f9c3510ea5d3f0e5d55872bad7c6b74c5240420cd33f597bfd657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115513216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c468045976da11696dc42cfd98d773c2eea00c8943ba7baab7b8015549b4f82`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 17 Oct 2024 01:08:45 GMT
ADD file:5fa3d47e52ee376ed002c84d34e93fe11e6db2308915238c5d7a9a5840814eda in / 
# Thu, 17 Oct 2024 01:08:52 GMT
CMD ["bash"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7bf8417b2ab139177317d556c6249cee54f60148ccee016ec60d45a13a21c7c2`  
		Last Modified: Thu, 17 Oct 2024 01:17:24 GMT  
		Size: 49.6 MB (49561619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1e2da8ed7879068986d6353bd3f056737023fc13746d7d1653e699bd3ba00d`  
		Last Modified: Mon, 04 Nov 2024 22:00:00 GMT  
		Size: 66.0 MB (65951597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9313f5b37c9a35572cb650c209bd3e7842c35fc7ddbe8566492879ee2adac56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8850901a89ad47f32ff757ef65561411696b8ae0efa376063f0c8db40dce9a4`

```dockerfile
```

-	Layers:
	-	`sha256:4c8a093ca14e1637a218256213b59fe554664ca3c00b754dae17ad9f6475f282`  
		Last Modified: Mon, 04 Nov 2024 21:59:53 GMT  
		Size: 13.5 KB (13542 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:2b2e00d98276ebef782b7ed05388e6cbe12afb344a1579d8b10036bad7ebb6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120662664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbadcf4e4330c77f688999881db4feb18e8fd9cbb75453b72db4de092e48b6c0`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:38 GMT
ADD file:c7ce4329d7c0cdfb8efa822e20a44ab1922fe70e4e8be36a317ec45c565a260b in / 
# Thu, 17 Oct 2024 01:18:40 GMT
CMD ["bash"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:bbeb3fa4a5ad17047af70a984a8c9e89b0702821c59cb2290ff6c49eec8d704f`  
		Last Modified: Thu, 17 Oct 2024 01:21:33 GMT  
		Size: 53.6 MB (53555597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d0e58fcb3751775281e45b4bebaf640905ad237971dab669f4969a8c963a3e`  
		Last Modified: Mon, 04 Nov 2024 21:19:26 GMT  
		Size: 67.1 MB (67107067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:07a95b5dc408068caacae1b65df9641eeec91b0dd3278a1ecea9760d44a50ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0104bc7b989f84dbaab1f7f0aac4a3b5672ce9e40fb22604471516df7c60f4bb`

```dockerfile
```

-	Layers:
	-	`sha256:49c6ee89b413d23d2baf228bd3ca0e869c346740a72f0e95a97460298ebd9ce7`  
		Last Modified: Mon, 04 Nov 2024 21:19:24 GMT  
		Size: 3.7 MB (3717136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d953c117164af81ca34ad504df1433a65ac1919e4a5837dba3f692ed89ccbb5b`  
		Last Modified: Mon, 04 Nov 2024 21:19:23 GMT  
		Size: 13.7 KB (13734 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:7be773c49f50bace966a5f782bf3edcdca97fec1909dc2578456426137a57782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.7 MB (113728288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c817cbd38f8e66d5b53d44a0c923d01ed7ac5af2066e6b215d69705746b6675c`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 17 Oct 2024 01:45:59 GMT
ADD file:be1cd8a5c7d60ebbe308ecf258da8f3d2dd59f7c877549c96e98e31165ba1eaf in / 
# Thu, 17 Oct 2024 01:46:00 GMT
CMD ["bash"]
# Sat, 02 Nov 2024 18:06:28 GMT
ENV OTP_VERSION=27.1.2 REBAR3_VERSION=3.24.0
# Sat, 02 Nov 2024 18:06:28 GMT
LABEL org.opencontainers.image.version=27.1.2
# Sat, 02 Nov 2024 18:06:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="365208d47f9590f27c0814ccd7ee7aec0e1b6ba2fe9d875e356edb5d9b054541" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sat, 02 Nov 2024 18:06:28 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:510daf83b7a2b266658f37f8849eeeba99ab0f02d08ef5c1ea7f613451a81239`  
		Last Modified: Thu, 17 Oct 2024 01:50:15 GMT  
		Size: 47.9 MB (47938447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3b6a2ad6c648360417d9fdd27c2ee28f691e8d3bcf538ce8bbbcfbf695d509`  
		Last Modified: Mon, 04 Nov 2024 21:16:36 GMT  
		Size: 65.8 MB (65789841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:cc7cb77c72b71f2cf9696522e66e08ed17e0ebfb8af8a7686212b4764005b033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0903b499f497d2263740bcd9515a2f3c5fd232c079110c3ac8174eaa333af567`

```dockerfile
```

-	Layers:
	-	`sha256:b649d0a3da08e1cd03cb8f4bf8b942cbe227514fd666ef39e335156affc1d601`  
		Last Modified: Mon, 04 Nov 2024 21:16:34 GMT  
		Size: 3.7 MB (3712512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3238ee1ac9edbc07a6a766ddaea41010c45f4fe5662c966b851c0ca354dbd06f`  
		Last Modified: Mon, 04 Nov 2024 21:16:34 GMT  
		Size: 13.7 KB (13691 bytes)  
		MIME: application/vnd.in-toto+json
