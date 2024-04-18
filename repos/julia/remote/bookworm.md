## `julia:bookworm`

```console
$ docker pull julia@sha256:986f430ddf5bf3b7e3160672eb2b070647f2e72b8f6a50eb900151c1fc3694a8
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
$ docker pull julia@sha256:9e937d5a591b59f2680e7c5d665bf96ad80029034f22638564ae59ad52b472b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (206967577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aca897d526d5f48d74110f50b3d01e7eee8a085cc22d562930145e1ab3e3558`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 02 Mar 2024 06:59:15 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["bash"]
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 02 Mar 2024 06:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_VERSION=1.10.2
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.2-linux-x86_64.tar.gz'; 			sha256='51bccc9bb245197f24e6b2394e6aa69c0dc1e41b4e300b796e17da34ef64db1e'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.2-linux-aarch64.tar.gz'; 			sha256='f319ff2812bece0918cb9ea6e0df54cc9412fc5ef8c0589b6a4fea485c07535d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.2-linux-i686.tar.gz'; 			sha256='1699988a1733375991937b78689339e8b8117fb0a1700b54a2c984829ce646e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.2?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4a1f2b195a932b9feddd23375a2334f035bbd9e3e6140319c4e23bb4ca234d`  
		Last Modified: Wed, 10 Apr 2024 02:57:47 GMT  
		Size: 5.7 MB (5707926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61762abcc2eefd0073b905ffba82393755040d9720b4e6fab79e9dae14aba819`  
		Last Modified: Wed, 10 Apr 2024 02:57:51 GMT  
		Size: 172.1 MB (172127921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd9f29f87effc698371c4993ae689ba9513e270a0bd9a9a54b68655e9872b5`  
		Last Modified: Wed, 10 Apr 2024 02:57:47 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f7c15532c82211a4263a98433708995b13e9679b0198598d6502e093ce767d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2434183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f3b17204299116f4c54fed625e98c52e726d9c3f10436ff52f6507ce66d8bf`

```dockerfile
```

-	Layers:
	-	`sha256:6774f3bea320a5a6545a768a1b31b8f222a978e6dff30319aa036db610ad8a0d`  
		Last Modified: Wed, 10 Apr 2024 02:57:47 GMT  
		Size: 2.4 MB (2415474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88461d4335ef4b7fa35afa911294710276882a2d17dc3b1f94846936ffba00a3`  
		Last Modified: Wed, 10 Apr 2024 02:57:47 GMT  
		Size: 18.7 KB (18709 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:28d3eff37bd3f60d064b036b7a6db127caa95abf9ba3644abbe0274e36b2b53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200599130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5763a12e038fd639e78cb3ed723c616b993e71acac3644034b895be09cf55524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 02 Mar 2024 06:59:15 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["bash"]
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 02 Mar 2024 06:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_VERSION=1.10.2
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.2-linux-x86_64.tar.gz'; 			sha256='51bccc9bb245197f24e6b2394e6aa69c0dc1e41b4e300b796e17da34ef64db1e'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.2-linux-aarch64.tar.gz'; 			sha256='f319ff2812bece0918cb9ea6e0df54cc9412fc5ef8c0589b6a4fea485c07535d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.2-linux-i686.tar.gz'; 			sha256='1699988a1733375991937b78689339e8b8117fb0a1700b54a2c984829ce646e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.2?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc2a70945b18a18ecc7929c1ec341812e2cdf8cdb6e7ba2322ae016299fff27`  
		Last Modified: Wed, 10 Apr 2024 16:32:06 GMT  
		Size: 5.5 MB (5533142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c5db653e05760c65c2aac360e8a081b8c1dfb78f1db509a1292438313ebce6`  
		Last Modified: Wed, 10 Apr 2024 16:34:59 GMT  
		Size: 165.9 MB (165903460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d0fcebf619f6a01c3d9963b6779b7270f4aca9ab9e82a1c0412e48d604f09b`  
		Last Modified: Wed, 10 Apr 2024 16:34:54 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3f81e079079c790598b1a7504f6c8272c66717511daee3d58aacd2b66ec2c97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2433299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d198d1cffa4c84c623b8df7c1e492c5d36325bc176fee6ede13db80e07f1ce`

```dockerfile
```

-	Layers:
	-	`sha256:f864b46b2c13b949c7d789171faaf09a6db79a89c8b6ec9e6baf3c6ac823f0cd`  
		Last Modified: Wed, 10 Apr 2024 16:34:54 GMT  
		Size: 2.4 MB (2414738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0144b0d5cfdd10495aa9bf8fce185f12dd435b72b3790ae11a30d7c06b579efc`  
		Last Modified: Wed, 10 Apr 2024 16:34:54 GMT  
		Size: 18.6 KB (18561 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:9422f09e7ae9de06dda06e85147bbad4ed496d1f3f272446947f7656d404c3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192410544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dedf6cb4a097c21e91c5b00986e5918915e5b4b8f213b814209f1c5a2c35f63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 02 Mar 2024 06:59:15 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["bash"]
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 02 Mar 2024 06:59:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 02 Mar 2024 06:59:15 GMT
ENV JULIA_VERSION=1.10.2
# Sat, 02 Mar 2024 06:59:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.2-linux-x86_64.tar.gz'; 			sha256='51bccc9bb245197f24e6b2394e6aa69c0dc1e41b4e300b796e17da34ef64db1e'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.2-linux-aarch64.tar.gz'; 			sha256='f319ff2812bece0918cb9ea6e0df54cc9412fc5ef8c0589b6a4fea485c07535d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.2-linux-i686.tar.gz'; 			sha256='1699988a1733375991937b78689339e8b8117fb0a1700b54a2c984829ce646e6'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.10.2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.10.2?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 02 Mar 2024 06:59:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Mar 2024 06:59:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289ba105e3681a84c72370bd6f4b90b1996473c33384f99da7bfd64c2956f747`  
		Last Modified: Wed, 10 Apr 2024 01:52:34 GMT  
		Size: 5.9 MB (5863288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b10957108b1376ec668d8bfdd9d54494190f5c4fd1e43dc6f36cb8cbfbb3b5d`  
		Last Modified: Wed, 10 Apr 2024 01:52:37 GMT  
		Size: 156.4 MB (156400369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3f654de2b9c8cb7ad72b1b8315c98764e54da94e816818991dc85fc0f20739`  
		Last Modified: Wed, 10 Apr 2024 01:52:33 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0585cca84e94ec7f2e286fab256cfa0ba1779394ce241fbb620f75dc9e1ff889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2431205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0f1bd2596812b2e13b1e4abf15e606a84020848ad10d0646d08521a817298f`

```dockerfile
```

-	Layers:
	-	`sha256:b88933c987fe95c0c8446d40c0edec03f09efd029af130341f6d473b85f9a244`  
		Last Modified: Wed, 10 Apr 2024 01:52:33 GMT  
		Size: 2.4 MB (2412546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29b2b0354448a0c35cfb56907db6928f8948d5b6e244528aa0d41442d7a62c1c`  
		Last Modified: Wed, 10 Apr 2024 01:52:33 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json
