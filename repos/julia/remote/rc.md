## `julia:rc`

```console
$ docker pull julia@sha256:1592d17fdb266eec4ce6d2b414d5b4a09486a58fe2d4d7e52885991e613ba477
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
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:f18341672c9c8f83f70783a06381d524c4f05a5374989a7845ad8bfcf636b9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291438506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a044be73f770ff65369d984763cf692eceb8180ed7e0360fbd09479e1fb51d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 19 Mar 2024 17:59:39 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["bash"]
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 Mar 2024 17:59:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha2-linux-x86_64.tar.gz'; 			sha256='173044a594847c9d1b2067ae616e9923acf1989d5650f668eedfa7f377edee17'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha2-linux-aarch64.tar.gz'; 			sha256='1727138eae5712d2b51a92428f19304121a7fcf8d298684bfc99c538f56fb609'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha2-linux-i686.tar.gz'; 			sha256='449e4d80b9cf73ffa161cc96c3798404e2d1516f48e2545132f28b0600cf6df8'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha2-linux-ppc64le.tar.gz'; 			sha256='3391afb9fc930b129ccea11e5510e672852e387c4f23d6f12818e605702b1a0f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha2?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82423d3c336d4ef1ce5681f350a8cae438788dfb763c2b35d17d570b4146f59`  
		Last Modified: Wed, 10 Apr 2024 02:54:39 GMT  
		Size: 5.7 MB (5707932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a8960e75f6fbfbbb799927bc6d155b36b85fa57a8f471b6f50c019404c5c58`  
		Last Modified: Wed, 10 Apr 2024 02:54:43 GMT  
		Size: 256.6 MB (256598844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9aee712115f7670901f79e77187c391df6f00c6b788a80cb25a0aaba50d6f0`  
		Last Modified: Wed, 10 Apr 2024 02:54:39 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:de23d7a1bde775d5fd47a67801a1ef894434f6a306e2dc494d3e96e82f34b383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2432895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3239bc0cf4f98c76153d45e2c3f009a9a7c1ecffc692194c99a509053b887e`

```dockerfile
```

-	Layers:
	-	`sha256:72ac24094873e02e94641ca82392029a0bf03fdbc5040678dc4cd1b69d5cfdae`  
		Last Modified: Wed, 10 Apr 2024 02:54:39 GMT  
		Size: 2.4 MB (2413963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ed899ecd83609f9617bd6d95a81fb718896b37d450124f42a937c976ac9a765`  
		Last Modified: Wed, 10 Apr 2024 02:54:39 GMT  
		Size: 18.9 KB (18932 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ccc4798154a59aa7e78b69e596f091f6b45b122c01eaf5ad9e622ea2dbb86d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289971155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5f5ebb373d9ce41d2142484643fae73bd10610db4d5f81d988c48558367b4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 19 Mar 2024 17:59:39 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["bash"]
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 Mar 2024 17:59:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha2-linux-x86_64.tar.gz'; 			sha256='173044a594847c9d1b2067ae616e9923acf1989d5650f668eedfa7f377edee17'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha2-linux-aarch64.tar.gz'; 			sha256='1727138eae5712d2b51a92428f19304121a7fcf8d298684bfc99c538f56fb609'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha2-linux-i686.tar.gz'; 			sha256='449e4d80b9cf73ffa161cc96c3798404e2d1516f48e2545132f28b0600cf6df8'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha2-linux-ppc64le.tar.gz'; 			sha256='3391afb9fc930b129ccea11e5510e672852e387c4f23d6f12818e605702b1a0f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha2?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 17:59:39 GMT
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
	-	`sha256:13c246723c102853ced7b1e4180d0039e68c1e1d5e1176d160ccfdbc9ea42402`  
		Last Modified: Wed, 10 Apr 2024 16:32:11 GMT  
		Size: 255.3 MB (255275483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e39160dd0413a706cf8bfbba0c5d833413f1bb8b3e53503370307682b42eb2`  
		Last Modified: Wed, 10 Apr 2024 16:32:05 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:c92b1b33a46eecee07d4446e59e66dfdb2f64079a49607c37c3878d819249f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2432977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e2b5e9b9997bd21c0497696b85c5a3f34777bcff422d3d34afc4ddc1e5f217`

```dockerfile
```

-	Layers:
	-	`sha256:c128cf3838026d329732b1a6e2a503aaa4022cb4df1fe001d65886b5ac1e8283`  
		Last Modified: Wed, 10 Apr 2024 16:32:06 GMT  
		Size: 2.4 MB (2414196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d37dbc38952433128987f8d2319481114e6bc2ce17febefa8c6591ee70c04a5`  
		Last Modified: Wed, 10 Apr 2024 16:32:05 GMT  
		Size: 18.8 KB (18781 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:94c926d6cc73a3336133b60e288b40e24b137d0d0f8ac3acc9b797333557a2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270449729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b959c6db34d6eea14c98689a9a5a20e1bba87ae761e449504e502da7e6c53121`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 19 Mar 2024 17:59:39 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["bash"]
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 Mar 2024 17:59:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha2-linux-x86_64.tar.gz'; 			sha256='173044a594847c9d1b2067ae616e9923acf1989d5650f668eedfa7f377edee17'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha2-linux-aarch64.tar.gz'; 			sha256='1727138eae5712d2b51a92428f19304121a7fcf8d298684bfc99c538f56fb609'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha2-linux-i686.tar.gz'; 			sha256='449e4d80b9cf73ffa161cc96c3798404e2d1516f48e2545132f28b0600cf6df8'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha2-linux-ppc64le.tar.gz'; 			sha256='3391afb9fc930b129ccea11e5510e672852e387c4f23d6f12818e605702b1a0f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha2?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de2ccf6b9ce9ee0a74c37ce093c694512c6869f8201be7dd721fcb69d3f9045`  
		Last Modified: Wed, 10 Apr 2024 01:53:12 GMT  
		Size: 5.9 MB (5863290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ae643478342c1c28823ffdff368569c4fabd40999d53ce7e8ef94781be8383`  
		Last Modified: Wed, 10 Apr 2024 01:53:17 GMT  
		Size: 234.4 MB (234439552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a63e4728ce90de2c891f0b2b80b51013ca4436ece030c860e550c8982c5416`  
		Last Modified: Wed, 10 Apr 2024 01:53:12 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:9b25a69052570e98e935ab42dfe7550175d3b7ed8e6288d582ffc2062b9149ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2429938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e0c8022fde45bfce744acb07c67adb7c2117684d99f15a6cf062e0c7f690b3`

```dockerfile
```

-	Layers:
	-	`sha256:d9a6b047a74a3629a6ba0c9d14c2f0bb5804a7aba331c622c96c4930980a3235`  
		Last Modified: Wed, 10 Apr 2024 01:53:12 GMT  
		Size: 2.4 MB (2411045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b23a552f09952db7586c4383896a93fa89b38a774fa5b846efa03d1b21ea96`  
		Last Modified: Wed, 10 Apr 2024 01:53:11 GMT  
		Size: 18.9 KB (18893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; ppc64le

```console
$ docker pull julia@sha256:5c5610566259355102314f365937ff00e8dcd65f3afa7d80be87c73da7ffb3c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283682915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0b7df4ad12ae38e4c6f7e9dcba6fc06aaeaa5adfecad68ddf7da00ce39dc46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 19 Mar 2024 17:59:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 19 Mar 2024 17:59:39 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 19 Mar 2024 17:59:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.0-alpha2-linux-x86_64.tar.gz'; 			sha256='173044a594847c9d1b2067ae616e9923acf1989d5650f668eedfa7f377edee17'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.0-alpha2-linux-aarch64.tar.gz'; 			sha256='1727138eae5712d2b51a92428f19304121a7fcf8d298684bfc99c538f56fb609'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.0-alpha2-linux-i686.tar.gz'; 			sha256='449e4d80b9cf73ffa161cc96c3798404e2d1516f48e2545132f28b0600cf6df8'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.0-alpha2-linux-ppc64le.tar.gz'; 			sha256='3391afb9fc930b129ccea11e5510e672852e387c4f23d6f12818e605702b1a0f'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version; 		echo '{"spdxVersion":"SPDX-2.3","SPDXID":"SPDXRef-DOCUMENT","name":"julia-sbom","packages":[{"name":"julia","versionInfo":"1.11.0-alpha2","SPDXID":"SPDXRef-Package--julia","externalRefs":[{"referenceCategory":"PACKAGE-MANAGER","referenceType":"purl","referenceLocator":"pkg:generic/julia@1.11.0-alpha2?os_name=debian&os_version=bookworm"}],"licenseDeclared":"MIT"}]}' > $JULIA_PATH/julia.spdx.json; # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 17:59:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 17:59:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343ac94481c1fce7acc63eef8340c59008fd662b7dd35e8c8e83c4b0b5ae7208`  
		Last Modified: Tue, 19 Mar 2024 23:11:59 GMT  
		Size: 6.2 MB (6239922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1deffa9a0119bb8f3b97eda677569cc3fa449f93da70c4a6c3fd5d829b147e7`  
		Last Modified: Tue, 19 Mar 2024 23:12:05 GMT  
		Size: 244.3 MB (244323602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93c82a4c4dd39308065a8281b8dbe8938c704e7f4487e397c0cee08ec5948cf`  
		Last Modified: Tue, 19 Mar 2024 23:11:58 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:170316ef83f99cf5f395f1e4cd6768e4d9cbad058f0ba783b10a0f98c55ea61d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48ed189bfca45f8933b0d57a2ffc2cbd7d88ea99a0a7a2507f5493aa49f68c9`

```dockerfile
```

-	Layers:
	-	`sha256:97e48039a84e7f20a3618b7a37f6b2c86ec8e10311d0d5ef3455d9ddc8136f53`  
		Last Modified: Tue, 19 Mar 2024 23:11:59 GMT  
		Size: 2.5 MB (2469297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53518a7566681752877918db7647ca5b0e427aadc5d9f89b3c4c132279d9e5fe`  
		Last Modified: Tue, 19 Mar 2024 23:11:58 GMT  
		Size: 19.0 KB (18986 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.20348.2402; amd64

```console
$ docker pull julia@sha256:c88e20d5b96948a1701b3e66c312b8a8239a07ccbec5ae116f69c57dff9ca10e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251410968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10850422c60f90e030d20f6920b2733b80a398b2a969361eeb4a362e936ce0ab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:59:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Apr 2024 23:59:02 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 09 Apr 2024 23:59:03 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-alpha2-win64.exe
# Tue, 09 Apr 2024 23:59:03 GMT
ENV JULIA_SHA256=acfbe50c378e3e0d6dc967525b5886edd5ae61ef3de85130343db378dfe88b0d
# Wed, 10 Apr 2024 00:00:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:00:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fb179a3d784ee6d4ee555ce2c9dbeb19de4a69c8146bd605283788491857d5`  
		Last Modified: Wed, 10 Apr 2024 00:00:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31699d5271eff157c95c94e14cc49b4600db1b860462c91dfcaddbfde663e4f8`  
		Last Modified: Wed, 10 Apr 2024 00:00:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82746ae8de4daa8e3f6aa1e7f409e969875d112d4a4edccaf6c29969606ec78e`  
		Last Modified: Wed, 10 Apr 2024 00:00:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98787512b898e7eeb7c7c7d02cd4410839cf296247a34a4e36b30874eac9ec69`  
		Last Modified: Wed, 10 Apr 2024 00:00:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347bb455d9d3442fec2a6415a7f32b4f3d26e4a1e6e5b694403cebc3e193e701`  
		Last Modified: Wed, 10 Apr 2024 00:00:50 GMT  
		Size: 252.0 MB (252030847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97ea9ab392191910f516e7d972257dea92f14bfb8296499788b0181ba6a7829`  
		Last Modified: Wed, 10 Apr 2024 00:00:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.17763.5696; amd64

```console
$ docker pull julia@sha256:6df7cc0d4116fe4f16ab39179759d0953e56ed163fdf7372f68b31b4405aaa92
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2416464646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba79f473b5131a0d7dfa858d245dce4f5d5a96f38ebe8862d70b0b565877c7d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 00:55:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 00:55:19 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Wed, 10 Apr 2024 00:55:20 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-alpha2-win64.exe
# Wed, 10 Apr 2024 00:55:20 GMT
ENV JULIA_SHA256=acfbe50c378e3e0d6dc967525b5886edd5ae61ef3de85130343db378dfe88b0d
# Wed, 10 Apr 2024 00:56:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:56:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01996b75daca9937cc4f047e71070c0c8625ae42c5d0a15e9f98c7d406ce065e`  
		Last Modified: Wed, 10 Apr 2024 00:56:43 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b357db38a2d0db89ac0fda0890ad54f2f03cf035024d8db62d465de952ce84`  
		Last Modified: Wed, 10 Apr 2024 00:56:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5071f66ce897fd65bc28348c48dd2d1eb2bf47f657c04a806ee3d60670f93f`  
		Last Modified: Wed, 10 Apr 2024 00:56:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ca619f378c0350c2532f26fe3e9214eec71d7fb57794bb125e63c12252deaa`  
		Last Modified: Wed, 10 Apr 2024 00:56:41 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b01c0be6fa2d4e86c449f0d3663d82398c7828fa316ba288092c5944ef29cd`  
		Last Modified: Wed, 10 Apr 2024 00:57:13 GMT  
		Size: 252.0 MB (252030201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9be0d6a03c04824c56861d42a45705568a6cd00d9954e57b7a9f8e6555b478`  
		Last Modified: Wed, 10 Apr 2024 00:56:41 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
