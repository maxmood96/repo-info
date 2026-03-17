## `erlang:24-slim`

```console
$ docker pull erlang@sha256:a57a44ecc5c97aa20e665e1237629de88745ade9f444251d786851bde3b243d4
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
$ docker pull erlang@sha256:3864ff27d9bf0a01469248a30e7425faa49f28b60dfbffdb09e1c7c36f385320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (119005182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4667f5404e859e44c7fca095de65c5525d8bca87f75954b3303b3e6a457c8ae6`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:44:13 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Mon, 16 Mar 2026 22:44:13 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Mon, 16 Mar 2026 22:44:13 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:13 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b5773395ba2cd3031d9fe28af54b228f376c3ecf066df73f59096699e1fb9de`  
		Last Modified: Mon, 16 Mar 2026 22:44:27 GMT  
		Size: 65.2 MB (65242701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:2790416b63865f129ad26e63c441dbbfba46a6490d6952269895bbd7a1a23ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4106bdcc5e704b401cc96f35a62de9788825c0dc019263484bf11408b9e2cec8`

```dockerfile
```

-	Layers:
	-	`sha256:70d9c3aa87cd643a89017182c28d0286af519976167209b16bb9fcac72a64c54`  
		Last Modified: Mon, 16 Mar 2026 22:44:25 GMT  
		Size: 4.1 MB (4098871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0772f9e071c986011749cd4ccef6e02c2b481592910eaa5c41058b2cb0f2a8bc`  
		Last Modified: Mon, 16 Mar 2026 22:44:25 GMT  
		Size: 13.6 KB (13568 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:db8b434ace1b3468ded5bb449eaa5fc7ab15a065722f91b585205fbe4c8b6422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107630135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e214f23e0ef821b3ab9fddbd58463c24e9925a835a69a7e5df9a406b8d485d`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 21:54:35 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Tue, 24 Feb 2026 21:54:35 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Tue, 24 Feb 2026 21:54:35 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:54:35 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:dada255a3ad6614e8b2a389545f0625a8ca4a68f069cd24789cbdcf7a89bee05`  
		Last Modified: Tue, 24 Feb 2026 18:42:25 GMT  
		Size: 49.0 MB (49047560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1fcf0d49e146621f65f132248ef581e467ad37d208d6428634ca28973f06ce`  
		Last Modified: Tue, 24 Feb 2026 21:54:48 GMT  
		Size: 58.6 MB (58582575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:4a9a48709621c704dcdd6a057969d4fd9c7a704ca9b2b121814cef6d9923a612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad630e2486d69598966d13815201747a8d9abf5bb4bf1030d2ab4ed22d4e14d`

```dockerfile
```

-	Layers:
	-	`sha256:b22cb0acbfaec517e6ede053cbfe89550f4d6e00e087cc61b6bbf8e4219a4597`  
		Last Modified: Tue, 24 Feb 2026 21:54:46 GMT  
		Size: 4.1 MB (4100472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b2c84e074217be4f13d38d7e15b54bed3a7276defc0e4916811f0759797713e`  
		Last Modified: Tue, 24 Feb 2026 21:54:46 GMT  
		Size: 13.6 KB (13648 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:5b169fcb92e7eac567b0bc9628dcf74a9887ff0f016e77763da3fd8ab8136274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110323848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b97fbd5da0271d19c21832327147259b9f335b009168de5709c222a6229024a`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:46:30 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Mon, 16 Mar 2026 22:46:30 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Mon, 16 Mar 2026 22:46:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:30 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892d9fc770b49a9525b928fd63dd0933a76365bc493287d61d46829772b11282`  
		Last Modified: Mon, 16 Mar 2026 22:46:44 GMT  
		Size: 58.1 MB (58076594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:b6641c51de56b88b23090ff641542b7b4ad535de596094704b1df733ccc5096a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc98843ffcf3df959266e5af272d32a38e3621739f6dfea543f612ff159a82c3`

```dockerfile
```

-	Layers:
	-	`sha256:81180711ed88de7e677209ad0985b5a6b4be60fb79cdf259d56d31df4ca4dbbe`  
		Last Modified: Mon, 16 Mar 2026 22:46:43 GMT  
		Size: 4.1 MB (4098492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702f30eac9a2f5e78092e56b7d828ff149ac44a8735bbc2f48ba0d5651d4b585`  
		Last Modified: Mon, 16 Mar 2026 22:46:42 GMT  
		Size: 13.7 KB (13672 bytes)  
		MIME: application/vnd.in-toto+json

### `erlang:24-slim` - linux; 386

```console
$ docker pull erlang@sha256:caa82ac15c120d4cac6dd4051ad06445392ff6c70c79be838acf37fc6243de17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112406802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d0e6869c38bf6ac0c5b47e8357549f6affa8d15e4d3971d357e58f2e6bfde9`
-	Default Command: `["erl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:47:12 GMT
ENV OTP_VERSION=24.3.4.17 REBAR3_VERSION=3.23.0
# Mon, 16 Mar 2026 22:47:12 GMT
LABEL org.opencontainers.image.version=24.3.4.17
# Mon, 16 Mar 2026 22:47:12 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="35f88a3af4d4885c5c17bcb8611da2d19f0626faa277392cd39c445254c015a2" 	&& fetchDeps=' 		curl 		ca-certificates' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $fetchDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256  otp-src.tar.gz" | sha256sum -c - 	&& runtimeDeps=' 		libodbc1 		libssl1.1 		libsctp1 	' 	&& buildDeps=' 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl-dev 		libsctp-dev 	' 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& export ERL_TOP="/usr/src/otp_src_${OTP_VERSION%%@*}" 	&& mkdir -vp $ERL_TOP 	&& tar -xzf otp-src.tar.gz -C $ERL_TOP --strip-components=1 	&& rm otp-src.tar.gz 	&& ( cd $ERL_TOP 	  && ./otp_build autoconf 	  && gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	  && ./configure --build="$gnuArch" 	  && make -j$(nproc) 	  && make install ) 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="00646b692762ffd340560e8f16486dbda840e1546749ee5a7f58feeb77e7b516" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:12 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:ad236c87f3ff6b413233974bf5899e332a9ceee3a606736011b98ba6596c59ea`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 54.7 MB (54702245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9548f1093b1eab0d97627fbf4540ed2cc18b53d523ade647adec80e297f8fb9c`  
		Last Modified: Mon, 16 Mar 2026 22:47:24 GMT  
		Size: 57.7 MB (57704557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `erlang:24-slim` - unknown; unknown

```console
$ docker pull erlang@sha256:a168fae58e0bf52f6639efe880c1adc3dd328e4f8faaa77f7507d1acf4b9647d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241b56d4044647b4200f3b4d19173473e233e928c20a8a7fa57197d3e1d034e0`

```dockerfile
```

-	Layers:
	-	`sha256:8847b37430f58283862c61ac10075e6045dcc14543bbbe34fdd049ad8ec28764`  
		Last Modified: Mon, 16 Mar 2026 22:47:23 GMT  
		Size: 4.1 MB (4095399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7c13f498ced34aad67f60b1caf7af8b2ecff9f5efc0a179e19014f073ecebb`  
		Last Modified: Mon, 16 Mar 2026 22:47:22 GMT  
		Size: 13.5 KB (13536 bytes)  
		MIME: application/vnd.in-toto+json
