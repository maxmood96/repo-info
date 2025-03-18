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
$ docker pull julia@sha256:bab8309d212703cdcb3725899e1ce3a89d6705ddc0194a37442c5d74b318180c
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

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:abedded0d1772aaeb02c6bba4109b7fd0745b4880c73eb811b30373d985d48b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302403240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b16b02d491ef44bf1edb4d4b55af7ed0859b2231bdb1cacb7dfb56f2d7d11d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf165c807d409f1e5e47644d10a56e62f760b04977240ccb92cb44373c0b0f69`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 5.7 MB (5713383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b6fe754913bc7659f03d356590438cc4eedd2dd68f4df602467584df07ac2`  
		Last Modified: Mon, 17 Mar 2025 23:13:45 GMT  
		Size: 268.5 MB (268484621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2ec09870a2c14b826ec97c7163f20459b189d4ac71ce5fc48c61be5cbf30db`  
		Last Modified: Mon, 17 Mar 2025 23:13:37 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:90638797f1b5d7e05dc89684f27edd24d0ec9c90049a8b4a7bd0ba55d5f49895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb188174850f12a03f938d4afbdc70ce9d2f1e201caf8312806b2c15c8016aa`

```dockerfile
```

-	Layers:
	-	`sha256:0485ab72220e8c25e8c44fd4643cb6401c32a43d460248901e04551b66c7a690`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.4 MB (2445468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7d10aaca52976692b814b68272ef08141b566e335fb00c2d7a87c20e54059e`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 18.4 KB (18399 bytes)  
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
$ docker pull julia@sha256:9f6cb4ab8de753dbdf08958fadb970ea57420a25940a9c66889d2675e1b30261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252906412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6160838c86bb01311ab4312fadcb5c79febbc02a9db5bec211474b6ae2d89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c313be324d81319409f757b6a9214e6e4505edd1870d857ef9335183bf456`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 5.9 MB (5872272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809e1e548a3d059caccea690a9ccc930a0ba4003bac183b117a14c4ef5eb0be5`  
		Last Modified: Mon, 17 Mar 2025 23:25:50 GMT  
		Size: 217.8 MB (217844242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790e28391a0fe4d76f864c7f5f2ad1d677cd00da4cfc75068849cd664e65683`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:66caada27c36606986912deb412ff68f7f7ec9bddf54775f6a16093eab0cfb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118730f876ef85874545babb36fc06e2768e0d5b721d060f23817c42124b3bc`

```dockerfile
```

-	Layers:
	-	`sha256:76a154e6def364e394399ef31951b53809301692945ecf7401bee9a909343563`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 2.4 MB (2442541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c82965d60d3d4aa1404ef241e92932d6ceef303d9cfac5e6b23310f702ee2b`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 18.3 KB (18345 bytes)  
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

### `julia:1` - windows version 10.0.26100.3476; amd64

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

### `julia:1` - windows version 10.0.20348.3328; amd64

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

### `julia:1` - windows version 10.0.17763.7009; amd64

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

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:5e3d4eba6d196e37b910cdcc059ff98730e33946bfcf0d9d813b3a56060e5fb6
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
$ docker pull julia@sha256:abedded0d1772aaeb02c6bba4109b7fd0745b4880c73eb811b30373d985d48b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302403240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b16b02d491ef44bf1edb4d4b55af7ed0859b2231bdb1cacb7dfb56f2d7d11d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf165c807d409f1e5e47644d10a56e62f760b04977240ccb92cb44373c0b0f69`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 5.7 MB (5713383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b6fe754913bc7659f03d356590438cc4eedd2dd68f4df602467584df07ac2`  
		Last Modified: Mon, 17 Mar 2025 23:13:45 GMT  
		Size: 268.5 MB (268484621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2ec09870a2c14b826ec97c7163f20459b189d4ac71ce5fc48c61be5cbf30db`  
		Last Modified: Mon, 17 Mar 2025 23:13:37 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:90638797f1b5d7e05dc89684f27edd24d0ec9c90049a8b4a7bd0ba55d5f49895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb188174850f12a03f938d4afbdc70ce9d2f1e201caf8312806b2c15c8016aa`

```dockerfile
```

-	Layers:
	-	`sha256:0485ab72220e8c25e8c44fd4643cb6401c32a43d460248901e04551b66c7a690`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.4 MB (2445468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7d10aaca52976692b814b68272ef08141b566e335fb00c2d7a87c20e54059e`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 18.4 KB (18399 bytes)  
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
$ docker pull julia@sha256:9f6cb4ab8de753dbdf08958fadb970ea57420a25940a9c66889d2675e1b30261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252906412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6160838c86bb01311ab4312fadcb5c79febbc02a9db5bec211474b6ae2d89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c313be324d81319409f757b6a9214e6e4505edd1870d857ef9335183bf456`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 5.9 MB (5872272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809e1e548a3d059caccea690a9ccc930a0ba4003bac183b117a14c4ef5eb0be5`  
		Last Modified: Mon, 17 Mar 2025 23:25:50 GMT  
		Size: 217.8 MB (217844242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790e28391a0fe4d76f864c7f5f2ad1d677cd00da4cfc75068849cd664e65683`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:66caada27c36606986912deb412ff68f7f7ec9bddf54775f6a16093eab0cfb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118730f876ef85874545babb36fc06e2768e0d5b721d060f23817c42124b3bc`

```dockerfile
```

-	Layers:
	-	`sha256:76a154e6def364e394399ef31951b53809301692945ecf7401bee9a909343563`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 2.4 MB (2442541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c82965d60d3d4aa1404ef241e92932d6ceef303d9cfac5e6b23310f702ee2b`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 18.3 KB (18345 bytes)  
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
$ docker pull julia@sha256:24cfd68cf777099d9204b778a9ac206fee9b3d4f8500b049aa928683671f1bb3
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
$ docker pull julia@sha256:e19adf478c932ddceb0cd543f385f1fbdf2e7112843ee8e3b0ceae918862f56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300961318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de69c31d798eaabef70e7c3edcfb0e64e992ef1d6b246a4ca76a53a04c50754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeafcf0ad42d0b7ba886b69799967535eaa98a21f8fbe73943453496d291b8ed`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.2 MB (2222677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39d5991f07d5c2acfdcb0ba4c1d31d3d14e71397cd848796aab3da3ab16430b`  
		Last Modified: Mon, 17 Mar 2025 23:13:44 GMT  
		Size: 268.5 MB (268484435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300bb409d0fb700f649d71205c2ca618d30e3779cfd378b109aa36417b48a88b`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:568bbe514f6c6d8dcf71ac23382e97947a5d89db7568870c18c84df734717373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7397c81b0cbe0408efb3157682c2b76db2f14059e420037d780d658526b746e`

```dockerfile
```

-	Layers:
	-	`sha256:542940db3f80626a40eb95fb688aeea3a5578fbd74ffe1d9dd79b9a8e1177c1e`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8e498258530cc6b44d6affd29bf756952c36580d0e9fe0c55c335ae153d695`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 17.2 KB (17230 bytes)  
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
$ docker pull julia@sha256:33620ae3d96ab9adaf7dab3ccf2264c0e80196363fd2b850af8b3a5c770b8f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251354291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c38d8ab7fbe3538882b71342b7da6729f5cae4146da2dffe153379cfe2c4d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecef606b0a992420b25835cdfaeff30b8f8795129a713d037053dda8ca79abf`  
		Last Modified: Mon, 17 Mar 2025 23:25:46 GMT  
		Size: 2.3 MB (2328062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebe87c0ddbcc8ab060a7709e68b17c43db9bf75d54ac67018c6503307a7bd5f`  
		Last Modified: Mon, 17 Mar 2025 23:25:51 GMT  
		Size: 217.8 MB (217845523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07087d0b8d9a969e61a9ec020d1c8afbb9fc0e52936e359dc2007c6063c0d7a`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:185707a3a086745c07344c4e3eea6ac898c6e92cb85bd8333d7d68fe75263122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b637ca421f08d79789664405fb6785198aa5af754f6921378a49380245cc7ae1`

```dockerfile
```

-	Layers:
	-	`sha256:418ba4380bab52bce1f331afb478eb78c44c136d74ae008472a52f32c9e9fe76`  
		Last Modified: Mon, 17 Mar 2025 23:25:46 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e547ae26d53300a9467d2c3227c5103d3827a9f84decb55f76ba258aa5d7f4cf`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:a58330d3909779ea6fda30203e9a87609ae28d7f332fe903b34f711bab76541a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `julia:1-windowsservercore` - windows version 10.0.26100.3476; amd64

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

### `julia:1-windowsservercore` - windows version 10.0.20348.3328; amd64

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

### `julia:1-windowsservercore` - windows version 10.0.17763.7009; amd64

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

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:690b3bb2cd57b68ea519b4c0e834a243b9d4bd415b7de871605ca4866b693169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

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

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:4426e2a8c83587fbc2b48d4eb2521fd9d412bc9cb7f6465a5c221e1712b6f1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

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

## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:096ec1ac6bd7714f5cb4555a0f63af46ee152de56046f33fa46583ca3c4b278e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

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

## `julia:1.10`

```console
$ docker pull julia@sha256:169320368b78e396fb2362f5c5a3a985fd5f12544194ba7325a3b8f68541ed7c
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

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:c86e76e3b6c06ead6c5008c90cb254948bbd4afa2c4a41119a4522123f8ac97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210411229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910cb8f602752beec1b63304aebb55636704fdefd5f4d958432088c0cd652fe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 10 Mar 2025 23:59:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7aab53e6a1511a0931d6a0f5147dbc9d24f9a979ca917cba864dfe48ca1ca0`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
		Size: 5.7 MB (5713447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb3654ea8f7d5e3fbf042235459d4356759f3161c81153ff24d89c42e738f4`  
		Last Modified: Mon, 17 Mar 2025 23:13:17 GMT  
		Size: 176.5 MB (176492552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536063d66300c08e535f283bde7a6d5dbeec0e61d4037bef1f812c74de3fe2a`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:41ca49af4d2789e2a9a2e44ad74976f418446233b5543ba46b547bcd38d07859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1c38127adbf8b544fab9408b37287285b83afacc3db4c55206f392017a5d7e`

```dockerfile
```

-	Layers:
	-	`sha256:cea5f221a6b08943dfd9bbe6def02a8cea0aa27cbeb3de8656c3a1ecb9074b5b`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
		Size: 2.4 MB (2445513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2a18450a2289f1eaf5a9ed3ce4d338deaed7318bb9a6c406bc79f083bc8d092`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
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
$ docker pull julia@sha256:88bd0a7a0d7bfbd14da32bffd8b15a29541f1794cb8954dbdd5748f8ded9e9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192818563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a7adcea18707c2ec078871c14b189d4ffbced0a2642ee9d9d532caf3f115b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 10 Mar 2025 23:59:15 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c73ce6cc283878cc1c0f4f2df059bfa168a2f3155cf3cdbaf37a41837076488`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
		Size: 5.9 MB (5872293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18741095039a71cdd865499ef05ae374ae63bccee2e78ca4835a088dee15dc33`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 157.8 MB (157756370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d134d4cb26e4df38cc330e351a79ac3e69934f9440a097955f19c28525e7eb`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:202ca39d2bea222bce0dfabd441f6e4b50f411b4ecd4e4528a355fad43aedc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908156ba460d7bf322eb70d6eb00b3d9ba44988f3bc6de528746bc0f75a7efc7`

```dockerfile
```

-	Layers:
	-	`sha256:ad0c4f2d8fb21820a0b278ffc0a0e2fa6a68de89c58a282053a6af77874a2bef`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
		Size: 2.4 MB (2442606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ef0cd94ee2bb41c33aadc6639346cfb1d145c95fa741ffc1641af893d953b3`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
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

### `julia:1.10` - windows version 10.0.26100.3476; amd64

```console
$ docker pull julia@sha256:6d4322e0a6962f14b38b77152b468a80195909b605d18647e1dbafc853b16bfb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3097391045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810d87f0ce83839f4773b100f8201db6aa3cf3697dc1cf60a7d84ffb73b3eabf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:27 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:47:28 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:47:29 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:48:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:48:14 GMT
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
	-	`sha256:06646829988e8751e866ce158547a93bf81c62c298e78e05965cb36ed5abe822`  
		Last Modified: Wed, 12 Mar 2025 18:48:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea9e5b43eb491f8227d43913edb19774bf9b3e2ceb9e721f6cf2fb7aef01bff`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa504cb06c4bf82666f726321b5b25f6a806936d4a562f1d510289eb0d49a136`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0eab3c553aa5966e5f06766a08d74abbe154aeb3e6a302f4b770010e34ffbd`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b72da77d1a2d616a388a688ba110a2ad50f83a56d6efce54a1e835374427c48`  
		Last Modified: Wed, 12 Mar 2025 18:48:46 GMT  
		Size: 188.7 MB (188736818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd649bbcba8e52396d192f5c3d1f24263e487fdcc82e2eb6c382c2a659d9ad`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.20348.3328; amd64

```console
$ docker pull julia@sha256:85c852b88149651a8e50c2641cdd9abdebe68dc398153324dc358891e88fb73c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2458640046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2059f62896dc80b0545285128282d1899c08182b87facd764e087ab2aa5779a3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:52:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:31 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:52:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:52:33 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:53:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:53:28 GMT
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
	-	`sha256:f7fcbbdc81fb789b7a508252cc8ceeccaefd394c89761e59ad500398276ef5df`  
		Last Modified: Wed, 12 Mar 2025 18:53:32 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3d43167617a095ca5f3123a244c87b642b0dbb46452b99fc560550abaa877f`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aede456ed8c6cd01914b66b210c124e1a6bf42f20115907ed65d224801a36f0`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f17adaa48f685bd225142f5e3f239584302ac3993e0dd9f9c84db0ee4ad2c6`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ddba1729af0274e0b2dc01bb9c32fd142ff08501c06573830b8cb5e18d2d2d`  
		Last Modified: Wed, 12 Mar 2025 18:53:55 GMT  
		Size: 188.7 MB (188692427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c2327b82e3dddeb6f0c6d79ff71af92ab90e43a4d96976d1124c393f58e567`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.7009; amd64

```console
$ docker pull julia@sha256:931836b6120961d4999cfdb468ab9fbef9d70c48791bdf10a6ba97bcc3addf57
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2340338714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24662fb63bbc9dd249033f01d25e885800ca56e27b6b1a88169db23d775aa679`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:55:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:55:48 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:55:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:55:49 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:57:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:57:34 GMT
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
	-	`sha256:4a22f2387ee5ad25ee19b638331e2d9e7ab6ec51a81ff35363a85b64660983b2`  
		Last Modified: Wed, 12 Mar 2025 18:57:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1177da773bdddc0e095e41fb53b6422c097150600d54ef635520c0991ac4e2`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d7be3e4f805ad689673ea4a9b10a59facbc02e95c087c33fb3f57d444e8bf`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f834bb5a94f14a47739aecf58e1c343f92bc9ed8203a8548e09590906268a10b`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc1663b632e24e8de6af0b375cdd61bbe00aff2e9224ad938dd77e9879051bf`  
		Last Modified: Wed, 12 Mar 2025 18:58:04 GMT  
		Size: 188.7 MB (188697575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f28f9e5186ef56f9683968f943528ddf2c3a7f9b3288bf5f492a7852f4a017`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1302 bytes)  
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
$ docker pull julia@sha256:538d5f5111223261449ee09fdacca92b7aa6ce9ca2582fa86f722e655331e416
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
$ docker pull julia@sha256:c86e76e3b6c06ead6c5008c90cb254948bbd4afa2c4a41119a4522123f8ac97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210411229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910cb8f602752beec1b63304aebb55636704fdefd5f4d958432088c0cd652fe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 10 Mar 2025 23:59:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7aab53e6a1511a0931d6a0f5147dbc9d24f9a979ca917cba864dfe48ca1ca0`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
		Size: 5.7 MB (5713447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb3654ea8f7d5e3fbf042235459d4356759f3161c81153ff24d89c42e738f4`  
		Last Modified: Mon, 17 Mar 2025 23:13:17 GMT  
		Size: 176.5 MB (176492552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536063d66300c08e535f283bde7a6d5dbeec0e61d4037bef1f812c74de3fe2a`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:41ca49af4d2789e2a9a2e44ad74976f418446233b5543ba46b547bcd38d07859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1c38127adbf8b544fab9408b37287285b83afacc3db4c55206f392017a5d7e`

```dockerfile
```

-	Layers:
	-	`sha256:cea5f221a6b08943dfd9bbe6def02a8cea0aa27cbeb3de8656c3a1ecb9074b5b`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
		Size: 2.4 MB (2445513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2a18450a2289f1eaf5a9ed3ce4d338deaed7318bb9a6c406bc79f083bc8d092`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
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
$ docker pull julia@sha256:88bd0a7a0d7bfbd14da32bffd8b15a29541f1794cb8954dbdd5748f8ded9e9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192818563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a7adcea18707c2ec078871c14b189d4ffbced0a2642ee9d9d532caf3f115b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 10 Mar 2025 23:59:15 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c73ce6cc283878cc1c0f4f2df059bfa168a2f3155cf3cdbaf37a41837076488`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
		Size: 5.9 MB (5872293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18741095039a71cdd865499ef05ae374ae63bccee2e78ca4835a088dee15dc33`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 157.8 MB (157756370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d134d4cb26e4df38cc330e351a79ac3e69934f9440a097955f19c28525e7eb`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:202ca39d2bea222bce0dfabd441f6e4b50f411b4ecd4e4528a355fad43aedc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908156ba460d7bf322eb70d6eb00b3d9ba44988f3bc6de528746bc0f75a7efc7`

```dockerfile
```

-	Layers:
	-	`sha256:ad0c4f2d8fb21820a0b278ffc0a0e2fa6a68de89c58a282053a6af77874a2bef`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
		Size: 2.4 MB (2442606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ef0cd94ee2bb41c33aadc6639346cfb1d145c95fa741ffc1641af893d953b3`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
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
$ docker pull julia@sha256:8bbc1b96adda6ada439f54853cbc3fe2836171e2690efc368031be14172de8e1
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
$ docker pull julia@sha256:88d907ae023c19fd075d27c1e8104a778613f1b14f68aa8c32470e7276a7afc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (208970683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7889065a5f19a3bae6da547ab97607cdb8105434d44de30b6689b1e2ea3d76f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 10 Mar 2025 23:59:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399cd1c6ef62c72c87eab5c68d580c0dde40c5022b3497721996ef96af22522d`  
		Last Modified: Mon, 17 Mar 2025 23:13:24 GMT  
		Size: 2.2 MB (2222647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4e344ad943cf3175024a0b796712a985e108f911896e3624d2a34104d68ed3`  
		Last Modified: Mon, 17 Mar 2025 23:13:28 GMT  
		Size: 176.5 MB (176493835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f83f5c5f5abab7ee47bbeaa9b07bee8af96e033bfaf5456c0c519f1c41537b6`  
		Last Modified: Mon, 17 Mar 2025 23:13:23 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:d8544b20aa86e2a26805ae5ad79da53e27ebd5ee5dc5ed89b1671bd4a6d8f7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6180839743035d582b2360a399abeab66580ede696aa1f0ac5540423280630f`

```dockerfile
```

-	Layers:
	-	`sha256:d71cd102171ced66ec44789dfe2c1eb9d2fb6129265d8e463cd76b24d7cc2b7b`  
		Last Modified: Mon, 17 Mar 2025 23:13:24 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea5c3e7e7393cdb0427b575f13f80db3fbca86dabecf4d15375fea3b13917fe`  
		Last Modified: Mon, 17 Mar 2025 23:13:23 GMT  
		Size: 16.6 KB (16624 bytes)  
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
$ docker pull julia@sha256:f4e754a7e05bbd3e06991c659e1890275bd9ab1cf08606a831d4508266b88e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191265135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f886c112b09dda985449d9352f0d8d0e23ed0ee664d7292cd30b66f9a99be37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 10 Mar 2025 23:59:15 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7936b0bfcb6212ad77af40e650966f94f678976c0322069ac4c10605546b3d`  
		Last Modified: Mon, 17 Mar 2025 23:25:34 GMT  
		Size: 2.3 MB (2328061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33735c78cbea761a7e61f5ab4efb142f413debdc930fdc75bf62fa8fab58192e`  
		Last Modified: Mon, 17 Mar 2025 23:25:38 GMT  
		Size: 157.8 MB (157756369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4ee1d611e9fd550c0d6d5da5a726885f8315625e1884a12b05b897ac224bb2`  
		Last Modified: Mon, 17 Mar 2025 23:25:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:844c7fbc3986752e99e75184c851aae7cca0d39f9e60100b0c7645c3e67adc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c546f98e5adadf6cc31dd6d737ea835c4486ebfeca905ab03518fa672573d43`

```dockerfile
```

-	Layers:
	-	`sha256:b65f9d183eb04ce257609b5f760a6fe2c570f1efb55c2038b87b0db8fb00d57f`  
		Last Modified: Mon, 17 Mar 2025 23:25:35 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6ae600d918ed9e000a561c579e37a336e8f9b283ebb4a2388022f9d7abd998`  
		Last Modified: Mon, 17 Mar 2025 23:25:34 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:39ddd683c3d3906445f709e17366ccb98408fa1d78ab65041fe6d67aed264b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull julia@sha256:6d4322e0a6962f14b38b77152b468a80195909b605d18647e1dbafc853b16bfb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3097391045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810d87f0ce83839f4773b100f8201db6aa3cf3697dc1cf60a7d84ffb73b3eabf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:27 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:47:28 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:47:29 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:48:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:48:14 GMT
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
	-	`sha256:06646829988e8751e866ce158547a93bf81c62c298e78e05965cb36ed5abe822`  
		Last Modified: Wed, 12 Mar 2025 18:48:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea9e5b43eb491f8227d43913edb19774bf9b3e2ceb9e721f6cf2fb7aef01bff`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa504cb06c4bf82666f726321b5b25f6a806936d4a562f1d510289eb0d49a136`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0eab3c553aa5966e5f06766a08d74abbe154aeb3e6a302f4b770010e34ffbd`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b72da77d1a2d616a388a688ba110a2ad50f83a56d6efce54a1e835374427c48`  
		Last Modified: Wed, 12 Mar 2025 18:48:46 GMT  
		Size: 188.7 MB (188736818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd649bbcba8e52396d192f5c3d1f24263e487fdcc82e2eb6c382c2a659d9ad`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull julia@sha256:85c852b88149651a8e50c2641cdd9abdebe68dc398153324dc358891e88fb73c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2458640046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2059f62896dc80b0545285128282d1899c08182b87facd764e087ab2aa5779a3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:52:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:31 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:52:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:52:33 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:53:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:53:28 GMT
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
	-	`sha256:f7fcbbdc81fb789b7a508252cc8ceeccaefd394c89761e59ad500398276ef5df`  
		Last Modified: Wed, 12 Mar 2025 18:53:32 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3d43167617a095ca5f3123a244c87b642b0dbb46452b99fc560550abaa877f`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aede456ed8c6cd01914b66b210c124e1a6bf42f20115907ed65d224801a36f0`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f17adaa48f685bd225142f5e3f239584302ac3993e0dd9f9c84db0ee4ad2c6`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ddba1729af0274e0b2dc01bb9c32fd142ff08501c06573830b8cb5e18d2d2d`  
		Last Modified: Wed, 12 Mar 2025 18:53:55 GMT  
		Size: 188.7 MB (188692427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c2327b82e3dddeb6f0c6d79ff71af92ab90e43a4d96976d1124c393f58e567`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull julia@sha256:931836b6120961d4999cfdb468ab9fbef9d70c48791bdf10a6ba97bcc3addf57
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2340338714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24662fb63bbc9dd249033f01d25e885800ca56e27b6b1a88169db23d775aa679`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:55:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:55:48 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:55:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:55:49 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:57:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:57:34 GMT
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
	-	`sha256:4a22f2387ee5ad25ee19b638331e2d9e7ab6ec51a81ff35363a85b64660983b2`  
		Last Modified: Wed, 12 Mar 2025 18:57:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1177da773bdddc0e095e41fb53b6422c097150600d54ef635520c0991ac4e2`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d7be3e4f805ad689673ea4a9b10a59facbc02e95c087c33fb3f57d444e8bf`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f834bb5a94f14a47739aecf58e1c343f92bc9ed8203a8548e09590906268a10b`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc1663b632e24e8de6af0b375cdd61bbe00aff2e9224ad938dd77e9879051bf`  
		Last Modified: Wed, 12 Mar 2025 18:58:04 GMT  
		Size: 188.7 MB (188697575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f28f9e5186ef56f9683968f943528ddf2c3a7f9b3288bf5f492a7852f4a017`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:d2fc54b1ffdf1a785dd4c5bf705933925c291353b3e249b5f12442d897743703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull julia@sha256:931836b6120961d4999cfdb468ab9fbef9d70c48791bdf10a6ba97bcc3addf57
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2340338714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24662fb63bbc9dd249033f01d25e885800ca56e27b6b1a88169db23d775aa679`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:55:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:55:48 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:55:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:55:49 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:57:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:57:34 GMT
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
	-	`sha256:4a22f2387ee5ad25ee19b638331e2d9e7ab6ec51a81ff35363a85b64660983b2`  
		Last Modified: Wed, 12 Mar 2025 18:57:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1177da773bdddc0e095e41fb53b6422c097150600d54ef635520c0991ac4e2`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d7be3e4f805ad689673ea4a9b10a59facbc02e95c087c33fb3f57d444e8bf`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f834bb5a94f14a47739aecf58e1c343f92bc9ed8203a8548e09590906268a10b`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc1663b632e24e8de6af0b375cdd61bbe00aff2e9224ad938dd77e9879051bf`  
		Last Modified: Wed, 12 Mar 2025 18:58:04 GMT  
		Size: 188.7 MB (188697575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f28f9e5186ef56f9683968f943528ddf2c3a7f9b3288bf5f492a7852f4a017`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:df52872dbf50013fbd689792b396c800738bc4edd0a9f33be69cbbfbfa1be889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull julia@sha256:85c852b88149651a8e50c2641cdd9abdebe68dc398153324dc358891e88fb73c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2458640046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2059f62896dc80b0545285128282d1899c08182b87facd764e087ab2aa5779a3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:52:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:31 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:52:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:52:33 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:53:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:53:28 GMT
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
	-	`sha256:f7fcbbdc81fb789b7a508252cc8ceeccaefd394c89761e59ad500398276ef5df`  
		Last Modified: Wed, 12 Mar 2025 18:53:32 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3d43167617a095ca5f3123a244c87b642b0dbb46452b99fc560550abaa877f`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aede456ed8c6cd01914b66b210c124e1a6bf42f20115907ed65d224801a36f0`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f17adaa48f685bd225142f5e3f239584302ac3993e0dd9f9c84db0ee4ad2c6`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ddba1729af0274e0b2dc01bb9c32fd142ff08501c06573830b8cb5e18d2d2d`  
		Last Modified: Wed, 12 Mar 2025 18:53:55 GMT  
		Size: 188.7 MB (188692427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c2327b82e3dddeb6f0c6d79ff71af92ab90e43a4d96976d1124c393f58e567`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:28ad16aef46622e6b1ad508ab189593de23e2ac079c9dab4611557a62b3a1b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `julia:1.10-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull julia@sha256:6d4322e0a6962f14b38b77152b468a80195909b605d18647e1dbafc853b16bfb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3097391045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810d87f0ce83839f4773b100f8201db6aa3cf3697dc1cf60a7d84ffb73b3eabf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:27 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:47:28 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:47:29 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:48:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:48:14 GMT
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
	-	`sha256:06646829988e8751e866ce158547a93bf81c62c298e78e05965cb36ed5abe822`  
		Last Modified: Wed, 12 Mar 2025 18:48:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea9e5b43eb491f8227d43913edb19774bf9b3e2ceb9e721f6cf2fb7aef01bff`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa504cb06c4bf82666f726321b5b25f6a806936d4a562f1d510289eb0d49a136`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0eab3c553aa5966e5f06766a08d74abbe154aeb3e6a302f4b770010e34ffbd`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b72da77d1a2d616a388a688ba110a2ad50f83a56d6efce54a1e835374427c48`  
		Last Modified: Wed, 12 Mar 2025 18:48:46 GMT  
		Size: 188.7 MB (188736818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd649bbcba8e52396d192f5c3d1f24263e487fdcc82e2eb6c382c2a659d9ad`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.9`

```console
$ docker pull julia@sha256:169320368b78e396fb2362f5c5a3a985fd5f12544194ba7325a3b8f68541ed7c
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

### `julia:1.10.9` - linux; amd64

```console
$ docker pull julia@sha256:c86e76e3b6c06ead6c5008c90cb254948bbd4afa2c4a41119a4522123f8ac97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210411229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910cb8f602752beec1b63304aebb55636704fdefd5f4d958432088c0cd652fe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 10 Mar 2025 23:59:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7aab53e6a1511a0931d6a0f5147dbc9d24f9a979ca917cba864dfe48ca1ca0`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
		Size: 5.7 MB (5713447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb3654ea8f7d5e3fbf042235459d4356759f3161c81153ff24d89c42e738f4`  
		Last Modified: Mon, 17 Mar 2025 23:13:17 GMT  
		Size: 176.5 MB (176492552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536063d66300c08e535f283bde7a6d5dbeec0e61d4037bef1f812c74de3fe2a`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9` - unknown; unknown

```console
$ docker pull julia@sha256:41ca49af4d2789e2a9a2e44ad74976f418446233b5543ba46b547bcd38d07859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1c38127adbf8b544fab9408b37287285b83afacc3db4c55206f392017a5d7e`

```dockerfile
```

-	Layers:
	-	`sha256:cea5f221a6b08943dfd9bbe6def02a8cea0aa27cbeb3de8656c3a1ecb9074b5b`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
		Size: 2.4 MB (2445513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2a18450a2289f1eaf5a9ed3ce4d338deaed7318bb9a6c406bc79f083bc8d092`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
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
$ docker pull julia@sha256:88bd0a7a0d7bfbd14da32bffd8b15a29541f1794cb8954dbdd5748f8ded9e9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192818563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a7adcea18707c2ec078871c14b189d4ffbced0a2642ee9d9d532caf3f115b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 10 Mar 2025 23:59:15 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c73ce6cc283878cc1c0f4f2df059bfa168a2f3155cf3cdbaf37a41837076488`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
		Size: 5.9 MB (5872293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18741095039a71cdd865499ef05ae374ae63bccee2e78ca4835a088dee15dc33`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 157.8 MB (157756370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d134d4cb26e4df38cc330e351a79ac3e69934f9440a097955f19c28525e7eb`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9` - unknown; unknown

```console
$ docker pull julia@sha256:202ca39d2bea222bce0dfabd441f6e4b50f411b4ecd4e4528a355fad43aedc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908156ba460d7bf322eb70d6eb00b3d9ba44988f3bc6de528746bc0f75a7efc7`

```dockerfile
```

-	Layers:
	-	`sha256:ad0c4f2d8fb21820a0b278ffc0a0e2fa6a68de89c58a282053a6af77874a2bef`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
		Size: 2.4 MB (2442606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ef0cd94ee2bb41c33aadc6639346cfb1d145c95fa741ffc1641af893d953b3`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
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

### `julia:1.10.9` - windows version 10.0.26100.3476; amd64

```console
$ docker pull julia@sha256:6d4322e0a6962f14b38b77152b468a80195909b605d18647e1dbafc853b16bfb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3097391045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810d87f0ce83839f4773b100f8201db6aa3cf3697dc1cf60a7d84ffb73b3eabf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:27 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:47:28 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:47:29 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:48:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:48:14 GMT
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
	-	`sha256:06646829988e8751e866ce158547a93bf81c62c298e78e05965cb36ed5abe822`  
		Last Modified: Wed, 12 Mar 2025 18:48:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea9e5b43eb491f8227d43913edb19774bf9b3e2ceb9e721f6cf2fb7aef01bff`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa504cb06c4bf82666f726321b5b25f6a806936d4a562f1d510289eb0d49a136`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0eab3c553aa5966e5f06766a08d74abbe154aeb3e6a302f4b770010e34ffbd`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b72da77d1a2d616a388a688ba110a2ad50f83a56d6efce54a1e835374427c48`  
		Last Modified: Wed, 12 Mar 2025 18:48:46 GMT  
		Size: 188.7 MB (188736818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd649bbcba8e52396d192f5c3d1f24263e487fdcc82e2eb6c382c2a659d9ad`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.9` - windows version 10.0.20348.3328; amd64

```console
$ docker pull julia@sha256:85c852b88149651a8e50c2641cdd9abdebe68dc398153324dc358891e88fb73c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2458640046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2059f62896dc80b0545285128282d1899c08182b87facd764e087ab2aa5779a3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:52:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:31 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:52:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:52:33 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:53:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:53:28 GMT
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
	-	`sha256:f7fcbbdc81fb789b7a508252cc8ceeccaefd394c89761e59ad500398276ef5df`  
		Last Modified: Wed, 12 Mar 2025 18:53:32 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3d43167617a095ca5f3123a244c87b642b0dbb46452b99fc560550abaa877f`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aede456ed8c6cd01914b66b210c124e1a6bf42f20115907ed65d224801a36f0`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f17adaa48f685bd225142f5e3f239584302ac3993e0dd9f9c84db0ee4ad2c6`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ddba1729af0274e0b2dc01bb9c32fd142ff08501c06573830b8cb5e18d2d2d`  
		Last Modified: Wed, 12 Mar 2025 18:53:55 GMT  
		Size: 188.7 MB (188692427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c2327b82e3dddeb6f0c6d79ff71af92ab90e43a4d96976d1124c393f58e567`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.9` - windows version 10.0.17763.7009; amd64

```console
$ docker pull julia@sha256:931836b6120961d4999cfdb468ab9fbef9d70c48791bdf10a6ba97bcc3addf57
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2340338714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24662fb63bbc9dd249033f01d25e885800ca56e27b6b1a88169db23d775aa679`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:55:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:55:48 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:55:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:55:49 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:57:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:57:34 GMT
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
	-	`sha256:4a22f2387ee5ad25ee19b638331e2d9e7ab6ec51a81ff35363a85b64660983b2`  
		Last Modified: Wed, 12 Mar 2025 18:57:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1177da773bdddc0e095e41fb53b6422c097150600d54ef635520c0991ac4e2`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d7be3e4f805ad689673ea4a9b10a59facbc02e95c087c33fb3f57d444e8bf`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f834bb5a94f14a47739aecf58e1c343f92bc9ed8203a8548e09590906268a10b`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc1663b632e24e8de6af0b375cdd61bbe00aff2e9224ad938dd77e9879051bf`  
		Last Modified: Wed, 12 Mar 2025 18:58:04 GMT  
		Size: 188.7 MB (188697575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f28f9e5186ef56f9683968f943528ddf2c3a7f9b3288bf5f492a7852f4a017`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1302 bytes)  
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
$ docker pull julia@sha256:538d5f5111223261449ee09fdacca92b7aa6ce9ca2582fa86f722e655331e416
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
$ docker pull julia@sha256:c86e76e3b6c06ead6c5008c90cb254948bbd4afa2c4a41119a4522123f8ac97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.4 MB (210411229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910cb8f602752beec1b63304aebb55636704fdefd5f4d958432088c0cd652fe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 10 Mar 2025 23:59:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7aab53e6a1511a0931d6a0f5147dbc9d24f9a979ca917cba864dfe48ca1ca0`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
		Size: 5.7 MB (5713447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cb3654ea8f7d5e3fbf042235459d4356759f3161c81153ff24d89c42e738f4`  
		Last Modified: Mon, 17 Mar 2025 23:13:17 GMT  
		Size: 176.5 MB (176492552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8536063d66300c08e535f283bde7a6d5dbeec0e61d4037bef1f812c74de3fe2a`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:41ca49af4d2789e2a9a2e44ad74976f418446233b5543ba46b547bcd38d07859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1c38127adbf8b544fab9408b37287285b83afacc3db4c55206f392017a5d7e`

```dockerfile
```

-	Layers:
	-	`sha256:cea5f221a6b08943dfd9bbe6def02a8cea0aa27cbeb3de8656c3a1ecb9074b5b`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
		Size: 2.4 MB (2445513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2a18450a2289f1eaf5a9ed3ce4d338deaed7318bb9a6c406bc79f083bc8d092`  
		Last Modified: Mon, 17 Mar 2025 23:13:14 GMT  
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
$ docker pull julia@sha256:88bd0a7a0d7bfbd14da32bffd8b15a29541f1794cb8954dbdd5748f8ded9e9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192818563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a7adcea18707c2ec078871c14b189d4ffbced0a2642ee9d9d532caf3f115b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 10 Mar 2025 23:59:15 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c73ce6cc283878cc1c0f4f2df059bfa168a2f3155cf3cdbaf37a41837076488`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
		Size: 5.9 MB (5872293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18741095039a71cdd865499ef05ae374ae63bccee2e78ca4835a088dee15dc33`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 157.8 MB (157756370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d134d4cb26e4df38cc330e351a79ac3e69934f9440a097955f19c28525e7eb`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:202ca39d2bea222bce0dfabd441f6e4b50f411b4ecd4e4528a355fad43aedc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908156ba460d7bf322eb70d6eb00b3d9ba44988f3bc6de528746bc0f75a7efc7`

```dockerfile
```

-	Layers:
	-	`sha256:ad0c4f2d8fb21820a0b278ffc0a0e2fa6a68de89c58a282053a6af77874a2bef`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
		Size: 2.4 MB (2442606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ef0cd94ee2bb41c33aadc6639346cfb1d145c95fa741ffc1641af893d953b3`  
		Last Modified: Mon, 17 Mar 2025 23:25:41 GMT  
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
$ docker pull julia@sha256:8bbc1b96adda6ada439f54853cbc3fe2836171e2690efc368031be14172de8e1
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
$ docker pull julia@sha256:88d907ae023c19fd075d27c1e8104a778613f1b14f68aa8c32470e7276a7afc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (208970683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7889065a5f19a3bae6da547ab97607cdb8105434d44de30b6689b1e2ea3d76f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 10 Mar 2025 23:59:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399cd1c6ef62c72c87eab5c68d580c0dde40c5022b3497721996ef96af22522d`  
		Last Modified: Mon, 17 Mar 2025 23:13:24 GMT  
		Size: 2.2 MB (2222647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4e344ad943cf3175024a0b796712a985e108f911896e3624d2a34104d68ed3`  
		Last Modified: Mon, 17 Mar 2025 23:13:28 GMT  
		Size: 176.5 MB (176493835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f83f5c5f5abab7ee47bbeaa9b07bee8af96e033bfaf5456c0c519f1c41537b6`  
		Last Modified: Mon, 17 Mar 2025 23:13:23 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:d8544b20aa86e2a26805ae5ad79da53e27ebd5ee5dc5ed89b1671bd4a6d8f7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6180839743035d582b2360a399abeab66580ede696aa1f0ac5540423280630f`

```dockerfile
```

-	Layers:
	-	`sha256:d71cd102171ced66ec44789dfe2c1eb9d2fb6129265d8e463cd76b24d7cc2b7b`  
		Last Modified: Mon, 17 Mar 2025 23:13:24 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea5c3e7e7393cdb0427b575f13f80db3fbca86dabecf4d15375fea3b13917fe`  
		Last Modified: Mon, 17 Mar 2025 23:13:23 GMT  
		Size: 16.6 KB (16624 bytes)  
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
$ docker pull julia@sha256:f4e754a7e05bbd3e06991c659e1890275bd9ab1cf08606a831d4508266b88e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191265135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f886c112b09dda985449d9352f0d8d0e23ed0ee664d7292cd30b66f9a99be37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 10 Mar 2025 23:59:15 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7936b0bfcb6212ad77af40e650966f94f678976c0322069ac4c10605546b3d`  
		Last Modified: Mon, 17 Mar 2025 23:25:34 GMT  
		Size: 2.3 MB (2328061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33735c78cbea761a7e61f5ab4efb142f413debdc930fdc75bf62fa8fab58192e`  
		Last Modified: Mon, 17 Mar 2025 23:25:38 GMT  
		Size: 157.8 MB (157756369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4ee1d611e9fd550c0d6d5da5a726885f8315625e1884a12b05b897ac224bb2`  
		Last Modified: Mon, 17 Mar 2025 23:25:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.9-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:844c7fbc3986752e99e75184c851aae7cca0d39f9e60100b0c7645c3e67adc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c546f98e5adadf6cc31dd6d737ea835c4486ebfeca905ab03518fa672573d43`

```dockerfile
```

-	Layers:
	-	`sha256:b65f9d183eb04ce257609b5f760a6fe2c570f1efb55c2038b87b0db8fb00d57f`  
		Last Modified: Mon, 17 Mar 2025 23:25:35 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6ae600d918ed9e000a561c579e37a336e8f9b283ebb4a2388022f9d7abd998`  
		Last Modified: Mon, 17 Mar 2025 23:25:34 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.9-windowsservercore`

```console
$ docker pull julia@sha256:39ddd683c3d3906445f709e17366ccb98408fa1d78ab65041fe6d67aed264b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `julia:1.10.9-windowsservercore` - windows version 10.0.26100.3476; amd64

```console
$ docker pull julia@sha256:6d4322e0a6962f14b38b77152b468a80195909b605d18647e1dbafc853b16bfb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3097391045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810d87f0ce83839f4773b100f8201db6aa3cf3697dc1cf60a7d84ffb73b3eabf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:27 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:47:28 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:47:29 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:48:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:48:14 GMT
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
	-	`sha256:06646829988e8751e866ce158547a93bf81c62c298e78e05965cb36ed5abe822`  
		Last Modified: Wed, 12 Mar 2025 18:48:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea9e5b43eb491f8227d43913edb19774bf9b3e2ceb9e721f6cf2fb7aef01bff`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa504cb06c4bf82666f726321b5b25f6a806936d4a562f1d510289eb0d49a136`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0eab3c553aa5966e5f06766a08d74abbe154aeb3e6a302f4b770010e34ffbd`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b72da77d1a2d616a388a688ba110a2ad50f83a56d6efce54a1e835374427c48`  
		Last Modified: Wed, 12 Mar 2025 18:48:46 GMT  
		Size: 188.7 MB (188736818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd649bbcba8e52396d192f5c3d1f24263e487fdcc82e2eb6c382c2a659d9ad`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.9-windowsservercore` - windows version 10.0.20348.3328; amd64

```console
$ docker pull julia@sha256:85c852b88149651a8e50c2641cdd9abdebe68dc398153324dc358891e88fb73c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2458640046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2059f62896dc80b0545285128282d1899c08182b87facd764e087ab2aa5779a3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:52:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:31 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:52:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:52:33 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:53:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:53:28 GMT
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
	-	`sha256:f7fcbbdc81fb789b7a508252cc8ceeccaefd394c89761e59ad500398276ef5df`  
		Last Modified: Wed, 12 Mar 2025 18:53:32 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3d43167617a095ca5f3123a244c87b642b0dbb46452b99fc560550abaa877f`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aede456ed8c6cd01914b66b210c124e1a6bf42f20115907ed65d224801a36f0`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f17adaa48f685bd225142f5e3f239584302ac3993e0dd9f9c84db0ee4ad2c6`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ddba1729af0274e0b2dc01bb9c32fd142ff08501c06573830b8cb5e18d2d2d`  
		Last Modified: Wed, 12 Mar 2025 18:53:55 GMT  
		Size: 188.7 MB (188692427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c2327b82e3dddeb6f0c6d79ff71af92ab90e43a4d96976d1124c393f58e567`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.9-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull julia@sha256:931836b6120961d4999cfdb468ab9fbef9d70c48791bdf10a6ba97bcc3addf57
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2340338714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24662fb63bbc9dd249033f01d25e885800ca56e27b6b1a88169db23d775aa679`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:55:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:55:48 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:55:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:55:49 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:57:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:57:34 GMT
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
	-	`sha256:4a22f2387ee5ad25ee19b638331e2d9e7ab6ec51a81ff35363a85b64660983b2`  
		Last Modified: Wed, 12 Mar 2025 18:57:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1177da773bdddc0e095e41fb53b6422c097150600d54ef635520c0991ac4e2`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d7be3e4f805ad689673ea4a9b10a59facbc02e95c087c33fb3f57d444e8bf`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f834bb5a94f14a47739aecf58e1c343f92bc9ed8203a8548e09590906268a10b`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc1663b632e24e8de6af0b375cdd61bbe00aff2e9224ad938dd77e9879051bf`  
		Last Modified: Wed, 12 Mar 2025 18:58:04 GMT  
		Size: 188.7 MB (188697575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f28f9e5186ef56f9683968f943528ddf2c3a7f9b3288bf5f492a7852f4a017`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.9-windowsservercore-1809`

```console
$ docker pull julia@sha256:d2fc54b1ffdf1a785dd4c5bf705933925c291353b3e249b5f12442d897743703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `julia:1.10.9-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull julia@sha256:931836b6120961d4999cfdb468ab9fbef9d70c48791bdf10a6ba97bcc3addf57
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2340338714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24662fb63bbc9dd249033f01d25e885800ca56e27b6b1a88169db23d775aa679`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 18:55:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:55:48 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:55:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:55:49 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:57:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:57:34 GMT
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
	-	`sha256:4a22f2387ee5ad25ee19b638331e2d9e7ab6ec51a81ff35363a85b64660983b2`  
		Last Modified: Wed, 12 Mar 2025 18:57:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1177da773bdddc0e095e41fb53b6422c097150600d54ef635520c0991ac4e2`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70d7be3e4f805ad689673ea4a9b10a59facbc02e95c087c33fb3f57d444e8bf`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f834bb5a94f14a47739aecf58e1c343f92bc9ed8203a8548e09590906268a10b`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc1663b632e24e8de6af0b375cdd61bbe00aff2e9224ad938dd77e9879051bf`  
		Last Modified: Wed, 12 Mar 2025 18:58:04 GMT  
		Size: 188.7 MB (188697575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f28f9e5186ef56f9683968f943528ddf2c3a7f9b3288bf5f492a7852f4a017`  
		Last Modified: Wed, 12 Mar 2025 18:57:39 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.9-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:df52872dbf50013fbd689792b396c800738bc4edd0a9f33be69cbbfbfa1be889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `julia:1.10.9-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull julia@sha256:85c852b88149651a8e50c2641cdd9abdebe68dc398153324dc358891e88fb73c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2458640046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2059f62896dc80b0545285128282d1899c08182b87facd764e087ab2aa5779a3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:52:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:52:31 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:52:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:52:33 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:53:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:53:28 GMT
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
	-	`sha256:f7fcbbdc81fb789b7a508252cc8ceeccaefd394c89761e59ad500398276ef5df`  
		Last Modified: Wed, 12 Mar 2025 18:53:32 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3d43167617a095ca5f3123a244c87b642b0dbb46452b99fc560550abaa877f`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aede456ed8c6cd01914b66b210c124e1a6bf42f20115907ed65d224801a36f0`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f17adaa48f685bd225142f5e3f239584302ac3993e0dd9f9c84db0ee4ad2c6`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ddba1729af0274e0b2dc01bb9c32fd142ff08501c06573830b8cb5e18d2d2d`  
		Last Modified: Wed, 12 Mar 2025 18:53:55 GMT  
		Size: 188.7 MB (188692427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c2327b82e3dddeb6f0c6d79ff71af92ab90e43a4d96976d1124c393f58e567`  
		Last Modified: Wed, 12 Mar 2025 18:53:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.9-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:28ad16aef46622e6b1ad508ab189593de23e2ac079c9dab4611557a62b3a1b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `julia:1.10.9-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull julia@sha256:6d4322e0a6962f14b38b77152b468a80195909b605d18647e1dbafc853b16bfb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3097391045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810d87f0ce83839f4773b100f8201db6aa3cf3697dc1cf60a7d84ffb73b3eabf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:27 GMT
ENV JULIA_VERSION=1.10.9
# Wed, 12 Mar 2025 18:47:28 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.9-win64.exe
# Wed, 12 Mar 2025 18:47:29 GMT
ENV JULIA_SHA256=64cfced950b3790279c560c53f084b28b0676e9588c918cc68f9653539b6b0df
# Wed, 12 Mar 2025 18:48:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:48:14 GMT
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
	-	`sha256:06646829988e8751e866ce158547a93bf81c62c298e78e05965cb36ed5abe822`  
		Last Modified: Wed, 12 Mar 2025 18:48:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea9e5b43eb491f8227d43913edb19774bf9b3e2ceb9e721f6cf2fb7aef01bff`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa504cb06c4bf82666f726321b5b25f6a806936d4a562f1d510289eb0d49a136`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0eab3c553aa5966e5f06766a08d74abbe154aeb3e6a302f4b770010e34ffbd`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b72da77d1a2d616a388a688ba110a2ad50f83a56d6efce54a1e835374427c48`  
		Last Modified: Wed, 12 Mar 2025 18:48:46 GMT  
		Size: 188.7 MB (188736818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fd649bbcba8e52396d192f5c3d1f24263e487fdcc82e2eb6c382c2a659d9ad`  
		Last Modified: Wed, 12 Mar 2025 18:48:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:bab8309d212703cdcb3725899e1ce3a89d6705ddc0194a37442c5d74b318180c
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

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:abedded0d1772aaeb02c6bba4109b7fd0745b4880c73eb811b30373d985d48b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302403240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b16b02d491ef44bf1edb4d4b55af7ed0859b2231bdb1cacb7dfb56f2d7d11d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf165c807d409f1e5e47644d10a56e62f760b04977240ccb92cb44373c0b0f69`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 5.7 MB (5713383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b6fe754913bc7659f03d356590438cc4eedd2dd68f4df602467584df07ac2`  
		Last Modified: Mon, 17 Mar 2025 23:13:45 GMT  
		Size: 268.5 MB (268484621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2ec09870a2c14b826ec97c7163f20459b189d4ac71ce5fc48c61be5cbf30db`  
		Last Modified: Mon, 17 Mar 2025 23:13:37 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:90638797f1b5d7e05dc89684f27edd24d0ec9c90049a8b4a7bd0ba55d5f49895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb188174850f12a03f938d4afbdc70ce9d2f1e201caf8312806b2c15c8016aa`

```dockerfile
```

-	Layers:
	-	`sha256:0485ab72220e8c25e8c44fd4643cb6401c32a43d460248901e04551b66c7a690`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.4 MB (2445468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7d10aaca52976692b814b68272ef08141b566e335fb00c2d7a87c20e54059e`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 18.4 KB (18399 bytes)  
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
$ docker pull julia@sha256:9f6cb4ab8de753dbdf08958fadb970ea57420a25940a9c66889d2675e1b30261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252906412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6160838c86bb01311ab4312fadcb5c79febbc02a9db5bec211474b6ae2d89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c313be324d81319409f757b6a9214e6e4505edd1870d857ef9335183bf456`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 5.9 MB (5872272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809e1e548a3d059caccea690a9ccc930a0ba4003bac183b117a14c4ef5eb0be5`  
		Last Modified: Mon, 17 Mar 2025 23:25:50 GMT  
		Size: 217.8 MB (217844242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790e28391a0fe4d76f864c7f5f2ad1d677cd00da4cfc75068849cd664e65683`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:66caada27c36606986912deb412ff68f7f7ec9bddf54775f6a16093eab0cfb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118730f876ef85874545babb36fc06e2768e0d5b721d060f23817c42124b3bc`

```dockerfile
```

-	Layers:
	-	`sha256:76a154e6def364e394399ef31951b53809301692945ecf7401bee9a909343563`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 2.4 MB (2442541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c82965d60d3d4aa1404ef241e92932d6ceef303d9cfac5e6b23310f702ee2b`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 18.3 KB (18345 bytes)  
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

### `julia:1.11` - windows version 10.0.26100.3476; amd64

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

### `julia:1.11` - windows version 10.0.20348.3328; amd64

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

### `julia:1.11` - windows version 10.0.17763.7009; amd64

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

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:5e3d4eba6d196e37b910cdcc059ff98730e33946bfcf0d9d813b3a56060e5fb6
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
$ docker pull julia@sha256:abedded0d1772aaeb02c6bba4109b7fd0745b4880c73eb811b30373d985d48b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302403240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b16b02d491ef44bf1edb4d4b55af7ed0859b2231bdb1cacb7dfb56f2d7d11d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf165c807d409f1e5e47644d10a56e62f760b04977240ccb92cb44373c0b0f69`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 5.7 MB (5713383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b6fe754913bc7659f03d356590438cc4eedd2dd68f4df602467584df07ac2`  
		Last Modified: Mon, 17 Mar 2025 23:13:45 GMT  
		Size: 268.5 MB (268484621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2ec09870a2c14b826ec97c7163f20459b189d4ac71ce5fc48c61be5cbf30db`  
		Last Modified: Mon, 17 Mar 2025 23:13:37 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:90638797f1b5d7e05dc89684f27edd24d0ec9c90049a8b4a7bd0ba55d5f49895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb188174850f12a03f938d4afbdc70ce9d2f1e201caf8312806b2c15c8016aa`

```dockerfile
```

-	Layers:
	-	`sha256:0485ab72220e8c25e8c44fd4643cb6401c32a43d460248901e04551b66c7a690`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.4 MB (2445468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7d10aaca52976692b814b68272ef08141b566e335fb00c2d7a87c20e54059e`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 18.4 KB (18399 bytes)  
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
$ docker pull julia@sha256:9f6cb4ab8de753dbdf08958fadb970ea57420a25940a9c66889d2675e1b30261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252906412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6160838c86bb01311ab4312fadcb5c79febbc02a9db5bec211474b6ae2d89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c313be324d81319409f757b6a9214e6e4505edd1870d857ef9335183bf456`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 5.9 MB (5872272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809e1e548a3d059caccea690a9ccc930a0ba4003bac183b117a14c4ef5eb0be5`  
		Last Modified: Mon, 17 Mar 2025 23:25:50 GMT  
		Size: 217.8 MB (217844242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790e28391a0fe4d76f864c7f5f2ad1d677cd00da4cfc75068849cd664e65683`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:66caada27c36606986912deb412ff68f7f7ec9bddf54775f6a16093eab0cfb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118730f876ef85874545babb36fc06e2768e0d5b721d060f23817c42124b3bc`

```dockerfile
```

-	Layers:
	-	`sha256:76a154e6def364e394399ef31951b53809301692945ecf7401bee9a909343563`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 2.4 MB (2442541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c82965d60d3d4aa1404ef241e92932d6ceef303d9cfac5e6b23310f702ee2b`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 18.3 KB (18345 bytes)  
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
$ docker pull julia@sha256:24cfd68cf777099d9204b778a9ac206fee9b3d4f8500b049aa928683671f1bb3
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
$ docker pull julia@sha256:e19adf478c932ddceb0cd543f385f1fbdf2e7112843ee8e3b0ceae918862f56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300961318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de69c31d798eaabef70e7c3edcfb0e64e992ef1d6b246a4ca76a53a04c50754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeafcf0ad42d0b7ba886b69799967535eaa98a21f8fbe73943453496d291b8ed`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.2 MB (2222677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39d5991f07d5c2acfdcb0ba4c1d31d3d14e71397cd848796aab3da3ab16430b`  
		Last Modified: Mon, 17 Mar 2025 23:13:44 GMT  
		Size: 268.5 MB (268484435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300bb409d0fb700f649d71205c2ca618d30e3779cfd378b109aa36417b48a88b`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:568bbe514f6c6d8dcf71ac23382e97947a5d89db7568870c18c84df734717373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7397c81b0cbe0408efb3157682c2b76db2f14059e420037d780d658526b746e`

```dockerfile
```

-	Layers:
	-	`sha256:542940db3f80626a40eb95fb688aeea3a5578fbd74ffe1d9dd79b9a8e1177c1e`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8e498258530cc6b44d6affd29bf756952c36580d0e9fe0c55c335ae153d695`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 17.2 KB (17230 bytes)  
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
$ docker pull julia@sha256:33620ae3d96ab9adaf7dab3ccf2264c0e80196363fd2b850af8b3a5c770b8f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251354291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c38d8ab7fbe3538882b71342b7da6729f5cae4146da2dffe153379cfe2c4d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecef606b0a992420b25835cdfaeff30b8f8795129a713d037053dda8ca79abf`  
		Last Modified: Mon, 17 Mar 2025 23:25:46 GMT  
		Size: 2.3 MB (2328062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebe87c0ddbcc8ab060a7709e68b17c43db9bf75d54ac67018c6503307a7bd5f`  
		Last Modified: Mon, 17 Mar 2025 23:25:51 GMT  
		Size: 217.8 MB (217845523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07087d0b8d9a969e61a9ec020d1c8afbb9fc0e52936e359dc2007c6063c0d7a`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:185707a3a086745c07344c4e3eea6ac898c6e92cb85bd8333d7d68fe75263122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b637ca421f08d79789664405fb6785198aa5af754f6921378a49380245cc7ae1`

```dockerfile
```

-	Layers:
	-	`sha256:418ba4380bab52bce1f331afb478eb78c44c136d74ae008472a52f32c9e9fe76`  
		Last Modified: Mon, 17 Mar 2025 23:25:46 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e547ae26d53300a9467d2c3227c5103d3827a9f84decb55f76ba258aa5d7f4cf`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:a58330d3909779ea6fda30203e9a87609ae28d7f332fe903b34f711bab76541a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.26100.3476; amd64

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

### `julia:1.11-windowsservercore` - windows version 10.0.20348.3328; amd64

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

### `julia:1.11-windowsservercore` - windows version 10.0.17763.7009; amd64

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

## `julia:1.11-windowsservercore-1809`

```console
$ docker pull julia@sha256:690b3bb2cd57b68ea519b4c0e834a243b9d4bd415b7de871605ca4866b693169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `julia:1.11-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

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

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:4426e2a8c83587fbc2b48d4eb2521fd9d412bc9cb7f6465a5c221e1712b6f1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

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

## `julia:1.11-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:096ec1ac6bd7714f5cb4555a0f63af46ee152de56046f33fa46583ca3c4b278e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `julia:1.11-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

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

## `julia:1.11.4`

```console
$ docker pull julia@sha256:bab8309d212703cdcb3725899e1ce3a89d6705ddc0194a37442c5d74b318180c
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

### `julia:1.11.4` - linux; amd64

```console
$ docker pull julia@sha256:abedded0d1772aaeb02c6bba4109b7fd0745b4880c73eb811b30373d985d48b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302403240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b16b02d491ef44bf1edb4d4b55af7ed0859b2231bdb1cacb7dfb56f2d7d11d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf165c807d409f1e5e47644d10a56e62f760b04977240ccb92cb44373c0b0f69`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 5.7 MB (5713383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b6fe754913bc7659f03d356590438cc4eedd2dd68f4df602467584df07ac2`  
		Last Modified: Mon, 17 Mar 2025 23:13:45 GMT  
		Size: 268.5 MB (268484621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2ec09870a2c14b826ec97c7163f20459b189d4ac71ce5fc48c61be5cbf30db`  
		Last Modified: Mon, 17 Mar 2025 23:13:37 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.4` - unknown; unknown

```console
$ docker pull julia@sha256:90638797f1b5d7e05dc89684f27edd24d0ec9c90049a8b4a7bd0ba55d5f49895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb188174850f12a03f938d4afbdc70ce9d2f1e201caf8312806b2c15c8016aa`

```dockerfile
```

-	Layers:
	-	`sha256:0485ab72220e8c25e8c44fd4643cb6401c32a43d460248901e04551b66c7a690`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.4 MB (2445468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7d10aaca52976692b814b68272ef08141b566e335fb00c2d7a87c20e54059e`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 18.4 KB (18399 bytes)  
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
$ docker pull julia@sha256:9f6cb4ab8de753dbdf08958fadb970ea57420a25940a9c66889d2675e1b30261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252906412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6160838c86bb01311ab4312fadcb5c79febbc02a9db5bec211474b6ae2d89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c313be324d81319409f757b6a9214e6e4505edd1870d857ef9335183bf456`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 5.9 MB (5872272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809e1e548a3d059caccea690a9ccc930a0ba4003bac183b117a14c4ef5eb0be5`  
		Last Modified: Mon, 17 Mar 2025 23:25:50 GMT  
		Size: 217.8 MB (217844242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790e28391a0fe4d76f864c7f5f2ad1d677cd00da4cfc75068849cd664e65683`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.4` - unknown; unknown

```console
$ docker pull julia@sha256:66caada27c36606986912deb412ff68f7f7ec9bddf54775f6a16093eab0cfb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118730f876ef85874545babb36fc06e2768e0d5b721d060f23817c42124b3bc`

```dockerfile
```

-	Layers:
	-	`sha256:76a154e6def364e394399ef31951b53809301692945ecf7401bee9a909343563`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 2.4 MB (2442541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c82965d60d3d4aa1404ef241e92932d6ceef303d9cfac5e6b23310f702ee2b`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 18.3 KB (18345 bytes)  
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

### `julia:1.11.4` - windows version 10.0.26100.3476; amd64

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

### `julia:1.11.4` - windows version 10.0.20348.3328; amd64

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

### `julia:1.11.4` - windows version 10.0.17763.7009; amd64

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

## `julia:1.11.4-bookworm`

```console
$ docker pull julia@sha256:5e3d4eba6d196e37b910cdcc059ff98730e33946bfcf0d9d813b3a56060e5fb6
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
$ docker pull julia@sha256:abedded0d1772aaeb02c6bba4109b7fd0745b4880c73eb811b30373d985d48b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302403240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b16b02d491ef44bf1edb4d4b55af7ed0859b2231bdb1cacb7dfb56f2d7d11d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf165c807d409f1e5e47644d10a56e62f760b04977240ccb92cb44373c0b0f69`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 5.7 MB (5713383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b6fe754913bc7659f03d356590438cc4eedd2dd68f4df602467584df07ac2`  
		Last Modified: Mon, 17 Mar 2025 23:13:45 GMT  
		Size: 268.5 MB (268484621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2ec09870a2c14b826ec97c7163f20459b189d4ac71ce5fc48c61be5cbf30db`  
		Last Modified: Mon, 17 Mar 2025 23:13:37 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.4-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:90638797f1b5d7e05dc89684f27edd24d0ec9c90049a8b4a7bd0ba55d5f49895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb188174850f12a03f938d4afbdc70ce9d2f1e201caf8312806b2c15c8016aa`

```dockerfile
```

-	Layers:
	-	`sha256:0485ab72220e8c25e8c44fd4643cb6401c32a43d460248901e04551b66c7a690`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.4 MB (2445468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7d10aaca52976692b814b68272ef08141b566e335fb00c2d7a87c20e54059e`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 18.4 KB (18399 bytes)  
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
$ docker pull julia@sha256:9f6cb4ab8de753dbdf08958fadb970ea57420a25940a9c66889d2675e1b30261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252906412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6160838c86bb01311ab4312fadcb5c79febbc02a9db5bec211474b6ae2d89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c313be324d81319409f757b6a9214e6e4505edd1870d857ef9335183bf456`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 5.9 MB (5872272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809e1e548a3d059caccea690a9ccc930a0ba4003bac183b117a14c4ef5eb0be5`  
		Last Modified: Mon, 17 Mar 2025 23:25:50 GMT  
		Size: 217.8 MB (217844242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790e28391a0fe4d76f864c7f5f2ad1d677cd00da4cfc75068849cd664e65683`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.4-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:66caada27c36606986912deb412ff68f7f7ec9bddf54775f6a16093eab0cfb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118730f876ef85874545babb36fc06e2768e0d5b721d060f23817c42124b3bc`

```dockerfile
```

-	Layers:
	-	`sha256:76a154e6def364e394399ef31951b53809301692945ecf7401bee9a909343563`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 2.4 MB (2442541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c82965d60d3d4aa1404ef241e92932d6ceef303d9cfac5e6b23310f702ee2b`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 18.3 KB (18345 bytes)  
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
$ docker pull julia@sha256:24cfd68cf777099d9204b778a9ac206fee9b3d4f8500b049aa928683671f1bb3
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
$ docker pull julia@sha256:e19adf478c932ddceb0cd543f385f1fbdf2e7112843ee8e3b0ceae918862f56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300961318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de69c31d798eaabef70e7c3edcfb0e64e992ef1d6b246a4ca76a53a04c50754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeafcf0ad42d0b7ba886b69799967535eaa98a21f8fbe73943453496d291b8ed`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.2 MB (2222677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39d5991f07d5c2acfdcb0ba4c1d31d3d14e71397cd848796aab3da3ab16430b`  
		Last Modified: Mon, 17 Mar 2025 23:13:44 GMT  
		Size: 268.5 MB (268484435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300bb409d0fb700f649d71205c2ca618d30e3779cfd378b109aa36417b48a88b`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.4-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:568bbe514f6c6d8dcf71ac23382e97947a5d89db7568870c18c84df734717373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7397c81b0cbe0408efb3157682c2b76db2f14059e420037d780d658526b746e`

```dockerfile
```

-	Layers:
	-	`sha256:542940db3f80626a40eb95fb688aeea3a5578fbd74ffe1d9dd79b9a8e1177c1e`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8e498258530cc6b44d6affd29bf756952c36580d0e9fe0c55c335ae153d695`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 17.2 KB (17230 bytes)  
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
$ docker pull julia@sha256:33620ae3d96ab9adaf7dab3ccf2264c0e80196363fd2b850af8b3a5c770b8f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251354291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c38d8ab7fbe3538882b71342b7da6729f5cae4146da2dffe153379cfe2c4d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecef606b0a992420b25835cdfaeff30b8f8795129a713d037053dda8ca79abf`  
		Last Modified: Mon, 17 Mar 2025 23:25:46 GMT  
		Size: 2.3 MB (2328062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebe87c0ddbcc8ab060a7709e68b17c43db9bf75d54ac67018c6503307a7bd5f`  
		Last Modified: Mon, 17 Mar 2025 23:25:51 GMT  
		Size: 217.8 MB (217845523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07087d0b8d9a969e61a9ec020d1c8afbb9fc0e52936e359dc2007c6063c0d7a`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.4-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:185707a3a086745c07344c4e3eea6ac898c6e92cb85bd8333d7d68fe75263122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b637ca421f08d79789664405fb6785198aa5af754f6921378a49380245cc7ae1`

```dockerfile
```

-	Layers:
	-	`sha256:418ba4380bab52bce1f331afb478eb78c44c136d74ae008472a52f32c9e9fe76`  
		Last Modified: Mon, 17 Mar 2025 23:25:46 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e547ae26d53300a9467d2c3227c5103d3827a9f84decb55f76ba258aa5d7f4cf`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.4-windowsservercore`

```console
$ docker pull julia@sha256:a58330d3909779ea6fda30203e9a87609ae28d7f332fe903b34f711bab76541a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `julia:1.11.4-windowsservercore` - windows version 10.0.26100.3476; amd64

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

### `julia:1.11.4-windowsservercore` - windows version 10.0.20348.3328; amd64

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

### `julia:1.11.4-windowsservercore` - windows version 10.0.17763.7009; amd64

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

## `julia:1.11.4-windowsservercore-1809`

```console
$ docker pull julia@sha256:690b3bb2cd57b68ea519b4c0e834a243b9d4bd415b7de871605ca4866b693169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `julia:1.11.4-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

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

## `julia:1.11.4-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:4426e2a8c83587fbc2b48d4eb2521fd9d412bc9cb7f6465a5c221e1712b6f1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `julia:1.11.4-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

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

## `julia:1.11.4-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:096ec1ac6bd7714f5cb4555a0f63af46ee152de56046f33fa46583ca3c4b278e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `julia:1.11.4-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

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

## `julia:bookworm`

```console
$ docker pull julia@sha256:5e3d4eba6d196e37b910cdcc059ff98730e33946bfcf0d9d813b3a56060e5fb6
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
$ docker pull julia@sha256:abedded0d1772aaeb02c6bba4109b7fd0745b4880c73eb811b30373d985d48b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302403240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b16b02d491ef44bf1edb4d4b55af7ed0859b2231bdb1cacb7dfb56f2d7d11d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf165c807d409f1e5e47644d10a56e62f760b04977240ccb92cb44373c0b0f69`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 5.7 MB (5713383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b6fe754913bc7659f03d356590438cc4eedd2dd68f4df602467584df07ac2`  
		Last Modified: Mon, 17 Mar 2025 23:13:45 GMT  
		Size: 268.5 MB (268484621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2ec09870a2c14b826ec97c7163f20459b189d4ac71ce5fc48c61be5cbf30db`  
		Last Modified: Mon, 17 Mar 2025 23:13:37 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:90638797f1b5d7e05dc89684f27edd24d0ec9c90049a8b4a7bd0ba55d5f49895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb188174850f12a03f938d4afbdc70ce9d2f1e201caf8312806b2c15c8016aa`

```dockerfile
```

-	Layers:
	-	`sha256:0485ab72220e8c25e8c44fd4643cb6401c32a43d460248901e04551b66c7a690`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.4 MB (2445468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7d10aaca52976692b814b68272ef08141b566e335fb00c2d7a87c20e54059e`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 18.4 KB (18399 bytes)  
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
$ docker pull julia@sha256:9f6cb4ab8de753dbdf08958fadb970ea57420a25940a9c66889d2675e1b30261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252906412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6160838c86bb01311ab4312fadcb5c79febbc02a9db5bec211474b6ae2d89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c313be324d81319409f757b6a9214e6e4505edd1870d857ef9335183bf456`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 5.9 MB (5872272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809e1e548a3d059caccea690a9ccc930a0ba4003bac183b117a14c4ef5eb0be5`  
		Last Modified: Mon, 17 Mar 2025 23:25:50 GMT  
		Size: 217.8 MB (217844242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790e28391a0fe4d76f864c7f5f2ad1d677cd00da4cfc75068849cd664e65683`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:66caada27c36606986912deb412ff68f7f7ec9bddf54775f6a16093eab0cfb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118730f876ef85874545babb36fc06e2768e0d5b721d060f23817c42124b3bc`

```dockerfile
```

-	Layers:
	-	`sha256:76a154e6def364e394399ef31951b53809301692945ecf7401bee9a909343563`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 2.4 MB (2442541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c82965d60d3d4aa1404ef241e92932d6ceef303d9cfac5e6b23310f702ee2b`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 18.3 KB (18345 bytes)  
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
$ docker pull julia@sha256:24cfd68cf777099d9204b778a9ac206fee9b3d4f8500b049aa928683671f1bb3
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
$ docker pull julia@sha256:e19adf478c932ddceb0cd543f385f1fbdf2e7112843ee8e3b0ceae918862f56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.0 MB (300961318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de69c31d798eaabef70e7c3edcfb0e64e992ef1d6b246a4ca76a53a04c50754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeafcf0ad42d0b7ba886b69799967535eaa98a21f8fbe73943453496d291b8ed`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.2 MB (2222677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39d5991f07d5c2acfdcb0ba4c1d31d3d14e71397cd848796aab3da3ab16430b`  
		Last Modified: Mon, 17 Mar 2025 23:13:44 GMT  
		Size: 268.5 MB (268484435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300bb409d0fb700f649d71205c2ca618d30e3779cfd378b109aa36417b48a88b`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:568bbe514f6c6d8dcf71ac23382e97947a5d89db7568870c18c84df734717373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7397c81b0cbe0408efb3157682c2b76db2f14059e420037d780d658526b746e`

```dockerfile
```

-	Layers:
	-	`sha256:542940db3f80626a40eb95fb688aeea3a5578fbd74ffe1d9dd79b9a8e1177c1e`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8e498258530cc6b44d6affd29bf756952c36580d0e9fe0c55c335ae153d695`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 17.2 KB (17230 bytes)  
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
$ docker pull julia@sha256:33620ae3d96ab9adaf7dab3ccf2264c0e80196363fd2b850af8b3a5c770b8f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251354291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c38d8ab7fbe3538882b71342b7da6729f5cae4146da2dffe153379cfe2c4d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecef606b0a992420b25835cdfaeff30b8f8795129a713d037053dda8ca79abf`  
		Last Modified: Mon, 17 Mar 2025 23:25:46 GMT  
		Size: 2.3 MB (2328062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebe87c0ddbcc8ab060a7709e68b17c43db9bf75d54ac67018c6503307a7bd5f`  
		Last Modified: Mon, 17 Mar 2025 23:25:51 GMT  
		Size: 217.8 MB (217845523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07087d0b8d9a969e61a9ec020d1c8afbb9fc0e52936e359dc2007c6063c0d7a`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:185707a3a086745c07344c4e3eea6ac898c6e92cb85bd8333d7d68fe75263122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b637ca421f08d79789664405fb6785198aa5af754f6921378a49380245cc7ae1`

```dockerfile
```

-	Layers:
	-	`sha256:418ba4380bab52bce1f331afb478eb78c44c136d74ae008472a52f32c9e9fe76`  
		Last Modified: Mon, 17 Mar 2025 23:25:46 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e547ae26d53300a9467d2c3227c5103d3827a9f84decb55f76ba258aa5d7f4cf`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:bab8309d212703cdcb3725899e1ce3a89d6705ddc0194a37442c5d74b318180c
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
$ docker pull julia@sha256:abedded0d1772aaeb02c6bba4109b7fd0745b4880c73eb811b30373d985d48b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302403240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b16b02d491ef44bf1edb4d4b55af7ed0859b2231bdb1cacb7dfb56f2d7d11d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf165c807d409f1e5e47644d10a56e62f760b04977240ccb92cb44373c0b0f69`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 5.7 MB (5713383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b6fe754913bc7659f03d356590438cc4eedd2dd68f4df602467584df07ac2`  
		Last Modified: Mon, 17 Mar 2025 23:13:45 GMT  
		Size: 268.5 MB (268484621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2ec09870a2c14b826ec97c7163f20459b189d4ac71ce5fc48c61be5cbf30db`  
		Last Modified: Mon, 17 Mar 2025 23:13:37 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:90638797f1b5d7e05dc89684f27edd24d0ec9c90049a8b4a7bd0ba55d5f49895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb188174850f12a03f938d4afbdc70ce9d2f1e201caf8312806b2c15c8016aa`

```dockerfile
```

-	Layers:
	-	`sha256:0485ab72220e8c25e8c44fd4643cb6401c32a43d460248901e04551b66c7a690`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 2.4 MB (2445468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7d10aaca52976692b814b68272ef08141b566e335fb00c2d7a87c20e54059e`  
		Last Modified: Mon, 17 Mar 2025 23:13:38 GMT  
		Size: 18.4 KB (18399 bytes)  
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
$ docker pull julia@sha256:9f6cb4ab8de753dbdf08958fadb970ea57420a25940a9c66889d2675e1b30261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252906412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe6160838c86bb01311ab4312fadcb5c79febbc02a9db5bec211474b6ae2d89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 11 Mar 2025 00:06:05 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c313be324d81319409f757b6a9214e6e4505edd1870d857ef9335183bf456`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 5.9 MB (5872272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809e1e548a3d059caccea690a9ccc930a0ba4003bac183b117a14c4ef5eb0be5`  
		Last Modified: Mon, 17 Mar 2025 23:25:50 GMT  
		Size: 217.8 MB (217844242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790e28391a0fe4d76f864c7f5f2ad1d677cd00da4cfc75068849cd664e65683`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:66caada27c36606986912deb412ff68f7f7ec9bddf54775f6a16093eab0cfb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4118730f876ef85874545babb36fc06e2768e0d5b721d060f23817c42124b3bc`

```dockerfile
```

-	Layers:
	-	`sha256:76a154e6def364e394399ef31951b53809301692945ecf7401bee9a909343563`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 2.4 MB (2442541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c82965d60d3d4aa1404ef241e92932d6ceef303d9cfac5e6b23310f702ee2b`  
		Last Modified: Mon, 17 Mar 2025 23:25:45 GMT  
		Size: 18.3 KB (18345 bytes)  
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

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:a58330d3909779ea6fda30203e9a87609ae28d7f332fe903b34f711bab76541a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `julia:windowsservercore` - windows version 10.0.26100.3476; amd64

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

### `julia:windowsservercore` - windows version 10.0.20348.3328; amd64

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

### `julia:windowsservercore` - windows version 10.0.17763.7009; amd64

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

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:690b3bb2cd57b68ea519b4c0e834a243b9d4bd415b7de871605ca4866b693169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.7009; amd64

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

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:4426e2a8c83587fbc2b48d4eb2521fd9d412bc9cb7f6465a5c221e1712b6f1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

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

## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:096ec1ac6bd7714f5cb4555a0f63af46ee152de56046f33fa46583ca3c4b278e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

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
