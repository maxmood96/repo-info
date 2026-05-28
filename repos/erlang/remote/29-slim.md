## `erlang:29-slim`

```console
$ docker pull erlang@sha256:01d8ddc2ef4d9e814efb4312b1b691ebdd8d855fcf7a7622c081fd8ca1dde895
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `erlang:29-slim` - linux; amd64

```console
$ docker pull erlang@sha256:ed09379fb8158c75122543f8d01127a5133a7cf15fa1db71c7eae80ab7387ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129590252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff77319096ce579547a96325814ed6205d540ae3c1da393a9588b6e85c2680e`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:30:06 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 28 May 2026 18:30:06 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 28 May 2026 18:30:06 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:30:06 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462f0fa98a669d4e1d50db65bd5e01453b4054cbee96d19624b8e4132db01b16`  
		Last Modified: Thu, 28 May 2026 18:30:21 GMT  
		Size: 80.3 MB (80279629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:fddcccbc0d9c8f1f3e218c799723441b32726708bb55e1987cb8faed53964007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3297757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfd81f863e189fdce2be65ee0e439fbe36e34eb6d6b8a62f641ef213abe5639`

```dockerfile
```

-	Layers:
	-	`sha256:0e8433e73bcacd49af35a491a37a2219a1c025b04ad9675eeaa5d54ebb0ff2a8`  
		Last Modified: Thu, 28 May 2026 18:30:20 GMT  
		Size: 3.3 MB (3283828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2696759324ee64d88eefce61bd7e94b01616afed973a11b894393c1750326e57`  
		Last Modified: Thu, 28 May 2026 18:30:19 GMT  
		Size: 13.9 KB (13929 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm variant v5

```console
$ docker pull erlang@sha256:7afc85f82f8a5d2b21cfd455d1330e7f09bfdc92a8ac7cdcbb2229bb3b7e662c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117924075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f34fe81f65ab66c1aa3c009c544627d5c63a50f1a42b46660b3515df0c407245`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:29:14 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 28 May 2026 18:29:14 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 28 May 2026 18:29:14 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:29:14 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:6cf4508cae9439867ef520e234c0d389bafbf206c9c5e0966546716701d698c7`  
		Last Modified: Tue, 19 May 2026 22:36:48 GMT  
		Size: 47.5 MB (47488046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482cacd77498e2d280232efa311e39a0e810d92e065e7d704f5e0b28ce1d23bf`  
		Last Modified: Thu, 28 May 2026 18:29:28 GMT  
		Size: 70.4 MB (70436029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:9aa59b8980ae030d9cbd13ead1da327a8f4c478bb34e2ec9c903e60d5fff44b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3300820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdc6bd14a3d65ea920c1640887c42c144589480eda25cf5b6693c5f12ac72c3`

```dockerfile
```

-	Layers:
	-	`sha256:66b734284bf20f8ae86b9bdb761138cf5d0ed3e37cb61fd63bc5d462c138b66f`  
		Last Modified: Thu, 28 May 2026 18:29:26 GMT  
		Size: 3.3 MB (3286803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6da89e2dfd0137c2d0566b960fbdf7e1e4b663e25b686d4a5cf28c7b588629`  
		Last Modified: Thu, 28 May 2026 18:29:26 GMT  
		Size: 14.0 KB (14017 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:f7673a833791cd4e394b3058827e06e35c5f8e2bca1d5e8ea33035acc3e21999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115748637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fb91fe12ca5d64ef00f4e298edb9a4cce57f15a684eb23119307e819a29d3c`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:28:40 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 28 May 2026 18:28:40 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 28 May 2026 18:28:40 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:28:40 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:16329e57da118ecb493828b7b07e7a4228b11fef4bc65ec0fa8d7fc9fac39b62`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 45.7 MB (45742031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a39a2ac4cec914f25baad9b5905d6b38da79f50b4c677723a7d60ba6f66405`  
		Last Modified: Thu, 28 May 2026 18:28:54 GMT  
		Size: 70.0 MB (70006606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:fe882e5ee5570ed7456b63affa2175bd600d3de8a7206a43b7c9e2717d113b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6425a2e96762a6dd83d5d84ea26e42bc31f9cd0b48aaec9adb5a131f36d7bb8d`

```dockerfile
```

-	Layers:
	-	`sha256:be567c3bf6b0292fbe9fb9c3db3b19873533656fa59e7fd8d25f69991bbac41d`  
		Last Modified: Thu, 28 May 2026 18:28:52 GMT  
		Size: 3.3 MB (3285252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:115927bf9272f15ab9aec01e6ec31f694bcc7e59d224ab4cd5075da7284ae6a8`  
		Last Modified: Thu, 28 May 2026 18:28:52 GMT  
		Size: 14.0 KB (14016 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:548e97d19e22c4a08731254eccc8bf55feebf61f5cf1356f737b5fb2cfb67cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128409580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b6b70312a1e51f78b068a08192e65e134bf5beb1edd6a606b613c376dcecb8`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:28:56 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 28 May 2026 18:28:56 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 28 May 2026 18:28:56 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:28:56 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d975fb1fee17f1d19f1a81b9fe80588bf47975b137ddf3424cb4452cd4075f`  
		Last Modified: Thu, 28 May 2026 18:29:12 GMT  
		Size: 78.7 MB (78737360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:102146735dc9176cb1c4c117438287d9894556b8a980d7a985bdc289054aa7d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3298771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2584f2eae0d43ff9245925134d49b2d6584ddc3bcaf503e22a5668ded86f09b`

```dockerfile
```

-	Layers:
	-	`sha256:8807242b7b70edb01b0543c7754d8d614bcda7055f090a552a094343ded974a8`  
		Last Modified: Thu, 28 May 2026 18:29:09 GMT  
		Size: 3.3 MB (3284726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7642a4b53b14053a83b459edd21eca546aea9c23f182a0e7f9f11167ad85835`  
		Last Modified: Thu, 28 May 2026 18:29:09 GMT  
		Size: 14.0 KB (14045 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; 386

```console
$ docker pull erlang@sha256:7d4ec2273d45d44cb64f4aa6684d9b8dff72f8f68d953328998d9cd414610648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121220089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6b523666dbeea85333cab47eb8bcf48eaf816d0d7428e6075deb30dc4a1672`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:29:10 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 28 May 2026 18:29:10 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 28 May 2026 18:29:10 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:29:10 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72388c27ed603b46c7760ec256823dadb8207b8d343fbb847a2515a09b6a389a`  
		Last Modified: Thu, 28 May 2026 18:29:24 GMT  
		Size: 70.4 MB (70390535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:ccde6562459c76f81c261e4fd639a2579aded7257310d831d113d93204b6371d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3294890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4606736e9bb77a05b27151c580a5856d594e69fbf09ccee1146b2b2880fc8b58`

```dockerfile
```

-	Layers:
	-	`sha256:ef6162e4337f09505c28a065c09c9111cdd8afa9b3d414ff0e7d162a32c1d0d5`  
		Last Modified: Thu, 28 May 2026 18:29:23 GMT  
		Size: 3.3 MB (3280998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ff353d55a4089945bba09ce2656f17070d6d00e8bbc70da4bc66c33e88ef31`  
		Last Modified: Thu, 28 May 2026 18:29:22 GMT  
		Size: 13.9 KB (13892 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; ppc64le

```console
$ docker pull erlang@sha256:035c20ffe191570350b93d0a311d4e6ddcd795d8d5091d5da427060b58cdae2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124509503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003f21aa2b2f038f7733dff8439a38057c6fcc551e251859f06755c9e57d38b2`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:28:51 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 28 May 2026 18:28:51 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 28 May 2026 18:28:51 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:28:51 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49be04d35f27c984f77217c21736346912de4a0a2b0856557ec5315e725667f`  
		Last Modified: Thu, 28 May 2026 18:29:22 GMT  
		Size: 71.4 MB (71377321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a03a2ba936e21debbe51345b1c00605066ec907a7874642268f4d9f6c2ccc9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3301398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ccb0273fd5833412ab5e362ce914b18b59ef74773e22a74c0db029a6d66293`

```dockerfile
```

-	Layers:
	-	`sha256:37b495932278edb643a01c885d43e1ee19e2e4d33c4d855207b9ce3e94858cf6`  
		Last Modified: Thu, 28 May 2026 18:29:20 GMT  
		Size: 3.3 MB (3287419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04e1e93d85ce2dbe48b05c064da18ff9ad76caeb6fa3b0877e7327dc35d73a47`  
		Last Modified: Thu, 28 May 2026 18:29:20 GMT  
		Size: 14.0 KB (13979 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:29-slim` - linux; s390x

```console
$ docker pull erlang@sha256:93f48941b127a4046038b2afd51b677b0df5d7e6a70db6cfd70b28a03d6d603c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120660469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad27e8727c0a3767b3c6fbcfa75aebe2f3eb1be590bd5dbd00766ba3650585c3`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Thu, 28 May 2026 18:28:12 GMT
ENV OTP_VERSION=29.0.1 REBAR3_VERSION=3.27.0
# Thu, 28 May 2026 18:28:12 GMT
LABEL org.opencontainers.image.version=29.0.1
# Thu, 28 May 2026 18:28:12 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/releases/download/OTP-${OTP_VERSION}/otp_src_${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="42299cd4674a898d354ccfcd16651a7940e0125af59ee3733f7bd5f4a0dd50cf" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc2 		libssl3t64 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="985cae6e957334cfa549190b9f5efb9185c184a18fc181c87b8dde096ba79f38" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 28 May 2026 18:28:12 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aee576bc312a1b8982dd72b09270248584a9ea40ce426f9f17bfe83dcfeb417`  
		Last Modified: Thu, 28 May 2026 18:28:31 GMT  
		Size: 71.3 MB (71280689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:29-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1031a8646830ff014ba9c380fe32a960c1ac38797de007a404b5dcb8fdc95f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3299198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfc71a67207d082da799eeb6a9d23ea15f1b16ff3718775d0c9d6f70a2d7597`

```dockerfile
```

-	Layers:
	-	`sha256:1d578a88fb596c7adb514b4f4d02b8d48ae9d88d36ad32a7ed09d9682d30a4f2`  
		Last Modified: Thu, 28 May 2026 18:28:29 GMT  
		Size: 3.3 MB (3285269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af879f7ace1d70a851bd58e6e7c2c250f3ebbcd87221a9b01c7e6cdc278ff3b3`  
		Last Modified: Thu, 28 May 2026 18:28:30 GMT  
		Size: 13.9 KB (13929 bytes)  
		MIME: application/vnd.in-toto+json
