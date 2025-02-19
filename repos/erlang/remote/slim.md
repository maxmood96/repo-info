## `erlang:slim`

```console
$ docker pull erlang@sha256:28dccace7a478d78297e62053c02bce3a9703e7e6b3afdf9adab31d5ad7e663c
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
$ docker pull erlang@sha256:98802bc4bed93baa31515ebf5c6b1db16bd7ecf926f7b554792246d504d4e7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124391376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adb72ae1873a8d9719fa7f0ab3309e45fb76017496ce46bf033a775148f8e47`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Mon, 17 Feb 2025 00:01:57 GMT
ENV OTP_VERSION=27.2.2 REBAR3_VERSION=3.24.0
# Mon, 17 Feb 2025 00:01:57 GMT
LABEL org.opencontainers.image.version=27.2.2
# Mon, 17 Feb 2025 00:01:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4f74095a24e48978f062b077651ac0876c5d3a42799b20fd996923bf15b5df29" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 17 Feb 2025 00:01:57 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19431a1487be35858f3eec276c40d3b00aebf988581e9e64dd0248776f4f5034`  
		Last Modified: Tue, 18 Feb 2025 20:33:19 GMT  
		Size: 75.9 MB (75911689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1675352a7fab95b587c0a2a279361b4fb1e92b4ee9e42b0868fe927a4ea06288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdc1a53a7ef0863da9a58f0e364c589a2ce408ae820160b8f38e468742cae58`

```dockerfile
```

-	Layers:
	-	`sha256:c7f82c5defaa69f6bbeea3ed90466cb13e0566059051d20defaf47a22c9d2cfe`  
		Last Modified: Tue, 18 Feb 2025 22:48:00 GMT  
		Size: 3.7 MB (3667810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:152421ce46395c0854284eb53e20009b38a1bee2b2b98a8a64460c9991b80ef0`  
		Last Modified: Tue, 18 Feb 2025 22:48:00 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:6f023bf3345590c24272dce897c5c3d4f78207d2e9419f98067391bf2cf3ec5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111423863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff76785bf4700763cc0ac1154d7c06065d9a03d8b1a8e9af26908ac05d1f83f`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Mon, 17 Feb 2025 00:01:57 GMT
ENV OTP_VERSION=27.2.2 REBAR3_VERSION=3.24.0
# Mon, 17 Feb 2025 00:01:57 GMT
LABEL org.opencontainers.image.version=27.2.2
# Mon, 17 Feb 2025 00:01:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4f74095a24e48978f062b077651ac0876c5d3a42799b20fd996923bf15b5df29" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 17 Feb 2025 00:01:57 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 15:56:22 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39b477d0ac96205174fbf4471fc40d9ed540da9ade0641cd2f56969d0070f43`  
		Last Modified: Tue, 18 Feb 2025 20:39:53 GMT  
		Size: 65.4 MB (65417289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a394cce9659625239c85e43d265344a70c08ea3cdce4406b1baa9b0f5548681f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3725881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56a293383a7994dbd58de8ef28100d275404885c5c9bcd99628f0bc6d7e8794`

```dockerfile
```

-	Layers:
	-	`sha256:06afb74752a261e6376e0effced435eaf9e4235b21aee164754577d1a424b566`  
		Last Modified: Tue, 18 Feb 2025 23:47:48 GMT  
		Size: 3.7 MB (3711830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aa09163d16b08b7fbb0e1ceed8a22ace274cde87dd19090d50b9564c668989f`  
		Last Modified: Tue, 18 Feb 2025 23:47:49 GMT  
		Size: 14.1 KB (14051 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:380ff17c1f6c3c48e96a4178d88ca7f6d3e7f8fa33082a4652f13ab2c65e5552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109212279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014ce02bc67c335b2a328dac6bab70d3a5510e87e126283e633f6a7044c1955a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Mon, 17 Feb 2025 00:01:57 GMT
ENV OTP_VERSION=27.2.2 REBAR3_VERSION=3.24.0
# Mon, 17 Feb 2025 00:01:57 GMT
LABEL org.opencontainers.image.version=27.2.2
# Mon, 17 Feb 2025 00:01:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4f74095a24e48978f062b077651ac0876c5d3a42799b20fd996923bf15b5df29" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 17 Feb 2025 00:01:57 GMT
CMD ["erl"]
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

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ba7335668295b8591baf67c14278c1c2dd41185b0a30e7083962a662651a0829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3724614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73156c07a5ea384eefd832dfad54f2cb7eae6acfca9924012032c0a4c765266b`

```dockerfile
```

-	Layers:
	-	`sha256:b7a73d5897a7638430f99e5153e59a62108179a1175eeceb44bcf300cd17795b`  
		Last Modified: Tue, 18 Feb 2025 23:47:51 GMT  
		Size: 3.7 MB (3710563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1317bfc0f22e89774420b82e36a6529a27f2ec30299361883c1bf4f9c1a68ba`  
		Last Modified: Tue, 18 Feb 2025 23:47:51 GMT  
		Size: 14.1 KB (14051 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:6a53710c966d5c02450684166ff77c16f61da4f8a6075450f8c23683987abeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121958065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cb28af194531e499869f1116ec248a01d46e2ef4504a5821c38f368771f2f2`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Mon, 17 Feb 2025 00:01:57 GMT
ENV OTP_VERSION=27.2.2 REBAR3_VERSION=3.24.0
# Mon, 17 Feb 2025 00:01:57 GMT
LABEL org.opencontainers.image.version=27.2.2
# Mon, 17 Feb 2025 00:01:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4f74095a24e48978f062b077651ac0876c5d3a42799b20fd996923bf15b5df29" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 17 Feb 2025 00:01:57 GMT
CMD ["erl"]
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

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:d0e72a9aa8118ce6598fcc2121d83af6debd138964445e3675ec0a3ce5e00e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312ec940847aca51f8100bc84e704065dd2ca95b9f449b4ecc9f35b6ae221ffb`

```dockerfile
```

-	Layers:
	-	`sha256:843a99991c6e2afdf74a3646faf242f3788fbee075b85089db657803d02b8a65`  
		Last Modified: Tue, 18 Feb 2025 23:47:54 GMT  
		Size: 3.7 MB (3708595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21584e4d3ee618c99a61945e66a2b10191e80e4c11f020f9a48ace74d15b713e`  
		Last Modified: Tue, 18 Feb 2025 23:47:54 GMT  
		Size: 14.1 KB (14082 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; 386

```console
$ docker pull erlang@sha256:97b35aa29f944b939bbf2429bc558f296f78753f40ea7608344e82e71f9b060d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115517741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bc0eec67ef3b3e2895dae638e49c92ac66bfdd6f036c3707264d26c77c349b`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Mon, 17 Feb 2025 00:01:57 GMT
ENV OTP_VERSION=27.2.2 REBAR3_VERSION=3.24.0
# Mon, 17 Feb 2025 00:01:57 GMT
LABEL org.opencontainers.image.version=27.2.2
# Mon, 17 Feb 2025 00:01:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4f74095a24e48978f062b077651ac0876c5d3a42799b20fd996923bf15b5df29" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 17 Feb 2025 00:01:57 GMT
CMD ["erl"]
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

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:50b693ac430e4643648b18446c0254dc498807cac77ee9eaeed3533aa74d9074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a9d3d54e140e1fd1e060d163c83fc3aa803d9b6904841d39df00c50ff36d65`

```dockerfile
```

-	Layers:
	-	`sha256:8c3957ae4e78238932f1c60631dd8091d0a885e21347bb51f949930a079667dc`  
		Last Modified: Tue, 18 Feb 2025 23:47:56 GMT  
		Size: 3.7 MB (3664925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9fad731b8f29c7307791eda14522653d668fbdb49342b000f328872b3ba8e9`  
		Last Modified: Tue, 18 Feb 2025 23:47:56 GMT  
		Size: 13.9 KB (13930 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; mips64le

```console
$ docker pull erlang@sha256:a813aa36f39cda73bb8e6b5f751b8d4d639ee08ee31b3b053e960da07928d375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114748674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08226bd3b932c4d505783a3a1e498b293672ab2003ee9f0b7a05d2119b602fa4`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Mon, 17 Feb 2025 00:01:57 GMT
ENV OTP_VERSION=27.2.2 REBAR3_VERSION=3.24.0
# Mon, 17 Feb 2025 00:01:57 GMT
LABEL org.opencontainers.image.version=27.2.2
# Mon, 17 Feb 2025 00:01:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4f74095a24e48978f062b077651ac0876c5d3a42799b20fd996923bf15b5df29" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 17 Feb 2025 00:01:57 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:467081b053e1cbae3c04ca1529cea6d968f9b38249f5cdd15b07f60be084dd00`  
		Last Modified: Tue, 04 Feb 2025 06:00:54 GMT  
		Size: 48.8 MB (48757800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d355d9a8514d5632cf59a1b1a47a85315cbfe561801bcf4ffd7ac6ab83a467`  
		Last Modified: Tue, 18 Feb 2025 21:02:12 GMT  
		Size: 66.0 MB (65990874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1a54feecbb42c5f3c7f570dfe286dae229fa4d8b23282e599e9c9c428a2f8617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e0fcb3e626676744e9271af8ac7fd1ffffca9e050968ef36e40cf8ed5ae162`

```dockerfile
```

-	Layers:
	-	`sha256:b5532a6e22bf13f1a22d30715987ef79aefb3616cdd37d286648631d76d8bf72`  
		Last Modified: Tue, 18 Feb 2025 23:47:58 GMT  
		Size: 13.8 KB (13827 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:0bf404da60cc260630761b009ae4ecf9028c48338b7e898000681fb06841920d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119476170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4744360ee5b6996f44d1963e214a2e9f8cceeeff4c891194a72a67e43c7bdcbc`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Mon, 17 Feb 2025 00:01:57 GMT
ENV OTP_VERSION=27.2.2 REBAR3_VERSION=3.24.0
# Mon, 17 Feb 2025 00:01:57 GMT
LABEL org.opencontainers.image.version=27.2.2
# Mon, 17 Feb 2025 00:01:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4f74095a24e48978f062b077651ac0876c5d3a42799b20fd996923bf15b5df29" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 17 Feb 2025 00:01:57 GMT
CMD ["erl"]
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

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:3c2b8cc4bfb032c7531112c9bc91397b0f6ab6e9c0fac73165adbe59101dc5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3726684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e024cb9a0f2736471b6eb5e128ee4615bf88bda305aca0f4be6d9bd45c6e8b`

```dockerfile
```

-	Layers:
	-	`sha256:abc11b859a570ebf01bb2ec40984cdc8ede78a238b918f2bb1746e2a5e688191`  
		Last Modified: Tue, 18 Feb 2025 23:48:00 GMT  
		Size: 3.7 MB (3712668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4698cbd8e9ab4bdf2d18626b9a245016ae31f51542e26f85759d9d85e63251`  
		Last Modified: Tue, 18 Feb 2025 23:48:00 GMT  
		Size: 14.0 KB (14016 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:slim` - linux; s390x

```console
$ docker pull erlang@sha256:8c5630fa2910507bffb87d06f44fd6b23f50ba91423760b786fdf8d693786f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (112958850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07478c0a2d40fa2fa9e07b98404c1b025c32327ef2f375e4d508a9e658fb3ed`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Mon, 17 Feb 2025 00:01:57 GMT
ENV OTP_VERSION=27.2.2 REBAR3_VERSION=3.24.0
# Mon, 17 Feb 2025 00:01:57 GMT
LABEL org.opencontainers.image.version=27.2.2
# Mon, 17 Feb 2025 00:01:57 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="4f74095a24e48978f062b077651ac0876c5d3a42799b20fd996923bf15b5df29" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl3 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="391b0eaa2825bb427fef1e55a0d166493059175f57a33b00346b84a20398216c" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 17 Feb 2025 00:01:57 GMT
CMD ["erl"]
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

### `erlang:slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b1bdacf3cc6217dcc89d69cc18649e254d1028de3eb948f1fb820f39c7e9b2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3722009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab2b43f9960c9111061f5b35bed20891f9035111fa5795d5d6626717dca857c3`

```dockerfile
```

-	Layers:
	-	`sha256:0cff3de84aacfc2600bcbb7607f223b972b253bd9f24ef82c0693eb50c6b908c`  
		Last Modified: Tue, 18 Feb 2025 23:48:02 GMT  
		Size: 3.7 MB (3708042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ed65965e0f763ccab544d0204451c190417b367ac841703c7dae481be7afbf`  
		Last Modified: Tue, 18 Feb 2025 23:48:03 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json
