## `elixir:slim`

```console
$ docker pull elixir@sha256:35f0421c9675b82fd8e535a87b9fa15c7a040f6e235ce84a9aa3d776d4627490
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `elixir:slim` - linux; amd64

```console
$ docker pull elixir@sha256:137d0684180b7f9ca601219165e5a79b04113ba901730a20c85b278b70056360
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132306296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a7d171609832f9cfc25551e49a0faa5ff6bd54a074309f0fb085003e386eba`
-	Default Command: `["iex"]`

```dockerfile
# Sun, 26 Jan 2025 05:59:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Sun, 26 Jan 2025 05:59:54 GMT
ENV OTP_VERSION=27.2.1 REBAR3_VERSION=3.24.0
# Sun, 26 Jan 2025 05:59:54 GMT
LABEL org.opencontainers.image.version=27.2.1
# Sun, 26 Jan 2025 05:59:54 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="07982134e10637dde57cf9cdc6dda6f65425810229986136d184766d4db9eda3" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 26 Jan 2025 05:59:54 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325fad59910dfe6d206f54edfd4c23bc375a6169d2775fc13c8f70d847197b00`  
		Last Modified: Tue, 04 Feb 2025 14:10:27 GMT  
		Size: 75.9 MB (75912163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d429894a716e7a25e44aada21154af691ad1881cec95e7b2276d7a519a2767a`  
		Last Modified: Tue, 11 Feb 2025 00:39:16 GMT  
		Size: 7.9 MB (7914446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:8597abcd5f14975a4233792de2aa5546b3d6bbf09a81f22bcc20ab85e01574a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ab955d6ce58a92522cb6997769073e52febc2fb1219dfd06e6de944f02da39`

```dockerfile
```

-	Layers:
	-	`sha256:af3db90faa6c3d1a2681cb35d543ca1c44495daf24d24d1fd3b52fcbb68d5934`  
		Last Modified: Sat, 15 Feb 2025 20:00:08 GMT  
		Size: 3.7 MB (3668146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8cf77d612727ca67aacbc6889ed2956df1420b0646607d5c50a1874e97ec953`  
		Last Modified: Sat, 15 Feb 2025 20:00:07 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; arm variant v7

```console
$ docker pull elixir@sha256:3f486540129487bde6659e7b4ca150614be8e48b57ef0972beb0b6e54a8deb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117126055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567d2267e1c16cd8aa79f78d89836ca6fdf6abf506339b31105804ded8e4264e`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.2 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.2
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4f74095a24e48978f062b077651ac0876c5d3a42799b20fd996923bf15b5df29" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 05:02:17 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a0f0e7fb6060a1397f3548bc97e1be4610cc45d605247b0636bd1f8d297b16`  
		Last Modified: Tue, 18 Feb 2025 20:41:11 GMT  
		Size: 65.0 MB (65028227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef482686824f8ba7467086516b2f8df836458dd51c567f18451808e582141df`  
		Last Modified: Tue, 18 Feb 2025 21:34:27 GMT  
		Size: 7.9 MB (7913776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:945a6dd321b1dd99bcc4ff6c66c58c3f7fef57b57e88b03ac94c5c0de5132efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3728984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad087e5926130da37c8c51b505af2403ebffe9699fe7c4c134d8265ed798bf6`

```dockerfile
```

-	Layers:
	-	`sha256:21ef911e497125e598f5fbf48298bcd760a33aa56dc1edd6aa29e35be93e1454`  
		Last Modified: Tue, 18 Feb 2025 22:48:24 GMT  
		Size: 3.7 MB (3718213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220969e9b1a0f8e6fda4a6c18a6efae165895ee2886b27838068f261299bff3b`  
		Last Modified: Tue, 18 Feb 2025 22:48:25 GMT  
		Size: 10.8 KB (10771 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; arm64 variant v8

```console
$ docker pull elixir@sha256:443182c62425c8475b06bccd29aa9b62b0603d80d4b1e54e9b8a4f17fbdd687f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.9 MB (129872155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0745f0903770b43ec5c4a26e6c5a4e98d239a4107becdbf1555e64b4bf4a8d8a`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.2 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.2
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4f74095a24e48978f062b077651ac0876c5d3a42799b20fd996923bf15b5df29" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b5c4efd5f1c341a186403ad1a65b07df6bd28986ef8622e379f22e9662bfc4`  
		Last Modified: Tue, 18 Feb 2025 20:36:13 GMT  
		Size: 73.7 MB (73651512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30763a51bf8d97e5b7690642f289f6795a0e5dc38a96c2ed17258928ade9c07e`  
		Last Modified: Tue, 18 Feb 2025 21:35:30 GMT  
		Size: 7.9 MB (7914090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:2a81e08efbae4010cd2415c7c75aed1e8421b9e3c29056c9b0e67c4ab06a3f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3727055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d82befe5188b220ee0a261aca0a361d44ba1e2b62aab0d00695ac4a24938eca`

```dockerfile
```

-	Layers:
	-	`sha256:c026a11a91b92c78b395314aabe02c3a8e46a94e086786a0e4b38fe6c6bdee56`  
		Last Modified: Tue, 18 Feb 2025 22:48:27 GMT  
		Size: 3.7 MB (3716249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a362c5546ac353b8e4a864402f6dc266380892dbfa2aa9d41211042c53cadd44`  
		Last Modified: Tue, 18 Feb 2025 22:48:27 GMT  
		Size: 10.8 KB (10806 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; 386

```console
$ docker pull elixir@sha256:1fdf125a3c9a00b59768a7903f5bf12a8f3fd4eda318fa707d6f3725caf57374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123431634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6e153ecc5f37720e40511d98a9e8dd5ee81d3061850a96bfe89ff3dd32585f`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.2 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.2
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4f74095a24e48978f062b077651ac0876c5d3a42799b20fd996923bf15b5df29" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 06:02:17 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1375de261051b6989290cb66553087c18d6ca1a353aa8772aa0d80c736652a8b`  
		Last Modified: Tue, 18 Feb 2025 20:33:28 GMT  
		Size: 66.1 MB (66060285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d741fafe68266f840108e4680376e9308b05b3e8580ea3d772b739cb4c0738c`  
		Last Modified: Tue, 18 Feb 2025 21:30:20 GMT  
		Size: 7.9 MB (7913893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:941632ca70a0dcbfb37d06e8cabedd4ed638801a497c1f458c74bee1939b55df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3675893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f52b607e955e913c6ec4a2e39d62be154f976fa2c4877fb427b3a482eef414a`

```dockerfile
```

-	Layers:
	-	`sha256:026e95960984858a500c3fc33f05ff6b67791ca5c7fae57f2e461c8bff303409`  
		Last Modified: Tue, 18 Feb 2025 22:48:29 GMT  
		Size: 3.7 MB (3665256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb537d59e30966504a24ae9589d528aa79bf1472e291333f61c7aba08e4f9725`  
		Last Modified: Tue, 18 Feb 2025 22:48:29 GMT  
		Size: 10.6 KB (10637 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; ppc64le

```console
$ docker pull elixir@sha256:aa2eb128b924c28b0506a356e6747b0dd5399626eb1dd87c20ed9769459293a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127390687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91420ff7d2cf9c79d848bc53586c0626c9c44aad1e1ad1c2cd8d4a2fc5599e2a`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.2 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.2
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4f74095a24e48978f062b077651ac0876c5d3a42799b20fd996923bf15b5df29" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 06:02:17 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befd4a64fa94913d5cf7f4e49090d82adae32b6f87f56e1ee2d911fd81608d92`  
		Last Modified: Tue, 18 Feb 2025 20:40:38 GMT  
		Size: 67.2 MB (67163313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc55a22ca47a043efeea01515d8b84cd032dff29e18a7425d1b2f7629080af7f`  
		Last Modified: Tue, 18 Feb 2025 21:39:00 GMT  
		Size: 7.9 MB (7914517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:ed0983a2bcadb15022b7906989c497f932be9f61cda2639c3c9d4f0949575822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79627e322cd6c3c65c90c8d59ccfd5a924019e00915f3095ca0191c137d1cd8`

```dockerfile
```

-	Layers:
	-	`sha256:8158d6b8eed15c88df5c629b611b8fc8c8712763f7323298f78bd24792c85229`  
		Last Modified: Tue, 18 Feb 2025 22:48:32 GMT  
		Size: 3.7 MB (3720316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68c40986f809499bcbd6aa8afbb2d94402387067acc2b9967673d69612b00e1d`  
		Last Modified: Tue, 18 Feb 2025 22:48:32 GMT  
		Size: 10.7 KB (10735 bytes)  
		MIME: application/vnd.in-toto+json

### `elixir:slim` - linux; s390x

```console
$ docker pull elixir@sha256:5f5101260b501910567499c71edabf57ba0653b8008ccb8e1d1d1c4a6b3ec0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120872841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c142cf96907d7418cac1ff7b3b0e04be2c806d8d4a64fcd7937b04e8b35286fe`
-	Default Command: `["iex"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Sun, 09 Feb 2025 02:28:09 GMT
ENV OTP_VERSION=27.2.2 REBAR3_VERSION=3.24.0
# Sun, 09 Feb 2025 02:28:09 GMT
LABEL org.opencontainers.image.version=27.2.2
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4f74095a24e48978f062b077651ac0876c5d3a42799b20fd996923bf15b5df29" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["erl"]
# Sun, 09 Feb 2025 02:28:09 GMT
ENV ELIXIR_VERSION=v1.18.2 LANG=C.UTF-8
# Sun, 09 Feb 2025 02:28:09 GMT
RUN set -xe 	&& ELIXIR_DOWNLOAD_URL="https://github.com/elixir-lang/elixir/archive/${ELIXIR_VERSION}.tar.gz" 	&& ELIXIR_DOWNLOAD_SHA256="efc8d0660b56dd3f0c7536725a95f4d8b6be9f11ca9779d824ad79377753e916" 	&& buildDeps=' 		ca-certificates 		curl 		make 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o elixir-src.tar.gz $ELIXIR_DOWNLOAD_URL 	&& echo "$ELIXIR_DOWNLOAD_SHA256  elixir-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/local/src/elixir 	&& tar -xzC /usr/local/src/elixir --strip-components=1 -f elixir-src.tar.gz 	&& rm elixir-src.tar.gz 	&& cd /usr/local/src/elixir 	&& make install clean 	&& find /usr/local/src/elixir/ -type f -not -regex "/usr/local/src/elixir/lib/[^\/]*/lib.*" -exec rm -rf {} + 	&& find /usr/local/src/elixir/ -type d -depth -empty -delete 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 09 Feb 2025 02:28:09 GMT
CMD ["iex"]
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 05:09:29 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62492f2261992ff1afdef0ccea3e5479c507fae5e9cd3c7ffa9f43bd268cd7d`  
		Last Modified: Tue, 18 Feb 2025 20:38:49 GMT  
		Size: 65.8 MB (65827358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8dd98c4ca901ed7e615dd198eb57d40b932edea27b7faf13e2bdf0ead2c0c6`  
		Last Modified: Tue, 18 Feb 2025 21:37:00 GMT  
		Size: 7.9 MB (7913991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elixir:slim` - unknown; unknown

```console
$ docker pull elixir@sha256:65e8a67ca17becd933d1aa40fd901f8cc82114406940354c740d58a6ae10393a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e20b119fb325cbd9fc17135b10c965a222516ca29f6ba2f2f7e185b6cde1c703`

```dockerfile
```

-	Layers:
	-	`sha256:3bdcd9baa6586b221e64bacab5728299602d36e284f1d8ff548915542fb9dab6`  
		Last Modified: Tue, 18 Feb 2025 22:48:34 GMT  
		Size: 3.7 MB (3715684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a0e1ad827b7e2de89bb14b7b38529f17d13e6a668c9b93e6c447836cfc2158b`  
		Last Modified: Tue, 18 Feb 2025 22:48:34 GMT  
		Size: 10.7 KB (10679 bytes)  
		MIME: application/vnd.in-toto+json
