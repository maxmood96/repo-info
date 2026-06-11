## `erlang:24-slim`

```console
$ docker pull erlang@sha256:0027dea6cf16d5e5136939218a5431bc4b60ff27f026e51347539877dabafcbe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `erlang:24-slim` - linux; amd64

```console
$ docker pull erlang@sha256:e240a11cd7fbc34bf7fbb2a6add61d2bc89bace7fbef5ff6c09629f947ecc978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (119014295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a205d3989ed8b78a342a67954f922e81e53475b1c3006ffe8c256ed40c74b792`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:47:23 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Jun 2026 00:47:23 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Jun 2026 00:47:23 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:23 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731096f9138d24aaa50dbfd2edb1e1bdb1ac3e416906dd42b3845ab9df23f3b9`  
		Last Modified: Thu, 11 Jun 2026 00:47:37 GMT  
		Size: 65.2 MB (65242526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4e66092aea556c40a3e6a6dc466d72c242e2146bde325186fe589cd65a4ee466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e79524692206df869fa81c9c9fc256a6d721685b72268febfdf220b09599479`

```dockerfile
```

-	Layers:
	-	`sha256:5bf16ebae21d2920ee22772ed24bb498ddb151ebcf05c1722b00714677bba1aa`  
		Last Modified: Thu, 11 Jun 2026 00:47:36 GMT  
		Size: 4.1 MB (4098875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc08fa9aea33b4a06fdf739c538dfdad3b4c2e729582a3d4741f00ad9f62966d`  
		Last Modified: Thu, 11 Jun 2026 00:47:35 GMT  
		Size: 13.6 KB (13568 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:70d4589426020e1176009a7a98ed0f3ade82959778400e4a800bc09e160833f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106289519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d2ac5637b8519e0212e5cef915a629347f4552108e9bbf21e98750c26a53d7`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:40:26 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Jun 2026 01:40:26 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Jun 2026 01:40:26 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:40:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:057662c04791d47966179d44811cec5af4565f7f7a6a4690c7d8e834d0ba3bd2`  
		Last Modified: Wed, 10 Jun 2026 23:40:48 GMT  
		Size: 49.1 MB (49064004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5cd0a097f6fb5539ac8db93f90452c69b87043c947d82192ebccf3cbf658b8`  
		Last Modified: Thu, 11 Jun 2026 01:40:38 GMT  
		Size: 57.2 MB (57225515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a723f6ee3e21edd6221be88a95bc5ce9c1bdab3fa67ef97b38f326ecfe7d6de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d451b9e957426a36fec75baa74530ae8d653e8e87a2986caec27a9d9021cfe07`

```dockerfile
```

-	Layers:
	-	`sha256:ea1ab594bf9cb2954aabc533330b86ecc7d8b73ce8b74ba73cc772355c08ebbe`  
		Last Modified: Thu, 11 Jun 2026 01:40:37 GMT  
		Size: 4.1 MB (4100476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496b7b5453b307f7e63ea7c6bc635154e22023ea510224fd51611b31228e5acd`  
		Last Modified: Thu, 11 Jun 2026 01:40:37 GMT  
		Size: 13.6 KB (13648 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:77015ede202546dec7d4e2fcade68761c5b1abe91afb4e885a365706b545c33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110340497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32dc2c818f0f3fc55f39afc17660557e4ced21b4decb6a263f8f5429b94363a`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:48:30 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Jun 2026 00:48:30 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Jun 2026 00:48:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:30 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f55e54a02efda13764f4347d270024e6f80c4c692f7e520aba0ee567ca6b19c`  
		Last Modified: Thu, 11 Jun 2026 00:48:43 GMT  
		Size: 58.1 MB (58076383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:1e9bf2fa9c9a8b41f6199adf1aa97bc60c4d626e79505f1c885727883b19d09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7433b766d48d1da235c3f646a5116717a5972de06ec85f3b870169adde9b8f2b`

```dockerfile
```

-	Layers:
	-	`sha256:8305c1b71f8cabd20228fded674e957d92d71214e5e2e2ae413a6a9edabe6007`  
		Last Modified: Thu, 11 Jun 2026 00:48:41 GMT  
		Size: 4.1 MB (4098496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ab46fc400d32df9ee74a182c9c73945c31112d518dc29c1df51758a52f70e1`  
		Last Modified: Thu, 11 Jun 2026 00:48:41 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; 386

```console
$ docker pull erlang@sha256:1d65eae891bc8d92616081119638bc06b8a08c1f4acd835a58abff365d596a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112417424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ca667971dd069cf2fc5487574fec48ebed5a6747162ca8f29e79f63ebf4a84`
-	Default Command: `["erl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:48:25 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Thu, 11 Jun 2026 00:48:25 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Thu, 11 Jun 2026 00:48:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:25 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:fa94b3659141003eaf4c6c1ec8d2e2140d97afd4e23da5fb64936eff3ddbe795`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 54.7 MB (54712857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb67364124a5562b781ad33a51076d53e5b3638f489a4e161d7029006040930`  
		Last Modified: Thu, 11 Jun 2026 00:48:38 GMT  
		Size: 57.7 MB (57704567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:3fbf64e474b9380560511c7c95665b6aff75858a6d6e5dc981568425e139c0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75342dd35a8b65f9eedba1b1a897f21efd24c4f1493910e64bea8e81582f2df2`

```dockerfile
```

-	Layers:
	-	`sha256:a7a923815398f379faa6741d1eb1a8b3a9c731f882b2fdbb86dbe9b43a945655`  
		Last Modified: Thu, 11 Jun 2026 00:48:35 GMT  
		Size: 4.1 MB (4095403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3c5990019302f22074bb2aca854b01100b7371bb5c0ed2df6a8de3d545e889`  
		Last Modified: Thu, 11 Jun 2026 00:48:35 GMT  
		Size: 13.5 KB (13536 bytes)  
		MIME: application/vnd.in-toto+json
