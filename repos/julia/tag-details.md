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
$ docker pull julia@sha256:01cc0092fb6793b4ad0a6f9f0d03660089e16abed71c6c69b44570c34d71d06f
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
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:580414c60d19e62298e89e9eb1127dd6f473a2774657828e7942efc4e9a65c28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081442433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a26e3c596df439e60599ef95126e620bcadd8a07e9d7c3d2a15a554a70debc`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 27 Feb 2025 18:19:00 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 27 Feb 2025 18:20:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:20:04 GMT
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
	-	`sha256:e9fdc02c27ab8440ae46b627a657673f4cd98a7796059a2bb4e9106c9aeb21d6`  
		Last Modified: Thu, 27 Feb 2025 18:20:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b680a25229271e6fd7cb1ebdc74da5ff6f4e4ada764930780edbff55bd04a3`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64b9b53f5526a424ae03d0a93bbdde5ab05c26d0ed76acb0fcaf19bda3c6d4f`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72753769a2de3c67535cc4e5521833c6a0de6fe45e4202963e90fa28559281fe`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed62356243026edb95a65bf17ba52e1776192a1a1998f783973173789c3c2936`  
		Last Modified: Thu, 27 Feb 2025 18:20:47 GMT  
		Size: 264.8 MB (264848359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b33da5e826269f7c9b668e1d0e4d753be5a3ad84f8e4a1abd3f09ae6d3ea3b`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
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
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
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
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:dfd895b0efb2e24cfb1f7b905368c1201724da48f6dd5e4810728e364cbff387
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
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
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
$ docker pull julia@sha256:1d1122bb36103f21a4c1cd63ae718bb9cc28c23b97000c043408b1a79a27add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1-windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:580414c60d19e62298e89e9eb1127dd6f473a2774657828e7942efc4e9a65c28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081442433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a26e3c596df439e60599ef95126e620bcadd8a07e9d7c3d2a15a554a70debc`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 27 Feb 2025 18:19:00 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 27 Feb 2025 18:20:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:20:04 GMT
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
	-	`sha256:e9fdc02c27ab8440ae46b627a657673f4cd98a7796059a2bb4e9106c9aeb21d6`  
		Last Modified: Thu, 27 Feb 2025 18:20:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b680a25229271e6fd7cb1ebdc74da5ff6f4e4ada764930780edbff55bd04a3`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64b9b53f5526a424ae03d0a93bbdde5ab05c26d0ed76acb0fcaf19bda3c6d4f`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72753769a2de3c67535cc4e5521833c6a0de6fe45e4202963e90fa28559281fe`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed62356243026edb95a65bf17ba52e1776192a1a1998f783973173789c3c2936`  
		Last Modified: Thu, 27 Feb 2025 18:20:47 GMT  
		Size: 264.8 MB (264848359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b33da5e826269f7c9b668e1d0e4d753be5a3ad84f8e4a1abd3f09ae6d3ea3b`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
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
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
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
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:2e7bd23cb87b2b1bd0cdcc013c54c0b618044b9750fe0527be5e012363a73f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
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
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:67a9470180bfe119828cda80614b5c765934f592f08dd030ae237136aff79352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
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
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:3d3f457a3b71660bf38adb6ea92286b29f1e342aba711815fa0cf72f8c92a0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:580414c60d19e62298e89e9eb1127dd6f473a2774657828e7942efc4e9a65c28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081442433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a26e3c596df439e60599ef95126e620bcadd8a07e9d7c3d2a15a554a70debc`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 27 Feb 2025 18:19:00 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 27 Feb 2025 18:20:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:20:04 GMT
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
	-	`sha256:e9fdc02c27ab8440ae46b627a657673f4cd98a7796059a2bb4e9106c9aeb21d6`  
		Last Modified: Thu, 27 Feb 2025 18:20:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b680a25229271e6fd7cb1ebdc74da5ff6f4e4ada764930780edbff55bd04a3`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64b9b53f5526a424ae03d0a93bbdde5ab05c26d0ed76acb0fcaf19bda3c6d4f`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72753769a2de3c67535cc4e5521833c6a0de6fe45e4202963e90fa28559281fe`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed62356243026edb95a65bf17ba52e1776192a1a1998f783973173789c3c2936`  
		Last Modified: Thu, 27 Feb 2025 18:20:47 GMT  
		Size: 264.8 MB (264848359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b33da5e826269f7c9b668e1d0e4d753be5a3ad84f8e4a1abd3f09ae6d3ea3b`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:58cb75fb0be5e2f9a631240677a973bc0394432b1ca884bf980184a368539a75
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
$ docker pull julia@sha256:e2098f0ec371c8d9544d0785b5b84647f8dab8b3f6cb50dd0631a0b39c83ff0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193459312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79611a383285f249aaee725495ccb56c1ec506f6cce28c08298f315b8d22c931`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a01e2350cb6f03b0da6d34b7ea67118dc4f0ee789279e0106e3e129ec4f2a1f`  
		Last Modified: Tue, 25 Feb 2025 02:36:23 GMT  
		Size: 155.2 MB (155157257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b90912e0605bcf3e5f1145012ba57e524d67ca2b53566f38bcd071077b3b7`  
		Last Modified: Tue, 25 Feb 2025 02:36:19 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:193328fad219591f1ebe48951e320b0d0ef8a074417ac72447204422a27409eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353333249b3cc3ccbf35310a0be7f9799c32b0a00de6b77197647599cb085a65`

```dockerfile
```

-	Layers:
	-	`sha256:bc375cc77ef1b96e128f67a0cc769ef1ffd2fe5fd98feb3390a049962a51b3a0`  
		Last Modified: Tue, 25 Feb 2025 02:36:20 GMT  
		Size: 2.4 MB (2448678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc454e075d0910fe622f24e0c3520fb73938b551685986a865d74f5d13356a33`  
		Last Modified: Tue, 25 Feb 2025 02:36:19 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:c20e6d39b5b15ceac309976935b7433692ceb4991a02a1f12e94c74328bf91a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3005288262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c744fec409b7a8b9c81497beacbcc9b8e1cd3930e099c042e4767ca75b476d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:19:00 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 27 Feb 2025 18:19:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 27 Feb 2025 18:19:05 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 27 Feb 2025 18:19:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:19:52 GMT
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
	-	`sha256:bfe3a6442bcb6568a2ddf5b69ddec3ab89a9476d9a9a87b1fd2699551ac14f25`  
		Last Modified: Thu, 27 Feb 2025 18:19:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad76bf1aede34687000191fd576cae81ccec02bbaded364db620f051558ea43`  
		Last Modified: Thu, 27 Feb 2025 18:19:55 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a30963f70e75e56847f580e5b84f30fdedcc79539013fd00c49b55f9d783c6b`  
		Last Modified: Thu, 27 Feb 2025 18:19:55 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb35810a682683430532940d023bfedbb488bc2602fc48cf59913f8fe64fc9e`  
		Last Modified: Thu, 27 Feb 2025 18:19:55 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201b636cd4f9393eeb08c06cddcfea112aa206b39e33fbe3f8d2ddb1ce16335`  
		Last Modified: Thu, 27 Feb 2025 18:20:23 GMT  
		Size: 188.7 MB (188694168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362e35f6568567e371a5d4b4720bf901f8d450bd8da0ef985e42b6f8fc6c8f3b`  
		Last Modified: Thu, 27 Feb 2025 18:19:55 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:ac79fdbb729145cb1bffbdcdac5c90f0659420b2c32a042db8e09ef5046c12ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452517945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a427a05613dcbebc39e69375a7a22c6de08dca1a906ce33785a88edddae738`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:37:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:37:49 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:38:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:44 GMT
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
	-	`sha256:4c7ed8e7202322ceebbde66bd5c17e8cb63f0a63deeba0dce25ca0165af4cd94`  
		Last Modified: Thu, 13 Feb 2025 00:38:48 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4113d463e8f59a011a182e6b4e5c59ca3b24501c020944150165d7923668fff5`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691753fae6105922bbdc47180303ef3e79f0262b36268f73c2ee704321a43dc1`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cedad76f34702d30642f568d3467dc6f1f420c3fc61ac77dfe77b68af40e468`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb673a4bf380f9c6a5308a15b2a2a57b82a2d923bc93c5afab400e3c1c1b838`  
		Last Modified: Thu, 13 Feb 2025 00:39:10 GMT  
		Size: 188.7 MB (188653406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d63bac5eabd3f54a59db28184d9bad8be6ad92dd626462ad51bc06e3f662db`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:9e3801b456c24260294efa77599c44818954fa48ec8a4a6f54bb5bbf57fc538a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325517602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d5322a337b2455c2f0d0235881437dfa635e05f9a936c4cb27dff5df3bbb53`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:34:08 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:35:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:19 GMT
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
	-	`sha256:6a8581044a74ef698a3ae34bab811faa129529027c7eb77a6b0c0754748f6055`  
		Last Modified: Thu, 13 Feb 2025 00:35:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79abe04602eb193952fd20451edc2e0c3edec25b5140860576ab8dd43434ccb`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45face97a75a56bdc0329ba85ac9adf2164e9692773043bba1e330df0a7701`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f5bde34f5706ee15891362936963912b7c2e41b557cf665abe48182cdd775b`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b58967fcbfa6fea8b02512fa1441f7ec6bd92d7623897ec3c826b7185d98f15`  
		Last Modified: Thu, 13 Feb 2025 00:35:47 GMT  
		Size: 188.6 MB (188602321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879ba356d441b938ba068b455cc2d082fac429a473b9dffa6f0f3eda32523be4`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1299 bytes)  
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
$ docker pull julia@sha256:cd76db5e1c2c9e7995340c5964ac158d1d9aa9f895440d64d9dfd357418b1f35
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
$ docker pull julia@sha256:e2098f0ec371c8d9544d0785b5b84647f8dab8b3f6cb50dd0631a0b39c83ff0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.5 MB (193459312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79611a383285f249aaee725495ccb56c1ec506f6cce28c08298f315b8d22c931`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Jan 2025 06:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Jan 2025 06:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Jan 2025 06:59:14 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 23 Jan 2025 06:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.8-linux-x86_64.tar.gz'; 			sha256='0410175aeec3df63173c15187f2083f179d40596d36fd3a57819cc5f522ae735'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.8-linux-aarch64.tar.gz'; 			sha256='8d63dd12595a08edc736be8d6c4fea1840f137b81c62079d970dbd1be448b8cd'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.8-linux-i686.tar.gz'; 			sha256='0258b5ae2aafc32f4b916b7aacc6887f7581a55e1726d7fb6f3655ed7e126430'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.8-linux-ppc64le.tar.gz'; 			sha256='6c10ba8ea349142dc0a14321ac17057e59ddf0fe925472f7fff1ead90c46a733'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Jan 2025 06:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2025 06:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a01e2350cb6f03b0da6d34b7ea67118dc4f0ee789279e0106e3e129ec4f2a1f`  
		Last Modified: Tue, 25 Feb 2025 02:36:23 GMT  
		Size: 155.2 MB (155157257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b90912e0605bcf3e5f1145012ba57e524d67ca2b53566f38bcd071077b3b7`  
		Last Modified: Tue, 25 Feb 2025 02:36:19 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:193328fad219591f1ebe48951e320b0d0ef8a074417ac72447204422a27409eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353333249b3cc3ccbf35310a0be7f9799c32b0a00de6b77197647599cb085a65`

```dockerfile
```

-	Layers:
	-	`sha256:bc375cc77ef1b96e128f67a0cc769ef1ffd2fe5fd98feb3390a049962a51b3a0`  
		Last Modified: Tue, 25 Feb 2025 02:36:20 GMT  
		Size: 2.4 MB (2448678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc454e075d0910fe622f24e0c3520fb73938b551685986a865d74f5d13356a33`  
		Last Modified: Tue, 25 Feb 2025 02:36:19 GMT  
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
$ docker pull julia@sha256:a5f91517030599caca26851a11c90d486c92ec81c611c2274ca8a343d409fc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:c20e6d39b5b15ceac309976935b7433692ceb4991a02a1f12e94c74328bf91a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3005288262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c744fec409b7a8b9c81497beacbcc9b8e1cd3930e099c042e4767ca75b476d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:19:00 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 27 Feb 2025 18:19:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 27 Feb 2025 18:19:05 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 27 Feb 2025 18:19:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:19:52 GMT
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
	-	`sha256:bfe3a6442bcb6568a2ddf5b69ddec3ab89a9476d9a9a87b1fd2699551ac14f25`  
		Last Modified: Thu, 27 Feb 2025 18:19:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad76bf1aede34687000191fd576cae81ccec02bbaded364db620f051558ea43`  
		Last Modified: Thu, 27 Feb 2025 18:19:55 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a30963f70e75e56847f580e5b84f30fdedcc79539013fd00c49b55f9d783c6b`  
		Last Modified: Thu, 27 Feb 2025 18:19:55 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb35810a682683430532940d023bfedbb488bc2602fc48cf59913f8fe64fc9e`  
		Last Modified: Thu, 27 Feb 2025 18:19:55 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201b636cd4f9393eeb08c06cddcfea112aa206b39e33fbe3f8d2ddb1ce16335`  
		Last Modified: Thu, 27 Feb 2025 18:20:23 GMT  
		Size: 188.7 MB (188694168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362e35f6568567e371a5d4b4720bf901f8d450bd8da0ef985e42b6f8fc6c8f3b`  
		Last Modified: Thu, 27 Feb 2025 18:19:55 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:ac79fdbb729145cb1bffbdcdac5c90f0659420b2c32a042db8e09ef5046c12ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452517945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a427a05613dcbebc39e69375a7a22c6de08dca1a906ce33785a88edddae738`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:37:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:37:49 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:38:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:44 GMT
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
	-	`sha256:4c7ed8e7202322ceebbde66bd5c17e8cb63f0a63deeba0dce25ca0165af4cd94`  
		Last Modified: Thu, 13 Feb 2025 00:38:48 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4113d463e8f59a011a182e6b4e5c59ca3b24501c020944150165d7923668fff5`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691753fae6105922bbdc47180303ef3e79f0262b36268f73c2ee704321a43dc1`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cedad76f34702d30642f568d3467dc6f1f420c3fc61ac77dfe77b68af40e468`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb673a4bf380f9c6a5308a15b2a2a57b82a2d923bc93c5afab400e3c1c1b838`  
		Last Modified: Thu, 13 Feb 2025 00:39:10 GMT  
		Size: 188.7 MB (188653406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d63bac5eabd3f54a59db28184d9bad8be6ad92dd626462ad51bc06e3f662db`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:9e3801b456c24260294efa77599c44818954fa48ec8a4a6f54bb5bbf57fc538a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325517602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d5322a337b2455c2f0d0235881437dfa635e05f9a936c4cb27dff5df3bbb53`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:34:08 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:35:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:19 GMT
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
	-	`sha256:6a8581044a74ef698a3ae34bab811faa129529027c7eb77a6b0c0754748f6055`  
		Last Modified: Thu, 13 Feb 2025 00:35:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79abe04602eb193952fd20451edc2e0c3edec25b5140860576ab8dd43434ccb`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45face97a75a56bdc0329ba85ac9adf2164e9692773043bba1e330df0a7701`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f5bde34f5706ee15891362936963912b7c2e41b557cf665abe48182cdd775b`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b58967fcbfa6fea8b02512fa1441f7ec6bd92d7623897ec3c826b7185d98f15`  
		Last Modified: Thu, 13 Feb 2025 00:35:47 GMT  
		Size: 188.6 MB (188602321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879ba356d441b938ba068b455cc2d082fac429a473b9dffa6f0f3eda32523be4`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:507c37ca88e0d966becafe997ce6dc105fa3cfa7c09182b23bf1f2ff3898c1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:9e3801b456c24260294efa77599c44818954fa48ec8a4a6f54bb5bbf57fc538a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2325517602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d5322a337b2455c2f0d0235881437dfa635e05f9a936c4cb27dff5df3bbb53`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:34:08 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:34:09 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:35:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:19 GMT
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
	-	`sha256:6a8581044a74ef698a3ae34bab811faa129529027c7eb77a6b0c0754748f6055`  
		Last Modified: Thu, 13 Feb 2025 00:35:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79abe04602eb193952fd20451edc2e0c3edec25b5140860576ab8dd43434ccb`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45face97a75a56bdc0329ba85ac9adf2164e9692773043bba1e330df0a7701`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f5bde34f5706ee15891362936963912b7c2e41b557cf665abe48182cdd775b`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b58967fcbfa6fea8b02512fa1441f7ec6bd92d7623897ec3c826b7185d98f15`  
		Last Modified: Thu, 13 Feb 2025 00:35:47 GMT  
		Size: 188.6 MB (188602321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879ba356d441b938ba068b455cc2d082fac429a473b9dffa6f0f3eda32523be4`  
		Last Modified: Thu, 13 Feb 2025 00:35:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:6ea0f734de4588ffd1d83678be1e21a39d6af7576cf876e5426c51c900b2c72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:ac79fdbb729145cb1bffbdcdac5c90f0659420b2c32a042db8e09ef5046c12ba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2452517945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a427a05613dcbebc39e69375a7a22c6de08dca1a906ce33785a88edddae738`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:47 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 13 Feb 2025 00:37:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 13 Feb 2025 00:37:49 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 13 Feb 2025 00:38:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:44 GMT
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
	-	`sha256:4c7ed8e7202322ceebbde66bd5c17e8cb63f0a63deeba0dce25ca0165af4cd94`  
		Last Modified: Thu, 13 Feb 2025 00:38:48 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4113d463e8f59a011a182e6b4e5c59ca3b24501c020944150165d7923668fff5`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691753fae6105922bbdc47180303ef3e79f0262b36268f73c2ee704321a43dc1`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cedad76f34702d30642f568d3467dc6f1f420c3fc61ac77dfe77b68af40e468`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb673a4bf380f9c6a5308a15b2a2a57b82a2d923bc93c5afab400e3c1c1b838`  
		Last Modified: Thu, 13 Feb 2025 00:39:10 GMT  
		Size: 188.7 MB (188653406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d63bac5eabd3f54a59db28184d9bad8be6ad92dd626462ad51bc06e3f662db`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:de19d4d8f0ca46489417ed69d73b6682f787dbe9546cb6fe27d21603b287d98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `julia:1.10-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:c20e6d39b5b15ceac309976935b7433692ceb4991a02a1f12e94c74328bf91a9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3005288262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c744fec409b7a8b9c81497beacbcc9b8e1cd3930e099c042e4767ca75b476d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:19:00 GMT
ENV JULIA_VERSION=1.10.8
# Thu, 27 Feb 2025 18:19:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.8-win64.exe
# Thu, 27 Feb 2025 18:19:05 GMT
ENV JULIA_SHA256=79d0cb8d6d4c36f1cab5c62a59232f6d54d5c7809fb981396bd88906d3e1b511
# Thu, 27 Feb 2025 18:19:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:19:52 GMT
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
	-	`sha256:bfe3a6442bcb6568a2ddf5b69ddec3ab89a9476d9a9a87b1fd2699551ac14f25`  
		Last Modified: Thu, 27 Feb 2025 18:19:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad76bf1aede34687000191fd576cae81ccec02bbaded364db620f051558ea43`  
		Last Modified: Thu, 27 Feb 2025 18:19:55 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a30963f70e75e56847f580e5b84f30fdedcc79539013fd00c49b55f9d783c6b`  
		Last Modified: Thu, 27 Feb 2025 18:19:55 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb35810a682683430532940d023bfedbb488bc2602fc48cf59913f8fe64fc9e`  
		Last Modified: Thu, 27 Feb 2025 18:19:55 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201b636cd4f9393eeb08c06cddcfea112aa206b39e33fbe3f8d2ddb1ce16335`  
		Last Modified: Thu, 27 Feb 2025 18:20:23 GMT  
		Size: 188.7 MB (188694168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362e35f6568567e371a5d4b4720bf901f8d450bd8da0ef985e42b6f8fc6c8f3b`  
		Last Modified: Thu, 27 Feb 2025 18:19:55 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.9`

```console
$ docker pull julia@sha256:b344c89d9facf14edc5d24c2031c7cbcb56c3892e9abceb4c19a4f8d97ce7eaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

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
$ docker pull julia@sha256:b344c89d9facf14edc5d24c2031c7cbcb56c3892e9abceb4c19a4f8d97ce7eaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
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
$ docker pull julia@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `julia:1.10.9-windowsservercore-1809`

```console
$ docker pull julia@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `julia:1.10.9-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `julia:1.10.9-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `julia:1.11`

```console
$ docker pull julia@sha256:01cc0092fb6793b4ad0a6f9f0d03660089e16abed71c6c69b44570c34d71d06f
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
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:580414c60d19e62298e89e9eb1127dd6f473a2774657828e7942efc4e9a65c28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081442433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a26e3c596df439e60599ef95126e620bcadd8a07e9d7c3d2a15a554a70debc`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 27 Feb 2025 18:19:00 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 27 Feb 2025 18:20:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:20:04 GMT
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
	-	`sha256:e9fdc02c27ab8440ae46b627a657673f4cd98a7796059a2bb4e9106c9aeb21d6`  
		Last Modified: Thu, 27 Feb 2025 18:20:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b680a25229271e6fd7cb1ebdc74da5ff6f4e4ada764930780edbff55bd04a3`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64b9b53f5526a424ae03d0a93bbdde5ab05c26d0ed76acb0fcaf19bda3c6d4f`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72753769a2de3c67535cc4e5521833c6a0de6fe45e4202963e90fa28559281fe`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed62356243026edb95a65bf17ba52e1776192a1a1998f783973173789c3c2936`  
		Last Modified: Thu, 27 Feb 2025 18:20:47 GMT  
		Size: 264.8 MB (264848359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b33da5e826269f7c9b668e1d0e4d753be5a3ad84f8e4a1abd3f09ae6d3ea3b`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
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
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
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
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:dfd895b0efb2e24cfb1f7b905368c1201724da48f6dd5e4810728e364cbff387
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
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
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
$ docker pull julia@sha256:1d1122bb36103f21a4c1cd63ae718bb9cc28c23b97000c043408b1a79a27add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:580414c60d19e62298e89e9eb1127dd6f473a2774657828e7942efc4e9a65c28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081442433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a26e3c596df439e60599ef95126e620bcadd8a07e9d7c3d2a15a554a70debc`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 27 Feb 2025 18:19:00 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 27 Feb 2025 18:20:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:20:04 GMT
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
	-	`sha256:e9fdc02c27ab8440ae46b627a657673f4cd98a7796059a2bb4e9106c9aeb21d6`  
		Last Modified: Thu, 27 Feb 2025 18:20:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b680a25229271e6fd7cb1ebdc74da5ff6f4e4ada764930780edbff55bd04a3`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64b9b53f5526a424ae03d0a93bbdde5ab05c26d0ed76acb0fcaf19bda3c6d4f`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72753769a2de3c67535cc4e5521833c6a0de6fe45e4202963e90fa28559281fe`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed62356243026edb95a65bf17ba52e1776192a1a1998f783973173789c3c2936`  
		Last Modified: Thu, 27 Feb 2025 18:20:47 GMT  
		Size: 264.8 MB (264848359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b33da5e826269f7c9b668e1d0e4d753be5a3ad84f8e4a1abd3f09ae6d3ea3b`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
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
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
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
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-1809`

```console
$ docker pull julia@sha256:2e7bd23cb87b2b1bd0cdcc013c54c0b618044b9750fe0527be5e012363a73f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:1.11-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
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
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:67a9470180bfe119828cda80614b5c765934f592f08dd030ae237136aff79352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
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
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:3d3f457a3b71660bf38adb6ea92286b29f1e342aba711815fa0cf72f8c92a0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `julia:1.11-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:580414c60d19e62298e89e9eb1127dd6f473a2774657828e7942efc4e9a65c28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081442433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a26e3c596df439e60599ef95126e620bcadd8a07e9d7c3d2a15a554a70debc`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 27 Feb 2025 18:19:00 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 27 Feb 2025 18:20:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:20:04 GMT
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
	-	`sha256:e9fdc02c27ab8440ae46b627a657673f4cd98a7796059a2bb4e9106c9aeb21d6`  
		Last Modified: Thu, 27 Feb 2025 18:20:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b680a25229271e6fd7cb1ebdc74da5ff6f4e4ada764930780edbff55bd04a3`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64b9b53f5526a424ae03d0a93bbdde5ab05c26d0ed76acb0fcaf19bda3c6d4f`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72753769a2de3c67535cc4e5521833c6a0de6fe45e4202963e90fa28559281fe`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed62356243026edb95a65bf17ba52e1776192a1a1998f783973173789c3c2936`  
		Last Modified: Thu, 27 Feb 2025 18:20:47 GMT  
		Size: 264.8 MB (264848359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b33da5e826269f7c9b668e1d0e4d753be5a3ad84f8e4a1abd3f09ae6d3ea3b`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.4`

```console
$ docker pull julia@sha256:796b31e45388557413cc9fbc1247c35ed686dcf7cf7ae2702d956822a21c80c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

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

## `julia:1.11.4-bookworm`

```console
$ docker pull julia@sha256:796b31e45388557413cc9fbc1247c35ed686dcf7cf7ae2702d956822a21c80c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
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
$ docker pull julia@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `julia:1.11.4-windowsservercore-1809`

```console
$ docker pull julia@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `julia:1.11.4-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `julia:1.11.4-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `julia:bookworm`

```console
$ docker pull julia@sha256:dfd895b0efb2e24cfb1f7b905368c1201724da48f6dd5e4810728e364cbff387
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
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
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
$ docker pull julia@sha256:01cc0092fb6793b4ad0a6f9f0d03660089e16abed71c6c69b44570c34d71d06f
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
$ docker pull julia@sha256:0a0f39b95d921f4bb97ad99b16a068026b74f8b0704dfdc31638c621575dd9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266856640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29713a1cdf39020a68decfa56884755ce9fbd74a1bb96550e50b6712fc4b2f83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 22 Jan 2025 06:59:19 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 22 Jan 2025 06:59:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 22 Jan 2025 06:59:19 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 06:59:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.3-linux-x86_64.tar.gz'; 			sha256='7d48da416c8cb45582a1285d60127ee31ef7092ded3ec594a9f2cf58431c07fd'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.3-linux-aarch64.tar.gz'; 			sha256='0c1f2f60c3ecc37ae0c559db325dc64858fb11d6729b25d63f23e5285f7906ef'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.3-linux-i686.tar.gz'; 			sha256='9001cbd4a077fad3030929eb18b4ff256067fe5bc8782f7e2d7b75e9dde56f27'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.3-linux-ppc64le.tar.gz'; 			sha256='6674366cb75f22342e6e79312737a66f43fbdc30e368fc9f1d6a73565bcd1c9d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Jan 2025 06:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jan 2025 06:59:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4708a00a4a1dabb4e3b37f11e0545198ed018ae176a8ce7b17a73cf6994007`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 6.2 MB (6249369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d8a17f15ca24488cded092d5ac20741139abbc7cf866d496ffe8de1cdfa07`  
		Last Modified: Tue, 25 Feb 2025 02:34:38 GMT  
		Size: 228.6 MB (228554589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe53ea57380de81858ce102ec1922eb8cdce1e7ac60bf7e3b205ae4ab9ca68`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:58dbb57ad02e9f1defa8e35fda67ded0ff908846cbc140bef532300aadca8279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2887f533a2680b99f0e646e589677e9e140af88ac348517bf955d7e395b47e`

```dockerfile
```

-	Layers:
	-	`sha256:ddee7d5a4ba2710ff22b1d6d50381d629c099f729c7c74655243de9551c37480`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 2.4 MB (2449888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64578371dd2da32c6807e98cbee6422b183bc7456606216f94efeac54e6172b0`  
		Last Modified: Tue, 25 Feb 2025 02:34:32 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:580414c60d19e62298e89e9eb1127dd6f473a2774657828e7942efc4e9a65c28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081442433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a26e3c596df439e60599ef95126e620bcadd8a07e9d7c3d2a15a554a70debc`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 27 Feb 2025 18:19:00 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 27 Feb 2025 18:20:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:20:04 GMT
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
	-	`sha256:e9fdc02c27ab8440ae46b627a657673f4cd98a7796059a2bb4e9106c9aeb21d6`  
		Last Modified: Thu, 27 Feb 2025 18:20:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b680a25229271e6fd7cb1ebdc74da5ff6f4e4ada764930780edbff55bd04a3`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64b9b53f5526a424ae03d0a93bbdde5ab05c26d0ed76acb0fcaf19bda3c6d4f`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72753769a2de3c67535cc4e5521833c6a0de6fe45e4202963e90fa28559281fe`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed62356243026edb95a65bf17ba52e1776192a1a1998f783973173789c3c2936`  
		Last Modified: Thu, 27 Feb 2025 18:20:47 GMT  
		Size: 264.8 MB (264848359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b33da5e826269f7c9b668e1d0e4d753be5a3ad84f8e4a1abd3f09ae6d3ea3b`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
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
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
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
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:1d1122bb36103f21a4c1cd63ae718bb9cc28c23b97000c043408b1a79a27add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `julia:windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:580414c60d19e62298e89e9eb1127dd6f473a2774657828e7942efc4e9a65c28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081442433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a26e3c596df439e60599ef95126e620bcadd8a07e9d7c3d2a15a554a70debc`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 27 Feb 2025 18:19:00 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 27 Feb 2025 18:20:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:20:04 GMT
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
	-	`sha256:e9fdc02c27ab8440ae46b627a657673f4cd98a7796059a2bb4e9106c9aeb21d6`  
		Last Modified: Thu, 27 Feb 2025 18:20:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b680a25229271e6fd7cb1ebdc74da5ff6f4e4ada764930780edbff55bd04a3`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64b9b53f5526a424ae03d0a93bbdde5ab05c26d0ed76acb0fcaf19bda3c6d4f`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72753769a2de3c67535cc4e5521833c6a0de6fe45e4202963e90fa28559281fe`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed62356243026edb95a65bf17ba52e1776192a1a1998f783973173789c3c2936`  
		Last Modified: Thu, 27 Feb 2025 18:20:47 GMT  
		Size: 264.8 MB (264848359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b33da5e826269f7c9b668e1d0e4d753be5a3ad84f8e4a1abd3f09ae6d3ea3b`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
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
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
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
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:2e7bd23cb87b2b1bd0cdcc013c54c0b618044b9750fe0527be5e012363a73f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull julia@sha256:e1d43fdeda35f9e09495043a6e377bf61e3a935287ad55c8b3cce6ce237ce707
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2401667309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b388a8fb4756a21a54f3d6ca62ac23e6bc5684f195136c1ad38c1d7f5aefb51`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:33:24 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:33:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:33:26 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:35:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:35:41 GMT
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
	-	`sha256:7419edf935a3a79a441c0927ec55432c106cc8c35171ca60586a27d7c08d2b6b`  
		Last Modified: Thu, 13 Feb 2025 00:35:46 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8082d0ca4115df0117c6c2660bb2e6003a16de378a2f626510f106bafd3d8bb1`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e7e16fd5eaa18ba502ba36439fb1f73650617c0dafc0b7ab41428b231b8e2`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a155c757a0f9b393fa9e069717af39d03985b731da0cfa12a0fc5a838c57b5b`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c427fba1baedd3e98219edffd1b235b2e51dc46f5506dff7829db28f1cf257`  
		Last Modified: Thu, 13 Feb 2025 00:36:19 GMT  
		Size: 264.8 MB (264752023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5c9da52a79cdb082047ab1ee85210146a9ac4f6518e89114cbbe3e2e0458ce`  
		Last Modified: Thu, 13 Feb 2025 00:35:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:67a9470180bfe119828cda80614b5c765934f592f08dd030ae237136aff79352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull julia@sha256:cee303f5169b77c6c994dda090e25f8151afceac3ed348d3300f1380527eef73
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2528625955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b5b88c5100a18b3a6e2f8936dbf765b0cf1bf73b98f57b8fec7339a1a8ac66`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:37:07 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 13 Feb 2025 00:37:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 13 Feb 2025 00:37:09 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 13 Feb 2025 00:38:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 13 Feb 2025 00:38:22 GMT
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
	-	`sha256:ef8612ff645a4db984c5ec791b857ce3a797a3e1d0cb85ff8f86117d0aa3d82d`  
		Last Modified: Thu, 13 Feb 2025 00:38:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6da9711d51524d8eb4971eef74c1017e76e5c591fb2951a7060795e9aec42d`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d5a3fdd8fc0f730ba2fd68c32ed2fa7b83f060fafd42a753bf9ca30a0278b`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fd987ffaab776255b99aef3a8b5be5249ef46e3447a351858ff34c2bea8eae`  
		Last Modified: Thu, 13 Feb 2025 00:38:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d23fa6d658868ee061bc56e89f0db2e24ba764189859cdbf0cac4e6478aae94`  
		Last Modified: Thu, 13 Feb 2025 00:38:59 GMT  
		Size: 264.8 MB (264761522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723f627e866bac971ed449b249e7a60e2752654de94aad27e35a91f8fcb05f38`  
		Last Modified: Thu, 13 Feb 2025 00:38:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:3d3f457a3b71660bf38adb6ea92286b29f1e342aba711815fa0cf72f8c92a0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull julia@sha256:580414c60d19e62298e89e9eb1127dd6f473a2774657828e7942efc4e9a65c28
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3081442433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a26e3c596df439e60599ef95126e620bcadd8a07e9d7c3d2a15a554a70debc`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_VERSION=1.11.3
# Thu, 27 Feb 2025 18:18:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Thu, 27 Feb 2025 18:19:00 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Thu, 27 Feb 2025 18:20:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:20:04 GMT
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
	-	`sha256:e9fdc02c27ab8440ae46b627a657673f4cd98a7796059a2bb4e9106c9aeb21d6`  
		Last Modified: Thu, 27 Feb 2025 18:20:09 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b680a25229271e6fd7cb1ebdc74da5ff6f4e4ada764930780edbff55bd04a3`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64b9b53f5526a424ae03d0a93bbdde5ab05c26d0ed76acb0fcaf19bda3c6d4f`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72753769a2de3c67535cc4e5521833c6a0de6fe45e4202963e90fa28559281fe`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed62356243026edb95a65bf17ba52e1776192a1a1998f783973173789c3c2936`  
		Last Modified: Thu, 27 Feb 2025 18:20:47 GMT  
		Size: 264.8 MB (264848359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b33da5e826269f7c9b668e1d0e4d753be5a3ad84f8e4a1abd3f09ae6d3ea3b`  
		Last Modified: Thu, 27 Feb 2025 18:20:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
