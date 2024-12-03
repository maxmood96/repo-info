## `julia:1-bullseye`

```console
$ docker pull julia@sha256:9ad976e364edc34edd72583734a234e66013f7c895fc1bc9c8248b59592ecd29
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
$ docker pull julia@sha256:e21ad0137c8b8a15b07d3f6195f181369084e6886674d03d719466e1b8e693b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289573975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b283efac7b94defa0b6bf2d95465edbfa72c96aa45afe84530634df90f493a72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cf17a4a247bda6618c4fd4a5e2f697d84b4575bbcbf5eed6aec8b9683260fa`  
		Last Modified: Tue, 03 Dec 2024 02:17:38 GMT  
		Size: 2.2 MB (2222690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2f3196fc55c0e1e266503f136dee778f9b3fb1a1b7543173ba25f340eed634`  
		Last Modified: Tue, 03 Dec 2024 02:17:44 GMT  
		Size: 257.1 MB (257098268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11c3c7d35a020e8396741424315667aa7faa7a2ca25960cc125143b9abe43d1`  
		Last Modified: Tue, 03 Dec 2024 02:17:37 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:71390e2a136bad7f3e40597957def443cd71973d3311409ab6d4a6549dfaa6ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c1127c7065175fb5bca231291874782eb785033aa605ae403ef16fa16d3586`

```dockerfile
```

-	Layers:
	-	`sha256:1d374a3dba343ba78f019fa976918d8e81b3b75e469edfb85cc0aaf1875c1128`  
		Last Modified: Tue, 03 Dec 2024 02:17:38 GMT  
		Size: 2.7 MB (2715160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e8dd6d13c2a59f9838ab75ab90af9396914516dedbb45330ee63f7c2d7b8442`  
		Last Modified: Tue, 03 Dec 2024 02:17:37 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f798c57648a0e9839faed7b80605afe746f10e91233bd9c8d56323833473f113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (284962256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8bac96e1f5e359fb62d7ea7ea96350af77e69578b892ddc739b837d4fd7dc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05013aee803e8b2dbaba9b0e035ac677b45e05e9bd51464de0ddc85524fba13d`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 2.2 MB (2210292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ecb8ff42f5d159e95271acfe6754860a7e5caa81f142e067200dd251f84166`  
		Last Modified: Tue, 03 Dec 2024 02:51:29 GMT  
		Size: 254.0 MB (254006669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603847c85db951da72dc623ab26bfa0d8b611f3c6000045ee8aec29142e4084e`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2ae870ab0aa4cd721b585fd780c47adba288682908c90fd92712ea9066906d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2732771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a711dd34c6db70375fac74699c4537d82afccb7009df2ecd59365e9c0fc3a9a6`

```dockerfile
```

-	Layers:
	-	`sha256:422a95300688a576bcbcbffd8a35fc6ddaeda8dd68da465003ee23070526ca61`  
		Last Modified: Tue, 03 Dec 2024 02:51:24 GMT  
		Size: 2.7 MB (2715422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c1a191ece5d050addd22e2bcd4b95df69c526f26db24f10570c867801c775e0`  
		Last Modified: Tue, 03 Dec 2024 02:51:23 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:b8c5e00251f9072e18e6056341881292bda3ac7500641b86ea9b162f8ce1db9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268166047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57d4abd1e50829e2dc8e48cdba72d41ceb67b43b3741bfdc515f360389b2dea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac99d6f64ac9099c145ee3db62bcfb8030850642fcdaa4429e523d6dc8fd80`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 2.3 MB (2328053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945d157d5a761800b63ba98bdc82e9dcf56f24fc61b6df22284c10440f8a9e80`  
		Last Modified: Tue, 03 Dec 2024 02:15:06 GMT  
		Size: 234.7 MB (234658568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d7d4ace25cdb8d2c5af7784bbf5625e038a9aa4e5b4ca90923f419010e1865`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:91263673457c8bc3c6a544d8083a5a7c3cd1c0dd296375da915012199187e637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecac8533b702416bddd428020d4c57838b9e633eff9c177f36aeddfa3e0d6c5`

```dockerfile
```

-	Layers:
	-	`sha256:2475be50377543347fcc684091713d6f8f1dd527b1e6eb8e5583d6e2c1928b81`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 2.7 MB (2712258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8835e1f2292911817cb16e50f7a082b1766f67c8fca1808216394d3b54ff92da`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json
