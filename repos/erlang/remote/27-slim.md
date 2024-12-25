## `erlang:27-slim`

```console
$ docker pull erlang@sha256:9105f1b69bbd76391fca90b85df2c2917ec9a9a9b5360ac6487737b893d18f60
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
$ docker pull erlang@sha256:8a7764d3569c3e08635123f0a57687bc48b5329f539186c9a9b9fecb7b764e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124376742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a63a8b7a65493dcbf30a7b4c667b098156e7972460f3f1f9fa828e4afd73cfa`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57160b581f62f2b52ac40bc5330a4e29f269cf62ac486e3b55faa4b77ea202ea`  
		Last Modified: Tue, 24 Dec 2024 22:34:08 GMT  
		Size: 75.9 MB (75879676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:5b3a9d7f528a204501fa366691245e158ebd2d2c336942ae44a3f259f528a945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8c2dd46389dba58b041df4d2cf9146c9f87969170286a965e7bf4e69d8c8d7`

```dockerfile
```

-	Layers:
	-	`sha256:52b2fb379e0b45be025b85d5e71f5d3b494158d7b7f306ccac31c760f86ca7c4`  
		Last Modified: Tue, 24 Dec 2024 22:34:06 GMT  
		Size: 3.7 MB (3708310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2765e2716776fb43d4e9b649bdb32a0e157a09d9014898a61c9dcd7f0f178aee`  
		Last Modified: Tue, 24 Dec 2024 22:34:05 GMT  
		Size: 13.9 KB (13890 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:1155748c13766db01a9bf8b0a3e69b129319a1d11aafceaa2cdc7229bcdea770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111410880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ec520da0c93579b6f16cfa93379a2f4338cd47a57de1599174c311e93a3211`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
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
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5977d1981a8dd254a92982955efea7890617039368c7131153d9913973730c53`  
		Last Modified: Wed, 25 Dec 2024 01:37:28 GMT  
		Size: 65.4 MB (65386638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:884bd12e34a02ac53ad606a847e930a3f06ab2d083dccd9517baf3660920d29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2908b8545300577bc8ef714778d50a388124576b333ec5d0b429c9678e4815b5`

```dockerfile
```

-	Layers:
	-	`sha256:4709628c48e0641c3cc528aef265449b46e032ef574d730b1cc88577d4ab7158`  
		Last Modified: Wed, 25 Dec 2024 01:37:26 GMT  
		Size: 3.7 MB (3711818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778cdbf3096cc564dda153ba6a8391f95d6505b0b23333d3b08a8082385611c4`  
		Last Modified: Wed, 25 Dec 2024 01:37:26 GMT  
		Size: 14.0 KB (13973 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:c8954360d037661bc8e3c7eff45777938b1aa1cfbd98e4327ed4017260f01e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109201698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657bbd1df719fcc47286f0de9d320ea112f04ccd618e708afd8721a9fced2896`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
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
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd3b67bcaa47bfd165b47944e6f50a16520251fc5eeccb01a2d7db1f8a34814`  
		Last Modified: Wed, 25 Dec 2024 03:55:39 GMT  
		Size: 65.0 MB (65001731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:c845e709fe7bf379c3d663d6e6b3f52e7ddbe6d84530099dd4e3518c826fecbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef7e8ba94456afecff8069d3f8ccaa483ee04bf64312074bb5f11090c3f8e00`

```dockerfile
```

-	Layers:
	-	`sha256:222381da80919f2bccf1c80ead5b76809fea671e97764be36ba662594db7284b`  
		Last Modified: Wed, 25 Dec 2024 03:55:37 GMT  
		Size: 3.7 MB (3710551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7cb7d242e35f1bc90fe440971faeb4c2d8acd4c7919ddcf86eac8c40dc54b6a`  
		Last Modified: Wed, 25 Dec 2024 03:55:36 GMT  
		Size: 14.0 KB (13974 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:338ad52bd5bc129614e59e62776c6fdb7c7d94bf79e81cee7626e602267ac0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121931347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919a0e9557b4f0c547aad36260b6431522efdd8593ffee576180ba285b4a57f4`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0a8527debe66b1505e613945c00c8576baf9c99fb6d6308da79ca1400ddc34`  
		Last Modified: Wed, 25 Dec 2024 02:01:20 GMT  
		Size: 73.6 MB (73605863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0e1cfb08ca900e7fc9768c3da077b0d06d14923d05278ae7bd3e2e372ad2a181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b4b21e583cb7a928574219b50f4b6911cbf062ada79eab277506b8ed53a99c`

```dockerfile
```

-	Layers:
	-	`sha256:8827a27fa02267203330fae3c89d68b4d691ffa1892b82b4b17a2257feb6360d`  
		Last Modified: Wed, 25 Dec 2024 02:01:18 GMT  
		Size: 3.7 MB (3708583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f497fa284301c23782d235f31e714af859337ac8dfeb00de4a105d4c7eaf8e4`  
		Last Modified: Wed, 25 Dec 2024 02:01:18 GMT  
		Size: 14.0 KB (14006 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:2f2e413ea00c5e2b93fdeb9b6fb67b0e02de9a65918e89adc22a224bd6e9d53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115512518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b12918f88e3c119d723773b254f550d051dc4db7e7aaeeb36497c14fed8a9b`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
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
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400b22076394db0050e1759c670f6766f37c079ab365e197c55432853c533243`  
		Last Modified: Tue, 24 Dec 2024 22:22:06 GMT  
		Size: 66.0 MB (66036593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:24fca4e3ee5d4262ae0d542f044d456bfbcbfe0f88d789b5a9fcfb917ec0cc04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3719278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3ba3e92696f3643b65909192a33f4b95b615309b2c2bd32121c14135183dc6`

```dockerfile
```

-	Layers:
	-	`sha256:f987f2af121a04680c6a77bfe986d48acec53956fc5f34adae553479381b7cdc`  
		Last Modified: Tue, 24 Dec 2024 22:22:05 GMT  
		Size: 3.7 MB (3705425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ccc1286455abb66b1b6d05104e1faecfafcadd991e84c3893ecbdf1389fc8e`  
		Last Modified: Tue, 24 Dec 2024 22:22:04 GMT  
		Size: 13.9 KB (13853 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; mips64le

```console
$ docker pull erlang@sha256:80d89874cfdcf984c49b3a2c9d64febfbd0c82fcd5be3db8077122acb3ab489e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114727242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793ebfdaedb461f7592c71468234db1678a7bb7e9516a33abbaec5152cb5773a`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
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
	-	`sha256:8f7c3140f4f3af477253c748b229283137cca4214e1c3df21109b821f9227620`  
		Last Modified: Tue, 03 Dec 2024 01:27:53 GMT  
		Size: 48.8 MB (48771844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5917337ede8a293bcf3ef4074c3ec1fd1ec9a829a3bcc18f4eff2515b0aaa1aa`  
		Last Modified: Tue, 03 Dec 2024 16:15:39 GMT  
		Size: 66.0 MB (65955398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:304cec14c25e9dd0c6bf4311a219403e39f57e7f7ee9c7d0e6676de06bf3351d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 KB (13748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c69afd7507cbf6b1e41f4061f50b000f1dce0f1ca1b6c9d17c8d6f85de56b23`

```dockerfile
```

-	Layers:
	-	`sha256:9f7dc814329acfd3b6b97b2e05303fb3dc98b23c913657a5c015fe3597d9738a`  
		Last Modified: Tue, 03 Dec 2024 16:15:32 GMT  
		Size: 13.7 KB (13748 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:bc4cc23b16e02771b18f8b45a6de146ceaa224e1f97e8e30cead6ea26814f96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119438395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bb73918e8e15dda86010088a5966aef61c03823d6ea27984882bedd5adcba9`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
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
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326935dcd00b5ebb733162e2f9c873059d6a6a845d004571619fc0d2464c3b5a`  
		Last Modified: Tue, 03 Dec 2024 05:02:22 GMT  
		Size: 67.1 MB (67110173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d0538c9013b988ea56c4694797c6bf73f9554c52b4276fa9eb446e1b5289a059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58754ed08b863f38d5513496eeffe6a6c65ae94919c64ef972aad815fcfb368c`

```dockerfile
```

-	Layers:
	-	`sha256:05d694a8a14ca0009875e3327c828c89008103cf0c8e23fa82544e8632e2c6a0`  
		Last Modified: Tue, 03 Dec 2024 05:02:20 GMT  
		Size: 3.7 MB (3715888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ea404644d15d44e403322058228d525a4868ef75e4461cef79e53f3c2f8261`  
		Last Modified: Tue, 03 Dec 2024 05:02:20 GMT  
		Size: 13.9 KB (13940 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; s390x

```console
$ docker pull erlang@sha256:a54d1a0e95bebeb49387b2ec9d92ce2360b28a36335d7cbbd4b412b2e06d133c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112941329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd79168b47370c9c1c3967213330957b1da2585b3f954ddc037d9a765fe404d0`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
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
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ab6ad539b4b078ed51f9865d4a9375df6f24b12a6e5850e030c1fc1ca2a143`  
		Last Modified: Wed, 25 Dec 2024 00:28:51 GMT  
		Size: 65.8 MB (65791704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d6212b133217e9c8a71c5850e70a3387adaac1f48cae50cbecb23a68a19b5156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3721920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2d815f487e8fa903da4711e96ed6ae290a098f89b3b9aac0d5a3429311d687`

```dockerfile
```

-	Layers:
	-	`sha256:df23929c7696b1018d5044cd4043d25fc047f5a77c9f56d8011647220fc6ac1e`  
		Last Modified: Wed, 25 Dec 2024 00:28:50 GMT  
		Size: 3.7 MB (3708030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d763c059646c63324ba9cd7a2b46db25f879ab2576ce1febeb109e58af3cbc78`  
		Last Modified: Wed, 25 Dec 2024 00:28:50 GMT  
		Size: 13.9 KB (13890 bytes)  
		MIME: application/vnd.in-toto+json
