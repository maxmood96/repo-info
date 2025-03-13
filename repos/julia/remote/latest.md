## `julia:latest`

```console
$ docker pull julia@sha256:5cc86d9b0eb097d25d2bc3b59e9ef14d04f3691ba5e22d30e5f846967bd5b39c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:d214bbfafb7857a1fe114fe4b075b84a11e0c6f50a0f470120dde2a398d64bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302417321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99460d03607f349d4b697cfd4578cc9881cd7ba523d5e39d58f71bc912b5e23f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 11 Mar 2025 00:06:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.4-linux-x86_64.tar.gz'; 			sha256='fb3d3c5fccef82158a70677c0044ac5ae40410eceb0604cdc8e643eeff21df8d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.4-linux-aarch64.tar.gz'; 			sha256='859f1a8cc4bce6911bc912f0e226a6ba2b1c144110b9d559d88f5077513d0e37'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.4-linux-i686.tar.gz'; 			sha256='0da3178ee5dacc1473e45c8c74838455252831f5d37483d716995742d3187e30'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.4-linux-ppc64le.tar.gz'; 			sha256='893f42cf47f58438d4d52a0eca3bcdf773dcf3681363d6fc24200c2ba8926286'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 00:06:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535c459fcc74dac8d9e522875cb04320fd535bd1082a99b578438a23e5a89c32`  
		Last Modified: Tue, 11 Mar 2025 17:58:01 GMT  
		Size: 5.7 MB (5713121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b144ff8aacbcfcd3cdece04aaa6daf87a18dbeffbf22548b5544179d846102`  
		Last Modified: Tue, 11 Mar 2025 17:58:08 GMT  
		Size: 268.5 MB (268484527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7371c84803b981758e7dc56f496baa8d2b0472215459be87d2a6c1eae4ba26`  
		Last Modified: Tue, 11 Mar 2025 17:58:01 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:29c70c3f3e5d44928a9e828734111a0d5175a03f53bda56e8d930653710a90ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac01963f49ae9cd090dfb8b756e4be30d53cffccab133b5e75cdde70fb1a76f6`

```dockerfile
```

-	Layers:
	-	`sha256:71e8fcb1a7d5895496ea719b4b601ea3688eb0c8c29a00c001a65776efc7cd8c`  
		Last Modified: Tue, 11 Mar 2025 17:58:01 GMT  
		Size: 2.4 MB (2445456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a838a91cc524ffdb57e7e52dbe440734cd6122632ed03a705e6f5b23e6604713`  
		Last Modified: Tue, 11 Mar 2025 17:58:01 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:1d41f5fcf6eefd3044965254f5881f4a2d6258d452d3b750c46cdc64d029feda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317587762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a855ad1238c9f6c0ee71bf4da3d2544ebdd6c8ed634a0108e9f23b8bb56e404`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 11 Mar 2025 00:06:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.4-linux-x86_64.tar.gz'; 			sha256='fb3d3c5fccef82158a70677c0044ac5ae40410eceb0604cdc8e643eeff21df8d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.4-linux-aarch64.tar.gz'; 			sha256='859f1a8cc4bce6911bc912f0e226a6ba2b1c144110b9d559d88f5077513d0e37'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.4-linux-i686.tar.gz'; 			sha256='0da3178ee5dacc1473e45c8c74838455252831f5d37483d716995742d3187e30'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.4-linux-ppc64le.tar.gz'; 			sha256='893f42cf47f58438d4d52a0eca3bcdf773dcf3681363d6fc24200c2ba8926286'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 00:06:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623c9e5d1ea31a7a45cb954b2a23a7b656d82aadfe8efe83457948c30abe81fb`  
		Last Modified: Tue, 11 Mar 2025 17:57:55 GMT  
		Size: 5.5 MB (5538119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9137d4c014db71ddd60cd04c959b931eb6ab19aee1e2512b60c2f7025da73497`  
		Last Modified: Tue, 11 Mar 2025 17:58:00 GMT  
		Size: 284.0 MB (284000848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9397f6ead4f31f178fa4ed2a6a79588d7fdadef3f973654ce9605665a29940`  
		Last Modified: Tue, 11 Mar 2025 17:57:54 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:f68c1c4ca53c523dae2cfea9df4abcf7f0cfb124bf3c3e497441c7977e9ce55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8408d54d2a4889b3f4231c670cf3c50aaabf437ec07877869d61175989e08f8d`

```dockerfile
```

-	Layers:
	-	`sha256:0fc250de16d38d47fc1e7f0f51ff4fe920508b74661c64b35ec86c4e52875b96`  
		Last Modified: Tue, 11 Mar 2025 17:57:55 GMT  
		Size: 2.4 MB (2445779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75812ce7e6faeac9f155572a45cf123cbdd70e5b95acfddba94dc660c63a8623`  
		Last Modified: Tue, 11 Mar 2025 17:57:55 GMT  
		Size: 18.6 KB (18567 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:e1ef335fd130382458b20d8bb50c3efc703858047f409f0587881c30b07b3f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252911275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd097551e97f865131278cf0bc654bee925f601e0565ad80ae74220108f03d35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 11 Mar 2025 00:06:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.4-linux-x86_64.tar.gz'; 			sha256='fb3d3c5fccef82158a70677c0044ac5ae40410eceb0604cdc8e643eeff21df8d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.4-linux-aarch64.tar.gz'; 			sha256='859f1a8cc4bce6911bc912f0e226a6ba2b1c144110b9d559d88f5077513d0e37'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.4-linux-i686.tar.gz'; 			sha256='0da3178ee5dacc1473e45c8c74838455252831f5d37483d716995742d3187e30'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.4-linux-ppc64le.tar.gz'; 			sha256='893f42cf47f58438d4d52a0eca3bcdf773dcf3681363d6fc24200c2ba8926286'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 00:06:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d06d63fe5b77e090fb1716bc0bf4b83f2392054dc3998fe2c050742dfeefd5`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 5.9 MB (5872106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd27c0378c35445527d2b66469ea87dcf9c095144704056bd9f4b7f6ce72429`  
		Last Modified: Tue, 11 Mar 2025 17:57:42 GMT  
		Size: 217.8 MB (217844207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfb350b81e2f393f116bb325a1bc6ea13b0929cdeb3bb6704328049c7d6418b`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:7bb6a82e605c460be44f3a45b87f26e8abc4eb5f98632ec26a6af80215813ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b181b76078511d00e90bf4b4afcc601d5ccade33038247be5015390746c5f72`

```dockerfile
```

-	Layers:
	-	`sha256:3839703f1aacaea993e3ab91203d69a093ace2da8023c940fc21b0ccc62e7baa`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 2.4 MB (2442529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a55d87603bca57de0480d83dc7216f4a0420bac6772636d073c5f8c4a3ae5556`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:b314c31b3cc543d19e37283eec96fc59768769db3bfbbefd08c88509254f4c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266934252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005f2e6519be575d63facce1e3dfdd01de9ecd5a923620bf519e46d2475ad268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 11 Mar 2025 00:06:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 11 Mar 2025 00:06:05 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 00:06:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.4-linux-x86_64.tar.gz'; 			sha256='fb3d3c5fccef82158a70677c0044ac5ae40410eceb0604cdc8e643eeff21df8d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.4-linux-aarch64.tar.gz'; 			sha256='859f1a8cc4bce6911bc912f0e226a6ba2b1c144110b9d559d88f5077513d0e37'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.4-linux-i686.tar.gz'; 			sha256='0da3178ee5dacc1473e45c8c74838455252831f5d37483d716995742d3187e30'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.4-linux-ppc64le.tar.gz'; 			sha256='893f42cf47f58438d4d52a0eca3bcdf773dcf3681363d6fc24200c2ba8926286'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 00:06:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 00:06:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c93a390612dd943c0e87e82b60fa07477135cb51cd54e204eb0dc9906d25b2`  
		Last Modified: Tue, 11 Mar 2025 18:06:33 GMT  
		Size: 6.2 MB (6249325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e2905179b467b1fbc14b4c84e0927b60f170ed19a1308fffd26cc76405cbbb`  
		Last Modified: Tue, 11 Mar 2025 18:06:39 GMT  
		Size: 228.6 MB (228632244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4af26c39439ba8719f8ec3aecb5c1911590cb2451a644f04903765ddabcf297`  
		Last Modified: Tue, 11 Mar 2025 18:06:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:a16dc4fa576b62c9bfdfbbcbafea6819751a7108674b33fc683de10bc388c859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69716412a55bec38efa9c09ed1c485b80a2dda7d22766875d05ef9446f8a1011`

```dockerfile
```

-	Layers:
	-	`sha256:3550e0e5b8a2762c5632aeb313cdf21328ee30bde9b83f75704b6a355aeddc9f`  
		Last Modified: Tue, 11 Mar 2025 18:06:33 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e02029b9a50374e5ce10784b6f760b548f3a07c600306aef4b0c559980fa62af`  
		Last Modified: Tue, 11 Mar 2025 18:06:33 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.3476; amd64

```console
$ docker pull julia@sha256:802388f92d0bbf7255a137144f8585c9a803acda8bc42a2a6b64d3985d3c3635
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 GB (3173800727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275b2acd98b73751584d6ab08bef0cd0d9244e704d549922417a67a3f9fbfcb4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 19:18:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 19:18:03 GMT
ENV JULIA_VERSION=1.11.4
# Wed, 12 Mar 2025 19:18:04 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Wed, 12 Mar 2025 19:18:06 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Wed, 12 Mar 2025 19:19:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:19:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf90ec15b3a941bc20ef48f0154930ca08ce03265e5168e2c0a92959707e2638`  
		Last Modified: Wed, 12 Mar 2025 19:19:20 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519faccc1c0f6bbe5ec6c3ece84b08c63c60e549ee7b9945b97b31113fd4f424`  
		Last Modified: Wed, 12 Mar 2025 19:19:19 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed31a36ee885bb4b3c52be3375f3efe98db930128da96d83fbf16b62fa4b320`  
		Last Modified: Wed, 12 Mar 2025 19:19:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152e6b3c43529daecbb6aafe1d0a99d66d2c00fe01b903d09ac45346f7d92b09`  
		Last Modified: Wed, 12 Mar 2025 19:19:19 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aef7aab92ed9cda3aea0d70ff5582a0e70a3c1ec10b1e0b80383b4732a6876`  
		Last Modified: Wed, 12 Mar 2025 19:19:59 GMT  
		Size: 265.1 MB (265146357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582dbe2668383dc1384492860b44d52092aa598848ef0aab775074836e7da1f0`  
		Last Modified: Wed, 12 Mar 2025 19:19:19 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.3328; amd64

```console
$ docker pull julia@sha256:b7e156aba083610d402c4deb76f4d0cfeb007cfa19fe247ed1508da984f235cb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2534985039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd056668a793e45ef8c7b40abfdf7a4dec7fc8672ce5e0ef6b2076937a27e49`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 19:25:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 19:25:58 GMT
ENV JULIA_VERSION=1.11.4
# Wed, 12 Mar 2025 19:25:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Wed, 12 Mar 2025 19:25:59 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Wed, 12 Mar 2025 19:27:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:27:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd17a49f6a739835ecc0588a2ee05921152a21b6254b17fe89eefc650672244d`  
		Last Modified: Wed, 12 Mar 2025 19:27:24 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2216df18b94860cde089178216a598fd88c9828c39340823a0d47e15014cd8cd`  
		Last Modified: Wed, 12 Mar 2025 19:27:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41306a625e141f7336a5eb1de893351034f4f0765f4f6fd84353eab11d45578c`  
		Last Modified: Wed, 12 Mar 2025 19:27:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f404eb1cccb63d04050cd1ca0711a31fea176087ebcf0fd868d1373664704532`  
		Last Modified: Wed, 12 Mar 2025 19:27:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadbacf47be8fb49f510a4d80bb9de78f38df0507aedaaa32f9614ce6e38a1dd`  
		Last Modified: Wed, 12 Mar 2025 19:27:58 GMT  
		Size: 265.0 MB (265037405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c647a37a1afbf0781145203ed926c5bd369d074b8a165bbb369bbbe096587db`  
		Last Modified: Wed, 12 Mar 2025 19:27:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.7009; amd64

```console
$ docker pull julia@sha256:82f581382655159903338b00e36f01556ea309b8813881e62a20a47cb8a09827
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2416666558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a68a2171d800af19c310edb6c485c6e695238862bc883aa12aafd0ea2db33e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:49:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:49:55 GMT
ENV JULIA_VERSION=1.11.4
# Wed, 12 Mar 2025 18:49:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Wed, 12 Mar 2025 18:49:57 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Wed, 12 Mar 2025 18:51:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:51:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6926468568f9dba2a26f9732388135773bea3cb569d51ab925d9831cf0cde9`  
		Last Modified: Wed, 12 Mar 2025 18:51:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef22978f7f51a1d14fc65783247fcb0bf9b5577d541e83f7e14724329db6703`  
		Last Modified: Wed, 12 Mar 2025 18:51:46 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6524557b573488cbbf88bc00de077e97ebee5abc14ffad0c05995ed545bf08ac`  
		Last Modified: Wed, 12 Mar 2025 18:51:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee78f577f70636d27c0565e28bce577555fcd6017e3f95392ce731c185886c73`  
		Last Modified: Wed, 12 Mar 2025 18:51:46 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7166bf71ef82c021c9fa8fdbf055250fe3a1f62f63db47e548a2c2793a282a`  
		Last Modified: Wed, 12 Mar 2025 18:52:21 GMT  
		Size: 265.0 MB (265025413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520fc9f949d30a4fe7d923f40a4e85d74c02e11ad57e1b7664e7439a695f0a5f`  
		Last Modified: Wed, 12 Mar 2025 18:51:46 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
