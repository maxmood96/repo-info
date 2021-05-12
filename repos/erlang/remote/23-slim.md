## `erlang:23-slim`

```console
$ docker pull erlang@sha256:b194cbb41b7a1f9e5993cd0fc613eca63a806ad4ad11d371c65afe92f0e88a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `erlang:23-slim` - linux; amd64

```console
$ docker pull erlang@sha256:441b3ff889f64db1204f55dabf6cafd253ae06d28e97043eeb68020f4efd36b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111360015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3eef5690eeb49b8961008038dc14712d2124f9338dee6c3c94cee34c8375300`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Mon, 10 May 2021 23:31:37 GMT
ENV OTP_VERSION=23.3.4
# Mon, 10 May 2021 23:31:38 GMT
LABEL org.opencontainers.image.version=23.3.4
# Mon, 10 May 2021 23:38:44 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="adc937319227774d53f941f25fa31990f5f89a530f6cb5511d5ea609f9f18ebe" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 10 May 2021 23:38:44 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95972e6b7dde02cb5bbe15b489d588f62a41ba120e39a33e3f631cd5f2d457c`  
		Last Modified: Mon, 10 May 2021 23:54:18 GMT  
		Size: 60.9 MB (60927044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:644314d4d94923f9da4a2a052c0461b593c78225031ad51c5d05a0061f893ff1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105335821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1585d55efea147424fe3e2eccdace5cb634652b99d84b26b501bdf05b29481`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 10 Apr 2021 00:59:18 GMT
ADD file:bd2081229497eea2b33310cb1582b965581ca78b00b87cc8e42bdc8b9f350678 in / 
# Sat, 10 Apr 2021 00:59:20 GMT
CMD ["bash"]
# Mon, 10 May 2021 23:15:40 GMT
ENV OTP_VERSION=23.3.4
# Mon, 10 May 2021 23:15:42 GMT
LABEL org.opencontainers.image.version=23.3.4
# Mon, 10 May 2021 23:22:28 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="adc937319227774d53f941f25fa31990f5f89a530f6cb5511d5ea609f9f18ebe" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 10 May 2021 23:22:32 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:de0ca59eb81518ffd92fbcd386251018f950dc16b1bd8ad2e642184db76be2a1`  
		Last Modified: Sat, 10 Apr 2021 01:07:26 GMT  
		Size: 45.9 MB (45915598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cabd5c0b5f8fd9fe11fd06da1e20bc031ba21a240686477105a1117c25425f`  
		Last Modified: Mon, 10 May 2021 23:32:40 GMT  
		Size: 59.4 MB (59420223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:14dfa617e3f8ec2e8efa030af305843084fdf676f0b56249ba5d739d4542ba1d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107066609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0bc32dba57def785c57de3fd082898704818c10130997cbd9596bc9ed65c910`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Mon, 10 May 2021 23:54:00 GMT
ENV OTP_VERSION=23.3.4
# Mon, 10 May 2021 23:54:01 GMT
LABEL org.opencontainers.image.version=23.3.4
# Tue, 11 May 2021 00:00:45 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="adc937319227774d53f941f25fa31990f5f89a530f6cb5511d5ea609f9f18ebe" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 11 May 2021 00:00:49 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf99f0a941220ddeb05e7d3e5b1bcfd3f542a207b1455a6bb2bd34583c17daa`  
		Last Modified: Tue, 11 May 2021 00:11:15 GMT  
		Size: 57.8 MB (57840827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; 386

```console
$ docker pull erlang@sha256:32061fb5e796aa01daa9a228de801d2a436fda5d2e2b44837e266456d4274d6a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111496128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39aed83b6f5a7f09a8f041e4c44ded4db69509dc43ab80fd0eaa243964ba6524`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 10 Apr 2021 00:39:26 GMT
ADD file:de914d3ff1619f3af1574fb9644ffde6f0590dfcfe402ffc9e7b2c0500481706 in / 
# Sat, 10 Apr 2021 00:39:26 GMT
CMD ["bash"]
# Mon, 10 May 2021 23:58:15 GMT
ENV OTP_VERSION=23.3.4
# Mon, 10 May 2021 23:58:15 GMT
LABEL org.opencontainers.image.version=23.3.4
# Tue, 11 May 2021 00:09:24 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="adc937319227774d53f941f25fa31990f5f89a530f6cb5511d5ea609f9f18ebe" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 11 May 2021 00:09:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:848aed59cb94060ff383c5bac16a4d69d7babe251466ce3f80195bf8f7209702`  
		Last Modified: Sat, 10 Apr 2021 00:45:25 GMT  
		Size: 51.2 MB (51198915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336ab31253cb018e09a7ffcd18b222e1814079829e04b46671b4f581b11d6a5e`  
		Last Modified: Tue, 11 May 2021 00:24:16 GMT  
		Size: 60.3 MB (60297213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:583624e5c2cb96e9cc59512d67c14a6f310490403d654c4ecc1c8d8edcefc3a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112926877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568d9d59f859d03ea51a9abc3cb54906e9c9d0f46e135541635c3aaf95210715`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 10 Apr 2021 01:26:11 GMT
ADD file:0671a70f02e705f591888f40e87a43122cd95a6ead3df61becbc4a7fb1c7ec43 in / 
# Sat, 10 Apr 2021 01:26:21 GMT
CMD ["bash"]
# Mon, 10 May 2021 23:37:16 GMT
ENV OTP_VERSION=23.3.4
# Mon, 10 May 2021 23:37:23 GMT
LABEL org.opencontainers.image.version=23.3.4
# Mon, 10 May 2021 23:49:11 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="adc937319227774d53f941f25fa31990f5f89a530f6cb5511d5ea609f9f18ebe" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Mon, 10 May 2021 23:49:18 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d018a28ea8249b332e6bce3cb93862d5b05dba493dbaf3531505ce3a3701001b`  
		Last Modified: Sat, 10 Apr 2021 01:33:24 GMT  
		Size: 54.2 MB (54179922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fdce92aa615733da1f926c320b930d6c85e22e7a30bad07a585165286e7efc`  
		Last Modified: Tue, 11 May 2021 00:02:29 GMT  
		Size: 58.7 MB (58746955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:23-slim` - linux; s390x

```console
$ docker pull erlang@sha256:1a958358cf5038ffed48a545d464fe0059ddec62a9a6e9d16386291d01321e19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.9 MB (106885404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45997216f41556a4de30b520a6b964941b1e46fab8c34b2ae077aeff7f1f3bd4`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 12 May 2021 00:43:13 GMT
ADD file:ffd730820ba7e4874e61b094cd8b1b19e272722efa2f96b6c2c0518882aa8010 in / 
# Wed, 12 May 2021 00:43:21 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:25:55 GMT
ENV OTP_VERSION=23.3.4
# Wed, 12 May 2021 01:25:56 GMT
LABEL org.opencontainers.image.version=23.3.4
# Wed, 12 May 2021 01:38:00 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="adc937319227774d53f941f25fa31990f5f89a530f6cb5511d5ea609f9f18ebe" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Wed, 12 May 2021 01:38:07 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:03edb521c4b9db23cdd0bda14609ccca13d11f4c37cd9ca16173028e6d3647df`  
		Last Modified: Wed, 12 May 2021 00:47:45 GMT  
		Size: 49.0 MB (49000941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aadc0b62d3a103cb2ae6a7969c4e99c88f31a67682c096e95566d6d38948ba1`  
		Last Modified: Wed, 12 May 2021 01:52:46 GMT  
		Size: 57.9 MB (57884463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
