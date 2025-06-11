## `erlang:slim`

```console
$ docker pull erlang@sha256:1591b1f1b45a4c725ac85baae13afcbfa6e80e1ee59ab9498d1f35277c96610e
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
$ docker pull erlang@sha256:0b70cd2aaff09e3af5e182641f03ab3e7bd506ea7aa121d24ccad53f3e3f32b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128328971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163be2164b890a2f282eacb864e67ed95e902654cf26e5b888e15d337efedf59`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 22 May 2025 12:07:47 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a079fc42b6e6fdc2b7d095ae6e5d2a10faa8a3b589b0eef3a28d112c72d994b0`  
		Last Modified: Wed, 11 Jun 2025 00:12:48 GMT  
		Size: 79.8 MB (79834699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:355e72423acb3c2903ed5c6fa63b06fec56a66a58132f095d38e19c146cd9184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3831540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ea945d7b5c0e90b9051bbc7032dce8341e5e24137b821219c4cba7e21afeb5`

```dockerfile
```

-	Layers:
	-	`sha256:f334ac9c30d6ba944eca7f58aa0a95db9a4fa1cd91a04f2c810d5e7b1ba1e79e`  
		Last Modified: Wed, 11 Jun 2025 01:47:47 GMT  
		Size: 3.8 MB (3817575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8024830e4270629c2a6e21d1b129f0e7da97678f569b74cd4bb828e574366c`  
		Last Modified: Wed, 11 Jun 2025 01:47:48 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:cb945b5233df5a442f5378835a157f686ddf841161d1dcd2ef3b5c0adbcb543e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115534392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:126cd79142b63dcfcdf7498abc44d5c8bd75c976c2867400a608095c5fdc1ac9`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d34b66573dd99436757429c603646ae3e6d1948a3fa85413a39cf069620a7229`  
		Last Modified: Tue, 03 Jun 2025 14:36:18 GMT  
		Size: 46.0 MB (46021484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7202fa27afdce2d6f3cfeced69aa7e60f039e8b6e799dc7553343ab9a56628dc`  
		Last Modified: Thu, 22 May 2025 18:41:39 GMT  
		Size: 69.5 MB (69512908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7af1f72aa48952210df2b1b5ae591abfc4c6712dcf8d6b311e2d273715bc7645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e224ef4867f3b1a829f1a47ff0de7915d6c6b8931e8999d4c3635f50d07796`

```dockerfile
```

-	Layers:
	-	`sha256:1804feb6f653fabee24fcb0edf4e6b6309bf8c8bd4bda51f95f695a729deb3a3`  
		Last Modified: Wed, 11 Jun 2025 01:47:53 GMT  
		Size: 3.7 MB (3730397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959d7dd62fd70215a6e2a4df18df02223c6ed02c93bd5dac49de057f8e4902f3`  
		Last Modified: Wed, 11 Jun 2025 01:47:54 GMT  
		Size: 14.0 KB (14049 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:9cbbdd1304668ff05b818c3b0f73504ce14ee02fe300cc9870f1ae10240a7e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113120480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03178169f9bf6c2536e0e5037c152f9ca6bcb3a03b849d0521b1dae792230c76`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0183c889ce2824e8a26aaa2eff3fd1ced98036fce740dbd964ebdc6e1dbeaac7`  
		Last Modified: Fri, 23 May 2025 08:01:09 GMT  
		Size: 68.9 MB (68917709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:dc916148e317698de7d9b65dbf01a3dda25b30a0d695816432344fc93f2fb85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e5b150740b3b1a77606f589080be78bd50cec701d5097285521624378480d6`

```dockerfile
```

-	Layers:
	-	`sha256:52a85c2e98db28ae0a9caf56e281c64115b9529e4b36ccc37dfc548bfe18514d`  
		Last Modified: Wed, 11 Jun 2025 01:48:00 GMT  
		Size: 3.7 MB (3728822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45a916d39bf38e9c24a01c66e3f1423e9223c78d9aaa22a68353321264562d9`  
		Last Modified: Wed, 11 Jun 2025 01:48:01 GMT  
		Size: 14.0 KB (14049 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:4126f949d298f0507db04a52867a26c05617031a11e2b00110d37f7a1bada4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125957140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22076c782b2b017818492222117aa16029622f18a815a8d683317d973af32aef`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d716c065972db9c2b6dd4c99601ab62036ed5fecf795ecc39aa1d9ee2e961df`  
		Last Modified: Tue, 03 Jun 2025 15:46:25 GMT  
		Size: 77.6 MB (77629959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:8f129fdfac344e991b0d6b28a528f555f86f7693067de291bf200d5f93b62eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee20c80c341df0dca6f1d2776ad0ba837ae94244d4ed26b55ceb4ae99532381c`

```dockerfile
```

-	Layers:
	-	`sha256:bd6050d13257d914b837c9eadf80e79f3aa170ce4260f4b6867c71e48ee50fc3`  
		Last Modified: Wed, 11 Jun 2025 01:48:06 GMT  
		Size: 3.7 MB (3726854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0033e31de908e936069fe25491e809a9c3dccf0e7377edc83d2b874f0138f581`  
		Last Modified: Wed, 11 Jun 2025 01:48:07 GMT  
		Size: 14.1 KB (14081 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:2c05d255ba459d644d15c679e889312e3343a9ce59fc2ef5a7d8d20ffadb60cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119525818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0a236cedb79e71c47efea0f9eafe7059f2feb63b80414c15fe0ef5fb3117a3`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 22 May 2025 12:07:47 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe04d804d5c2eb71dd0442ee0b7f4c88d270098b93419218fbdea4af53beb73`  
		Last Modified: Tue, 10 Jun 2025 23:39:26 GMT  
		Size: 70.0 MB (70048344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:907619a392bfa383118a6a8cc78ea7da3daf05d11a5ad004669afc522b3c6bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3828665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e68274f30f0255b46260c6f3e322258d5275a1fd1140082653296a87be3f07c`

```dockerfile
```

-	Layers:
	-	`sha256:0b16c98e963cebb5c7e1653e9ddb073feb7e2ea4ee76c068087d0b18c00c2fec`  
		Last Modified: Wed, 11 Jun 2025 01:48:13 GMT  
		Size: 3.8 MB (3814737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45409250402a194d8b75fac28e7ccadf0b669a245850eb5ae8c64bb1ab043c3e`  
		Last Modified: Wed, 11 Jun 2025 01:48:14 GMT  
		Size: 13.9 KB (13928 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; mips64le

```console
$ docker pull erlang@sha256:2ff9df14514effa3a38632939f14dbaad2d8b5eecac16551390a7b7d6fc63ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118752849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64351edd35a81e334535535520c85253ab947e83e508ca9ea41a9b5aa18bb8ed`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:d480a40975e955224ed64be37e82f220f731f0379d20a7b8c36be0e47e31d8df`  
		Last Modified: Tue, 03 Jun 2025 14:36:18 GMT  
		Size: 48.8 MB (48769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f78183eb7a632b7f8a07be89d4adbf76f64d751a359289eff75a1001013d2f9`  
		Last Modified: Fri, 23 May 2025 04:56:59 GMT  
		Size: 70.0 MB (69983096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:24556f34ec03fd8cb5d0a3d5b80eac65c511c7e4fe80d5c417ff1dccff76a37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6767c6c70a6452f844cb40f7f691969f5a76ba87cb0291437077731edaac9554`

```dockerfile
```

-	Layers:
	-	`sha256:2565619da21dd0e74b34140858329eba1e3b302d664c4055884454ed4756ea3a`  
		Last Modified: Wed, 11 Jun 2025 01:48:19 GMT  
		Size: 13.8 KB (13825 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:4119147da31b5ba5d3eb5e9988ac20dd9343bfadb5bfc13f613c61de811e811b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123397387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373698f6de69451b114576901b31a27cf6e0222c02a0c92b88167011ee5cad3b`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88547891be63f2b608bc231c7557fba2fe192759467fb6e214874d634a320bc`  
		Last Modified: Thu, 22 May 2025 17:06:09 GMT  
		Size: 71.1 MB (71065768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d379d06d3adb9d2268dba5132049a3d023f9d27ab3cd5d7e2e4aa8fe5bea11b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5542904b38b6f9a19974fe2dd6ee3f270ace31fe32dd34c27d4e40f27c3dec4`

```dockerfile
```

-	Layers:
	-	`sha256:16767e63f46254c48c4f3116ef66e90d4618e26ee894350e33f0bcdce969b177`  
		Last Modified: Wed, 11 Jun 2025 01:48:23 GMT  
		Size: 3.7 MB (3731025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f09b786e7a8d3a6c90f2b301aca4027cadae1fa1cb353d1932d01df018a8ea10`  
		Last Modified: Wed, 11 Jun 2025 01:48:24 GMT  
		Size: 14.0 KB (14015 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:436b7224ec58b514a23386b2a7a0f21aeda0eeb09e44630e86917c6302626886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116817598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137881c201df44843d8247479d0e6bab45f8936116d43a344836c43788167f9c`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Thu, 22 May 2025 12:07:47 GMT
ENV OTP_VERSION=28.0 REBAR3_VERSION=3.24.0
# Thu, 22 May 2025 12:07:47 GMT
LABEL org.opencontainers.image.version=28.0
# Thu, 22 May 2025 12:07:47 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="71b5bf16e5b7b5d9fae98576c87aceac447964aaa3b4b457a5f60906839af92c" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 22 May 2025 12:07:47 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026a57d20a879fb2b3cd9a28d1261babfd12a99e574be1263c4b77d06a8af598`  
		Last Modified: Thu, 22 May 2025 18:40:27 GMT  
		Size: 69.7 MB (69673756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:6d28544c48a693ba5696ed3489c2b6a5e972e5ff8fd7db60cac6e790dbc067ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6765af1b738d89251669dca5fd472b6d36cb1b623cef8db2a8777e04afc3840c`

```dockerfile
```

-	Layers:
	-	`sha256:78dd46fdc6b2cae2c29d43de2681ca95226357e4b7438db2bcb53c5dbaf4fd55`  
		Last Modified: Wed, 11 Jun 2025 01:48:30 GMT  
		Size: 3.7 MB (3726301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c6dadba143685d19e7628d128fd66183e9514d9b6f4223869ee76035aa3d19`  
		Last Modified: Wed, 11 Jun 2025 01:48:31 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json
