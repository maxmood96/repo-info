## `erlang:27-slim`

```console
$ docker pull erlang@sha256:1f0d00ef0d78bd8c65b1f5cebf0cda54d82bc46170c938ebbb907cd75677e00d
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
$ docker pull erlang@sha256:581297d307f04ee450e45d1fb9b18ac36d34883a041a45504216a54603ae49bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124376862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bcc889df013fb52328bd95f29dcfadf735253efd63f7b3d0a766a3b104de09`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69f955e52d6a4567ff93630bf5853c8ff1a7465d11392965172f49221218b8`  
		Last Modified: Tue, 03 Dec 2024 02:38:52 GMT  
		Size: 75.9 MB (75879652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:7936f4f056f2e5c4436a61454e3206b462bd9166615fb7b219a9af2398311824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff291ce219c2bfa7c2c2bd75637cac0895752449a5b0786f412d1fd5f66b988`

```dockerfile
```

-	Layers:
	-	`sha256:5dd1495d4fa33ebfd5f5bc8cf71883cddf6d69853282bf61d6a463c82ce4e460`  
		Last Modified: Tue, 03 Dec 2024 02:38:51 GMT  
		Size: 3.7 MB (3711543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faed81f51ca86e7e29d5f1e4fca9308d305170a676198891208856efbd5de403`  
		Last Modified: Tue, 03 Dec 2024 02:38:50 GMT  
		Size: 13.9 KB (13890 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:c66e11ee67e6066fc5694c7b268fb3a96e782a9116ca08006665745a3858dfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111411039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cfee83836210c01ba2ceffe318a25bbd74b7407ad5b1e482f0ecb6e7edb65b`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
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
	-	`sha256:a8ab0b752e573ceb3480052f24bc5fe3f4f4665c13a338db39c1d51f749528e9`  
		Last Modified: Tue, 03 Dec 2024 01:27:04 GMT  
		Size: 46.0 MB (46024374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7893d457fba2b4dd0ca4d2bf1fd33ca16edf871c188b2e44771168f467a0b4`  
		Last Modified: Tue, 03 Dec 2024 05:30:37 GMT  
		Size: 65.4 MB (65386665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4f497f9497c194901cace97d870b3db5cc01ba8dc3ab669ab4576c9be6b47c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3729024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b298e3283ca698f2ea9d31a67380d1c05a5dc16213ed75cdb85c5c7e7860c7c1`

```dockerfile
```

-	Layers:
	-	`sha256:9989d089a2e258a70a250ea18ca1afb14258b5c48a0f2e4023625ff54abfa0fe`  
		Last Modified: Tue, 03 Dec 2024 05:30:35 GMT  
		Size: 3.7 MB (3715050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e5349f6251d67d773c1666042aba9b7bd1d02748909f649083ef4caec4049d9`  
		Last Modified: Tue, 03 Dec 2024 05:30:34 GMT  
		Size: 14.0 KB (13974 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:a64bbc194ddf3c172eb987de0274051ab27d7733d2fe009e81b3b8e9b5d764b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109201865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c03a16a1b1e696cfb2e4fc541f72d5f4395ccb5f15740486868e3896198f736`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
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
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814b634c471405bffb5373ac62b1e3b08f4833a9b7aedbe76a926e094f1f45c8`  
		Last Modified: Tue, 03 Dec 2024 07:54:47 GMT  
		Size: 65.0 MB (65001756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d414cb2840f59c30a15d3df76c45a791a18c2639787ecab5067e270d38e87178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbceca706538641254d845854d82a5268f2dbb13f5dc4cd48b09089c535ca04`

```dockerfile
```

-	Layers:
	-	`sha256:75ff03726af7b384f6f3a3fec8162577917ece312b3492077f8cd29b9f1baaa9`  
		Last Modified: Tue, 03 Dec 2024 07:54:45 GMT  
		Size: 3.7 MB (3713783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:445acac320a268d2140a03be90ba84a51f47ef4732d017d010e8ce7f73ab77d7`  
		Last Modified: Tue, 03 Dec 2024 07:54:44 GMT  
		Size: 14.0 KB (13974 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:c38b7f498582b81ccf85ab671a819a8c4c4e01700815117f3582791cf595b2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121931601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7d4c732f11b7357dd21404dbb6ba27e46b18ccda23c0dd7797d28883762c5d`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5cdaf04dc22ba3cf57cf5c1f785ed69372464ecbbbd3113c2105e0f014cdb4`  
		Last Modified: Tue, 03 Dec 2024 05:58:01 GMT  
		Size: 73.6 MB (73605921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:975b671d6442720971da22f382d31dcdf8c00ab5c8449f6302b37df4e0e08435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53d16e57ce243beb7332426da81d035eb6fbc874a6094c899137fab500f891c`

```dockerfile
```

-	Layers:
	-	`sha256:99c1b649c6ab5cef84a74edab1e87de4e00a7da88ab741052987a7a5f5f88547`  
		Last Modified: Tue, 03 Dec 2024 05:57:59 GMT  
		Size: 3.7 MB (3711815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83cd696afade1297d121de02129193c62f77718e8d6788d40b7a9a348ecdb0ce`  
		Last Modified: Tue, 03 Dec 2024 05:57:59 GMT  
		Size: 14.0 KB (14005 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:27-slim` - linux; 386

```console
$ docker pull erlang@sha256:b3ba02f77eca2cec202654d699e5d54e4afb7545e222a6eff99edd633f11ecaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115512964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3354efd806f4c8f63d34f435ef8524ce94159032ef8e4bfd4aed19d465ff2b79`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
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
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f584e4d6050740d9d05f9206daf654540d8cbf4afaa6a44c6bcb50fc1e7d6acb`  
		Last Modified: Tue, 03 Dec 2024 02:22:07 GMT  
		Size: 66.0 MB (66036812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9a92d668de9e08b92fe0e82b345edb78202fd6072369fadae548c90cb5fb1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595c5ac1daa7164d573e86458ce892ab5107f1b283d46d0a6cdeda3dcec00ca4`

```dockerfile
```

-	Layers:
	-	`sha256:e09ca42fcd564a45a4576dc0e1079ab1c01414542eeafc239ca889b68b14e22b`  
		Last Modified: Tue, 03 Dec 2024 02:22:04 GMT  
		Size: 3.7 MB (3708657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f0a16f7750dd6c73fcb4eaccb6576b668950c681eee34cba88499e688c0146`  
		Last Modified: Tue, 03 Dec 2024 02:22:04 GMT  
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
$ docker pull erlang@sha256:1ee67ed30da3b855080568c591f9cc5afbad74783e8989312ff0a2d15db8f5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112941248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cd52538513ba0d52c1c63c698e8d2adef228afd62e3b5d7c766dc981e0feeb`
-	Default Command: `["erl"]`

```dockerfile
# Sat, 02 Nov 2024 18:06:28 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
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
	-	`sha256:53a5c0dbd93a4a7f540e18bbe49ba3d7fadaa390ebbce009c756e34c5b1ae048`  
		Last Modified: Tue, 03 Dec 2024 01:27:55 GMT  
		Size: 47.1 MB (47149767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50468267d822f7550cf1fe7cdc5dbb47b67e19f56377c2b968d27e08eca863ae`  
		Last Modified: Tue, 03 Dec 2024 04:27:10 GMT  
		Size: 65.8 MB (65791481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:27-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:0053315f6843730a7f1dcd7723e6cfab2323078db6ae1f071fa00bcffd1a1f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92b0ca32d51702699892be155f29b0e2abd70fc1d7ce6709a156e6128a68a9c`

```dockerfile
```

-	Layers:
	-	`sha256:688c2ae80deb1a226e609c413805eb745bc905002b23b52e084c33b2efe1bfb6`  
		Last Modified: Tue, 03 Dec 2024 04:27:09 GMT  
		Size: 3.7 MB (3711264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0abaf5766c88b17a0448c5a0b976246c423f44cdd1eae6d0d5c79647a342c3`  
		Last Modified: Tue, 03 Dec 2024 04:27:08 GMT  
		Size: 13.9 KB (13890 bytes)  
		MIME: application/vnd.in-toto+json
