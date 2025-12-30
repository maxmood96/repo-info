## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:2634e60c215db5e40daead77c862cd6db94d55478ee53acb13207513e3c96875
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
$ docker pull julia@sha256:91ac0aa799e822cc33b0b7870b78a3f6fe0a1b9591e5796f0939ece4a4bf4e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.6 MB (340626338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705d2b28cf401c9d3c3fd30a2673ab3970315d75eb0929e5710b7e8e0498b3c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:22:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Dec 2025 23:22:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:22:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Dec 2025 23:22:03 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Mon, 29 Dec 2025 23:22:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Dec 2025 23:22:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:22:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:22:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d3afbfba759148c77df641ff03408f7ac1530921d1620d9f906248c2c26434`  
		Last Modified: Mon, 29 Dec 2025 23:23:02 GMT  
		Size: 5.7 MB (5716352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1ab0f5a261d651afb6858072b8a94d8fcd2ef690af22c3090fc41685d881e4`  
		Last Modified: Mon, 29 Dec 2025 23:23:39 GMT  
		Size: 306.7 MB (306681194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadab8563d9d85e9da351e96dc666fe38e7bad18dc88de26e315656a894bfbb5`  
		Last Modified: Mon, 29 Dec 2025 23:23:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:550b0a08b963842cadcfe4b1551fe1d26c25c51e6cc3fe74dfc63a3f7beb3420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a760583c85bf2063d66e65146fe17d7de66af15acaac1d8f97d8136ac3270f3`

```dockerfile
```

-	Layers:
	-	`sha256:1ed2ef6130a0bae02effc161d47a4fc089de1bbd9fc7b0bfadea12d13760348d`  
		Last Modified: Tue, 30 Dec 2025 03:04:04 GMT  
		Size: 2.6 MB (2568616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:484a813fbac6c8cfa498242aedd04126dfad864c74e9aba5938790f969e77c43`  
		Last Modified: Tue, 30 Dec 2025 03:04:04 GMT  
		Size: 16.3 KB (16333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2db92c0368ebd1b3188b74bd8f2656fe843be3c9061d65bc097649f388703fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363349045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ffb43583afa32feb074024ad8e20b96fb5df56b7676a46fc3a3e0ee704266c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:21:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:22:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Dec 2025 23:22:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:22:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Dec 2025 23:22:14 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Mon, 29 Dec 2025 23:22:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Dec 2025 23:22:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:22:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:22:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b7b382d2df6a5ca51c323361ac44c2afce2867dae484d7e2cb383a19287ba1`  
		Last Modified: Mon, 29 Dec 2025 23:23:14 GMT  
		Size: 5.6 MB (5567191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbf9a976d3fd69b9d211adb0bf022c11fda03cf687575283154158159b1dd3f`  
		Last Modified: Mon, 29 Dec 2025 23:23:41 GMT  
		Size: 329.7 MB (329679278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b713b5873eacddb4e1a6ef0ec0463f6b7507eeff05f10373067f5831c648624f`  
		Last Modified: Mon, 29 Dec 2025 23:23:14 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0865247de4425c8514edda51eebfc801e3bf73afecb48d1d3209a1b34daa9ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2585317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66fac243adb054d4aafb7d04143f38a8dc9ed44142655e7f9b931bfed32c3c3f`

```dockerfile
```

-	Layers:
	-	`sha256:aa916ddaafdcc38adcfc3d1a9e8715798a1765d35a004b371e881a7a46f7ae88`  
		Last Modified: Tue, 30 Dec 2025 03:04:08 GMT  
		Size: 2.6 MB (2568879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf6e5ca7703d1bb1fe88f28a7ab71d7e57b135a797efdde2112a9645e6775b3c`  
		Last Modified: Tue, 30 Dec 2025 03:04:09 GMT  
		Size: 16.4 KB (16438 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:6853ff0bb9d1b93c05d432c7e2c645dc260696666a200db7bec2cd26d32982ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277570136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1a5e63d014d6c0b4c2fe692efec7f749ec239b3d2e49ceeddfa2f4408cc944`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 29 Dec 2025 23:17:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:17:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 29 Dec 2025 23:17:11 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Mon, 29 Dec 2025 23:17:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 29 Dec 2025 23:17:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:17:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:17:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611673e0e13442d8c61ca00ad28b00fedf9faf25bc271789ddb5ad885a588f`  
		Last Modified: Mon, 29 Dec 2025 23:17:54 GMT  
		Size: 5.9 MB (5878057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81cd8890a310cf990706f79775298158902e2b8f5118d39b557f0ec3a196420`  
		Last Modified: Mon, 29 Dec 2025 23:18:03 GMT  
		Size: 242.5 MB (242481935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0089aec2359ee5f0c5a9c3bee58a942132bfc916153381c551e9d2edbda8e4`  
		Last Modified: Mon, 29 Dec 2025 23:17:54 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:48548e26dfcfe68b6086c262336d2ae13327452d28ba50bd01f4423b7d11fb54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff21ac28e26e0bf36459909212bf46e28df5dd2ed0c4a0a2ad2923411c1c7ba`

```dockerfile
```

-	Layers:
	-	`sha256:7cd47479d10babe20cb165d110bb98b47564659a50d6c2f92e76563fab477ccd`  
		Last Modified: Tue, 30 Dec 2025 03:04:12 GMT  
		Size: 2.6 MB (2565768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c72094672eabb1728fe4c71bf8e8fed078717b63310c5ec9d110e428f9d3f05b`  
		Last Modified: Tue, 30 Dec 2025 03:04:13 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json
