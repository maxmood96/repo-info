## `erlang:19-slim`

```console
$ docker pull erlang@sha256:525533407fbee1d5966e7810c7268358e399104f58ebcfeec4551b02feaba63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `erlang:19-slim` - linux; amd64

```console
$ docker pull erlang@sha256:14748d0854e6211acc6c395968e99f674a25488de802a9cf97c20012796cfb9a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380693461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a9a6bf6b42e642fe385766a1324797eb05961fee8265cf3761bfb654e36771`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 07:55:40 GMT
ENV OTP_VERSION=19.3.6.13 REBAR3_VERSION=3.15.2
# Thu, 22 Jul 2021 08:20:30 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="11a914176a33068226644f4e999ecc6e965ab1c60a324d90020f164641631fae" 	&& runtimeDeps=' 		libodbc1 		libssl1.0.2 		libsctp1 		libwxgtk3.0 	' 	&& buildDeps=' 		curl 		ca-certificates 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl1.0-dev 		libsctp-dev 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256 otp-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/otp-src 	&& tar -xzf otp-src.tar.gz -C /usr/src/otp-src --strip-components=1 	&& rm otp-src.tar.gz 	&& cd /usr/src/otp-src 	&& ./otp_build autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	&& ./configure --build="$gnuArch" 		--enable-dirty-schedulers 	&& make -j$(nproc) 	&& make install 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 22 Jul 2021 08:20:34 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72984ee6fe484e174537e5f33f7e7e7e58726c7a02ac45e55d0d0936a341d9a`  
		Last Modified: Thu, 22 Jul 2021 08:53:34 GMT  
		Size: 335.3 MB (335313680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:19-slim` - linux; arm variant v7

```console
$ docker pull erlang@sha256:2255e834c0e766d42605e6b75264a82f136a7d5597ca6c98d049edd0716b57d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.2 MB (357164750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7ce94fcc46743da30a09785fb7495dc501975043aeea9abefc8540b95a2ba09`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 22 Jul 2021 02:06:56 GMT
ADD file:544c40297b94c3ecc6561cf7bfef1cdf9763a18ce5e24b6841a1b70d0516d41d in / 
# Thu, 22 Jul 2021 02:06:57 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 07:04:58 GMT
ENV OTP_VERSION=19.3.6.13 REBAR3_VERSION=3.15.2
# Thu, 22 Jul 2021 07:19:17 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="11a914176a33068226644f4e999ecc6e965ab1c60a324d90020f164641631fae" 	&& runtimeDeps=' 		libodbc1 		libssl1.0.2 		libsctp1 		libwxgtk3.0 	' 	&& buildDeps=' 		curl 		ca-certificates 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl1.0-dev 		libsctp-dev 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256 otp-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/otp-src 	&& tar -xzf otp-src.tar.gz -C /usr/src/otp-src --strip-components=1 	&& rm otp-src.tar.gz 	&& cd /usr/src/otp-src 	&& ./otp_build autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	&& ./configure --build="$gnuArch" 		--enable-dirty-schedulers 	&& make -j$(nproc) 	&& make install 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 22 Jul 2021 07:19:20 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:b3cc5e47308fe8ded537d7ffdcaba46fcdf803cfe9878bd9264754a50eaa128b`  
		Last Modified: Thu, 22 Jul 2021 02:20:37 GMT  
		Size: 42.1 MB (42120108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d738ddc66f48a8d5b990174232430671435a1993d1f4a10c0ddf9a94b00e8e2f`  
		Last Modified: Thu, 22 Jul 2021 08:03:58 GMT  
		Size: 315.0 MB (315044642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:19-slim` - linux; arm64 variant v8

```console
$ docker pull erlang@sha256:317f0bbc297ce63d83a366d3791a7990418414791a89eddb47c7f336abf9d503
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.9 MB (365851570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7537b534fad63b7fa0c75dc06ba968dec0d4d5710e77062f4ec4d67aad27b4a6`
-	Default Command: `["erl"]`

```dockerfile
# Tue, 17 Aug 2021 01:48:17 GMT
ADD file:79e0d0ec943ec405612e2310514d8f0c72cf83483eea6d5f1a7c28b36fa21cf8 in / 
# Tue, 17 Aug 2021 01:48:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 05:22:15 GMT
ENV OTP_VERSION=19.3.6.13 REBAR3_VERSION=3.15.2
# Tue, 17 Aug 2021 05:31:32 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="11a914176a33068226644f4e999ecc6e965ab1c60a324d90020f164641631fae" 	&& runtimeDeps=' 		libodbc1 		libssl1.0.2 		libsctp1 		libwxgtk3.0 	' 	&& buildDeps=' 		curl 		ca-certificates 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl1.0-dev 		libsctp-dev 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256 otp-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/otp-src 	&& tar -xzf otp-src.tar.gz -C /usr/src/otp-src --strip-components=1 	&& rm otp-src.tar.gz 	&& cd /usr/src/otp-src 	&& ./otp_build autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	&& ./configure --build="$gnuArch" 		--enable-dirty-schedulers 	&& make -j$(nproc) 	&& make install 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Tue, 17 Aug 2021 05:31:35 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:a410f7a7fb8af899e64ef008ec59cc8062766e91abbf21ba5cee65faac7ba3fa`  
		Last Modified: Tue, 17 Aug 2021 01:57:32 GMT  
		Size: 43.2 MB (43177652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efca582ba54fe164647a6ede4201d7c9f0708b91e0db3f7e16cd4f96d875f0a6`  
		Last Modified: Tue, 17 Aug 2021 05:42:58 GMT  
		Size: 322.7 MB (322673918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `erlang:19-slim` - linux; 386

```console
$ docker pull erlang@sha256:5689ef9371ce0ae85187434b799324a0877331bcec2400d2c6b96c20cf829c97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.5 MB (380532126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9df8c30eee4795a8de1a3c9304fad7ed8cd05cdf18b93ace150515216d1693`
-	Default Command: `["erl"]`

```dockerfile
# Thu, 22 Jul 2021 00:41:29 GMT
ADD file:c83a7d581497b7df343b529417c3b904cf901379d5124d738ac2539c778912a3 in / 
# Thu, 22 Jul 2021 00:41:29 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 03:18:20 GMT
ENV OTP_VERSION=19.3.6.13 REBAR3_VERSION=3.15.2
# Thu, 22 Jul 2021 03:42:25 GMT
RUN set -xe 	&& OTP_DOWNLOAD_URL="https://github.com/erlang/otp/archive/OTP-${OTP_VERSION}.tar.gz" 	&& OTP_DOWNLOAD_SHA256="11a914176a33068226644f4e999ecc6e965ab1c60a324d90020f164641631fae" 	&& runtimeDeps=' 		libodbc1 		libssl1.0.2 		libsctp1 		libwxgtk3.0 	' 	&& buildDeps=' 		curl 		ca-certificates 		autoconf 		dpkg-dev 		gcc 		g++ 		make 		libncurses-dev 		unixodbc-dev 		libssl1.0-dev 		libsctp-dev 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $runtimeDeps 	&& apt-get install -y --no-install-recommends $buildDeps 	&& curl -fSL -o otp-src.tar.gz "$OTP_DOWNLOAD_URL" 	&& echo "$OTP_DOWNLOAD_SHA256 otp-src.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/otp-src 	&& tar -xzf otp-src.tar.gz -C /usr/src/otp-src --strip-components=1 	&& rm otp-src.tar.gz 	&& cd /usr/src/otp-src 	&& ./otp_build autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_HOST_GNU_TYPE)" 	&& ./configure --build="$gnuArch" 		--enable-dirty-schedulers 	&& make -j$(nproc) 	&& make install 	&& find /usr/local -name examples | xargs rm -rf 	&& REBAR3_DOWNLOAD_URL="https://github.com/erlang/rebar3/archive/${REBAR3_VERSION}.tar.gz" 	&& REBAR3_DOWNLOAD_SHA256="11b6bead835421a276e287562588580b63ac1c8dcb0e3c51f674887e4ab395cd" 	&& mkdir -p /usr/src/rebar3-src 	&& curl -fSL -o rebar3-src.tar.gz "$REBAR3_DOWNLOAD_URL" 	&& echo "$REBAR3_DOWNLOAD_SHA256 rebar3-src.tar.gz" | sha256sum -c - 	&& tar -xzf rebar3-src.tar.gz -C /usr/src/rebar3-src --strip-components=1 	&& rm rebar3-src.tar.gz 	&& cd /usr/src/rebar3-src 	&& HOME=$PWD ./bootstrap 	&& install -v ./rebar3 /usr/local/bin/ 	&& rm -rf /usr/src/rebar3-src 	&& apt-get purge -y --auto-remove $buildDeps $fetchDeps 	&& rm -rf $ERL_TOP /var/lib/apt/lists/*
# Thu, 22 Jul 2021 03:42:26 GMT
CMD ["erl"]
```

-	Layers:
	-	`sha256:27f236654eb1268b8d3986746d9f9fc7ef6d5ea038754025d6953961a088aff0`  
		Last Modified: Thu, 22 Jul 2021 00:49:20 GMT  
		Size: 46.1 MB (46097283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca8a97b4de46552e5f2b188fa566b7cc874dd6ef36eddbf496dbbc4bee68c87`  
		Last Modified: Thu, 22 Jul 2021 04:00:59 GMT  
		Size: 334.4 MB (334434843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
