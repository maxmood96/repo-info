## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:5fc7d4173c60430d0d8a5804bbce6004a463c1a722b957b237bbe513da7f6a20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:rc-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:6b624a9a9f0f373de48cb4d3fb931fcc1743b181583406db1da98b4a11af97fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340626277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef605dac46beb2542e122a9fc8053b7bfa01cfd25e9a5c2729fe01fa11316b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Sat, 06 Dec 2025 01:09:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 01:09:56 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 06 Dec 2025 01:09:56 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 01:09:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 06 Dec 2025 01:09:56 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Sat, 06 Dec 2025 01:09:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 06 Dec 2025 01:09:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Dec 2025 01:09:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Dec 2025 01:09:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2a9f2d35ca86448abc9baf32f52227d842a6c20501ab2f0efcdf037f3c2f49`  
		Last Modified: Sat, 06 Dec 2025 01:10:54 GMT  
		Size: 5.7 MB (5716357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd77f517b297f34dfb2bd4cb3eb5e44e12e07fd78161c175ec59557e8dc9173`  
		Last Modified: Sat, 06 Dec 2025 01:11:08 GMT  
		Size: 306.7 MB (306681100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb33c3a8c6de1c917980ec0bf58e21351992b801caeda347da9b2d166a0bccf`  
		Last Modified: Sat, 06 Dec 2025 01:10:52 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:96042806fb603134e46c6be4e7d9098cc4fbe4bb30feea6a5b28feecaf45a365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4efcfdea37d0be503c1634af418c1daf69537813814c4acdf6693cad21b0b8`

```dockerfile
```

-	Layers:
	-	`sha256:34312a460bf721618faa9e55b40ba782fe9b6c53756bdac976e8e4d0a836ee84`  
		Last Modified: Sat, 06 Dec 2025 03:04:49 GMT  
		Size: 2.6 MB (2568616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fef876dca673e0df128e78788de3527bd34b48e699f95ba258402dc59208c058`  
		Last Modified: Sat, 06 Dec 2025 03:04:50 GMT  
		Size: 16.3 KB (16333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:118cdb4597390c0a7a093ded9f267f5ef11980813e805a0e1f3b76f450324092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363348867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841a6fb8c9ed24672bcac6ca566b2f4f46fc5cbacbf88ea366eea6e4d81fcdf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Sat, 06 Dec 2025 01:08:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 01:09:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 06 Dec 2025 01:09:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 01:09:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 06 Dec 2025 01:09:11 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Sat, 06 Dec 2025 01:09:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 06 Dec 2025 01:09:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Dec 2025 01:09:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Dec 2025 01:09:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ce9dbe444e503b4a235051b121c6457a416c4902495bbbe27eaac64e1c1624`  
		Last Modified: Sat, 06 Dec 2025 01:10:15 GMT  
		Size: 5.6 MB (5567096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebe8e5456b4c9c180dad2f29cd0077f904946e5297bfbc0b5c5ccc86a69afc7`  
		Last Modified: Sat, 06 Dec 2025 01:12:16 GMT  
		Size: 329.7 MB (329679196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d081a8779efca2d08d646e298531a8f76b2cf88ad900bdc7b6c54b67a45e68c0`  
		Last Modified: Sat, 06 Dec 2025 01:10:14 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:09b6406d832acb074c2c74adb011aa461bdcac4a80c19b665de0916324e152de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2585319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea1c61f16165452b13693611de16f64142f2f3bb79b5b0fb8c82d10b0cfe5c8`

```dockerfile
```

-	Layers:
	-	`sha256:149f190630bc18208b9377dd960cc0c37150a28e354031d481448d438b52d6ad`  
		Last Modified: Sat, 06 Dec 2025 03:04:53 GMT  
		Size: 2.6 MB (2568879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2e072c8e35dd9fd5fd94a5d64f30c20321f7888144154ab8c45255e42b9410`  
		Last Modified: Sat, 06 Dec 2025 03:04:54 GMT  
		Size: 16.4 KB (16440 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:0080c692da8f6d177e836f98afff9e7907783296fa2eaf7d97b99b981a8ea18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277569991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a5caaf38724ae2a07be17f3873157019929a59603ad3c61e93009b3d9774d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Sat, 06 Dec 2025 01:09:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 06 Dec 2025 01:09:55 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 06 Dec 2025 01:09:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Dec 2025 01:09:55 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 06 Dec 2025 01:09:55 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Sat, 06 Dec 2025 01:09:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 06 Dec 2025 01:09:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 06 Dec 2025 01:09:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 06 Dec 2025 01:09:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720935d1d8bd99976aa3b3a217e83ca810b8e65e34bde583d4d07555cfcd172f`  
		Last Modified: Sat, 06 Dec 2025 01:10:43 GMT  
		Size: 5.9 MB (5877969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1249661240b21524b3192b600538c1094c62228abca0542111ede03541033f9`  
		Last Modified: Sat, 06 Dec 2025 01:10:51 GMT  
		Size: 242.5 MB (242481946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91f6753a5c8d6fcb1272692c4d59bd42ca36aac190cc6accfa5839001072aaa`  
		Last Modified: Sat, 06 Dec 2025 01:10:43 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:45437dc57f72edc2ea0b84a3a8eefe33c4e7572ed538e34b16be3aec327f172c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46880ec21e53706a0e7815224058237b9f8274788b99acc15cb7c51278970f5d`

```dockerfile
```

-	Layers:
	-	`sha256:ad14b6455375e3e6c462e50d4c4b20e7a5f871ab7ec3c42d51f4c46007e2d602`  
		Last Modified: Sat, 06 Dec 2025 03:04:58 GMT  
		Size: 2.6 MB (2565768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fedda950a4f552be5468e446b2940dd19abec5fa1c970ff6e6ca18bbf2eafe4a`  
		Last Modified: Sat, 06 Dec 2025 03:04:58 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json
