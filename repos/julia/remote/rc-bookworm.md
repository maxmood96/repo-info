## `julia:rc-bookworm`

```console
$ docker pull julia@sha256:bcca4891b69a27c4aeaf4041d90a02cbd48c1dafb9eb3f1efaf3961930d6cce1
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
$ docker pull julia@sha256:14140db8b8b7d98beae0dd102b0c01da567a617fc70373f7ee55137d68d57c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.3 MB (343330778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f5d2dc0d082d7858fe15519a187846bae8057259c9484d5144748b569b6eaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:23:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 11 Jun 2026 00:23:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:23:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 11 Jun 2026 00:23:15 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Thu, 11 Jun 2026 00:23:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 11 Jun 2026 00:23:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231f6f751002c8b29aaa1cbdcb0514bfc5d4178512adf0b7ac4f4051ad2b5c86`  
		Last Modified: Thu, 11 Jun 2026 00:23:59 GMT  
		Size: 5.7 MB (5721495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dcfc3ebcbf7ac1b013076eb365fcf844ca2ba96e573e2b06fbcde7e09fedfc`  
		Last Modified: Thu, 11 Jun 2026 00:24:05 GMT  
		Size: 309.4 MB (309371290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e68e8f7a8a0f62d8bbfe99b72ffe5e233ac35694cb939af00fae043eb5e065`  
		Last Modified: Thu, 11 Jun 2026 00:23:58 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:ffeaee0188bdc74932b082d7efa3c4747d5d97a11b94fa41f76354e57b26a3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4961daa3c80adbf49f2dc852304031a994daa36a6ec4791b6ee72ac1283bb3`

```dockerfile
```

-	Layers:
	-	`sha256:ba346f00f761f24c24c286729a88a3e55dd3d3015dc48891f984b906b7f9c412`  
		Last Modified: Thu, 11 Jun 2026 00:23:59 GMT  
		Size: 2.6 MB (2568656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a9ff903a14a98d1443c8417a1e7a53ddb0b07166103752213ae1d7d55ffadf`  
		Last Modified: Thu, 11 Jun 2026 00:23:58 GMT  
		Size: 16.3 KB (16295 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:5f0aa560aa03bf8cfd47624f9fe5f7ccfb1b981c8c8abe8102c5360ca60040d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.5 MB (367456053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd049d2034da0eeb66b32da44fea46592ff27e0f6e6b2bc077b0090967c1fbbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:23:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 11 Jun 2026 00:23:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:23:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 11 Jun 2026 00:23:28 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Thu, 11 Jun 2026 00:23:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 11 Jun 2026 00:23:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:23:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636e782a5a38cfb07fa9ee06cb54d7c313ac4b35f1c84c8baf95a78c013f9cb8`  
		Last Modified: Thu, 11 Jun 2026 00:24:15 GMT  
		Size: 5.6 MB (5570441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61dd3e321c4f3e1d2f1a4d9ae45a8e92165dad5a91a2a47b09e4a2b6d346533`  
		Last Modified: Thu, 11 Jun 2026 00:24:22 GMT  
		Size: 333.8 MB (333762936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbba81f691b42b1b32100a677a4c9dc15106a68197fe81ce1c22e0bf4b65aab`  
		Last Modified: Thu, 11 Jun 2026 00:24:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:db352f38722dc498dc84a8be51d38dfb21f8582c67efb6b502b59d09acdc6cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2585320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a360f33fec64ec9713b944c5ec3bf2a94ed9e26a3dac25f93f999679b3f8ff8`

```dockerfile
```

-	Layers:
	-	`sha256:1f7c0474ca6341244e787dadfd33cae6ba7864457bbdf005d0ccd04ab017018a`  
		Last Modified: Thu, 11 Jun 2026 00:24:15 GMT  
		Size: 2.6 MB (2568919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a67059f7b263605c28aba687526978a953fae705e712e38ece9ff360790cc3`  
		Last Modified: Thu, 11 Jun 2026 00:24:15 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc-bookworm` - linux; 386

```console
$ docker pull julia@sha256:3ec0fe87eb9924d2c7331a4fcd09075d21d1da61accbd0cbf728ec051468df04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278403921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821074ca9ebf3ba03ac56f8038ebda0942308c6a1487b0ab484d77c3c24f2c46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:15:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:15:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 11 Jun 2026 00:15:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:15:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 11 Jun 2026 00:15:49 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Thu, 11 Jun 2026 00:15:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 11 Jun 2026 00:15:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:15:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:15:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:707460b758530d4476f3fefff30544db7cf8dbd98838ccc3533bc05e79016be4`  
		Last Modified: Wed, 10 Jun 2026 23:40:00 GMT  
		Size: 29.2 MB (29225762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ddb4e08c7cbdde9e4eea357acb6454c73609e3d8db53baac10e438bcbb6081`  
		Last Modified: Thu, 11 Jun 2026 00:16:25 GMT  
		Size: 5.9 MB (5880025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb8ae7cb443d30369f76d21bd614ec1371d1ef7a3a724882f6ce699de892f0d`  
		Last Modified: Thu, 11 Jun 2026 00:16:33 GMT  
		Size: 243.3 MB (243297763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97200373e577681c036c0e9a5cd84d16c53087a043fb655dc26948c43635a3bf`  
		Last Modified: Thu, 11 Jun 2026 00:16:24 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:07a5cf9b4b175e712db266d6abb0dc67423a1990693260fef92ea939fe608744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863752e400ff62b0ede802d2ff000641d39c955065321540cb48241b189bff79`

```dockerfile
```

-	Layers:
	-	`sha256:41dec9b1c800aa3dff14f112ead7c452324b03e5106b8cec7c5adda80abcdec7`  
		Last Modified: Thu, 11 Jun 2026 00:16:25 GMT  
		Size: 2.6 MB (2565808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c921f3ae977dd146dbf25786c8ad9c087f254927c16704a3f8b8a2812a6d1484`  
		Last Modified: Thu, 11 Jun 2026 00:16:24 GMT  
		Size: 16.3 KB (16266 bytes)  
		MIME: application/vnd.in-toto+json
