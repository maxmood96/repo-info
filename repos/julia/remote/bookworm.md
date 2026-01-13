## `julia:bookworm`

```console
$ docker pull julia@sha256:5e68a8f4b2d03eaf7e4e31ab6aa6182a170bd6b9d152136437454547a815f33b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:bookworm` - linux; amd64

```console
$ docker pull julia@sha256:72dd5dcea2af512583924e6c7773a43881f19f38084159d1be244922f1797884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.8 MB (323769205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e48d2934b4aa4d18709f180d0a3c7504717934152bdab1424975923746c89c74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Thu, 08 Jan 2026 19:04:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Jan 2026 19:04:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 08 Jan 2026 19:04:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Jan 2026 19:04:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 08 Jan 2026 19:04:29 GMT
ENV JULIA_VERSION=1.12.4
# Thu, 08 Jan 2026 19:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 08 Jan 2026 19:04:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 08 Jan 2026 19:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Jan 2026 19:04:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648fc7fc079142c391b2b6869e1160c6171968d973cdfd83c22010af842c8fc3`  
		Last Modified: Thu, 08 Jan 2026 19:05:49 GMT  
		Size: 5.7 MB (5716385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abd5e63431ab1440254f8567bcf203a78107af180cd63744981b342e4788b8d`  
		Last Modified: Thu, 08 Jan 2026 19:06:02 GMT  
		Size: 289.8 MB (289824029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3bd07ac5abdcb546fa58eebdf02d5382bbf93956cc0900c25ff8167eec5ffe`  
		Last Modified: Thu, 08 Jan 2026 19:05:49 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:11ff0f3dd2322dee46f513dd0f929c905deb5d08a229e7f18fa6fab9b94f4120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:380ee7e2e19b6bb3f1d85eb541169c9e8935dc4b3c7662cba1e477751f7fab1f`

```dockerfile
```

-	Layers:
	-	`sha256:3473c5c1c693a8f98ace833b81e7a66af7fdd2770ad92b7d5e5d002ec073cbf8`  
		Last Modified: Thu, 08 Jan 2026 21:02:58 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2faa79fe6e6fbf376b9a024644495bd570405a2d5771cb21275704edd8050f54`  
		Last Modified: Thu, 08 Jan 2026 21:02:59 GMT  
		Size: 16.5 KB (16546 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:7df69debe6e7b9d5e176ea0f91d5a65505b6aad70bdd076489b9ef28110157f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344948590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af62499fae014adde6c44706a1467725361fd60e68dfec7622d11f53572259b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:22:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Jan 2026 01:22:40 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:22:40 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Jan 2026 01:22:40 GMT
ENV JULIA_VERSION=1.12.4
# Tue, 13 Jan 2026 01:22:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 13 Jan 2026 01:22:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6261cdbd0dfe0a5a37080c4e0d495c4f202ae5c0e908ac614c11ff7b79ea984`  
		Last Modified: Tue, 13 Jan 2026 01:23:41 GMT  
		Size: 5.6 MB (5567755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf441ca52a584796d6766b0f2a2eb115e6b1ed8222d81c9d970e8dd477f7952`  
		Last Modified: Tue, 13 Jan 2026 01:23:52 GMT  
		Size: 311.3 MB (311272579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f36a0f2f0d447c47d15f33bc6f7265affebeb061e1366e62b07fea0f36952e8`  
		Last Modified: Tue, 13 Jan 2026 01:23:41 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:151c56dcbd6f925baef578450639e99c8b234cb36bd9321a0da0f5e2022c11fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f40530ab143ebf523a1e6e1d02d7f4fc180161527f21034433c30675df5532`

```dockerfile
```

-	Layers:
	-	`sha256:12c9c237ad03513b98018ea102ee3ad801aaf529ed0fee46f53c1326973584f2`  
		Last Modified: Tue, 13 Jan 2026 03:04:33 GMT  
		Size: 2.6 MB (2567971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c68c44c61791e1147b79d21f11761ae3d46187ddfdec15c7ad9986465f19de5`  
		Last Modified: Tue, 13 Jan 2026 03:04:39 GMT  
		Size: 16.7 KB (16665 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:ff79315d3564940d86072e7ed90dc3d972c2bb9429ad72a30e68633b1d234164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266295707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1489ba87cf3b0b57c196abeb47a005e870cb5c0bb1388837429eaec10bf6c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:58 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Jan 2026 01:18:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:18:58 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Jan 2026 01:18:58 GMT
ENV JULIA_VERSION=1.12.4
# Tue, 13 Jan 2026 01:18:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 13 Jan 2026 01:18:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:18:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:18:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:45 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226ce8b7e04a04fa6b26e2c2d91e45c34f22111596846479288481a9a0b17c1a`  
		Last Modified: Tue, 13 Jan 2026 01:19:40 GMT  
		Size: 5.9 MB (5878408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e5bc3d50ce9b90c97e946d51c176dde97ac5b648d6eafdd359c1c0f161f4e6`  
		Last Modified: Tue, 13 Jan 2026 01:19:51 GMT  
		Size: 231.2 MB (231206861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866423de7ae1c1430a3da51bcf61bf9525742d7839b4b4c884ef2735aeada9c4`  
		Last Modified: Tue, 13 Jan 2026 01:19:39 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0b861165d96eb671b80db24417b8ea94702868dba09b2a204842f37f03272417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a587441191ec347516d97030610b14943f4fff6ecf2bb8cac056c2986dd5bee`

```dockerfile
```

-	Layers:
	-	`sha256:c3484d6ab3102b2f72444ab78810bd8fdc50286bef8959851f668329952478f5`  
		Last Modified: Tue, 13 Jan 2026 03:04:45 GMT  
		Size: 2.6 MB (2564843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5388d9e5733901f1d4a328340e34074ece02d3b2924920ca756026970bd5e644`  
		Last Modified: Tue, 13 Jan 2026 03:04:45 GMT  
		Size: 16.5 KB (16513 bytes)  
		MIME: application/vnd.in-toto+json
