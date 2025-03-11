<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1-bookworm`](#julia1-bookworm)
-	[`julia:1-bullseye`](#julia1-bullseye)
-	[`julia:1-windowsservercore`](#julia1-windowsservercore)
-	[`julia:1-windowsservercore-1809`](#julia1-windowsservercore-1809)
-	[`julia:1-windowsservercore-ltsc2022`](#julia1-windowsservercore-ltsc2022)
-	[`julia:1-windowsservercore-ltsc2025`](#julia1-windowsservercore-ltsc2025)
-	[`julia:1.10`](#julia110)
-	[`julia:1.10-alpine`](#julia110-alpine)
-	[`julia:1.10-alpine3.20`](#julia110-alpine320)
-	[`julia:1.10-alpine3.21`](#julia110-alpine321)
-	[`julia:1.10-bookworm`](#julia110-bookworm)
-	[`julia:1.10-bullseye`](#julia110-bullseye)
-	[`julia:1.10-windowsservercore`](#julia110-windowsservercore)
-	[`julia:1.10-windowsservercore-1809`](#julia110-windowsservercore-1809)
-	[`julia:1.10-windowsservercore-ltsc2022`](#julia110-windowsservercore-ltsc2022)
-	[`julia:1.10-windowsservercore-ltsc2025`](#julia110-windowsservercore-ltsc2025)
-	[`julia:1.10.9`](#julia1109)
-	[`julia:1.10.9-alpine`](#julia1109-alpine)
-	[`julia:1.10.9-alpine3.20`](#julia1109-alpine320)
-	[`julia:1.10.9-alpine3.21`](#julia1109-alpine321)
-	[`julia:1.10.9-bookworm`](#julia1109-bookworm)
-	[`julia:1.10.9-bullseye`](#julia1109-bullseye)
-	[`julia:1.10.9-windowsservercore`](#julia1109-windowsservercore)
-	[`julia:1.10.9-windowsservercore-1809`](#julia1109-windowsservercore-1809)
-	[`julia:1.10.9-windowsservercore-ltsc2022`](#julia1109-windowsservercore-ltsc2022)
-	[`julia:1.10.9-windowsservercore-ltsc2025`](#julia1109-windowsservercore-ltsc2025)
-	[`julia:1.11`](#julia111)
-	[`julia:1.11-bookworm`](#julia111-bookworm)
-	[`julia:1.11-bullseye`](#julia111-bullseye)
-	[`julia:1.11-windowsservercore`](#julia111-windowsservercore)
-	[`julia:1.11-windowsservercore-1809`](#julia111-windowsservercore-1809)
-	[`julia:1.11-windowsservercore-ltsc2022`](#julia111-windowsservercore-ltsc2022)
-	[`julia:1.11-windowsservercore-ltsc2025`](#julia111-windowsservercore-ltsc2025)
-	[`julia:1.11.4`](#julia1114)
-	[`julia:1.11.4-bookworm`](#julia1114-bookworm)
-	[`julia:1.11.4-bullseye`](#julia1114-bullseye)
-	[`julia:1.11.4-windowsservercore`](#julia1114-windowsservercore)
-	[`julia:1.11.4-windowsservercore-1809`](#julia1114-windowsservercore-1809)
-	[`julia:1.11.4-windowsservercore-ltsc2022`](#julia1114-windowsservercore-ltsc2022)
-	[`julia:1.11.4-windowsservercore-ltsc2025`](#julia1114-windowsservercore-ltsc2025)
-	[`julia:bookworm`](#juliabookworm)
-	[`julia:bullseye`](#juliabullseye)
-	[`julia:latest`](#julialatest)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-1809`](#juliawindowsservercore-1809)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)
-	[`julia:windowsservercore-ltsc2025`](#juliawindowsservercore-ltsc2025)

## `julia:1`

```console
$ docker pull julia@sha256:3930bce3315aa328a039d06295aa25c759705b57b9946263ac8a817a2078a5cd
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
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1` - linux; amd64

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

### `julia:1` - unknown; unknown

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

### `julia:1` - linux; arm64 variant v8

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

### `julia:1` - unknown; unknown

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

### `julia:1` - linux; 386

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

### `julia:1` - unknown; unknown

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

### `julia:1` - linux; ppc64le

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

### `julia:1` - unknown; unknown

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

### `julia:1` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:8acf88f620e712a0a209bfbccf0eed2dcc0b2946508997213353097da27d170e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081734503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cc4c1f77bbe2ff3fc6f90bcc7f0b4d7d47e9aa0617b9c179e358c1eaf7baf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:13 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:13:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:13:15 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:14:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:14:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b580e80688f1e334734aea2880fa5931e55370f3539fc8e78058543d2fbb4`  
		Last Modified: Tue, 11 Mar 2025 18:14:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec1357c0e2eb61ac9298926dd9084156bd2d05dcea183ea8786979784c324`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a8e2f5c7e51683c21328502741d075647e87f5e9d195902a79b4362af9708`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a47c47f5f7ce9891789821dc08dbb73af7a03679e28d975173ca02457a3c85`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b401c362d821c447b22c6303f6e897b6cc2098aab4b7061cdd239ad38f00356`  
		Last Modified: Tue, 11 Mar 2025 18:15:03 GMT  
		Size: 265.1 MB (265140438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a26224618776b48b976e6718b0c66dc407c2f1423a2a911b49b31fa347919`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:4ec46cc1e5ec14205a112b7bcf25d17feb1195c4427bea62804de7c93aa1d464
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528934099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdb17d614282c158734ba03f7db6e9dc4b123d2b2fa012b800e11be2b66dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e613cb0bd6b9cdefc91ef48f6b84eafc8bfedc674b985f05222969a1e708d2`  
		Last Modified: Tue, 11 Mar 2025 18:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55928cd0613a4698f021e84a732f32008287c1079893322ef0577d3b68e1d7e3`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769b36b1b267ac98d3c0b181635a870dbbb219e2ce05ed2bc0e25172e009aaa`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc75c329d096e43a1095e057c53bce7d7b5fa96ca5a61ad0a496b1e89bd34f`  
		Last Modified: Tue, 11 Mar 2025 18:11:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de433e53b119c1cea9de09b3637d6600006b928c83e8554570ae155ad81392d0`  
		Last Modified: Tue, 11 Mar 2025 18:11:58 GMT  
		Size: 265.1 MB (265069668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734d83e3be039a110407a2e7cd36a59ad3f092bf4f426da5936550ea2e7e933`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:399302474cb5ef2ccf216c1c73c97c7bf0a39666c35c6d80ef67ba01fb6aa3ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1-bookworm` - linux; amd64

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

### `julia:1-bookworm` - unknown; unknown

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

### `julia:1-bookworm` - linux; arm64 variant v8

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

### `julia:1-bookworm` - unknown; unknown

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

### `julia:1-bookworm` - linux; 386

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

### `julia:1-bookworm` - unknown; unknown

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

### `julia:1-bookworm` - linux; ppc64le

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

### `julia:1-bookworm` - unknown; unknown

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

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:8a5776a35daa3f5821996974b6bfccbca0acb93c57adb7be66f808fd48601b35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:72c9ae493b9eca82f0c07a276f2f0b4f7863d119474f66f8586eefa0a8053ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300961401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c67a903937f5891a72c30c6adc5ed4626c951909fa33c301f1aa5aa4c45948`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7165c83944224063d633634d136cf1bf62f390d866ccb2ae699c012548aac6`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 2.2 MB (2222654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725e528a3666541c2953691421b6a228673594440c7d539fb35f71fc2a46be48`  
		Last Modified: Tue, 11 Mar 2025 17:58:00 GMT  
		Size: 268.5 MB (268484444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d38f27ed12d5f890c2121a4a56d39f8767d3f6cbb1c14d39ddfbb22f45e415`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8a02228943143116153ce0d2488cd203e6ce948bb248949bcb0429c8686408b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91301a3221f1b9ae49dc24f7c05ad6161194f3e57f108ca52589d84115267526`

```dockerfile
```

-	Layers:
	-	`sha256:fc3a810a8f575b0ac14f3c720fac7a97fde163cba0299bdb59633c6e09cd7717`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7391d4ac599c40348906465dcc052d096f6db456615fe307bd2b39cb79da36c5`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dc6141754eb15dc1abb94a4e67d1c698f01f879691520bdc23842d794c80adda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (314957093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f10b2054506b5f7fbdf5f4b4cc409f99caaf7ba0559d1ce43fcad496c62ed92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc5dc01c337dce742e7c6026ccf096f7b1c09278ca05a29613e61d8fe553208`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 2.2 MB (2210309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47705c544b0c43fa505ea4141d20e1bd7047b8da8398c7a5e3d1214f40573e1`  
		Last Modified: Tue, 11 Mar 2025 17:59:35 GMT  
		Size: 284.0 MB (284000422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e906007b13ae7c53726d61e1006d643af01db9a126dcf54f834921cca9a146a`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:063ec1c56311e72dc3969d58c12069c7431f9663a075fb5fbca0ecea6b4fadb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8736a85ebdb295f549dc129bf2389633fae54193cc5512562d7d6452465fdb`

```dockerfile
```

-	Layers:
	-	`sha256:f153b82ac16be75d5ce35c461d4642790760c612f40500aba30fd809ff482f9d`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3990310fdd52100587e443fc54cd91ffdd102077037c0b0003599851c0c10ca7`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:415eda97c01612223e23e19484ef8c99744317636dc5c495c6a3ce456ce2c57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251354410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a238940033d7286786b0a0ebdb5f1de9242b3576a705221eccc3e647c6a3a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768dc8869224f294d9e2ae8231a8c8a74f708a8e5495e183d94dfbedf98d3816`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 2.3 MB (2328071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e4bd659adb5b6bdf7cd848dd04bdd531234e9725242266aa53357febdcb23a`  
		Last Modified: Tue, 11 Mar 2025 17:57:47 GMT  
		Size: 217.8 MB (217845544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706ff1c0df0fa586527b601c6e9c2b526f2521b19a51b12649fedbc429419671`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:257c12809f8a9b581f7dde263775c80db30df53d4fcf13cd4fd1820599b3ce66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0464719ad93ca07e66b0669a89f783025f238fad94ecff01f027d6f292c6ea`

```dockerfile
```

-	Layers:
	-	`sha256:e12e0dd0133063f2b20338f66514bc5628916b5506a86b7491ad172daa119aab`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b13c04845b43675f6fc2c6eb60313e14e089c471deb5b03bff80a58579050c65`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 17.2 KB (17195 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:558e56296c78e7898fafefc944345bcb81b21a48f6137d1b8c9a74322b32c243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1-windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:8acf88f620e712a0a209bfbccf0eed2dcc0b2946508997213353097da27d170e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081734503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cc4c1f77bbe2ff3fc6f90bcc7f0b4d7d47e9aa0617b9c179e358c1eaf7baf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:13 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:13:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:13:15 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:14:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:14:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b580e80688f1e334734aea2880fa5931e55370f3539fc8e78058543d2fbb4`  
		Last Modified: Tue, 11 Mar 2025 18:14:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec1357c0e2eb61ac9298926dd9084156bd2d05dcea183ea8786979784c324`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a8e2f5c7e51683c21328502741d075647e87f5e9d195902a79b4362af9708`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a47c47f5f7ce9891789821dc08dbb73af7a03679e28d975173ca02457a3c85`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b401c362d821c447b22c6303f6e897b6cc2098aab4b7061cdd239ad38f00356`  
		Last Modified: Tue, 11 Mar 2025 18:15:03 GMT  
		Size: 265.1 MB (265140438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a26224618776b48b976e6718b0c66dc407c2f1423a2a911b49b31fa347919`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:4ec46cc1e5ec14205a112b7bcf25d17feb1195c4427bea62804de7c93aa1d464
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528934099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdb17d614282c158734ba03f7db6e9dc4b123d2b2fa012b800e11be2b66dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e613cb0bd6b9cdefc91ef48f6b84eafc8bfedc674b985f05222969a1e708d2`  
		Last Modified: Tue, 11 Mar 2025 18:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55928cd0613a4698f021e84a732f32008287c1079893322ef0577d3b68e1d7e3`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769b36b1b267ac98d3c0b181635a870dbbb219e2ce05ed2bc0e25172e009aaa`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc75c329d096e43a1095e057c53bce7d7b5fa96ca5a61ad0a496b1e89bd34f`  
		Last Modified: Tue, 11 Mar 2025 18:11:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de433e53b119c1cea9de09b3637d6600006b928c83e8554570ae155ad81392d0`  
		Last Modified: Tue, 11 Mar 2025 18:11:58 GMT  
		Size: 265.1 MB (265069668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734d83e3be039a110407a2e7cd36a59ad3f092bf4f426da5936550ea2e7e933`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:f6329f6ba2acb70fa9e6ebbc91d4d536d0672c1f7305a02fbbef863042afb5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:48b3643c0c3cd7f12c11619010332d97e6a3023a78fd6e385b1ee9934378d93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:4ec46cc1e5ec14205a112b7bcf25d17feb1195c4427bea62804de7c93aa1d464
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528934099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdb17d614282c158734ba03f7db6e9dc4b123d2b2fa012b800e11be2b66dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e613cb0bd6b9cdefc91ef48f6b84eafc8bfedc674b985f05222969a1e708d2`  
		Last Modified: Tue, 11 Mar 2025 18:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55928cd0613a4698f021e84a732f32008287c1079893322ef0577d3b68e1d7e3`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769b36b1b267ac98d3c0b181635a870dbbb219e2ce05ed2bc0e25172e009aaa`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc75c329d096e43a1095e057c53bce7d7b5fa96ca5a61ad0a496b1e89bd34f`  
		Last Modified: Tue, 11 Mar 2025 18:11:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de433e53b119c1cea9de09b3637d6600006b928c83e8554570ae155ad81392d0`  
		Last Modified: Tue, 11 Mar 2025 18:11:58 GMT  
		Size: 265.1 MB (265069668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734d83e3be039a110407a2e7cd36a59ad3f092bf4f426da5936550ea2e7e933`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:77810f8d3cfceabad6bc16d6a389038ef89b0aca5c3042647606edd4eb74e52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:8acf88f620e712a0a209bfbccf0eed2dcc0b2946508997213353097da27d170e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081734503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cc4c1f77bbe2ff3fc6f90bcc7f0b4d7d47e9aa0617b9c179e358c1eaf7baf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:13 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:13:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:13:15 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:14:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:14:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b580e80688f1e334734aea2880fa5931e55370f3539fc8e78058543d2fbb4`  
		Last Modified: Tue, 11 Mar 2025 18:14:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec1357c0e2eb61ac9298926dd9084156bd2d05dcea183ea8786979784c324`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a8e2f5c7e51683c21328502741d075647e87f5e9d195902a79b4362af9708`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a47c47f5f7ce9891789821dc08dbb73af7a03679e28d975173ca02457a3c85`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b401c362d821c447b22c6303f6e897b6cc2098aab4b7061cdd239ad38f00356`  
		Last Modified: Tue, 11 Mar 2025 18:15:03 GMT  
		Size: 265.1 MB (265140438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a26224618776b48b976e6718b0c66dc407c2f1423a2a911b49b31fa347919`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:64e97f858e608dbaf724bbbece77e03dc3058bcc244a61ba4e45f225d75e6c17
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
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:8b0b59d70d25ad404428e8486e74afde1d1a77e89502c355243565a7fb15d7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210425312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19a74370a82c72f6745fd426077618ce3740e98bd26c71f8f55b467d24b6f16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfc3dde3fd3040765e99ffc81d694b63ceb83d88acea588c3e78f70a6eb445c`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 5.7 MB (5713109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6070c34eb6800f6d9580d96eb86c7a2f9722ac29ab738415b85c44f12f135ba`  
		Last Modified: Tue, 11 Mar 2025 17:57:38 GMT  
		Size: 176.5 MB (176492533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892b3a2797f3020dd1cf49bf0a76ad36b933f70ae42432ebc5f3ffdfa9229c02`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:bffe6578ba0212569be14de5faf69c4af7ced3088ccf16fa916f318b104b440b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93e022a9b68075d114f8dee364b9951705dcd950490a2ea8c5da13f653d4827`

```dockerfile
```

-	Layers:
	-	`sha256:a41409be7d8ea6d673173ccbfb1e9028f19103f93cdc87be50425104194df821`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 2.4 MB (2445501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f8fec7de9ee60a632fef43c99cc831b39c40c1302fa4de539cf5b053744fae2`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 17.2 KB (17213 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f33030be0ee76820af5d911dcd32a0d1b97a3594f787f6d78586c86633492abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210862164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8017f21911655a08fb3600e729a5cd8541b3f931cb8ba42639fc7388e5475eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
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
	-	`sha256:46834ae3839a09815ec69233743ecfc9832db91a32485080ffb99af8be0ef2bf`  
		Last Modified: Tue, 11 Mar 2025 18:00:39 GMT  
		Size: 177.3 MB (177275248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab774d07ab7f63d48bb4a973b081c6f1e4d102cbbd0a0bb3faf456a907722e0`  
		Last Modified: Tue, 11 Mar 2025 18:00:34 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:8589227b1d465fae3685376827a4d750abe2560addd1d5707bb4e0462285c70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddb5602e2af30ea4bf35f790e37c2f6097fb5915ab8b0a9cc0582181cb1f5f5`

```dockerfile
```

-	Layers:
	-	`sha256:e953707a8312de0f8cccb7494265711bf518ba696d66785d43898471752cd611`  
		Last Modified: Tue, 11 Mar 2025 18:00:34 GMT  
		Size: 2.4 MB (2444545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df08f09be34090691176e4fbab8f7e83a9048ac57cabefba8dbc98eef377ec18`  
		Last Modified: Tue, 11 Mar 2025 18:00:34 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:de661161c1ece613b1030880da247ad6aec649e9a1610d95bbaa62d0b7d5f979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192823403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65c0ccc81974eee6b02c4c0e6fd8aee62c6e98eec95f4e174f68bea19d9b050`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad1046056eddfa74f5394894757c881bbf2cb01ef448af3d2020ed37c5882bd`  
		Last Modified: Tue, 11 Mar 2025 17:57:40 GMT  
		Size: 5.9 MB (5872032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f740f0d2db8cfc8a9465e690bc54c8ccc7083e41f7ee81284f69180e5555e426`  
		Last Modified: Tue, 11 Mar 2025 17:57:44 GMT  
		Size: 157.8 MB (157756408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a31e5bd03ee7113898e0824ace082e847618d5de5ec4d8a7072308cf7a786d`  
		Last Modified: Tue, 11 Mar 2025 17:57:39 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:97b55c239880540424f4e77a5b0fd9d35e5db7acb23d3040b5b2e7ae52ff43b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdb69cd1a95eba4262e022c6d861fca6c5648252cf51ffa5178cff9416f686d`

```dockerfile
```

-	Layers:
	-	`sha256:881f4f97440ef8d3651bbf686f00f7ba0ee3648d6a1003518a35fde07d7cf5f6`  
		Last Modified: Tue, 11 Mar 2025 17:57:39 GMT  
		Size: 2.4 MB (2442594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c01afa785c68a5852cdabdc2e65d5be13de11546af018ee7c40218072dda4ae`  
		Last Modified: Tue, 11 Mar 2025 17:57:39 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:f96f1de1b1836c0bd0923a9db025a40bc6da908b494dee681d5b1130b548566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193588610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5764f98f1c7d5e558bf92aa0052c5ef898911ab412f7a2ff005529c1e081802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
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
	-	`sha256:62c8b46c3aa2c0351fdc38df3a419c00ad9433827e45971822caa3fe02edcae4`  
		Last Modified: Tue, 11 Mar 2025 18:08:48 GMT  
		Size: 155.3 MB (155286603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a97a864525b59fba4a1137860dca62feffc62ae2c32e0754f0fbe9aa94993d7`  
		Last Modified: Tue, 11 Mar 2025 18:08:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:5bfc0698770e23eb7f5708c258256fc1f4eec2b42c2b04c25cb746d0e050e11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ed690a6028d6bf71be20aefeb2faf90a6c0db3199c2b2f3eaf61ceddceaf74`

```dockerfile
```

-	Layers:
	-	`sha256:2110249f1dde77e879f5260ca2e5ddeaa7cc0f53945892068dc0d87e3c795077`  
		Last Modified: Tue, 11 Mar 2025 18:08:43 GMT  
		Size: 2.4 MB (2448678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52bcc79f567d3332d8b6e78848a51afee62fc04798bc7638cca9fa90ace46823`  
		Last Modified: Tue, 11 Mar 2025 18:08:42 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:446b532f2f2d95c4d92d43c3c53cf272635ddc41d61432c91fe4c8e073a4d5ca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3005350438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8d63d6aab22ac6cdcce7c795a4e6eb4a643e53b0ae54e32f786245fa525eaa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:06 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:13:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:13:07 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:13:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:13:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97123365fbddeee79f4b37f0c2695f00f6dff271674dcc2aa0bb753115e86d5c`  
		Last Modified: Tue, 11 Mar 2025 18:13:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33faa754f1c2ecb18d865f3f93ea7e9a9df4166725c41c075d8019f6927ccbe0`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218a8ee7842459c03202660309caa82ba9054b2ba7c1a61667708244b4bf868e`  
		Last Modified: Tue, 11 Mar 2025 18:13:57 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af43409c1d69dc82793654c3ad5ca25ce2a9b7f452c4febd48bf1d6afa2b8fb7`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a015971492e83a7d992dca3d44be0ef46cf25792a6163774724a3abf3e0091`  
		Last Modified: Tue, 11 Mar 2025 18:14:24 GMT  
		Size: 188.8 MB (188756293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de15ab10ea3df45c2660f02a68d9f93a8f1d0e9ac1e281fbb7256875d9bdc86`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:a714a2d227085380226a475fd4f8d87347d68deaa39c380bb8a39f5c47904599
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452575686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337ca17c5313826be0d9e2d8ad00dc04fb82ddb265913b3aa849973c2ad0df9f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:42 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:08:43 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:08:44 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:10:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:10:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca70396628086048ee435c5ea681c12a42f47c964a13fe4681a4142eb46f309c`  
		Last Modified: Tue, 11 Mar 2025 18:10:37 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd558c6ded40bc493214da6479f570a8a1f055cb9c677cd5f7b91e3ea030717f`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8fd327b091fd9c321aab4a5cc14fe7ba146e31ad38ec90ddb17b747d004f02`  
		Last Modified: Tue, 11 Mar 2025 18:10:35 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cc8ade5c4bb6f4924ae74a69bf14226c81352e032d226089078877f358bab3`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfdbb42798cec7b45028bbbf24a756fd93aa29f7682d53444badad3327d42b8`  
		Last Modified: Tue, 11 Mar 2025 18:10:58 GMT  
		Size: 188.7 MB (188711229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f9ba9ed5eded42ca0c770f523700c989f3ea05f8439aa2ad1b5acea030ac99`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:f41ce426b1226aad6dd2d3ee6ff0b10c9d24cf47e6258311b2821f03dcc3cb2d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325602338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7e1311d7c0913449f35cd2c834f43dd87f148685605f0aa78ded3b82a81f96`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:08:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:08:48 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:11:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a17a83c8ddb404c7098a5aff94e15880eb3e16310d14f48dee3027f5b8906e`  
		Last Modified: Tue, 11 Mar 2025 18:11:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330cfaaf7f45b162bfd993005821d6c0d29b9d40f9cc38016259f97f204c767`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546e90a888c88a3d48ab94f1a6daa0cc58b6cc4c1a5ce5d754577881dd0c8d46`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de1d5b3f1bc550bf5fd4eb65cbaee826a9d9be6c3b03c5e87cc429ad24c95a4`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08945d1f42ec7c107909cb258eb71a398a305af6b9b17e538dac289a9a4c3d64`  
		Last Modified: Tue, 11 Mar 2025 18:11:56 GMT  
		Size: 188.7 MB (188687047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde799d583621d42ac5b6f311ccbcf1aa015989a8f6ce4646342e908c71f73d8`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-alpine`

```console
$ docker pull julia@sha256:8e4ffc534ac11fe111200ebab165d7a261bfba9d29fcc04a04aa7c2bd31b118c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:05deda0ce568e7a486b0fc78655b9bef56733d5cfcd208798402f88226a6c561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182007528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f25ad31514dea1aabdc59453a663a229195e7149590fc1a5847f0af9cc85253`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.9-musl-x86_64.tar.gz'; 			sha256='db7454a7acf677598c23216eb4798d0b0ebc6be7c7d03ea2e7ee10f7a5985a64'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc378e9762465cbab26df40725a9ecfe34e926aaf564feddb91cc95c13de7b28`  
		Last Modified: Tue, 11 Mar 2025 17:57:44 GMT  
		Size: 178.4 MB (178364914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4520b8b4e112fc364be7582ee2b4ca8061b8052366dd86efaf248e566205e5`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:2223de82816678d7a5d22c595d7f20df940a4c8fa334c4e873afbc9e4bbd6661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 KB (92467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4525c47a13d5dcf6cdcf5eb0a1782ec015ee9d67036a9c66416fc7df4c675636`

```dockerfile
```

-	Layers:
	-	`sha256:cd6f6fd2d3a0b982ec6c85d31fd7ed1b92c51d681a819bb033ad45cd64fa41d2`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 79.9 KB (79887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8be5f503861b92fe7dbe4f2f3ee14b81ddf62127c3b8ee5309c746073e18aac0`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.20`

```console
$ docker pull julia@sha256:81f5bc3f2a97bea0882aaf015bb3de2be43df79b24ada259ad76f91daea7ed45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:9131fd82410f167efb10f0d16d426f9e6f39afa1aeca0fccfbaacb1204f4a7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181991132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0985fdedfd97d7aa5f5474cf3e4678ff6df6e85b96f910e5cf2cddd3450f7ba8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.9-musl-x86_64.tar.gz'; 			sha256='db7454a7acf677598c23216eb4798d0b0ebc6be7c7d03ea2e7ee10f7a5985a64'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71785e30ec36ae8f1c1bfa80a151812603ffd7422c6ac8648c8ea8c50ede4b14`  
		Last Modified: Tue, 11 Mar 2025 17:57:32 GMT  
		Size: 178.4 MB (178363869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9475bb49640359a1dbb9b7deadb033831e371dbe2cd9c974e711e56057c0e4`  
		Last Modified: Tue, 11 Mar 2025 17:57:29 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:6ac78f52fab40551ab05791c769648be90f88c3b9f3b7113a8f82f964f9e3504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54c9cec2429055f41565bfda85c251e0c44c54202420c168d84584ca64ce9b8`

```dockerfile
```

-	Layers:
	-	`sha256:5615806ab6fdc8c53b4cf2fcac1cef95a8f764b5ba4d7b18a1a08998c3413470`  
		Last Modified: Tue, 11 Mar 2025 17:57:29 GMT  
		Size: 73.5 KB (73545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:715651ac7e91e91b53873a3398a8d77dcf1560c954704458e18deb5898e67aa1`  
		Last Modified: Tue, 11 Mar 2025 17:57:29 GMT  
		Size: 12.0 KB (11964 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.21`

```console
$ docker pull julia@sha256:8e4ffc534ac11fe111200ebab165d7a261bfba9d29fcc04a04aa7c2bd31b118c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:05deda0ce568e7a486b0fc78655b9bef56733d5cfcd208798402f88226a6c561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182007528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f25ad31514dea1aabdc59453a663a229195e7149590fc1a5847f0af9cc85253`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.9-musl-x86_64.tar.gz'; 			sha256='db7454a7acf677598c23216eb4798d0b0ebc6be7c7d03ea2e7ee10f7a5985a64'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc378e9762465cbab26df40725a9ecfe34e926aaf564feddb91cc95c13de7b28`  
		Last Modified: Tue, 11 Mar 2025 17:57:44 GMT  
		Size: 178.4 MB (178364914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4520b8b4e112fc364be7582ee2b4ca8061b8052366dd86efaf248e566205e5`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:2223de82816678d7a5d22c595d7f20df940a4c8fa334c4e873afbc9e4bbd6661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 KB (92467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4525c47a13d5dcf6cdcf5eb0a1782ec015ee9d67036a9c66416fc7df4c675636`

```dockerfile
```

-	Layers:
	-	`sha256:cd6f6fd2d3a0b982ec6c85d31fd7ed1b92c51d681a819bb033ad45cd64fa41d2`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 79.9 KB (79887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8be5f503861b92fe7dbe4f2f3ee14b81ddf62127c3b8ee5309c746073e18aac0`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:a38cfecb98b3454159eb9e422e89632d6f03447cd8966f8f5ec529c28c37fdc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:8b0b59d70d25ad404428e8486e74afde1d1a77e89502c355243565a7fb15d7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210425312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19a74370a82c72f6745fd426077618ce3740e98bd26c71f8f55b467d24b6f16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfc3dde3fd3040765e99ffc81d694b63ceb83d88acea588c3e78f70a6eb445c`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 5.7 MB (5713109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6070c34eb6800f6d9580d96eb86c7a2f9722ac29ab738415b85c44f12f135ba`  
		Last Modified: Tue, 11 Mar 2025 17:57:38 GMT  
		Size: 176.5 MB (176492533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892b3a2797f3020dd1cf49bf0a76ad36b933f70ae42432ebc5f3ffdfa9229c02`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:bffe6578ba0212569be14de5faf69c4af7ced3088ccf16fa916f318b104b440b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93e022a9b68075d114f8dee364b9951705dcd950490a2ea8c5da13f653d4827`

```dockerfile
```

-	Layers:
	-	`sha256:a41409be7d8ea6d673173ccbfb1e9028f19103f93cdc87be50425104194df821`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 2.4 MB (2445501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f8fec7de9ee60a632fef43c99cc831b39c40c1302fa4de539cf5b053744fae2`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 17.2 KB (17213 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f33030be0ee76820af5d911dcd32a0d1b97a3594f787f6d78586c86633492abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210862164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8017f21911655a08fb3600e729a5cd8541b3f931cb8ba42639fc7388e5475eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
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
	-	`sha256:46834ae3839a09815ec69233743ecfc9832db91a32485080ffb99af8be0ef2bf`  
		Last Modified: Tue, 11 Mar 2025 18:00:39 GMT  
		Size: 177.3 MB (177275248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab774d07ab7f63d48bb4a973b081c6f1e4d102cbbd0a0bb3faf456a907722e0`  
		Last Modified: Tue, 11 Mar 2025 18:00:34 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8589227b1d465fae3685376827a4d750abe2560addd1d5707bb4e0462285c70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddb5602e2af30ea4bf35f790e37c2f6097fb5915ab8b0a9cc0582181cb1f5f5`

```dockerfile
```

-	Layers:
	-	`sha256:e953707a8312de0f8cccb7494265711bf518ba696d66785d43898471752cd611`  
		Last Modified: Tue, 11 Mar 2025 18:00:34 GMT  
		Size: 2.4 MB (2444545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df08f09be34090691176e4fbab8f7e83a9048ac57cabefba8dbc98eef377ec18`  
		Last Modified: Tue, 11 Mar 2025 18:00:34 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:de661161c1ece613b1030880da247ad6aec649e9a1610d95bbaa62d0b7d5f979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192823403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65c0ccc81974eee6b02c4c0e6fd8aee62c6e98eec95f4e174f68bea19d9b050`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad1046056eddfa74f5394894757c881bbf2cb01ef448af3d2020ed37c5882bd`  
		Last Modified: Tue, 11 Mar 2025 17:57:40 GMT  
		Size: 5.9 MB (5872032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f740f0d2db8cfc8a9465e690bc54c8ccc7083e41f7ee81284f69180e5555e426`  
		Last Modified: Tue, 11 Mar 2025 17:57:44 GMT  
		Size: 157.8 MB (157756408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a31e5bd03ee7113898e0824ace082e847618d5de5ec4d8a7072308cf7a786d`  
		Last Modified: Tue, 11 Mar 2025 17:57:39 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:97b55c239880540424f4e77a5b0fd9d35e5db7acb23d3040b5b2e7ae52ff43b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdb69cd1a95eba4262e022c6d861fca6c5648252cf51ffa5178cff9416f686d`

```dockerfile
```

-	Layers:
	-	`sha256:881f4f97440ef8d3651bbf686f00f7ba0ee3648d6a1003518a35fde07d7cf5f6`  
		Last Modified: Tue, 11 Mar 2025 17:57:39 GMT  
		Size: 2.4 MB (2442594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c01afa785c68a5852cdabdc2e65d5be13de11546af018ee7c40218072dda4ae`  
		Last Modified: Tue, 11 Mar 2025 17:57:39 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:f96f1de1b1836c0bd0923a9db025a40bc6da908b494dee681d5b1130b548566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193588610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5764f98f1c7d5e558bf92aa0052c5ef898911ab412f7a2ff005529c1e081802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
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
	-	`sha256:62c8b46c3aa2c0351fdc38df3a419c00ad9433827e45971822caa3fe02edcae4`  
		Last Modified: Tue, 11 Mar 2025 18:08:48 GMT  
		Size: 155.3 MB (155286603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a97a864525b59fba4a1137860dca62feffc62ae2c32e0754f0fbe9aa94993d7`  
		Last Modified: Tue, 11 Mar 2025 18:08:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5bfc0698770e23eb7f5708c258256fc1f4eec2b42c2b04c25cb746d0e050e11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ed690a6028d6bf71be20aefeb2faf90a6c0db3199c2b2f3eaf61ceddceaf74`

```dockerfile
```

-	Layers:
	-	`sha256:2110249f1dde77e879f5260ca2e5ddeaa7cc0f53945892068dc0d87e3c795077`  
		Last Modified: Tue, 11 Mar 2025 18:08:43 GMT  
		Size: 2.4 MB (2448678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52bcc79f567d3332d8b6e78848a51afee62fc04798bc7638cca9fa90ace46823`  
		Last Modified: Tue, 11 Mar 2025 18:08:42 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bullseye`

```console
$ docker pull julia@sha256:26b265a6e2a5bb710814762459f6a3adf4cb16031d8a20ff5590b0b67594d7e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:a359bc7048257d6d14d332482447142f9ff65f8b61b812733263979498904593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (208970883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c058bb2161080c08c4a1c2605abce277908069e532b9e8cfbbfa66aca6c395`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430b039f93073c03482645206793f4d953e78de8d00f5d1d5c1bc8ab34e118ec`  
		Last Modified: Tue, 11 Mar 2025 17:57:45 GMT  
		Size: 2.2 MB (2222651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4404939bfc543c9749b9c47addd8ef29ed082979cdb85e748d12bba35fc7f2dc`  
		Last Modified: Tue, 11 Mar 2025 17:57:49 GMT  
		Size: 176.5 MB (176493928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c6680b3af4d305df03b38964b8f08b92e7df82967a5441aa875f10a8575224`  
		Last Modified: Tue, 11 Mar 2025 17:57:44 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:6049e9318a2b539969e6d340d4ac631d5a0cc600cfa1afbf715c5add0e678d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d3dde32990671ef2c80f62a55d30490c034da5d2fbdb85e938a3cf5cd9fb6a`

```dockerfile
```

-	Layers:
	-	`sha256:02a3276015fbc18fcd763f574041640f1d1b20e1ef7f871b01bfdb10986461ff`  
		Last Modified: Tue, 11 Mar 2025 17:57:45 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5193f8373a94eec6c560fa126be877bd84e52a4877e663fdd6971044dab29f2e`  
		Last Modified: Tue, 11 Mar 2025 17:57:44 GMT  
		Size: 16.6 KB (16625 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:bf15aea11334363726c621ddce60a1890e8648bb77367c9c2c8bb53dd3e6758f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208231962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7308e7f3fb0bacd82050242ca33406839ef21b3e4996941632ce3f98b4aeaed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc5dc01c337dce742e7c6026ccf096f7b1c09278ca05a29613e61d8fe553208`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 2.2 MB (2210309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e70fdfc06723ceb275af0e9e09f8be51bf723c58761f8f3ecb0ae4fffddff7`  
		Last Modified: Tue, 11 Mar 2025 18:01:38 GMT  
		Size: 177.3 MB (177275295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d642bb0ce5f955ccb4b7302b0d9297295b15a397570517e08b1484ad84814e1d`  
		Last Modified: Tue, 11 Mar 2025 18:01:33 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:4d7a5cdb49528c2af835f0e91c20e51c0ca171eb0a147e691012e72dee4b1a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a631687d0a2377e4da2424c12fb57a59996cd86dc1b06d06898f75c704c74d`

```dockerfile
```

-	Layers:
	-	`sha256:878f8fec3dee010a4a5e3b0d77074587964d959a0754edd043f8f1fc23120e42`  
		Last Modified: Tue, 11 Mar 2025 18:01:33 GMT  
		Size: 2.7 MB (2712181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee8c33359dc7d305e61c7de3255800385e7898052e6d852e89d1be25f06950e`  
		Last Modified: Tue, 11 Mar 2025 18:01:33 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; 386

```console
$ docker pull julia@sha256:37d7fcbd4245247644a59a4c45e0748d8af7d7288683c4c72d485fcd6161c000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191265287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ea07724114db9957b20dd858bb23a65a080b695c8b560869bca85f82b68d37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578b5ac6328415549e35f4b2b368227d2fcac715b85c2919af7537f87ae610b6`  
		Last Modified: Tue, 11 Mar 2025 17:57:33 GMT  
		Size: 2.3 MB (2328059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573ebe960fc2da6002de3ed24efaefc7bd3c69998e20e9d4b03bd1e61191486e`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 157.8 MB (157756432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f140ecd12f3dd3f8a39e95a29e5d9de5575a70ba53fa59ffd659154e099150b`  
		Last Modified: Tue, 11 Mar 2025 17:57:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:16628feb8c2cfb9bf19f0b3ae88b2a9cd83cde2e2e3530392530380044c3e0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96cca7d128b27d6cfd8e5848c8c1b94f7b76ef644d8325d43c23a3b4220daff`

```dockerfile
```

-	Layers:
	-	`sha256:6ba51ee3834a88c46a90578cb672c323f01931b57f705dbec0df26b5d4a49ee1`  
		Last Modified: Tue, 11 Mar 2025 17:57:32 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65abb8f99a69871222c2324f5e79f1b5516b4e431dec9e174b3ccc0a65ebc009`  
		Last Modified: Tue, 11 Mar 2025 17:57:32 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:1a1cd97e99d8602ead0c527f352adf9fd27d9d80446ef00e12f1b8a707935617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:446b532f2f2d95c4d92d43c3c53cf272635ddc41d61432c91fe4c8e073a4d5ca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3005350438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8d63d6aab22ac6cdcce7c795a4e6eb4a643e53b0ae54e32f786245fa525eaa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:06 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:13:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:13:07 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:13:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:13:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97123365fbddeee79f4b37f0c2695f00f6dff271674dcc2aa0bb753115e86d5c`  
		Last Modified: Tue, 11 Mar 2025 18:13:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33faa754f1c2ecb18d865f3f93ea7e9a9df4166725c41c075d8019f6927ccbe0`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218a8ee7842459c03202660309caa82ba9054b2ba7c1a61667708244b4bf868e`  
		Last Modified: Tue, 11 Mar 2025 18:13:57 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af43409c1d69dc82793654c3ad5ca25ce2a9b7f452c4febd48bf1d6afa2b8fb7`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a015971492e83a7d992dca3d44be0ef46cf25792a6163774724a3abf3e0091`  
		Last Modified: Tue, 11 Mar 2025 18:14:24 GMT  
		Size: 188.8 MB (188756293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de15ab10ea3df45c2660f02a68d9f93a8f1d0e9ac1e281fbb7256875d9bdc86`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:a714a2d227085380226a475fd4f8d87347d68deaa39c380bb8a39f5c47904599
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452575686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337ca17c5313826be0d9e2d8ad00dc04fb82ddb265913b3aa849973c2ad0df9f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:42 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:08:43 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:08:44 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:10:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:10:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca70396628086048ee435c5ea681c12a42f47c964a13fe4681a4142eb46f309c`  
		Last Modified: Tue, 11 Mar 2025 18:10:37 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd558c6ded40bc493214da6479f570a8a1f055cb9c677cd5f7b91e3ea030717f`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8fd327b091fd9c321aab4a5cc14fe7ba146e31ad38ec90ddb17b747d004f02`  
		Last Modified: Tue, 11 Mar 2025 18:10:35 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cc8ade5c4bb6f4924ae74a69bf14226c81352e032d226089078877f358bab3`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfdbb42798cec7b45028bbbf24a756fd93aa29f7682d53444badad3327d42b8`  
		Last Modified: Tue, 11 Mar 2025 18:10:58 GMT  
		Size: 188.7 MB (188711229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f9ba9ed5eded42ca0c770f523700c989f3ea05f8439aa2ad1b5acea030ac99`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:f41ce426b1226aad6dd2d3ee6ff0b10c9d24cf47e6258311b2821f03dcc3cb2d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325602338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7e1311d7c0913449f35cd2c834f43dd87f148685605f0aa78ded3b82a81f96`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:08:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:08:48 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:11:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a17a83c8ddb404c7098a5aff94e15880eb3e16310d14f48dee3027f5b8906e`  
		Last Modified: Tue, 11 Mar 2025 18:11:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330cfaaf7f45b162bfd993005821d6c0d29b9d40f9cc38016259f97f204c767`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546e90a888c88a3d48ab94f1a6daa0cc58b6cc4c1a5ce5d754577881dd0c8d46`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de1d5b3f1bc550bf5fd4eb65cbaee826a9d9be6c3b03c5e87cc429ad24c95a4`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08945d1f42ec7c107909cb258eb71a398a305af6b9b17e538dac289a9a4c3d64`  
		Last Modified: Tue, 11 Mar 2025 18:11:56 GMT  
		Size: 188.7 MB (188687047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde799d583621d42ac5b6f311ccbcf1aa015989a8f6ce4646342e908c71f73d8`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:e2e598f7776cec38557649fb37f679a49980a957c9c628f40d750ef9514771c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:f41ce426b1226aad6dd2d3ee6ff0b10c9d24cf47e6258311b2821f03dcc3cb2d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325602338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7e1311d7c0913449f35cd2c834f43dd87f148685605f0aa78ded3b82a81f96`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:08:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:08:48 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:11:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a17a83c8ddb404c7098a5aff94e15880eb3e16310d14f48dee3027f5b8906e`  
		Last Modified: Tue, 11 Mar 2025 18:11:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330cfaaf7f45b162bfd993005821d6c0d29b9d40f9cc38016259f97f204c767`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546e90a888c88a3d48ab94f1a6daa0cc58b6cc4c1a5ce5d754577881dd0c8d46`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de1d5b3f1bc550bf5fd4eb65cbaee826a9d9be6c3b03c5e87cc429ad24c95a4`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08945d1f42ec7c107909cb258eb71a398a305af6b9b17e538dac289a9a4c3d64`  
		Last Modified: Tue, 11 Mar 2025 18:11:56 GMT  
		Size: 188.7 MB (188687047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde799d583621d42ac5b6f311ccbcf1aa015989a8f6ce4646342e908c71f73d8`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:5ad48e65d3c3913fdc998742893793d8796b413a39d58910729c0e270e482595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:a714a2d227085380226a475fd4f8d87347d68deaa39c380bb8a39f5c47904599
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452575686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337ca17c5313826be0d9e2d8ad00dc04fb82ddb265913b3aa849973c2ad0df9f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:42 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:08:43 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:08:44 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:10:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:10:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca70396628086048ee435c5ea681c12a42f47c964a13fe4681a4142eb46f309c`  
		Last Modified: Tue, 11 Mar 2025 18:10:37 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd558c6ded40bc493214da6479f570a8a1f055cb9c677cd5f7b91e3ea030717f`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8fd327b091fd9c321aab4a5cc14fe7ba146e31ad38ec90ddb17b747d004f02`  
		Last Modified: Tue, 11 Mar 2025 18:10:35 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cc8ade5c4bb6f4924ae74a69bf14226c81352e032d226089078877f358bab3`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfdbb42798cec7b45028bbbf24a756fd93aa29f7682d53444badad3327d42b8`  
		Last Modified: Tue, 11 Mar 2025 18:10:58 GMT  
		Size: 188.7 MB (188711229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f9ba9ed5eded42ca0c770f523700c989f3ea05f8439aa2ad1b5acea030ac99`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:d77160d7a3a4382bbf8d1e9fc3cbc3e6a19c67e45790c96ee40c07a7e79f4e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `julia:1.10-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:446b532f2f2d95c4d92d43c3c53cf272635ddc41d61432c91fe4c8e073a4d5ca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3005350438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8d63d6aab22ac6cdcce7c795a4e6eb4a643e53b0ae54e32f786245fa525eaa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:06 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:13:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:13:07 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:13:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:13:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97123365fbddeee79f4b37f0c2695f00f6dff271674dcc2aa0bb753115e86d5c`  
		Last Modified: Tue, 11 Mar 2025 18:13:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33faa754f1c2ecb18d865f3f93ea7e9a9df4166725c41c075d8019f6927ccbe0`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218a8ee7842459c03202660309caa82ba9054b2ba7c1a61667708244b4bf868e`  
		Last Modified: Tue, 11 Mar 2025 18:13:57 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af43409c1d69dc82793654c3ad5ca25ce2a9b7f452c4febd48bf1d6afa2b8fb7`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a015971492e83a7d992dca3d44be0ef46cf25792a6163774724a3abf3e0091`  
		Last Modified: Tue, 11 Mar 2025 18:14:24 GMT  
		Size: 188.8 MB (188756293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de15ab10ea3df45c2660f02a68d9f93a8f1d0e9ac1e281fbb7256875d9bdc86`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.9`

```console
$ docker pull julia@sha256:64e97f858e608dbaf724bbbece77e03dc3058bcc244a61ba4e45f225d75e6c17
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
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.10.9` - linux; amd64

```console
$ docker pull julia@sha256:8b0b59d70d25ad404428e8486e74afde1d1a77e89502c355243565a7fb15d7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210425312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19a74370a82c72f6745fd426077618ce3740e98bd26c71f8f55b467d24b6f16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfc3dde3fd3040765e99ffc81d694b63ceb83d88acea588c3e78f70a6eb445c`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 5.7 MB (5713109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6070c34eb6800f6d9580d96eb86c7a2f9722ac29ab738415b85c44f12f135ba`  
		Last Modified: Tue, 11 Mar 2025 17:57:38 GMT  
		Size: 176.5 MB (176492533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892b3a2797f3020dd1cf49bf0a76ad36b933f70ae42432ebc5f3ffdfa9229c02`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9` - unknown; unknown

```console
$ docker pull julia@sha256:bffe6578ba0212569be14de5faf69c4af7ced3088ccf16fa916f318b104b440b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93e022a9b68075d114f8dee364b9951705dcd950490a2ea8c5da13f653d4827`

```dockerfile
```

-	Layers:
	-	`sha256:a41409be7d8ea6d673173ccbfb1e9028f19103f93cdc87be50425104194df821`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 2.4 MB (2445501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f8fec7de9ee60a632fef43c99cc831b39c40c1302fa4de539cf5b053744fae2`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 17.2 KB (17213 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.9` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f33030be0ee76820af5d911dcd32a0d1b97a3594f787f6d78586c86633492abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210862164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8017f21911655a08fb3600e729a5cd8541b3f931cb8ba42639fc7388e5475eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
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
	-	`sha256:46834ae3839a09815ec69233743ecfc9832db91a32485080ffb99af8be0ef2bf`  
		Last Modified: Tue, 11 Mar 2025 18:00:39 GMT  
		Size: 177.3 MB (177275248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab774d07ab7f63d48bb4a973b081c6f1e4d102cbbd0a0bb3faf456a907722e0`  
		Last Modified: Tue, 11 Mar 2025 18:00:34 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9` - unknown; unknown

```console
$ docker pull julia@sha256:8589227b1d465fae3685376827a4d750abe2560addd1d5707bb4e0462285c70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddb5602e2af30ea4bf35f790e37c2f6097fb5915ab8b0a9cc0582181cb1f5f5`

```dockerfile
```

-	Layers:
	-	`sha256:e953707a8312de0f8cccb7494265711bf518ba696d66785d43898471752cd611`  
		Last Modified: Tue, 11 Mar 2025 18:00:34 GMT  
		Size: 2.4 MB (2444545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df08f09be34090691176e4fbab8f7e83a9048ac57cabefba8dbc98eef377ec18`  
		Last Modified: Tue, 11 Mar 2025 18:00:34 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.9` - linux; 386

```console
$ docker pull julia@sha256:de661161c1ece613b1030880da247ad6aec649e9a1610d95bbaa62d0b7d5f979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192823403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65c0ccc81974eee6b02c4c0e6fd8aee62c6e98eec95f4e174f68bea19d9b050`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad1046056eddfa74f5394894757c881bbf2cb01ef448af3d2020ed37c5882bd`  
		Last Modified: Tue, 11 Mar 2025 17:57:40 GMT  
		Size: 5.9 MB (5872032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f740f0d2db8cfc8a9465e690bc54c8ccc7083e41f7ee81284f69180e5555e426`  
		Last Modified: Tue, 11 Mar 2025 17:57:44 GMT  
		Size: 157.8 MB (157756408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a31e5bd03ee7113898e0824ace082e847618d5de5ec4d8a7072308cf7a786d`  
		Last Modified: Tue, 11 Mar 2025 17:57:39 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9` - unknown; unknown

```console
$ docker pull julia@sha256:97b55c239880540424f4e77a5b0fd9d35e5db7acb23d3040b5b2e7ae52ff43b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdb69cd1a95eba4262e022c6d861fca6c5648252cf51ffa5178cff9416f686d`

```dockerfile
```

-	Layers:
	-	`sha256:881f4f97440ef8d3651bbf686f00f7ba0ee3648d6a1003518a35fde07d7cf5f6`  
		Last Modified: Tue, 11 Mar 2025 17:57:39 GMT  
		Size: 2.4 MB (2442594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c01afa785c68a5852cdabdc2e65d5be13de11546af018ee7c40218072dda4ae`  
		Last Modified: Tue, 11 Mar 2025 17:57:39 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.9` - linux; ppc64le

```console
$ docker pull julia@sha256:f96f1de1b1836c0bd0923a9db025a40bc6da908b494dee681d5b1130b548566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193588610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5764f98f1c7d5e558bf92aa0052c5ef898911ab412f7a2ff005529c1e081802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
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
	-	`sha256:62c8b46c3aa2c0351fdc38df3a419c00ad9433827e45971822caa3fe02edcae4`  
		Last Modified: Tue, 11 Mar 2025 18:08:48 GMT  
		Size: 155.3 MB (155286603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a97a864525b59fba4a1137860dca62feffc62ae2c32e0754f0fbe9aa94993d7`  
		Last Modified: Tue, 11 Mar 2025 18:08:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9` - unknown; unknown

```console
$ docker pull julia@sha256:5bfc0698770e23eb7f5708c258256fc1f4eec2b42c2b04c25cb746d0e050e11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ed690a6028d6bf71be20aefeb2faf90a6c0db3199c2b2f3eaf61ceddceaf74`

```dockerfile
```

-	Layers:
	-	`sha256:2110249f1dde77e879f5260ca2e5ddeaa7cc0f53945892068dc0d87e3c795077`  
		Last Modified: Tue, 11 Mar 2025 18:08:43 GMT  
		Size: 2.4 MB (2448678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52bcc79f567d3332d8b6e78848a51afee62fc04798bc7638cca9fa90ace46823`  
		Last Modified: Tue, 11 Mar 2025 18:08:42 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.9` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:446b532f2f2d95c4d92d43c3c53cf272635ddc41d61432c91fe4c8e073a4d5ca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3005350438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8d63d6aab22ac6cdcce7c795a4e6eb4a643e53b0ae54e32f786245fa525eaa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:06 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:13:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:13:07 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:13:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:13:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97123365fbddeee79f4b37f0c2695f00f6dff271674dcc2aa0bb753115e86d5c`  
		Last Modified: Tue, 11 Mar 2025 18:13:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33faa754f1c2ecb18d865f3f93ea7e9a9df4166725c41c075d8019f6927ccbe0`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218a8ee7842459c03202660309caa82ba9054b2ba7c1a61667708244b4bf868e`  
		Last Modified: Tue, 11 Mar 2025 18:13:57 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af43409c1d69dc82793654c3ad5ca25ce2a9b7f452c4febd48bf1d6afa2b8fb7`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a015971492e83a7d992dca3d44be0ef46cf25792a6163774724a3abf3e0091`  
		Last Modified: Tue, 11 Mar 2025 18:14:24 GMT  
		Size: 188.8 MB (188756293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de15ab10ea3df45c2660f02a68d9f93a8f1d0e9ac1e281fbb7256875d9bdc86`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.9` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:a714a2d227085380226a475fd4f8d87347d68deaa39c380bb8a39f5c47904599
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452575686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337ca17c5313826be0d9e2d8ad00dc04fb82ddb265913b3aa849973c2ad0df9f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:42 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:08:43 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:08:44 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:10:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:10:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca70396628086048ee435c5ea681c12a42f47c964a13fe4681a4142eb46f309c`  
		Last Modified: Tue, 11 Mar 2025 18:10:37 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd558c6ded40bc493214da6479f570a8a1f055cb9c677cd5f7b91e3ea030717f`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8fd327b091fd9c321aab4a5cc14fe7ba146e31ad38ec90ddb17b747d004f02`  
		Last Modified: Tue, 11 Mar 2025 18:10:35 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cc8ade5c4bb6f4924ae74a69bf14226c81352e032d226089078877f358bab3`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfdbb42798cec7b45028bbbf24a756fd93aa29f7682d53444badad3327d42b8`  
		Last Modified: Tue, 11 Mar 2025 18:10:58 GMT  
		Size: 188.7 MB (188711229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f9ba9ed5eded42ca0c770f523700c989f3ea05f8439aa2ad1b5acea030ac99`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.9` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:f41ce426b1226aad6dd2d3ee6ff0b10c9d24cf47e6258311b2821f03dcc3cb2d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325602338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7e1311d7c0913449f35cd2c834f43dd87f148685605f0aa78ded3b82a81f96`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:08:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:08:48 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:11:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a17a83c8ddb404c7098a5aff94e15880eb3e16310d14f48dee3027f5b8906e`  
		Last Modified: Tue, 11 Mar 2025 18:11:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330cfaaf7f45b162bfd993005821d6c0d29b9d40f9cc38016259f97f204c767`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546e90a888c88a3d48ab94f1a6daa0cc58b6cc4c1a5ce5d754577881dd0c8d46`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de1d5b3f1bc550bf5fd4eb65cbaee826a9d9be6c3b03c5e87cc429ad24c95a4`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08945d1f42ec7c107909cb258eb71a398a305af6b9b17e538dac289a9a4c3d64`  
		Last Modified: Tue, 11 Mar 2025 18:11:56 GMT  
		Size: 188.7 MB (188687047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde799d583621d42ac5b6f311ccbcf1aa015989a8f6ce4646342e908c71f73d8`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.9-alpine`

```console
$ docker pull julia@sha256:8e4ffc534ac11fe111200ebab165d7a261bfba9d29fcc04a04aa7c2bd31b118c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.9-alpine` - linux; amd64

```console
$ docker pull julia@sha256:05deda0ce568e7a486b0fc78655b9bef56733d5cfcd208798402f88226a6c561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182007528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f25ad31514dea1aabdc59453a663a229195e7149590fc1a5847f0af9cc85253`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.9-musl-x86_64.tar.gz'; 			sha256='db7454a7acf677598c23216eb4798d0b0ebc6be7c7d03ea2e7ee10f7a5985a64'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc378e9762465cbab26df40725a9ecfe34e926aaf564feddb91cc95c13de7b28`  
		Last Modified: Tue, 11 Mar 2025 17:57:44 GMT  
		Size: 178.4 MB (178364914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4520b8b4e112fc364be7582ee2b4ca8061b8052366dd86efaf248e566205e5`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:2223de82816678d7a5d22c595d7f20df940a4c8fa334c4e873afbc9e4bbd6661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 KB (92467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4525c47a13d5dcf6cdcf5eb0a1782ec015ee9d67036a9c66416fc7df4c675636`

```dockerfile
```

-	Layers:
	-	`sha256:cd6f6fd2d3a0b982ec6c85d31fd7ed1b92c51d681a819bb033ad45cd64fa41d2`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 79.9 KB (79887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8be5f503861b92fe7dbe4f2f3ee14b81ddf62127c3b8ee5309c746073e18aac0`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.9-alpine3.20`

```console
$ docker pull julia@sha256:81f5bc3f2a97bea0882aaf015bb3de2be43df79b24ada259ad76f91daea7ed45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.9-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:9131fd82410f167efb10f0d16d426f9e6f39afa1aeca0fccfbaacb1204f4a7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181991132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0985fdedfd97d7aa5f5474cf3e4678ff6df6e85b96f910e5cf2cddd3450f7ba8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.9-musl-x86_64.tar.gz'; 			sha256='db7454a7acf677598c23216eb4798d0b0ebc6be7c7d03ea2e7ee10f7a5985a64'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71785e30ec36ae8f1c1bfa80a151812603ffd7422c6ac8648c8ea8c50ede4b14`  
		Last Modified: Tue, 11 Mar 2025 17:57:32 GMT  
		Size: 178.4 MB (178363869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9475bb49640359a1dbb9b7deadb033831e371dbe2cd9c974e711e56057c0e4`  
		Last Modified: Tue, 11 Mar 2025 17:57:29 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:6ac78f52fab40551ab05791c769648be90f88c3b9f3b7113a8f82f964f9e3504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54c9cec2429055f41565bfda85c251e0c44c54202420c168d84584ca64ce9b8`

```dockerfile
```

-	Layers:
	-	`sha256:5615806ab6fdc8c53b4cf2fcac1cef95a8f764b5ba4d7b18a1a08998c3413470`  
		Last Modified: Tue, 11 Mar 2025 17:57:29 GMT  
		Size: 73.5 KB (73545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:715651ac7e91e91b53873a3398a8d77dcf1560c954704458e18deb5898e67aa1`  
		Last Modified: Tue, 11 Mar 2025 17:57:29 GMT  
		Size: 12.0 KB (11964 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.9-alpine3.21`

```console
$ docker pull julia@sha256:8e4ffc534ac11fe111200ebab165d7a261bfba9d29fcc04a04aa7c2bd31b118c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.9-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:05deda0ce568e7a486b0fc78655b9bef56733d5cfcd208798402f88226a6c561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182007528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f25ad31514dea1aabdc59453a663a229195e7149590fc1a5847f0af9cc85253`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.9-musl-x86_64.tar.gz'; 			sha256='db7454a7acf677598c23216eb4798d0b0ebc6be7c7d03ea2e7ee10f7a5985a64'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc378e9762465cbab26df40725a9ecfe34e926aaf564feddb91cc95c13de7b28`  
		Last Modified: Tue, 11 Mar 2025 17:57:44 GMT  
		Size: 178.4 MB (178364914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4520b8b4e112fc364be7582ee2b4ca8061b8052366dd86efaf248e566205e5`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:2223de82816678d7a5d22c595d7f20df940a4c8fa334c4e873afbc9e4bbd6661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 KB (92467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4525c47a13d5dcf6cdcf5eb0a1782ec015ee9d67036a9c66416fc7df4c675636`

```dockerfile
```

-	Layers:
	-	`sha256:cd6f6fd2d3a0b982ec6c85d31fd7ed1b92c51d681a819bb033ad45cd64fa41d2`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 79.9 KB (79887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8be5f503861b92fe7dbe4f2f3ee14b81ddf62127c3b8ee5309c746073e18aac0`  
		Last Modified: Tue, 11 Mar 2025 17:57:37 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.9-bookworm`

```console
$ docker pull julia@sha256:a38cfecb98b3454159eb9e422e89632d6f03447cd8966f8f5ec529c28c37fdc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10.9-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:8b0b59d70d25ad404428e8486e74afde1d1a77e89502c355243565a7fb15d7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210425312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19a74370a82c72f6745fd426077618ce3740e98bd26c71f8f55b467d24b6f16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfc3dde3fd3040765e99ffc81d694b63ceb83d88acea588c3e78f70a6eb445c`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 5.7 MB (5713109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6070c34eb6800f6d9580d96eb86c7a2f9722ac29ab738415b85c44f12f135ba`  
		Last Modified: Tue, 11 Mar 2025 17:57:38 GMT  
		Size: 176.5 MB (176492533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892b3a2797f3020dd1cf49bf0a76ad36b933f70ae42432ebc5f3ffdfa9229c02`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:bffe6578ba0212569be14de5faf69c4af7ced3088ccf16fa916f318b104b440b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93e022a9b68075d114f8dee364b9951705dcd950490a2ea8c5da13f653d4827`

```dockerfile
```

-	Layers:
	-	`sha256:a41409be7d8ea6d673173ccbfb1e9028f19103f93cdc87be50425104194df821`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 2.4 MB (2445501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f8fec7de9ee60a632fef43c99cc831b39c40c1302fa4de539cf5b053744fae2`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 17.2 KB (17213 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.9-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f33030be0ee76820af5d911dcd32a0d1b97a3594f787f6d78586c86633492abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210862164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8017f21911655a08fb3600e729a5cd8541b3f931cb8ba42639fc7388e5475eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
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
	-	`sha256:46834ae3839a09815ec69233743ecfc9832db91a32485080ffb99af8be0ef2bf`  
		Last Modified: Tue, 11 Mar 2025 18:00:39 GMT  
		Size: 177.3 MB (177275248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab774d07ab7f63d48bb4a973b081c6f1e4d102cbbd0a0bb3faf456a907722e0`  
		Last Modified: Tue, 11 Mar 2025 18:00:34 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8589227b1d465fae3685376827a4d750abe2560addd1d5707bb4e0462285c70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddb5602e2af30ea4bf35f790e37c2f6097fb5915ab8b0a9cc0582181cb1f5f5`

```dockerfile
```

-	Layers:
	-	`sha256:e953707a8312de0f8cccb7494265711bf518ba696d66785d43898471752cd611`  
		Last Modified: Tue, 11 Mar 2025 18:00:34 GMT  
		Size: 2.4 MB (2444545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df08f09be34090691176e4fbab8f7e83a9048ac57cabefba8dbc98eef377ec18`  
		Last Modified: Tue, 11 Mar 2025 18:00:34 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.9-bookworm` - linux; 386

```console
$ docker pull julia@sha256:de661161c1ece613b1030880da247ad6aec649e9a1610d95bbaa62d0b7d5f979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192823403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65c0ccc81974eee6b02c4c0e6fd8aee62c6e98eec95f4e174f68bea19d9b050`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad1046056eddfa74f5394894757c881bbf2cb01ef448af3d2020ed37c5882bd`  
		Last Modified: Tue, 11 Mar 2025 17:57:40 GMT  
		Size: 5.9 MB (5872032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f740f0d2db8cfc8a9465e690bc54c8ccc7083e41f7ee81284f69180e5555e426`  
		Last Modified: Tue, 11 Mar 2025 17:57:44 GMT  
		Size: 157.8 MB (157756408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a31e5bd03ee7113898e0824ace082e847618d5de5ec4d8a7072308cf7a786d`  
		Last Modified: Tue, 11 Mar 2025 17:57:39 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:97b55c239880540424f4e77a5b0fd9d35e5db7acb23d3040b5b2e7ae52ff43b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdb69cd1a95eba4262e022c6d861fca6c5648252cf51ffa5178cff9416f686d`

```dockerfile
```

-	Layers:
	-	`sha256:881f4f97440ef8d3651bbf686f00f7ba0ee3648d6a1003518a35fde07d7cf5f6`  
		Last Modified: Tue, 11 Mar 2025 17:57:39 GMT  
		Size: 2.4 MB (2442594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c01afa785c68a5852cdabdc2e65d5be13de11546af018ee7c40218072dda4ae`  
		Last Modified: Tue, 11 Mar 2025 17:57:39 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.9-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:f96f1de1b1836c0bd0923a9db025a40bc6da908b494dee681d5b1130b548566c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193588610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5764f98f1c7d5e558bf92aa0052c5ef898911ab412f7a2ff005529c1e081802`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
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
	-	`sha256:62c8b46c3aa2c0351fdc38df3a419c00ad9433827e45971822caa3fe02edcae4`  
		Last Modified: Tue, 11 Mar 2025 18:08:48 GMT  
		Size: 155.3 MB (155286603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a97a864525b59fba4a1137860dca62feffc62ae2c32e0754f0fbe9aa94993d7`  
		Last Modified: Tue, 11 Mar 2025 18:08:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5bfc0698770e23eb7f5708c258256fc1f4eec2b42c2b04c25cb746d0e050e11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ed690a6028d6bf71be20aefeb2faf90a6c0db3199c2b2f3eaf61ceddceaf74`

```dockerfile
```

-	Layers:
	-	`sha256:2110249f1dde77e879f5260ca2e5ddeaa7cc0f53945892068dc0d87e3c795077`  
		Last Modified: Tue, 11 Mar 2025 18:08:43 GMT  
		Size: 2.4 MB (2448678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52bcc79f567d3332d8b6e78848a51afee62fc04798bc7638cca9fa90ace46823`  
		Last Modified: Tue, 11 Mar 2025 18:08:42 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.9-bullseye`

```console
$ docker pull julia@sha256:26b265a6e2a5bb710814762459f6a3adf4cb16031d8a20ff5590b0b67594d7e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10.9-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:a359bc7048257d6d14d332482447142f9ff65f8b61b812733263979498904593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (208970883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c058bb2161080c08c4a1c2605abce277908069e532b9e8cfbbfa66aca6c395`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430b039f93073c03482645206793f4d953e78de8d00f5d1d5c1bc8ab34e118ec`  
		Last Modified: Tue, 11 Mar 2025 17:57:45 GMT  
		Size: 2.2 MB (2222651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4404939bfc543c9749b9c47addd8ef29ed082979cdb85e748d12bba35fc7f2dc`  
		Last Modified: Tue, 11 Mar 2025 17:57:49 GMT  
		Size: 176.5 MB (176493928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c6680b3af4d305df03b38964b8f08b92e7df82967a5441aa875f10a8575224`  
		Last Modified: Tue, 11 Mar 2025 17:57:44 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:6049e9318a2b539969e6d340d4ac631d5a0cc600cfa1afbf715c5add0e678d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d3dde32990671ef2c80f62a55d30490c034da5d2fbdb85e938a3cf5cd9fb6a`

```dockerfile
```

-	Layers:
	-	`sha256:02a3276015fbc18fcd763f574041640f1d1b20e1ef7f871b01bfdb10986461ff`  
		Last Modified: Tue, 11 Mar 2025 17:57:45 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5193f8373a94eec6c560fa126be877bd84e52a4877e663fdd6971044dab29f2e`  
		Last Modified: Tue, 11 Mar 2025 17:57:44 GMT  
		Size: 16.6 KB (16625 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.9-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:bf15aea11334363726c621ddce60a1890e8648bb77367c9c2c8bb53dd3e6758f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.2 MB (208231962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7308e7f3fb0bacd82050242ca33406839ef21b3e4996941632ce3f98b4aeaed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc5dc01c337dce742e7c6026ccf096f7b1c09278ca05a29613e61d8fe553208`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 2.2 MB (2210309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e70fdfc06723ceb275af0e9e09f8be51bf723c58761f8f3ecb0ae4fffddff7`  
		Last Modified: Tue, 11 Mar 2025 18:01:38 GMT  
		Size: 177.3 MB (177275295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d642bb0ce5f955ccb4b7302b0d9297295b15a397570517e08b1484ad84814e1d`  
		Last Modified: Tue, 11 Mar 2025 18:01:33 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:4d7a5cdb49528c2af835f0e91c20e51c0ca171eb0a147e691012e72dee4b1a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a631687d0a2377e4da2424c12fb57a59996cd86dc1b06d06898f75c704c74d`

```dockerfile
```

-	Layers:
	-	`sha256:878f8fec3dee010a4a5e3b0d77074587964d959a0754edd043f8f1fc23120e42`  
		Last Modified: Tue, 11 Mar 2025 18:01:33 GMT  
		Size: 2.7 MB (2712181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee8c33359dc7d305e61c7de3255800385e7898052e6d852e89d1be25f06950e`  
		Last Modified: Tue, 11 Mar 2025 18:01:33 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.9-bullseye` - linux; 386

```console
$ docker pull julia@sha256:37d7fcbd4245247644a59a4c45e0748d8af7d7288683c4c72d485fcd6161c000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191265287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ea07724114db9957b20dd858bb23a65a080b695c8b560869bca85f82b68d37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 10 Mar 2025 23:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 10 Mar 2025 23:59:15 GMT
ENV JULIA_VERSION=1.10.9
# Mon, 10 Mar 2025 23:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.9-linux-x86_64.tar.gz'; 			sha256='5a2d2c5224594b683c97e7304cb72407fbcf0be4a0187789cba1a2f73f0cbf09'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.9-linux-aarch64.tar.gz'; 			sha256='be222882e3674f960f43b6842f7bbb52a369977e40d5dcd26498793e1cd2dfb6'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.9-linux-i686.tar.gz'; 			sha256='012d6b13d9c9b98d56b4b0a67fe5e8efc59df880dd432beb062c2a1502238d86'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.9-linux-ppc64le.tar.gz'; 			sha256='484efe8e5eb9e142431f0c57c261d4877b496656e936065c2d57f012d0eef57f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Mar 2025 23:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Mar 2025 23:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578b5ac6328415549e35f4b2b368227d2fcac715b85c2919af7537f87ae610b6`  
		Last Modified: Tue, 11 Mar 2025 17:57:33 GMT  
		Size: 2.3 MB (2328059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573ebe960fc2da6002de3ed24efaefc7bd3c69998e20e9d4b03bd1e61191486e`  
		Last Modified: Tue, 11 Mar 2025 17:57:36 GMT  
		Size: 157.8 MB (157756432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f140ecd12f3dd3f8a39e95a29e5d9de5575a70ba53fa59ffd659154e099150b`  
		Last Modified: Tue, 11 Mar 2025 17:57:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:16628feb8c2cfb9bf19f0b3ae88b2a9cd83cde2e2e3530392530380044c3e0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96cca7d128b27d6cfd8e5848c8c1b94f7b76ef644d8325d43c23a3b4220daff`

```dockerfile
```

-	Layers:
	-	`sha256:6ba51ee3834a88c46a90578cb672c323f01931b57f705dbec0df26b5d4a49ee1`  
		Last Modified: Tue, 11 Mar 2025 17:57:32 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65abb8f99a69871222c2324f5e79f1b5516b4e431dec9e174b3ccc0a65ebc009`  
		Last Modified: Tue, 11 Mar 2025 17:57:32 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.9-windowsservercore`

```console
$ docker pull julia@sha256:1a1cd97e99d8602ead0c527f352adf9fd27d9d80446ef00e12f1b8a707935617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.10.9-windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:446b532f2f2d95c4d92d43c3c53cf272635ddc41d61432c91fe4c8e073a4d5ca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3005350438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8d63d6aab22ac6cdcce7c795a4e6eb4a643e53b0ae54e32f786245fa525eaa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:06 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:13:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:13:07 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:13:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:13:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97123365fbddeee79f4b37f0c2695f00f6dff271674dcc2aa0bb753115e86d5c`  
		Last Modified: Tue, 11 Mar 2025 18:13:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33faa754f1c2ecb18d865f3f93ea7e9a9df4166725c41c075d8019f6927ccbe0`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218a8ee7842459c03202660309caa82ba9054b2ba7c1a61667708244b4bf868e`  
		Last Modified: Tue, 11 Mar 2025 18:13:57 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af43409c1d69dc82793654c3ad5ca25ce2a9b7f452c4febd48bf1d6afa2b8fb7`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a015971492e83a7d992dca3d44be0ef46cf25792a6163774724a3abf3e0091`  
		Last Modified: Tue, 11 Mar 2025 18:14:24 GMT  
		Size: 188.8 MB (188756293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de15ab10ea3df45c2660f02a68d9f93a8f1d0e9ac1e281fbb7256875d9bdc86`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.9-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:a714a2d227085380226a475fd4f8d87347d68deaa39c380bb8a39f5c47904599
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452575686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337ca17c5313826be0d9e2d8ad00dc04fb82ddb265913b3aa849973c2ad0df9f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:42 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:08:43 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:08:44 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:10:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:10:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca70396628086048ee435c5ea681c12a42f47c964a13fe4681a4142eb46f309c`  
		Last Modified: Tue, 11 Mar 2025 18:10:37 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd558c6ded40bc493214da6479f570a8a1f055cb9c677cd5f7b91e3ea030717f`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8fd327b091fd9c321aab4a5cc14fe7ba146e31ad38ec90ddb17b747d004f02`  
		Last Modified: Tue, 11 Mar 2025 18:10:35 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cc8ade5c4bb6f4924ae74a69bf14226c81352e032d226089078877f358bab3`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfdbb42798cec7b45028bbbf24a756fd93aa29f7682d53444badad3327d42b8`  
		Last Modified: Tue, 11 Mar 2025 18:10:58 GMT  
		Size: 188.7 MB (188711229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f9ba9ed5eded42ca0c770f523700c989f3ea05f8439aa2ad1b5acea030ac99`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.9-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:f41ce426b1226aad6dd2d3ee6ff0b10c9d24cf47e6258311b2821f03dcc3cb2d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325602338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7e1311d7c0913449f35cd2c834f43dd87f148685605f0aa78ded3b82a81f96`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:08:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:08:48 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:11:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a17a83c8ddb404c7098a5aff94e15880eb3e16310d14f48dee3027f5b8906e`  
		Last Modified: Tue, 11 Mar 2025 18:11:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330cfaaf7f45b162bfd993005821d6c0d29b9d40f9cc38016259f97f204c767`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546e90a888c88a3d48ab94f1a6daa0cc58b6cc4c1a5ce5d754577881dd0c8d46`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de1d5b3f1bc550bf5fd4eb65cbaee826a9d9be6c3b03c5e87cc429ad24c95a4`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08945d1f42ec7c107909cb258eb71a398a305af6b9b17e538dac289a9a4c3d64`  
		Last Modified: Tue, 11 Mar 2025 18:11:56 GMT  
		Size: 188.7 MB (188687047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde799d583621d42ac5b6f311ccbcf1aa015989a8f6ce4646342e908c71f73d8`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.9-windowsservercore-1809`

```console
$ docker pull julia@sha256:e2e598f7776cec38557649fb37f679a49980a957c9c628f40d750ef9514771c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:1.10.9-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:f41ce426b1226aad6dd2d3ee6ff0b10c9d24cf47e6258311b2821f03dcc3cb2d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325602338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7e1311d7c0913449f35cd2c834f43dd87f148685605f0aa78ded3b82a81f96`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:08:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:08:48 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:11:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a17a83c8ddb404c7098a5aff94e15880eb3e16310d14f48dee3027f5b8906e`  
		Last Modified: Tue, 11 Mar 2025 18:11:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6330cfaaf7f45b162bfd993005821d6c0d29b9d40f9cc38016259f97f204c767`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546e90a888c88a3d48ab94f1a6daa0cc58b6cc4c1a5ce5d754577881dd0c8d46`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de1d5b3f1bc550bf5fd4eb65cbaee826a9d9be6c3b03c5e87cc429ad24c95a4`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08945d1f42ec7c107909cb258eb71a398a305af6b9b17e538dac289a9a4c3d64`  
		Last Modified: Tue, 11 Mar 2025 18:11:56 GMT  
		Size: 188.7 MB (188687047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde799d583621d42ac5b6f311ccbcf1aa015989a8f6ce4646342e908c71f73d8`  
		Last Modified: Tue, 11 Mar 2025 18:11:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.9-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:5ad48e65d3c3913fdc998742893793d8796b413a39d58910729c0e270e482595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1.10.9-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:a714a2d227085380226a475fd4f8d87347d68deaa39c380bb8a39f5c47904599
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452575686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337ca17c5313826be0d9e2d8ad00dc04fb82ddb265913b3aa849973c2ad0df9f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:42 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:08:43 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:08:44 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:10:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:10:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca70396628086048ee435c5ea681c12a42f47c964a13fe4681a4142eb46f309c`  
		Last Modified: Tue, 11 Mar 2025 18:10:37 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd558c6ded40bc493214da6479f570a8a1f055cb9c677cd5f7b91e3ea030717f`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8fd327b091fd9c321aab4a5cc14fe7ba146e31ad38ec90ddb17b747d004f02`  
		Last Modified: Tue, 11 Mar 2025 18:10:35 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cc8ade5c4bb6f4924ae74a69bf14226c81352e032d226089078877f358bab3`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfdbb42798cec7b45028bbbf24a756fd93aa29f7682d53444badad3327d42b8`  
		Last Modified: Tue, 11 Mar 2025 18:10:58 GMT  
		Size: 188.7 MB (188711229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f9ba9ed5eded42ca0c770f523700c989f3ea05f8439aa2ad1b5acea030ac99`  
		Last Modified: Tue, 11 Mar 2025 18:10:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.9-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:d77160d7a3a4382bbf8d1e9fc3cbc3e6a19c67e45790c96ee40c07a7e79f4e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `julia:1.10.9-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:446b532f2f2d95c4d92d43c3c53cf272635ddc41d61432c91fe4c8e073a4d5ca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3005350438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8d63d6aab22ac6cdcce7c795a4e6eb4a643e53b0ae54e32f786245fa525eaa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:06 GMT
ENV JULIA_VERSION=1.10.9
# Tue, 11 Mar 2025 18:13:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Tue, 11 Mar 2025 18:13:07 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Tue, 11 Mar 2025 18:13:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:13:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97123365fbddeee79f4b37f0c2695f00f6dff271674dcc2aa0bb753115e86d5c`  
		Last Modified: Tue, 11 Mar 2025 18:13:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33faa754f1c2ecb18d865f3f93ea7e9a9df4166725c41c075d8019f6927ccbe0`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218a8ee7842459c03202660309caa82ba9054b2ba7c1a61667708244b4bf868e`  
		Last Modified: Tue, 11 Mar 2025 18:13:57 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af43409c1d69dc82793654c3ad5ca25ce2a9b7f452c4febd48bf1d6afa2b8fb7`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a015971492e83a7d992dca3d44be0ef46cf25792a6163774724a3abf3e0091`  
		Last Modified: Tue, 11 Mar 2025 18:14:24 GMT  
		Size: 188.8 MB (188756293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de15ab10ea3df45c2660f02a68d9f93a8f1d0e9ac1e281fbb7256875d9bdc86`  
		Last Modified: Tue, 11 Mar 2025 18:13:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:3930bce3315aa328a039d06295aa25c759705b57b9946263ac8a817a2078a5cd
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
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.11` - linux; amd64

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

### `julia:1.11` - unknown; unknown

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

### `julia:1.11` - linux; arm64 variant v8

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

### `julia:1.11` - unknown; unknown

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

### `julia:1.11` - linux; 386

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

### `julia:1.11` - unknown; unknown

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

### `julia:1.11` - linux; ppc64le

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

### `julia:1.11` - unknown; unknown

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

### `julia:1.11` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:8acf88f620e712a0a209bfbccf0eed2dcc0b2946508997213353097da27d170e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081734503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cc4c1f77bbe2ff3fc6f90bcc7f0b4d7d47e9aa0617b9c179e358c1eaf7baf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:13 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:13:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:13:15 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:14:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:14:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b580e80688f1e334734aea2880fa5931e55370f3539fc8e78058543d2fbb4`  
		Last Modified: Tue, 11 Mar 2025 18:14:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec1357c0e2eb61ac9298926dd9084156bd2d05dcea183ea8786979784c324`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a8e2f5c7e51683c21328502741d075647e87f5e9d195902a79b4362af9708`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a47c47f5f7ce9891789821dc08dbb73af7a03679e28d975173ca02457a3c85`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b401c362d821c447b22c6303f6e897b6cc2098aab4b7061cdd239ad38f00356`  
		Last Modified: Tue, 11 Mar 2025 18:15:03 GMT  
		Size: 265.1 MB (265140438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a26224618776b48b976e6718b0c66dc407c2f1423a2a911b49b31fa347919`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:4ec46cc1e5ec14205a112b7bcf25d17feb1195c4427bea62804de7c93aa1d464
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528934099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdb17d614282c158734ba03f7db6e9dc4b123d2b2fa012b800e11be2b66dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e613cb0bd6b9cdefc91ef48f6b84eafc8bfedc674b985f05222969a1e708d2`  
		Last Modified: Tue, 11 Mar 2025 18:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55928cd0613a4698f021e84a732f32008287c1079893322ef0577d3b68e1d7e3`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769b36b1b267ac98d3c0b181635a870dbbb219e2ce05ed2bc0e25172e009aaa`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc75c329d096e43a1095e057c53bce7d7b5fa96ca5a61ad0a496b1e89bd34f`  
		Last Modified: Tue, 11 Mar 2025 18:11:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de433e53b119c1cea9de09b3637d6600006b928c83e8554570ae155ad81392d0`  
		Last Modified: Tue, 11 Mar 2025 18:11:58 GMT  
		Size: 265.1 MB (265069668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734d83e3be039a110407a2e7cd36a59ad3f092bf4f426da5936550ea2e7e933`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:399302474cb5ef2ccf216c1c73c97c7bf0a39666c35c6d80ef67ba01fb6aa3ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11-bookworm` - linux; amd64

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

### `julia:1.11-bookworm` - unknown; unknown

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

### `julia:1.11-bookworm` - linux; arm64 variant v8

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

### `julia:1.11-bookworm` - unknown; unknown

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

### `julia:1.11-bookworm` - linux; 386

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

### `julia:1.11-bookworm` - unknown; unknown

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

### `julia:1.11-bookworm` - linux; ppc64le

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

### `julia:1.11-bookworm` - unknown; unknown

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

## `julia:1.11-bullseye`

```console
$ docker pull julia@sha256:8a5776a35daa3f5821996974b6bfccbca0acb93c57adb7be66f808fd48601b35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:72c9ae493b9eca82f0c07a276f2f0b4f7863d119474f66f8586eefa0a8053ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300961401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c67a903937f5891a72c30c6adc5ed4626c951909fa33c301f1aa5aa4c45948`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7165c83944224063d633634d136cf1bf62f390d866ccb2ae699c012548aac6`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 2.2 MB (2222654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725e528a3666541c2953691421b6a228673594440c7d539fb35f71fc2a46be48`  
		Last Modified: Tue, 11 Mar 2025 17:58:00 GMT  
		Size: 268.5 MB (268484444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d38f27ed12d5f890c2121a4a56d39f8767d3f6cbb1c14d39ddfbb22f45e415`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8a02228943143116153ce0d2488cd203e6ce948bb248949bcb0429c8686408b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91301a3221f1b9ae49dc24f7c05ad6161194f3e57f108ca52589d84115267526`

```dockerfile
```

-	Layers:
	-	`sha256:fc3a810a8f575b0ac14f3c720fac7a97fde163cba0299bdb59633c6e09cd7717`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7391d4ac599c40348906465dcc052d096f6db456615fe307bd2b39cb79da36c5`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dc6141754eb15dc1abb94a4e67d1c698f01f879691520bdc23842d794c80adda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (314957093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f10b2054506b5f7fbdf5f4b4cc409f99caaf7ba0559d1ce43fcad496c62ed92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc5dc01c337dce742e7c6026ccf096f7b1c09278ca05a29613e61d8fe553208`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 2.2 MB (2210309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47705c544b0c43fa505ea4141d20e1bd7047b8da8398c7a5e3d1214f40573e1`  
		Last Modified: Tue, 11 Mar 2025 17:59:35 GMT  
		Size: 284.0 MB (284000422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e906007b13ae7c53726d61e1006d643af01db9a126dcf54f834921cca9a146a`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:063ec1c56311e72dc3969d58c12069c7431f9663a075fb5fbca0ecea6b4fadb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8736a85ebdb295f549dc129bf2389633fae54193cc5512562d7d6452465fdb`

```dockerfile
```

-	Layers:
	-	`sha256:f153b82ac16be75d5ce35c461d4642790760c612f40500aba30fd809ff482f9d`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3990310fdd52100587e443fc54cd91ffdd102077037c0b0003599851c0c10ca7`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; 386

```console
$ docker pull julia@sha256:415eda97c01612223e23e19484ef8c99744317636dc5c495c6a3ce456ce2c57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251354410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a238940033d7286786b0a0ebdb5f1de9242b3576a705221eccc3e647c6a3a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768dc8869224f294d9e2ae8231a8c8a74f708a8e5495e183d94dfbedf98d3816`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 2.3 MB (2328071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e4bd659adb5b6bdf7cd848dd04bdd531234e9725242266aa53357febdcb23a`  
		Last Modified: Tue, 11 Mar 2025 17:57:47 GMT  
		Size: 217.8 MB (217845544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706ff1c0df0fa586527b601c6e9c2b526f2521b19a51b12649fedbc429419671`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:257c12809f8a9b581f7dde263775c80db30df53d4fcf13cd4fd1820599b3ce66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0464719ad93ca07e66b0669a89f783025f238fad94ecff01f027d6f292c6ea`

```dockerfile
```

-	Layers:
	-	`sha256:e12e0dd0133063f2b20338f66514bc5628916b5506a86b7491ad172daa119aab`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b13c04845b43675f6fc2c6eb60313e14e089c471deb5b03bff80a58579050c65`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 17.2 KB (17195 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:558e56296c78e7898fafefc944345bcb81b21a48f6137d1b8c9a74322b32c243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:8acf88f620e712a0a209bfbccf0eed2dcc0b2946508997213353097da27d170e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081734503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cc4c1f77bbe2ff3fc6f90bcc7f0b4d7d47e9aa0617b9c179e358c1eaf7baf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:13 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:13:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:13:15 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:14:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:14:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b580e80688f1e334734aea2880fa5931e55370f3539fc8e78058543d2fbb4`  
		Last Modified: Tue, 11 Mar 2025 18:14:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec1357c0e2eb61ac9298926dd9084156bd2d05dcea183ea8786979784c324`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a8e2f5c7e51683c21328502741d075647e87f5e9d195902a79b4362af9708`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a47c47f5f7ce9891789821dc08dbb73af7a03679e28d975173ca02457a3c85`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b401c362d821c447b22c6303f6e897b6cc2098aab4b7061cdd239ad38f00356`  
		Last Modified: Tue, 11 Mar 2025 18:15:03 GMT  
		Size: 265.1 MB (265140438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a26224618776b48b976e6718b0c66dc407c2f1423a2a911b49b31fa347919`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:4ec46cc1e5ec14205a112b7bcf25d17feb1195c4427bea62804de7c93aa1d464
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528934099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdb17d614282c158734ba03f7db6e9dc4b123d2b2fa012b800e11be2b66dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e613cb0bd6b9cdefc91ef48f6b84eafc8bfedc674b985f05222969a1e708d2`  
		Last Modified: Tue, 11 Mar 2025 18:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55928cd0613a4698f021e84a732f32008287c1079893322ef0577d3b68e1d7e3`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769b36b1b267ac98d3c0b181635a870dbbb219e2ce05ed2bc0e25172e009aaa`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc75c329d096e43a1095e057c53bce7d7b5fa96ca5a61ad0a496b1e89bd34f`  
		Last Modified: Tue, 11 Mar 2025 18:11:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de433e53b119c1cea9de09b3637d6600006b928c83e8554570ae155ad81392d0`  
		Last Modified: Tue, 11 Mar 2025 18:11:58 GMT  
		Size: 265.1 MB (265069668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734d83e3be039a110407a2e7cd36a59ad3f092bf4f426da5936550ea2e7e933`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-1809`

```console
$ docker pull julia@sha256:f6329f6ba2acb70fa9e6ebbc91d4d536d0672c1f7305a02fbbef863042afb5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:1.11-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:48b3643c0c3cd7f12c11619010332d97e6a3023a78fd6e385b1ee9934378d93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:4ec46cc1e5ec14205a112b7bcf25d17feb1195c4427bea62804de7c93aa1d464
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528934099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdb17d614282c158734ba03f7db6e9dc4b123d2b2fa012b800e11be2b66dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e613cb0bd6b9cdefc91ef48f6b84eafc8bfedc674b985f05222969a1e708d2`  
		Last Modified: Tue, 11 Mar 2025 18:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55928cd0613a4698f021e84a732f32008287c1079893322ef0577d3b68e1d7e3`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769b36b1b267ac98d3c0b181635a870dbbb219e2ce05ed2bc0e25172e009aaa`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc75c329d096e43a1095e057c53bce7d7b5fa96ca5a61ad0a496b1e89bd34f`  
		Last Modified: Tue, 11 Mar 2025 18:11:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de433e53b119c1cea9de09b3637d6600006b928c83e8554570ae155ad81392d0`  
		Last Modified: Tue, 11 Mar 2025 18:11:58 GMT  
		Size: 265.1 MB (265069668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734d83e3be039a110407a2e7cd36a59ad3f092bf4f426da5936550ea2e7e933`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:77810f8d3cfceabad6bc16d6a389038ef89b0aca5c3042647606edd4eb74e52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `julia:1.11-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:8acf88f620e712a0a209bfbccf0eed2dcc0b2946508997213353097da27d170e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081734503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cc4c1f77bbe2ff3fc6f90bcc7f0b4d7d47e9aa0617b9c179e358c1eaf7baf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:13 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:13:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:13:15 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:14:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:14:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b580e80688f1e334734aea2880fa5931e55370f3539fc8e78058543d2fbb4`  
		Last Modified: Tue, 11 Mar 2025 18:14:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec1357c0e2eb61ac9298926dd9084156bd2d05dcea183ea8786979784c324`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a8e2f5c7e51683c21328502741d075647e87f5e9d195902a79b4362af9708`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a47c47f5f7ce9891789821dc08dbb73af7a03679e28d975173ca02457a3c85`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b401c362d821c447b22c6303f6e897b6cc2098aab4b7061cdd239ad38f00356`  
		Last Modified: Tue, 11 Mar 2025 18:15:03 GMT  
		Size: 265.1 MB (265140438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a26224618776b48b976e6718b0c66dc407c2f1423a2a911b49b31fa347919`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.4`

```console
$ docker pull julia@sha256:3930bce3315aa328a039d06295aa25c759705b57b9946263ac8a817a2078a5cd
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
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.11.4` - linux; amd64

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

### `julia:1.11.4` - unknown; unknown

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

### `julia:1.11.4` - linux; arm64 variant v8

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

### `julia:1.11.4` - unknown; unknown

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

### `julia:1.11.4` - linux; 386

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

### `julia:1.11.4` - unknown; unknown

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

### `julia:1.11.4` - linux; ppc64le

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

### `julia:1.11.4` - unknown; unknown

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

### `julia:1.11.4` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:8acf88f620e712a0a209bfbccf0eed2dcc0b2946508997213353097da27d170e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081734503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cc4c1f77bbe2ff3fc6f90bcc7f0b4d7d47e9aa0617b9c179e358c1eaf7baf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:13 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:13:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:13:15 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:14:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:14:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b580e80688f1e334734aea2880fa5931e55370f3539fc8e78058543d2fbb4`  
		Last Modified: Tue, 11 Mar 2025 18:14:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec1357c0e2eb61ac9298926dd9084156bd2d05dcea183ea8786979784c324`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a8e2f5c7e51683c21328502741d075647e87f5e9d195902a79b4362af9708`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a47c47f5f7ce9891789821dc08dbb73af7a03679e28d975173ca02457a3c85`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b401c362d821c447b22c6303f6e897b6cc2098aab4b7061cdd239ad38f00356`  
		Last Modified: Tue, 11 Mar 2025 18:15:03 GMT  
		Size: 265.1 MB (265140438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a26224618776b48b976e6718b0c66dc407c2f1423a2a911b49b31fa347919`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.4` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:4ec46cc1e5ec14205a112b7bcf25d17feb1195c4427bea62804de7c93aa1d464
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528934099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdb17d614282c158734ba03f7db6e9dc4b123d2b2fa012b800e11be2b66dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e613cb0bd6b9cdefc91ef48f6b84eafc8bfedc674b985f05222969a1e708d2`  
		Last Modified: Tue, 11 Mar 2025 18:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55928cd0613a4698f021e84a732f32008287c1079893322ef0577d3b68e1d7e3`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769b36b1b267ac98d3c0b181635a870dbbb219e2ce05ed2bc0e25172e009aaa`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc75c329d096e43a1095e057c53bce7d7b5fa96ca5a61ad0a496b1e89bd34f`  
		Last Modified: Tue, 11 Mar 2025 18:11:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de433e53b119c1cea9de09b3637d6600006b928c83e8554570ae155ad81392d0`  
		Last Modified: Tue, 11 Mar 2025 18:11:58 GMT  
		Size: 265.1 MB (265069668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734d83e3be039a110407a2e7cd36a59ad3f092bf4f426da5936550ea2e7e933`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.4` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.4-bookworm`

```console
$ docker pull julia@sha256:399302474cb5ef2ccf216c1c73c97c7bf0a39666c35c6d80ef67ba01fb6aa3ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11.4-bookworm` - linux; amd64

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

### `julia:1.11.4-bookworm` - unknown; unknown

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

### `julia:1.11.4-bookworm` - linux; arm64 variant v8

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

### `julia:1.11.4-bookworm` - unknown; unknown

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

### `julia:1.11.4-bookworm` - linux; 386

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

### `julia:1.11.4-bookworm` - unknown; unknown

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

### `julia:1.11.4-bookworm` - linux; ppc64le

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

### `julia:1.11.4-bookworm` - unknown; unknown

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

## `julia:1.11.4-bullseye`

```console
$ docker pull julia@sha256:8a5776a35daa3f5821996974b6bfccbca0acb93c57adb7be66f808fd48601b35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11.4-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:72c9ae493b9eca82f0c07a276f2f0b4f7863d119474f66f8586eefa0a8053ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300961401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c67a903937f5891a72c30c6adc5ed4626c951909fa33c301f1aa5aa4c45948`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7165c83944224063d633634d136cf1bf62f390d866ccb2ae699c012548aac6`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 2.2 MB (2222654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725e528a3666541c2953691421b6a228673594440c7d539fb35f71fc2a46be48`  
		Last Modified: Tue, 11 Mar 2025 17:58:00 GMT  
		Size: 268.5 MB (268484444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d38f27ed12d5f890c2121a4a56d39f8767d3f6cbb1c14d39ddfbb22f45e415`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.4-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8a02228943143116153ce0d2488cd203e6ce948bb248949bcb0429c8686408b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91301a3221f1b9ae49dc24f7c05ad6161194f3e57f108ca52589d84115267526`

```dockerfile
```

-	Layers:
	-	`sha256:fc3a810a8f575b0ac14f3c720fac7a97fde163cba0299bdb59633c6e09cd7717`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7391d4ac599c40348906465dcc052d096f6db456615fe307bd2b39cb79da36c5`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.4-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dc6141754eb15dc1abb94a4e67d1c698f01f879691520bdc23842d794c80adda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (314957093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f10b2054506b5f7fbdf5f4b4cc409f99caaf7ba0559d1ce43fcad496c62ed92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc5dc01c337dce742e7c6026ccf096f7b1c09278ca05a29613e61d8fe553208`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 2.2 MB (2210309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47705c544b0c43fa505ea4141d20e1bd7047b8da8398c7a5e3d1214f40573e1`  
		Last Modified: Tue, 11 Mar 2025 17:59:35 GMT  
		Size: 284.0 MB (284000422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e906007b13ae7c53726d61e1006d643af01db9a126dcf54f834921cca9a146a`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.4-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:063ec1c56311e72dc3969d58c12069c7431f9663a075fb5fbca0ecea6b4fadb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8736a85ebdb295f549dc129bf2389633fae54193cc5512562d7d6452465fdb`

```dockerfile
```

-	Layers:
	-	`sha256:f153b82ac16be75d5ce35c461d4642790760c612f40500aba30fd809ff482f9d`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3990310fdd52100587e443fc54cd91ffdd102077037c0b0003599851c0c10ca7`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.4-bullseye` - linux; 386

```console
$ docker pull julia@sha256:415eda97c01612223e23e19484ef8c99744317636dc5c495c6a3ce456ce2c57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251354410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a238940033d7286786b0a0ebdb5f1de9242b3576a705221eccc3e647c6a3a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768dc8869224f294d9e2ae8231a8c8a74f708a8e5495e183d94dfbedf98d3816`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 2.3 MB (2328071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e4bd659adb5b6bdf7cd848dd04bdd531234e9725242266aa53357febdcb23a`  
		Last Modified: Tue, 11 Mar 2025 17:57:47 GMT  
		Size: 217.8 MB (217845544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706ff1c0df0fa586527b601c6e9c2b526f2521b19a51b12649fedbc429419671`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.4-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:257c12809f8a9b581f7dde263775c80db30df53d4fcf13cd4fd1820599b3ce66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0464719ad93ca07e66b0669a89f783025f238fad94ecff01f027d6f292c6ea`

```dockerfile
```

-	Layers:
	-	`sha256:e12e0dd0133063f2b20338f66514bc5628916b5506a86b7491ad172daa119aab`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b13c04845b43675f6fc2c6eb60313e14e089c471deb5b03bff80a58579050c65`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 17.2 KB (17195 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.4-windowsservercore`

```console
$ docker pull julia@sha256:558e56296c78e7898fafefc944345bcb81b21a48f6137d1b8c9a74322b32c243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.11.4-windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:8acf88f620e712a0a209bfbccf0eed2dcc0b2946508997213353097da27d170e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081734503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cc4c1f77bbe2ff3fc6f90bcc7f0b4d7d47e9aa0617b9c179e358c1eaf7baf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:13 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:13:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:13:15 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:14:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:14:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b580e80688f1e334734aea2880fa5931e55370f3539fc8e78058543d2fbb4`  
		Last Modified: Tue, 11 Mar 2025 18:14:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec1357c0e2eb61ac9298926dd9084156bd2d05dcea183ea8786979784c324`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a8e2f5c7e51683c21328502741d075647e87f5e9d195902a79b4362af9708`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a47c47f5f7ce9891789821dc08dbb73af7a03679e28d975173ca02457a3c85`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b401c362d821c447b22c6303f6e897b6cc2098aab4b7061cdd239ad38f00356`  
		Last Modified: Tue, 11 Mar 2025 18:15:03 GMT  
		Size: 265.1 MB (265140438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a26224618776b48b976e6718b0c66dc407c2f1423a2a911b49b31fa347919`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.4-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:4ec46cc1e5ec14205a112b7bcf25d17feb1195c4427bea62804de7c93aa1d464
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528934099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdb17d614282c158734ba03f7db6e9dc4b123d2b2fa012b800e11be2b66dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e613cb0bd6b9cdefc91ef48f6b84eafc8bfedc674b985f05222969a1e708d2`  
		Last Modified: Tue, 11 Mar 2025 18:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55928cd0613a4698f021e84a732f32008287c1079893322ef0577d3b68e1d7e3`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769b36b1b267ac98d3c0b181635a870dbbb219e2ce05ed2bc0e25172e009aaa`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc75c329d096e43a1095e057c53bce7d7b5fa96ca5a61ad0a496b1e89bd34f`  
		Last Modified: Tue, 11 Mar 2025 18:11:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de433e53b119c1cea9de09b3637d6600006b928c83e8554570ae155ad81392d0`  
		Last Modified: Tue, 11 Mar 2025 18:11:58 GMT  
		Size: 265.1 MB (265069668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734d83e3be039a110407a2e7cd36a59ad3f092bf4f426da5936550ea2e7e933`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.4-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.4-windowsservercore-1809`

```console
$ docker pull julia@sha256:f6329f6ba2acb70fa9e6ebbc91d4d536d0672c1f7305a02fbbef863042afb5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:1.11.4-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.4-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:48b3643c0c3cd7f12c11619010332d97e6a3023a78fd6e385b1ee9934378d93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1.11.4-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:4ec46cc1e5ec14205a112b7bcf25d17feb1195c4427bea62804de7c93aa1d464
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528934099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdb17d614282c158734ba03f7db6e9dc4b123d2b2fa012b800e11be2b66dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e613cb0bd6b9cdefc91ef48f6b84eafc8bfedc674b985f05222969a1e708d2`  
		Last Modified: Tue, 11 Mar 2025 18:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55928cd0613a4698f021e84a732f32008287c1079893322ef0577d3b68e1d7e3`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769b36b1b267ac98d3c0b181635a870dbbb219e2ce05ed2bc0e25172e009aaa`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc75c329d096e43a1095e057c53bce7d7b5fa96ca5a61ad0a496b1e89bd34f`  
		Last Modified: Tue, 11 Mar 2025 18:11:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de433e53b119c1cea9de09b3637d6600006b928c83e8554570ae155ad81392d0`  
		Last Modified: Tue, 11 Mar 2025 18:11:58 GMT  
		Size: 265.1 MB (265069668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734d83e3be039a110407a2e7cd36a59ad3f092bf4f426da5936550ea2e7e933`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.4-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:77810f8d3cfceabad6bc16d6a389038ef89b0aca5c3042647606edd4eb74e52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `julia:1.11.4-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:8acf88f620e712a0a209bfbccf0eed2dcc0b2946508997213353097da27d170e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081734503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cc4c1f77bbe2ff3fc6f90bcc7f0b4d7d47e9aa0617b9c179e358c1eaf7baf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:13 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:13:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:13:15 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:14:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:14:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b580e80688f1e334734aea2880fa5931e55370f3539fc8e78058543d2fbb4`  
		Last Modified: Tue, 11 Mar 2025 18:14:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec1357c0e2eb61ac9298926dd9084156bd2d05dcea183ea8786979784c324`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a8e2f5c7e51683c21328502741d075647e87f5e9d195902a79b4362af9708`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a47c47f5f7ce9891789821dc08dbb73af7a03679e28d975173ca02457a3c85`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b401c362d821c447b22c6303f6e897b6cc2098aab4b7061cdd239ad38f00356`  
		Last Modified: Tue, 11 Mar 2025 18:15:03 GMT  
		Size: 265.1 MB (265140438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a26224618776b48b976e6718b0c66dc407c2f1423a2a911b49b31fa347919`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bookworm`

```console
$ docker pull julia@sha256:399302474cb5ef2ccf216c1c73c97c7bf0a39666c35c6d80ef67ba01fb6aa3ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:bookworm` - linux; amd64

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

### `julia:bookworm` - unknown; unknown

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

### `julia:bookworm` - linux; arm64 variant v8

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

### `julia:bookworm` - unknown; unknown

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

### `julia:bookworm` - linux; 386

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

### `julia:bookworm` - unknown; unknown

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

### `julia:bookworm` - linux; ppc64le

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

### `julia:bookworm` - unknown; unknown

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

## `julia:bullseye`

```console
$ docker pull julia@sha256:8a5776a35daa3f5821996974b6bfccbca0acb93c57adb7be66f808fd48601b35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:72c9ae493b9eca82f0c07a276f2f0b4f7863d119474f66f8586eefa0a8053ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300961401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c67a903937f5891a72c30c6adc5ed4626c951909fa33c301f1aa5aa4c45948`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7165c83944224063d633634d136cf1bf62f390d866ccb2ae699c012548aac6`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 2.2 MB (2222654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725e528a3666541c2953691421b6a228673594440c7d539fb35f71fc2a46be48`  
		Last Modified: Tue, 11 Mar 2025 17:58:00 GMT  
		Size: 268.5 MB (268484444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d38f27ed12d5f890c2121a4a56d39f8767d3f6cbb1c14d39ddfbb22f45e415`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8a02228943143116153ce0d2488cd203e6ce948bb248949bcb0429c8686408b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91301a3221f1b9ae49dc24f7c05ad6161194f3e57f108ca52589d84115267526`

```dockerfile
```

-	Layers:
	-	`sha256:fc3a810a8f575b0ac14f3c720fac7a97fde163cba0299bdb59633c6e09cd7717`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7391d4ac599c40348906465dcc052d096f6db456615fe307bd2b39cb79da36c5`  
		Last Modified: Tue, 11 Mar 2025 17:57:56 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dc6141754eb15dc1abb94a4e67d1c698f01f879691520bdc23842d794c80adda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.0 MB (314957093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f10b2054506b5f7fbdf5f4b4cc409f99caaf7ba0559d1ce43fcad496c62ed92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc5dc01c337dce742e7c6026ccf096f7b1c09278ca05a29613e61d8fe553208`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 2.2 MB (2210309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47705c544b0c43fa505ea4141d20e1bd7047b8da8398c7a5e3d1214f40573e1`  
		Last Modified: Tue, 11 Mar 2025 17:59:35 GMT  
		Size: 284.0 MB (284000422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e906007b13ae7c53726d61e1006d643af01db9a126dcf54f834921cca9a146a`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:063ec1c56311e72dc3969d58c12069c7431f9663a075fb5fbca0ecea6b4fadb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8736a85ebdb295f549dc129bf2389633fae54193cc5512562d7d6452465fdb`

```dockerfile
```

-	Layers:
	-	`sha256:f153b82ac16be75d5ce35c461d4642790760c612f40500aba30fd809ff482f9d`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3990310fdd52100587e443fc54cd91ffdd102077037c0b0003599851c0c10ca7`  
		Last Modified: Tue, 11 Mar 2025 17:59:27 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:415eda97c01612223e23e19484ef8c99744317636dc5c495c6a3ce456ce2c57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251354410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a238940033d7286786b0a0ebdb5f1de9242b3576a705221eccc3e647c6a3a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768dc8869224f294d9e2ae8231a8c8a74f708a8e5495e183d94dfbedf98d3816`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 2.3 MB (2328071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e4bd659adb5b6bdf7cd848dd04bdd531234e9725242266aa53357febdcb23a`  
		Last Modified: Tue, 11 Mar 2025 17:57:47 GMT  
		Size: 217.8 MB (217845544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706ff1c0df0fa586527b601c6e9c2b526f2521b19a51b12649fedbc429419671`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:257c12809f8a9b581f7dde263775c80db30df53d4fcf13cd4fd1820599b3ce66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0464719ad93ca07e66b0669a89f783025f238fad94ecff01f027d6f292c6ea`

```dockerfile
```

-	Layers:
	-	`sha256:e12e0dd0133063f2b20338f66514bc5628916b5506a86b7491ad172daa119aab`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b13c04845b43675f6fc2c6eb60313e14e089c471deb5b03bff80a58579050c65`  
		Last Modified: Tue, 11 Mar 2025 17:57:41 GMT  
		Size: 17.2 KB (17195 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:3930bce3315aa328a039d06295aa25c759705b57b9946263ac8a817a2078a5cd
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
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

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

### `julia:latest` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:8acf88f620e712a0a209bfbccf0eed2dcc0b2946508997213353097da27d170e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081734503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cc4c1f77bbe2ff3fc6f90bcc7f0b4d7d47e9aa0617b9c179e358c1eaf7baf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:13 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:13:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:13:15 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:14:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:14:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b580e80688f1e334734aea2880fa5931e55370f3539fc8e78058543d2fbb4`  
		Last Modified: Tue, 11 Mar 2025 18:14:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec1357c0e2eb61ac9298926dd9084156bd2d05dcea183ea8786979784c324`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a8e2f5c7e51683c21328502741d075647e87f5e9d195902a79b4362af9708`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a47c47f5f7ce9891789821dc08dbb73af7a03679e28d975173ca02457a3c85`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b401c362d821c447b22c6303f6e897b6cc2098aab4b7061cdd239ad38f00356`  
		Last Modified: Tue, 11 Mar 2025 18:15:03 GMT  
		Size: 265.1 MB (265140438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a26224618776b48b976e6718b0c66dc407c2f1423a2a911b49b31fa347919`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:4ec46cc1e5ec14205a112b7bcf25d17feb1195c4427bea62804de7c93aa1d464
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528934099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdb17d614282c158734ba03f7db6e9dc4b123d2b2fa012b800e11be2b66dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e613cb0bd6b9cdefc91ef48f6b84eafc8bfedc674b985f05222969a1e708d2`  
		Last Modified: Tue, 11 Mar 2025 18:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55928cd0613a4698f021e84a732f32008287c1079893322ef0577d3b68e1d7e3`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769b36b1b267ac98d3c0b181635a870dbbb219e2ce05ed2bc0e25172e009aaa`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc75c329d096e43a1095e057c53bce7d7b5fa96ca5a61ad0a496b1e89bd34f`  
		Last Modified: Tue, 11 Mar 2025 18:11:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de433e53b119c1cea9de09b3637d6600006b928c83e8554570ae155ad81392d0`  
		Last Modified: Tue, 11 Mar 2025 18:11:58 GMT  
		Size: 265.1 MB (265069668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734d83e3be039a110407a2e7cd36a59ad3f092bf4f426da5936550ea2e7e933`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:558e56296c78e7898fafefc944345bcb81b21a48f6137d1b8c9a74322b32c243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:8acf88f620e712a0a209bfbccf0eed2dcc0b2946508997213353097da27d170e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081734503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cc4c1f77bbe2ff3fc6f90bcc7f0b4d7d47e9aa0617b9c179e358c1eaf7baf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:13 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:13:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:13:15 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:14:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:14:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b580e80688f1e334734aea2880fa5931e55370f3539fc8e78058543d2fbb4`  
		Last Modified: Tue, 11 Mar 2025 18:14:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec1357c0e2eb61ac9298926dd9084156bd2d05dcea183ea8786979784c324`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a8e2f5c7e51683c21328502741d075647e87f5e9d195902a79b4362af9708`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a47c47f5f7ce9891789821dc08dbb73af7a03679e28d975173ca02457a3c85`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b401c362d821c447b22c6303f6e897b6cc2098aab4b7061cdd239ad38f00356`  
		Last Modified: Tue, 11 Mar 2025 18:15:03 GMT  
		Size: 265.1 MB (265140438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a26224618776b48b976e6718b0c66dc407c2f1423a2a911b49b31fa347919`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:4ec46cc1e5ec14205a112b7bcf25d17feb1195c4427bea62804de7c93aa1d464
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528934099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdb17d614282c158734ba03f7db6e9dc4b123d2b2fa012b800e11be2b66dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e613cb0bd6b9cdefc91ef48f6b84eafc8bfedc674b985f05222969a1e708d2`  
		Last Modified: Tue, 11 Mar 2025 18:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55928cd0613a4698f021e84a732f32008287c1079893322ef0577d3b68e1d7e3`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769b36b1b267ac98d3c0b181635a870dbbb219e2ce05ed2bc0e25172e009aaa`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc75c329d096e43a1095e057c53bce7d7b5fa96ca5a61ad0a496b1e89bd34f`  
		Last Modified: Tue, 11 Mar 2025 18:11:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de433e53b119c1cea9de09b3637d6600006b928c83e8554570ae155ad81392d0`  
		Last Modified: Tue, 11 Mar 2025 18:11:58 GMT  
		Size: 265.1 MB (265069668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734d83e3be039a110407a2e7cd36a59ad3f092bf4f426da5936550ea2e7e933`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:f6329f6ba2acb70fa9e6ebbc91d4d536d0672c1f7305a02fbbef863042afb5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:8ad31d1752b1f0c669803070b0e8bbe64eddfb056b7eda49ad799ec57a62541c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401936804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923e316cbf91463823c056fc4e266d582af13f82f2707b7d1603d6ff4012a3ca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 11 Mar 2025 18:08:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:47 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e793f4a27ada1921fa7a6f35c350c6e3c5f0bca9fc42397359a97ad93278f6cf`  
		Last Modified: Tue, 11 Mar 2025 18:11:32 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd2a5605b3c55b8feadde212c716b76a7a3e5a33771696234ece8d402201b25`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9389350b152c012a9e291e7b563cdd7ff4c7c2d03c59e29e29be9acb1fb569c`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c0bc11e47454553d037f9a67d969af3c4c0f792e25e6bee65d057f42753237`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3216fcc008d4a46867539098843cd7d58ea318ca98750c4c96ba5ca0cd9b05d5`  
		Last Modified: Tue, 11 Mar 2025 18:12:05 GMT  
		Size: 265.0 MB (265021483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f5a886dc471f9ee592ab5c28b09da0e88d6aff3c1e4f6ea5229d404fcb761`  
		Last Modified: Tue, 11 Mar 2025 18:11:30 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:48b3643c0c3cd7f12c11619010332d97e6a3023a78fd6e385b1ee9934378d93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:4ec46cc1e5ec14205a112b7bcf25d17feb1195c4427bea62804de7c93aa1d464
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528934099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7bdb17d614282c158734ba03f7db6e9dc4b123d2b2fa012b800e11be2b66dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 11 Mar 2025 18:08:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:08:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:08:46 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:11:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:11:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e613cb0bd6b9cdefc91ef48f6b84eafc8bfedc674b985f05222969a1e708d2`  
		Last Modified: Tue, 11 Mar 2025 18:11:27 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55928cd0613a4698f021e84a732f32008287c1079893322ef0577d3b68e1d7e3`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6769b36b1b267ac98d3c0b181635a870dbbb219e2ce05ed2bc0e25172e009aaa`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc75c329d096e43a1095e057c53bce7d7b5fa96ca5a61ad0a496b1e89bd34f`  
		Last Modified: Tue, 11 Mar 2025 18:11:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de433e53b119c1cea9de09b3637d6600006b928c83e8554570ae155ad81392d0`  
		Last Modified: Tue, 11 Mar 2025 18:11:58 GMT  
		Size: 265.1 MB (265069668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8734d83e3be039a110407a2e7cd36a59ad3f092bf4f426da5936550ea2e7e933`  
		Last Modified: Tue, 11 Mar 2025 18:11:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:77810f8d3cfceabad6bc16d6a389038ef89b0aca5c3042647606edd4eb74e52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:8acf88f620e712a0a209bfbccf0eed2dcc0b2946508997213353097da27d170e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081734503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831cc4c1f77bbe2ff3fc6f90bcc7f0b4d7d47e9aa0617b9c179e358c1eaf7baf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Tue, 11 Mar 2025 18:13:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Mar 2025 18:13:13 GMT
ENV JULIA_VERSION=1.11.4
# Tue, 11 Mar 2025 18:13:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.4-win64.exe
# Tue, 11 Mar 2025 18:13:15 GMT
ENV JULIA_SHA256=afdbf24eac425086753d672f04c09b892423ec10ff905c9a773277fad16ae8ce
# Tue, 11 Mar 2025 18:14:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Mar 2025 18:14:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559b580e80688f1e334734aea2880fa5931e55370f3539fc8e78058543d2fbb4`  
		Last Modified: Tue, 11 Mar 2025 18:14:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2ec1357c0e2eb61ac9298926dd9084156bd2d05dcea183ea8786979784c324`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033a8e2f5c7e51683c21328502741d075647e87f5e9d195902a79b4362af9708`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a47c47f5f7ce9891789821dc08dbb73af7a03679e28d975173ca02457a3c85`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b401c362d821c447b22c6303f6e897b6cc2098aab4b7061cdd239ad38f00356`  
		Last Modified: Tue, 11 Mar 2025 18:15:03 GMT  
		Size: 265.1 MB (265140438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a26224618776b48b976e6718b0c66dc407c2f1423a2a911b49b31fa347919`  
		Last Modified: Tue, 11 Mar 2025 18:14:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
