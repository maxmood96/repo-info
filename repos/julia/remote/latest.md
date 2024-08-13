## `julia:latest`

```console
$ docker pull julia@sha256:48c57c62ee9c56d11e4e4aea03dbeca89af22817232c074debe9941e44d749d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:9d86dd2f27a5cd8632ff194246834f8381d379421118824e5c3ed8d94da20c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211059398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c4ae89d4e53d45ae8d7e1b7b5de73c722c40eb01bec275be5cbb7f8b8559bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Jun 2024 23:59:16 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Jun 2024 23:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.4-linux-x86_64.tar.gz'; 			sha256='079f61757c3b5b40d2ade052b3cc4816f50f7ef6df668825772562b3746adff1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.4-linux-aarch64.tar.gz'; 			sha256='ae4ae6ade84a103cdf30ce91c8d4035a0ef51c3e2e66f90a0c13abeb4e100fc4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.4-linux-i686.tar.gz'; 			sha256='5771c6032b2be4442f4d4f4fc610eac09a48888ce1f4a41d10208e9d413f5054'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.4-linux-ppc64le.tar.gz'; 			sha256='0703f983894974491715e816a006e0f063966544023f470c94c71ef99dff9dba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f9c7f7497bf76f572bcc80b9a6467130776724540bddf084f997e62236d237`  
		Last Modified: Tue, 13 Aug 2024 01:19:24 GMT  
		Size: 5.7 MB (5711066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfd68a54a05d8193c454b26865397e855193e279941ef5b93d02ec278f232ba`  
		Last Modified: Tue, 13 Aug 2024 01:19:27 GMT  
		Size: 176.2 MB (176221730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d8d53cf1109ec5a445d866dfedccec92ed041c46ab95f88afb686535d74182`  
		Last Modified: Tue, 13 Aug 2024 01:19:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:2c26559135ddedaa24b9a882f0a8777ea5600216432bfb757db1cc294c20e714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701d63266be1bc1375d36b8e99ad184ffa6e8a41022a9406a148552dad64ced2`

```dockerfile
```

-	Layers:
	-	`sha256:944224e730121dd119a4acacb659431153787484706467b471f63058cecc2ae0`  
		Last Modified: Tue, 13 Aug 2024 01:19:24 GMT  
		Size: 2.4 MB (2436724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4aca70433c978123c0723a63c8cff51ffa84b1b6b21cd192bbe1ea49e62bb32`  
		Last Modified: Tue, 13 Aug 2024 01:19:23 GMT  
		Size: 18.2 KB (18192 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:101e6819484e693032933cefcffe246ee12a5f4a790da69555c821e89f566820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212993394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d60347a3386e3c85356c57eeb29c812160d4dda120b10df3f7295b156ea484d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Jun 2024 23:59:16 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Jun 2024 23:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.4-linux-x86_64.tar.gz'; 			sha256='079f61757c3b5b40d2ade052b3cc4816f50f7ef6df668825772562b3746adff1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.4-linux-aarch64.tar.gz'; 			sha256='ae4ae6ade84a103cdf30ce91c8d4035a0ef51c3e2e66f90a0c13abeb4e100fc4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.4-linux-i686.tar.gz'; 			sha256='5771c6032b2be4442f4d4f4fc610eac09a48888ce1f4a41d10208e9d413f5054'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.4-linux-ppc64le.tar.gz'; 			sha256='0703f983894974491715e816a006e0f063966544023f470c94c71ef99dff9dba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191a448ade7364c770870a3eaccbcbe0d914083527dcac9eb1034639054ae3d2`  
		Last Modified: Tue, 13 Aug 2024 07:24:34 GMT  
		Size: 5.5 MB (5535780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c32e962d53dfd9dcb6b48010425af8e8521e98972fbc28d5be4880feca6331`  
		Last Modified: Tue, 13 Aug 2024 07:28:03 GMT  
		Size: 178.3 MB (178300715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fbf5cec6517c6ef753f56581a08863ce5a7ae4c36271ed4084b1030e0668b4`  
		Last Modified: Tue, 13 Aug 2024 07:27:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:ae768786aec61a8f7e62945304eca27dd4e237499c32a4706c8e1a779fbba339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2454481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee49bb2ea158eff7a276f4eb0dbedae61ae3d9bd52de985b90ce91f4d8419d8`

```dockerfile
```

-	Layers:
	-	`sha256:e05aee8e9937ce70d68373dd0c0f2368753c74c29adc6e62a2997edbd2ab1202`  
		Last Modified: Tue, 13 Aug 2024 07:27:59 GMT  
		Size: 2.4 MB (2435930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d27a860388f9a51df843a8fda5ed7e1fe403dfde983dfc29c4135ae487bea0`  
		Last Modified: Tue, 13 Aug 2024 07:27:58 GMT  
		Size: 18.6 KB (18551 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:e4513b2ec3cdc56d96ab4f6b0f975f6a2b47c3c007594a68942aa693e2ecf012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193582002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3101e660f0508896b562117e82c06b9b03aa0e4e0b2f10f791a8a97d4df75c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Jun 2024 23:59:16 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Jun 2024 23:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.4-linux-x86_64.tar.gz'; 			sha256='079f61757c3b5b40d2ade052b3cc4816f50f7ef6df668825772562b3746adff1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.4-linux-aarch64.tar.gz'; 			sha256='ae4ae6ade84a103cdf30ce91c8d4035a0ef51c3e2e66f90a0c13abeb4e100fc4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.4-linux-i686.tar.gz'; 			sha256='5771c6032b2be4442f4d4f4fc610eac09a48888ce1f4a41d10208e9d413f5054'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.4-linux-ppc64le.tar.gz'; 			sha256='0703f983894974491715e816a006e0f063966544023f470c94c71ef99dff9dba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982ba649ab4c4bbb3735a1902cacf92d7e020f36e314d0753d29db1a8d871b36`  
		Last Modified: Tue, 13 Aug 2024 01:19:30 GMT  
		Size: 5.9 MB (5867510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5090e682ee389b6c51102125e49e7bb42b911562252196c574f0acb63ac98758`  
		Last Modified: Tue, 13 Aug 2024 01:19:33 GMT  
		Size: 157.6 MB (157569842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476c06c192cf90a0c2a5e8082f735ab7dff1f84f9fe3d7fa18a7e9534229bcd6`  
		Last Modified: Tue, 13 Aug 2024 01:19:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:5b417e247f3d7b8e9b38a78fe8279bca3d0918db0768c77fc11ee95ec870731f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2451939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5408a05eb429d881c9a66e659ecfd05886f9a2310d82a55ac2e4ef15bf1bb460`

```dockerfile
```

-	Layers:
	-	`sha256:6234779ff74b64bc7545d6553bc5d148e37a8ef92efd56fa3cd6206995cb7104`  
		Last Modified: Tue, 13 Aug 2024 01:19:30 GMT  
		Size: 2.4 MB (2433796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd3e053e17c0d9d019f48d88511497f8043ad6d8eda3da7c9c6919789224d35`  
		Last Modified: Tue, 13 Aug 2024 01:19:30 GMT  
		Size: 18.1 KB (18143 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:c154c65eef00270d5442724ddbfbec05d010e53fb683336781b0f93616c3f9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194499193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada340b633b769fea1870edd5aa0955cc319089b97c0b7476af052ed2e467c9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Jun 2024 23:59:16 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["bash"]
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Jun 2024 23:59:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Jun 2024 23:59:16 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 04 Jun 2024 23:59:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.4-linux-x86_64.tar.gz'; 			sha256='079f61757c3b5b40d2ade052b3cc4816f50f7ef6df668825772562b3746adff1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.4-linux-aarch64.tar.gz'; 			sha256='ae4ae6ade84a103cdf30ce91c8d4035a0ef51c3e2e66f90a0c13abeb4e100fc4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.4-linux-i686.tar.gz'; 			sha256='5771c6032b2be4442f4d4f4fc610eac09a48888ce1f4a41d10208e9d413f5054'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.4-linux-ppc64le.tar.gz'; 			sha256='0703f983894974491715e816a006e0f063966544023f470c94c71ef99dff9dba'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Jun 2024 23:59:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jun 2024 23:59:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27354beb6d5b41cd112e1326b77a495fdad31160ac7aab5c4318874b7448abf`  
		Last Modified: Tue, 13 Aug 2024 06:52:13 GMT  
		Size: 6.2 MB (6245987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc2048dfce1dd660d9804a721cd407a5fb34788010b17948c4d3dbbd4beb5e1`  
		Last Modified: Tue, 13 Aug 2024 06:55:58 GMT  
		Size: 155.1 MB (155130539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1513e5622ba6483619be2986c1bd6a8dcb9608530aba2256ff1412798e0aaf1b`  
		Last Modified: Tue, 13 Aug 2024 06:55:54 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:6c736e17f77044692fece0c975200448847599c849c82317cabc57c5757257b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:349c4fa2b37264490e708d6071dc9bdf00997a1958456cd69cd955c7661eb520`

```dockerfile
```

-	Layers:
	-	`sha256:29885ccea959f3b1b0737b7310408a9b62b7951174bceb80b7af33a79a4ddb13`  
		Last Modified: Tue, 13 Aug 2024 06:55:54 GMT  
		Size: 2.4 MB (2440039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8dc481cb73bfc00eb20cc67a91bc5f7ce7767389fe04bae5e05bb56378584c`  
		Last Modified: Tue, 13 Aug 2024 06:55:54 GMT  
		Size: 18.3 KB (18258 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.20348.2655; amd64

```console
$ docker pull julia@sha256:81b3e34b24c5b78824203d9434253f2d4d6f24db280db27c2f5bedba42dd4acb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329097466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac3f5a0970e9eed03fd5559679c59d336128fcce07dec4cfa3045a4faf18b5a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 13 Aug 2024 20:17:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:17:09 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 13 Aug 2024 20:17:10 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.4-win64.exe
# Tue, 13 Aug 2024 20:17:10 GMT
ENV JULIA_SHA256=c1b659abc90991dcbdf461f33cae483501da736fc223c11d4c51f337338ccb21
# Tue, 13 Aug 2024 20:17:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:17:59 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a091bf53af6b0bb1c322029fb19af7a9ec4417e0c319e9fe64e364c7396fc7`  
		Last Modified: Tue, 13 Aug 2024 20:18:11 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bce9140797cc0ff17923df2abe33eac6040c0d3c3eea10651a5a34bfe7049e1`  
		Last Modified: Tue, 13 Aug 2024 20:18:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6249ddcbad3ab288415f482d58e1227cbec6757cf0cd43dfcdbc88a6dfbf88`  
		Last Modified: Tue, 13 Aug 2024 20:18:09 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00f5dd3f0788d19b1fdd79596027b9d7da44560369e955fdbcc7ebfd6cd6468`  
		Last Modified: Tue, 13 Aug 2024 20:18:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8ce52ac9fd42d51820971281fc567292ffedbb464b1127ce03cba1fbd3b4e6`  
		Last Modified: Tue, 13 Aug 2024 20:18:32 GMT  
		Size: 187.3 MB (187326067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfe855bf3d5a9754151dda491315e2bfb168a133672ff9673b5b447961f4394`  
		Last Modified: Tue, 13 Aug 2024 20:18:09 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.6189; amd64

```console
$ docker pull julia@sha256:2f7b9d7e855a01b053946329b95c1cc8013f3d9f38ff5635890085f5ccf377e9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2432631492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0a9ebd0906f1c10c31b5d7d834e07df5763b423429fb37c495ddd099776842`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:07:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:07:44 GMT
ENV JULIA_VERSION=1.10.4
# Tue, 13 Aug 2024 20:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.4-win64.exe
# Tue, 13 Aug 2024 20:07:47 GMT
ENV JULIA_SHA256=c1b659abc90991dcbdf461f33cae483501da736fc223c11d4c51f337338ccb21
# Tue, 13 Aug 2024 20:09:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:09:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466660ab88f39644bf2424a39259379c6086eb48b2d953dacaf09aaa733b651b`  
		Last Modified: Tue, 13 Aug 2024 20:09:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9a0170b18a1d2902f05f758d754e7fde53b62a0b733a5f2e3871feb0d74416`  
		Last Modified: Tue, 13 Aug 2024 20:09:07 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cc82bf302859215f03f2747b5e3710582e58a8b040fbf54e41cc2a1269e795`  
		Last Modified: Tue, 13 Aug 2024 20:09:07 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7c70c01270ef25ae24ff8b7b09f910de1bd12b9a2079f404f9e081a244e54a`  
		Last Modified: Tue, 13 Aug 2024 20:09:07 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d85cbf1002fb6640e6e56bf81c86b1e3a29c4e0303a79fa707b84b08016126`  
		Last Modified: Tue, 13 Aug 2024 20:09:32 GMT  
		Size: 187.4 MB (187421769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc75a49c3d92e9cb3c5f5d799aecc6d03e5eeeb26bb593f92786869ee28510b`  
		Last Modified: Tue, 13 Aug 2024 20:09:07 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
